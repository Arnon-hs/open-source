# frumu-ai/tandem

[![Stars](https://img.shields.io/github/stars/frumu-ai/tandem?style=flat-square&color=yellow)](https://github.com/frumu-ai/tandem/stargazers) [![Forks](https://img.shields.io/github/forks/frumu-ai/tandem?style=flat-square&color=blue)](https://github.com/frumu-ai/tandem/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Tandem is the authority layer for AI-first work: runtime authority for agents, tools, memory, approvals, and audit trails.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 108 |
| 🍴 **Forks** | 13 |
| 💻 **Language** | Rust |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic-workflow` `anthropic` `governed-execution` `help-wanted` `human-in-the-loop` `local-first` `ollama` `openai` `openrouter`

## 🎯 Categories

Orchestration · Automation

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Tandem is an open‑source “authority layer” that lets you stitch together AI agents, tools, memory stores, approval gates and audit trails into repeatable, governed workflows. Written in Rust, it provides runtime orchestration, security controls and provenance for AI‑first applications, turning ad‑hoc prompts into durable pipelines.

**Value**  
- **Governed AI pipelines** – Tandem centralises policy (approvals, audit logs) and state (agent memory) so that multi‑agent or tool‑augmented workflows are auditable and compliant.  
- **Reusability** – By abstracting agents, tools and their interactions into composable components, teams can build libraries of “prompt‑as‑code” that are versioned and shared across projects.  
- **Security & compliance** – Built‑in runtime authority and audit trails help organisations meet internal governance and external regulatory requirements for AI usage.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the provided examples, and verify the README instructions on a single‑agent use case.  
2. **Pilot Integration** – Wrap an existing internal tool or LLM endpoint with Tandem’s agent‑tool interface, add a simple approval step, and test end‑to‑end execution in a sandbox environment.  
3. **Incremental Expansion** – Gradually layer additional agents, memory back‑ends, and audit logging, while automating CI/CD for the Rust components.  
4. **Production Hardening** – Conduct a security audit of dependencies, lock the Rust toolchain, and establish monitoring for the authority service before rolling out to production workloads.

**Production Readiness**  
Tandem sits at a **medium** readiness level: it is actively maintained (last commit 2026‑06‑23), has modest community traction (108 ★, 13 forks) and is written in a performant, safety‑focused language (Rust). It is suitable for prototypes, internal tooling, or regulated environments where governance outweighs the need for enterprise‑grade SLAs. Before production use, teams should verify the licensing terms, perform a dependency vulnerability scan, and confirm that an active maintainer can address any critical issues that arise.

### Русский

Tandem — это слой авторизации для AI‑ориентированных приложений, который обеспечивает runtime‑контроль над агентами, инструментами, памятью, процессом одобрения и аудита, позволяя превращать разрозненные запросы и инструменты в воспроизводимые рабочие потоки. Типичное внедрение начинается с небольшого proof‑of‑concept: интегрировать библиотеку в существующий Rust‑проект, настроить базовый конвейер с несколькими агентами и инструментами, проверить работу памяти и журналов аудита, а затем расширять сценарий. Проект находится на среднем уровне готовности: подходит для прототипов и внутренних процессов, но требует проверки зависимостей, лицензии и поддержки перед запуском в продакшн.

### 中文

**价值**  
Tandem 为 AI‑first 应用提供“运行时权威层”，统一管理智能体、工具、记忆、审批和审计日志。它能够把零散的 Prompt 与工具包装成可重复、可追踪的工作流，让多智能体协同、工具链调用以及记忆管理变得标准化、可审计，从而大幅提升研发效率和系统可靠性。

**典型接入方式**  
1. **先做小型 PoC**：在项目根目录 clone 仓库，阅读 `README.md` 中的快速启动示例，使用提供的 Dockerfile 或 `cargo run` 启动本地 Tandem 服务。  
2. **定义 Agent/Tool 配置**：通过 JSON/YAML 描述智能体、可调用工具及其权限，放入 `config/` 目录，Tandem 会在启动时自动加载。  
3. **在业务代码中调用**：使用官方的 Rust SDK（或通过 HTTP/REST 接口）向 Tandem 注册智能体、提交任务、查询记忆或获取审计记录。  
4. **逐步扩展**：在 PoC 验证后，可把 Tandem 部署到 Kubernetes（提供 Helm chart）或云原生环境，配合现有 CI/CD 完成持续集成。

**生产可用性**  
- **成熟度**：目前评分 71/100，GitHub 具备 108 星、13 Fork，活跃更新至 2026‑06‑23，代码基于 Rust，具备较好的性能和安全特性。  
- **适用场景**：适合原型开发、内部工具链以及需要审计、权限控制的多智能体工作流。  
- **上线注意**：在正式生产前需完成以下检查：  
  1. **依赖审计**：确认所有第三方 crate 的许可证兼容性和已知安全漏洞。  
  2. **安全加固**：开启 TLS、API Token 认证，并对审计日志进行加密存储。  
  3. **运维准备**：配置持久化存储（Memory、Approval、Audit），并为关键组件（如数据库、消息队列）设定健康检查与自动伸缩。  
- **结论**：在完成上述依赖与安全审查后，Tandem 可作为内部生产环境的核心编排层使用；若对高可用和多租户有更严格需求，则需自行实现相应的 HA 与治理扩展。

## 🧭 Practical evaluation

**Value:** frumu-ai/tandem helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 108 GitHub stars
- 13 forks
- updated 2026-06-23
- primary language: Rust
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 43/100 |
| topics | 100/100 |
| outlook | 62/100 |
| quality | 58/100 |
| recency | 40/100 |
| adoption | 39/100 |
| production | 54/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/frumu-ai/tandem) · [← Back to Orchestration](./README.md)</sub>
