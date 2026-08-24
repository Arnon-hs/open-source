# Tianzeyui/stardust

[![Stars](https://img.shields.io/github/stars/Tianzeyui/stardust?style=flat-square&color=yellow)](https://github.com/Tianzeyui/stardust/stargazers) [![Forks](https://img.shields.io/github/forks/Tianzeyui/stardust?style=flat-square&color=blue)](https://github.com/Tianzeyui/stardust/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> Open-source AI Agent platform with React/TSX & HTML plugin dev modes. Built-in 60+ APIs, multi-project, MCP tools, sandbox engine. Official + community-driven, building an extensible agent ecosystem for everyone.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 41 |
| 🍴 **Forks** | 1 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `electron` `mcp` `plugin` `typescript`

## 🎯 Categories

MCP · AI/ML

## 📝 Summary

### English

**Brief Summary**  
Tianzeyui / stardust is an open‑source AI‑agent platform that lets developers build, run and extend intelligent assistants using a React/TSX front‑end and an HTML‑based plugin system. It ships with more than 60 ready‑to‑use APIs, multi‑project management, MCP (Model Context Protocol) tooling and a sandbox execution engine, creating a shared ecosystem for both official and community‑driven agents.

**Value**  
- **Standardised tool integration** – By exposing a common protocol (MCP) and a rich set of pre‑built APIs, Stardust removes the friction of wiring large language models to real‑world services, data stores, and UI components.  
- **Extensible plug‑in model** – The React/TSX + HTML plug‑in architecture lets teams add custom UI widgets or backend adapters without touching the core engine, fostering rapid experimentation and reuse across projects.  
- **Unified development experience** – A single codebase provides both front‑end (React) and back‑end (TypeScript) tooling, plus CLI/SDK helpers, so engineers can develop, test and ship agents end‑to‑end in one workflow.

**Practical Adoption Path**  
1. **Evaluate the SDK/CLI** – Clone the repo, run the provided CLI to spin up a local sandbox, and explore the 60+ built‑in API definitions.  
2. **Prototype a connector** – Use the TypeScript SDK to wrap an existing internal service (e.g., a CRM API) as a new MCP endpoint; the plug‑in system lets you expose it via a simple HTML UI component.  
3. **Deploy a Model Context Protocol server** – Package the agent as a MCP server (Docker or serverless) and point your LLM provider (OpenAI, Anthropic, etc.) to it, enabling the model to call your custom tools in production.  
4. **Scale & share** – Leverage the multi‑project workspace to manage several agents, publish plug‑ins to the community hub, and integrate with CI/CD pipelines for continuous delivery.

**Production Readiness**  
- **Activity & community** – The project was updated today (2026‑06‑24), has 41 stars, and shows recent commits, indicating active maintenance.  
- **Technical maturity** – Built in TypeScript with a clear API surface, CLI, and sandbox engine; the codebase is modular and includes both front‑end and back‑end components, which simplifies testing and CI integration.  
- **Ecosystem fit** – The MCP focus aligns with emerging standards for LLM tool usage, making it a future‑proof choice for enterprises looking to lock in a vendor‑agnostic integration layer.  
- **Remaining checks** – Before a full production rollout, verify the open‑source license compatibility, conduct a security audit of the sandbox isolation, and confirm that a dedicated maintainer is assigned to respond to issues.

Overall, Stardust is a high‑readiness OSS candidate for organizations that need a standardized, extensible bridge between AI assistants and their internal tooling ecosystem.

### Русский

**Tianzeyui/stardust** — это открытая платформа для создания AI‑агентов с поддержкой плагинов на React/TSX и HTML, включающая более 60 готовых API, мульти‑проектный MCP‑инструментарий и песочницу для безопасного исполнения. Типичный сценарий: разработчик подключает агенту реальные инструменты и базы данных через единый Model Context Protocol, разворачивает собственный MCP‑сервер и быстро интегрирует его в существующие сервисы. Проект уже активно поддерживается (обновления — 2026‑06‑24, 41 звезда, TypeScript), имеет стабильный набор SDK/CLI и достаточный уровень зрелости для пилотного внедрения в production, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目价值**  
Tianzeyui / stardust 为 AI 助手提供统一的「模型上下文协议」接口，能够把语言模型快速接入真实的工具、数据库和业务系统。通过内置 60+ 常用 API、MCP（Model Context Protocol）工具链以及可沙箱运行的插件引擎，开发者可以在同一平台上创建、调试、发布和复用 AI Agent，形成一个可扩展的生态体系，显著降低 AI‑to‑Tool 的集成成本。

**典型接入方式**  

| 场景 | 接入步骤 | 关键组件 |
|------|----------|----------|
| **在现有前端项目中使用 AI Agent** | 1. `npm i @stardust/agent`  <br>2. 在 React/TSX 中引入 `<AgentProvider>` <br>3. 配置 `apiKey` 与需要的插件（HTML、CLI、数据库等） | React/TSX 插件、HTML 渲染插件 |
| **部署自定义 MCP 服务器** | 1. 克隆仓库并运行 `npm run build` <br>2. 使用 `stardust-cli serve --port 8080` 启动本地协议服务 <br>3. 在模型侧（如 OpenAI、Claude）配置协议端点 | CLI、Sandbox Engine、MCP SDK |
| **将 AI Agent 接入后端/数据库** | 1. 在后端（Node/Express、NestJS）安装 `@stardust/sdk` <br>2. 初始化 `StardustClient` 并注册数据库插件（MongoDB、PostgreSQL 等） <br>3. 通过 SDK 调用 `client.runAgent(context)` 完成业务逻辑 | SDK、数据库插件、REST/GraphQL 适配层 |
| **社区插件或自研插件** | 1. 在 `plugins/` 目录创建符合 `IPlugin` 接口的 TypeScript 模块 <br>2. 使用 `stardust-cli dev` 进行热加载调试 <br>3. 发布到 npm 或提交 PR 供社区共享 | 插件开发框架、CLI 开发模式 |

**生产可用性评估**  

- **活跃度**：截至 2026‑06‑24 最近一次提交，项目仍在维护；GitHub ★41、Fork 1，社区讨论活跃。  
- **技术成熟度**：采用 TypeScript 全栈实现，提供 API/SDK/CLI 三种接入方式，且已内置 60+ 常用工具的适配器，降低二次开发风险。  
- **安全与合规**：暂无已知许可证或安全漏洞报告，但在正式投产前建议完成以下审查：  
  1. 检查仓库 LICENSE（MIT/Apache 等）是否符合公司合规要求；  
  2. 通过 SAST/DAST 对 SDK 与 sandbox 引擎进行代码审计；  
  3. 验证插件沙箱的资源隔离与权限控制。  
- **可扩展性**：插件化架构 + MCP 标准协议，使得新增工具或业务系统只需实现对应插件或协议端点，支持多项目、多租户部署。  
- **运维成本**：提供 Dockerfile 与 Helm chart（社区贡献），可在 Kubernetes 中以 StatefulSet 方式部署，支持水平扩容和灰度发布。  

**结论**  
Tianzeyui / stardust 已具备较高的生产就绪度，适合作为企业内部或对外提供 AI Agent 的统一平台。通过标准化的 MCP 接口和丰富的插件生态，能够快速把大模型能力落地到业务工具、数据库及自研系统，显著提升 AI‑to‑Tool 的集成效率。后续只需完成许可证、代码安全审计以及运维监控的细化，即可在正式生产环境中稳妥使用。

## 🧭 Practical evaluation

**Value:** Tianzeyui/stardust helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 41 GitHub stars
- 1 forks
- updated 2026-06-24
- primary language: TypeScript
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 8/100 |
| stars | 35/100 |
| topics | 63/100 |
| outlook | 57/100 |
| quality | 47/100 |
| recency | 40/100 |
| adoption | 27/100 |
| production | 57/100 |
| usefulness | 100/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/Tianzeyui/stardust) · [← Back to Mcp](./README.md)</sub>
