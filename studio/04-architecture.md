# PEYT Chat 技术架构

## 核心通信架构

这是 PEYT 最有特色的一部分。

我们没有采用 WebXDC「应用跟着消息走」，而采用：**应用固定在客户端，消息只同步数据变化。**

```
PEYT Client

聊天
投票
卡片
待办
频道
未来功能

        ↓

PEYT Event

        ↓

Delta Chat Core

        ↓

Chatmail
```

### 核心思想

Chatmail 不存储 PEYT 数据。Chatmail 只是**安全传输层**，不是**权威数据库**。真正数据存在客户端。

## Event 模型

不发送「整个状态」，而发送「状态变化事件」。

例如：创建投票 `poll.create`；投票 `poll.vote`；修改 `poll.update`。

每个事件包含：

```
event_id
entity_id
type
payload
```

其中 `event_id` 是一次操作的唯一 ID，`entity_id` 是对象 ID，两者区分。

## Event Sourcing 思想

PEYT 采用类似 Git / Event Sourcing 的思想。

核心：事件是真实事实，数据库只是事件产生的结果。

```
Event Store

      ↓ replay

当前状态

      ↓

数据库
```

如果数据库损坏，理论上可以重新播放事件，恢复状态。

## 版本兼容理念

PEYT Event 带 schema version。例如旧 `card.update v1` → 新 `card.update v2`。

* 历史事件不修改，通过 migration 兼容未来；
* 未知事件不会丢弃。例如新功能 `project.archive`，旧客户端收到后保存，等待未来解析。

---

## 信封协议落地现状（截至 2026-08-04）

`[PEYT]` 信封协议已实现**发送端**（`src-tauri/src/envelope.rs`）：

```
[PEYT]{
  "version": 1,
  "type": "card.create",
  "id": "<uuid>",          // 发送端幂等键，防重试/多端重复处理
  "timestamp": <unix_ts>,  // 发送端单调时钟，冲突消解
  "from": { "app":"peyt", "ver":"...", "kind":"desktop" },
  "payload": { ... }
}
```

字段与上文 Event 模型**存在演进**：

* 原：`event_id` / `entity_id` / `type` / `payload`
* 现：`version` / `type` / `id`(uuid) / `timestamp` / `from` / `payload`

其中 `id` 承担幂等键（防重复处理），`timestamp` 承担冲突消解。

现状（重要）：

* **接收端目前不解析 `[PEYT]` 信封**，信封消息原样渲染为普通消息（方便调试）；
* 卡片跨设备同步**实际走 `[CARD]` 前缀消息**（`[CARD]{...}` JSON），不是 `[PEYT]`；
* 架构愿景（Event Sourcing、版本兼容）正在分阶段落地：先让同步可用（`[CARD]`），再演进到通用信封协议（`[PEYT]`）。
