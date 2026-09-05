# apache/openwhisk

[![Stars](https://img.shields.io/github/stars/apache/openwhisk?style=flat-square&color=yellow)](https://github.com/apache/openwhisk/stargazers) [![Forks](https://img.shields.io/github/forks/apache/openwhisk?style=flat-square&color=blue)](https://github.com/apache/openwhisk/network) [![Language](https://img.shields.io/badge/lang-Scala-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> Apache OpenWhisk is an open source serverless cloud platform

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 6.8k |
| 🍴 **Forks** | 1.2k |
| 💻 **Language** | Scala |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`apache` `cloud` `docker` `faas` `functions` `functions-as-a-service` `kubernetes` `openwhisk` `serverless` `serverless-architectures` `serverless-functions`

## 🎯 Categories

Cloud & Storage · DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
Apache OpenWhisk is an open‑source, serverless cloud platform that lets teams reuse common backend infrastructure instead of building it from scratch. It accelerates API‑service delivery, enforces standardized service patterns, and offers a rich set of integration points (API, SDK, CLI, language metadata). With strong community activity, 6.8 k ★ on GitHub and recent updates, it is ready for serious pilot deployments.

**Value**  
OpenWhisk abstracts away the operational plumbing of functions‑as‑a‑service, giving developers a consistent runtime for any language while the platform handles scaling, routing, and event handling. This lets organizations focus on business logic, cut time‑to‑market for new APIs, and maintain uniform security and observability across services.

**Practical Adoption Path**  
1. **Evaluation** – Spin up the official Docker‑compose or Kubernetes helm chart in a sandbox environment; use the CLI/SDK to deploy a few test functions in your preferred language.  
2. **Integration** – Connect existing CI/CD pipelines to the OpenWhisk API for automated function packaging and deployment; leverage the built‑in triggers (HTTP, Kafka, Cloud Events) to hook into existing data sources.  
3. **Pilot** – Migrate a low‑risk microservice or internal API to OpenWhisk, monitor latency and cost, and validate logging/monitoring integrations (Prometheus, Grafana, OpenTelemetry).  
4. **Scale‑out** – Gradually replace legacy backend pieces with serverless functions, using OpenWhisk’s namespace and package mechanisms to enforce service boundaries and governance.

**Production Readiness**  
The project shows high production readiness: active maintainers, frequent releases (last update 2026‑06‑27), a large contributor base, and wide adoption in several cloud‑native stacks. Its mature API surface, extensive documentation, and ecosystem of plugins (e.g., for Kafka, OpenAPI, and authentication) make it suitable for a production pilot, though a final review of licensing, security patches, and long‑term maintainer commitment is recommended before full‑scale rollout.

### Русский

Apache OpenWhisk — это серверлесс‑платформа с открытым кодом, позволяющая командам быстро переиспользовать готовую инфраструктуру сервисов (API, функции, обработчики событий) вместо самостоятельной разработки общих бэкенд‑компонентов. Типичный сценарий — ускоренный вывод API‑сервисов в продакшн, стандартизация паттернов взаимодействия и интеграция через удобные API/SDK/CLI. Проект считается готовым к production: активная разработка, широкое принятие, более 6 000 звёзд на GitHub и сильный экосистемный набор сигналов, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**简短介绍**  
Apache OpenWhisk 是一款开源的无服务器云平台，提供统一的函数执行、事件驱动和 API 管理能力。它帮助团队复用已有的服务基础设施，避免重复搭建常见的后端组件，从而更快交付 API 服务并统一后端模式。

**价值**  
- **复用基础设施**：通过统一的函数即服务（FaaS）运行时，团队可以直接使用平台提供的调度、日志、监控等通用能力，而无需自行实现。  
- **加速交付**：开发者只需编写业务函数并通过 API/SDK/CLI 部署，即可快速上线 API 服务，显著缩短从代码到生产的周期。  
- **标准化模式**：平台内置的语言元数据、触发器和动作模板帮助团队在不同项目之间保持一致的服务设计与运维实践。

**典型接入方式**  
1. **API/CLI**：使用 OpenWhisk 提供的 RESTful API 或 `wsk` 命令行工具创建、更新、调用 Action（函数）。  
2. **SDK**：官方支持多语言 SDK（如 Java、Node.js、Python），在代码中直接调用平台 API 完成部署和触发。  
3. **事件源集成**：通过绑定 Kafka、CloudEvents、GitHub Webhook 等触发器，实现事件驱动的函数执行。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑27，项目拥有 6,781 星、1,178 Fork，最近一次提交仅数天前，社区活跃。  
- **成熟生态**：支持多语言运行时、丰富的插件体系以及与 Kubernetes、Docker 的深度集成，已在多个企业级项目中落地。  
- **可靠性**：平台提供内置的自动扩缩容、日志/监控（Prometheus、Grafana）以及容错调度，满足高可用需求。  
- **风险提示**：仍需对许可证（Apache 2.0）合规性、第三方依赖的安全漏洞以及核心维护者的长期可用性进行最终审查。  

综上，Apache OpenWhisk 在功能完整性、社区活跃度和企业级使用案例方面具备较高的生产就绪度，是值得在内部进行试点并逐步推广的 OSS 服务器无服务器解决方案。

## 🧭 Practical evaluation

**Value:** apache/openwhisk helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 6781 GitHub stars
- 1178 forks
- updated 2026-06-27
- primary language: Scala
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 77/100 |
| stars | 82/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 86/100 |
| recency | 80/100 |
| adoption | 80/100 |
| production | 76/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/apache/openwhisk) · [← Back to Cloud--storage](./README.md)</sub>
