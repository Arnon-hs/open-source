# redisson/redisson

[![Stars](https://img.shields.io/github/stars/redisson/redisson?style=flat-square&color=yellow)](https://github.com/redisson/redisson/stargazers) [![Forks](https://img.shields.io/github/forks/redisson/redisson?style=flat-square&color=blue)](https://github.com/redisson/redisson/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-79%2F100-brightgreen?style=flat-square)](#)

> Redisson - Valkey & Redis Java client. Real-Time Data Platform. Sync/Async/RxJava/Reactive API. Over 50 Valkey and Redis based Java objects and services: Set, Multimap, SortedSet, Map, List, Queue, Deque, Semaphore, Lock, AtomicLong, Map Reduce, Bloom filter, Spring, Tomcat, Scheduler, JCache API, Hibernate, RPC, local cache..

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 24.3k |
| 🍴 **Forks** | 5.5k |
| 💻 **Language** | Java |
| 📈 **Score** | 79/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cache` `distributed` `distributed-locks` `executor` `hibernate` `java` `json` `lock` `map` `micronaut` `quarkus` `queue`

## 🎯 Categories

Automation · Database

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Redisson is a high‑performance Java client for Valkey and Redis that offers synchronous, asynchronous, RxJava, and reactive APIs, together with more than 50 ready‑to‑use distributed data structures and services (e.g., maps, queues, locks, Bloom filters, and Spring/Hibernate integrations). It abstracts the low‑level Redis protocol, letting developers replace repetitive manual data‑handling code with declarative, fault‑tolerant constructs. The library is actively maintained, widely adopted, and packaged for easy inclusion in any Java‑based stack.

**Value**  
- **Productivity boost** – By providing drop‑in distributed equivalents of common Java collections and concurrency primitives, Redisson eliminates boiler‑plate code for serialization, connection handling, and cluster coordination.  
- **Unified API surface** – A single client supports sync, async, and reactive programming models, allowing teams to evolve their architecture without swapping libraries.  
- **Ecosystem integration** – Built‑in adapters for Spring, JCache, Hibernate, Tomcat, and RPC frameworks make it straightforward to embed Redisson in existing enterprise applications.  

**Practical Adoption Path**  
1. **Evaluation** – Add the Maven/Gradle dependency and run the provided unit‑test suite against a local or cloud‑hosted Redis/Valkey instance.  
2. **Prototype** – Replace a critical Java collection (e.g., `ConcurrentMap`) with its Redisson counterpart (`RMap`) to validate latency, serialization, and failover behavior.  
3. **Integration** – Leverage Spring Boot autoconfiguration or the Redisson Spring Cache manager to wire the client into the application context; configure clustering, TLS, and retry policies via `redisson.yaml`.  
4. **Scale‑out** – Enable additional services (distributed locks, semaphores, Bloom filters) as needed, and optionally enable the local‑cache or near‑cache layer for read‑heavy workloads.  

**Production Readiness**  
- **Activity & Community** – Over 24 k stars, 5.5 k forks, frequent commits (last update 2026‑05‑12) and a large contributor base indicate a healthy, actively maintained project.  
- **Maturity** – The library has been used in many high‑traffic production systems; its extensive test coverage and compatibility with Redis/Valkey 6.x‑7.x reinforce stability.  
- **Risk Profile** – No major licensing or security red flags have been identified, though a final review of the Apache‑2.0 license compliance and any disclosed CVEs is recommended.  

Overall, Redisson offers a robust, feature‑rich client that can be adopted incrementally and is ready for mission‑critical deployments.

### Русский

Redisson (redisson/redisson) — это высокопроизводительный Java‑клиент для Valkey/Redis, предоставляющий более 50 готовых распределённых структур данных и сервисов (Map, Set, Queue, Lock, Bloom filter и др.) с синхронным, асинхронным, RxJava и реактивным API, а также интеграцию со Spring, Hibernate, JCache и другими фреймворками. Типичный сценарий внедрения — замена ручных, небезопасных операций синхронизации и кэширования на надёжные распределённые объекты, автоматизация фоновых задач и построение реактивных потоков данных без написания собственного кода распределения. Проект имеет высокую готовность к продакшену: активные коммиты, более 24 тыс. звёзд, широкое сообщество и поддержка, что делает его надёжным выбором для критичных бизнес‑приложений.

### 中文

**项目简介（2‑3 句）**  
Redisson 是面向 Valkey 与 Redis 的 Java 客户端，提供同步、异步、RxJava 与响应式 API，并实现了 50 多种基于 Redis 的高级数据结构与服务（如分布式锁、队列、布隆过滤器、Map‑Reduce、Spring / Tomcat 集成、JCache、Hibernate、RPC、本地缓存等），帮助开发者在 Java 应用中轻松构建实时数据平台。

**价值**  
- **消除重复手工操作**：通过丰富的分布式集合、锁、信号量等对象，业务逻辑可以直接使用高层 API 替代自行实现的 Redis 脚本或命令，显著降低代码量和出错风险。  
- **统一的编程模型**：同步、异步、响应式风格统一封装，开发者可以根据业务需求自由切换，提升系统的可维护性与扩展性。  
- **生态兼容**：原生支持 Spring、Spring Boot、Tomcat、Hibernate、JCache 等主流框架，便于在现有微服务或传统应用中快速接入。

**典型接入方式**  
1. **Maven/Gradle 引入**：在项目的 `pom.xml`（或 `build.gradle`）中加入 `org.redisson:redisson` 依赖。  
2. **配置 RedissonClient**：通过 `Config` 对象指定单机、主从、哨兵或集群模式的连接信息（IP、端口、密码、SSL 等），随后创建 `RedissonClient` 实例。  
3. **获取分布式对象**：`redisson.getMap("myMap")`、`redisson.getLock("myLock")`、`redisson.getQueue("myQueue")` 等，即可直接使用对应的 Java 集合或同步/异步 API。  
4. **Spring 集成**：使用 `RedissonAutoConfiguration`（Spring Boot Starter）即可自动装配 `RedissonClient`，并在 Spring Bean 中注入使用。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑12，项目拥有 24,323 ★、5,488 Fork，最近一次提交在同日，说明社区和维护者仍在积极迭代。  
- **成熟的生态**：支持多种部署模式（单机、哨兵、集群），并提供完整的分布式锁、限流、调度器等生产级功能，已被多家大型互联网公司在高并发业务中采用。  
- **质量与安全**：项目使用 Apache 2.0 许可证，拥有完整的单元/集成测试，且社区对安全漏洞响应及时。结合其广泛的使用案例和丰富的文档，可视为 **生产级 OSS**，适合作为正式业务系统的核心缓存/分布式协作层。

## 🧭 Practical evaluation

**Value:** redisson/redisson helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 24323 GitHub stars
- 5488 forks
- updated 2026-05-12
- primary language: Java
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 93/100 |
| stars | 93/100 |
| topics | 100/100 |
| outlook | 86/100 |
| quality | 92/100 |
| recency | 80/100 |
| adoption | 93/100 |
| production | 78/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/redisson/redisson) · [← Back to Automation](./README.md)</sub>
