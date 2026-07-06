# surrealdb/surrealdb

[![Stars](https://img.shields.io/github/stars/surrealdb/surrealdb?style=flat-square&color=yellow)](https://github.com/surrealdb/surrealdb/stargazers) [![Forks](https://img.shields.io/github/forks/surrealdb/surrealdb?style=flat-square&color=blue)](https://github.com/surrealdb/surrealdb/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> A scalable, distributed, collaborative, document-graph database, for the realtime web

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 32.6k |
| 🍴 **Forks** | 1.3k |
| 💻 **Language** | Rust |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-07-06 |
| 🔍 **Source** | github |

## 🏷️ Topics

`backend-as-a-service` `cloud-database` `database` `database-as-a-service` `developer-tools` `devtools` `distributed` `distributed-database` `document-database` `graph-database` `iot-database` `nosql`

## 🎯 Categories

Backend · DevTools · Data · Database

## 📝 Summary

### English

**Summary:** SurrealDB is an open-source, scalable, and collaborative document-graph database designed for the real-time web. It enables teams to reuse backend infrastructure, accelerating the development of API services and standardizing service patterns. With its strong ecosystem signals and recent activity, SurrealDB is production-ready for serious pilots.

**Value:** The value proposition of SurrealDB lies in its ability to help teams reuse service infrastructure, reducing the need to rebuild common backend pieces. This allows teams to focus on developing API services faster and standardizing service patterns, ultimately improving the efficiency and effectiveness of their backend infrastructure.

**Practical Adoption Path:** To adopt SurrealDB, teams should start with a small proof of concept and thoroughly check the README documentation. While integration with SurrealDB appears feasible, the path may not be immediately obvious, and setup costs should be validated before committing to a full-scale implementation.

**Production Readiness:** SurrealDB has a high level of production readiness, thanks to its recent activity, strong adoption, and robust ecosystem signals. With over 32,600 GitHub stars and 1,291 forks, SurrealDB has demonstrated its viability and potential for large-scale deployment. Its primary language, Rust, also suggests a high level of technical rigor and maintainability.

### Русский

SurrealDB — это масштабируемая распределённая документно‑графовая БД, написанная на Rust, которая позволяет быстро разрабатывать и запускать realtime‑API, экономя командам время за счёт повторного использования единой инфраструктуры вместо создания собственного бекенда. Для внедрения рекомендуется начать с небольшого proof‑of‑concept, следуя инструкциям в README, чтобы оценить сложность интеграции, а затем расширять использование в продакшн‑среде. По количеству звёзд, форков, активным коммитам и поддержке сообщества проект считается готовым к серьёзным пилотным запускам.

### 中文

**价值**  
SurrealDB 通过统一的文档‑图模型、内置的实时订阅和水平可扩展的分布式架构，让团队能够直接复用一套后端基础设施，而无需自行实现 API、权限、事务、实时推送等通用功能。这样可以显著缩短 API 服务的交付周期、统一服务模式，并降低运维复杂度。

**典型接入方式**  
1. **快速原型**：在本地或 CI 环境使用官方提供的 Docker 镜像（`docker run surrealdb/surrealdb:latest`），通过 HTTP / WebSocket 端点执行 SurrealQL。  
2. **语言客户端**：项目提供官方 Rust、Go、Node.js、Python、Java 等 SDK，直接在业务代码中创建 `Surreal` 实例、连接 URL（如 `ws://localhost:8000/rpc`），并使用 `SELECT/CREATE/UPDATE` 等语句进行 CRUD 与图遍历。  
3. **小范围 PoC**：在现有微服务中仅把某个聚合根（如用户资料或实时聊天）迁移到 SurrealDB，验证实时订阅、事务和分布式复制的行为后，再逐步扩大使用范围。  
4. **生产部署**：采用官方的多节点集群模式（`surreal start --bind 0.0.0.0:8000 --user root --pass <pwd> --log debug --namespace <ns> --database <db>`），配合 Kubernetes StatefulSet 或 Nomad 作业，实现自动扩容与持久化存储。

**生产可用性**  
- **活跃度**：截至 2026‑07‑06，仓库拥有 32 628 ★、1 291 Fork，最近一次提交在当日，说明社区和维护者都非常活跃。  
- **技术成熟度**：核心实现基于 Rust，具备高性能和内存安全；提供完整的事务、ACID 保证、水平分片与多副本同步。  
- **生态与文档**：官方 README、SurrealQL 手册以及多语言 SDK 示例齐全，足以支撑从 PoC 到全量上线的全链路。  
- **风险点**：元数据中未提供统一的 “一键部署” 脚本，实际集成时需要自行规划网络、认证、备份与监控方案；因此建议在正式生产前先完成小规模的概念验证（PoC），评估运维成本与故障恢复流程。  

综合来看，SurrealDB 已具备 **高** 生产就绪度，适合作为后端基础设施的统一数据层，在需要实时协作、文档‑图混合查询以及水平扩展的业务场景中快速落地。

## 🧭 Practical evaluation

**Value:** surrealdb/surrealdb helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 32628 GitHub stars
- 1291 forks
- updated 2026-07-06
- primary language: Rust
- 18 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 78/100 |
| stars | 96/100 |
| topics | 100/100 |
| outlook | 89/100 |
| quality | 96/100 |
| recency | 100/100 |
| adoption | 91/100 |
| production | 80/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/surrealdb/surrealdb) · [← Back to Backend](./README.md)</sub>
