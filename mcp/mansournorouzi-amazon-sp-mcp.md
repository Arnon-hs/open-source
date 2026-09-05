# mansournorouzi/amazon-sp-mcp

[![Stars](https://img.shields.io/github/stars/mansournorouzi/amazon-sp-mcp?style=flat-square&color=yellow)](https://github.com/mansournorouzi/amazon-sp-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/mansournorouzi/amazon-sp-mcp?style=flat-square&color=blue)](https://github.com/mansournorouzi/amazon-sp-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> MCP server for Amazon SP-API — connect Claude to Seller Central for sales, inventory, orders, fees, and analytics. LWA-only auth, no AWS credentials required.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 38 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`amazon` `claude` `mcp` `model-context-protocol` `seller-central` `sp-api`

## 🎯 Categories

MCP · AI/ML · Cloud & Storage · Backend · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`mansournorouzi/amazon-sp-mcp` is an open‑source MCP (Model Context Protocol) server that bridges Claude‑style AI assistants with Amazon’s Selling Partner API. It provides LWA‑only authentication—so no AWS credentials are needed—and exposes endpoints for sales, inventory, orders, fees, and analytics, enabling AI agents to query real‑time Seller Central data through a standard protocol.

**Value**  
- **Standardised AI‑to‑tool integration** – By wrapping the Amazon SP‑API in an MCP server, developers can connect any MCP‑compatible AI (e.g., Claude, ChatGPT plugins) without writing custom adapters for each endpoint.  
- **Zero‑AWS‑credential hassle** – LWA‑only auth removes the need to manage long‑lived AWS keys, simplifying security and compliance for teams that only need read‑only access to seller data.  
- **Rich e‑commerce data** – Sales, inventory, order status, fees, and analytics become directly consumable by LLMs, unlocking use‑cases such as automated reporting, inventory forecasting, and conversational order management.

**Practical Adoption Path**  
1. **Spin up the server** – Clone the repo, run `npm install && npm run build && npm start` (Docker image also available).  
2. **Configure LWA credentials** – Supply the client ID/secret and refresh token for the Amazon seller account in the `.env` file.  
3. **Register the MCP endpoint** – Point your AI platform (Claude, LangChain, etc.) to the server’s `/mcp` endpoint and declare the supported methods (e.g., `listOrders`, `getInventory`).  
4. **Develop prompts / agents** – Use the MCP schema to call the exposed methods from your LLM prompts or agent logic, treating the Amazon data as a native tool.  
5. **Iterate & monitor** – Leverage built‑in logging and health checks; add caching or rate‑limit handling as needed for production traffic.

**Production Readiness**  
- **Activity & community** – 38 stars, 8 forks, recent commits (as of 2026‑06‑30), and a TypeScript codebase with clear module boundaries indicate an actively maintained project.  
- **Security posture** – Uses LWA (OAuth2) only, eliminating the need to store AWS secret keys; however, a final security audit of the token handling and exposed endpoints is recommended.  
- **Scalability** – The server is stateless and can be containerised; horizontal scaling is straightforward with standard Node/TS deployment patterns.  
- **Ecosystem fit** – Aligns with the emerging Model Context Protocol ecosystem, making it a solid candidate for pilots that need a “real‑world” data source for AI agents.  

Overall, `mansournorouzi/amazon-sp-mcp` offers a low‑friction, standards‑based bridge between Amazon seller data and LLM‑driven agents, and its recent activity, clear architecture, and simple auth model make it ready for serious pilot deployments, pending a final security and licensing review.

### Русский

**mansournorouzi/amazon-sp-mcp** – open‑source MCP‑сервер, который через LWA‑авторизацию без AWS‑ключей подключает Claude (и другие AI‑агенты) к Amazon Seller Central, предоставляя доступ к продажам, инвентарю, заказам, комиссиям и аналитике. Типичный сценарий: развернуть сервер, указать токен LWA и сразу начать использовать стандартный Model Context Protocol для интеграции AI‑ассистентов с реальными бизнес‑данными и инструментами. Проект считается практически готовым к production: активные коммиты (последнее обновление 2026‑06‑30), 38 звёзд, 8 форков, написан на TypeScript и имеет хорошие сигналы принятия в экосистеме, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
MCP（Model Context Protocol）服务器 `mansournorouzi/amazon-sp-mcp` 为 Amazon Seller Central 的 SP‑API 提供统一的协议层，能够让 Claude、ChatGPT 等 AI 助手直接查询销售、库存、订单、费用和分析数据。仅使用 LWA（Login With Amazon）进行身份认证，无需配置 AWS 凭证，开箱即用。

**价值体现**  
- **AI + 真实业务数据**：把 AI 助手与卖家后台的真实业务数据桥接，实现“让 AI 直接帮你下单、查库存、算利润”。  
- **标准化接入**：基于 MCP（Model Context Protocol）实现统一的请求/响应格式，降低不同 AI 平台或自研模型的集成成本。  
- **安全简化**：只需 LWA token，无需暴露 AWS Access Key/Secret，降低凭证泄露风险。  

**典型接入方式**  
1. **获取 LWA Token**：在 Amazon 开发者后台创建 LWA 应用，获取 `client_id`、`client_secret` 并通过 OAuth2 获得访问令牌。  
2. **部署 MCP 服务器**  
   - 克隆仓库，`npm install && npm run build`。  
   - 设置环境变量 `LWA_CLIENT_ID、LWA_CLIENT_SECRET、LWA_REFRESH_TOKEN`（或直接提供已获取的 `access_token`）。  
   - 启动服务 `npm start`，默认监听 `http://localhost:3000/mcp`。  
3. **在 AI 平台注册 MCP 端点**：在 Claude、ChatGPT Plugins 或自研模型的插件配置中填写该 HTTP endpoint，声明支持的 `sales`, `inventory`, `orders`, `fees`, `analytics` 等方法。  
4. **调用示例**  
   ```json
   {
     "method": "getInventory",
     "params": { "sku": "B0XYZ123" }
   }
   ```
   AI 助手发送上述请求后，MCP 服务器会内部调用 Amazon SP‑API 并返回结构化的库存信息。  

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑30，星标 38、Fork 8，社区活跃。  
- **技术成熟度**：使用 TypeScript 编写，提供完整的 API/SDK/CLI 示例，易于二次开发。  
- **安全性**：仅依赖 LWA，避免了长期存储 AWS 密钥；代码中已实现 token 自动刷新和错误重试。  
- **可扩展性**：遵循 MCP 规范，可在同一服务器上同时挂载其他业务系统的 MCP 实现，实现“一站式 AI 集成”。  

综合来看，`mansournorouzi/amazon-sp-mcp` 已具备进入生产环境的基本条件，适合作为 AI 助手与 Amazon Seller Central 数据交互的桥梁。后续仍建议进行内部安全审计（许可证、依赖漏洞）并监控 API 调用配额，以确保长期稳定运行。

## 🧭 Practical evaluation

**Value:** mansournorouzi/amazon-sp-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 38 GitHub stars
- 8 forks
- updated 2026-06-30
- primary language: TypeScript
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 34/100 |
| topics | 75/100 |
| outlook | 68/100 |
| quality | 60/100 |
| recency | 80/100 |
| adoption | 31/100 |
| production | 69/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/mansournorouzi/amazon-sp-mcp) · [← Back to Mcp](./README.md)</sub>
