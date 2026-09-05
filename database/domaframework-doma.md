# domaframework/doma

[![Stars](https://img.shields.io/github/stars/domaframework/doma?style=flat-square&color=yellow)](https://github.com/domaframework/doma/stargazers) [![Forks](https://img.shields.io/github/forks/domaframework/doma?style=flat-square&color=blue)](https://github.com/domaframework/doma/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> DAO oriented database mapping framework for Java

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 501 |
| 🍴 **Forks** | 75 |
| 💻 **Language** | Java |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`annotation-processor` `dao` `doma` `java` `jdbc` `kotlin` `no-dependencies` `sql`

## 🎯 Categories

Database

## 📝 Summary

### English

**Summary**  
Doma is a DAO‑oriented database‑mapping framework for Java that streamlines the conversion of raw data into searchable, analyzable forms and supports automated pipelines. It is well‑suited for building analytics pipelines, processing large datasets, and improving reporting workflows, especially in prototype or internal‑tool scenarios. Integration is straightforward for a small proof‑of‑concept, but the setup details are not fully exposed in the repository metadata, so a quick README review and a test module are recommended before wider adoption.  

**Value**  
- Provides type‑safe, compile‑time‑checked SQL mapping, reducing runtime errors and easing maintenance.  
- Encourages clean separation of data‑access objects (DAOs) from business logic, which speeds up development of analytics and reporting features.  

**Practical adoption path**  
1. Clone the repo and run the existing unit tests to verify the build on your Java version.  
2. Create a minimal PoC module that defines a few DAOs against a test database, following the README examples.  
3. Evaluate generated SQL, performance, and compatibility with your existing ORM or JDBC stack.  

**Production readiness**  
- **Maturity:** Medium – 501 stars, 75 forks, recent updates (June 2026) indicate active maintenance, but documentation and integration guidance are limited.  
- **Risk:** Integration steps are not fully documented; you’ll need to validate dependency compatibility and assess the effort to configure the build (e.g., annotation processing).  
- **Recommendation:** Suitable for prototypes, internal tools, or services where you can afford a short validation phase; for mission‑critical production systems, perform a deeper dependency audit and consider a fallback ORM if the integration cost proves high.

### Русский

**domaframework/doma** — это DAO‑ориентированный фреймворк для маппинга баз данных в Java, который упрощает преобразование сырых данных в удобные для поиска и анализа структуры, ускоряя создание аналитических и отчётных конвейеров. Рекомендуется начать с небольшого proof‑of‑concept, следуя README, чтобы проверить интеграцию и понять требования к зависимостям; при успешном тестировании его можно применять в прототипах и внутренних workflow‑ах. Готовность к продакшн — средняя: фреймворк стабилен и активно поддерживается (501★, 75 форков, последние коммиты 2026‑06‑26), но перед выводом в продакшн требуется оценить стоимость настройки и обеспечить надёжное сопровождение зависимостей.

### 中文

**价值**  
domaframework/doma 是面向 DAO（Data Access Object）的轻量级数据库映射框架，能够把原始的关系型数据快速映射为 Java 对象，降低手写 SQL 与对象转换的成本。它的类型安全查询、编译期检查以及对批处理、分页等常用数据库操作的内置支持，使得后端服务在构建分析、报表或数据加工流水线时更加可靠且易于维护。

**典型接入方式**  
1. **依赖引入**：在 Maven/Gradle 项目中加入 `org.seasar.doma:doma-core`（或对应的最新版本）以及对应的 JDBC 驱动。  
2. **配置数据源**：在 `application.yml`（或 Spring 配置）中声明 JDBC URL、用户名、密码等信息，或使用 Doma 自带的 `DataSourceProvider`。  
3. **定义 Entity 与 DAO**：  
   ```java
   @Entity
   public class User {
       @Id @GeneratedValue
       private Integer id;
       private String name;
       // getter / setter
   }

   @Dao
   public interface UserDao {
       @Select
       List<User> findAll();

       @Insert
       int insert(User user);
   }
   ```  
4. **启动验证**：编写一个小的单元测试或 `main` 方法，调用 DAO 方法执行一次查询/插入，确认映射和事务能够正常工作。  
5. **逐步迁移**：在已有项目中先把关键的查询或写入逻辑迁移到 Doma，保持原有代码运行，待验证无误后再全面替换。

**生产可用性**  
- **成熟度**：GitHub 近 500 星、75 次 fork，最近一次提交在 2026‑06‑26，活跃度尚可。  
- **适用场景**：非常适合内部原型、数据分析服务或中小规模的业务系统；对大型分布式事务或多租户场景需要自行补充事务管理和监控。  
- **准备度**：**中等**。在生产环境使用前建议：  
  1. 完成依赖版本锁定（尤其是 Doma 与 JDBC 驱动的兼容性）。  
  2. 编写集成测试，确保 DAO 方法的编译期检查在实际数据库上能够通过。  
  3. 评估运维成本，如日志、监控、异常捕获的统一方案。  
  4. 如有需要，可结合 Spring Boot 的自动配置或自行实现统一的事务拦截器，以满足企业级可靠性要求。  

综上，domaframework/doma 能显著提升 Java 项目中数据库访问层的安全性与开发效率，接入门槛低，适合先在小范围 PoC 中验证，再根据测试结果决定是否在生产环境全面推广。

## 🧭 Practical evaluation

**Value:** domaframework/doma helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 501 GitHub stars
- 75 forks
- updated 2026-06-26
- primary language: Java
- 8 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 47/100 |
| stars | 57/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 75/100 |
| recency | 80/100 |
| adoption | 55/100 |
| production | 67/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/domaframework/doma) · [← Back to Database](./README.md)</sub>
