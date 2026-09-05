# projectnessie/nessie

[![Stars](https://img.shields.io/github/stars/projectnessie/nessie?style=flat-square&color=yellow)](https://github.com/projectnessie/nessie/stargazers) [![Forks](https://img.shields.io/github/forks/projectnessie/nessie?style=flat-square&color=blue)](https://github.com/projectnessie/nessie/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> Nessie: Transactional Catalog for Data Lakes with Git-like semantics

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.5k |
| 🍴 **Forks** | 177 |
| 💻 **Language** | Java |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`aws-lambda` `data` `git` `iceberg` `java` `spark`

## 🎯 Categories

Cloud & Storage · Data

## 📝 Summary

### English

**Summary**  
Nessie is an open‑source transactional catalog for data lakes that gives you Git‑like versioning, branching, and merging of table metadata. It lets teams treat raw data as first‑class objects that can be searched, audited, and replayed across analytics pipelines, improving data governance and reproducibility.

**Value**  
By externalizing table definitions and schema evolution into a versioned catalog, Nessie makes it easy to roll back to a known good state, compare changes between branches, and automate pipeline triggers based on catalog events. This reduces manual data‑lake housekeeping, speeds up exploratory analysis, and supports reliable reporting and CI/CD for data products.

**Adoption path**  
1. **Proof‑of‑concept** – Clone the repo, spin up the Docker compose setup, and run the provided integration tests to verify compatibility with your lake format (Iceberg, Delta, etc.).  
2. **Pilot** – Connect a small, non‑critical dataset (e.g., a staging schema) to Nessie via the Java client or REST API and replace direct Hive/Glue calls with catalog‑driven reads/writes.  
3. **Scale** – Gradually migrate additional namespaces, integrate CI pipelines to create branches for feature work, and add hooks for automated validation or lineage capture.

**Production readiness**  
Nessie scores a medium readiness level: it is mature enough for internal prototypes and controlled production workloads, backed by 1.5 k stars and active maintenance (last update 2026‑06‑24). Before full rollout, verify the integration effort (e.g., client libraries, authentication, and deployment model) and put in place monitoring for catalog latency and backup of the underlying metadata store. With those checks, Nessie can become a reliable backbone for data‑lake version control in production environments.

### Русский

**Nessie (projectnessie/nessie)** — это открытый Java‑каталог с транзакционной поддержкой и Git‑подобной семантикой, позволяющий превратить «сырой» data lake в управляемый, версионируемый набор данных, готовый к поиску, аналитике и автоматическим пайплайнам. Типичный сценарий внедрения — небольшое POC, в котором Nessie подключается к существующему хранилищу (например, S3/Delta Lake), организует версии таблиц и упрощает построение аналитических и ETL‑конвейеров; после подтверждения работоспособности можно расширять покрытие на все датасеты. Готовность к production — средняя: проект достаточно популярен (≈1,5 к звёзд) и активно поддерживается, но требует предварительной проверки интеграционных точек, зависимости и процессов обновления перед использованием в критических продакшн‑средах.

### 中文

**项目简介**  
Nessie（projectnessie/nessie）是面向数据湖的事务型目录服务，提供类似 Git 的版本控制语义，让数据的增删改都可以被追溯、回滚并安全并行操作。它把原始数据包装成可搜索、可分析的对象，帮助构建可靠的分析管道和自动化工作流。

**价值**  
- **数据治理与可追溯**：每一次元数据变更都有版本记录，支持回滚、分支和合并，极大降低误删或误改的风险。  
- **统一目录**：为分布式存储（如 Iceberg、Delta Lake、Parquet 等）提供统一的命名空间，使上层查询、报表和机器学习管道能够一致地定位数据。  
- **加速开发**：开发者可以像使用 Git 那样管理数据集，快速搭建原型并在不同分支上并行实验，提升数据团队的敏捷性。

**典型接入方式**  
1. **依赖引入**：在 Maven/Gradle 项目中加入 `org.projectnessie:nessie-client`（或对应的 SDK）。  
2. **配置连接**：在 `application.yml`（或等价配置文件）中指定 Nessie 服务的 URL、认证方式（Token/Basic）以及使用的仓库（repository）名称。  
3. **初始化仓库**：使用 Nessie CLI 或 API 创建仓库（`nessie create-repo`），并在首次写入时创建根分支（如 `main`）。  
4. **在业务代码中使用**：通过 Nessie 客户端获取 `Reference`（分支/标签），随后在 Iceberg/Delta Lake 表创建或查询时将 `catalog` 参数指向 Nessie，使表的元数据自动写入目录服务。  
5. **小规模 PoC**：先在本地或单节点 Docker 容器中跑一个 Nessie 实例，跑通 “创建分支 → 写入表 → 回滚” 的完整流程，确认与现有数据湖（如 Hive/Presto）兼容后再迁移到生产环境。

**生产可用性**  
- **成熟度**：GitHub ★1470，活跃维护（截至 2026‑06‑24），社区贡献较多，适合作为内部原型或中等规模生产系统的元数据层。  
- **准备度**：中等。功能已相对完整，但仍需自行评估以下方面后方可上线：  
  - **高可用部署**：官方提供基于 Kubernetes 的 Helm chart，可实现多副本、持久化存储和滚动升级。  
  - **安全与审计**：集成企业 SSO/OIDC 或 Token 机制，开启审计日志以满足合规要求。  
  - **运维成本**：依赖 Java 运行时和后端数据库（如 PostgreSQL），需要监控 JVM、数据库连接池以及对象存储的健康状态。  
- **适用场景**：原型开发、内部数据治理、跨团队协作的分析管道、需要版本化数据目录的机器学习实验平台。对于极高并发、超大规模数据湖的全局元数据服务，仍建议在正式投产前进行压测和灾备演练。  

综上，Nessie 为数据湖提供了 Git‑like 的事务目录，能够显著提升数据治理与开发效率；典型接入方式是通过 Maven/Gradle 引入客户端并在配置文件中指定服务地址；在做好高可用、权限与监控配置后，可在内部生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** projectnessie/nessie helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1470 GitHub stars
- 177 forks
- updated 2026-06-24
- primary language: Java
- 6 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 56/100 |
| stars | 67/100 |
| topics | 75/100 |
| outlook | 70/100 |
| quality | 75/100 |
| recency | 80/100 |
| adoption | 64/100 |
| production | 68/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/projectnessie/nessie) · [← Back to Cloud--storage](./README.md)</sub>
