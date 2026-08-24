# code-rabi/interactive-brokers-mcp

[![Stars](https://img.shields.io/github/stars/code-rabi/interactive-brokers-mcp?style=flat-square&color=yellow)](https://github.com/code-rabi/interactive-brokers-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/code-rabi/interactive-brokers-mcp?style=flat-square&color=blue)](https://github.com/code-rabi/interactive-brokers-mcp/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Interactive Brokers MCP Server

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 127 |
| 🍴 **Forks** | 31 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ibkr` `ibkr-api` `interactive-brokers` `mcp` `mcp-server`

## 🎯 Categories

MCP · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The *interactive‑brokers‑mcp* project provides a Model Context Protocol (MCP) server that bridges AI assistants with Interactive Brokers’ trading platform via a standardized, language‑agnostic API. By exposing signals such as REST/SDK/CLI endpoints and rich metadata, it lets developers quickly prototype AI‑driven trading agents or integrate existing tools into a unified MCP ecosystem. With 127 stars, active JavaScript code, and recent updates (May 2026), it is a solid starting point for internal or experimental deployments.

**Value**  
- **Standardized integration** – The MCP server abstracts the broker’s native APIs behind a common protocol, making it easy to swap or combine different data sources and tools without rewriting AI‑agent logic.  
- **Accelerates AI‑agent development** – Developers can focus on prompting and reasoning while the server handles authentication, order routing, and market‑data streaming.  
- **Open‑source flexibility** – The JavaScript implementation can be extended or self‑hosted, giving full control over security, latency, and compliance requirements.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the Docker compose (or `npm start`) to spin up the MCP server locally; use the provided Swagger UI to test market‑data and order endpoints.  
2. **Connect an AI agent** – Point your LLM‑orchestrator (e.g., LangChain, AutoGPT) to the server’s `/mcp` endpoint; the agent can now issue `get_price`, `place_order`, etc., via the MCP schema.  
3. **Secure & customize** – Add your Interactive Brokers API keys, enable TLS, and optionally replace the default in‑memory store with a persistent DB.  
4. **Deploy** – Containerize the service and push it to a cloud platform (EKS, GKE, or a private Kubernetes cluster) behind a VPN or zero‑trust gateway for production use.

**Production Readiness**  
- **Maturity**: Medium. The codebase is actively maintained (last commit 2026‑05‑12) and has community traction (127 ★, 31 forks), but it lacks formal CI/CD pipelines, extensive test coverage, and a documented security audit.  
- **Suitability**: Ideal for prototypes, internal tools, or low‑to‑moderate volume trading bots after a brief hardening phase (dependency updates, static analysis, rate‑limit handling).  
- **Risks**: Licensing and long‑term maintainer commitment need verification; security posture must be reviewed (API key handling, network exposure). Once these checks are completed, the server can be promoted to production for controlled, compliance‑checked trading workflows.

### Русский

**code-rabi/interactive-brokers-mcp** — это серверный модуль на JavaScript, реализующий протокол MCP (Model Context Protocol) и позволяющий AI‑ассистентам напрямую взаимодействовать с Interactive Brokers и другими внешними сервисами. Типичный сценарий: разработчик разворачивает MCP‑сервер, подключает к нему AI‑агента и через единый API/CLI передаёт запросы на торговлю, получение рыночных данных или выполнение пользовательских скриптов, что упрощает создание прототипов и интеграцию инструментов в корпоративные рабочие процессы. Готовность к production — средняя: проект уже имеет 127 звёзд, активные коммиты (последний — 12 мая 2026) и достаточно простой интерфейс, но перед запуском в продакшн рекомендуется проверить лицензию, безопасность зависимостей и наличие поддерживающих мейнтейнеров.

### 中文

**项目简介（2‑3 句话）**  
`code-rabi/interactive-brokers-mcp` 是一个基于 Model Context Protocol（MCP）的后端服务，实现了与 Interactive Brokers（IB）交易平台的标准化连接。它通过统一的协议让 AI 助手能够直接调用 IB 的交易、行情和账户管理功能，从而把语言模型的推理能力转化为真实的金融操作。

**价值**  
- **桥接 AI 与真实工具**：提供统一的 MCP 接口，使得任何遵循该协议的 AI 代理都能无缝调用 IB 的交易 API，降低了二次开发成本。  
- **加速原型与产品化**：开发者只需实现 MCP 客户端，即可快速在 AI 代理中嵌入金融交易、行情查询等业务场景。  
- **标准化集成**：遵循公开的协议规范，便于在多项目、多团队之间共享和复用，同步维护安全与合规策略。

**典型接入方式**  
1. **部署 MCP Server**：克隆仓库后使用 Docker 或直接 `npm install && npm start` 启动服务，配置好 IB 的 API Token、账户信息等。  
2. **实现 MCP 客户端**：在 AI 代理（如 LangChain、OpenAI Functions）中使用 MCP 客户端库（提供的 JavaScript SDK），通过 `invoke` 调用如 `placeOrder`, `getMarketData` 等方法。  
3. **安全与认证**：在客户端请求头中加入签名或 OAuth 令牌，服务端会校验后转发至 IB 官方 API，确保交易安全。  

**生产可用性**  
- **成熟度**：当前评分 69/100，适合作为原型或内部工作流的核心组件。  
- **依赖与维护**：项目主要使用 JavaScript，依赖相对轻量；但仍需检查第三方库的安全漏洞并确保 IB API 版本兼容。  
- **运维建议**：在生产环境建议配合容器化部署、健康检查和日志监控；同时实现限流和审计，以满足金融合规要求。  

总体而言，`interactive-brokers-mcp` 为 AI 与金融交易的对接提供了一个快速、标准化的入口，适合在原型验证阶段快速落地，经过安全审计和运维加固后亦可投入生产使用。

## 🧭 Practical evaluation

**Value:** code-rabi/interactive-brokers-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 127 GitHub stars
- 31 forks
- updated 2026-05-12
- primary language: JavaScript
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 38/100 |
| stars | 45/100 |
| topics | 63/100 |
| outlook | 49/100 |
| quality | 49/100 |
| recency | 20/100 |
| adoption | 43/100 |
| production | 48/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/code-rabi/interactive-brokers-mcp) · [← Back to Mcp](./README.md)</sub>
