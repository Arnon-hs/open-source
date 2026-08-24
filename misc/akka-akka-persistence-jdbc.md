# akka/akka-persistence-jdbc

[![Stars](https://img.shields.io/github/stars/akka/akka-persistence-jdbc?style=flat-square&color=yellow)](https://github.com/akka/akka-persistence-jdbc/stargazers) [![Forks](https://img.shields.io/github/forks/akka/akka-persistence-jdbc?style=flat-square&color=blue)](https://github.com/akka/akka-persistence-jdbc/network) [![Language](https://img.shields.io/badge/lang-Scala-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-47%2F100-brightgreen?style=flat-square)](#)

> Asynchronously writes journal and snapshot entries to configured JDBC databases so that Akka Actors can recover state

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 309 |
| 🍴 **Forks** | 134 |
| 💻 **Language** | Scala |
| 📈 **Score** | 47/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`akka-persistence` `journal` `persistence-query` `scala` `slick`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`akka-persistence-jdbc` is an Akka Persistence plugin that asynchronously stores journal and snapshot events in any JDBC‑compatible database, enabling Akka actors to recover their state after restarts. By decoupling persistence from the in‑memory runtime, it lets you build reliable, fault‑tolerant event‑sourced systems while leveraging existing relational databases.

**Value**  
- **Unified storage** – Use a single relational database (PostgreSQL, MySQL, Oracle, etc.) for both event journals and snapshots, avoiding the need for a separate event store.  
- **Scalable analytics** – Persisted events become readily queryable with standard SQL tools, making it easy to feed downstream analytics pipelines, dashboards, or automated reporting.  
- **Low‑entry barrier** – If your organization already operates JDBC databases, you can add durable Akka persistence without provisioning new infrastructure.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, follow the README to configure a small H2 or PostgreSQL instance, and instrument a simple persistent actor. Verify that events are written to the `journal` and `snapshot` tables and that recovery works after a restart.  
2. **Integration testing** – Add the library to your build (Scala 2.13/3.x), run the supplied integration tests against your target DB, and experiment with the provided `JdbcReadJournal` queries.  
3. **Pipeline hookup** – Once events are in a relational table, connect your analytics tools (e.g., Apache Spark, dbt, or BI platforms) to the same schema for reporting or downstream processing.  
4. **Production rollout** – Deploy the plugin behind a feature flag, monitor write latency and DB connection pool health, and gradually migrate existing actors to the JDBC backend.

**Production Readiness**  
- **Maturity**: 309 ★, 134 forks, recent updates (July 2026) indicate active maintenance, but the project is still classified as *medium* readiness.  
- **Strengths**: Strong community backing, clear Scala API, and support for major RDBMSs.  
- **Caveats**: The integration steps are not fully documented in the metadata; you’ll need to verify connection‑pool sizing, transaction isolation, and backup strategies for your chosen DB. Dependency management (Akka version compatibility) should be audited before a full production push.  

Overall, `akka-persistence-jdbc` is a solid choice for prototypes, internal services, or production systems that already rely on relational databases, provided you perform a small PoC and validate the operational overhead.

### Русский

**akka‑persistence‑jdbc** — это библиотека, позволяющая асинхронно сохранять журналы и снапшоты Akka‑актеров в любые JDBC‑совместимые базы данных, тем самым обеспечивая возможность восстановления их состояния и построения аналитических или автоматизированных пайплайнов на основе этих данных. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept, проверка README и базовой конфигурации, после чего интеграция в существующие Akka‑приложения для организации аналитических потоков, обработки наборов данных и улучшения отчётности. Готовность к production — средняя: проект стабилен и активно поддерживается (309★, 134 форка, последние обновления в июле 2026), но перед запуском в продакшн следует оценить зависимост‑и и потенциальные затраты на настройку.

### 中文

**项目简介（2‑3 句）**  
`akka/akka-persistence-jdbc` 为 Akka Persistence 提供基于 JDBC 的持久化实现，能够异步将 Actor 的事件日志（journal）和快照（snapshot）写入任意关系型数据库，从而保证 Actor 在重启或故障后能够完整恢复状态。

**价值**  
- **统一持久化层**：使用熟悉的关系型数据库（PostgreSQL、MySQL、SQL Server 等）即可保存事件流，免去专门的 NoSQL 或事件存储系统的运维成本。  
- **可靠的状态恢复**：借助事务和数据库的 ACID 特性，确保事件写入的原子性和持久性，提升系统的容错能力。  
- **生态兼容**：与 Akka Actor、Akka Streams、Akka Cluster 等核心模块无缝集成，适合作为微服务或事件驱动架构的底层数据层。

**典型接入方式**  
1. **添加依赖**：在 `build.sbt` 中加入对应的 JDBC 驱动和 `akka-persistence-jdbc` 依赖，例如  
   ```scala
   libraryDependencies ++= Seq(
     "com.typesafe.akka" %% "akka-persistence-jdbc" % "5.0.0",
     "org.postgresql"    %  "postgresql"          % "42.7.1"
   )
   ```
2. **配置数据库**：在 `application.conf` 中配置 `akka.persistence.jdbc`，指定 JDBC URL、用户名、密码以及方言（postgresql、mysql 等）。  
3. **声明持久化 Actor**：让业务 Actor 继承 `PersistentActor`（或 `EventSourcedBehavior`），并在 `receiveRecover` 与 `receiveCommand` 中处理事件与快照。  
4. **启动并验证**：运行应用，观察 `journal` 与 `snapshot` 表是否被创建并写入数据；可先在本地使用 SQLite 或 H2 完成 PoC，确认序列化、查询和恢复逻辑。

**生产可用性**  
- **成熟度**：项目已有 309 ⭐、134 🍴，活跃维护至 2026‑07‑06，代码基于 Scala，社区贡献较为活跃。  
- **适用场景**：适合内部原型、数据分析管道、报表系统以及对持久化一致性要求较高的企业内部服务。  
- **风险与注意事项**  
  - **集成成本**：需要自行管理数据库的 schema 迁移（journal、snapshot 表结构）以及连接池配置。  
  - **性能瓶颈**：在高并发写入场景下，受限于关系型数据库的事务开销，可能需要调优批量写入、写入线程池或使用专用的写入节点。  
  - **运维依赖**：确保数据库的备份、恢复和监控到位，否则持久化层将成为单点故障。  

总体而言，`akka-persistence-jdbc` 在 **中等** 生产就绪度（Medium）上表现良好；对原型或内部业务系统可直接投入使用，但在面向大流量、全链路容错的生产环境时，建议先进行压力测试并结合数据库的 HA/读写分离方案进行部署。

## 🧭 Practical evaluation

**Value:** akka/akka-persistence-jdbc helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 309 GitHub stars
- 134 forks
- updated 2026-07-06
- primary language: Scala
- 5 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 53/100 |
| stars | 53/100 |
| topics | 63/100 |
| outlook | 52/100 |
| quality | 58/100 |
| recency | 40/100 |
| adoption | 53/100 |
| production | 52/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/akka/akka-persistence-jdbc) · [← Back to Misc](./README.md)</sub>
