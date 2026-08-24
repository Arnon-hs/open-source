# Sushegaad/MCP-Server-for-ISO27001

[![Stars](https://img.shields.io/github/stars/Sushegaad/MCP-Server-for-ISO27001?style=flat-square&color=yellow)](https://github.com/Sushegaad/MCP-Server-for-ISO27001/stargazers) [![Forks](https://img.shields.io/github/forks/Sushegaad/MCP-Server-for-ISO27001?style=flat-square&color=blue)](https://github.com/Sushegaad/MCP-Server-for-ISO27001/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> Model Context Protocol (MCP) server for ISO27001: A stateful Model Context Protocol (MCP) server that gives Claude a complete ISO 27001:2022 Information Security Management System (ISMS). Ask Claude to run gap assessments, manage risks, generate policies, track evidence, and run audits — all backed by an encrypted SQLite database on your machine.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 23 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`iso27001` `iso27001-compliance` `mcp` `mcp-server` `open-source`

## 🎯 Categories

MCP · Backend · Database · Security

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
The MCP‑Server‑for‑ISO27001 is a stateful Model Context Protocol (MCP) server written in TypeScript that equips Claude (or any MCP‑compatible LLM) with a full‑featured ISO 27001:2022 ISMS on your own machine. It stores all evidence, policies, risk registers and audit results in an encrypted SQLite database, letting you ask the AI to run gap assessments, manage risks, generate documentation, and conduct audits through a standard MCP API/CLI.

**Value**  
- **AI‑driven security governance** – By exposing the ISMS data via MCP, security teams can leverage Claude’s natural‑language capabilities to automate routine ISO 27001 tasks (risk analysis, policy drafting, evidence collection) without building custom scripts.  
- **Standardized integration** – MCP provides a vendor‑agnostic contract, so the same server can be swapped for other AI assistants or integrated into existing CI/CD, ticketing, or GRC platforms with minimal code changes.  
- **Local, encrypted data store** – All sensitive information stays on‑premises in an encrypted SQLite DB, satisfying data‑sovereignty and compliance requirements while still being easily queryable by the AI.

**Practical adoption path**  
1. **Prototype** – Clone the repo, run `npm install && npm start` to launch the server locally; use the provided CLI or HTTP endpoint to feed your existing ISO 27001 artifacts (risk register, policies, evidence).  
2. **Connect Claude** – Configure Claude (or another MCP‑compatible model) with the server’s endpoint and authentication token; start issuing natural‑language commands (e.g., “run a gap assessment for Control A.12.4”).  
3. **Iterate & extend** – Add custom MCP signals or SDK wrappers to map internal tools (ticketing systems, CI pipelines) to the server’s actions, and optionally replace SQLite with a more robust DB for larger deployments.  
4. **Pilot in a controlled environment** – Deploy the server behind your corporate firewall, enable role‑based access, and run a limited‑scope audit to validate accuracy and audit‑trail completeness.  

**Production readiness**  
- **Maturity**: Medium. The project is functional and actively updated (as of 2026‑06‑29) with 23 stars and 5 forks, but it lacks extensive production‑grade testing, automated security scans, and formal SLAs.  
- **Dependencies**: Relies on Node/TypeScript and an encrypted SQLite backend; suitable for internal prototypes or small‑to‑medium teams, but larger enterprises may want to replace SQLite with PostgreSQL or another hardened DB and add container‑orchestration health checks.  
- **Risk considerations**: No glaring licensing or metadata issues, yet a thorough review of the MIT‑style license, dependency vulnerabilities, and long‑term maintainer commitment is recommended before a critical production rollout.  

In short, the MCP‑Server‑for‑ISO27001 offers a quick way to blend AI assistance with ISO 27001 governance, is straightforward to spin up for pilots, and can be hardened for production with modest engineering effort and a security review.

### Русский

**Sushegaad/MCP-Server-for-ISO27001** — это сервер Model Context Protocol, реализованный на TypeScript и хранящий данные в зашифрованной SQLite‑базе, который позволяет подключать AI‑ассистентов (например, Claude) к полноценной системе управления информационной безопасностью по ISO 27001:2022: проводить оценку разрывов, управлять рисками, генерировать политики, фиксировать доказательства и выполнять аудиты. Типичный сценарий — запуск прототипа или внутреннего workflow, где AI‑агент взаимодействует с реальными инструментами и данными через единый MCP‑интерфейс; сервер легко разворачивается локально и предоставляет API/SDK/CLI для интеграции. Готовность к production — средняя: проект подходит для прототипов и ограниченных внутренних применений, но перед выпуском в продакшн требуется проверка зависимостей, лицензии и усиление мер поддержки.

### 中文

**项目简介**  
Sushegaad/MCP-Server-for-ISO27001 是一个基于 Model Context Protocol（MCP）的状态化服务，能够在本地通过加密的 SQLite 数据库为 Claude（或其他兼容的 AI 助手）提供完整的 ISO 27001:2022 信息安全管理体系（ISMS）。用户可以让 Claude 执行差距评估、风险管理、政策生成、证据追踪和审计等任务，实现 AI 与真实安全工具和数据的无缝对接。

**价值**  
- **标准化 AI‑工具交互**：通过 MCP 将 AI 助手与 ISO 27001 相关的业务流程、文档和风险库统一包装，降低集成成本。  
- **本地安全**：所有数据均存储在本机加密的 SQLite 中，避免敏感信息外泄。  
- **提升效率**：AI 可自动生成政策、评估风险、准备审计材料，显著缩短信息安全管理的周期。

**典型接入方式**  
1. **API/SDK 调用**：在后端服务中引入项目提供的 TypeScript SDK，使用 `POST /mcp` 等端点与 Claude 进行上下文对话。  
2. **CLI 交互**：通过项目自带的命令行工具直接在终端发起 Gap Assessment、风险登记等操作，适合脚本化工作流。  
3. **自定义插件**：将 MCP 服务器作为微服务部署，配合 OpenAI/Anthropic 的函数调用（function calling）或 LangChain 等框架，实现“AI → MCP → 本地数据库”的闭环。

**生产可用性**  
- **成熟度**：项目已在 GitHub 获得 23 ⭐、5 🍴，最近一次提交于 2026‑06‑29，代码基于 TypeScript，结构清晰。  
- **适用场景**：适合原型验证、内部安全工作流或中小团队的 ISMS 自动化；在生产环境使用前建议完成以下检查：  
  - 依赖安全审计（尤其是 SQLite 加密实现）。  
  - 许可证兼容性确认（项目采用的开源许可证）。  
  - 维护者活跃度和社区支持评估。  
- **总体评估**：**中等**（Medium）——功能可用且易于集成，但在大规模生产部署前仍需进行安全、性能和运维方面的额外验证。

## 🧭 Practical evaluation

**Value:** Sushegaad/MCP-Server-for-ISO27001 helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 23 GitHub stars
- 5 forks
- updated 2026-06-29
- primary language: TypeScript
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 29/100 |
| topics | 63/100 |
| outlook | 48/100 |
| quality | 46/100 |
| recency | 40/100 |
| adoption | 27/100 |
| production | 52/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/Sushegaad/MCP-Server-for-ISO27001) · [← Back to Mcp](./README.md)</sub>
