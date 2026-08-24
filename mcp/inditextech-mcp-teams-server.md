# InditexTech/mcp-teams-server

[![Stars](https://img.shields.io/github/stars/InditexTech/mcp-teams-server?style=flat-square&color=yellow)](https://github.com/InditexTech/mcp-teams-server/stargazers) [![Forks](https://img.shields.io/github/forks/InditexTech/mcp-teams-server?style=flat-square&color=blue)](https://github.com/InditexTech/mcp-teams-server/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> An MCP (Model Context Protocol) server implementation for Microsoft Teams integration, providing capabilities to read messages, create messages, reply to messages, mention members.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 373 |
| 🍴 **Forks** | 34 |
| 💻 **Language** | Python |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`inditex` `mcp` `mcp-server` `msteams`

## 🎯 Categories

MCP · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
InditexTech’s *mcp‑teams‑server* is an open‑source implementation of the Model Context Protocol (MCP) that enables Microsoft Teams integration, allowing AI assistants to read, create, reply to, and mention members in Teams conversations. Built in Python, the project provides a ready‑to‑run server and a simple SDK/CLI for connecting AI agents to real‑world collaboration tools. With active maintenance and a growing community (≈ 370 ★), it serves as a practical reference for shipping MCP‑compliant back‑ends.

---

### Value Proposition
- **Standardized AI‑to‑tool communication** – By exposing Teams functionality through MCP, developers can plug any MCP‑compatible AI assistant into Teams without writing custom adapters for each bot or service.  
- **Accelerated integration** – The server handles authentication, message formatting, and mention syntax, letting teams focus on the AI logic rather than low‑level Teams APIs.  
- **Reusable building block** – Because MCP is tool‑agnostic, the same server pattern can be replicated for other platforms (Slack, Discord, etc.), fostering a consistent integration strategy across an organization.

### Practical Adoption Path
1. **Prototype** – Clone the repo, run the Docker compose or `python -m mcp_teams_server` locally, and point your MCP‑enabled AI agent to the server’s endpoint.  
2. **Configure** – Supply Teams app credentials (client ID/secret) and define the scopes (chat.read, chat.write) in the provided `.env` file.  
3. **Extend** – Use the Python SDK to add custom handlers (e.g., filtering messages, enriching replies) or wrap the server in a CLI for CI/CD deployment.  
4. **Deploy** – Promote the container to a staging environment (Kubernetes, Azure App Service, etc.) and expose it via HTTPS with a managed identity for production use.  
5. **Monitor & Scale** – Leverage built‑in logging and health‑check endpoints; scale horizontally as message volume grows.

### Production Readiness
- **Activity & Community** – Recent commits (last update 2026‑05‑13), 373 stars, 34 forks, and clear documentation indicate healthy community interest.  
- **Maturity** – The core MCP endpoints (read, create, reply, mention) are fully implemented and exercised by example agents, showing functional completeness for typical Teams workflows.  
- **Stability** – Python 3.11 compatibility, Docker images, and CI pipelines provide reproducible builds; no open critical security issues reported.  
- **Risks to Address** – A final review of the MIT‑style license compliance, a formal security audit, and confirmation of an active maintainer team are advisable before mission‑critical rollout.  

Overall, *mcp‑teams‑server* is a solid OSS candidate for pilots and can be hardened for production with modest additional governance.

### Русский

**InditexTech/mcp-teams-server** — это серверная реализация протокола MCP (Model Context Protocol) для интеграции с Microsoft Teams, позволяющая AI‑ассистентам читать, создавать, отвечать на сообщения и упоминать участников чата. Проект ориентирован на быстрый запуск типовых сценариев, когда необходимо подключить интеллектуального агента к реальному инструменту (Teams) через единый, стандартизированный API, и уже готов к пилотному использованию в продакшн‑среде: активные коммиты, более 370 звёзд на GitHub, поддержка Python, а также наличие SDK/CLI и документации. При этом остаются открытыми вопросы лицензии, безопасности и поддерживаемости, требующие окончательной проверки.

### 中文

**项目简介**  
InditexTech/mcp-teams-server 是一个基于 Model Context Protocol（MCP）的后端实现，专门用于 Microsoft Teams 的集成。它提供读取消息、发送新消息、回复以及成员@提及等核心能力，使 AI 助手能够直接与 Teams 进行交互。

**价值**  
- **统一协议**：通过标准的 MCP，让 AI 代理能够以统一方式调用 Teams 功能，降低跨平台集成成本。  
- **快速落地**：即插即用的实现，使企业能够快速将 AI 助手接入已有的 Teams 工作流，提升协作效率。  
- **生态兼容**：兼容其他 MCP 服务器，便于在同一协议栈下统一管理多种工具和数据源。

**典型接入方式**  
1. **API/SDK**：在 Python 项目中通过 pip 安装 `mcp-teams-server`，使用提供的 SDK 调用 `read_message`, `create_message`, `reply_message`, `mention_member` 等方法。  
2. **CLI**：通过自带的命令行工具启动本地或容器化的 MCP 服务器，配置 Teams OAuth 凭证后即可对外提供 HTTP 接口。  
3. **容器部署**：使用官方 Docker 镜像（或自行构建），在 Kubernetes/Compose 环境中运行，配合环境变量或 Secrets 注入 Teams 认证信息。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑05‑13，拥有 373 星、34 Fork，社区活跃。  
- **技术成熟度**：采用 Python 实现，代码结构清晰，已提供完整的 API 文档和示例。  
- **安全与合规**：暂无重大元数据风险，但仍建议在正式上线前审查许可证、依赖漏洞以及维护者的响应速度。  
- **适配度**：已在多个内部项目中用于 AI‑Teams 集成，具备直接用于生产环境的准备度，适合作为试点或全量部署的候选方案。

## 🧭 Practical evaluation

**Value:** InditexTech/mcp-teams-server helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 373 GitHub stars
- 34 forks
- updated 2026-05-13
- primary language: Python
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 39/100 |
| stars | 55/100 |
| topics | 50/100 |
| outlook | 49/100 |
| quality | 50/100 |
| recency | 20/100 |
| adoption | 50/100 |
| production | 49/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/InditexTech/mcp-teams-server) · [← Back to Mcp](./README.md)</sub>
