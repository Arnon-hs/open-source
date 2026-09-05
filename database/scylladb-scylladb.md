# scylladb/scylladb

[![Stars](https://img.shields.io/github/stars/scylladb/scylladb?style=flat-square&color=yellow)](https://github.com/scylladb/scylladb/stargazers) [![Forks](https://img.shields.io/github/forks/scylladb/scylladb?style=flat-square&color=blue)](https://github.com/scylladb/scylladb/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> NoSQL data store using the Seastar framework, compatible with Apache Cassandra and Amazon DynamoDB

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 15.6k |
| 🍴 **Forks** | 1.5k |
| 💻 **Language** | C++ |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`c-plus-plus` `cassandra` `cpp` `database` `nosql` `scylla` `seastar`

## 🎯 Categories

Database

## 📝 Summary

### English

**Brief Summary**  
ScyllaDB is a high‑performance, open‑source NoSQL data store built on the Seastar asynchronous framework. It offers drop‑in compatibility with Apache Cassandra and Amazon DynamoDB, delivering lower latency and higher throughput for large‑scale analytics and real‑time pipelines. With over 15 k stars, active maintenance, and a strong community, it is ready for serious pilot projects.

**Value**  
ScyllaDB turns raw, high‑velocity data into a searchable, queryable store that can feed analytics dashboards, machine‑learning pipelines, and automated reporting workflows. Its Cassandra‑compatible query language lets teams reuse existing tools while gaining the performance benefits of a native C++ engine.

**Practical Adoption Path**  

1. **Proof‑of‑Concept (PoC)** – Clone the repo, follow the README to spin up a single‑node cluster (Docker or native package). Load a representative dataset and run a few CQL queries to validate latency and throughput against your current store.  
2. **Integration Checklist** – Verify driver compatibility (Cassandra drivers for Java, Python, Go, etc.), confirm data model mapping, and test backup/restore procedures.  
3. **Scaling Test** – Add nodes to a multi‑node cluster, benchmark replication and fault‑tolerance, and evaluate operational tooling (monitoring, metrics, Scylla Manager).  
4. **Production Rollout** – Deploy via your preferred orchestration (Kubernetes Helm chart or bare‑metal), configure automated scaling, and establish CI/CD pipelines for schema migrations.

**Production Readiness**  
ScyllaDB scores high on production readiness: recent commits (as of 2026‑07‑02), a large and active community, extensive documentation, and proven adoption in large‑scale enterprises. The main risk is the integration effort—its setup and tuning can be non‑trivial, so allocate time for environment validation and performance tuning before committing to a full migration.

### Русский

ScyllaDB — это высокопроизводительная NoSQL‑база, построенная на асинхронном фреймворке Seastar и совместимая с API Apache Cassandra и Amazon DynamoDB. Она позволяет быстро преобразовывать сырые данные в индексируемые наборы для аналитических и автоматизированных пайплайнов, что делает её идеальной для построения аналитических конвейеров, обработки больших датасетов и улучшения процессов отчётности. По показателям активности (15630 звёзд, 1506 форков, свежие коммиты) и поддержке сообщества проект готов к пилотному запуску в продакшн, однако интеграцию стоит начать с небольшого proof‑of‑concept и проверить детали установки в README.

### 中文

**项目简介**  
ScyllaDB 是基于 Seastar 框架构建的高性能 NoSQL 数据库，兼容 Apache Cassandra 和 Amazon DynamoDB 接口，能够在毫秒级延迟下处理 TB 级别的数据。

**价值**  
- **极致性能**：利用 C++ 与 Seastar 的无锁、事件驱动模型，实现单节点每秒上百万写入、低延迟查询，显著提升分析、报表和实时流水线的吞吐。  
- **兼容生态**：直接使用 Cassandra 的 CQL、驱动和工具链，无需改写现有代码，即可在更高效的底层上运行。  
- **弹性扩展**：水平扩容无缝，自动分片与复制，适配大规模数据湖与机器学习特征库。

**典型接入方式**  
1. **概念验证（PoC）**：在本地或单节点云实例上通过官方 Docker 镜像或二进制包快速启动，使用已有的 Cassandra 客户端（Java、Python、Go 等）连接并执行 CQL。  
2. **CI/CD 集成**：在 CI 流水线中加入 `scylladb/scylladb` 的 Docker 镜像，跑单元/集成测试，验证查询延迟与写入吞吐是否满足 SLA。  
3. **生产部署**：使用官方提供的 Ansible/Kubernetes Helm chart 将集群部署到裸机或云 VM，结合 Prometheus + Grafana 监控节点指标（CPU、IO、网络）以及 Scylla‑Manager 进行自动化运维。  

**生产可用性**  
- **成熟度**：GitHub ★15.6k、Fork 1.5k，最近一次提交为 2026‑07‑02，活跃的社区和商业版支持表明项目已进入稳态。  
- **可靠性**：具备自动故障转移、强一致性（Quorum）与可调一致性等级，已在金融、广告、IoT 等高并发场景中大规模使用。  
- **可评估性**：虽然元数据未提供完整的接入指南，但官方 README、文档站点与社区 Slack/Discord 能快速帮助完成环境搭建与调优。  

**结论**：ScyllaDB 具备高吞吐、低延迟的技术优势，兼容现有 Cassandra 生态，适合作为实时分析、数据管道和报表系统的后端存储。建议先在小规模集群上完成 PoC，验证性能与运维成本后，再逐步推广至生产环境。

## 🧭 Practical evaluation

**Value:** scylladb/scylladb helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 15630 GitHub stars
- 1506 forks
- updated 2026-07-02
- primary language: C++
- 7 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 79/100 |
| stars | 89/100 |
| topics | 88/100 |
| outlook | 80/100 |
| quality | 87/100 |
| recency | 80/100 |
| adoption | 87/100 |
| production | 72/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/scylladb/scylladb) · [← Back to Database](./README.md)</sub>
