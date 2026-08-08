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
| 项目板块版式 | 纵向滚动，每个作品一张全屏卡片（含旗舰 PEYT Chat + 组织作品墙） | 用户要求「一仓库一张全屏大卡片」，突出作品实力 |
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

### 板块 3 — 我们的项目（Our Projects）

> 主视觉句：我们把一次研学变成了一系列真实项目。每一个都在解决真实问题。

版式：**纵向滚动，每个作品一张全屏卡片**（占满视口高度），依次往下排布。旗舰项目 PEYT Chat 在最前，组织作品按主题在后。每张卡片均带 GitHub 链接（指向组织仓库）。

#### 卡 1 · PEYT Chat（旗舰项目，篇幅最重）

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

#### 卡 2 · EGGDataScience · 脑电数据分析平台

> 跨学科任务切换会如何破坏心流？这个问题来自我们的研学实验——受试者佩戴便携式 EEG 头环，在不同学科任务间切换，我们想量化「心流的恢复需要多久」。
>
> 它是一套完整的数据分析平台：支持 4 种实验条件（A→A / A→B / A→C / B→C），覆盖 6 项 EEG 指标的可视化（Theta/Alpha 比值、Alpha/Beta/Gamma 能量、谱熵、认知负载指数），用 ±5% 容差、30 秒连续窗口量化恢复时长，再做配对 t 检验与重复测量 ANOVA 的跨条件统计比较——最后自动生成结构化分析报告。
>
> 从数据采集到报告输出，一条流水线打通。我们不用 Excel 手搓脑电分析。
>
> **亮点**：不是玩具 demo，是能跑通完整科研流程的分析平台——数据、统计、报告三合一。
>
> 技术栈：Python 3.11+ / FastAPI / numpy / pandas / scipy / Chart.js

#### 卡 3 · NeuroLink-EEG · EEG BCI 心流实验平台

> 心流实验不止是「记录数据」，更是一场多方协作的实时演出：主控端操控实验流程，监视端观察实时脑电，受试者端执行任务，实验控制台统一调度——四端同步同一台 OpenBCI Ganglion 头环的实时波形。
>
> 数据链路是 UDP → 本地桥接 → 云端 WebSocket 中继，把便携式头环的脑电波形、频带功率、认知负载指标实时推到所有端。
>
> 它支撑「诱发 → 切换 → 恢复」递进式心流实验范式，回答那个核心问题：跨学科任务切换（文理 / 理艺 / 文艺）对心流的破坏程度，和脑电指标的恢复时长。
>
> **亮点**：一套头环 + 一个平台，四端实时同步——把科研实验从「单人记 Excel」变成「多人协作的实时系统」。
>
> 技术栈：OpenBCI Ganglion / UDP / WebSocket / Node.js

#### 卡 4 · Nervefeyn · AI 研究代理

> 研究最耗时的部分不是读，而是「找」和「连」——在成百上千篇论文里检索、梳理综述、多角度调查一个问题。我们把它交给一个代理来做。
>
> Nervefeyn 是开源的神经计算研究工作台：基于 Pi 运行时，内置论文搜索、文献综述、多代理深度调查、有界实验循环与长线自主研究。它不止是聊天机器人，而是一个能自主推进研究流程的工作台。
>
> **亮点**：不是套壳问答，而是长线自主研究——从检索到综述到多代理调查，代理真的能推着研究往前走。
>
> 技术栈：TypeScript / Astro / Pi 运行时

#### 卡 5 · NoargueWorkspace · 时光绿径待办

> 待办工具不缺，缺的是「能一起用」的。时光绿径是一个微信小程序 + Node.js 后端的待办管理：个人清单、组合归类、共享协作。
>
> 它最花心思的地方在协作与同步：待办可以分配给特定成员，完成方式有三种——全员完成、任一完成、指定某人完成；本地优先存储，再异步同步到后端，带冲突检测，本地云端都有改动时走 merge。
>
> **亮点**：不止是清单 App——它解决的是多端协作下最难的「同步一致性问题」，离线优先 + 冲突检测 merge。
>
> 技术栈：微信小程序原生 / TDesign / Express / MySQL（老版本 5.5，JSON 列都要自己序列化）

#### 卡 6 · PeytDocs · 团队文档站

> 团队的知识需要一个家。PeytDocs 收录 Peyt 系列项目的技术文档、API 接入规范、架构设计——从 PEYT Chat 客户端到时光绿径 API 再到 Workspace OS 架构。
>
> 基于 Docsify，零构建、纯静态，改一页 markdown 推到 main 就能生效，GitHub Pages 直接部署。文档不是负担，才能被持续维护。
>
> **亮点**：零构建、纯静态，写 markdown 即发布——文档的维护成本被降到最低。
>
> 技术栈：Docsify / GitHub Pages

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
- **组织仓库即工作室作品**：板块 3 的作品卡涵盖组织全部 6 个仓库（About 除外，作为档案页），旗舰 PEYT Chat + 脑科学/工具/文档作品墙，全部按全屏卡片呈现，数据来自 [studio/06-repos.md](../studio/06-repos.md)。
- **成员卡片**需每人一张，头像为 CSS 圆角（非 `<kbd>`），活人感为成员本人提供的话或 `*（待定）*` 占位。
- **加入入口**为 `@JOINUS.jpg` 二维码图，跳转 QQ 群。
- 全站中英双语：正文中文为主，关键板块（Hero、每节标题、首句/钩子、团队、招新）附英文。

## 待办（实现阶段）

- [ ] 决定官网技术栈与构建方式
- [ ] 放置 `@JOINUS.jpg` 二维码素材
- [ ] 补充 NoWint / CarryRao / Falsw / MaherJon 四人的一句话活人感
- [ ] 同步修正本仓库 README 中过时的「11 套主题」「Vanilla JS」等表述（可选，另开任务）
