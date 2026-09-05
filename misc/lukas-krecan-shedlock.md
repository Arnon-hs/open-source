# lukas-krecan/ShedLock

[![Stars](https://img.shields.io/github/stars/lukas-krecan/ShedLock?style=flat-square&color=yellow)](https://github.com/lukas-krecan/ShedLock/stargazers) [![Forks](https://img.shields.io/github/forks/lukas-krecan/ShedLock?style=flat-square&color=blue)](https://github.com/lukas-krecan/ShedLock/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> Distributed lock for your scheduled tasks

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4.2k |
| 🍴 **Forks** | 566 |
| 💻 **Language** | Java |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
ShedLock is a lightweight Java library that provides a distributed lock for scheduled tasks, ensuring that a job runs only once across a cluster of instances. With over 4 k stars and active maintenance, it is a popular choice for preventing duplicate executions in micro‑service environments. It is best suited for projects where the existing README and activity align with your scheduling workflow, but the integration details need to be examined manually.

**Value**  
- **Safety for scheduled jobs:** Guarantees single execution of a task even when multiple application nodes poll the same schedule (e.g., Spring @Scheduled, Quartz, or custom executors).  
- **Simple API:** A few annotations or programmatic calls wrap the lock acquisition, keeping the codebase clean.  
- **Pluggable storage back‑ends:** Supports JDBC, MongoDB, Redis, Zookeeper, and others, letting you reuse an existing datastore as the lock coordinator.  

**Practical Adoption Path**  
1. **Assess compatibility:** Verify that your scheduler (Spring Boot, Quarkus, plain `java.util.Timer`, etc.) is listed in the README’s supported integrations.  
2. **Choose a lock store:** Pick a backend already present in your infrastructure (e.g., the same PostgreSQL used for the app) to avoid additional services.  
3. **Add the dependency:** Include the appropriate Maven/Gradle artifact (e.g., `shedlock-spring` + the chosen store module).  
4. **Instrument your jobs:** Annotate the method with `@SchedulerLock(name = "myJob", lockAtMostFor = "10m", lockAtLeastFor = "5m")` or use the programmatic API.  
5. **Run a local integration test:** Spin up two instances of the service (Docker compose) and confirm that only one instance executes the job per schedule.  
6. **Monitor & tune:** Enable logging (`shedlock` logger) and adjust lock timeouts to match the job’s expected runtime.  

**Production Readiness**  
- **Maturity:** Medium. The library is widely adopted (4 k+ stars, active commits as of May 2026) and stable for internal or prototype use.  
- **Risks:** Integration guidance is sparse in the metadata; you must verify that the chosen storage backend meets your latency and durability requirements.  
- **Recommended for:** Internal services, prototypes, or production systems where a single‑node lock is insufficient and you can afford a short validation effort. For mission‑critical workloads, perform a thorough integration test and consider fallback mechanisms (e.g., circuit breaker) before promoting to production.

### Русский

ShedLock — это Java‑библиотека, позволяющая реализовать распределённый блокировщик для плановых задач (cron, @Scheduled и т.п.) в кластерах, гарантируя, что каждый запуск будет выполнен только одним из экземпляров сервиса. Подойдёт для прототипов и внутренних сервисов, где требуется простая синхронизация без внедрения сложных оркестраторов, однако перед переходом в production следует проверить совместимость с используемыми хранилищами (DB, Redis, Zookeeper) и оценить нагрузку на инфраструктуру. Текущий статус — средняя готовность: проект активно поддерживается (обновления 2026‑05‑14, 4 k+ звёзд), но интеграционные детали требуют ручного аудита.

### 中文

**项目简介（2‑3 句）**  
ShedLock 是一个基于分布式锁的库，帮助在多实例部署的环境中确保 **Spring、Quartz、Micronaut 等框架的定时任务只会被单个实例执行**，从而避免重复执行和资源竞争。

**价值**  
- **防止任务重复**：在 Kubernetes、Docker Swarm、云服务器等水平扩展的场景下，自动为同一调度任务加锁，保证业务逻辑只跑一次。  
- **实现简单**：只需在已有的 `@Scheduled`（或对应框架）方法上加上 `@SchedulerLock` 注解，底层通过 JDBC、MongoDB、Redis、Zookeeper 等持久化介质实现锁的获取与释放。  
- **兼容性强**：支持 Java 8+，可与 Spring Boot、Spring Cloud、Micronaut、Quarkus 等主流生态无缝集成。

**典型接入方式**  
1. **引入依赖**（以 Spring Boot 为例）  
   ```xml
   <dependency>
       <groupId>net.javacrumbs.shedlock</groupId>
       <artifactId>shedlock-spring</artifactId>
       <version>5.10.0</version>
   </dependency>
   <dependency>
       <groupId>net.javacrumbs.shedlock</groupId>
       <artifactId>shedlock-provider-jdbc-template</artifactId>
       <version>5.10.0</version>
   </dependency>
   ```  
2. **配置锁存储**（以数据库为例）  
   ```properties
   spring.datasource.url=jdbc:postgresql://host/db
   spring.datasource.username=...
   spring.datasource.password=...
   ```  
   并在 `@Configuration` 中声明 `LockProvider`：  
   ```java
   @Bean
   public LockProvider lockProvider(DataSource dataSource) {
       return new JdbcTemplateLockProvider(dataSource);
   }
   ```  
3. **为任务加锁**  
   ```java
   @Scheduled(cron = "0 */5 * * * *")
   @SchedulerLock(name = "myTask", lockAtMostFor = "PT4M", lockAtLeastFor = "PT1M")
   public void myTask() {
       // 业务代码
   }
   ```  

**生产可用性**  
- **成熟度**：已有 4 k+ stars、500+ forks，社区活跃，最近一次提交在 2026‑05‑14，表明仍在维护。  
- **适用场景**：适合内部系统、原型或对任务唯一性有强需求的生产环境（如报表生成、批量同步、限流任务等）。  
- **风险与注意点**：  
  - 需要自行选择并部署锁的持久化介质（数据库、Redis、MongoDB 等），确保其高可用性。  
  - 对锁的超时（`lockAtMostFor`）和最短持有时间（`lockAtLeastFor`）要根据业务容忍度进行调优，防止因锁未及时释放导致任务“卡死”。  
  - 在极高并发或跨语言系统中，需评估锁实现的性能和一致性模型（如 Redis 的单节点 vs 集群）。  

总体而言，ShedLock 在保证分布式调度任务唯一执行方面提供了 **轻量、易集成且经过社区验证的解决方案**，只要做好存储层的可靠性和锁超时策略，就可以在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** lukas-krecan/ShedLock may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 4154 GitHub stars
- 566 forks
- updated 2026-05-14
- primary language: Java

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 69/100 |
| stars | 77/100 |
| topics | 0/100 |
| outlook | 65/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 75/100 |
| production | 65/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/lukas-krecan/ShedLock) · [← Back to Misc](./README.md)</sub>
