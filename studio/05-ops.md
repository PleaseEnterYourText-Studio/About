# 运营与招募

## 代码仓库

目前主要平台：GitHub
组织：PEYT Studio GitHub Organization
项目：PEYT Chat，NoWint 创建，`PleaseEnterYourTextCommunity`

本地开发仓库：

| 仓库 | 本地路径 | 性质 |
|---|---|---|
| PEYT Community | `E:\WechatDevelop\PEYT Community\` | PEYT Chat 桌面客户端（Tauri v2 + deltachat core） |
| ChatMail | `E:\WechatDevelop\ChatMail\` | 自部署 Chatmail（上游 relay + Docker 部署方案） |
| About | 本仓库 | 工作室官方档案 |

## 开源态度

PEYT Chat 保持开放源码，但不会主动大规模宣传。

原因：P2P、去中心化、E2EE 这些理念在国内环境下推广存在现实限制。

策略：有技术能力的人，可以自行部署。

## 招募理念

目前计划扩招，限制 15 人以内。

希望成员拥有：编程热情、开发能力、GitHub 使用经验、Git 协作经验、海外技术平台经验、AI 兴趣。

关注：LLM、AGI、AIGC、Agent、Harness。

不希望：混名额、不写代码、只会给 AI 下指令、不懂工程、不懂协作、不接受团队合作。

欢迎：有基础、愿学习、愿探索的人。

---

## ChatMail 部署现状（截至 2026-08-04）

* 完整 clone 上游 `chatmail/relay`（chatmaild + cmdeploy Python 包）；
* `deploy/aliyun/` 提供 Docker「嫁接」部署方案：任意非 Debian Linux（已在阿里云 Linux 3 验证）上部署 ChatMail Relay；
* 容器内（Debian 12）：Dovecot / Postfix / Nginx / OpenDKIM / fcgiwrap；
* 宿主机：chatmaild venv / filtermail / iroh-relay / mtail / unbound / certbot；
* 通信：bind mount 文件卷 + Unix socket（`/home/vmail/run/`）；
* 踩坑记录：`deploy/aliyun/docs/PITFALLS.md` 共 26 条；
* 硬限制：阿里云出站 25 端口被物理封死 → 外发走 DirectMail SMTP 中继（80 端口 STARTTLS）；
* 服务域名：`yzjtiantian.cn`（客户端快速开始默认使用的 chatmail）。
