# bbossgroups/bboss-elasticsearch

[![Stars](https://img.shields.io/github/stars/bbossgroups/bboss-elasticsearch?style=flat-square&color=yellow)](https://github.com/bbossgroups/bboss-elasticsearch/stargazers) [![Forks](https://img.shields.io/github/forks/bbossgroups/bboss-elasticsearch?style=flat-square&color=blue)](https://github.com/bbossgroups/bboss-elasticsearch/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> 通用高性能Elasticsearch highlevel java orm rest client 客户端，100%兼容elasticsearch 1.x,2.x,5.x,6.x,7.x,8.x，兼容spring boot 1.x,2.x,3.x,开箱即用

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 528 |
| 🍴 **Forks** | 139 |
| 💻 **Language** | Java |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bboss` `elasticsearch` `java` `orm`

## 🎯 Categories

Database

## 📝 Summary

### English

**Project Summary:**

bbossgroups/bboss-elasticsearch is an open-source, high-performance Elasticsearch ORM (Object-Relational Mapping) REST client written in Java, providing 100% compatibility with Elasticsearch versions 1.x to 8.x and Spring Boot versions 1.x to 3.x. This client helps developers streamline their workflows by automating local engineering tasks and improving CI feedback. With over 528 GitHub stars, it's a popular tool for speeding up developer workflows.

**Value:**

The primary value proposition of bbossgroups/bboss-elasticsearch lies in its ability to save developers time in their daily development and review loops. By automating local engineering tasks and improving CI feedback, this client enables developers to focus on higher-level tasks, reducing the time spent on mundane activities.

**Practical Adoption Path:**

To adopt bbossgroups/bboss-elasticsearch, developers can follow these steps:

1. Evaluate the client's compatibility with their existing Elasticsearch and Spring Boot versions.
2. Integrate the client into their project by including it as a dependency in their build file (e.g., Maven or Gradle).
3. Configure the client to connect to their Elasticsearch instance.
4. Use the client's high-level API to interact with Elasticsearch, replacing lower-level REST calls

### Русский

**bbossgroups/bboss‑elasticsearch** — это высокопроизводительный Java‑ORM/REST‑клиент для Elasticsearch, полностью совместимый с версиями 1‑8 и интегрируемый в Spring Boot (1‑3.x). Он позволяет разработчикам быстро подключать поисковый движок, автоматизировать локальные задачи и ускорять CI‑проверки, экономя время на написании собственного клиента. Проект имеет средний уровень готовности к production: достаточная популярность (528 ★, 139 forks) и свежие обновления, но перед развертыванием в продакшн следует проверить лицензию, безопасность и активность поддержки.

### 中文

**项目简介**  
bbossgroups/bboss‑elasticsearch 是一款通用、高性能的 Elasticsearch High‑Level Java ORM/REST 客户端，代码层面 100% 兼容 Elasticsearch 1.x‑8.x 以及 Spring Boot 1.x‑3.x，开箱即用，帮助开发者在 Java 项目中以面向对象的方式快速完成索引、查询、聚合等操作。

**价值**  
- **统一 API**：一次引入即可同时支持多代 Elasticsearch，避免因版本升级而频繁更换客户端。  
- **提升开发效率**：提供 ORM 风格的实体映射、自动建索引、批量写入等封装，显著减少手写 JSON 与 HTTP 请求的工作量。  
- **兼容 Spring Boot**：可直接作为 Spring Bean 注入，配合 Spring Data 风格使用，适配现有微服务架构。  

**典型接入方式**  
1. **Maven/Gradle 依赖**  
   ```xml
   <dependency>
       <groupId>com.bbossgroups</groupId>
       <artifactId>bboss-elasticsearch</artifactId>
       <version>最新版本</version>
   </dependency>
   ```  
2. **Spring Boot 配置**（application.yml）  
   ```yaml
   bboss:
     elasticsearch:
       cluster-nodes: localhost:9200
       username: elastic
       password: secret
       connect-timeout: 5000
   ```  
3. **代码使用**  
   ```java
   @Autowired
   private ElasticSearchTemplate esTemplate;

   // 保存实体
   esTemplate.save(entity);

   // 条件查询
   SearchResponse resp = esTemplate.search(new SearchQuery()
           .setQuery(QueryBuilders.termQuery("status", "ACTIVE")));
   ```  
   也可以直接使用 `ElasticSearchRestClient` 进行低层 REST 调用，满足高级自定义需求。

**生产可用性**  
- **成熟度**：已有 528+ Stars、139+ Forks，社区活跃，最近一次提交在 2026‑06‑29，代码基于 Java 实现，适配主流 Spring Boot 版本。  
- **适用场景**：非常适合内部原型、业务中台或需要快速集成 Elasticsearch 的微服务；在生产环境使用前建议：  
  1. **依赖审计**：确认所使用的 Elasticsearch 版本与客户端兼容，并锁定依赖版本防止突变。  
  2. **安全审查**：检查许可证（Apache‑2.0）以及是否引入了已知的安全漏洞。  
  3. **性能验证**：在预上线环境进行批量写入、并发查询的压测，确保满足业务 SLA。  
- **总体评估**：在完成上述检查后，可视为 **中等风险** 的生产级组件，适合对可靠性要求不极端的业务系统。

## 🧭 Practical evaluation

**Value:** bbossgroups/bboss-elasticsearch helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 528 GitHub stars
- 139 forks
- updated 2026-06-29
- primary language: Java
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 54/100 |
| stars | 58/100 |
| topics | 50/100 |
| outlook | 55/100 |
| quality | 58/100 |
| recency | 40/100 |
| adoption | 57/100 |
| production | 54/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/bbossgroups/bboss-elasticsearch) · [← Back to Database](./README.md)</sub>
