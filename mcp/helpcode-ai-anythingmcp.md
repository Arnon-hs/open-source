# HelpCode-ai/anythingmcp

[![Stars](https://img.shields.io/github/stars/HelpCode-ai/anythingmcp?style=flat-square&color=yellow)](https://github.com/HelpCode-ai/anythingmcp/stargazers) [![Forks](https://img.shields.io/github/forks/HelpCode-ai/anythingmcp?style=flat-square&color=blue)](https://github.com/HelpCode-ai/anythingmcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-78%2F100-brightgreen?style=flat-square)](#)

> Self-hosted MCP gateway & API-to-MCP bridge. Convert REST/SOAP/WSDL/GraphQL/SQL APIs into MCP servers for Claude, ChatGPT, Gemini, Copilot, Cursor. OpenAPI/Postman/WSDL import, OAuth2, RBAC, audit log. 29 pre-built adapters (DHL, DATEV, Weclapp, Personio, Handelsregister, Shopware...). Source-available.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 35 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 78/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `anthropic` `api-gateway` `api-to-mcp` `chatgpt` `claude` `database` `gemini` `graphql` `llm-tools` `mcp` `mcp-gateway`

## 🎯 Categories

MCP · AI/ML · Frontend · Backend · Data

## 📝 Summary

### English

**Brief summary**  
AnythingMCP (HelpCode‑ai/anythingmcp) is a self‑hosted gateway that turns any REST, SOAP, GraphQL, SQL or OpenAPI/WSDL endpoint into a Model‑Context‑Protocol (MCP) server, letting LLMs such as Claude, ChatGPT, Gemini, Copilot or Cursor invoke real‑world tools and data. It ships with 29 ready‑made adapters (e.g., DHL, DATEV, Shopware, Personio) and provides OAuth2, RBAC, audit logging, and a CLI/API for rapid deployment.

**Value proposition**  
- **Unified AI‑to‑tool interface** – By exposing external services through the standard MCP, developers can plug any LLM into existing business systems without writing custom prompt‑engineering or wrapper code.  
- **Accelerated integration** – The built‑in adapters cover common SaaS and on‑premise systems, turning a “point‑and‑click” API import into a functioning MCP endpoint in minutes.  
- **Governance & security** – Built‑in OAuth2, role‑based access control and audit logs give enterprises the controls they need to expose sensitive back‑ends to AI agents safely.

**Practical adoption path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | **Spin up the service** – Clone the repo, run `docker compose up` (or use the provided Helm chart) on a dev cluster. | Quick, reproducible environment; no compile‑time dependencies. |
| 2️⃣  | **Import an API** – Upload an OpenAPI/Swagger, Postman collection or WSDL via the UI or CLI (`anythingmcp import`). | Generates the MCP schema automatically, handling auth, request/response mapping. |
| 3️⃣  | **Configure security** – Attach OAuth2 client credentials or API keys, define RBAC roles for each adapter. | Ensures only authorized AI agents or users can call the endpoints. |
| 4️⃣  | **Test with an LLM** – Use the MCP client library (or the built‑in test console) to call the new MCP endpoint from Claude/ChatGPT. | Verifies end‑to‑end connectivity and data shaping. |
| 5️⃣  | **Deploy to production** – Promote the Docker/Helm deployment to a production namespace, enable audit logging and monitoring (Prometheus metrics are exposed). | Provides observability and compliance for a production‑grade rollout. |
| 6️⃣  | **Iterate & extend** – Add custom adapters or tweak generated ones; the TypeScript SDK lets you write bespoke transformation logic if needed. | Keeps the platform flexible as business requirements evolve. |

**Production readiness**  
- **Activity & community** – The repo shows recent commits (last update 2026‑05‑11), 35 ★, 5 forks, and a TypeScript codebase with ~20 topic tags, indicating an engaged maintainer and a modest but growing community.  
- **Feature completeness** – Core MCP gateway, OpenAPI/WSDL import, OAuth2, RBAC, audit logs, and a sizable catalog of pre‑built adapters are all production‑grade components.  
- **Observability** – Built‑in Prometheus metrics, structured logs, and an audit trail make it suitable for enterprise monitoring and compliance.  
- **Risk considerations** – The license is source‑available (check exact SPDX identifier), and a formal security audit is still pending; organizations should perform their own vulnerability scan and verify maintainer responsiveness before a critical rollout.  

Overall, AnythingMCP offers a high‑value, low‑friction way to expose existing APIs to LLMs via a standardized protocol, and its recent activity, feature set, and operational tooling make it ready for pilot projects and, with proper security vetting, for production deployment.

### Русский

HelpCode‑ai/anythingmcp — это self‑hosted шлюз MCP и мост API‑to‑MCP, позволяющий мгновенно превратить любые REST/SOAP/WSDL/GraphQL/SQL‑интерфейсы в серверы Model Context Protocol для Claude, ChatGPT, Gemini, Copilot и других ассистентов. Типичный сценарий: импортировать OpenAPI/Postman/WSDL, настроить OAuth2 и RBAC, выбрать один из 29 готовых адаптеров (DHL, DATEV, Shopware и пр.) и запустить MCP‑сервер, через который AI‑агенты получают доступ к реальным бизнес‑инструментам и данным. Проект активно поддерживается (обновления 2026‑05‑11, 35 звёзд, 5 форков), написан на TypeScript и готов к пилотному внедрению в production после финального аудита лицензии и безопасности.

### 中文

**项目简介**  
HelpCode‑ai/anythingmcp 是一套自托管的 **MCP（Model Context Protocol）网关 & API‑to‑MCP 桥梁**，能够把任意 REST、SOAP、WSDL、GraphQL、SQL 等传统接口快速包装成符合 MCP 规范的服务，让 Claude、ChatGPT、Gemini、Copilot、Cursor 等大模型直接调用真实业务系统。项目提供 OpenAPI / Postman / WSDL 导入、OAuth2 鉴权、基于角色的访问控制（RBAC）以及审计日志，并内置 29 套常用业务适配器（如 DHL、DATEV、Weclapp、Personio、Handelsregister、Shopware 等），代码全部开源（Source‑available）。

---

### 价值点

1. **统一协议、快速集成**：无需为每个后端系统单独实现大模型插件，只要有标准化的 API，即可一键生成 MCP 服务，极大降低集成成本。  
2. **安全合规**：内置 OAuth2、RBAC 与审计日志，满足企业对身份、权限和审计的基本要求。  
3. **丰富适配器**：29 个即插即用的业务适配器覆盖物流、财务、人事、电商等常见场景，直接开箱即用。  
4. **开源可自托管**：企业可以在内部网络中部署，完全掌控数据流向与安全边界。  

---

### 典型接入方式

| 步骤 | 操作 | 说明 |
|------|------|------|
| 1️⃣ 部署 | 使用 Docker Compose / Helm Chart 将 `anythingmcp` 部署到 Kubernetes、Docker 或本地机器。 | 项目提供官方镜像，默认使用 TypeScript 编译的 Node.js 运行时。 |
| 2️⃣ 导入 API | 通过 UI 或 CLI 导入 OpenAPI、Postman Collection、WSDL 或直接填写 GraphQL/SQL 配置。 | 支持自动生成对应的 MCP 接口描述（`mcp.yaml`）。 |
| 3️⃣ 配置鉴权 | 在管理后台配置 OAuth2 客户端、API‑Key 或自定义身份提供者，并为不同角色分配访问权限。 | RBAC 通过角色‑资源‑操作矩阵实现。 |
| 4️⃣ 启动 MCP 服务 | 系统自动生成并启动对应的 MCP 端点（如 `grpc://host:50051`），并在 UI 中展示可调用的函数列表。 | 大模型通过标准的 MCP SDK（如 `@mcp/client`）即可发现并调用。 |
| 5️⃣ 调用示例 | 在 Claude、ChatGPT 等大模型的插件代码中使用 `mcp.call("adapterName.method", {...})`。 | 返回值即为后端 API 的原始响应或经过适配的结构化数据。 |

> **快速原型**：只需在几分钟内完成 Docker 启动 → OpenAPI 导入 → 生成 MCP → 在 Playground 中测试调用，即可验证业务可行性。

---

### 生产可用性评估

| 维度 | 现状 | 结论 |
|------|------|------|
| **代码活跃度** | 最近一次提交：2026‑05‑11；GitHub ★35、Fork 5；20+ 主题标签 | 活跃，适合生产环境评估 |
| **技术栈成熟度** | 主语言 TypeScript，依赖成熟的 Node.js、gRPC、OAuth2 库 | 稳定 |
| **安全与合规** | 支持 OAuth2、RBAC、审计日志；仍需自行审计依赖的 NPM 包安全性 | 基础安全满足企业需求，建议做一次依赖漏洞扫描 |
| **部署便利性** | 提供 Docker Compose、Helm Chart、CLI 一键部署脚本 | 易于在云端或本地私有环境部署 |
| **社区与文档** | 官方 README、API 导入指南、适配器使用手册较完整；社区讨论较少 | 文档足够，社区规模小但可自行维护 |
| **可扩展性** | 通过插件机制可以自定义适配器；支持自定义函数、拦截器 | 高度可定制 |
| **总体评分** | 78/100 | **适合作为正式项目的 Pilot 或生产候选**，在完成安全审计和运维流程后即可投入使用。 |

**结论**：HelpCode‑ai/anythingmcp 为企业提供了一条从传统业务系统到大模型的“即插即用”路径，部署简单、功能完整、具备企业级安全控制，经过一次内部安全审计和运维方案落地后即可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** HelpCode-ai/anythingmcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 35 GitHub stars
- 5 forks
- updated 2026-05-11
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 33/100 |
| topics | 100/100 |
| outlook | 82/100 |
| quality | 68/100 |
| recency | 100/100 |
| adoption | 29/100 |
| production | 77/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/HelpCode-ai/anythingmcp) · [← Back to Mcp](./README.md)</sub>
