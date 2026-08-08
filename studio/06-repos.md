# 仓库与个人主页归档

> 盘点日期：2026-08-08。数据来自 GitHub API 实测（组织页 + 各成员主页）。
> 本文件是工作室对外代码资产的总览：组织仓库、成员个人主页、成员个人仓库。

---

## 一、组织仓库（PleaseEnterYourText-Studio）

组织共 **6 个公开仓库**。除 `About` 外，其余 5 个均为**成员个人仓库的 fork 镜像**——组织统一收录，源仓库仍归各成员所有。

| 仓库 | 类型 | 源（成员） | 语言 | 说明 |
|---|---|---|---|---|
| [About](https://github.com/PleaseEnterYourText-Studio/About) | 原创 | — | — | 本档案仓库 · 工作室官方 About |
| [NoargueWorkspace](https://github.com/PleaseEnterYourText-Studio/NoargueWorkspace) | fork | NoWint | JS/TS | 时光绿径待办：微信小程序 + Node.js 待办管理 |
| [EGGDataScience](https://github.com/PleaseEnterYourText-Studio/EGGDataScience) | fork | NoWint | Python | EEG 数据分析平台（FastAPI，心流研究） |
| [Nervefeyn](https://github.com/PleaseEnterYourText-Studio/Nervefeyn) | fork | NoWint | TS/Astro | 开源 AI 研究代理 · 神经计算研究工作台 |
| [NeuroLink-EEG](https://github.com/PleaseEnterYourText-Studio/NeuroLink-EEG) | fork | TiantianYZJ | HTML/JS | EEG BCI 心流实验平台（OpenBCI Ganglion） |
| [PeytDocs](https://github.com/PleaseEnterYourText-Studio/PeytDocs) | fork | NoWint | CSS/HTML | Peyt 系列项目与团队技术文档站（Docsify） |

> 观察：组织仓库集中在两块主题——**脑科学/研学**（EGG、Nervefeyn、NeuroLink）与 **PEYT 生态/文档**（PeytDocs）。主项目 PEYT Chat 客户端（PleaseEnterYourTextCommunity）目前**未镜像到组织**，仅在成员个人名下。

---

## 二、成员个人主页

| 成员 | GitHub 用户名 | 个人站 | 状态 |
|---|---|---|---|
| NoWint | [NoWint](https://github.com/NoWint) | [nowint.github.io](https://nowint.github.io) | 在职 · 联合创始人 |
| TiantianYZJ | [TiantianYZJ](https://github.com/TiantianYZJ) | [yzjtiantian.cn](https://yzjtiantian.cn/) | 在职 · 联合创始人 |
| CarryRao | [Carry-Rao](https://github.com/Carry-Rao) | [carryrao.top](https://carryrao.top/) | 在职 · 核心成员 |
| 浣芷轩 | [ieshishinjin](https://github.com/ieshishinjin) | [bilibili](https://space.bilibili.com/1716940207) | 在职 · 核心成员 |
| Falsw | [FALSW](https://github.com/FALSW) | [falswqwq.github.io](https://falswqwq.github.io/) | 在职 · 核心成员 |
| MaherJon | [MaherJon](https://github.com/MaherJon) | [MAHE](https://maherjon.github.io/MAHE/) | 在职 · 核心成员 |
| SUKY | [suky](https://github.com/suky) | — | 不在职 · 联合创始人 |
| chenmuyun_bit | [chenmuyun-bit](https://github.com/chenmuyun-bit) | — | 不在职 · 联合创始人 |

> 备注：
> - CarryRao 用户名为 `Carry-Rao`（连字符），个人站 carryrao.top 确认。
> - 浣芷轩 GitHub 用户名 `ieshishinjin`，bio 为「(◐‿◑) 你爹来啦」。
> - FALSW、chenmuyun-bit 当前公开仓库为 0（可能私仓或未上传）。
> - GitHub 用户名不允许下划线，故 chenmuyun_bit 在 GitHub 上是 `chenmuyun-bit`。

---

## 三、成员个人仓库清单

### NoWint（43 个仓库，个人站 nowint.github.io）

**PEYT 生态**
- [PleaseEnterYourTextCommunity](https://github.com/NoWint/PleaseEnterYourTextCommunity) — Rust, ⭐5 — PEYT Chat 桌面客户端（主仓库）
- [core](https://github.com/NoWint/core) — fork — Peytc 的 chatmail core（submodule）
- [PeytDocs](https://github.com/NoWint/PeytDocs) — CSS, ⭐2 — 团队文档站

**脑科学 / 研学**
- [EGGDataScience](https://github.com/NoWint/EGGDataScience) — Python, ⭐2 — EEG 脑电数据科学分析工具
- [Nervefeyn](https://github.com/NoWint/Nervefeyn) — TS, ⭐1 — AI 研究代理 · 神经计算研究工作台
- [Open-EEG-Dataset](https://github.com/NoWint/Open-EEG-Dataset) — TS, ⭐1 — EEG 研究数据集（BrainFlow 原始记录）
- [XEGG_luajava_android](https://github.com/NoWint/XEGG_luajava_android) — Kotlin, ⭐1 — EEG 相关 Android 端
- [Procession](https://github.com/NoWint/Procession) — TS, ⭐2 — 3D 城市景观可视化（进程即建筑）

**AI / Agent 工具**
- [AgentVault](https://github.com/NoWint/AgentVault) — Rust, ⭐2 — Git for AI Agents · 提示/上下文管理
- [AgentToolbox](https://github.com/NoWint/AgentToolbox) — TS — agent 工具箱
- [ContextHub](https://github.com/NoWint/ContextHub) — TS — agent context manager
- [knowledge-base](https://github.com/NoWint/knowledge-base) — TS — agent 知识库
- [ReasonLoop](https://github.com/NoWint/ReasonLoop) — TS, ⭐2 — agent 推理中间件
- [multi-track-development-planning](https://github.com/NoWint/multi-track-development-planning) — Shell, ⭐3 — 抗 agent 项目架构
- [doge-code](https://github.com/NoWint/doge-code) — fork — Claude Code 的 fork（番外篇）
- [qwen2API](https://github.com/NoWint/qwen2API) — fork — Qwen 网页转 API
- [WebAI2API](https://github.com/NoWint/WebAI2API) — fork — 网页 AI 转 API（Camoufox）
- [SecretScanner](https://github.com/NoWint/SecretScanner) — Go, ⭐2 — 仓库密钥扫描（安全）
- [STFU](https://github.com/NoWint/STFU) — Python, ⭐1 — 自动确认 AI IDE 弹窗
- [WallStreetAgentss](https://github.com/NoWint/WallStreetAgentss) — Rust — 金融 agent

**效率 / 工具**
- [NoargueWorkspace](https://github.com/NoWint/NoargueWorkspace) — JS, ⭐2 — 时光绿径待办（微信小程序）
- [TimeGreenPathTodo](https://github.com/NoWint/TimeGreenPathTodo) — JS, ⭐2 — 每日任务足迹管理
- [AsharesDashboard](https://github.com/NoWint/AsharesDashboard) — TS, ⭐1 — A股数据看板
- [SuperSync](https://github.com/NoWint/SuperSync) — Python, ⭐2 — 超级同步
- [EricPointSystem](https://github.com/NoWint/EricPointSystem) — 积分系统
- [RepoLens](https://github.com/NoWint/RepoLens) — TS — GitHub 仓库分析
- [CCcompanion](https://github.com/NoWint/CCcompanion) — TS, ⭐1 — 实用工具集
- [tiyuzhongkaotiku](https://github.com/NoWint/tiyuzhongkaotiku) — HTML — 体育中考题库
- [BMCanvas](https://github.com/NoWint/BMCanvas) — TS, ⭐1 — Canvas 画板
- [100-Projects](https://github.com/NoWint/100-Projects) — 百项目练习

**Minecraft / 整活**
- [BonNextMinecraftLauncher-Rust](https://github.com/NoWint/BonNextMinecraftLauncher-Rust) — TS, ⭐17 — Minecraft 启动器
- [BonjourMinecraftLauncher](https://github.com/NoWint/BonjourMinecraftLauncher) — TS, ⭐2 — vibe coding 启动器
- [BonjourPrism](https://github.com/NoWint/BonjourPrism) — C++ — Prism 的现代化 fork
- [BonjourOVO](https://github.com/NoWint/BonjourOVO) / [BonNextRelease](https://github.com/NoWint/BonNextRelease) — HTML — 启动器发布页
- [singularity](https://github.com/NoWint/singularity) — fork — Three.js 黑洞渲染
- [AFFiNE](https://github.com/NoWint/AFFiNE) — fork — Notion/Miro 替代
- [fluent_ui](https://github.com/NoWint/fluent_ui) — fork — WinUI3 in Flutter
- [VSCodeAndroid](https://github.com/NoWint/VSCodeAndroid) — fork — VSCode Android 移植
- [justblackhole](https://github.com/NoWint/justblackhole) / [mewed](https://github.com/NoWint/mewed) — 个人实验

**个人主页**
- [NoWint.github.io](https://github.com/NoWint/NoWint.github.io) — TS — 个人主页
- [NoWint](https://github.com/NoWint/NoWint) — ItzNoWint2026

### TiantianYZJ（14 个仓库，个人站 yzjtiantian.cn）

**PEYT 生态**
- [PleaseEnterYourTextCommunity](https://github.com/TiantianYZJ/PleaseEnterYourTextCommunity) — Rust, ⭐5 — PEYT Chat 客户端
- [ChatMail-ANY-Linux-Deploy](https://github.com/TiantianYZJ/ChatMail-ANY-Linux-Deploy) — Python, ⭐2 — 任意 Linux 自部署 Chatmail
- [PeytDocs](https://github.com/TiantianYZJ/PeytDocs) — CSS, ⭐2 — 团队文档站
- [About](https://github.com/TiantianYZJ/About) — ⭐1 — 官方档案（本仓库）

**脑科学 / 研学**
- [NeuroLink-EEG](https://github.com/TiantianYZJ/NeuroLink-EEG) — HTML, ⭐2 — EEG BCI 心流实验平台
- [Procession](https://github.com/TiantianYZJ/Procession) — TS, ⭐2 — 3D 城市景观可视化

**效率 / 工具**
- [NoargueWorkspace](https://github.com/TiantianYZJ/NoargueWorkspace) — JS, ⭐2 — 时光绿径待办
- [TimeGreenPathTodo](https://github.com/TiantianYZJ/TimeGreenPathTodo) — JS, ⭐2 — 每日任务足迹
- [CountdownApp](https://github.com/TiantianYZJ/CountdownApp) — HTML — 桌面倒计时组件（中考倒计时等）
- [TaskWing](https://github.com/TiantianYZJ/TaskWing) — HTML, ⭐1 — 学习待办管理
- [WeekFlow](https://github.com/TiantianYZJ/WeekFlow) — HTML — 工作代办管理
- [clawd-on-desk](https://github.com/TiantianYZJ/clawd-on-desk) — fork

**个人主页**
- [tiantianyzj.github.io](https://github.com/TiantianYZJ/tiantianyzj.github.io) / [t.github.io](https://github.com/TiantianYZJ/t.github.io) — HTML — 个人主页

### CarryRao（11 个仓库，个人站 carryrao.top）

**PEYT 生态**
- [PleaseEnterYourTextCommunity](https://github.com/Carry-Rao/PleaseEnterYourTextCommunity) — Rust, ⭐5 — PEYT Chat 客户端
- [peytchat-android](https://github.com/Carry-Rao/peytchat-android) — Kotlin — Android 端

**学习 / 练手**
- [goutils](https://github.com/Carry-Rao/goutils) — Go — Go 工具集
- [learn](https://github.com/Carry-Rao/learn) — JS — 学习记录
- [tinystl](https://github.com/Carry-Rao/tinystl) — STL 学习
- [userd](https://github.com/Carry-Rao/userd) — C++ — Linux 工具
- [vnet](https://github.com/Carry-Rao/vnet) — Kotlin — 网络
- [cat-catch](https://github.com/Carry-Rao/cat-catch) — fork — 浏览器资源嗅探扩展
- [fangyuhan001.github.io](https://github.com/Carry-Rao/fangyuhan001.github.io) — fork — 网页
- [status](https://github.com/Carry-Rao/status) — JS — 状态页

### 浣芷轩 / ieshishinjin（31 个仓库，个人站 bilibili）

**PEYT 生态**
- [PleaseEnterYourTextCommunity](https://github.com/ieshishinjin/PleaseEnterYourTextCommunity) — Rust, ⭐5 — PEYT Chat 客户端
- [PleaseEnterYourTextCommunityPluginsMarket](https://github.com/ieshishinjin/PleaseEnterYourTextCommunityPluginsMarket) — JS, ⭐1 — PEYT 插件市场
- [PeytDocs](https://github.com/ieshishinjin/PeytDocs) — CSS, ⭐2 — 团队文档站
- [plugin-market](https://github.com/ieshishinjin/plugin-market) — fork — 插件市场模板

**效率 / 工具**
- [Apple-Music-Playlist-Converter](https://github.com/ieshishinjin/Apple-Music-Playlist-Converter) — JS, ⭐3 — Apple Music 歌单转换
- [iLyricMP3](https://github.com/ieshishinjin/iLyricMP3) — Go, ⭐2 — lrc 歌词内嵌工具
- [TianHeDoc](https://github.com/ieshishinjin/TianHeDoc) — Swift, ⭐2 — 文档软件
- [RePKG-G](https://github.com/ieshishinjin/RePKG-G) — Rust — 资源解包
- [xwguidecompress](https://github.com/ieshishinjin/xwguidecompress) — fork — 图形化压缩软件
- [skillsforemikowalski](https://github.com/ieshishinjin/skillsforemikowalski) — fork — Skills for Design Engineers
- [dongbeidongbei](https://github.com/ieshishinjin/dongbeidongbei) / [Somethings](https://github.com/ieshishinjin/Somethings) — 个人实验
- [exampleswiftapp](https://github.com/ieshishinjin/exampleswiftapp) — Swift 练手
- [testie](https://github.com/ieshishinjin/testie) — Vue — 测试

**Minecraft / 游戏（量大，主导兴趣）**
- [Minecraft-Transit-Railway](https://github.com/ieshishinjin/Minecraft-Transit-Railway) — fork — MTR 模组
- [BML-s-Transit-Expansion](https://github.com/ieshishinjin/BML-s-Transit-Expansion) — fork — MTR 扩展
- [MaximizeMTRMod](https://github.com/ieshishinjin/MaximizeMTRMod) — Java, ⭐1 — MTR 性能优化
- [JR-Style-Mod](https://github.com/ieshishinjin/JR-Style-Mod) — Java, ⭐2 — JR 风格模组
- [Shade-Mod](https://github.com/ieshishinjin/Shade-Mod) — Java, ⭐1 — 光影模组
- [Painting-Addon](https://github.com/ieshishinjin/Painting-Addon) — Java — 画作附属
- [FirstmodForMe](https://github.com/ieshishinjin/FirstmodForMe) — Java — 第一个 Forge 项目
- [MultiLoader-Template](https://github.com/ieshishinjin/MultiLoader-Template) — fork — NeoForge+Fabric 模板
- [Splice](https://github.com/ieshishinjin/Splice) — Java, ⭐2 — Minecraft 模组版本迁移 CLI
- [HMCL](https://github.com/ieshishinjin/HMCL) / [PCL](https://github.com/ieshishinjin/PCL) — fork — Minecraft 启动器
- [SeaLantern](https://github.com/ieshishinjin/SeaLantern) — fork — B 站社区开服器
- [StardustSandBox](https://github.com/ieshishinjin/StardustSandBox) — C#, ⭐3 — 自由探索沙盘游戏
- [Dress](https://github.com/ieshishinjin/Dress) — fork — 女装备份（整活）
- [myvocaloid2025](https://github.com/ieshishinjin/myvocaloid2025) — VOCALOID 整活

### MaherJon（12 个仓库，个人站 MAHE）

**PEYT 生态**
- [PleaseEnterYourTextCommunity](https://github.com/MaherJon/PleaseEnterYourTextCommunity) — TS — PEYTC 移动端实现
- [peytchat-android](https://github.com/MaherJon/peytchat-android) — Kotlin — Android 端
- [Old_PEYTC_Android](https://github.com/MaherJon/Old_PEYTC_Android) — JS — PEYTC Android 旧实现

**自研项目**
- [MAHE](https://github.com/MaherJon/MAHE) — HTML — 个人主页
- [maheOS-Minimalist-Agile-Hardware-Enabled-OS](https://github.com/MaherJon/maheOS-Minimalist-Agile-Hardware-Enabled-OS) — Shell, ⭐6 — 极简操作系统设计
- [Mino](https://github.com/MaherJon/Mino) — C, ⭐4 — 自写面向对象编程语言
- [Tenne](https://github.com/MaherJon/Tenne) — 二分类模型（AICG 检测）
- [Tenne-Qt](https://github.com/MaherJon/Tenne-Qt) — C++, ⭐3 — Tenne AICG 检测图形版
- [Code-Assistant](https://github.com/MaherJon/Code-Assistant) — Python — 代码助手
- [NAICG_WEB](https://github.com/MaherJon/NAICG_WEB) — HTML — Not AICG 计划网页

### FALSW（0 个公开仓库，个人站 falswqwq.github.io）

- 当前无公开仓库（可能私仓）。

### SUKY（2 个仓库，不在职）

- [TWRP_cn](https://github.com/suky/TWRP_cn) — C, ⭐16 — TWRP 中文化（安卓刷机）
- [android_kernel_pantech_ef65l](https://github.com/suky/android_kernel_pantech_ef65l) — C — 安卓内核（Pantech IM-A820L）

### chenmuyun-bit（0 个公开仓库，不在职）

- 当前无公开仓库。

---

## 四、主题归类速览

| 主题 | 主要仓库 | 主要成员 |
|---|---|---|
| **PEYT Chat 客户端** | PleaseEnterYourTextCommunity（多端镜像） | NoWint / TiantianYZJ / MaherJon / Carry-Rao / ieshishinjin |
| **Chatmail 部署** | ChatMail-ANY-Linux-Deploy | TiantianYZJ |
| **团队文档** | PeytDocs | NoWint / TiantianYZJ / ieshishinjin |
| **插件生态** | PleaseEnterYourTextCommunityPluginsMarket | ieshishinjin |
| **脑科学 / EEG 研学** | EGGDataScience / NeuroLink-EEG / Nervefeyn / Open-EEG-Dataset | NoWint / TiantianYZJ |
| **AI / Agent 工具** | AgentVault / AgentToolbox / ReasonLoop / ContextHub / SecretScanner 等 | NoWint |
| **效率 / 待办** | NoargueWorkspace / TimeGreenPathTodo / CountdownApp / TaskWing / WeekFlow | NoWint / TiantianYZJ |
| **Minecraft / 游戏** | MTR 系列模组 / 启动器 / StardustSandBox | ieshishinjin / NoWint |
| **自研语言 / OS** | Mino / maheOS | MaherJon |

---

## 五、备注

- 组织仓库目前是成员仓库的镜像集，源仓库在成员个人名下；未来可将 PEYT Chat 主仓库也镜像入组织。
- 本文件与 [05-ops.md](05-ops.md) 的本地仓库表互补：05-ops 记本地路径与开发性质，本文件记线上资产全貌。
