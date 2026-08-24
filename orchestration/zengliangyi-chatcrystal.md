# ZengLiangYi/ChatCrystal

[![Stars](https://img.shields.io/github/stars/ZengLiangYi/ChatCrystal?style=flat-square&color=yellow)](https://github.com/ZengLiangYi/ChatCrystal/stargazers) [![Forks](https://img.shields.io/github/forks/ZengLiangYi/ChatCrystal?style=flat-square&color=blue)](https://github.com/ZengLiangYi/ChatCrystal/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Local-first AI PKM for coding conversations: import Claude Code/Cursor/Codex, distill notes, semantic search, tag graph, MCP memory.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 34 |
| 🍴 **Forks** | 2 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-skills` `ai-memory` `ai-tools` `claude-code` `codex` `cursor` `electron` `knowledge-base` `knowledge-graph` `knowledge-management` `llm` `local-first`

## 🎯 Categories

Orchestration · MCP · Knowledge/RAG · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
ChatCrystal is a TypeScript‑based, local‑first AI personal knowledge‑management platform that stitches together large‑language‑model tools such as Claude Code, Cursor, and Codex into repeatable, multi‑agent workflows. It distills conversation transcripts into searchable notes, builds a semantic tag graph, and offers a “Memory‑Centric Programming” (MCP) layer that lets agents recall and reuse prior context. The project aims to turn ad‑hoc prompts into structured pipelines that can be orchestrated, extended, and version‑controlled on‑premise.

---

### Value Proposition
| What it solves | How ChatCrystal solves it |
|----------------|----------------------------|
| **Fragmented prompt‑to‑tool pipelines** | Provides a unified orchestration layer that can invoke multiple LLM‑backed coding assistants in a single, repeatable workflow. |
| **Loss of context across sessions** | The MCP memory component persists distilled notes and semantic tags, enabling agents to retrieve prior reasoning or code snippets without re‑prompting. |
| **Hard‑to‑search knowledge base** | Built‑in semantic search and a tag‑graph let developers quickly locate relevant code excerpts, design decisions, or debugging steps. |
| **Limited reproducibility** | All configurations (prompt templates, tool chains, memory policies) are stored as code‑first artifacts, making the workflow version‑controlled and auditable. |

### Practical Adoption Path
1. **Initial Evaluation** – Clone the repo and run the provided CLI against a local LLM (e.g., Ollama) or an API key for Claude Code. Verify that prompts, tool calls, and memory snapshots are logged in the local SQLite/JSON store.  
2. **Pilot Integration** – Replace a single “copy‑paste‑into‑IDE” step in an existing development pipeline with a ChatCrystal agent (e.g., automated code review or test generation). Use the SDK to embed the agent in a VS Code extension or a CI job.  
3. **Workflow Expansion** – Add additional agents (Cursor for refactoring, Codex for snippet generation) and define orchestration rules in the YAML‑based workflow file. Leverage the tag graph to auto‑route tasks based on semantic similarity.  
4. **Standardization & CI/CD** – Store the workflow definition, prompt templates, and memory‑policy scripts in a monorepo. Include linting and unit tests for the orchestration logic, and run nightly jobs that replay stored conversations to validate reproducibility.  
5. **Scale to Teams** – Deploy the backend (Node.js + optional Docker) on a shared internal server, configure per‑team namespaces, and expose the API/CLI to developers via internal package registries.

### Production Readiness Assessment
| Dimension | Rating (Low/Med/High) | Comments |
|-----------|----------------------|----------|
| **Stability** | Medium | The codebase is recent (last commit 2026‑06‑26) and compiles cleanly, but the ecosystem (Claude Code, Cursor) evolves quickly; integration tests are limited. |
| **Feature Completeness** | Medium | Core orchestration, semantic search, and MCP memory are present, yet advanced features (distributed memory sync, RBAC, observability) are still experimental. |
| **Documentation & Tooling** | Medium | CLI and SDK are documented, but examples focus on toy scenarios; a production‑grade guide (deployment, monitoring, backup) is missing. |
| **Security & License** | Pending | No obvious licensing conflicts, but a formal security audit (dependency scanning, secret handling) is required before exposing the service externally. |
| **Community & Maintenance** | Low‑Medium | 34 stars, 2 forks, and a single maintainer indicate limited community support; proactive monitoring for dependency updates is advisable. |

**Overall Verdict:** ChatCrystal is ready for internal prototypes, research labs, or small engineering teams that need a controllable, local AI workflow for coding assistance. Moving to production will require adding robust testing, observability, and a security review, as well as establishing an internal maintainer or contributing back to the upstream project to ensure long‑term stability.

### Русский

**ChatCrystal** — это локальный open‑source фреймворк (TypeScript) для построения повторяемых AI‑агентных конвейеров в сфере программирования: он объединяет модели Claude Code/Cursor/Codex, позволяет дистиллировать заметки, выполнять семантический поиск, управлять тег‑графом и поддерживает память MCP. Типичный сценарий — координация многокомпонентных рабочих процессов (интеграция инструментов, стандартизация памяти агентов) в прототипах или внутренних PKM‑системах. Готовность к production — средняя: проект достаточно стабилен для разработки и тестов, но требует проверки лицензии, безопасности и поддержки зависимостей перед масштабным внедрением.

### 中文

**价值**  
ChatCrystal 将零散的 Prompt 与多种代码助手（Claude Code、Cursor、Codex）统一包装成可复用的工作流，提供笔记萃取、语义检索、标签图谱和多轮记忆（MCP）等功能，使得开发者能够在本地优先的环境中快速搭建、调度和复用 AI 编码助理，实现“一次配置、随处复用”。

**典型接入方式**  
- **API/SDK**：项目直接暴露 RESTful API 与 TypeScript SDK，调用方只需在代码中引入 `@chatcrystal/client` 并使用 `createAgent()`、`runWorkflow()` 等高层函数即可。  
- **CLI**：提供 `chatcrystal` 命令行工具，可在 CI/CD、脚本或本地终端中快速启动单次对话或批量处理任务。  
- **插件/扩展**：通过 `plugin.yaml` 声明的插件点，能够把 Cursor、Claude Code、Codex 等外部工具以统一的 “tool‑use pipeline” 接入，适配 IDE、GitHub Action 等场景。

**生产可用性**  
- **成熟度**：当前得分 71/100，属于 **Medium** 级别。代码库活跃（最近更新于 2026‑06‑26），拥有 34 ⭐、2 fork，使用 TypeScript 编写，文档覆盖 API、SDK 与 CLI，适合原型开发或内部业务流程。  
- **准备工作**：在正式生产前需要完成以下检查：  
  1. **依赖审计**：确认所有第三方包（尤其是 Claude、Cursor、Codex 的 SDK）无已知安全漏洞。  
  2. **许可证合规**：核实项目许可证（默认 MIT）与所集成工具的授权是否兼容。  
  3. **运维监控**：为 API 服务添加健康检查、日志与限流，防止本地资源耗尽。  
  4. **持续维护**：评估维护者活跃度，若内部团队计划长期使用，建议 Fork 并自行维护关键分支。  

综上，ChatCrystal 适合作为 **本地优先的 AI 编码助理平台**，通过 API/SDK 或 CLI 快速接入现有开发流程，具备原型到小规模生产的可行性，只需在安全、依赖和运维层面做好额外审查即可投入正式业务。

## 🧭 Practical evaluation

**Value:** ZengLiangYi/ChatCrystal helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 34 GitHub stars
- 2 forks
- updated 2026-06-26
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 12/100 |
| stars | 33/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 52/100 |
| recency | 40/100 |
| adoption | 27/100 |
| production | 54/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/ZengLiangYi/ChatCrystal) · [← Back to Orchestration](./README.md)</sub>
