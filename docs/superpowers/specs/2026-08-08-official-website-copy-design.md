# PEYT Studio 官网文案设计

- **日期：** 2026-08-08
- **状态：** 待审阅
- **目的：** 为 PEYT Studio 官网落地页提供文案（content copy），供后续实现阶段使用
- **范围：** 单页落地页文案 + 结构定义。不含页面实现技术栈、样式、部署

## 背景

PEYT Studio（PleaseEnterYourText Studio / 请输入文本工作室）是一个由中学生开发者组成的年轻技术社团，slogan「Type Everything」。起源于深圳「AIx脑科学研学活动」中的 4 人小组，后发展为长期工作室。核心项目为 PEYT Chat（E2EE 团队聊天工具）。

官网将承担三种职能：**招新、作品展示、团队形象**。本设计只负责文案，页面实现另走流程。

## 设计决策

| 决策点 | 结论 | 理由 |
|---|---|---|
| 目的 | 三者兼顾（招新 + 展示 + 形象） | 一个页面同时服务三类受众 |
| 语言 | 中英双语（中文为主，关键板块附英文） | 国内招新为主，兼顾 GitHub 国际社区 |
| 结构 | 单页落地页（Hero → 关于 → 项目 → 团队 → 加入） | 简洁、维护成本低 |
| 语气 | 年轻 · 专业 | 保留社团感但不失可信度 |
| 叙事主轴 | E2EE + 自部署「功能优先」的温和表达 | 不控诉翻墙，对外友好 |
| 团队成员呈现 | 每位成员一张卡片 | 用户明确要求「一个人是一个 card」 |
| 平台说明 | `<kbd>` 圆角 hack 不用于真实网页，改用 CSS | 网页非 README，CSS 原生支持 |

## 文案素材来源（实测）

| 来源 | 说明 |
|---|---|
| 本仓库 README.md | 现有 About 页，提供大部分结构骨架 |
| studio/01-about.md | 成立背景 / 定位 / 文化 / 理念 |
| studio/02-team.md | 团队架构 / 分工 |
| studio/03-project.md、04-architecture.md | PEYT Chat 定位 / 技术路线 |
| studio/05-ops.md | 开源态度 / 招募理念 / Chatmail 部署 |
| members/*.md | 成员个人档案（活人感） |
| **PEYT Community 代码库**（E:\WechatDevelop\PEYT Community\） | 项目能力清单依据（实测） |
| **ChatMail-ANY-Linux-Deploy**（E:\WechatDevelop\ChatMail\） | 基础设施 / 自部署方案依据 |

> 注意：README 中「11 套主题」「Vanilla JS」等说法已过时，与代码库不符。本设计的项目能力清单以**代码库实测**为准（见下）。

## 文案正文

### 板块 1 — Hero

```
PEYT Studio
PleaseEnterYourText Studio · 请输入文本工作室
Type Everything
----
我们是一群中学生开发者。因一次研学相遇，因热爱技术走到一起，用真实项目练习成为真正的软件工程师。
We are a group of teenage developers. We met at a research camp, bonded over tech — and now we build real software together.

[徽章] members 8 · project PEYT Chat · open source
[主 CTA] 加入我们（锚点跳转招新区）
```

### 板块 2 — 关于我们（Who We Are）

```
我们是一个由中学生开发者组成的年轻技术工作室。

我们起源于深圳的 AIx脑科学研学活动。TiantianYZJ、NoWint、SUKY、chenmuyun_bit 四人在 5 天的研学中组队实验、一起完成汇报、彻夜讨论 AI 与技术。活动结束那天，大家不想就此失联——于是把一个研学小组，变成了一个长期技术工作室。

我们不是公司，也不是商业创业团队，更像一个年轻开发者技术社团：因兴趣聚集，因项目合作，因技术成长。成员年龄大约 13–15 岁，自由、开放、兴趣驱动。

EN: We are a teenage developer studio born from an AI research camp in Shenzhen. Four strangers turned teammates in 5 days — and chose to keep going. We're not a company; we're a community of young devs who build real software together.
```

### 板块 3 — 我们的项目（Our Project）

```
主项目：PEYT Chat — 面向开发团队的端到端加密协作聊天

普通聊天工具不适合开发团队。所以我们自己造了一个。
EN: PEYT Chat is our end-to-end encrypted chat built for dev teams — with kanban tasks, bots, and a built-in knowledge base.

能力清单（实测，分三组）：
- 聊天：workspace / channel · 手写消息 · Markdown 渲染 · @成员 / #频道彩色 tag · 群组 / 已读回执 / 置顶 / 转发 · 语音 · webxdc
- 协作：Work 页卡片任务（看板 / 列表 / 日历 / 时间线）· 多账号 · 收件箱 · 3D 词云 / 词频分析
- 智能：Bot + LLM 运行时（DeepSeek / OpenAI / Claude）· 知识库 / 自动总结（本地 llama-server）· GitHub 集成 · 插件系统（GitHub Pages 市场 + 权限门控）

架构（Mermaid 图）：
Chatmail 只是安全传输层，真正数据存在客户端；只同步「状态变化事件」。

配套：自部署 Chatmail（ChatMail-ANY-Linux-Deploy：任意 Linux 的 Docker 方案，阿里云实测，26 条踩坑文档）
```

### 板块 4 — 团队（Our Team）

```
6 位在职成员，一群用真实项目练习成长的年轻开发者。
EN: Six active members — teenage devs leveling up through real projects.

成员卡片墙（CSS Grid，每张卡片 = 圆形头像 + 名字 + 一句话活人感 + 角色/方向 + 个人站）：

[NoWint]  联合创始人 · macOS / TUI        活人感：*（待定）*        nowint.github.io
[TiantianYZJ] 联合创始人 · Windows       活人感：「我不是冯诺 1 曼派」   yzjtiantian.cn
[CarryRao]  核心成员 · Android / Linux    活人感：*（待定）*        carryrao.top
[浣芷轩]   核心成员 · macOS              活人感：「(◐‿◑) 你爹来啦」    bilibili
[Falsw]    核心成员 · 底层               活人感：*（待定）*        falswqwq.github.io
[MaherJon] 核心成员 · Android            活人感：*（待定）*        MAHE

分工 Mermaid 图（保留 README 那张）。

脚注：SUKY、chenmuyun_bit 为不在职联合创始人；规模计划 10 人左右，长期上限 15 人。
```

### 板块 5 — 加入我们（Join Us）

```
我们正在招人，面向 14–18 岁、有热情有基础的年轻开发者。
EN: We're recruiting teenage devs — 14 to 18 — who code, learn, and build.

我们关注：LLM · AGI · AIGC · Agent · Harness
我们需要：编程热情 · 开发能力 · Git 协作经验 · AI 兴趣
我们不欢迎：混名额 · 不写代码 · 只会给 AI 下指令 · 不懂工程 · 不协作

怎么加入：扫描 @JOINUS.jpg 加入 QQ 群。

开源与自主可控：E2EE 加密 + 自主可控 + 可自部署，是我们造 PEYT Chat 的动机，也是对外叙事的主轴。
```

## 内容要求

- **项目能力清单**必须以 PEYT Community 代码库实测为准（97 TS 文件 / 58 Rust 文件 / 192 Tauri 命令 / 15+9 套主题），不得沿用过时 README。
- **成员卡片**需每人一张，头像为 CSS 圆角（非 `<kbd>`），活人感为成员本人提供的话或 `*（待定）*` 占位。
- **加入入口**为 `@JOINUS.jpg` 二维码图，跳转 QQ 群。
- 全站中英双语：正文中文为主，关键板块（Hero、每节标题、首句/钩子、团队、招新）附英文。

## 待办（实现阶段）

- [ ] 决定官网技术栈与构建方式
- [ ] 放置 `@JOINUS.jpg` 二维码素材
- [ ] 补充 NoWint / CarryRao / Falsw / MaherJon 四人的一句话活人感
- [ ] 同步修正本仓库 README 中过时的「11 套主题」「Vanilla JS」等表述（可选，另开任务）
