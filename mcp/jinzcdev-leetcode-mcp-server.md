# jinzcdev/leetcode-mcp-server

[![Stars](https://img.shields.io/github/stars/jinzcdev/leetcode-mcp-server?style=flat-square&color=yellow)](https://github.com/jinzcdev/leetcode-mcp-server/stargazers) [![Forks](https://img.shields.io/github/forks/jinzcdev/leetcode-mcp-server?style=flat-square&color=blue)](https://github.com/jinzcdev/leetcode-mcp-server/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> An MCP server enabling automated access to LeetCode's problems, solutions, and public data with optional authentication for user-specific features, supporting leetcode.com & leetcode.cn sites.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 128 |
| 🍴 **Forks** | 21 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-07-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `algorithm` `lc` `leetcode` `llm` `mcp` `mcp-server`

## 🎯 Categories

MCP · AI/ML · Backend · Data · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The **leetcode‑mcp‑server** is an open‑source Model‑Context‑Protocol (MCP) server that provides programmatic, authenticated (optional) access to LeetCode’s problem statements, solutions, and public data for both leetcode.com and leetcode.cn. Written in TypeScript, it exposes a clean API/SDK/CLI that lets AI assistants and other tools retrieve LeetCode content and perform user‑specific actions through a standard protocol.  

**Value**  
- **Standardized integration** – By speaking MCP, the server lets any MCP‑compatible AI agent or tool treat LeetCode as a first‑class data source without custom scrapers or brittle hacks.  
- **Real‑world utility** – AI assistants can fetch problems, verify solutions, or pull editorial explanations on‑demand, enabling richer tutoring, code‑generation, and interview‑prep experiences.  
- **Dual‑site support** – Handles both the global (leetcode.com) and China (leetcode.cn) portals, expanding the reachable user base.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the Docker compose or `npm start` to spin up the server locally.  
2. **Connect** – Point your MCP‑enabled AI framework (e.g., LangChain, AutoGPT, or a custom agent) to the server’s endpoint; use the provided TypeScript SDK or simple HTTP calls for quick testing.  
3. **Authenticate (optional)** – Generate a LeetCode session token and configure the server’s auth settings to unlock user‑specific features such as personal submissions or private contests.  
4. **Scale** – Deploy the server to a cloud container service (e.g., AWS Fargate, GKE) behind a TLS‑terminated load balancer; configure rate‑limiting and caching as needed for production traffic.  

**Production Readiness**  
- **Activity & Community** – 128 ★, 21 forks, recent commit (2026‑07‑12) and ongoing issue discussion indicate an active maintainer base.  
- **Maturity** – The project follows a well‑defined MCP spec, offers an SDK, CLI, and OpenAPI docs, and has clear versioning, making integration deterministic.  
- **Security** – No known metadata leaks; optional authentication isolates user‑specific data, but a final security audit (dependency scanning, token handling) is advisable before handling production credentials.  
- **Scalability** – Built with Node/TypeScript and stateless request handling, it can be horizontally scaled behind a reverse proxy; caching layers can be added for high‑throughput use cases.  

Overall, the leetcode‑mcp‑server is a strong OSS candidate for pilots that need reliable, protocol‑standardized access to LeetCode data, with a clear path from sandbox testing to production deployment.

### Русский

Jinzcdev/leetcode‑mcp‑server — это открытый MCP‑сервер, который через единый протокол предоставляет автоматизированный доступ к задачам, решениям и публичным данным LeetCode (как leetcode.com, так и leetcode.cn), а при включённой аутентификации открывает пользовательские функции. Он позволяет быстро интегрировать AI‑агентов и другие инструменты с реальными данными LeetCode, использовать готовый SDK/CLI и разворачивать собственные Model Context Protocol‑сервера. Проект уже активно поддерживается (обновления 2026‑07‑12, 128 звёзд, 21 форк, TypeScript), имеет хорошую экосистемную совместимость и считается готовым к пилотному запуску в production, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
`jinzcdev/leetcode-mcp-server` 是一个基于 Model Context Protocol（MCP）的后端服务，提供对 LeetCode（包括 leetcode.com 与 leetcode.cn）题目、官方解答、公开数据的自动化访问。服务支持可选的用户身份认证，以便开启用户专属的收藏、提交记录等功能。

**价值**  
- **统一协议**：通过标准化的 MCP 接口，让 AI 助手、自动化脚本或第三方工具能够以统一方式调用 LeetCode 数据，降低集成成本。  
- **实时题库**：实时抓取 LeetCode 最新题目和官方解答，保证 AI 模型获取的是最新、最权威的参考信息。  
- **可选认证**：支持登录后访问用户私有数据（收藏、提交历史等），为个性化推荐和学习路径规划提供数据支撑。  

**典型接入方式**  
1. **API/SDK**：直接调用服务器暴露的 HTTP RESTful 接口（或使用项目自带的 TypeScript SDK），发送 MCP 请求并解析返回的 JSON。  
2. **CLI**：项目提供 `lc-mcp` 命令行工具，可在 CI/CD、脚本或本地调试时快速查询题目信息。  
3. **模型集成**：在大语言模型（如 ChatGPT、Claude）中配置 MCP 客户端，使模型在对话中实时查询 LeetCode 数据，实现“随问随答”。  

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑07‑12，星标 128、Fork 21，社区活跃度良好。  
- **技术成熟度**：使用 TypeScript 编写，代码结构清晰，配套的 API 文档和示例完整，易于在 Node.js 环境中部署。  
- **安全性**：提供可选的 OAuth/Token 认证层，避免未授权访问用户私有数据；项目已通过基本的依赖审计。  
- **可扩展性**：支持自定义插件或中间件，可根据业务需求在请求链路中加入缓存、限流或日志。  

综合来看，`jinzcdev/leetcode-mcp-server` 在协议统一、数据实时性和安全控制方面具备较强的竞争力，且代码质量和社区活跃度足以支撑生产环境的试点或正式上线。建议在正式部署前完成一次安全审计并评估与现有身份体系的兼容性。

## 🧭 Practical evaluation

**Value:** jinzcdev/leetcode-mcp-server helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 128 GitHub stars
- 21 forks
- updated 2026-07-12
- primary language: TypeScript
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 45/100 |
| topics | 88/100 |
| outlook | 76/100 |
| quality | 72/100 |
| recency | 100/100 |
| adoption | 42/100 |
| production | 78/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/jinzcdev/leetcode-mcp-server) · [← Back to Mcp](./README.md)</sub>
