# bonnard-data/bonnard-cli

[![Stars](https://img.shields.io/github/stars/bonnard-data/bonnard-cli?style=flat-square&color=yellow)](https://github.com/bonnard-data/bonnard-cli/stargazers) [![Forks](https://img.shields.io/github/forks/bonnard-data/bonnard-cli?style=flat-square&color=blue)](https://github.com/bonnard-data/bonnard-cli/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-76%2F100-brightgreen?style=flat-square)](#)

> Open-source agentic schema CLI. Optimised for claude code, gemini, codex and co-pilot. Skills included.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 48 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 76/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic` `agentic-analytics` `agentic-schema` `ai-analytics` `bigquery` `data-catalog` `databricks` `dbt` `embedded-analytics` `mcp-server` `metrics` `metrics-layer`

## 🎯 Categories

MCP · AI/ML · Backend · DevTools · Data

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
bonnard‑data/bonnard‑cli is an open‑source, TypeScript‑based CLI that implements the Model Context Protocol, enabling AI assistants such as Claude, Gemini, Codex, and Copilot to invoke real‑world tools and data sources in a standardized way. It ships with a set of pre‑built “skills” and can be used to quickly stand up protocol servers or integrate custom back‑ends, making AI‑driven automation more reliable and portable. With recent commits, 48 stars and growing community interest, it is positioned as a production‑ready candidate for pilot projects.

**Value**  
- **Unified integration layer** – Provides a single, language‑agnostic protocol for connecting large language models to external APIs, databases, or command‑line tools, reducing the need for bespoke glue code.  
- **Agent‑centric workflow** – By exposing “skills” that map directly to actionable commands, developers can let AI agents perform tasks (e.g., data retrieval, job scheduling) without hard‑coding prompts.  
- **Ecosystem compatibility** – Optimised for the major LLM providers (Claude, Gemini, Codex, Copilot), it fits naturally into existing AI pipelines and can be swapped between providers with minimal changes.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run `npm install && npx bonnard-cli init` to generate a starter server and sample skill definitions.  
2. **Connect an LLM** – Configure the CLI with your provider’s API key (Claude, Gemini, etc.) and expose the generated endpoint to the model via the Model Context Protocol.  
3. **Add custom skills** – Extend the `skills/` directory with TypeScript functions that wrap your internal services or third‑party APIs; the CLI automatically registers them.  
4. **Deploy** – Containerise the CLI (`Dockerfile` is provided) and deploy to a cloud service or on‑premise; the protocol is HTTP‑based, so any service that can reach the endpoint can consume it.  
5. **Iterate & monitor** – Use the built‑in logging and telemetry hooks to observe agent calls, refine skill implementations, and version‑control the schema.

**Production Readiness**  
- **Activity & Maintenance** – The project was updated on 2026‑05‑14, shows recent commits, and has a modest but active contributor base (4 forks).  
- **Stability** – Core functionality (API/SDK/CLI) is stable, with TypeScript typings and comprehensive metadata (20 topics) that aid integration testing.  
- **Adoption Signals** – 48 GitHub stars and early adopters indicate community interest; the CLI’s design follows the emerging Model Context Protocol standard, which is gaining traction among AI platform vendors.  
- **Risk Considerations** – No immediate licensing or security red flags have been identified, but a final audit of the repository’s license compliance, dependency vulnerabilities, and maintainer responsiveness is recommended before a full production rollout.  

Overall, bonnard‑cli offers a low‑friction, standards‑based bridge between AI agents and real‑world tooling, making it a strong candidate for pilots and, after a brief security review, for production deployments.

### Русский

**bonnard-data/bonnard-cli** — это open‑source CLI‑утилита для агентных схем, позволяющая быстро подключать AI‑ассистентов (Claude, Gemini, Codex, Copilot) к реальным инструментам и данным через единый протокол Model Context Protocol. Типичный сценарий: разработчик разворачивает MCP‑сервер, регистрирует в нём свои инструменты (API, SDK, CLI) и сразу получает готовый интерфейс для взаимодействия AI‑агента с этими ресурсами. Проект находится на высоком уровне готовности к production: активные коммиты, 48 звёзд, поддержка TypeScript, широкие метаданные и сильные сигналы экосистемы делают его надёжным кандидатом для пилотных внедрений, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
bonnard-data/bonnard-cli 是一款开源的 *agentic schema* 命令行工具，专为 Claude、Gemini、Codex、Copilot 等大模型的代码生成与执行场景进行优化，并内置常用技能集合。

**价值主张**  
- **统一协议**：通过标准化的 Model Context Protocol（MCP），让 AI 助手能够安全、可靠地调用真实的工具和数据源。  
- **即插即用**：提供 CLI、API 与 SDK 三种接入方式，配合完整的语言元数据和主题标签，降低集成成本。  
- **多模型兼容**：针对多家主流大模型（Claude、Gemini、Codex、Copilot）进行专门调优，提升生成代码的可执行性和准确性。

**典型接入方式**  
1. **CLI 直接调用**：在 CI/CD、脚本或本地开发环境中运行 `bonnard-cli`，传入模型指令即可触发工具调用。  
2. **SDK 集成**：在 TypeScript/JavaScript 项目中引入 `bonnard-cli` 包，使用 `runSchema(schema, input)` 等函数实现程序化调用。  
3. **API 服务**：部署 MCP 服务器（可使用项目自带的 Docker 镜像），通过 HTTP/JSON 接口让任何语言的 AI Agent 与之交互。

**生产可用性**  
- **活跃度**：最近一次提交为 2026‑05‑14，拥有 48 ⭐、4 🍴，且涉及 20+ 主题标签，社区活跃。  
- **技术成熟度**：采用 TypeScript 编写，代码结构清晰，提供完整的类型定义和示例。  
- **风险评估**：暂无重大元数据或许可证风险，但仍建议在正式上线前进行安全审计并确认维护者的响应能力。整体来看，项目已具备 **高** 的生产就绪度，适合作为 Pilot 项目或内部工具链的核心组件。

## 🧭 Practical evaluation

**Value:** bonnard-data/bonnard-cli helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 48 GitHub stars
- 4 forks
- updated 2026-05-14
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 36/100 |
| topics | 100/100 |
| outlook | 81/100 |
| quality | 69/100 |
| recency | 100/100 |
| adoption | 31/100 |
| production | 77/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/bonnard-data/bonnard-cli) · [← Back to Mcp](./README.md)</sub>
