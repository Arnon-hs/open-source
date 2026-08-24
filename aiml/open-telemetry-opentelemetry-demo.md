# open-telemetry/opentelemetry-demo

[![Stars](https://img.shields.io/github/stars/open-telemetry/opentelemetry-demo?style=flat-square&color=yellow)](https://github.com/open-telemetry/opentelemetry-demo/stargazers) [![Forks](https://img.shields.io/github/forks/open-telemetry/opentelemetry-demo?style=flat-square&color=blue)](https://github.com/open-telemetry/opentelemetry-demo/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> This repository contains the OpenTelemetry Astronomy Shop, a microservice-based distributed system intended to illustrate the implementation of OpenTelemetry in a near real-world environment.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.2k |
| 🍴 **Forks** | 6.7k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`demo` `jaeger` `opentelemetry` `opentelemetry-collector` `opentelemetry-dotnet` `opentelemetry-erlang` `opentelemetry-go` `opentelemetry-java-agent` `opentelemetry-javascript` `opentelemetry-python` `opentelemetry-rust` `prometheus`

## 🎯 Categories

AI/ML · Observability

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The OpenTelemetry Astronomy Shop is a micro‑service‑based demo system that showcases how to instrument a realistic, distributed application with OpenTelemetry. Written in TypeScript, it provides ready‑made services, tracing, metrics, and logs that can be used as a reference implementation or a sandbox for experimenting with observability and AI‑enhanced workflows.

**Value**  
- **Hands‑on observability**: Gives developers a concrete, end‑to‑end example of OpenTelemetry best practices, saving the time needed to build a testbed from scratch.  
- **AI‑ready foundation**: The demo’s modular design lets you attach LLM‑driven features (e.g., RAG, agent orchestration) on top of the existing services, accelerating prototyping of AI‑augmented use cases.  
- **Community credibility**: With >3 k stars, thousands of forks, and active maintenance, the project benefits from a vibrant ecosystem and plenty of community‑contributed extensions.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the Docker‑Compose setup, and verify that traces, metrics, and logs appear in your preferred backend (Jaeger, Prometheus, etc.).  
2. **Instrument Your Services** – Follow the demo’s README to replicate its OpenTelemetry SDK configuration in your own micro‑services, swapping out the sample business logic for your code.  
3. **Add AI Layers** – Introduce LLM calls or RAG pipelines into the demo’s “shop” services, using the existing telemetry to monitor latency, error rates, and token usage.  
4. **Scale & Harden** – Replace the demo’s in‑memory stores with production databases, enable TLS, and configure production‑grade exporters (OTLP, Cloud‑specific agents).

**Production Readiness**  
- **Maturity**: Recent commits (as of 2026‑06‑24), extensive community adoption, and a solid TypeScript codebase indicate a stable foundation.  
- **Observability**: Full OpenTelemetry support (traces, metrics, logs) is already baked in, making monitoring and debugging production deployments straightforward.  
- **Risk Considerations**: No major licensing or metadata issues have been identified, but a final security audit and verification of active maintainers are recommended before a large‑scale rollout.  

Overall, the project is a high‑readiness OSS candidate for teams looking to prototype AI‑enhanced services while leveraging proven OpenTelemetry instrumentation.

### Русский

OpenTelemetry Demo – это готовый микросервисный стенд «Astronomy Shop», демонстрирующий практическую интеграцию OpenTelemetry в распределённой системе; он позволяет быстро прототипировать AI‑фичи, RAG‑или агентные воркфлоу и оценить инструменты моделирования без построения инфраструктуры с нуля. Для внедрения рекомендуется начать с небольшого proof‑of‑concept, следуя README, после чего система готова к масштабированию в продакшн благодаря активному развитию, большому сообществу (3159 звёзд, 6707 форков) и современной TypeScript‑базе. Несмотря на отсутствие критических рисков, окончательная проверка лицензии и безопасности всё же требуется.

### 中文

**项目价值**  
OpenTelemetry Demo（`open-telemetry/opentelemetry-demo`）提供了一个完整的微服务示例——“Astronomy Shop”，在接近真实的业务场景中展示了 OpenTelemetry 的数据采集、追踪、指标和日志全链路可观测性。通过该项目，团队可以快速验证和演练分布式追踪、度量以及日志聚合的实现方式，省去从零搭建观察系统的时间成本，为后续在实际业务系统中引入 AI/ML 监控、RAG（检索增强生成）或智能体工作流提供可靠的观测基础设施。

**典型接入方式**  
1. **克隆仓库并运行示例**：`git clone https://github.com/open-telemetry/opentelemetry-demo && cd opentelemetry-demo`，使用 Docker Compose 启动全部微服务（`docker compose up -d`），即可得到一套已预装 OpenTelemetry SDK 的运行环境。  
2. **在自有服务中复用**：参考 `services/*/src` 目录下的 TypeScript/Node.js 示例代码，将 OpenTelemetry SDK（`@opentelemetry/sdk-node`、`@opentelemetry/instrumentation-*`）和对应的 Exporter（如 OTLP、Jaeger、Prometheus）复制到自己的项目中。  
3. **配置 Exporter**：在 `otel-collector-config.yaml` 中定义将数据发送到的后端（如 Grafana Cloud、Tempo、Prometheus），然后在自家服务的初始化代码里加载相同的 Collector 地址，实现统一的遥测上报。  
4. **验证与调优**：使用 Demo 自带的 UI（Shop UI、Jaeger、Prometheus/Grafana）检查链路、指标和日志是否完整；根据业务需求在代码层面开启/关闭特定的自动化插件（HTTP、gRPC、数据库等）。

**生产可用性**  
- **活跃度**：截至 2026‑06‑24，项目仍在持续更新，拥有 3 159+ 星、6 707+ Fork，社区贡献活跃。  
- **技术成熟度**：基于 TypeScript 的实现，使用官方推荐的 OpenTelemetry SDK 与 Collector，符合 CNCF 观测最佳实践。  
- **可扩展性**：示例采用 Docker Compose，易迁移到 Kubernetes（已有 Helm chart 示例），可在大规模微服务环境中平滑扩展。  
- **风险**：暂无重大元数据或许可证问题，但仍建议在正式投产前进行一次安全审计（依赖库漏洞扫描）并确认维护者响应速度。  

综合来看，`open-telemetry/opentelemetry-demo` 具备 **高** 的生产候选级别（OSS Candidate），适合作为 **小规模 PoC → 完整观测平台** 的起点，帮助团队在引入 AI/ML 能力前先搭建可靠的可观测性基线。

## 🧭 Practical evaluation

**Value:** open-telemetry/opentelemetry-demo helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 3159 GitHub stars
- 6707 forks
- updated 2026-06-24
- primary language: TypeScript
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 96/100 |
| stars | 74/100 |
| topics | 100/100 |
| outlook | 66/100 |
| quality | 76/100 |
| recency | 40/100 |
| adoption | 80/100 |
| production | 65/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/open-telemetry/opentelemetry-demo) · [← Back to AI/ML](./README.md)</sub>
