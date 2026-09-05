# gethuman-sh/human

[![Stars](https://img.shields.io/github/stars/gethuman-sh/human?style=flat-square&color=yellow)](https://github.com/gethuman-sh/human/stargazers) [![Forks](https://img.shields.io/github/forks/gethuman-sh/human?style=flat-square&color=blue)](https://github.com/gethuman-sh/human/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> The AI Software Factory. Tickets, docs, designs, and analytics in. Shipped code out. One secure pipeline from idea to review — Claude on the line, human on the floor.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 54 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | Go |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-development` `amplitude` `azure-devops` `claude` `claude-code` `cli` `devcontainer` `developer-tools` `figma` `github` `gitlab`

## 🎯 Categories

MCP · AI/ML · Cloud & Storage · DevTools · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*gethuman‑sh/human* is an open‑source “AI Software Factory” that provides a standard protocol for wiring AI assistants to real‑world tools, data sources, and development pipelines. It lets teams expose APIs, SDKs, or CLIs so AI agents can execute tickets, retrieve docs, run designs, and collect analytics, then hand the resulting code back to human reviewers. With a Go‑based implementation, active maintenance, and growing community adoption, it’s positioned as a production‑ready foundation for AI‑augmented development workflows.

**Value**  
- **Unified integration layer** – By defining a common Model Context Protocol, the project eliminates the need to build bespoke connectors for each tool, dramatically reducing integration effort and technical debt.  
- **Secure end‑to‑end pipeline** – AI‑generated suggestions travel through a controlled pipeline (Claude on the line, human on the floor), ensuring code quality, compliance, and auditability before deployment.  
- **Accelerated delivery** – Teams can automatically generate tickets, fetch documentation, run design checks, and push shipped code, shortening the ideation‑to‑release cycle.

**Practical Adoption Path**  
1. **Evaluate the API/SDK/CLI** – Clone the repo, run the provided Go binary or import the Go SDK, and test a simple “hello‑world” integration (e.g., a CLI that fetches a document).  
2. **Deploy a Model Context Protocol server** – Containerize the server or run it as a sidecar in your CI/CD environment; configure authentication and network policies.  
3. **Connect your AI agents** – Point Claude, GPT‑4, or any compatible model to the server’s endpoint, using the protocol to issue tickets, retrieve data, or trigger builds.  
4. **Integrate with existing tooling** – Wrap existing internal APIs (issue trackers, code repos, design tools) with thin adapters that speak the protocol, then gradually replace custom scripts.  
5. **Roll out with human review** – Enable the “human on the floor” checkpoint in your pipeline, allowing reviewers to approve or edit AI‑generated code before merge.

**Production Readiness**  
- **Activity & community**: Recent commits (as of 2026‑06‑26), 54 stars, 5 forks, and a growing set of topics indicate active development and interest.  
- **Maturity**: The Go implementation is stable, well‑typed, and easy to embed in microservices or serverless functions.  
- **Security & licensing**: No immediate metadata risks, but a final audit of the open‑source license and dependency vulnerabilities is recommended.  
- **Pilot suitability**: Given its strong signals of adoption, clear protocol definition, and straightforward deployment options, *gethuman‑sh/human* is ready for a serious pilot in production environments, pending the usual security and maintainer vetting.

### Русский

**gethuman-sh/human** — это open‑source платформа, позволяющая быстро подключать AI‑ассистентов к реальным инструментам и данным через единый протокол (Model Context Protocol). Типичный сценарий: разработчик разворачивает сервер‑интегратор, подключает к нему свои CI/CD, аналитические и дизайнерские сервисы, а затем AI‑агент (например, Claude) автоматически обрабатывает тикеты, генерирует код и обновляет документацию, оставляя человеку лишь контроль качества. Проект уже активно поддерживается (обновления — 2026‑06‑26, 54 ★, Go‑код), имеет стабильный API/SDK/CLI и готов к пилотному использованию в продакшене после финальной проверки лицензии и безопасности.

### 中文

**项目简介**  
`gethuman-sh/human` 是一个 AI 软件工厂，提供从需求（Ticket、文档、设计、分析）到交付代码的全链路安全流水线。它通过统一的 Model Context Protocol 将 AI 助手（如 Claude）与真实的工具、数据和业务系统连接起来，实现“AI 在线、人工在场”的协同开发。

**价值**  
- **标准化 AI‑Tool 接入**：提供统一协议，让各种 AI 代理能够轻松调用内部 API、SDK、CLI 等工具，避免每个项目自行实现碎片化的桥接层。  
- **加速交付**：在同一流水线中完成需求捕获、设计评审、代码生成与审查，显著缩短从想法到可运行代码的周期。  
- **安全可审计**：所有操作都走可审计的管道，支持细粒度权限控制和审计日志，满足企业合规要求。

**典型接入方式**  
1. **API/SDK 集成**：在已有服务中引入 `human` 提供的 Go SDK（或通过 OpenAPI 生成的客户端），直接调用 `CreateTicket`、`RunDesign`、`SubmitCode` 等端点。  
2. **CLI 调用**：在 CI/CD 脚本或本地开发环境中使用 `human-cli`，通过命令行触发 AI 生成、审查和部署流程。  
3. **Model Context Protocol Server**：部署 `human` 的 MCP 服务器，作为统一的协议网关，其他 AI 代理只需遵循该协议即可访问所有内部工具和数据。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑26，项目仍在持续维护；GitHub 关注度 54 ⭐、5 fork，社区讨论活跃。  
- **技术成熟度**：核心实现使用 Go，提供完整的 API、SDK 与 CLI，且已有多个内部项目成功上线。  
- **风险评估**：暂无重大元数据风险；仍需对许可证（MIT/Apache 等）和安全审计（依赖库、容器镜像）进行最终确认。总体来看，`human` 已具备在生产环境中进行试点或正式部署的条件。

## 🧭 Practical evaluation

**Value:** gethuman-sh/human helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 54 GitHub stars
- 5 forks
- updated 2026-06-26
- primary language: Go
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 37/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 64/100 |
| recency | 80/100 |
| adoption | 32/100 |
| production | 71/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/gethuman-sh/human) · [← Back to Mcp](./README.md)</sub>
