# apache/kyuubi

[![Stars](https://img.shields.io/github/stars/apache/kyuubi?style=flat-square&color=yellow)](https://github.com/apache/kyuubi/stargazers) [![Forks](https://img.shields.io/github/forks/apache/kyuubi?style=flat-square&color=blue)](https://github.com/apache/kyuubi/network) [![Language](https://img.shields.io/badge/lang-Scala-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Apache Kyuubi is a distributed and multi-tenant gateway to provide serverless SQL on data warehouses and lakehouses.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.3k |
| 🍴 **Forks** | 1k |
| 💻 **Language** | Scala |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`data-lake` `hacktoberfest` `hadoop` `hive` `jdbc` `kubernetes` `spark` `spark-sql` `sql` `thrift`

## 🎯 Categories

Data · DevOps/Infra

## 📝 Summary

### English

**Project Overview: Apache Kyuubi**

Apache Kyuubi is an open-source, distributed gateway that enables serverless SQL access to data warehouses and lakehouses. This project helps teams reuse existing backend infrastructure, reducing the need to rebuild common components.

**Value Proposition:**

The value proposition of Apache Kyuubi lies in its ability to facilitate the reuse of service infrastructure, allowing teams to develop and deploy API services faster. By standardizing service patterns and leveraging existing backend infrastructure, organizations can improve efficiency and reduce costs.

**Practical Adoption Path:**

To adopt Apache Kyuubi, teams should start with a small proof of concept and thoroughly review the project's README. This will help them evaluate the project's feasibility and identify potential integration points. As a high-production-readiness OSS candidate, Apache Kyuubi is suitable for serious pilots and production environments, thanks to its strong adoption, recent activity, and ecosystem signals.

**Production Readiness:**

Apache Kyuubi has demonstrated high production readiness, with recent activity, strong adoption (2348 GitHub stars and 1004 forks), and a robust ecosystem. The project's primary language is Scala, and it has 10 topics, indicating a well-maintained and versatile codebase. However, final reviews of the license, security posture,

### Русский

Резюме:

Apache Kyuubi - это распределенная и многопользовательская в_gateway, которая обеспечивает серверно-независимую SQL-обработку для хранилищ данных и озер данных. Этот проект позволяет командам повторно использовать инфраструктуру сервисов, вместо того, чтобы заново создавать общую базовую часть backend. Apache Kyuubi подходит для стандартизации шаблонов сервисов и ускорения развертывания API-сервисов. Проект имеет высокий уровень готовности к production, с сильными сигналами активности, приема и экосистемы.

### 中文

**项目简介（2‑3 句）**  
Apache Kyuubi 是一个分布式、多租户的网关，能够在数据仓库和湖仓上提供无服务器（Serverless）SQL 服务。它把底层计算资源抽象为统一的 SQL 接口，让团队无需自行搭建和维护复杂的后端执行层，即可快速对外提供查询 API。

**价值**  
- **复用基础设施**：统一的 Kyuubi 服务可被多个业务共享，避免为每个项目重复搭建 Spark、Flink 等计算集群。  
- **加速 API 上线**：开发者只需编写 SQL 或轻量的业务逻辑，即可通过统一入口对外提供数据查询服务。  
- **标准化服务模式**：统一的身份认证、资源隔离和监控实现多租户治理，提升运维效率和安全合规性。

**典型接入方式**  
1. **部署 Kyuubi Server**：在已有的 Spark/Flink 集群上以独立进程方式启动 Kyuubi（支持 Kubernetes、YARN、Standalone 等多种调度器）。  
2. **配置数据源**：在 `kyuubi.conf` 中声明 Hive、Iceberg、Delta Lake 等数据仓库的 JDBC/Thrift 连接信息。  
3. **客户端接入**：使用 JDBC、ODBC、REST 或 Thrift 客户端（如 Spark‑SQL、Presto、Superset）直接连接 Kyuubi，执行标准 SQL。  
4. **小规模 PoC**：先在测试环境部署单节点 Kyuubi，跑通 README 中的示例查询，验证兼容性后再扩展到多节点高可用集群。

**生产可用性**  
- **成熟度高**：截至 2026‑06‑29，项目活跃，拥有 2.3k+ Stars、1k+ Forks，最近一次提交仅数天前。  
- **高可用与容错**：支持多实例 HA、会话恢复、动态资源调度，已在多家大数据平台上进行实战验证。  
- **生态兼容**：兼容 Hive、Iceberg、Delta Lake、Trino 等主流湖仓，且提供完整的监控（Prometheus）和审计（日志、审计插件）能力。  
- **风险点**：仍需对许可证、长期维护者以及安全补丁策略进行最终确认，但整体已具备在生产环境进行正式试点的条件。

## 🧭 Practical evaluation

**Value:** apache/kyuubi helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2348 GitHub stars
- 1004 forks
- updated 2026-06-29
- primary language: Scala
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 75/100 |
| stars | 72/100 |
| topics | 100/100 |
| outlook | 61/100 |
| quality | 73/100 |
| recency | 40/100 |
| adoption | 73/100 |
| production | 59/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/apache/kyuubi) · [← Back to Data](./README.md)</sub>
