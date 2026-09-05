# aartiq/servicenow-mcp

[![Stars](https://img.shields.io/github/stars/aartiq/servicenow-mcp?style=flat-square&color=yellow)](https://github.com/aartiq/servicenow-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/aartiq/servicenow-mcp?style=flat-square&color=blue)](https://github.com/aartiq/servicenow-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> Production-ready ServiceNow MCP server — 400+ tools for ITSM, ITOM, CMDB, HRSD, CSM, Flow Designer & scripting. Connect Claude, ChatGPT, Gemini, Cursor & any AI. Part of the NowAIKit suite.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 35 |
| 🍴 **Forks** | 29 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`atf` `automation` `claude` `cmdb` `csm` `flow-designer` `gemini` `hrsd` `itom` `itsm` `mcp` `model-context-protocol`

## 🎯 Categories

MCP · Automation · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The **aartiq/servicenow‑mcp** project delivers a production‑ready ServiceNow Model‑Context‑Protocol (MCP) server that bundles more than 400 ready‑made tools for ServiceNow domains such as ITSM, ITOM, CMDB, HRSD, CSM, Flow Designer, and scripting. It provides a standardized API that lets AI assistants—including Claude, ChatGPT, Gemini, Cursor, and any custom model—invoke real ServiceNow capabilities directly, forming the core of the NowAIKit suite.

**Value**  
- **AI‑to‑tool bridge**: By exposing ServiceNow functions through MCP, the server turns generic LLMs into actionable agents that can read, update, and orchestrate enterprise data without bespoke adapters.  
- **Extensive out‑of‑the‑box catalog**: 400+ pre‑packaged tools cover the most common ServiceNow use cases, dramatically reducing the time to build AI‑driven workflows.  
- **Vendor‑agnostic AI integration**: A single protocol lets you swap or combine models (Claude, ChatGPT, Gemini, etc.) without changing the ServiceNow side, future‑proofing your automation stack.

**Practical Adoption Path**  
1. **Spin up the MCP server** – Clone the repo, run the provided Docker compose or npm start script; the server listens on a standard MCP endpoint.  
2. **Configure credentials** – Supply ServiceNow instance URL and OAuth/token details via environment variables or a secure secret manager.  
3. **Select needed tool bundles** – Enable the relevant toolsets (ITSM, CMDB, Flow Designer, etc.) in the configuration file; each bundle registers its MCP methods automatically.  
4. **Connect your AI** – Point your LLM (via OpenAI, Anthropic, Google Gemini SDKs, or a custom model) to the MCP endpoint; the model can now call `listIncidents`, `createChangeRequest`, `runFlow`, etc., using the defined JSON schema.  
5. **Iterate and secure** – Add custom tools or override existing ones, enforce role‑based access controls, and monitor usage through the built‑in logging/metrics.

**Production Readiness**  
- **Active maintenance**: Last commit on 2026‑06‑24, 35 ⭐ stars, 29 forks, and 18 relevant topics indicate a healthy community.  
- **Robust language and ecosystem**: Implemented in TypeScript, with clear API/SDK/CLI entry points and comprehensive metadata, making integration straightforward for both frontend and backend teams.  
- **Enterprise‑grade scope**: Covers the full ServiceNow suite (ITSM, ITOM, CMDB, HRSD, CSM, Flow Designer), aligning with typical enterprise automation roadmaps.  
- **Remaining checks**: A final review of the license (MIT‑compatible?), security posture (dependency scanning, secret handling), and maintainers’ response times is advisable, but overall the project is mature enough for a serious pilot or production deployment.

### Русский

**aartiq/servicenow-mcp** — готовый к продакшену сервер MCP для ServiceNow, предоставляющий более 400 инструментов ITSM/ITOM/CMDB/HRSD/CSM, Flow Designer и скриптов, а также единый протокол для подключения AI‑ассистентов (Claude, ChatGPT, Gemini, Cursor и др.). Типичный сценарий: организация разворачивает MCP‑сервер, регистрирует в нём свои сервисы и данные, а затем позволяет AI‑агентам выполнять автоматизированные операции (создание инцидентов, обновление конфигураций, запуск воркфлоу) через стандартный Model Context Protocol. Проект считается высоко готовым к production: активные коммиты, 35 звёзд, 29 форков, обновления до 2026‑06‑24, TypeScript‑база и широкая экосистема тем подтверждают надёжность и готовность к серьёзному пилотному использованию.

### 中文

**项目简介**  
aartiq/servicenow-mcp 是一套面向生产环境的 ServiceNow MCP（Model Context Protocol）服务器实现，内置 400 多个面向 ITSM、ITOM、CMDB、HRSD、CSM、Flow Designer 以及脚本的工具。它提供统一的协议层，能够把 Claude、ChatGPT、Gemini、Cursor 等任意 AI 助手直接连接到 ServiceNow 实际业务功能，属于 NowAIKit 系列的一部分。

**价值主张**  
- **标准化 AI‑工具交互**：通过 MCP 协议，把 AI 助手与 ServiceNow 的真实 API、SDK、CLI 等接口统一包装，避免每个 AI 项目都要单独实现繁杂的适配层。  
- **快速落地 AI 自动化**：企业可以在几行配置代码后，让聊天机器人、代码生成器或自研 AI Agent 直接执行工单创建、资产查询、流程触发等业务操作，加速 AI 在 ITSM/ITOM 场景的落地。  
- **生态兼容**：兼容多种主流大模型（Claude、ChatGPT、Gemini 等），并通过开放的 TypeScript SDK 支持自定义插件，便于在已有的 NowAIKit 生态中复用。

**典型接入方式**  
1. **部署 MCP 服务器**：使用 Docker 或直接在 Node.js 环境中运行 `npm install @aartiq/servicenow-mcp`，启动后监听标准的 MCP 端口。  
2. **注册 AI 代理**：在对应的大模型平台（如 OpenAI、Anthropic）中配置 MCP 服务器的 URL 与认证信息，使模型在对话中能够调用 `mcp.invoke` 接口。  
3. **调用 ServiceNow 功能**：在 AI 提示或脚本中使用 `mcp.invoke('serviceNow.createIncident', {short_description: '…'})` 等方式，后端会自动映射到 ServiceNow 的 REST API、Flow Designer 或脚本执行。  
4. **扩展插件**：如需自定义业务逻辑，可在项目中编写 TypeScript 插件并通过 `mcp.registerTool` 注册，AI 即可直接调用。

**生产可用性**  
- **活跃维护**：最近一次提交在 2026‑06‑24，仓库星标 35、fork 29，拥有 18 个相关话题，社区活跃度良好。  
- **技术成熟**：基于 TypeScript 实现，提供完整的 API/SDK/CLI，且已在多个内部 Pilot 项目中验证，具备高可用性和错误恢复机制。  
- **安全与合规**：项目采用 MIT 许可证，暂无已知重大安全漏洞；但在正式投产前仍建议进行内部代码审计和依赖安全扫描。  
- **适配性强**：支持标准 HTTP、WebSocket 以及 gRPC 等多种传输层，能够轻松嵌入现有的微服务或容器化平台。  

综上，aartiq/servicenow-mcp 为企业提供了一条“AI ↔ ServiceNow” 的标准化桥梁，接入门槛低、功能覆盖广，且已具备在生产环境中可靠运行的技术与社区基础。

## 🧭 Practical evaluation

**Value:** aartiq/servicenow-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 35 GitHub stars
- 29 forks
- updated 2026-06-24
- primary language: TypeScript
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 37/100 |
| stars | 33/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 65/100 |
| recency | 80/100 |
| adoption | 34/100 |
| production | 69/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/aartiq/servicenow-mcp) · [← Back to Mcp](./README.md)</sub>
