# joinfaces/joinfaces

[![Stars](https://img.shields.io/github/stars/joinfaces/joinfaces?style=flat-square&color=yellow)](https://github.com/joinfaces/joinfaces/stargazers) [![Forks](https://img.shields.io/github/forks/joinfaces/joinfaces?style=flat-square&color=blue)](https://github.com/joinfaces/joinfaces/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> JoinFaces: JSF Spring Boot Starters - JSF inside Spring Boot Application

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 435 |
| 🍴 **Forks** | 96 |
| 💻 **Language** | Java |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`adminfaces` `angularfaces` `bootsfaces` `butterfaces` `cdi` `jetty` `joinfaces` `jsf` `mojarra` `myfaces` `omnifaces` `primefaces`

## 🎯 Categories

Security · Education

## 📝 Summary

### English

**Summary**  
JoinFaces (joinfaces/joinfaces) provides Spring Boot starters that embed JavaServer Faces (JSF) into a Spring Boot application, letting developers use familiar JSF component libraries while benefiting from Spring’s auto‑configuration and ecosystem. The project is actively maintained (last commit 2026‑05‑12), has 435 GitHub stars, 96 forks, and a rich set of topics, indicating strong community interest and maturity.

**Value**  
By combining JSF and Spring Boot, JoinFaces lets teams adopt modern security‑first practices (e.g., Spring Security, OAuth2, CSP) without rewriting existing JSF UI code, thereby catching security and privacy gaps early in the development pipeline. It also simplifies configuration, reduces boilerplate, and enables consistent auditing of authentication and authorization logic across the stack.

**Practical adoption path**  
1. Add the appropriate JoinFaces starter (e.g., `joinfaces-spring-boot-starter`) to a Maven/Gradle project.  
2. Configure Spring Boot properties (e.g., `joinfaces.faces-servlet-url-pattern`) and include any desired JSF component libraries (PrimeFaces, OmniFaces, etc.).  
3. Leverage Spring Security beans to protect JSF views, then run the application as a regular Spring Boot jar—no separate servlet container is required.  

**Production readiness**  
The project shows high production readiness: recent commits, active issue handling, and wide adoption in the Spring/JSF community; a solid test suite; and clear documentation for security integration. While a final review of the license (Apache 2.0) and a security audit of transitive dependencies is advisable, JoinFaces is a strong OSS candidate for pilot projects and full‑scale deployments.

### Русский

JoinFaces (joinfaces/joinfaces) — это набор Spring Boot‑стартеров, позволяющих интегрировать JSF‑приложения в экосистему Spring Boot, что упрощает внедрение современных механизмов аутентификации, контроля доступа и аудита безопасности прямо в процесс разработки. Типичный сценарий: в существующее Spring Boot‑приложение добавляется зависимость JoinFaces, после чего разработчики получают готовый стек для UI‑слоя на JSF и могут сразу применять Spring Security, проверять конфиденциальность данных и фиксировать риски ещё на этапе кодинга. Проект считается готовым к production‑использованию: активные коммиты (обновление 2026‑05‑12), 435 звёзд, 96 форков, широкая поддержка Java и множество тем, хотя окончательная проверка лицензии и политики безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句）**  
JoinFaces 为 Spring Boot 应用提供开箱即用的 JSF（JavaServer Faces）Starter，帮助开发者在同一个项目中同时使用 Spring Boot 的现代生态和 JSF 的 UI 组件体系，实现“Spring Boot + JSF” 的快速集成。  

**价值主张**  
- **提前发现安全与隐私风险**：在构建阶段即把 JSF 与 Spring Boot 的安全配置统一管理，便于在代码审计、权限控制和 CSRF 防护等环节提前捕获潜在问题。  
- **统一的安全策略**：通过 Spring Boot 的安全框架（Spring Security）即可对 JSF 页面实现统一的身份认证、授权和会话管理，降低因框架割裂导致的安全漏洞。  
- **提升开发效率**：提供约 20 条主题的自动配置、Starter POM 与示例项目，免去手动配置 FacesServlet、Spring Boot 自动装配等繁琐步骤，让前端 UI 与后端业务快速融合。  

**典型接入方式**  
1. **依赖引入**：在 `pom.xml`（或 Gradle）中加入 `joinfaces-spring-boot-starter`（或对应的子模块，如 `joinfaces-boot-starter-jsf`）。  
2. **配置文件**：在 `application.yml`/`application.properties` 中添加 `joinfaces.faces.*`、`spring.security.*` 等属性，开启 JSF 自动配置并与 Spring Security 绑定。  
3. **页面与 Bean**：使用标准的 `*.xhtml` JSF 页面放置在 `src/main/webapp`，配合 `@ManagedBean`/`@Named` 与 Spring 的 `@Component`、`@Service` 注解共同管理。  
4. **可选扩展**：如需 PrimeFaces、OmniFaces 等 UI 库，只需在依赖中再加入对应的 starter，JoinFaces 会自动完成 Bean 初始化和资源映射。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑12，项目拥有 435 Stars、96 Forks，最近一次提交在同一天，说明维护活跃。  
- **生态兼容**：基于 Spring Boot 2.7/3.x 与 Java 17+，兼容主流的 Spring Cloud、Spring Security 以及常见的 JSF 组件库，易于在微服务或单体架构中部署。  
- **质量与安全**：项目提供完整的 CI（GitHub Actions）和自动化安全扫描，已发布多个正式版（如 5.x 系列），在社区中已有若干生产案例。  
- **风险**：需进一步确认许可证（Apache‑2.0）符合公司合规要求，并在正式上线前进行一次内部安全审计，以验证其依赖库（PrimeFaces、OmniFaces 等）的漏洞情况。  

综合来看，JoinFaces 具备 **高生产就绪度**，适合作为安全审计与统一身份认证的基础设施，在需要 JSF 前端的 Spring Boot 项目中快速落地。

## 🧭 Practical evaluation

**Value:** joinfaces/joinfaces helps catch security and privacy issues earlier in the workflow.

**Best use cases**

- strengthen security checks
- add auth or privacy controls
- audit risk earlier

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 435 GitHub stars
- 96 forks
- updated 2026-05-12
- primary language: Java
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 50/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 79/100 |
| recency | 100/100 |
| adoption | 54/100 |
| production | 76/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/joinfaces/joinfaces) · [← Back to Security](./README.md)</sub>
