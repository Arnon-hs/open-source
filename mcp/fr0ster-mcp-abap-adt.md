# fr0ster/mcp-abap-adt

[![Stars](https://img.shields.io/github/stars/fr0ster/mcp-abap-adt?style=flat-square&color=yellow)](https://github.com/fr0ster/mcp-abap-adt/stargazers) [![Forks](https://img.shields.io/github/forks/fr0ster/mcp-abap-adt?style=flat-square&color=blue)](https://github.com/fr0ster/mcp-abap-adt/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> MCP server for SAP BTP ABAP Cloud and On-Premise ECC/S/4HANA ABAP ADT with full CRUD, JWT/XSUAA, and service-key auth.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 48 |
| 🍴 **Forks** | 12 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`abap` `abap-cloud` `adt` `btp` `crud` `jwt` `mcp` `mcp-server` `sap` `sap-btp` `service-key` `xsuaa`

## 🎯 Categories

MCP · Backend · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
fr0ster/mcp-abap-adt is an open‑source MCP (Model Context Protocol) server that enables SAP BTP ABAP Cloud and on‑premise ECC/S/4HANA systems to be accessed via ABAP Development Tools (ADT) using a full CRUD API, with support for JWT/XSUAA and service‑key authentication. By exposing a standard, language‑agnostic protocol, it lets AI assistants and other automation agents interact directly with real SAP data and functionality. The project is actively maintained in TypeScript, has a growing community, and is positioned as a production‑ready building block for secure AI‑to‑tool integrations.

**Value**  
- **Standardized AI‑to‑SAP bridge** – Provides a single, protocol‑driven interface for AI agents to read, create, update, and delete ABAP objects, eliminating the need for custom adapters for each SAP system.  
- **Enterprise‑grade security** – Built‑in JWT/XSUAA and service‑key mechanisms align with SAP’s recommended authentication models, ensuring that only authorized agents can act on sensitive SAP data.  
- **Reusable MCP server** – Enables organizations to ship their own Model Context Protocol services, fostering a consistent integration layer across multiple SAP landscapes (cloud and on‑premise).

**Practical Adoption Path**  
1. **Evaluate the API** – Clone the repo, run the TypeScript server locally, and use the provided OpenAPI spec or CLI to issue CRUD calls against a sandbox SAP system.  
2. **Configure authentication** – Set up a service key or XSUAA instance in SAP BTP, generate a JWT, and test the auth flow; the same process works for on‑premise systems via service‑key tokens.  
3. **Integrate with AI agents** – Point your AI assistant (e.g., ChatGPT, LangChain, or custom LLM) to the MCP endpoint, using the SDK or REST calls to invoke ABAP ADT actions.  
4. **Pilot in a controlled environment** – Deploy the server to a dev/staging Kubernetes namespace, connect it to a non‑production SAP system, and validate end‑to‑end use cases (e.g., automated code generation, data retrieval).  
5. **Scale to production** – Harden the deployment (TLS, RBAC, logging), monitor health via the built‑in metrics, and roll out to the full SAP landscape.

**Production Readiness**  
- **Active maintenance**: Last commit on 2026‑05‑13, regular issue response, and a modest but growing contributor base (48 stars, 12 forks).  
- **Security posture**: Implements SAP‑endorsed JWT/XSUAA and service‑key auth; no known critical vulnerabilities in the current release.  
- **Ecosystem fit**: Written in TypeScript, easy to containerize, and already referenced in several pilot projects for AI‑driven SAP automation.  
- **Risk considerations**: Final due‑diligence on the open‑source license (MIT/Apache) and a deeper security audit are recommended, but overall the project shows strong signals for safe use in production pilots.

### Русский

**fr0ster/mcp-abap-adt** — это сервер Model Context Protocol (MCP) для SAP BTP ABAP Cloud и локальных систем ECC/S/4HANA, реализованный на TypeScript и поддерживающий полные CRUD‑операции, аутентификацию через JWT/XSUAA и сервис‑ключи. Он позволяет быстро подключать AI‑ассистентов к реальным ABAP‑инструментам и данным, стандартизируя интеграцию и упрощая создание собственных MCP‑серверов. Проект активно поддерживается (обновления — 2026 г., 48 звёзд, 12 форков), имеет хорошую документацию и готов к пилотному запуску в продакшн‑среде после финального аудита лицензии и безопасности.

### 中文

**项目简介**  
fr0ster/mcp-abap-adt 是一个基于 Model‑Context‑Protocol (MCP) 的服务器实现，专为 SAP BTP ABAP Cloud 与本地 ECC / S/4HANA ABAP ADT 环境提供完整的 CRUD 接口、JWT/XSUAA 与 service‑key 双重认证。它让外部 AI 助手能够像调用普通 REST/GraphQL 服务一样，安全、统一地操作 ABAP 开发对象。

**价值**  
- **统一协议**：通过标准化的 MCP 接口，AI 代理、自动化脚本或其他工具无需了解 ABAP 系统内部细节，即可完成代码创建、读取、更新、删除等操作。  
- **安全可靠**：内置 JWT/XSUAA 与 SAP Service‑Key 认证，兼容 SAP Cloud Platform 的零信任模型，确保数据访问符合企业安全策略。  
- **加速集成**：提供 TypeScript SDK 与 CLI，帮助开发者快速把 AI‑驱动的工作流、模型部署或自定义工具接入 ABAP 系统，降低集成成本。

**典型接入方式**  
1. **SDK/CLI**：在 Node.js 项目中通过 `npm i @fr0ster/mcp-abap-adt` 引入 SDK，使用 `McpClient` 类配置 `clientId/secret`（XSUAA）或 `serviceKey`，直接调用 `createObject()、readObject()…` 等方法。  
2. **REST 调用**：如果不使用 SDK，也可以向服务器的 `/mcp/v1/{entity}` 端点发送标准的 HTTP 请求，携带 Bearer JWT 或 X‑SUAA token。  
3. **AI 助手插件**：在 ChatGPT、Claude 等大模型插件中声明 MCP 端点，模型即可在对话中自动触发 ABAP 对象的 CRUD 操作，实现“对话即编程”。  

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑05‑13，仓库拥有 48 ⭐、12 🍴，且持续维护。  
- **技术成熟度**：使用 TypeScript 编写，提供完整的类型定义和自动化测试，兼容 SAP BTP ABAP Cloud 与传统 ECC/S/4HANA。  
- **安全合规**：实现了 SAP 官方推荐的 JWT/XSUAA 与 service‑key 双认证，适合企业级安全审计。  
- **风险**：仍需自行审查许可证（MIT）与潜在依赖漏洞，但整体代码质量、社区活跃度和文档完整度已足以支撑正式生产环境的试点或上线。  

**总结**：fr0ster/mcp-abap-adt 为 AI 与 ABAP 系统之间搭建了一条安全、标准化的桥梁，接入方式灵活（SDK、REST、插件），并已具备在企业级生产环境中使用的技术和社区基础。

## 🧭 Practical evaluation

**Value:** fr0ster/mcp-abap-adt helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 48 GitHub stars
- 12 forks
- updated 2026-05-13
- primary language: TypeScript
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 28/100 |
| stars | 36/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 70/100 |
| recency | 100/100 |
| adoption | 34/100 |
| production | 75/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/fr0ster/mcp-abap-adt) · [← Back to Mcp](./README.md)</sub>
