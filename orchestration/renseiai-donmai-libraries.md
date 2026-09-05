# RenseiAI/donmai-libraries

[![Stars](https://img.shields.io/github/stars/RenseiAI/donmai-libraries?style=flat-square&color=yellow)](https://github.com/RenseiAI/donmai-libraries/stargazers) [![Forks](https://img.shields.io/github/forks/RenseiAI/donmai-libraries?style=flat-square&color=blue)](https://github.com/RenseiAI/donmai-libraries/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> The open-source software factory — multi-agent fleet management for coding agents

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 60 |
| 🍴 **Forks** | 10 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `claude` `coding-agent` `fleet-management` `linear` `multi-agent` `open-source` `orchestrator` `typescript`

## 🎯 Categories

Orchestration · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
RenseiAI’s **donmai‑libraries** is an open‑source “software factory” that lets you stitch together isolated LLM prompts, tools, and memory stores into repeatable, multi‑agent workflows. Built in TypeScript, it provides orchestration primitives for coordinating coding agents, adding tool‑use pipelines, and standardising agent state across a fleet.

**Value**  
- **From ad‑hoc prompts to production‑grade pipelines:** The library abstracts away the boilerplate of launching, monitoring, and persisting the state of multiple agents, turning experimental prompt chains into reusable components.  
- **Accelerates complex AI‑assisted development:** Teams can compose specialized agents (e.g., code generator, test writer, reviewer) that hand off work via a shared memory layer, reducing manual glue code and improving consistency.  
- **Extensible and language‑agnostic:** Although the core is TypeScript, the APIs expose generic interfaces that can be called from any language that can invoke a Node.js service, making it easy to embed in existing CI/CD or IDE tooling.

**Practical Adoption Path**  

| Step | Action | Goal |
|------|--------|------|
| 1️⃣  | **Prototype a single‑agent use case** – clone the repo, run the provided README example (e.g., a “write‑test‑then‑refactor” pipeline). | Validate that the library works in your environment and understand its API surface. |
| 2️⃣  | **Add a custom tool** – implement a small wrapper (e.g., a static‑analysis CLI) that conforms to the `Tool` interface and register it in the orchestrator. | Test the tool‑integration flow and verify memory sharing between agents. |
| 3️⃣  | **Scale to a multi‑agent fleet** – define a workflow file (YAML/JSON) that spins up a code‑generator, a reviewer, and a deployment‑checker agent, linking them via the built‑in memory store. | Demonstrate end‑to‑end coordination and measure latency/throughput. |
| 4️⃣  | **CI/CD integration** – containerise the orchestrator, add it as a step in your pipeline (e.g., GitHub Actions), and expose health checks. | Move from a proof‑of‑concept to a repeatable build‑time automation. |
| 5️⃣  | **Operational monitoring & governance** – hook up logging, tracing (OpenTelemetry), and role‑based access controls; audit the license and dependency tree. | Harden the setup for internal production use. |

**Production Readiness**  
- **Maturity:** Medium. The project has recent activity (last commit 2026‑07‑05), 60 stars, and a modest fork count, indicating community interest but limited large‑scale validation.  
- **Dependencies & Maintenance:** Written in TypeScript with a modest dependency graph; however, a formal security audit and a check on active maintainers are still required before a production rollout.  
- **Best‑fit scenarios:** Internal prototypes, developer tooling, or “AI‑assist” features that can tolerate occasional downtime while the library is further hardened. For mission‑critical services, plan additional testing, version pinning, and possibly contribute patches to address any security or stability gaps.  

In short, donmai‑libraries offers a practical way to turn scattered LLM prompts into orchestrated, multi‑agent pipelines, and it can be adopted incrementally—starting with a small proof‑of‑concept and scaling up to CI/CD integration—provided you perform the usual due‑diligence on security, licensing, and long‑term maintainer support.

### Русский

RenseiAI/donmai-libraries — это TypeScript‑фреймворк для оркестрации многопользовательских AI‑агентов, позволяющий превратить отдельные подсказки и инструменты в повторяемые, стандартизированные рабочие процессы с поддержкой памяти и пайплайнов инструментов. Типичное внедрение начинается с небольшого proof‑of‑concept: подключаем библиотеку к существующей системе, описываем цепочку агентов в README и проверяем её на простом кейсе координации нескольких моделей. Готовность к production — средняя: проект подходит для прототипов и внутренних сервисов, но перед запуском в прод необходимо проверить лицензию, безопасность зависимостей и наличие активных мейнтейнеров.

### 中文

**项目简介（2‑3 句话）**  
RenseiAI/donmai‑libraries 是一套面向编码机器人的开源软件工厂，提供多代理（multi‑agent）编排能力，能够把零散的 Prompt 与工具组合成可重复、可维护的工作流。它通过统一的记忆层、工具调用管线以及任务调度框架，让多个 AI 代理协同完成复杂的编码任务。

**价值主张**  
- **把孤立的 Prompt 与工具转化为可复用的工作流**，显著提升开发效率和代码质量。  
- **统一的记忆与状态管理**，让不同代理之间能够共享上下文，避免信息丢失。  
- **可视化的多代理调度**，支持并行、串行及条件分支等复杂编排模式，适用于代码生成、单元测试、自动重构等场景。

**典型接入方式**  
1. **阅读 README 与示例**，快速跑通 `npm install`、`npm run demo` 的最小演示。  
2. **在现有项目中引入库**：在 TypeScript 项目里 `import { AgentFleet, ToolRegistry } from 'donmai-libraries'`，根据业务需求配置 `AgentFleet`（定义代理、记忆存储、调度策略）和 `ToolRegistry`（注册 CLI、API、IDE 插件等工具）。  
3. **编写自定义 Prompt 与工具适配器**，利用库提供的 `Agent` 接口实现业务专属的代码生成或审查逻辑。  
4. **通过 CI/CD 流水线进行验证**，先在小型 PoC（例如单个微服务的代码生成）中验证功能与性能，再逐步扩展到更大范围。

**生产可用性评估**  
- **成熟度**：GitHub ★60、Fork 10，最近一次更新为 2026‑07‑05，使用 TypeScript 开发，社区活跃度一般。适合作为原型或内部工具的底层框架。  
- **依赖与维护**：需自行审查第三方依赖的安全性，并确认项目维护者的响应速度；在生产环境前建议锁定依赖版本并加入内部安全审计。  
- **部署建议**：先在隔离的测试环境进行完整的 PoC，验证多代理调度、记忆持久化以及工具调用的可靠性；随后在内部 CI 中加入单元/集成测试，确保升级不会破坏既有工作流。  
- **总体可用性**：**中等**（Medium）。对原型、内部自动化或实验性产品非常适用；若用于面向外部用户的关键业务，建议在安全、监控和运维层面进行额外加固后再投入生产。

## 🧭 Practical evaluation

**Value:** RenseiAI/donmai-libraries helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 60 GitHub stars
- 10 forks
- updated 2026-07-05
- primary language: TypeScript
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 26/100 |
| stars | 38/100 |
| topics | 100/100 |
| outlook | 68/100 |
| quality | 66/100 |
| recency | 80/100 |
| adoption | 35/100 |
| production | 66/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/RenseiAI/donmai-libraries) · [← Back to Orchestration](./README.md)</sub>
