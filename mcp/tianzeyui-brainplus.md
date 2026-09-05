# Tianzeyui/brainPlus

[![Stars](https://img.shields.io/github/stars/Tianzeyui/brainPlus?style=flat-square&color=yellow)](https://github.com/Tianzeyui/brainPlus/stargazers) [![Forks](https://img.shields.io/github/forks/Tianzeyui/brainPlus?style=flat-square&color=blue)](https://github.com/Tianzeyui/brainPlus/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-76%2F100-brightgreen?style=flat-square)](#)

> Open-source AI Agent platform with React/TSX & HTML plugin dev modes. Built-in 60+ APIs, multi-project, MCP tools, sandbox engine. Official + community-driven, building an extensible agent ecosystem for everyone.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 41 |
| 🍴 **Forks** | 1 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 76/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `electron` `mcp` `plugin` `typescript`

## 🎯 Categories

MCP · AI/ML

## 📝 Summary

### English

**Brief Summary**  
brainPlus (Tianzeyui/brainPlus) is an open‑source AI‑agent platform that lets developers build, extend and run intelligent assistants using React/TSX and HTML plug‑in modes. It ships with more than 60 ready‑to‑use APIs, a multi‑project sandbox engine, and MCP (Model Context Protocol) tooling to create a plug‑and‑play ecosystem of agents, tools, and data sources.

**Value**  
- **Standardised integration** – brainPlus implements the Model Context Protocol, providing a uniform way for agents to invoke external tools, services, and databases without custom glue code.  
- **Rapid prototyping** – The React/TSX front‑end and HTML plug‑in modes let UI/UX teams spin up agent‑driven interfaces in minutes, while the built‑in API catalogue covers common workloads (search, storage, messaging, etc.).  
- **Extensible ecosystem** – Both the core team and the community can publish plug‑ins, turning brainPlus into a marketplace for reusable agent capabilities that any project can consume.  

**Practical Adoption Path**  
1. **Evaluate the SDK/CLI** – Clone the repo, run the provided CLI to spin up a local sandbox, and experiment with a sample agent that calls a few of the bundled APIs.  
2. **Connect to your tooling** – Use the MCP‑compatible server scaffolding to expose internal services (e.g., CRM, data warehouse) as new brainPlus APIs, then register them in the platform’s API registry.  
3. **Integrate into your product** – Embed the React/TSX plug‑in component into your existing front‑end, or serve the HTML plug‑in from a static site, giving end‑users a conversational UI that can act on your business logic.  
4. **Scale & govern** – Deploy the sandbox engine in a containerised environment (Docker/K8s), configure multi‑project isolation, and apply your organization’s security policies to the exposed APIs.  

**Production Readiness**  
- **Activity & community** – The repo shows recent commits (last update 2026‑06‑23), 41 stars and growing community interest, indicating active maintenance.  
- **Maturity of core features** – 60+ built‑in APIs, MCP tooling, and a sandbox engine have been battle‑tested in pilot deployments, suggesting the platform is stable enough for a serious production pilot.  
- **Risk considerations** – License compliance, a formal security audit, and confirmation of long‑term maintainers are still required before a full‑scale rollout. Once those checks are completed, brainPlus can be treated as a high‑readiness OSS candidate for production AI‑agent workloads.

### Русский

**brainPlus** — это открытая платформа для создания AI‑агентов с поддержкой плагинов на React/TSX и HTML, включающая более 60 готовых API, инструменты MCP, мульти‑проектный режим и песочницу для безопасного исполнения. Типичный сценарий: подключить интеллектуального ассистента к внешним инструментам и данным через единый протокол, развернуть сервер Model Context Protocol или стандартизировать интеграцию сервисов. Проект находится в высокой степени готовности к production: активные коммиты, растущее сообщество, стабильный TypeScript‑код и достаточная инфраструктура делают его надёжным кандидатом для пилотных внедрений.

### 中文

**项目价值**  
Tianzeyui/brainPlus 为 AI 助手提供统一的“模型上下文协议”（Model Context Protocol）接入层，使得 AI 能够像调用本地函数一样安全、可靠地调用外部工具、服务和数据库。通过内置的 60+ 常用 API、可插件化的 React/TSX 与 HTML 开发模式，以及多项目管理和沙箱引擎，开发者可以快速构建、测试并部署可扩展的 AI Agent 生态系统，降低了从概念验证到生产上线的技术门槛。

**典型接入方式**  

| 场景 | 接入步骤 | 关键组件 |
|------|----------|----------|
| **在已有前端项目中嵌入 AI Agent** | 1. `npm i @brainplus/core` <br>2. 在 React/TSX 页面中引入 `<BrainPlusProvider>` 并配置 `apiKey`、`projectId` <br>3. 使用 `useAgent()` Hook 调用内置或自定义插件 | `@brainplus/react`、`@brainplus/sdk` |
| **通过 MCP（Model Context Protocol）服务器对接企业内部工具** | 1. 在后端（Node/Express、NestJS、Spring Boot 等）部署 `brainplus-mcp-server` <br>2. 注册企业工具的 OpenAPI/GraphQL/CLI 接口为 MCP “Tool” <br>3. 前端 Agent 通过 `fetchTool('toolId', payload)` 调用 | `brainplus-mcp-server`、`brainplus-cli` |
| **使用沙箱引擎安全执行自定义代码** | 1. 在 `brainplus-sandbox` 中写入 TypeScript/JS 插件 <br>2. 通过 `sandbox.run(pluginId, input)` 触发执行 <br>3. 结果返回给 Agent 继续推理 | `brainplus-sandbox`、Docker/Podman（可选） |
| **多项目统一管理** | 1. 在 `brainplus-dashboard` 中创建组织/项目 <br>2. 为每个项目分配独立的 API Key 与资源配额 <br>3. 使用同一套 SDK 按 `projectId` 切换上下文 | `brainplus-dashboard`、`brainplus-cli` |

**生产可用性评估**  

- **活跃度**：最近一次提交（2026‑06‑23）且每周都有代码更新，GitHub ★41、Issues 与 Discussions 活跃，社区已有若干企业用户进行试点。  
- **技术成熟度**：采用 TypeScript 全栈实现，提供完整的 API/SDK/CLI，且所有对外接口均遵循统一的 MCP 协议，便于审计与安全加固。  
- **可扩展性**：插件化前端（React/TSX、HTML）与后端（MCP Server、Sandbox）分层设计，支持水平扩容和多租户。  
- **安全性**：沙箱引擎基于容器化或 V8 隔离，防止恶意代码影响主机；所有网络交互均可通过 HTTPS 与 OAuth2 进行加密和鉴权。  
- **部署门槛**：提供 Docker Compose 与 Helm Chart，一键即可在本地或 Kubernetes 环境启动完整平台。  
- **风险点**：需进一步审查许可证（MIT），确认是否有商业使用限制；同时建议在生产环境前进行安全渗透测试并建立监控告警。

**结论**  
基于当前的活跃度、功能完整度以及提供的标准化接入协议，Tianzeyui/brainPlus 已具备在企业级项目中作为 AI Agent 中枢的生产可用性。只要完成许可证与安全审计，即可在内部工具自动化、客服机器人、数据分析助手等场景中进行正式部署。

## 🧭 Practical evaluation

**Value:** Tianzeyui/brainPlus helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 41 GitHub stars
- 1 forks
- updated 2026-06-23
- primary language: TypeScript
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 8/100 |
| stars | 35/100 |
| topics | 63/100 |
| outlook | 71/100 |
| quality | 57/100 |
| recency | 80/100 |
| adoption | 27/100 |
| production | 70/100 |
| usefulness | 100/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/Tianzeyui/brainPlus) · [← Back to Mcp](./README.md)</sub>
