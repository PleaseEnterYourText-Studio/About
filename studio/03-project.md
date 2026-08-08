# 项目：PEYT Chat

## 项目定位

PEYT Chat 是 PEYT Studio 当前核心项目。

准确定位：PEYT 内部使用的端到端加密团队聊天工具。

不是：

* 面向大众的微信替代品；
* 商业 IM；
* 去中心化社交平台。

用途：解决 PEYT 自己的问题——团队沟通、程序员协作、代码交流。

## 技术路线

基础：Delta Chat + Chatmail
客户端：采用 Tauri，覆盖 Windows / macOS / Linux / Android

### 为什么做 PEYT Chat？

1. **团队磨合**：作为 PEYT 第一个完整项目，训练协作、开发流程、跨平台开发。
2. **自己需要**：普通聊天工具不适合开发团队，所以增加代码化渲染、GitHub 操作、待办看板、程序员友好功能。

## 后端

后端：自部署 Chatmail
作用：提供消息传输、通信基础设施。
特点：自己部署、自己维护、不依赖公共服务。

---

## 实际开发状态（截至 2026-08-04）

### 客户端实际进度

已远超早期设计描述的进度：

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

> 详细技术架构见 [04-architecture.md](04-architecture.md)。

### 待办与不一致项

* 根目录 `CLAUDE.md` 缺失（`docs/agent/README.md` 有引用）；
* 根 `README.md` 过时（仍写 Vanilla JS、旧目录结构，未提 bot / 插件 / `[PEYT]` 协议）；
* 早期 UI 审计 / 修复报告引用的 `.js` 文件名已过时（代码已迁 `.ts`）；
* Delta 对齐后续 stub 待做（资料 / 已读回执完善 / 转发 / 静音 / 置顶 / 群成员添加 / 角色 / 我的 QR / webxdc blob / 批次 4.5 通话）。
