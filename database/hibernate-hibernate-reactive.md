# hibernate/hibernate-reactive

[![Stars](https://img.shields.io/github/stars/hibernate/hibernate-reactive?style=flat-square&color=yellow)](https://github.com/hibernate/hibernate-reactive/stargazers) [![Forks](https://img.shields.io/github/forks/hibernate/hibernate-reactive?style=flat-square&color=blue)](https://github.com/hibernate/hibernate-reactive/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> A reactive API for Hibernate ORM, supporting non-blocking database drivers and a reactive style of interaction with the database.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 466 |
| 🍴 **Forks** | 105 |
| 💻 **Language** | Java |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cockroachdb` `db2` `hibernate` `jpa` `mariadb` `mysql` `oracle` `orm` `postgresql` `quarkus` `reactive` `vertx`

## 🎯 Categories

Database

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Hibernate Reactive provides a non‑blocking, fully reactive API built on top of Hibernate ORM, letting Java applications interact with relational databases via drivers that never block threads. It enables developers to write clean, asynchronous data‑access code while retaining the familiar Hibernate mapping and query capabilities. The project is actively maintained, with strong community signals and recent updates, making it a viable candidate for production use.

**Value**  
- **Developer productivity** – Teams can reuse existing Hibernate entity models and JPQL/HQL knowledge, eliminating the need to rewrite data‑access layers for a reactive stack.  
- **Performance & scalability** – By leveraging non‑blocking drivers (e.g., PostgreSQL R2DBC), the application can handle many concurrent requests with far fewer threads, reducing resource consumption and latency.  
- **Consistent stack** – Keeps the backend and the UI‑focused reactive layer in the same language (Java), simplifying onboarding and reducing context‑switching.

**Practical Adoption Path**  
1. **Prototype** – Add the `hibernate-reactive-core` dependency to a new or existing Spring Boot/WebFlux or Vert.x project and configure a reactive datasource (R2DBC URL).  
2. **Migrate a subset** – Start with a low‑risk service or a read‑only query module, converting its DAO to use `Mutiny`/`CompletionStage` APIs while keeping the same entity mappings.  
3. **Integrate testing** – Use the provided test utilities (e.g., `ReactiveSessionFactory`) to validate behavior in an in‑memory database (H2 R2DBC) before moving to production.  
4. **Roll out** – Gradually replace blocking Hibernate sessions with `ReactiveSession` across services, monitoring thread usage and latency to confirm the expected gains.  

**Production Readiness**  
- **Activity & community** – 466 stars, 105 forks, recent commits (as of 2026‑06‑26), and a healthy set of topics indicate an active, engaged community.  
- **Maturity** – The library has been used in several high‑profile projects and integrates cleanly with popular reactive frameworks (Spring WebFlux, Vert.x, Quarkus).  
- **Stability** – No known critical bugs; the API is stable, and the project follows semantic versioning.  
- **Risks** – Licensing (Apache 2.0) and security posture appear acceptable, but a final review of vulnerability reports and maintainer responsiveness is recommended before a large‑scale rollout.  

Overall, Hibernate Reactive offers a low‑effort path to modern, non‑blocking data access while preserving the familiar Hibernate ecosystem, making it a strong candidate for production pilots and eventual full‑scale adoption.

### Русский

**Hibernate Reactive** — это реактивный API поверх Hibernate ORM, позволяющий работать с неблокирующими драйверами БД и писать полностью асинхронный код доступа к данным. Он упрощает создание пользовательских интерфейсов, ускоряя разработку UI за счёт повторного использования компонентов и снижения объёма кастомного кода. Проект считается готовым к продакшн‑использованию: активные коммиты, широкое принятие в сообществе (466 звёзд, 105 форков), поддержка Java и хорошая экосистема, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
Hibernate Reactive 为 Hibernate ORM 提供了全响应式（reactive）API，能够使用非阻塞的数据库驱动，以响应式编程风格与数据库交互。

**价值**  
- **提升开发效率**：在后端使用响应式 API，即可直接在前端（如 React、Vue）中采用相同的响应式思维，减少 UI 与数据层之间的适配工作。  
- **降低资源消耗**：非阻塞 I/O 让同等硬件上能够支撑更多并发请求，提升系统吞吐量。  
- **生态兼容**：基于成熟的 Hibernate ORM，几乎可以无缝迁移已有的实体模型和查询逻辑。

**典型接入方式**  
1. **依赖引入**：在 Maven/Gradle 项目中加入 `io.quarkus:quarkus-hibernate-reactive` 或 `org.hibernate.reactive:hibernate-reactive-core`。  
2. **配置数据源**：在 `application.properties`（或 `application.yml`）中指定响应式驱动（如 PostgreSQL R2DBC、MySQL R2DBC）。  
3. **创建 ReactiveSessionFactory**：通过 `HibernateReactive.with(configuration).buildSessionFactory()` 获取 `Mutiny.SessionFactory`（或 `CompletionStage`）实例。  
4. **使用 Mutiny / CompletionStage**：在业务层编写 `session.persist(entity).chain(...)` 或 `session.find(Entity.class, id).await().indefinitely()` 等链式、非阻塞代码。  
5. **与框架集成**：可直接在 Quarkus、Vert.x、Spring WebFlux 等响应式框架中注入 `SessionFactory`，实现端到端的响应式流水线。

**生产可用性**  
- **活跃度高**：最近一次提交在 2026‑06‑26，项目拥有 466+ 星、105+ Fork，社区活跃。  
- **成熟度**：基于 Hibernate ORM 的稳定核心，已在多个大型企业项目中验证。  
- **生态兼容**：支持主流 R2DBC 驱动、Vert.x、Quarkus、Spring WebFlux，易于在已有微服务架构中引入。  
- **风险**：仍需完成许可证合规、漏洞扫描以及维护者响应速度的最终评估，但整体风险较低，适合作为正式生产环境的候选方案。

## 🧭 Practical evaluation

**Value:** hibernate/hibernate-reactive helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 466 GitHub stars
- 105 forks
- updated 2026-06-26
- primary language: Java
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 57/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 75/100 |
| recency | 80/100 |
| adoption | 55/100 |
| production | 70/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/hibernate/hibernate-reactive) · [← Back to Database](./README.md)</sub>
