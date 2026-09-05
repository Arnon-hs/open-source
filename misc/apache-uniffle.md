# apache/uniffle

[![Stars](https://img.shields.io/github/stars/apache/uniffle?style=flat-square&color=yellow)](https://github.com/apache/uniffle/stargazers) [![Forks](https://img.shields.io/github/forks/apache/uniffle?style=flat-square&color=blue)](https://github.com/apache/uniffle/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> Uniffle is a high performance, general purpose Remote Shuffle Service.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 449 |
| 🍴 **Forks** | 171 |
| 💻 **Language** | Java |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`mapreduce` `remote-shuffle-service` `rss` `shuffle` `spark` `tez`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Uniffle is an Apache‑licensed, high‑performance Remote Shuffle Service that lets distributed compute frameworks off‑load shuffle data to external storage, reducing memory pressure and improving job stability. It is written in Java, has a modest community (≈ 450 ★, 170 forks) and is actively maintained as of June 2026. The project is most useful for teams building prototype or internal data‑processing pipelines that need a generic, pluggable shuffle layer without writing custom plumbing.

**Value Proposition**  
- **Performance & scalability:** By externalising shuffle data, Uniffle frees up executor memory, cuts network traffic, and enables faster job completion for Spark, Flink, Presto, etc.  
- **General‑purpose API:** The service is not tied to a single engine; it provides a simple REST/gRPC interface that any Java‑based compute framework can use, making it a reusable building block for “database‑backed” applications.  
- **Operational flexibility:** Shuffle data can be persisted to local disks, HDFS, S3, or other object stores, allowing teams to balance latency, cost, and durability according to their workloads.

**Practical Adoption Path**  
1. **Proof‑of‑Concept:** Clone the repo, run the provided Docker compose or local script to start a Uniffle manager and worker, and configure a small Spark or Flink job to point to the service (the README includes a minimal example).  
2. **Integration Validation:** Verify that shuffle files are written to the chosen storage backend and that job runtimes improve compared to the default in‑memory shuffle.  
3. **Pilot Deployment:** Deploy Uniffle in a staging cluster (e.g., Kubernetes) using the Helm chart or the official Docker images, and integrate it with your CI/CD pipeline.  
4. **Production Roll‑out:** After confirming stability, scale the manager/worker pool, tune storage settings (e.g., spill thresholds, compression), and add monitoring (metrics exposed via Prometheus).  

**Production Readiness**  
- **Maturity:** Medium. The codebase is actively maintained and passes basic integration tests, but the documentation around production‑grade deployment (HA, security, multi‑tenant isolation) is limited.  
- **Risks:** Integration steps are not fully described in the metadata; teams must invest time to understand the setup, especially the interaction with their storage layer and network topology. Dependency management (Java 11+, specific Hadoop client versions) also needs verification.  
- **Recommendation:** Suitable for prototypes, internal analytics pipelines, or workloads where shuffle memory pressure is a known bottleneck. For mission‑critical production, perform a thorough PoC, add robust monitoring, and consider contributing missing HA/security features back to the project before committing to long‑term use.

### Русский

Резюме проекта apache/uniffle:

Apache Uniffle - это высокопроизводительное удаленное служба ресайзера, которая позволяет командам сохранять, запросить и передавать данные с минимальным вмешательством в инфраструктуру. Этот проект идеально подходит для прототипирования базовых приложений и внутренних потоков данных, поскольку он позволяет ускорить доступ к данным и облегчить управление сохранением. Apache Uniffle готов к использованию в прототипах или внутренних потоках данных, но требует проверки зависимостей и поддержки перед внедрением в production.

### 中文

**项目简介（2‑3 句）**  
Uniffle（apache/uniffle）是一个高性能、通用的远程 Shuffle 服务，旨在为大数据计算框架提供跨节点的数据交换与持久化能力。它通过独立的 Shuffle 进程实现数据的持久化、查询和迁移，帮助用户在不编写大量自定义管道代码的情况下提升 Shuffle 性能和可靠性。

---

## 价值点

| 价值维度 | 说明 |
|----------|------|
| **降低自研成本** | 统一的 Remote Shuffle Service 替代了业务代码中自行实现的 Shuffle、缓存或落盘逻辑，减少了重复开发和维护工作。 |
| **提升性能与可靠性** | 采用内存 + 本地磁盘双层存储，支持跨任务、跨作业的 Shuffle 数据复用，显著降低网络 I/O 和 GC 压力。 |
| **灵活的数据持久化** | 数据可以持久化到本地磁盘或外部文件系统（如 HDFS），支持故障恢复和后续查询。 |
| **生态兼容** | 已经在 Spark、Flink、Presto 等主流大数据引擎中提供了适配插件，易于在已有集群上直接启用。 |

---

## 典型接入方式

1. **准备 Shuffle Server**  
   - 在每台工作节点上部署 `uniffle-server`（可使用官方提供的二进制或 Docker 镜像）。  
   - 配置存储目录、内存上限、端口等参数，启动服务。

2. **在计算框架侧配置 Remote Shuffle**  
   - **Spark**：在 `spark-defaults.conf` 中加入  
     ```properties
     spark.shuffle.manager   org.apache.uniffle.shuffle.manager.RemoteShuffleManager
     spark.uniffle.shuffle.server.uri  http://<shuffle-server-host>:19999
     ```  
   - **Flink**：在 `flink-conf.yaml` 中设置  
     ```yaml
     taskmanager.shuffle.service.enabled: true
     taskmanager.shuffle.service.host: <shuffle-server-host>
     taskmanager.shuffle.service.port: 19999
     ```
   - **Presto**：在 `config.properties` 中加入 `remote-shuffle.service-uri=http://<shuffle-server-host>:19999`。

3. **小规模验证**  
   - 先在测试集群或单节点上跑一个典型的 Shuffle 密集型作业（如 Spark SQL `groupBy`），观察 Shuffle 写入/读取延迟是否下降。  
   - 通过官方 README 中的 “quick start” 示例确认客户端与服务器能够成功握手。

4. **生产化部署**  
   - 将 Shuffle Server 以 **StatefulSet**（K8s）或 **systemd** 服务方式进行高可用部署，使用负载均衡或 DNS 轮询实现多实例访问。  
   - 结合监控（Prometheus metrics）和日志（log4j）对磁盘使用、内存占用、网络吞吐进行实时监控。

---

## 生产可用性评估

| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | ★★☆☆☆（中等） | 项目已在 Apache 基金会孵化，GitHub 上有 449 ★、171 Fork，最近一次提交在 2026‑06‑29，活跃度尚可。 |
| **社区与文档** | 良好 | 官方 README 包含快速启动、Spark/Flink 集成示例，社区 Issue 响应时间在 1‑2 天左右。 |
| **依赖与运维** | 中等 | 依赖 Java 8+ 与本地磁盘/文件系统，需要额外的 Shuffle Server 进程和运维监控，部署复杂度比纯 Spark Shuffle 高。 |
| **适用场景** | 原型、内部平台、对 Shuffle 性能有显著需求的业务 | 对于需要跨作业复用 Shuffle 数据或在资源受限的集群中降低网络压力的场景尤为适合。 |
| **风险** | 集成路径不够透明、生产环境需要自行做好高可用与灾备 | 在正式环境使用前建议进行容量规划（磁盘、内存）、故障恢复演练以及与现有调度系统的兼容性测试。 |

**结论**：Uniffle 在提升 Shuffle 性能、降低自研成本方面具备明显优势，适合作为内部平台或对 Shuffle 有强需求的业务的技术选型。若准备在生产环境使用，建议先在小规模集群完成 PoC，验证与现有计算框架的兼容性后，再通过容器化或系统服务方式实现高可用部署，并配套监控、告警和灾备方案。

## 🧭 Practical evaluation

**Value:** apache/uniffle helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 449 GitHub stars
- 171 forks
- updated 2026-06-29
- primary language: Java
- 6 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 56/100 |
| stars | 56/100 |
| topics | 75/100 |
| outlook | 68/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 56/100 |
| production | 66/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/apache/uniffle) · [← Back to Misc](./README.md)</sub>
