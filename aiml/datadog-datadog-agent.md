# DataDog/datadog-agent

[![Stars](https://img.shields.io/github/stars/DataDog/datadog-agent?style=flat-square&color=yellow)](https://github.com/DataDog/datadog-agent/stargazers) [![Forks](https://img.shields.io/github/forks/DataDog/datadog-agent?style=flat-square&color=blue)](https://github.com/DataDog/datadog-agent/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-75%2F100-brightgreen?style=flat-square)](#)

> Main repository for Datadog Agent

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.7k |
| 🍴 **Forks** | 1.4k |
| 💻 **Language** | Go |
| 📈 **Score** | 75/100 |
| 🗓️ **Last push** | 2026-06-25 |
| 🔍 **Source** | github |

## 🏷️ Topics

`apm-agent` `apm-instrumentation` `datadog` `distributed-tracing` `go` `logging` `metrics` `monitoring` `observability` `open-telemetry` `otel` `profiling`

## 🎯 Categories

AI/ML · Data · Observability

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The **Datadog Agent** repository houses the open‑source core of Datadog’s observability platform, written in Go and actively maintained with over 3 600 stars. It enables teams to quickly prototype AI‑enhanced monitoring, RAG, or autonomous agent workflows without building a telemetry stack from scratch. A small proof‑of‑concept can be launched by following the README and leveraging the existing integration ecosystem.

**Value**  
- **Accelerated AI enablement** – The agent already collects, processes, and ships metrics, traces, and logs, providing a rich data source that AI models can consume for anomaly detection, root‑cause analysis, or automated remediation.  
- **Low‑code entry point** – By extending the agent with custom checks or plugins, developers can prototype AI features (e.g., RAG over logs) without provisioning separate data pipelines.  
- **Strong community and ecosystem** – With 1 449 forks, frequent releases, and a broad set of integrations, the project offers proven patterns and community support for extending observability with AI.

**Practical Adoption Path**  
1. **Read the README & Quick‑Start** – Deploy the agent in a sandbox environment (Docker or a single VM) using the official installation script.  
2. **Validate data flow** – Confirm that metrics, traces, and logs are reaching a Datadog workspace or a local collector.  
3. **Add a custom check or plugin** – Use the Go SDK to emit additional signals or to invoke an AI model (e.g., a local LLM) for on‑the‑fly analysis.  
4. **Prototype the AI use case** – Build a lightweight service that consumes the agent’s output (via the Datadog API or a local queue) and returns insights, alerts, or RAG results.  
5. **Iterate & scale** – Once the proof‑of‑concept is stable, roll the extended agent out to production clusters using existing orchestration tools (Kubernetes DaemonSet, Chef, Ansible, etc.).

**Production Readiness**  
- **Maturity** – The repository shows recent activity (last update 2026‑06‑25), a high star count, and extensive fork activity, indicating a well‑tested codebase.  
- **Stability** – The core agent is battle‑tested in large‑scale Datadog deployments; adding custom plugins follows documented, versioned interfaces.  
- **Ecosystem fit** – Built‑in integrations for cloud providers, containers, and popular services simplify data ingestion, while the Go language offers strong performance and static analysis tooling.  
- **Risk considerations** – No major metadata or licensing concerns are evident, but a final security audit (dependency scanning, CVE checks) and verification of maintainers’ responsiveness are recommended before full production rollout.  

Overall, the Datadog Agent is a high‑readiness OSS component that can serve as a solid foundation for AI‑augmented observability pilots and, with proper validation, scale to production environments.

### Русский

DataDog /datadog‑agent — это основной репозиторий агента наблюдаемости Datadog, написанный на Go, с активным сообществом (3654 ★, 1449 fork) и регулярными обновлениями, что делает его готовым к использованию в production‑окружениях. Он позволяет быстро добавить возможности AI‑наблюдаемости (прототипирование AI‑фич, построение RAG‑ или агентных воркфлоу) без необходимости разрабатывать стек модели с нуля, начиная с небольшого proof‑of‑concept и проверки README. Несмотря на отсутствие серьёзных метаданных‑рисков, рекомендуется окончательно проверить лицензию, безопасность и наличие активных мейнтейнеров перед масштабным внедрением.

### 中文

**价值**  
DataDog Agent 是 Datadog 生态的核心组件，负责在服务器、容器和云环境中采集指标、日志、追踪以及安全信号。它内置了丰富的插件和集成，可直接将原始监控数据送入 Datadog 平台，帮助团队实现 **可观测性**、**异常检测** 与 **AI‑驱动的根因分析**，无需自行搭建采集、归一化和上报的完整链路。

**典型接入方式**  
1. **快速部署**：通过官方提供的单行脚本（`DD_AGENT_MAJOR_VERSION=7 DD_API_KEY=your_key bash -c "$(curl -L https://s3.amazonaws.com/dd-agent/scripts/install_script.sh)"`）在 Linux、Windows、macOS、Kubernetes、ECS 等环境一键安装。  
2. **配置插件**：在 `/etc/datadog-agent/conf.d/` 目录下添加对应的 YAML 配置文件（如 `nginx.d/conf.yaml`、`postgres.d/conf.yaml`），开启所需的监控集成。  
3. **自定义检查**：使用 Go 编写自定义检查（Custom Check）或 Python 脚本（Python Integration），将业务特有的指标、日志或安全事件注入 Datadog。  
4. **AI/ML 扩展**：利用 Datadog 的 **Watchdog**、**Anomaly Detection** 与 **RAG**（Retrieval‑Augmented Generation）功能，直接在 Agent 收集的数据上运行模型，快速原型化异常预测或智能告警。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑25，仓库拥有 3,654 ★、1,449 Fork，最近一次提交在当天，说明社区与 Datadog 官方均在持续维护。  
- **成熟生态**：支持 300+ 官方集成，覆盖数据库、消息队列、容器编排、云服务等主流技术栈，已在全球数万家企业的生产环境中运行。  
- **可靠性**：提供完整的健康检查、日志轮转、TLS 加密、自动重试与高可用模式（Agent v2 集群），符合企业级 SLA 要求。  
- **安全合规**：遵循 Apache‑2.0 许可证，官方提供安全审计报告与漏洞响应流程，适合在合规环境中使用。  

**结论**：DataDog Agent 具备高可靠性、丰富的即插即用集成以及对 AI/ML 功能的天然支持，是在现有业务上快速实现可观测性和智能运维的首选 OSS 组件。建议先在小范围（如单个节点或测试命名空间）完成部署并验证 README 中的示例配置，再逐步推广至全量生产环境。

## 🧭 Practical evaluation

**Value:** DataDog/datadog-agent helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 3654 GitHub stars
- 1449 forks
- updated 2026-06-25
- primary language: Go
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 79/100 |
| stars | 76/100 |
| topics | 100/100 |
| outlook | 89/100 |
| quality | 90/100 |
| recency | 100/100 |
| adoption | 77/100 |
| production | 80/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/DataDog/datadog-agent) · [← Back to AI/ML](./README.md)</sub>
