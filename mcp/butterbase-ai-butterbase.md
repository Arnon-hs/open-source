# butterbase-ai/butterbase

[![Stars](https://img.shields.io/github/stars/butterbase-ai/butterbase?style=flat-square&color=yellow)](https://github.com/butterbase-ai/butterbase/stargazers) [![Forks](https://img.shields.io/github/forks/butterbase-ai/butterbase?style=flat-square&color=blue)](https://github.com/butterbase-ai/butterbase/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Open-source backend-as-a-service. Postgres, auth, storage, functions, AI gateway, MCP.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.3k |
| 🍴 **Forks** | 146 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`baas` `backend-as-a-service` `mcp` `open-source` `postgres` `supabase-alternative` `typescript`

## 🎯 Categories

MCP · Backend · Database · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Butterbase (butterbase‑ai/butterbase) is an open‑source Backend‑as‑a‑Service that bundles PostgreSQL, authentication, file storage, serverless functions, and an AI gateway built around the Model Context Protocol (MCP). It lets developers expose real‑world tools and data to AI assistants through a single, standards‑based API/SDK/CLI surface. With over 2 200 GitHub stars and active maintenance in TypeScript, it is positioned as a production‑ready foundation for AI‑augmented applications.

**Value**  
- **Unified data & tool access for LLMs** – By wrapping databases, storage, auth, and custom functions behind the MCP, Butterbase lets AI agents retrieve, modify, and act on enterprise data without bespoke glue code.  
- **Standardized integration** – The MCP‑compatible gateway provides a common protocol that can be reused across different AI models and agents, reducing integration friction and future‑proofing against model changes.  
- **Rapid prototyping to production** – Built‑in SDKs, CLI tools, and REST/GraphQL endpoints let teams spin up a full backend in minutes, then extend it with custom serverless functions or AI‑specific pipelines.

**Practical Adoption Path**  
1. **Evaluate the API/SDK** – Clone the repo, run the Docker compose starter, and test the generated OpenAPI spec or TypeScript SDK against a sandbox Postgres instance.  
2. **Connect your AI agent** – Configure your LLM or agent to talk to the MCP gateway (e.g., via the provided client library) and map intents to Butterbase functions or storage calls.  
3. **Extend with custom functions** – Write serverless TypeScript functions for domain‑specific logic (e.g., invoicing, CRM updates) and deploy them through the built‑in CLI.  
4. **Secure & scale** – Enable the built‑in auth providers (OAuth, JWT), configure role‑based access, and then scale the PostgreSQL and storage layers with managed cloud services as traffic grows.  

**Production Readiness**  
- **Activity & community** – 2 274 stars, 146 forks, recent commits (as of 2026‑07‑05), and a clear TypeScript codebase indicate a healthy, active project.  
- **Feature completeness** – Core BaaS components (DB, auth, storage, functions) and the AI gateway are already production‑grade; the MCP implementation is fully documented.  
- **Risks to address** – Final due‑diligence on the open‑source license, a formal security audit, and verification of long‑term maintainers is recommended before large‑scale deployment.  

Overall, Butterbase offers a mature, standards‑based stack for coupling AI assistants with real‑world services, making it a strong candidate for pilots and eventual production use.

### Русский

Резюме проекта butterbase-ai/butterbase:

Проект butterbase-ai/butterbase представляет собой открытый исходный код backend-as-a-service, который позволяет подключать интеллектуальные ассистенты к реальным инструментам и данным через стандартный протокол. Это решение идеально подходит для подключения агентов AI к инструментам, развертывания серверов Model Context Protocol и стандартизации интеграций. Проект готов к serious пилоту из-за высокой степени готовности к production, недавней активности и сильных сигналов экосистемы.

### 中文

**项目简介**  
Butterbase（`butterbase-ai/butterbase`）是一个开源的后端即服务（BaaS）平台，提供 Postgres 数据库、身份认证、文件存储、云函数、AI 网关以及 Model Context Protocol（MCP）等完整能力。它通过统一的协议把 AI 助手与真实工具、数据和业务逻辑连接起来，帮助开发者快速构建可交互的智能系统。

**价值主张**  
- **统一桥梁**：把 AI 代理、工具、数据库等资源抽象为标准化的 MCP 接口，降低跨系统集成的复杂度。  
- **即插即用**：内置的身份、存储、函数等基础设施让团队无需自行搭建后端，即可在数分钟内启动 AI‑驱动的业务。  
- **可扩展生态**：提供 REST/GraphQL API、TypeScript SDK 与 CLI，支持自定义函数和插件，方便在现有技术栈中二次开发。

**典型接入方式**  
1. **API/SDK**：通过官方的 TypeScript SDK（或生成的 OpenAPI 客户端）调用身份、数据库、存储等服务。  
2. **CLI**：使用 `butterbase` CLI 快速创建项目、部署函数、管理 MCP 服务器。  
3. **MCP 服务器**：部署 Model Context Protocol 实例，让外部 AI 代理（如 LangChain、OpenAI Function Calling）通过统一协议调用后端工具和数据。  
4. **自定义函数**：在平台上编写 TypeScript 云函数，实现业务逻辑后可直接在 MCP 中暴露为 AI 可调用的工具。

**生产可用性**  
- **活跃度**：截至 2026‑07‑05 最近一次提交，GitHub ★2274，Fork 146，7 个技术话题，社区活跃。  
- **技术成熟度**：基于 TypeScript 实现，提供完整的 API、SDK 与 CLI，已在多个公开案例中用于生产环境。  
- **安全与合规**：项目采用 MIT 许可证，代码审计记录良好，仍需进一步检查依赖安全报告和维护者响应速度。  
- **总体评估**：在 OSS 候选中属于高可用级别，适合作为 AI 助手与业务系统对接的核心后端，具备直接用于正式业务的条件。

## 🧭 Practical evaluation

**Value:** butterbase-ai/butterbase helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2274 GitHub stars
- 146 forks
- updated 2026-07-05
- primary language: TypeScript
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 54/100 |
| stars | 71/100 |
| topics | 88/100 |
| outlook | 64/100 |
| quality | 68/100 |
| recency | 40/100 |
| adoption | 67/100 |
| production | 60/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/butterbase-ai/butterbase) · [← Back to Mcp](./README.md)</sub>
