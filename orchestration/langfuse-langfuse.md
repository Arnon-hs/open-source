# langfuse/langfuse

[![Stars](https://img.shields.io/github/stars/langfuse/langfuse?style=flat-square&color=yellow)](https://github.com/langfuse/langfuse/stargazers) [![Forks](https://img.shields.io/github/forks/langfuse/langfuse?style=flat-square&color=blue)](https://github.com/langfuse/langfuse/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-83%2F100-brightgreen?style=flat-square)](#)

> 🪢 Open source AI engineering platform: LLM evals, observability, metrics, prompt management, playground, datasets. Integrates with OpenTelemetry, LangChain, OpenAI SDK, LiteLLM, and more. 🍊YC W23

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 29.5k |
| 🍴 **Forks** | 3.1k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 83/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`analytics` `autogen` `evaluation` `langchain` `large-language-models` `llama-index` `llm` `llm-evaluation` `llm-observability` `llmops` `monitoring` `observability`

## 🎯 Categories

Orchestration · AI/ML · Libraries & SDKs · Data · Observability

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Langfuse is an open‑source AI‑engineering platform that centralises LLM evaluation, observability, metrics, prompt management, playgrounds and dataset handling. It plugs into the existing AI stack via OpenTelemetry, LangChain, the OpenAI SDK, LiteLLM and other tools, turning ad‑hoc prompts and utilities into repeatable, monitorable agent workflows. With a strong community (≈29 k stars) and active development, it is ready for serious pilot projects.

**Value**  
- **End‑to‑end workflow orchestration:** By capturing prompts, tool calls, and responses as first‑class signals, Langfuse lets teams build, version, and reuse multi‑agent pipelines rather than scattering code across notebooks.  
- **Observability & metrics:** Built‑in tracing, latency dashboards, cost tracking and evaluation suites give immediate insight into model performance and drift, reducing the time spent debugging.  
- **Prompt & dataset governance:** Centralised prompt libraries, versioned datasets and a playground accelerate experimentation while enforcing consistency and auditability across teams.

**Practical Adoption Path**  
1. **Integrate the SDK/CLI** into existing services (e.g., LangChain or LiteLLM‑based apps) to start emitting traces and logs.  
2. **Migrate existing prompts** to Langfuse’s prompt store, enabling version control and reuse.  
3. **Configure evaluation suites** (e.g., automated test cases, cost dashboards) to monitor new or updated agents.  
4. **Gradually expand** to multi‑agent orchestration by wiring tool‑use pipelines and memory modules through Langfuse’s API, using its UI to visualise end‑to‑end flows.  
5. **Roll out to production** once observability dashboards confirm expected latency, cost and accuracy thresholds.

**Production Readiness**  
- **Activity & community:** 29 k stars, 3 k forks, recent commits (as of 2026‑06‑22) and a vibrant TypeScript ecosystem indicate strong momentum.  
- **Ecosystem integration:** Native support for OpenTelemetry, LangChain, OpenAI SDK, LiteLLM, and CLI makes hookup straightforward in most AI stacks.  
- **Stability:** The platform is already used in YC‑backed startups and other early adopters, showing it can handle real‑world traffic and multi‑agent scenarios.  
- **Risks to verify:** Final due‑diligence on the license (MIT‑compatible), security posture (dependency scanning, supply‑chain hardening) and maintainer bandwidth is still required, but no red flags have emerged.  

Overall, Langfuse offers a production‑grade, open‑source foundation for turning isolated LLM calls into observable, repeatable agent workflows, with a clear migration path and a maturity level suitable for pilot‑to‑production deployments.

### Русский

**langfuse** — это открытая платформа для инженерии LLM, объединяющая оценку моделей, наблюдаемость, метрики, управление промптами, playground и наборы данных, с готовой интеграцией в OpenTelemetry, LangChain, OpenAI SDK, LiteLLM и прочие инструменты. Она позволяет превратить разрозненные запросы и вспомогательные сервисы в воспроизводимые агентные пайплайны — например, координировать работу нескольких агентов, добавлять инструменты в их цепочки и стандартизировать память агентов. Проект имеет высокий уровень готовности к продакшн: активные коммиты, более 29 тыс. звёзд, широкое принятие в сообществе и поддержка ключевых экосистемных компонентов.

### 中文

**项目简介**  
langfuse 是一款开源的 AI 工程平台，提供 LLM 评估、可观测性、指标、Prompt 管理、交互 Playground、数据集等完整能力，并原生集成 OpenTelemetry、LangChain、OpenAI SDK、LiteLLM 等生态组件。它帮助把零散的 Prompt 与工具组合成可复用、可监控的智能体工作流。

**价值**  
- **统一治理**：将分散的 Prompt、工具调用和模型输出统一记录、可视化，便于调试与审计。  
- **可观测性 & 指标**：自动采集调用链、延迟、错误率等 OpenTelemetry 标准指标，支持实时监控与历史分析。  
- **工作流复用**：通过 Prompt 管理和 Agent Memory 标准化，实现多 Agent、工具链的可编排、可复用流程。  
- **评估闭环**：内置 LLM evals 与数据集管理，帮助快速迭代模型与 Prompt 的质量。

**典型接入方式**  
1. **SDK / API**：在代码中引入 `@langfuse/client`（TypeScript/JavaScript）或对应的 Python SDK，直接在每一次 LLM 调用、工具调用前后埋点。  
2. **CLI**：使用 `langfuse-cli` 进行本地实验、数据导入/导出、Playground 调试等。  
3. **OpenTelemetry**：通过 OpenTelemetry Collector 将已有的 tracing/metrics 自动上报到 Langfuse，无需改动业务代码。  
4. **框架集成**：在 LangChain、LiteLLM、OpenAI SDK 等常用库的中间件层加入 Langfuse 插件，即可实现“一键可观测”。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑22，仓库拥有 29.5k 星、3.1k Fork，最近一次提交在数天前，社区活跃且 PR 合并速度快。  
- **技术成熟**：核心实现使用 TypeScript，提供完整的 API 文档、示例项目和 CI/CD 测试，已在多个 YC 项目中实战。  
- **生态兼容**：兼容 OpenTelemetry、LangChain、OpenAI、LiteLLM 等主流工具，易于在已有 AI 基础设施上叠加。  
- **风险点**：仍需审查许可证（MIT），以及长期维护者的可持续性和安全审计报告，但整体风险低，适合作为正式生产环境的监控与工作流编排层。  

综上，langfuse 具备完善的可观测性、评估与工作流编排能力，接入方式灵活，社区活跃度和技术成熟度足以支撑企业级生产使用。

## 🧭 Practical evaluation

**Value:** langfuse/langfuse helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 29540 GitHub stars
- 3074 forks
- updated 2026-06-22
- primary language: TypeScript
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 87/100 |
| stars | 95/100 |
| topics | 100/100 |
| outlook | 89/100 |
| quality | 92/100 |
| recency | 80/100 |
| adoption | 93/100 |
| production | 78/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/langfuse/langfuse) · [← Back to Orchestration](./README.md)</sub>
