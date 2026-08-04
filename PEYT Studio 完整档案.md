# PEYT Studio 完整档案

> 本档案为 PEYT Studio 工作室官方档案，由工作室成员共同维护。
> 首版整理：TiantianYZJ 于 2026 年。
> 最后更新：2026-08-04。

---

## 一、基本信息

**名称：**
PEYT Studio

**全称：**
PleaseEnterYourText Studio（请输入文本工作室）

**Slogan：**
Type Everything

**Logo：**
黑白极简开发者风格 Logo：

```
>
_
```

视觉元素来源于：

* Terminal 命令提示符；
* 代码符号；
* 输入光标；
* 开发者文化。

整体传递：
输入、创造、编程、表达。

---

## 二、成立背景

PEYT 并不是传统意义上的创业团队，而是由一次技术研学活动发展而来。

**起源**
地点：
深圳

活动：
AIx脑科学研学活动

最初成员：

* TiantianYZJ
* NoWint
* SUKY
* chenmuyun_bit

四人在活动期间组成研学小组。

在 5 天的共同经历中：

* 一起实验探究；
* 一起完成汇报；
* 一起讨论 AI 与技术；
* 建立了较强的团队关系。

活动结束后，成员不希望彼此断开联系，因此决定继续合作。

最终：
一个研学小组 → 一个长期技术工作室

PEYT Studio 由此形成。

---

## 三、团队成员

目前：

* 计划规模：10 人左右
* 当前核心规模：8 人
* 长期限制：15 人以内

### 联合创始人

**NoWint**
状态：
在职

方向：

* Desktop @ macOS
* Desktop @ TUI（早期验证）

负责：

* 前期架构搭建；
* 群聊 Bot 支持；
* 主题系统开发。

**TiantianYZJ**
状态：
在职

方向：

* Desktop @ Windows

负责：

* PEYT Chat 聊天系统开发；
* JSON 二次封装；
* Chatmail 服务部署。

**SUKY**
状态：
不在职

身份：
联合创始人

**chenmuyun_bit**
状态：
不在职

身份：
联合创始人

### 核心成员

**CarryRao**
状态：
在职

方向：

* Android Backend
* Desktop Linux

负责：

* 后端移植；
* 平台适配；
* API 开发与对接。

**浣芷轩**
状态：
在职

方向：

* Desktop macOS

负责：

* UI/UX 设计；
* 界面优化。

**Falsw**
状态：
在职

**MaherJon**
状态：
在职

方向：

* Android Frontend

负责：

* Android UI/UX；
* 前端开发。

---

## 四、团队定位

PEYT 的核心定位：
一个由热爱编程与 AI 的年轻群体（尤其是中学生）组成的工作室，充满热情与活力。

目前 PEYT 不像：

* 公司；
* 商业创业团队；
* 严格科研机构。

更像：
一个年轻开发者技术社团。

特点：

* 因兴趣聚集；
* 因项目合作；
* 因技术成长。

---

## 五、团队文化

PEYT 内部氛围：
偏向：
B. 朋友组成的技术社团，一边玩一边创造。

成员之间：
除了推进项目：
也会：

* 闲聊；
* 聊技术；
* 聊 AI；
* 分享新发现。

整体特点：

* 自由；
* 开放；
* 兴趣驱动；
* 年轻。

成员年龄：
大约：
13-15 岁。

例如：

* NoWint：14 岁
* TiantianYZJ：15 岁
* CarryRao：13 岁
* MaherJon：15 岁
* 浣芷轩：13 岁

---

## 六、发展理念

PEYT 最初没有明确宏大目标。

成立原因：
不想因为研学结束而失去联系，希望利用各自能力一起做项目，闯出一点名头。

当前理念：
不是
「我要马上成为一家企业」
而是
一群年轻人一起创造一些真正的东西。

---

## 七、主要项目：PEYT Chat

### 项目定位

PEYT Chat 是 PEYT Studio 当前核心项目。

准确定位：
PEYT 内部使用的端到端加密团队聊天工具。

不是：

* 面向大众的微信替代品；
* 商业 IM；
* 去中心化社交平台。

用途：
解决 PEYT 自己的问题：

* 团队沟通；
* 程序员协作；
* 代码交流。

---

## 八、PEYT Chat 技术路线

基础：

* Delta Chat
* Chatmail

客户端：
采用：
Tauri

覆盖：

* Windows
* macOS
* Linux
* Android

### 为什么做 PEYT Chat？

两个主要原因：

1. **团队磨合**
   作为 PEYT 第一个完整项目：
   训练：

   * 协作；
   * 开发流程；
   * 跨平台开发。

2. **自己需要**
   普通聊天工具不适合开发团队。
   所以增加：

   * 代码化渲染；
   * GitHub 操作；
   * 待办看板；
   * 程序员友好功能。

---

## 九、PEYT Chat 后端

后端：
自部署 Chatmail

作用：
提供：

* 消息传输；
* 通信基础设施。

特点：

* 自己部署；
* 自己维护；
* 不依赖公共服务。

---

## 十、PEYT Chat 核心通信架构

这是 PEYT 最有特色的一部分。

我们没有采用：
WebXDC「应用跟着消息走」
而采用：
应用固定在客户端，消息只同步数据变化。

架构：

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

Chatmail 不存储 PEYT 数据

Chatmail：
只是：
安全传输层。
不是：
权威数据库。

真正数据：
存在客户端。

### Event 模型

不发送：
「整个状态」
而发送：
「状态变化事件」

例如：

创建投票：

```
poll.create
```

投票：

```
poll.vote
```

修改：

```
poll.update
```

每个事件：
包含：

```
event_id
entity_id
type
payload
```

其中：

* `event_id`：一次操作的唯一 ID
* `entity_id`：对象 ID

两者区分。

---

## 十一、Event Sourcing 思想

PEYT 采用类似：

* Git；
* Event Sourcing；

的思想。

核心：
事件是真实事实，数据库只是事件产生的结果。

结构：

```
Event Store

      ↓ replay

当前状态

      ↓

数据库
```

如果数据库损坏：
理论上可以：
重新播放事件。
恢复状态。

---

## 十二、版本兼容理念

PEYT Event：
带：
schema version

例如：
旧：

```
card.update v1
```

新：

```
card.update v2
```

历史事件：
不修改。
通过 migration：
兼容未来。

未知事件：
不会丢弃。

例如：
新功能：

```
project.archive
```

旧客户端：
收到后：
保存。
等待未来解析。

---

## 十三、PEYT Chat 开发分工

```
          PEYT Chat

Windows
  |
TiantianYZJ

macOS
  |
NoWint
浣芷轩

Linux
  |
CarryRao

Android
  |
MaherJon
CarryRao
```

---

## 十四、代码仓库

目前主要平台：
GitHub

组织：
PEYT Studio GitHub Organization

项目：
PEYT Chat：
NoWint 创建：
`PleaseEnterYourTextCommunity`

---

## 十五、开源态度

PEYT Chat：
保持：
开放源码。
但：
不会主动大规模宣传。

原因：

* P2P；
* 去中心化；
* E2EE；

这些理念在国内环境下推广存在现实限制。

策略：
有技术能力的人，可以自行部署。

---

## 十六、招募理念

目前：
计划扩招。
限制：
15 人以内。

希望成员：
拥有：

* 编程热情；
* 开发能力；
* GitHub 使用经验；
* Git 协作经验；
* 海外技术平台经验；
* AI 兴趣。

关注：

* LLM
* AGI
* AIGC
* Agent
* Harness

不希望：

* 混名额；
* 不写代码；
* 只会给 AI 下指令；
* 不懂工程；
* 不懂协作；
* 不接受团队合作。

欢迎：
有基础、愿学习、愿探索的人。

---

## 十七、当前 PEYT 的整体画像

如果让我用一句话总结：

> PEYT Studio 是一个由中学生开发者组成的年轻技术工作室，起源于 AI 研学中的伙伴关系，以兴趣和创造驱动，通过 PEYT Chat 等真实项目探索软件开发、AI 与协作技术。

更简短：
一群年轻程序员，用自己的方式 Type Everything。

---

## 十八、我认为 PEYT 当前阶段的关键词

```
年轻
+
技术兴趣
+
真实项目
+
自由协作
+
AI探索
+
开源精神
+
工程实践
```

目前 PEYT 最大的特点不是规模，而是：
在很早的年龄阶段，就开始按照真正软件团队的方式解决真实问题。

---

## 十九、实际开发档案（截至 2026-08-04）

> 以下内容由 TiantianYZJ 与 AI 协作整理，基于本地工作区两个仓库的实际状态。
> 与「档案」前文的设计愿景相比，此处记录的是**已经落地**的现实。

### 19.1 两个仓库

| 仓库 | 本地路径 | 性质 |
|---|---|---|
| PEYT Community | `E:\WechatDevelop\PEYT Community\` | PEYT Chat 桌面客户端（Tauri v2 + deltachat core） |
| ChatMail | `E:\WechatDevelop\ChatMail\` | 自部署 Chatmail（上游 relay + Docker 部署方案） |

### 19.2 PEYT Chat 客户端实际进度

已远超「档案」早期描述的进度：

* 技术栈：Tauri v2 + deltachat 核心（submodule）+ **Vanilla TypeScript** + Vite，无框架、无状态库、无 tauri-plugin。
* 前端：63 个 TS 文件，单一 `styles.css`（约 3000 行）。
* 后端：13 个 Rust 文件，约 115 个 Tauri 命令，双数据库（deltachat 核心 SQLite + 应用 `peytchat.db`）。

已建成功能：

* workspace / channel 体系（含 `spaceType: chat / card`）；
* Work 页卡片任务系统：看板 / 列表 / 日历 / 时间线四视图；
* Bot 账号系统 + LLM 运行时（DeepSeek / OpenAI / Claude，自动回帖）；
* 插件系统（GitHub Pages 市场安装，`new Function` 直执行 + 权限门控）；
* 好友邀请系统（选择联系人 / 邮箱 / `peyt://` 链接 / SecureJoin 二维码）；
* 11 套主题 + 全局字体缩放；
* Delta Chat 功能对齐批次 1-4（归档 / 保存 / 草稿 / 搜索 / 相册 / 语音 / webxdc / 通知 / 保护 / 多设备 / 备份）；
* 群组 / 已读回执 / 静音 / 置顶 / 转发等。

### 19.3 PEYT Event 落地现状

信封协议已实现**发送端**（`src-tauri/src/envelope.rs`）：

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

字段与「档案」第十章的 Event 模型**存在演进**：

* 原：`event_id` / `entity_id` / `type` / `payload`
* 现：`version` / `type` / `id`(uuid) / `timestamp` / `from` / `payload`

其中：

* `id` 承担幂等键（防重复处理）；
* `timestamp` 承担冲突消解。

现状（重要）：

* **接收端目前不解析 `[PEYT]` 信封**，信封消息原样渲染为普通消息（方便调试）；
* 卡片跨设备同步**实际走 `[CARD]` 前缀消息**（`[CARD]{...}` JSON），不是 `[PEYT]`；
* 架构愿景（Event Sourcing、版本兼容）正在分阶段落地：先让同步可用（`[CARD]`），再演进到通用信封协议（`[PEYT]`）。

### 19.4 ChatMail 部署现状

* 完整 clone 上游 `chatmail/relay`（chatmaild + cmdeploy Python 包）；
* `deploy/aliyun/` 提供 Docker「嫁接」部署方案：任意非 Debian Linux（已在阿里云 Linux 3 验证）上部署 ChatMail Relay；
* 容器内（Debian 12）：Dovecot / Postfix / Nginx / OpenDKIM / fcgiwrap；
* 宿主机：chatmaild venv / filtermail / iroh-relay / mtail / unbound / certbot；
* 通信：bind mount 文件卷 + Unix socket（`/home/vmail/run/`）；
* 踩坑记录：`deploy/aliyun/docs/PITFALLS.md` 共 26 条；
* 硬限制：阿里云出站 25 端口被物理封死 → 外发走 DirectMail SMTP 中继（80 端口 STARTTLS）；
* 服务域名：`yzjtiantian.cn`（客户端快速开始默认使用的 chatmail）。

### 19.5 待办与不一致项

* 根目录 `CLAUDE.md` 缺失（`docs/agent/README.md` 有引用）；
* 根 `README.md` 过时（仍写 Vanilla JS、旧目录结构，未提 bot / 插件 / `[PEYT]` 协议）；
* 早期 UI 审计 / 修复报告引用的 `.js` 文件名已过时（代码已迁 `.ts`）；
* Delta 对齐后续 stub 待做（资料 / 已读回执完善 / 转发 / 静音 / 置顶 / 群成员添加 / 角色 / 我的 QR / webxdc blob / 批次 4.5 通话）。

---

## 二十、后续档案补充计划

* PEYT 的历史时间线；
* 成员能力矩阵；
* 项目路线图；
* 官方介绍文案；
* 团队章程（轻量版，不破坏自由氛围）。
