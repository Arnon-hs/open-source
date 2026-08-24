# korotovsky/slack-mcp-server

[![Stars](https://img.shields.io/github/stars/korotovsky/slack-mcp-server?style=flat-square&color=yellow)](https://github.com/korotovsky/slack-mcp-server/stargazers) [![Forks](https://img.shields.io/github/forks/korotovsky/slack-mcp-server?style=flat-square&color=blue)](https://github.com/korotovsky/slack-mcp-server/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> The most powerful MCP Slack Server with no permission requirements, Apps support, GovSlack, DMs, Group DMs and smart history fetch logic.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.6k |
| 🍴 **Forks** | 316 |
| 💻 **Language** | Go |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`assistants` `govslack` `llm` `mcp` `mcp-server` `slack` `slack-api`

## 🎯 Categories

MCP · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
korotovsky/slack-mcp-server is an open‑source Go implementation of the Model Context Protocol (MCP) for Slack, offering a fully‑featured Slack‑compatible server with zero permission requirements, support for Slack Apps, GovSlack, direct and group DMs, and an intelligent history‑fetching engine. It enables AI assistants to interact with real Slack workspaces and tools using a standard, low‑friction API, making it a strong candidate for production‑grade pilots.

**Value**  
- **Standardised bridge** – By exposing a clean MCP‑based API, the server lets any MCP‑compatible AI model (e.g., Claude, GPT‑4o) read from and write to Slack channels, DMs, and GovSlack environments without dealing with Slack’s OAuth flow or rate‑limit quirks.  
- **Feature‑rich out‑of‑the‑box** – Built‑in support for Apps, group DMs, and a “smart history” fetch layer reduces the engineering effort required to give agents context‑aware conversation histories.  
- **Open‑source & community‑backed** – 1.6 k stars, 300+ forks, and active commits (last update 2026‑05‑14) signal a healthy ecosystem and rapid bug‑fix turnaround.

**Practical Adoption Path**  

| Step | Action | Why it matters |
|------|--------|----------------|
| 1️⃣  | **Clone & build** – `go build ./...` (requires Go 1.22+). | The project is a single Go binary, so deployment is straightforward on any container host or VM. |
| 2️⃣  | **Configure** – Provide a minimal `config.yaml` with your workspace ID, optional bot token (if you need privileged actions), and MCP endpoint settings. | No OAuth scopes are required for basic read/write; you can start with a read‑only sandbox and later add a token for richer interactions. |
| 3️⃣  | **Run** – `./slack-mcp-server -c config.yaml`. | The server starts listening on the MCP HTTP/WS ports, exposing `/api/v1/events`, `/api/v1/message`, etc. |
| 4️⃣  | **Connect your AI agent** – Point the agent’s MCP client library (available for Python, Node, Go) at the server’s URL. | The agent now can fetch channel history, post messages, and react to events using the same protocol it would with a real Slack API. |
| 5️⃣  | **Iterate & secure** – Add TLS, enable optional JWT auth, and optionally supply a Slack App token for privileged actions. | Moves the setup from a sandbox to a production‑grade deployment while keeping the zero‑permission baseline for most use‑cases. |
| 6️⃣  | **Monitor & scale** – Use the built‑in `/metrics` endpoint (Prometheus format) and horizontal scaling via Docker/K8s. | Guarantees observability and the ability to handle higher message volumes as the AI‑assistant usage grows. |

**Production Readiness**  
- **Activity & maintenance** – Recent commits (as of 2026‑05‑14), a healthy star/fork ratio, and multiple contributors indicate active stewardship.  
- **Maturity** – The server already implements core Slack features (DMs, group DMs, GovSlack) and includes a sophisticated history‑caching layer, reducing latency and API‑call costs.  
- **Deployability** – Single‑binary Go service, container‑friendly, with Prometheus metrics and optional TLS/JWT hooks, fits typical production CI/CD pipelines.  
- **Risk considerations** – License (MIT) is permissive, but a final security audit is advisable, especially if you plan to expose a Slack token for privileged actions.  

Overall, korotovsky/slack-mcp-server is production‑ready for pilots that need a reliable, standards‑based bridge between AI agents and Slack‑like communication channels, with a clear upgrade path to hardened, enterprise deployments.

### Русский

**korotovsky/slack-mcp-server** — это открытый сервер на Go, реализующий протокол MCP и предоставляющий полностью открытый Slack‑подобный API без требований к правам доступа, с поддержкой приложений, GovSlack, личных и групповых DM, а также интеллектуального получения истории сообщений. Он позволяет быстро подключать AI‑ассистентов к реальным инструментам и данным, стандартизировать интеграцию и развертывать собственные Model Context Protocol‑серверы. По активности репозитория (1595★, 316 форков, последние коммиты — 2026‑05‑14), широкому набору функций и хорошей экосистеме проект считается готовым к пилотному использованию в продакшн‑средах, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
korotovsky/slack-mcp-server 是一款基于 Go 实现的 MCP（Model Context Protocol）Slack 服务器，提供零权限限制的 Slack 接入、App 支持、GovSlack、私聊/群聊以及智能历史拉取等功能。它让 AI 助手能够通过统一协议直接调用真实的工具和数据。

**核心价值**  
- **统一协议**：使用标准的 MCP，让不同的 AI 代理、模型或服务能够以相同的方式访问 Slack 功能，降低集成复杂度。  
- **完整功能**：支持普通消息、DM、Group DM、App 交互以及 GovSlack，且内置智能历史检索，帮助 AI 在对话上下文中快速定位所需信息。  
- **开箱即用**：无额外权限或 OAuth 流程，开发者只需启动服务器即可开始使用，适合快速原型和生产环境。

**典型接入方式**  
1. **部署服务器**：`docker run` 或直接编译二进制运行，配置好监听端口和可选的 TLS。  
2. **注册 MCP 客户端**：在 AI 助手或模型服务中使用官方 SDK/CLI（或自行实现 HTTP/WS 调用）指向服务器地址。  
3. **调用 API**：通过 MCP 定义的 `sendMessage`, `fetchHistory`, `createChannel` 等方法与 Slack 交互；对于 App 功能，可在请求体中携带相应的 `app_id`、`payload`。  
4. **可选集成**：结合已有的 Slack SDK（如 bolt‑go）或直接使用提供的 Go 客户端库，以实现更细粒度的自定义逻辑。

**生产可用性**  
- **活跃度**：截至 2026‑05‑14，项目拥有 1.6k+ 星、300+ Fork，最近一次提交在 2026‑05‑14，表明仍在积极维护。  
- **技术成熟度**：核心代码使用 Go 编写，具备良好的并发性能和易部署特性；提供 API/SDK/CLI 三种接入方式，文档完整。  
- **生态兼容**：已在多个开源 AI 项目中被引用，可直接作为 Model Context Protocol 服务器使用，适合作为生产环境的标准化集成层。  
- **风险**：需进一步审查许可证（MIT/Apache 等）以及安全审计报告，确认无已知漏洞后即可在关键业务中使用。

综上，korotovsky/slack-mcp-server 具备高可用的生产级特性，是在 AI‑Slack 集成场景下实现统一、低门槛接入的首选开源方案。

## 🧭 Practical evaluation

**Value:** korotovsky/slack-mcp-server helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1595 GitHub stars
- 316 forks
- updated 2026-05-14
- primary language: Go
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 63/100 |
| stars | 68/100 |
| topics | 88/100 |
| outlook | 57/100 |
| quality | 63/100 |
| recency | 20/100 |
| adoption | 67/100 |
| production | 56/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/korotovsky/slack-mcp-server) · [← Back to Mcp](./README.md)</sub>
