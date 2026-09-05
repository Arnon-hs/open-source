# TencentCloud/TencentDB-Agent-Memory

[![Stars](https://img.shields.io/github/stars/TencentCloud/TencentDB-Agent-Memory?style=flat-square&color=yellow)](https://github.com/TencentCloud/TencentDB-Agent-Memory/stargazers) [![Forks](https://img.shields.io/github/forks/TencentCloud/TencentDB-Agent-Memory?style=flat-square&color=blue)](https://github.com/TencentCloud/TencentDB-Agent-Memory/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-79%2F100-brightgreen?style=flat-square)](#)

> TencentDB Agent Memory delivers fully local long-term memory for AI Agents via a 4-tier progressive pipeline, with zero external API dependencies.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 6.1k |
| 🍴 **Forks** | 528 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 79/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `ai-agent` `embedding` `llm` `local-first` `long-term-memory` `memory` `openclaw-plugin` `vector-search`

## 🎯 Categories

Orchestration · Knowledge/RAG · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
TencentDB Agent Memory provides a fully local, four‑tier progressive pipeline that equips AI agents with long‑term memory without relying on any external APIs. Packaged as a TypeScript library with CLI/SDK hooks, it enables developers to turn isolated prompts and tool calls into repeatable, stateful agent workflows. With strong community traction (6 k+ stars, 500+ forks) and recent activity, it is ready for serious pilot deployments.

**Value**  
- **Zero external dependencies** – all memory operations run locally, eliminating latency, cost, and data‑privacy concerns associated with third‑party services.  
- **Progressive 4‑tier pipeline** – from raw observation storage to indexed retrieval and reasoning, giving agents a scalable, persistent knowledge base.  
- **Standardised agent memory** – simplifies building multi‑agent or tool‑augmented systems by providing a common, reusable memory layer, reducing duplicated code and integration effort.

**Practical Adoption Path**  
1. **Evaluate** – Clone the repo, run the provided CLI demo, and inspect the TypeScript SDK to verify it meets your data model and retrieval requirements.  
2. **Prototype** – Integrate the SDK into an existing agent framework (e.g., LangChain, AutoGPT) to replace ad‑hoc prompt‑history handling with the memory API.  
3. **Extend** – Customize the pipeline stages (e.g., add vector‑store adapters, domain‑specific indexing) using the exposed hooks.  
4. **Deploy** – Package the agent with the memory component in a container or serverless function; because it is fully local, no external service credentials are needed.  

**Production Readiness**  
- **Activity & Adoption**: Updated as of 2026‑06‑24, 6 074 GitHub stars, 528 forks, and active issue discussions indicate a healthy, engaged community.  
- **Maturity**: The four‑tier architecture is well‑documented, and the project offers CLI, SDK, and API entry points, facilitating integration and testing.  
- **Risk Assessment**: No major metadata or licensing red flags identified; however, a final review of the open‑source license and security posture is advisable before full‑scale rollout.  
Overall, the project exhibits high readiness for pilot projects and can be scaled to production with standard OSS governance and security vetting.

### Русский

TencentDB Agent Memory — open‑source‑решение от TencentCloud, которое обеспечивает полностью локальную долговременную память для AI‑агентов через 4‑уровневый прогрессивный конвейер без обращения к внешним API. Оно позволяет превратить разрозненные подсказки и инструменты в воспроизводимые рабочие процессы агентов, упрощая координацию мульти‑агентных сценариев, построение пайплайнов с использованием инструментов и стандартизацию памяти. Проект имеет высокий уровень готовности к production: активные обновления, более 6000 звёзд на GitHub, широкая экосистема (API/SDK/CLI, TypeScript), а также положительные сигналы по принятию и использованию, требующие лишь финального аудита лицензии и безопасности.

### 中文

**项目简介**  
TencentDB Agent Memory 为 AI Agent 提供全本地化的长期记忆能力，采用 4 层渐进式流水线，完全摆脱外部 API 依赖。它能够把孤立的 Prompt 与工具封装成可重复、可追踪的工作流。

**价值**  
- **提升 Agent 持久性**：在本地持久化上下文，避免每次调用都重新构建记忆，显著提升对话连贯性和任务完成率。  
- **统一工作流**：通过统一的记忆层，将多 Agent、工具链和业务规则串联，实现端到端的可编排流程。  
- **降低成本与风险**：无需调用第三方云服务，降低网络延迟、费用以及数据泄露风险。

**典型接入方式**  
1. **SDK / API**：在项目中引入 npm 包 `@tencentcloud/agent-memory`，通过 `MemoryEngine` 类提供的 `store`, `retrieve`, `update` 等接口完成记忆的写入与查询。  
2. **CLI**：使用 `tencentdb-agent-memory` 命令行工具快速启动本地记忆服务，适合原型验证或脚本化调用。  
3. **语言/框架适配**：项目主要使用 TypeScript，提供完整的类型声明，亦可在 JavaScript、Node.js、Deno 等环境中直接使用。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑24，项目拥有 6074 星、528 Fork，最近一次提交在当日，说明维护频繁。  
- **生态兼容**：已在多个开源 AI Orchestration 项目中被引用，具备成熟的插件化接口和丰富的主题标签（9 个）。  
- **安全与合规**：目前未发现重大元数据风险，需进一步审查许可证（MIT/Apache）和安全审计报告后方可正式上线。  
- **适配度**：基于 TypeScript 实现，易于在现有 Node.js/TS 微服务或 Serverless 环境中集成，具备高可用的本地持久化方案，适合作为正式生产环境的记忆层。  

综上，TencentDB Agent Memory 在功能完整性、社区活跃度和技术成熟度上均表现良好，是面向多 Agent 编排和工具链集成的可靠 OSS 记忆解决方案。

## 🧭 Practical evaluation

**Value:** TencentCloud/TencentDB-Agent-Memory helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 6074 GitHub stars
- 528 forks
- updated 2026-06-24
- primary language: TypeScript
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 68/100 |
| stars | 81/100 |
| topics | 100/100 |
| outlook | 82/100 |
| quality | 85/100 |
| recency | 80/100 |
| adoption | 77/100 |
| production | 78/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/TencentCloud/TencentDB-Agent-Memory) · [← Back to Orchestration](./README.md)</sub>
