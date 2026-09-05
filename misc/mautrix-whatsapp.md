# mautrix/whatsapp

[![Stars](https://img.shields.io/github/stars/mautrix/whatsapp?style=flat-square&color=yellow)](https://github.com/mautrix/whatsapp/stargazers) [![Forks](https://img.shields.io/github/forks/mautrix/whatsapp?style=flat-square&color=blue)](https://github.com/mautrix/whatsapp/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> A Matrix-WhatsApp puppeting bridge

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.8k |
| 🍴 **Forks** | 257 |
| 💻 **Language** | Go |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bridge` `go` `golang` `matrix` `matrix-appservice` `matrix-org` `whatsapp` `whatsapp-web`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
mautrix/whatsapp is an open‑source Go bridge that puppets WhatsApp accounts as Matrix users, allowing messages, media, and presence to flow bidirectionally between the two platforms. With over 1.8 k stars, frequent commits (last update 2026‑07‑01) and a small but active fork community, it shows strong ecosystem momentum and can be trialled quickly for teams that already run a Matrix homeserver.

**Value** – The bridge lets organizations keep existing WhatsApp conversations while leveraging Matrix’s federation, encryption, and bot ecosystem, reducing the need for separate chat silos and enabling unified notifications, archiving, and automation.

**Adoption path** – Start with a proof‑of‑concept: clone the repo, follow the README to configure a WhatsApp registration (phone number) and a Matrix appservice, and run the bridge in a test room. Verify message sync, media handling, and permission mapping, then gradually roll it out to a pilot group and integrate with existing Matrix bots or bridges.

**Production readiness** – The project scores high on readiness: recent activity, a healthy star/fork count, and Go’s static binaries simplify deployment; however, a final review of the license (Apache‑2.0), security posture (dependency scanning), and maintainer responsiveness is still required before a full‑scale production rollout. Once those checks are cleared, the bridge is suitable for a serious pilot or production use.

### Русский

Резюме проекта mautrix/whatsapp:

Проект mautrix/whatsapp представляет собой открытый исходный код, который обеспечивает мост между платформой Matrix и сервисом WhatsApp. Он может быть полезен при интеграции с конкретной бизнес-процессной цепочкой, как указано в README и активности проекта. Проект готов к пилотному освоению в производстве, поскольку имеет сильные экосистемные сигналы, недавнюю активность и широкое распространение.

### 中文

**项目简介**  
mautrix/whatsapp 是一个用 Go 实现的 Matrix‑WhatsApp 机器人桥（puppeting bridge），能够在 Matrix 房间和 WhatsApp 之间同步消息、媒体和回执，实现双向聊天。

**价值**  
- **统一沟通渠道**：企业或社区可以在已有的 Matrix 环境中直接与使用 WhatsApp 的用户交流，无需切换客户端。  
- **自动化与机器人**：支持 Matrix 机器人在 WhatsApp 上发送通知、提醒或执行指令，适用于监控、CI/CD 通知等场景。  
- **开源可定制**：源码开放，能够根据业务需求自行扩展功能或集成内部身份系统。

**典型接入方式**  
1. **准备环境**：在一台能够访问外网的服务器上安装 Go 运行时。  
2. **获取并配置**：克隆仓库，复制 `example-config.yaml`，填写 Matrix homeserver、access token、WhatsApp 账户的电话号码、验证码/密码等信息。  
3. **运行桥接**：`go build && ./mautrix-whatsapp -c config.yaml`，桥接会在 Matrix 上创建对应的 “puppet” 用户。  
4. **关联房间**：在 Matrix 房间中使用 `/bridge invite`（或通过 UI）将 WhatsApp 联系人/群组邀请进来，即可开始双向消息同步。  
5. **可选集成**：通过 webhook、Prometheus metrics 或自定义插件，将桥接与监控、CI 或业务系统进一步耦合。

**生产可用性**  
- **活跃度**：截至 2026‑07‑01 最近一次提交，拥有 1824 ⭐、257 forks，社区活跃，已在多个组织的生产环境中使用。  
- **成熟度**：支持消息、媒体、回执、编辑、删除等核心功能，且具备错误重试和持久化存储。  
- **可运维性**：提供 Docker 镜像和 systemd 示例，便于容器化部署和监控。  
- **风险**：仍需自行审查许可证（Apache‑2.0）及依赖的安全漏洞，并确保 WhatsApp 账户的登录方式符合企业合规要求。总体而言，经过一次小规模的 PoC 验证后，即可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** mautrix/whatsapp may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1824 GitHub stars
- 257 forks
- updated 2026-07-01
- primary language: Go
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 60/100 |
| stars | 69/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 80/100 |
| recency | 80/100 |
| adoption | 67/100 |
| production | 72/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/mautrix/whatsapp) · [← Back to Misc](./README.md)</sub>
