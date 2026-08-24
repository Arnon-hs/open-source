# dapr/dapr-agents

[![Stars](https://img.shields.io/github/stars/dapr/dapr-agents?style=flat-square&color=yellow)](https://github.com/dapr/dapr-agents/stargazers) [![Forks](https://img.shields.io/github/forks/dapr/dapr-agents?style=flat-square&color=blue)](https://github.com/dapr/dapr-agents/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> Build autonomous, resilient and observable AI agents with built-in workflow orchestration, security, statefulness and telemetry.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 673 |
| 🍴 **Forks** | 121 |
| 💻 **Language** | Python |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Orchestration · Automation · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Dapr Agents is an open‑source Python framework that lets you compose autonomous, stateful AI agents with built‑in workflow orchestration, security, and telemetry. By turning isolated prompts and tool calls into repeatable, observable pipelines, it enables multi‑agent coordination, tool‑use pipelines, and standardized agent memory. The project is moderately popular (≈670 ★, 120 forks) and actively maintained as of May 2026.

**Value**  
- **End‑to‑end agent orchestration** – Dapr Agents abstracts the plumbing of message passing, state persistence, and observability, so developers can focus on the business logic of each AI “agent.”  
- **Built‑in non‑functional concerns** – Security (identity, secret management), resilience (retries, circuit‑breakers), and telemetry (metrics, tracing) are provided out of the box, reducing the operational overhead of custom implementations.  
- **Reusable workflows** – Prompt sequences, tool‑use steps, and memory handling are defined once and can be reused across projects, accelerating prototyping and ensuring consistency.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided examples, and replace the sample prompts/tools with your own logic.  
2. **Integrate** – Wrap existing Python services or LLM wrappers as Dapr Agent components; use the Dapr SDK to connect to your preferred state store (e.g., Redis, Azure Cosmos) and observability stack (Prometheus, OpenTelemetry).  
3. **Validate** – Perform a manual code review and security audit (the integration signals are sparse), and run end‑to‑end tests for your specific workflow.  
4. **Hardening** – Enable Dapr’s secret management, configure TLS/mTLS, and set resource limits before moving to a staging environment.  
5. **Deploy** – Deploy via Docker/Kubernetes using the official Dapr sidecar, monitor with the built‑in telemetry, and iterate.

**Production Readiness**  
- **Maturity**: Medium. The codebase is actively updated and has a healthy star/fork count, making it suitable for prototypes and internal tooling.  
- **Dependencies**: Relies on the Dapr runtime and Python ecosystem; ensure compatible versions and monitor upstream Dapr releases.  
- **Operational considerations**: Verify licensing, perform a security posture review, and establish a maintenance plan for the Dapr sidecar and any state stores.  
- **Recommendation**: Deploy in a controlled environment (staging or internal services) first, conduct thorough testing and monitoring, and only promote to production once the integration, security, and reliability checks are satisfied.

### Русский

**dapr/dapr-agents** — это open‑source фреймворк для создания автономных AI‑агентов с оркестрацией рабочих процессов, встроенной безопасностью, состоянием и телеметрией. Он позволяет превратить разрозненные подсказки и инструменты в повторяемые, масштабируемые пайплайны — например, координировать взаимодействие нескольких агентов, добавлять цепочки использования внешних сервисов или стандартизировать «память» агента. Готовность к production — средняя: проект подходит для прототипов и внутренних решений, но требует проверки зависимостей, лицензий и активного сопровождения перед запуском в продакшн.

### 中文

**项目简介（2‑3 句）**  
dapr/dapr‑agents 是一个基于 Dapr 的开源框架，帮助开发者快速构建具备工作流编排、状态管理、安全与可观测性的自主 AI 代理。它将零散的 Prompt 与工具包装成可复用、可监控的代理流水线，适用于多代理协同、工具调用链和统一记忆管理等场景。

**价值**  
- **统一化工作流**：把单个 Prompt、工具或模型调用抽象为可编排的步骤，形成端到端的业务流程。  
- **内置弹性与可观测**：利用 Dapr 的分布式状态、服务发现、密钥管理以及 OpenTelemetry 集成，实现故障自动恢复和全链路监控。  
- **可复用的记忆层**：提供统一的状态存储（Redis、Mongo、Cosmos 等），让不同代理能够共享和检索历史上下文，提升对话连贯性。

**典型接入方式**  
1. **环境准备**：在 Kubernetes 或本地 Docker Compose 中部署 Dapr sidecar（`dapr init`），并根据需求启用状态存储、秘钥管理等组件。  
2. **定义 Agent**：在 Python 项目中继承 `dapr_agents.Agent`，声明工具函数、状态模型以及工作流步骤（使用 Dapr Workflow 或自定义 DAG）。  
3. **注册与调用**：通过 Dapr 的服务调用 API（HTTP/gRPC）将 Agent 暴露为微服务，其他系统或前端可直接调用 `/v1.0/invoke/<app-id>/method/<endpoint>`。  
4. **监控&调优**：开启 OpenTelemetry 导出器，将指标、日志、追踪推送到 Prometheus/Grafana、Jaeger 或 Azure Monitor，实时观察代理的执行情况。

**生产可用性**  
- **成熟度**：当前评分 66/100，属于 **中等** 级别。代码活跃（2026‑05‑14 最近更新），拥有 673 ★、121 Fork，适合原型、内部业务或对可靠性要求不极端的生产环境。  
- **准备工作**：在正式上线前需完成以下检查：  
  1. **依赖审计**：确认所有 Dapr 组件（state store、pub/sub、secret store）已在目标平台经过安全加固。  
  2. **安全评估**：审查许可证（Apache‑2.0）兼容性，评估容器镜像的 CVE 报告。  
  3. **运维规划**：配置自动扩缩容、健康探针以及故障转移策略，确保 sidecar 与工作流服务的高可用。  
- **适用场景**：快速验证多代理协作、工具链集成或记忆化对话系统；在经过上述审计后，可推广至对可观测性和弹性有基本要求的生产业务。  

综上，dapr/dapr‑agents 为 AI 代理提供了“一站式”编排与运维能力，只要在上线前完成依赖、安保与运维的细致检查，即可在内部或轻量级生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** dapr/dapr-agents helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 673 GitHub stars
- 121 forks
- updated 2026-05-14
- primary language: Python

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 52/100 |
| stars | 60/100 |
| topics | 0/100 |
| outlook | 46/100 |
| quality | 46/100 |
| recency | 20/100 |
| adoption | 58/100 |
| production | 45/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/dapr/dapr-agents) · [← Back to Orchestration](./README.md)</sub>
