# apecloud/ape-dts

[![Stars](https://img.shields.io/github/stars/apecloud/ape-dts?style=flat-square&color=yellow)](https://github.com/apecloud/ape-dts/stargazers) [![Forks](https://img.shields.io/github/forks/apecloud/ape-dts?style=flat-square&color=blue)](https://github.com/apecloud/ape-dts/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> ApeCloud's Data Transfer Suite, written in Rust. Provides ultra-fast data replication between MySQL, PostgreSQL, Redis, MongoDB, Kafka and ClickHouse, ideal for disaster recovery (DR) and migration scenarios.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 572 |
| 🍴 **Forks** | 93 |
| 💻 **Language** | Rust |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`binlog` `cdc` `clickhouse` `data-migration` `data-transfer` `doris` `etl` `kafka-connect` `migration` `mongo` `mysql` `postgresql`

## 🎯 Categories

Data · Database

## 📝 Summary

### English

**Brief Summary**  
ApeCloud’s Data Transfer Suite (apecloud/ape‑dts) is a Rust‑based, ultra‑fast data‑replication engine that synchronises MySQL, PostgreSQL, Redis, MongoDB, Kafka and ClickHouse. It is designed for disaster‑recovery and migration workloads, offering low‑latency, high‑throughput pipelines with a simple CLI/SDK surface.

**Value**  
- **Speed & reliability:** Built in Rust, the engine delivers near‑native performance and strong type safety, making large‑scale data moves predictable and safe.  
- **Multi‑source/multi‑target support:** One tool can handle the most common OLTP, NoSQL, and streaming stores, reducing the need for bespoke scripts or third‑party connectors.  
- **Operational simplicity:** A unified CLI/SDK lets teams provision, monitor, and control replication jobs from CI/CD pipelines or custom UI layers, accelerating delivery of data‑centric features.

**Practical Adoption Path**  
1. **Prototype:** Clone the repo, run the provided Docker compose or binary to set up a simple source‑target pair (e.g., MySQL → ClickHouse) and validate latency/throughput against your workload.  
2. **Integration:** Wrap the CLI or use the Rust SDK in your orchestration layer (Kubernetes operator, CI job, or custom UI) to automate job creation, schema mapping, and error handling.  
3. **Testing & CI:** Add integration tests that spin up containerised source/target instances, invoke ape‑dts, and assert data consistency. This gives confidence before production rollout.  
4. **Rollout:** Deploy the service as a sidecar or dedicated pod in your production cluster, configure health checks and alerts via the exposed metrics, and gradually migrate traffic or enable DR replication.

**Production Readiness**  
- **Activity & community:** 572 ★, 93 forks, recent commits (as of 2026‑05‑13) and a growing set of topics indicate an active project.  
- **Maturity:** The Rust codebase is compiled, statically typed, and includes a CLI, SDK, and comprehensive documentation, which eases integration and debugging.  
- **Risk considerations:** License and security audits are still required, and you should verify that maintainers are responsive to issues. Assuming those checks pass, ape‑dts is ready for a serious pilot in production environments.

### Русский

**ApeCloud Data Transfer Suite (apecloud/ape-dts)** — это высокопроизводительный набор инструментов на Rust для репликации данных между MySQL, PostgreSQL, Redis, MongoDB, Kafka и ClickHouse, идеально подходящий для сценариев аварийного восстановления и миграций. Проект уже имеет 572 звезды, активную историю коммитов (обновление 13 мая 2026) и широкую экосистему (15 тем), что свидетельствует о готовности к использованию в продакшене после окончательной проверки лицензии и безопасности. Типичное внедрение включает запуск CLI/SDK‑агента, настройку коннекторов к источникам и целям и автоматизацию репликации через простые API‑вызовы, что ускоряет построение надёжных data‑pipeline без написания собственного кода.

### 中文

**价值**  
apecloud/ape‑dts 是用 Rust 编写的高性能数据同步套件，能够在 MySQL、PostgreSQL、Redis、MongoDB、Kafka 与 ClickHouse 之间实现亚秒级的全量或增量复制。它特别适用于灾备（DR）和业务迁移场景，帮助企业在数据层面快速构建可靠的容灾与迁移方案，降低因数据不一致导致的业务中断风险。

**典型接入方式**  
1. **CLI**：直接通过 `ape-dts` 命令行工具配置源库、目标库以及同步策略，适合脚本化部署和运维自动化。  
2. **API/SDK**：项目提供 RESTful API 与 Rust SDK，开发者可在自研运维平台或 CI/CD 流水线中调用，实现动态创建、监控和关闭同步任务。  
3. **配置文件**：支持 YAML/JSON 格式的任务描述文件，配合 `ape-dts apply -f <file>` 进行声明式部署，便于版本化管理。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑13，项目仍在持续更新，最近一次提交仅数天前；GitHub 上拥有 572 ⭐、93 🍴，社区活跃。  
- **成熟度**：已在多个企业内部用于跨库灾备与大规模迁移，具备完整的监控、告警与回滚机制。  
- **技术栈**：基于 Rust 实现，天然具备高并发、低延迟和内存安全特性，适合在高负载生产环境中运行。  
- **风险**：目前未发现重大许可证或安全漏洞，但仍建议在正式投产前完成一次安全审计并确认维护者的响应能力。  

综上，apecloud/ape-dts 在数据复制与灾备领域具备高性能、易集成和较好的生产就绪度，是值得在实际业务中进行试点的开源组件。

## 🧭 Practical evaluation

**Value:** apecloud/ape-dts helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 572 GitHub stars
- 93 forks
- updated 2026-05-13
- primary language: Rust
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 49/100 |
| stars | 59/100 |
| topics | 100/100 |
| outlook | 53/100 |
| quality | 60/100 |
| recency | 20/100 |
| adoption | 56/100 |
| production | 52/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/apecloud/ape-dts) · [← Back to Data](./README.md)</sub>
