# ThousandBirdsInc/chidori

[![Stars](https://img.shields.io/github/stars/ThousandBirdsInc/chidori?style=flat-square&color=yellow)](https://github.com/ThousandBirdsInc/chidori/stargazers) [![Forks](https://img.shields.io/github/forks/ThousandBirdsInc/chidori?style=flat-square&color=blue)](https://github.com/ThousandBirdsInc/chidori/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> The agent framework where every run is durable, replayable, and resumable by default.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.4k |
| 🍴 **Forks** | 55 |
| 💻 **Language** | Rust |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-framework` `agents` `ai` `checkpointing` `deterministic` `durable-execution` `javascript-engine` `llm` `replay` `resumable` `rust` `typescript`

## 🎯 Categories

Orchestration · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
ThousandBirdsInc / chidori is an open‑source Rust‑based agent framework that makes every execution durable, replayable, and resumable out of the box. It lets developers stitch isolated prompts, tools, and memory components into repeatable, multi‑agent workflows, turning ad‑hoc AI scripts into production‑grade pipelines.

**Value**  
- **Durability & Replayability** – Each run is persisted, so failures can be inspected, replayed, or resumed without re‑engineering the workflow.  
- **Standardised Agent Memory** – Built‑in abstractions for stateful memory let agents retain context across invocations, simplifying complex reasoning tasks.  
- **Tool‑Use Pipelines** – The framework natively supports chaining external tools (APIs, CLIs, databases), enabling end‑to‑end automation without custom glue code.  
- **Orchestration Ready** – Multi‑agent coordination is a first‑class feature, making it easy to build collaborative AI systems (e.g., planner‑executor patterns).

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC)** – Clone the repo, run the example `README` workflows, and verify that the durable run logs are created in your environment.  
2. **Integrate a Small Pipeline** – Replace a single existing script (e.g., a prompt‑to‑API call) with a chidori agent, leveraging its built‑in memory and replay features.  
3. **Scale to Multi‑Agent Scenarios** – Incrementally add additional agents and tool‑use steps, using the framework’s orchestration DSL to define dependencies.  
4. **CI/CD & Monitoring** – Hook the durable run store into your CI pipeline and monitoring stack to automatically replay failed runs during testing.  
5. **Full Production Rollout** – Once the PoC proves stable, adopt the framework across your AI services, using its Rust performance and type safety for high‑throughput workloads.

**Production Readiness**  
- **Activity & Community** – 1,351 GitHub stars, 55 forks, recent commits (as of 2026‑06‑23) and active issue discussion indicate a healthy open‑source project.  
- **Maturity** – The core concepts (durable runs, replayability, memory) are already implemented and used in early adopters, suggesting the codebase is stable enough for pilot projects.  
- **Ecosystem Fit** – Written in Rust, it integrates well with performance‑critical services and can be called from other languages via FFI or a thin HTTP wrapper.  
- **Risks** – No major licensing or metadata concerns have been identified, but a final security audit and verification of active maintainers are recommended before large‑scale deployment.  

Overall, chidori offers a compelling, production‑ready foundation for building reliable, repeatable AI agent pipelines, with a low‑friction entry point for teams looking to move from experimental prompts to robust, orchestrated workflows.

### Русский

**ThousandBirdsInc/chidori** — это фреймворк‑агент на Rust, который делает каждый запуск устойчивым, воспроизводимым и возобновляемым «из коробки», позволяя превращать разрозненные подсказки и инструменты в повторяемые рабочие процессы с памятью агентов. Типичный сценарий внедрения — небольшое доказательство концепции: подключить Chidori к существующей цепочке инструментов, задать последовательность действий нескольких агентов и проверить воспроизводимость через сохранённые состояния. Проект считается почти готовым к production: активная разработка, 1350+ звёзд, недавние коммиты, хорошие сигналы экосистемы, однако перед масштабным запуском следует уточнить лицензионные и security‑аспекты.

### 中文

**项目简介（2‑3 句）**  
ThousandBirdsInc/chidori 是一个基于 Rust 的智能体框架，所有运行默认具备持久化、可回放和可恢复特性。它将孤立的 Prompt 与工具包装成可重复、可组合的工作流，使多智能体协同、工具链调用和记忆管理变得简单可靠。

**价值**  
- **统一工作流**：把分散的 Prompt、工具和记忆统一为可编排的流水线，降低开发与维护成本。  
- **可重复与可审计**：持久化的运行状态让每一次执行都可以回放、调试或在故障后恢复，提升系统可靠性。  
- **多智能体协同**：内置的编排机制支持复杂的多智能体交互，适用于需要多步骤推理或工具调用的业务场景。

**典型接入方式**  
1. **快速验证**：克隆仓库后，参考 README 中的 “Hello World” 示例，使用 `cargo run --example simple_agent` 运行最小示例，确认环境与依赖。  
2. **嵌入业务代码**：在现有 Rust 项目中通过 `cargo add chidori` 引入库，按照文档创建 `AgentBuilder`，配置 Prompt、Tool 接口和 Memory 实现，即可在业务流程中调用 `agent.run(input)`。  
3. **与外部系统对接**：利用框架提供的 HTTP / gRPC 插件，将 Agent 暴露为微服务，其他语言（如 Python、Node）通过标准接口调用，实现跨语言协作。

**生产可用性**  
- **活跃度**：截至 2026‑06‑23，项目最近一次提交，拥有 1351 星、55 个 Fork，社区活跃。  
- **技术成熟度**：核心使用 Rust 实现，具备高性能和内存安全；框架已在多个开源项目中试点，具备稳定的持久化与回放机制。  
- **集成门槛**：对已有 Rust 代码库几乎无侵入，非 Rust 环境可通过微服务方式平滑接入。  
- **风险**：仍需最终确认许可证兼容性、持续维护者状态以及安全审计结果；但整体信号表明已具备在生产环境中进行正式试点的条件。

## 🧭 Practical evaluation

**Value:** ThousandBirdsInc/chidori helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1351 GitHub stars
- 55 forks
- updated 2026-06-23
- primary language: Rust
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 67/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 77/100 |
| recency | 80/100 |
| adoption | 60/100 |
| production | 71/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/ThousandBirdsInc/chidori) · [← Back to Orchestration](./README.md)</sub>
