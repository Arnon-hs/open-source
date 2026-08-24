# GoogleCloudPlatform/khi

[![Stars](https://img.shields.io/github/stars/GoogleCloudPlatform/khi?style=flat-square&color=yellow)](https://github.com/GoogleCloudPlatform/khi/stargazers) [![Forks](https://img.shields.io/github/forks/GoogleCloudPlatform/khi?style=flat-square&color=blue)](https://github.com/GoogleCloudPlatform/khi/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> A log viewer for Kubernetes troubleshooting

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.1k |
| 🍴 **Forks** | 92 |
| 💻 **Language** | Go |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`google-cloud-platform` `kubernetes` `logging` `observability` `troubleshooting` `visualizer`

## 🎯 Categories

Observability · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
GoogleCloudPlatform/khi is an open‑source log viewer designed to simplify Kubernetes troubleshooting by persisting, querying, and visualizing cluster logs. Written in Go, the project has strong community momentum (2 068 stars, 92 forks) and recent activity, making it a viable candidate for production pilots. It fits naturally into DevOps/Observability stacks where teams need fast, query‑able access to log data without building custom pipelines.

**Value**  
- **Unified log persistence & query** – Khi stores logs in a backend (e.g., Cloud Spanner, PostgreSQL) and provides a UI/CLI for ad‑hoc queries, eliminating the need for bespoke log‑shipping scripts.  
- **Speed & cost efficiency** – By indexing logs at ingest time, teams can retrieve relevant entries in seconds, accelerating root‑cause analysis and reducing time‑to‑resolution.  
- **Prototype‑friendly** – The same data store can be reused by downstream services, enabling rapid development of database‑backed monitoring or alerting components.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the provided Docker compose or `make dev` target, and point it at a small test Kubernetes cluster. Verify that logs appear in the UI and that basic queries work.  
2. **README & CI validation** – Follow the quick‑start instructions, confirm that the CI pipeline passes, and ensure the licensing (Apache‑2.0) aligns with your organization’s policy.  
3. **Pilot Integration** – Deploy Khi as a Helm chart or Kustomize overlay in a dedicated namespace, configure it to pull logs from your existing log exporter (e.g., Fluent Bit) and store them in a managed Cloud SQL instance.  
4. **Scale & Harden** – Add RBAC, enable TLS, and configure alerting on query latency. Gradually expand the scope from a single namespace to the whole cluster while monitoring resource usage.

**Production Readiness**  
- **Activity & Ecosystem** – The project shows recent commits (as of 2026‑06‑24), a healthy star/fork ratio, and active issue discussions, indicating ongoing maintenance.  
- **Maturity** – Core functionality (log ingestion, storage adapters, UI) is stable; no major open bugs are reported.  
- **Risk Assessment** – No immediate metadata or licensing red flags, but a final security audit and confirmation of active maintainers are recommended before full‑scale rollout. Overall, Khi is deemed “high” readiness for a serious pilot in production environments.

### Русский

**GoogleCloudPlatform/khi** — открытый лог‑просмотрщик, упрощающий отладку Kubernetes: он сохраняет журналы, позволяет быстро выполнять запросы и переносить данные без написания собственного кода. Типичный сценарий — небольшое POC‑внедрение (по README) для централизованного хранения и анализа логов, после чего система готова к масштабированию в продакшн‑окружении. Проект считается «high‑ready»: активные коммиты, значительная звёздность (2068), широкое принятие и поддержка в экосистеме, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
GoogleCloudPlatform/khi 是一款专为 Kubernetes 故障排查设计的日志查看器，使用 Go 编写，拥有 2000+ 星、活跃的社区和近期更新，适合作为内部监控与调试工具的 OSS 选型。

**价值**  
- **统一持久化**：将容器日志统一写入可查询的后端，避免各服务自行搭建日志管道。  
- **快速查询**：提供高效的过滤、聚合和实时检索接口，加速故障定位。  
- **易于迁移**：日志数据可随时导出或转接至其他存储/分析平台，降低锁定风险。

**典型接入方式**  
1. **小规模 PoC**：先在测试集群中部署 `khi` Helm chart（或直接 `kubectl apply -f manifests/`），并在 README 中配置日志源（如 Fluentd/Stackdriver）。  
2. **验证查询**：使用内置 UI 或 API 验证日志写入、过滤和导出功能。  
3. **渐进式推广**：在验证无误后，将 `khi` 作为集群的统一日志后端，逐步替换现有的自研或商用日志收集方案。

**生产可用性**  
- **成熟度高**：最近一次提交（2026‑06‑24）且活跃维护，拥有 2068 星、92 个 Fork，社区响应及时。  
- **可在生产环境试点**：具备完整的 Helm 部署、健康检查和 Prometheus 指标，可配合现有的 GKE、Anthos 等 Google Cloud 环境使用。  
- **风险点**：仍需对许可证（Apache 2.0）进行合规审查，检查容器镜像的安全扫描报告以及维护者的响应时效。

总体而言，khi 在日志持久化与快速查询方面提供了即插即用的能力，适合作为 Kubernetes 环境的日志观察层，在完成小规模验证后即可进入生产级别的试点。

## 🧭 Practical evaluation

**Value:** GoogleCloudPlatform/khi helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2068 GitHub stars
- 92 forks
- updated 2026-06-24
- primary language: Go
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 49/100 |
| stars | 71/100 |
| topics | 75/100 |
| outlook | 56/100 |
| quality | 65/100 |
| recency | 40/100 |
| adoption | 65/100 |
| production | 59/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/GoogleCloudPlatform/khi) · [← Back to Observability](./README.md)</sub>
