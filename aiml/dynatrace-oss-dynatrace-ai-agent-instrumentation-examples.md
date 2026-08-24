# dynatrace-oss/dynatrace-ai-agent-instrumentation-examples

[![Stars](https://img.shields.io/github/stars/dynatrace-oss/dynatrace-ai-agent-instrumentation-examples?style=flat-square&color=yellow)](https://github.com/dynatrace-oss/dynatrace-ai-agent-instrumentation-examples/stargazers) [![Forks](https://img.shields.io/github/forks/dynatrace-oss/dynatrace-ai-agent-instrumentation-examples?style=flat-square&color=blue)](https://github.com/dynatrace-oss/dynatrace-ai-agent-instrumentation-examples/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> Dynatrace AI Observability OTel instrumentation examples

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 85 |
| 🍴 **Forks** | 22 |
| 💻 **Language** | Python |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agents` `ai` `genai` `instrumentation` `opentelemetry` `otel` `python` `typescript`

## 🎯 Categories

AI/ML · Observability

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The *dynatrace‑oss/dynatrace‑ai‑agent‑instrumentation‑examples* repository provides ready‑to‑run OpenTelemetry instrumentation snippets that let you attach Dynatrace AI Observability capabilities to Python applications. With just a few lines of code you can prototype Retrieval‑Augmented Generation (RAG) pipelines, autonomous agents, or other AI‑enhanced observability use cases without building a model stack from scratch.  

**Value**  
- **Accelerated AI enablement** – The examples bundle the necessary SDK calls, configuration, and telemetry exporters, so developers can focus on the AI logic (e.g., prompt engineering, RAG) rather than on low‑level instrumentation.  
- **Reusable patterns** – Each sample demonstrates a concrete workflow (trace‑driven context propagation, custom metrics, log enrichment) that can be copied into production services, reducing duplication and errors.  
- **Ecosystem alignment** – By leveraging Dynatrace’s AI Observability platform, the code automatically feeds enriched traces, metrics, and logs into Dynatrace dashboards, enabling root‑cause analysis, anomaly detection, and model performance monitoring out of the box.  

**Practical Adoption Path**  
1. **Read the README** – Verify the supported Python version and required Dynatrace API keys.  
2. **Run a small proof‑of‑concept** – Clone the repo, install dependencies in a virtual environment, and execute one of the sample scripts against a non‑critical service.  
3. **Instrument your own code** – Copy the relevant `instrumentation.py` snippet into your codebase, replace placeholder values (service name, model endpoint, API token), and enable the Dynatrace exporter.  
4. **Iterate and extend** – Add custom attributes, experiment with different LLM back‑ends, and validate telemetry in the Dynatrace UI.  
5. **Scale to production** – Package the instrumentation as a library or CI/CD step, enforce secret management for tokens, and configure alerting based on the AI‑generated observability signals.  

**Production Readiness**  
The project scores high on readiness: recent commits (as of 2026‑06‑23), active community engagement (85 ★, 22 forks), and a clear Python implementation make it suitable for a serious pilot. While no critical licensing or security red flags have been identified, a final review of the repository’s license (Apache 2.0) and a dependency vulnerability scan are recommended before full rollout. With these checks completed, the examples can be treated as a production‑grade starting point for integrating Dynatrace AI Observability into enterprise workloads.

### Русский

**dynatrace-oss/dynatrace-ai-agent-instrumentation-examples** — набор готовых примеров OTel‑инструментирования, позволяющих быстро добавить в приложение возможности AI‑Observability от Dynatrace без построения собственного стекa моделей. Типичный сценарий — запуск небольшого proof‑of‑concept: подключаем библиотеку к сервису, прототипируем RAG‑или агентные воркфлоу и оцениваем инструменты моделирования в реальном наблюдаемом окружении. Проект находится в высокой готовности к production: активные коммиты, 85 звёзд, 22 форка, поддержка Python и хорошая экосистема, однако перед масштабным внедрением рекомендуется проверить лицензию, безопасность и наличие активных мейнтейнеров.

### 中文

**项目价值**  
`dynatrace-oss/dynatrace-ai-agent-instrumentation-examples` 为在 Dynatrace AI Observability 环境中快速加入 AI 能力提供了一套开箱即用的 OpenTelemetry（OTel）示例代码。通过这些示例，开发者无需从零搭建模型堆栈，即可原型化 RAG（检索增强生成）或智能代理工作流，快速评估不同模型、向量库和提示工程的效果，从而大幅缩短 AI 功能的实验周期。

**典型接入方式**  
1. **克隆仓库并阅读 README**：确认示例所依赖的 Python 版本、Dynatrace 环境变量及 OTel SDK。  
2. **创建小型 PoC**：在本地或 CI 环境中运行 `example_*` 脚本，先完成模型调用（如 OpenAI、Anthropic）和向量检索的基本链路。  
3. **接入 Dynatrace AI Observability**：在代码中使用 Dynatrace 提供的 `dt-otlp` 导出器，将链路、指标、日志以及 AI 推理元数据（prompt、response、token 计数等）统一上报到 Dynatrace。  
4. **逐步扩展**：在 PoC 验证后，可把示例代码迁入业务微服务或 Lambda 函数，结合现有的 OpenTelemetry 自动注入方案，实现全链路可观测。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑23，星标 85、Fork 22，社区活跃，代码基于 Python 并遵循 OTel 标准。  
- **成熟度**：示例已覆盖常见的模型调用、向量检索、提示工程以及 Dynatrace 元数据注入，具备直接在生产环境中做“即插即用”实验的条件。  
- **风险**：目前未发现重大元数据泄露风险，但仍需对许可证（Apache‑2.0）和依赖库的安全审计进行最终确认。  

综合来看，该项目具备 **高** 的生产候选级别（OSS‑ready），适合作为 **AI 功能原型**、**RAG/Agent 工作流** 的快速起点，并可在确认安全合规后平滑迁移至正式业务环境。

## 🧭 Practical evaluation

**Value:** dynatrace-oss/dynatrace-ai-agent-instrumentation-examples helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 85 GitHub stars
- 22 forks
- updated 2026-06-23
- primary language: Python
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 41/100 |
| topics | 100/100 |
| outlook | 55/100 |
| quality | 58/100 |
| recency | 40/100 |
| adoption | 39/100 |
| production | 56/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/dynatrace-oss/dynatrace-ai-agent-instrumentation-examples) · [← Back to AI/ML](./README.md)</sub>
