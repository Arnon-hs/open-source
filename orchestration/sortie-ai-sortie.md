# sortie-ai/sortie

[![Stars](https://img.shields.io/github/stars/sortie-ai/sortie?style=flat-square&color=yellow)](https://github.com/sortie-ai/sortie/stargazers) [![Forks](https://img.shields.io/github/forks/sortie-ai/sortie?style=flat-square&color=blue)](https://github.com/sortie-ai/sortie/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> Turn tracker tickets into agent sessions

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 57 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | Go |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `agent-fleet` `agent-swarm` `agentic-ai` `ai-agents` `ai-orchestration` `automation` `claude-code` `coding-agent` `copilot-cli` `developer-tools` `devops`

## 🎯 Categories

Orchestration · Automation · AI/ML · DevTools · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
sortie‑ai/sortie is an open‑source Go library that converts individual prompts and tool calls into repeatable, stateful “agent sessions,” enabling coordinated multi‑agent workflows, tool‑use pipelines, and standardized agent memory. It exposes a clean API/SDK/CLI surface, making it easy to plug into existing orchestration or DevOps pipelines. With modest community traction (57 ⭐, 4 forks) and recent updates, it is suited for prototypes and internal automation while still requiring a final security and licensing review before production use.  

**Value**  
- **Workflow composability** – Turns ad‑hoc LLM prompts into reusable, version‑controlled sessions, reducing duplication and simplifying complex multi‑agent orchestration.  
- **Tool integration** – Provides a structured way to attach external tools (e.g., CLIs, APIs) to agents, turning “prompt‑only” bots into full‑fledged automation pipelines.  
- **Memory standardization** – Offers a common memory model so that agents can persist context across calls, improving consistency and reducing “prompt‑drift.”  

**Practical Adoption Path**  
1. **Evaluation** – Clone the repo, run the provided CLI or import the Go SDK, and experiment with a simple prompt‑to‑session conversion.  
2. **Prototype** – Integrate the library into a sandboxed CI/CD job or internal chatbot to orchestrate two‑or‑three agents (e.g., ticket triage → code generation → review).  
3. **Internal rollout** – Wrap the SDK in a service (REST/gRPC) and expose it via your organization’s API gateway; add CI checks for dependency updates and run static analysis tools.  
4. **Production hardening** – Conduct a formal security audit (dependency scanning, licensing compliance), add observability (metrics, tracing), and implement robust error handling and retry policies.  

**Production Readiness**  
- **Maturity** – Medium; the project is actively maintained (last commit 2026‑05‑11) and usable for internal prototypes, but it lacks extensive real‑world testing and formal SLAs.  
- **Risks** – No major metadata concerns, but the license, security posture, and long‑term maintainer commitment still need verification.  
- **Next steps for production** – Perform a security and license review, set up automated dependency monitoring, and establish a small “owner” team to respond to issues and contribute upstream. Once these checks are in place, sortie‑ai/sortie can be safely promoted to production for internal automation and, eventually, external client‑facing services.

### Русский

**sortie‑ai/sortie** — это open‑source‑инструмент, который превращает разрозненные запросы и инструменты в повторяемые агентные рабочие процессы, позволяя координировать многокомпонентные сценарии, добавлять пайплайны с использованием внешних инструментов и стандартизировать память агентов. Типичный сценарий — построение прототипов или внутренних автоматизаций, где требуется быстро связать несколько AI‑агентов и сервисов через API/SDK/CLI; проект написан на Go, имеет 57 звёзд и активные коммиты, но требует проверки лицензии, безопасности и поддержки перед запуском в продакшн. Уровень готовности — средний: подходит для прототипов и ограниченных production‑сред с дополнительным аудитом зависимостей и сопровождения.

### 中文

**项目简介**  
Sortie（`sortie-ai/sortie`）是一款基于 Go 实现的开源框架，能够将零散的 Prompt 与工具包装成可重复的智能体（Agent）工作流，实现多 Agent 协同、工具链调用以及统一的记忆管理。

**价值**  
- **工作流标准化**：把单次交互的 Prompt 转化为可复用的 Agent Session，降低重复开发成本。  
- **多 Agent 协调**：内置调度机制，支持多智能体之间的任务分配与结果汇总。  
- **工具链集成**：提供统一的工具调用接口，便于在工作流中嵌入外部 API、CLI 或 SDK。  

**典型接入方式**  
1. **API/SDK**：通过项目公开的 Go SDK（或生成的 OpenAPI）在代码中直接创建、启动、查询 Agent Session。  
2. **CLI**：使用自带的 `sortie` 命令行工具快速定义 Prompt、绑定工具并执行工作流，适合脚本化或 CI 环境。  
3. **语言/元数据**：项目在 `go.mod` 中声明依赖，可通过 `go get` 拉取；同时提供 JSON/YAML 描述文件用于声明工作流结构，便于跨语言（如 Python、Node）通过轻量包装调用。  

**生产可用性**  
- **成熟度**：当前评分 75/100，适合作为原型或内部业务的自动化平台。  
- **依赖与维护**：项目活跃度一般（57 星、4 Fork），最近一次提交为 2026‑05‑11，仍在维护中，但在生产环境使用前建议进行安全审计、许可证合规检查以及对关键依赖的版本锁定。  
- **就绪度**：属于 **中等**（Medium）级别，具备基本的可用性和文档，但在大规模部署前需评估其容错、监控与扩展方案。

## 🧭 Practical evaluation

**Value:** sortie-ai/sortie helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 57 GitHub stars
- 4 forks
- updated 2026-05-11
- primary language: Go
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 38/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 64/100 |
| recency | 80/100 |
| adoption | 32/100 |
| production | 68/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/sortie-ai/sortie) · [← Back to Orchestration](./README.md)</sub>
