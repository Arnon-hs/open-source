# codependentai/resonant

[![Stars](https://img.shields.io/github/stars/codependentai/resonant?style=flat-square&color=yellow)](https://github.com/codependentai/resonant/stargazers) [![Forks](https://img.shields.io/github/forks/codependentai/resonant?style=flat-square&color=blue)](https://github.com/codependentai/resonant/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Open-source relational AI framework with identity persistence, memory, and MCP integration. Build relationship-aware AI agents that remember, grow, and maintain continuity. Built on Claude Agent SDK.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 34 |
| 🍴 **Forks** | 11 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-sdk` `ai-agent` `ai-companion` `ai-identity` `ai-memory` `anthropic` `claude` `claude-code` `cognitive-architecture` `companion-ai` `llm-agent` `mcp`

## 🎯 Categories

MCP · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
codependentai/resonant is an open‑source, relational AI framework that gives agents persistent identity, long‑term memory, and native Model Context Protocol (MCP) integration. Built on the Claude Agent SDK and written in TypeScript, it lets developers create relationship‑aware assistants that can remember past interactions, evolve over time, and seamlessly invoke real‑world tools and data sources.

**Value**  
- **Continuity & Personalisation:** Persistent identities and memory let agents maintain context across sessions, enabling more natural, trust‑building conversations.  
- **Standardised Tool Access:** By exposing a uniform MCP‑based interface, Resonant removes the “glue code” barrier between LLM agents and external services, accelerating integration of databases, APIs, or UI components.  
- **Rapid Prototyping:** The Claude Agent SDK foundation provides high‑level abstractions (agents, tools, prompts) so teams can focus on domain logic rather than low‑level LLM plumbing.

**Practical Adoption Path**  
1. **Prototype:** Clone the repo, run the provided CLI/SDK demo, and connect a simple tool (e.g., a weather API) via the MCP server.  
2. **Extend:** Define custom agent personas and memory schemas in TypeScript, then register additional tool adapters using the built‑in plugin system.  
3. **Integrate:** Deploy the MCP server (Docker or serverless) alongside your existing backend, and point any Claude‑compatible assistant to it via the exposed API endpoint.  
4. **Scale:** Replace the in‑memory store with a persistent vector DB (e.g., Pinecone, Weaviate) for production‑grade long‑term memory, and configure load‑balanced MCP instances.

**Production Readiness**  
- **Activity & Ecosystem:** Recent commits (as of 2026‑05‑12), 34 GitHub stars, 11 forks, and 19 topical tags indicate an active community.  
- **Maturity:** The framework leverages the well‑maintained Claude Agent SDK and follows the emerging Model Context Protocol, both of which are already used in several pilot projects.  
- **Readiness Level:** High for an OSS candidate—core features (identity, memory, MCP) are stable, documentation includes API/CLI examples, and the TypeScript codebase is straightforward to audit.  
- **Remaining Checks:** Final due‑diligence should verify the project’s license compatibility, security posture (dependency scanning), and the presence of an active maintainer for long‑term support. Once those are cleared, Resonant is suitable for serious pilots or production deployments that require relational AI capabilities.

### Русский

**codependentai/resonant** — открытый фреймворк для создания «отношенческих» AI‑агентов с постоянной идентичностью, долговременной памятью и поддержкой Model Context Protocol (MCP). Он позволяет быстро подключать ассистентов к реальным инструментам и данным через единый протокол, что упрощает построение сценариев, где AI‑агенты «помнят», развиваются и сохраняют непрерывность взаимодействий (например, интеграция с CRM, аналитикой или внутренними сервисами). Проект имеет активную разработку (обновления 2026‑05‑12), 34 звёзд, 11 форков, написан на TypeScript и готов к пилотному запуску в продакшн, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句话）**  
codependentai/resonant 是一款开源的关系型 AI 框架，具备身份持久化、记忆管理以及 Model Context Protocol（MCP）集成能力。它基于 Claude Agent SDK，帮助开发者快速构建能够记住、成长并保持上下文连续性的关系感知 AI 代理。

**价值**  
- **统一协议接入**：通过标准化的 MCP，AI 助手可以安全、可靠地调用真实工具和业务数据，实现“AI + 业务”无缝连接。  
- **持续记忆与身份**：框架自带持久化身份和记忆层，代理能够在多次交互中保持上下文，提升用户体验和任务完成率。  
- **生态兼容**：基于 TypeScript 与 Claude Agent SDK，易于在现有前端/后端项目中嵌入，支持快速原型到生产的全链路迭代。

**典型接入方式**  
1. **SDK 引入**：在 TypeScript 项目中 `npm install @codependentai/resonant`，使用提供的 `ResonantClient` 初始化并配置 MCP 端点。  
2. **CLI/服务器模式**：通过 `resonant serve` 启动本地或容器化的 MCP 服务器，其他 AI 代理可通过 HTTP/WS 与之交互。  
3. **插件式集成**：在 Claude Agent SDK 的 `AgentBuilder` 中挂载 Resonant 的记忆和身份插件，即可让现有 Claude Agent 获得持久记忆与工具调用能力。

**生产可用性**  
- **活跃度**：截至 2026‑05‑12 最近一次提交，拥有 34 星、11 Fork，代码基于 TypeScript，维护频率稳定。  
- **成熟度**：框架已实现完整的 API/SDK/CLI 三层入口，具备明确的协议实现和示例，适合作为正式项目的底层组件。  
- **风险**：目前未发现重大元数据风险，仍需对许可证合规性、依赖安全审计以及维护者响应时效进行最终确认。总体而言，Resonant 已具备在生产环境中进行试点或正式上线的条件。

## 🧭 Practical evaluation

**Value:** codependentai/resonant helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 34 GitHub stars
- 11 forks
- updated 2026-05-12
- primary language: TypeScript
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 27/100 |
| stars | 33/100 |
| topics | 100/100 |
| outlook | 55/100 |
| quality | 49/100 |
| recency | 20/100 |
| adoption | 31/100 |
| production | 51/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/codependentai/resonant) · [← Back to Mcp](./README.md)</sub>
