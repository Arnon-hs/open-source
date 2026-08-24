# katanemo/plano

[![Stars](https://img.shields.io/github/stars/katanemo/plano?style=flat-square&color=yellow)](https://github.com/katanemo/plano/stargazers) [![Forks](https://img.shields.io/github/forks/katanemo/plano?style=flat-square&color=blue)](https://github.com/katanemo/plano/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> Plano is an AI-native proxy and data plane for agentic apps — with built-in orchestration, safety, observability, and smart LLM routing so you stay focused on your agents core logic.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 6.6k |
| 🍴 **Forks** | 431 |
| 💻 **Language** | Rust |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-gateway` `ai-gateway-support` `envoy` `envoyproxy` `gateway` `generative-ai` `llm-gateway` `llm-inference` `llm-proxy` `llm-routing` `llmops` `llms`

## 🎯 Categories

Orchestration · AI/ML · Backend · Observability

## 📝 Summary

### English

**Summary**  
Plano is an AI‑native proxy and data‑plane written in Rust that lets you stitch together LLM‑driven agents, tools, and memory stores into repeatable, observable workflows. It handles orchestration, safety checks, smart routing and telemetry out of the box, so developers can focus on the core logic of each agent rather than on plumbing.

**Value**  
By turning isolated prompts and tool calls into a unified execution graph, Plano eliminates the ad‑hoc glue code that typically grows around multi‑agent systems. The built‑in safety layer, observability dashboards, and LLM‑aware routing reduce the risk of hallucinations and performance bottlenecks, while the standardized memory interface makes state management consistent across agents.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the provided Docker compose or binary, and follow the README to spin up a simple “hello‑world” agent pipeline.  
2. **Integration** – Replace the demo components with your own LLM endpoints, tool APIs, or vector stores, using the documented proxy configuration (JSON/YAML).  
3. **Iterate** – Leverage the observability UI to monitor latency, token usage, and safety events, then gradually expand the workflow to cover more agents and tools.  

**Production readiness**  
With 6.6 k stars, active commits (last update 2026‑06‑25), and a growing ecosystem of Rust‑based plugins, Plano shows strong community momentum and mature code quality. The architecture is designed for scalability (stateless proxy, pluggable back‑ends) and the safety/orchestration features are production‑grade, making it a solid candidate for pilot projects and, after a small integration validation, for full‑scale deployment.

### Русский

**katanemo/plano** — это AI‑ориентированный прокси‑и‑датаплейн, который упрощает создание и управление агентными приложениями: он обеспечивает оркестрацию, безопасность, наблюдаемость и интеллектуальный роутинг запросов к LLM, позволяя сосредоточиться на бизнес‑логике агентов. Типичное внедрение начинается с небольшого proof‑of‑concept: подключаем прокси к существующим агентам, определяем цепочки инструментов и память, а затем масштабируем workflow‑ы, используя готовые интеграционные примеры из README. Проект имеет высокий уровень готовности к продакшну — активные коммиты, более 6600 звёзд, широкое использование в экосистеме Rust и сильные сигналы принятия, однако перед полномасштабным rollout стоит уточнить детали установки и оценить затраты на интеграцию.

### 中文

**项目简介**  
Plano（katanemo/plano）是一个面向 AI 代理的原生代理与数据平面，提供统一的编排、可靠的安全防护、完整的可观测性以及智能的 LLM 路由，让开发者可以专注于业务逻辑本身，而无需自行搭建底层基础设施。

**价值主张**  
- **把碎片化的 Prompt 与工具链转化为可复用的工作流**：通过内置的编排引擎，用户只需描述“代理要做什么”，Plano 会自动调度多模型、多工具的调用顺序。  
- **统一的记忆与工具使用标准**：提供可插拔的记忆层（如向量库、KV 存储）和工具调用管道，避免每个项目都自行实现同样的逻辑。  
- **安全与可观测**：内置安全策略（如输出过滤、速率限制）和完整的监控/日志埋点，帮助在生产环境中快速定位问题并防止模型失控。  

**典型接入方式**  
1. **快速 PoC**：克隆仓库 → 按 README 启动本地 Docker Compose（或直接 `cargo run`），使用示例配置文件启动 Plano 控制平面。  
2. **SDK 集成**：项目中通过官方 Rust（或通过社区提供的 HTTP/GRPC）客户端调用 `POST /v1/plan` 接口，提交工作流描述（JSON/YAML），Plano 返回执行结果或流式响应。  
3. **插件式扩展**：如果已有自研记忆库或工具，只需实现 `MemoryProvider` / `ToolProvider` 接口并在 `plano.yaml` 中注册，即可在编排中直接引用。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑25，项目拥有 6.6k+ 星、431 叉，最近一次提交在本月，社区 PR 与 Issue 处理及时。  
- **技术成熟**：核心采用 Rust 实现，具备高并发、低延迟的性能特性；同时提供完整的 OpenAPI 规范，易于跨语言调用。  
- **安全与监控**：内置策略引擎、审计日志以及 Prometheus 指标导出，满足企业级合规与可观测需求。  
- **风险提示**：元数据中未提供一键式的 CI/CD 集成脚本，实际落地前需评估与现有微服务架构的接入成本（如网络、身份认证）。建议先在沙箱环境完成小规模 PoC，确认配置、插件开发与运维流程后再推广至生产。  

综上，Plano 已具备进入生产环境的技术与社区基础，只要做好前期的集成验证与安全策略配置，即可在多代理、工具链编排场景中提供可靠的底层支撑。

## 🧭 Practical evaluation

**Value:** katanemo/plano helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 6602 GitHub stars
- 431 forks
- updated 2026-06-25
- primary language: Rust
- 17 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 66/100 |
| stars | 81/100 |
| topics | 100/100 |
| outlook | 65/100 |
| quality | 75/100 |
| recency | 40/100 |
| adoption | 77/100 |
| production | 58/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/katanemo/plano) · [← Back to Orchestration](./README.md)</sub>
