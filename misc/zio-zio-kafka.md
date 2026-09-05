# zio/zio-kafka

[![Stars](https://img.shields.io/github/stars/zio/zio-kafka?style=flat-square&color=yellow)](https://github.com/zio/zio-kafka/stargazers) [![Forks](https://img.shields.io/github/forks/zio/zio-kafka?style=flat-square&color=blue)](https://github.com/zio/zio-kafka/network) [![Language](https://img.shields.io/badge/lang-Scala-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> A fast Kafka client for ZIO and ZIO Streams

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 366 |
| 🍴 **Forks** | 148 |
| 💻 **Language** | Scala |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*zio‑kafka* is a high‑performance, ZIO‑native Kafka client that integrates seamlessly with ZIO Streams, letting Scala developers write type‑safe, composable streaming pipelines with minimal boilerplate. With 366 ★ and recent activity (last commit 2026‑07‑06), it offers a modern alternative to the Java client for teams already using ZIO.  

**Value**  
- **Developer productivity** – By leveraging ZIO’s effect system, the library removes the need for manual thread‑management, callbacks, and error‑prone resource handling, cutting development and review cycles.  
- **Consistent tooling** – All Kafka interactions become first‑class ZIO effects, making them easy to test, mock, and compose with existing ZIO‑based services.  
- **Speed of iteration** – The client’s non‑blocking design and tight integration with ZIO Streams enable rapid prototyping of streaming workloads and faster CI feedback loops.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, run the example in the README, and connect to a local Kafka instance (e.g., via Docker).  
2. **Dependency audit** – Verify the library’s transitive dependencies align with your organization’s policy and that the Apache‑2.0 license is acceptable.  
3. **Pilot integration** – Replace a small existing Kafka consumer/producer with the ZIO‑based version in a non‑critical service; use ZIO Test to validate behavior.  
4. **Gradual rollout** – Extend the pilot to additional services, adding custom error handling, metrics, and tracing as needed.  

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (latest commit within days) and has a healthy star/fork count, but it is still best suited for internal tools, prototypes, or services where ZIO is already the core runtime.  
- **Considerations before production**:  
  * Perform a license and security scan of the library and its dependencies.  
  * Evaluate the maintainers’ activity (issue response time, release cadence) to ensure long‑term support.  
  * Conduct load testing against your production Kafka clusters to confirm throughput and latency meet SLAs.  

Overall, *zio‑kafka* can accelerate Kafka‑centric development for ZIO‑centric teams, provided a small PoC validates compatibility and the organization completes the standard security and maintenance checks before full production deployment.

### Русский

Резюме проекта zio/zio-kafka:

Проект zio/zio-kafka представляет собой быстрый клиент Kafka для ZIO и ZIO Streams, позволяющий инженерам экономить время в повседневной разработке и ревью. Этот проект может помочь ускорить разработку, автоматизировать локальные задачи инженеров и улучшить обратную связь в CI. Проект готов к эксплуатации среднего уровня, что делает его подходящим для прототипирования или внутренних потоков работы, но требует тщательного рассмотрения зависимостей и обслуживания перед выпуском в производство.

### 中文

**项目简介**  
zio‑kafka 是为 ZIO 与 ZIO Streams 打造的高性能 Kafka 客户端，提供类型安全、资源安全的生产者/消费者 API，帮助 Scala 开发者在函数式环境中更便捷地使用 Kafka。

**价值**  
- **提升开发效率**：统一的 ZIO 生态让 Kafka 操作可以像普通 ZIO 任务一样组合、重试和并发，省去手动管理线程、回调和资源的时间。  
- **加速 CI 反馈**：在测试或 CI 流水线中直接使用 ZIO‑Kafka 进行本地或容器化的 Kafka 仿真，可实现快速的端到端验证。  
- **降低运维成本**：通过 ZIO 的资源管理（`ZManaged`/`ZIO.acquireRelease`），自动处理连接、事务和关闭，减少泄漏和错误。

**典型接入方式**  
1. **依赖引入**  
   ```scala
   libraryDependencies += "dev.zio" %% "zio-kafka" % "2.2.0"
   ```
2. **创建 Kafka 环境**（在 ZIO 程序的 `ZLayer` 中提供）  
   ```scala
   val kafkaEnv = ZLayer.make[Kafka](
     ZLayer.succeed(KafkaConfig(brokers = List("localhost:9092"))),
     ZKafkaProducer.live,
     ZKafkaConsumer.live
   )
   ```
3. **在业务代码中使用**  
   ```scala
   def produce(topic: String, record: ProducerRecord[String, String]): ZIO[Kafka, Throwable, RecordMetadata] =
     ZIO.serviceWithZIO[KafkaProducer](_.produce(record).provideLayer(kafkaEnv))
   ```
4. **在 CI/本地开发中**，可配合 `testcontainers` 启动临时 Kafka 实例，验证生产者/消费者逻辑。

**生产可用性**  
- **成熟度**：GitHub ★366、Fork ★148，活跃维护至 2026‑07‑06，代码基于 Scala 2.13/3，适合作为原型或内部服务的 Kafka 接入层。  
- **风险**：仍需自行审查许可证（Apache‑2.0）以及潜在的安全依赖；在大规模生产环境使用前建议进行依赖升级、性能基准测试并加入监控（如 Kafka‑JMX、ZIO‑Metrics）。  
- **推荐策略**：先在小范围 PoC（例如单一微服务或 CI 步骤）验证功能和资源占用，再根据结果评估是否推广至全链路生产。  

总体而言，zio‑kafka 为 ZIO 项目提供了简洁且安全的 Kafka 集成方案，适合希望在函数式 Scala 环境中快速构建可靠流处理的团队。

## 🧭 Practical evaluation

**Value:** zio/zio-kafka helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 366 GitHub stars
- 148 forks
- updated 2026-07-06
- primary language: Scala

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 54/100 |
| stars | 55/100 |
| topics | 0/100 |
| outlook | 63/100 |
| quality | 60/100 |
| recency | 80/100 |
| adoption | 55/100 |
| production | 64/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/zio/zio-kafka) · [← Back to Misc](./README.md)</sub>
