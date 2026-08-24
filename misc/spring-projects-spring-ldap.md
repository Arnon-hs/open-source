# spring-projects/spring-ldap

[![Stars](https://img.shields.io/github/stars/spring-projects/spring-ldap?style=flat-square&color=yellow)](https://github.com/spring-projects/spring-ldap/stargazers) [![Forks](https://img.shields.io/github/forks/spring-projects/spring-ldap?style=flat-square&color=blue)](https://github.com/spring-projects/spring-ldap/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-45%2F100-brightgreen?style=flat-square)](#)

> Spring LDAP

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 373 |
| 🍴 **Forks** | 489 |
| 💻 **Language** | Java |
| 📈 **Score** | 45/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Spring LDAP is an open‑source Java library that provides Spring‑based abstractions for interacting with LDAP directories. It simplifies common LDAP operations (search, bind, modify, authentication) while integrating seamlessly with the Spring ecosystem. With a solid community following (≈ 370 ★, 490 forks) and recent activity, it can be a handy building block for applications that need directory services.

**Value**  
- **Familiar Spring API** – developers already using Spring can work with LDAP using the same dependency‑injection, configuration, and exception‑handling patterns they know.  
- **Reduced boilerplate** – the library wraps the low‑level JNDI API, handling resource management, connection pooling, and object‑mapping, which speeds up development and reduces error‑prone code.  
- **Extensible integration** – it can be combined with Spring Security for LDAP‑based authentication, or used alongside Spring Data for hybrid data‑access layers.

**Practical Adoption Path**  
1. **Evaluate the README & Samples** – clone the repo, run the provided integration tests, and review the sample `LdapTemplate` usage to confirm it matches your directory schema and query patterns.  
2. **Add the Dependency** – include the latest Maven/Gradle artifact (`org.springframework.ldap:spring-ldap-core`) in your project.  
3. **Configure a Connection Factory** – supply LDAP URL, credentials, and optional connection‑pool settings via Spring Boot properties or a `@Configuration` class.  
4. **Prototype Core Operations** – implement a small service that performs a search or authentication against a test LDAP server; verify that `LdapTemplate` correctly maps entries to your domain objects.  
5. **Run Integration Tests** – spin up an embedded LDAP server (e.g., ApacheDS) in CI to catch regressions early.  
6. **Iterate & Harden** – add error handling, TLS/StartTLS, and connection‑pool tuning before moving the code to a staging environment.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑06‑25) and has a respectable star/fork count, indicating community trust, but the documentation is sparse on advanced deployment scenarios.  
- **Suitability**: Ideal for prototypes, internal tools, or services where LDAP is a supporting data source. For high‑throughput, mission‑critical workloads, you should perform a dedicated performance benchmark, verify TLS configuration, and ensure the library’s version aligns with your Spring Framework release.  
- **Risk Mitigation**: Conduct a manual integration review, confirm compatibility with your LDAP server version, and establish a monitoring plan for connection‑pool health and authentication failures before promoting to production.

### Русский

Spring LDAP — это открытая Java‑библиотека от Spring, позволяющая быстро подключать LDAP‑каталоги к Spring‑приложениям (аутентификация, поиск и управление пользователями). Подойдёт для прототипов и внутренних сервисов, где требуется простая интеграция с LDAP без написания собственного клиентского кода; при переходе в продакшн следует проверить совместимость зависимостей, обновляемость проекта и покрытие тестами, так как пути интеграции из метаданных неочевидны. В целом готовность к production — средняя: библиотека активно поддерживается (обновление 2026‑06‑25, 373 звёзд), но требует ручной оценки рисков и настройки перед масштабным использованием.

### 中文

**项目简介（2‑3 句）**  
Spring LDAP 是 Spring Framework 官方提供的 LDAP（轻量目录访问协议）集成库，封装了 JNDI 的底层细节，提供了基于 Spring 编程模型的 LDAP 操作 API，帮助开发者在 Spring 应用中轻松完成目录查询、增删改等常见任务。

**价值**  
- **与 Spring 生态无缝衔接**：使用 Spring 的依赖注入、事务管理和模板模式，免去繁琐的 JNDI 配置。  
- **简化代码**：提供 `LdapTemplate`、`LdapQueryBuilder` 等高级抽象，使 LDAP 操作像使用 JDBC 一样直观。  
- **可扩展性强**：支持自定义 `ContextSource`、`Authenticator`、`Mapper` 等插件，满足企业级目录服务的复杂需求。  

**典型接入方式**  
1. **引入依赖**（Maven / Gradle）  
   ```xml
   <dependency>
       <groupId>org.springframework.ldap</groupId>
       <artifactId>spring-ldap-core</artifactId>
       <version>2.5.0</version>
   </dependency>
   ```  
2. **配置 `ContextSource`**（在 `application.yml` 或 Java Config 中）  
   ```yaml
   spring:
     ldap:
       urls: ldap://ldap.example.com:389
       base: dc=example,dc=com
       username: cn=admin,dc=example,dc=com
       password: secret
   ```  
3. **使用 `LdapTemplate`** 注入并执行查询/更新  
   ```java
   @Service
   public class UserService {
       private final LdapTemplate ldapTemplate;

       public UserService(LdapTemplate ldapTemplate) {
           this.ldapTemplate = ldapTemplate;
       }

       public List<String> findAllUserDns() {
           return ldapTemplate.search(
               query().where("objectclass").is("person"),
               (Attributes attrs) -> (String) attrs.get("distinguishedName").get());
       }
   }
   ```  

**生产可用性**  
- **成熟度**：项目已有 373+ Stars、489+ Forks，且最近一次提交在 2026‑06‑25，活跃度仍然良好。  
- **适用场景**：适合内部系统、企业内部管理平台或任何需要与 LDAP / Active Directory 对接的 Spring Boot 应用。  
- **风险与注意事项**：  
  - 官方文档相对简洁，集成细节（如 TLS、分页、复杂过滤）需要自行调研和测试。  
  - 依赖 Spring Framework 5.x/6.x，升级时需检查兼容性。  
  - 在高并发生产环境下，建议自行评估连接池（如 `PoolingContextSource`）的配置以及异常恢复策略。  

总体而言，Spring LDAP 在功能完整性和 Spring 生态兼容性方面表现出色，适合作为原型或内部服务的目录访问层；在投入生产前，进行一次完整的功能、性能和安全性验证即可。

## 🧭 Practical evaluation

**Value:** spring-projects/spring-ldap may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 373 GitHub stars
- 489 forks
- updated 2026-06-25
- primary language: Java

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 67/100 |
| stars | 55/100 |
| topics | 0/100 |
| outlook | 47/100 |
| quality | 51/100 |
| recency | 40/100 |
| adoption | 58/100 |
| production | 49/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/spring-projects/spring-ldap) · [← Back to Misc](./README.md)</sub>
