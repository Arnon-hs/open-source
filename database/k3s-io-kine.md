# k3s-io/kine

[![Stars](https://img.shields.io/github/stars/k3s-io/kine?style=flat-square&color=yellow)](https://github.com/k3s-io/kine/stargazers) [![Forks](https://img.shields.io/github/forks/k3s-io/kine?style=flat-square&color=blue)](https://github.com/k3s-io/kine/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> Run Kubernetes on MySQL, Postgres, sqlite, not etcd.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.4k |
| 🍴 **Forks** | 304 |
| 💻 **Language** | Go |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Database · DevOps/Infra

## 📝 Summary

### English

**Summary**  
kine is a lightweight, etcd‑compatible datastore that lets you run Kubernetes (including k3s) on traditional relational databases such as MySQL, PostgreSQL, or SQLite. By swapping the default etcd backend for an existing SQL engine, teams can reuse familiar DB operations, simplify backup/restore pipelines, and reduce the operational overhead of managing a separate key‑value store.

**Value**  
- **Leverage existing DB expertise** – No need to learn etcd APIs; you can use familiar SQL tools for querying, backups, and migrations.  
- **Unified data plane** – Store Kubernetes state alongside application data, making cross‑service audits and data movement easier.  
- **Lower infrastructure cost** – In small‑to‑medium clusters you can run Kubernetes on a single database instance instead of provisioning a dedicated etcd cluster.

**Practical adoption path**  
1. **Proof‑of‑concept** – Deploy a test k3s cluster with the `--datastore-endpoint` flag pointing to a local MySQL/Postgres/SQLite instance; verify that core components (API server, controller manager, scheduler) start correctly.  
2. **Integration testing** – Run your CI pipelines against the test cluster, exercising typical workloads (CRD creation, scaling, upgrades) to ensure compatibility and performance meet expectations.  
3. **Production rollout** – Deploy the chosen SQL database with high‑availability settings (replication, backups, monitoring). Update the k3s/kube‑apiserver configuration to use the production DB endpoint, and gradually migrate workloads while keeping the old etcd cluster as a fallback until stability is confirmed.  

**Production readiness**  
Kine scores 63/100 and shows strong OSS health signals: 2.3 k stars, 300+ forks, recent commits (as of 2026‑06‑23), and active adoption in the k3s ecosystem. While the metadata around integration is sparse and a final security/license audit is still required, the project’s recent activity and community traction make it suitable for a serious pilot or production use in environments that already run MySQL/Postgres/SQLite.

### Русский

**k3s-io/kine** — это лёгкая замена etcd, позволяющая хранить состояние Kubernetes в привычных реляционных СУБД (MySQL, PostgreSQL, SQLite). Проект подходит для команд, которым нужен быстрый доступ к данным, возможность использовать уже существующую инфраструктуру баз данных и упростить миграцию/прототипирование приложений, работающих с хранилищем кластера. По метрикам активности (2352 ★, 304 fork, регулярные коммиты) и поддержке в экосистеме, kine считается готовым к серьёзным пилотам в продакшн, хотя перед внедрением следует проверить лицензию, безопасность и наличие активных мейнтейнеров.

### 中文

**项目简介**  
k3s-io/kine 是一个用 Go 编写的轻量级存储层，能够让 Kubernetes 将 etcd 替换为 MySQL、PostgreSQL、SQLite 等常见关系型数据库。它专为 k3s 设计，也可在其他 Kubernetes 环境中单独使用。

**价值**  
- **降低运维成本**：利用已有的关系型数据库，无需额外部署、维护 etcd 集群。  
- **数据统一管理**：业务数据和集群状态共享同一数据库，便于备份、迁移和审计。  
- **加速原型开发**：在本地 SQLite 或云端 MySQL/Postgres 上即可快速启动完整的 Kubernetes 环境，适合 CI/CD、测试和演示。

**典型接入方式**  
1. **在 k3s 启动参数中指定** `--datastore-endpoint`，指向目标数据库的 DSN（如 `mysql://user:pwd@tcp(host:3306)/k3s`）。  
2. **在独立部署时**，运行 `kine` 二进制或容器镜像，监听本地端口并提供 HTTP/GRPC 接口；随后在 `kube-apiserver` 的 `--etcd-servers` 参数中填入 `http://localhost:2379`（kine 默认端口）。  
3. **数据库准备**：提前在目标数据库中创建 `kine` 所需的 schema（kine 启动时会自动迁移），并确保网络、TLS 与访问权限配置妥当。

**生产可用性**  
- **活跃度**：截至 2026‑06‑23，项目仍在维护，最近一次提交在当日；拥有 2.3k+ Stars、300+ Fork，社区讨论活跃。  
- **成熟度**：已在多个生产 k3s 部署中使用，官方文档提供了 MySQL、Postgres、SQLite 的详细示例。  
- **风险**：需要自行审查许可证（Apache‑2.0）和安全审计报告；数据库的高可用与备份策略仍需由使用方自行实现。  

综合来看，kine 在 OSS 生态中具备较高的生产就绪度，适合作为 **轻量化、数据库统一** 的 Kubernetes 数据存储方案进行试点或正式上线。

## 🧭 Practical evaluation

**Value:** k3s-io/kine helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2352 GitHub stars
- 304 forks
- updated 2026-06-23
- primary language: Go

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 62/100 |
| stars | 72/100 |
| topics | 0/100 |
| outlook | 50/100 |
| quality | 56/100 |
| recency | 40/100 |
| adoption | 69/100 |
| production | 56/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/k3s-io/kine) · [← Back to Database](./README.md)</sub>
