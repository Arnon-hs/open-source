# dromara/Sa-Token

[![Stars](https://img.shields.io/github/stars/dromara/Sa-Token?style=flat-square&color=yellow)](https://github.com/dromara/Sa-Token/stargazers) [![Forks](https://img.shields.io/github/forks/dromara/Sa-Token?style=flat-square&color=blue)](https://github.com/dromara/Sa-Token/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> ✨ 开源、免费、一站式 Java 权限认证框架，让鉴权变得简单、优雅！—— 登录认证、权限认证、分布式 Session 会话、微服务网关鉴权、SSO 单点登录、OAuth2.0 统一认证、jwt 集成、API Key 秘钥授权、API 参数签名

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 18.9k |
| 🍴 **Forks** | 2.9k |
| 💻 **Language** | Java |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-07-04 |
| 🔍 **Source** | github |

## 🏷️ Topics

`aouth2` `authorization` `java` `springcloud` `sso` `token`

## 🎯 Categories

Backend · Security

## 📝 Summary

### English

**Project Summary:**

Sa-Token is an open-source, one-stop Java framework for authentication and authorization, simplifying and streamlining complex authentication processes. It offers a range of features, including login authentication, permission authentication, distributed session management, and more. With its high production readiness and strong ecosystem signals, Sa-Token is a reliable choice for teams looking to reuse service infrastructure and accelerate API service development.

**Value Proposition:**

Sa-Token helps teams reduce development time and costs by reusing common backend infrastructure, allowing them to focus on building their core services. By providing a standardized framework for authentication and authorization, Sa-Token enables teams to ship API services faster and with greater confidence.

**Practical Adoption Path:**

To adopt Sa-Token, teams can follow these steps:

1. Evaluate Sa-Token's features and compatibility with their existing infrastructure.
2. Integrate Sa-Token into their backend services using the provided APIs, SDKs, or CLI tools.
3. Configure Sa-Token to meet their specific authentication and authorization requirements.
4. Test and deploy Sa-Token in their production environment.

**Production Readiness:**

Sa-Token has demonstrated high production readiness, with recent activity, strong adoption, and a robust ecosystem. Its recent update and large community of contributors (18,917 GitHub stars and 2,915

### Русский

Резюме проекта dromara/Sa-Token:

dromara/Sa-Token - это открытый и бесплатный Java-решение для управления правами, которое упрощает процесс аутентификации и авторизации. Этот проект позволяет командам повторно использовать уже существующую инфраструктуру, а не тратить время на создание общих элементов backend. dromara/Sa-Token готов к использованию в продакшене и имеет сильные сигналы о готовности к пилотному проекту.

### 中文

**项目简介**  
Sa‑Token（dromara/Sa-Token）是一款开源、免费的一站式 Java 权限认证框架，提供登录、权限、分布式 Session、微服务网关鉴权、SSO、OAuth2.0、JWT、API Key、参数签名等完整能力，让鉴权工作变得简单且优雅。

**价值**  
- **统一安全底座**：一次实现登录、会话、授权等核心功能，所有业务系统直接复用，避免重复造轮子。  
- **快速交付**：提供即插即用的注解、拦截器和 API，配合 SpringBoot、Spring Cloud 等生态，可在数分钟完成权限体系搭建。  
- **灵活扩展**：支持多种认证方式（密码、验证码、短信、OAuth2、JWT、API Key 等）以及分布式会话、单点登录、微服务网关鉴权，满足从单体到微服务的全链路安全需求。  

**典型接入方式**  
1. **依赖引入**：在 Maven/Gradle 中加入 `sa-token-spring-boot-starter`。  
2. **配置**：在 `application.yml`（或 `application.properties`）中打开所需模块（如 `sa-token.jwt`, `sa-token.sso`），并配置 token 有效期、存储方式（Redis、内存、数据库）等。  
3. **注解使用**：在 Controller、Service 方法上使用 `@SaCheckLogin`、`@SaCheckPermission`、`@SaCheckRole` 等注解进行权限校验，或在代码中调用 `StpUtil.login(id)`、`StpUtil.checkPermission("xxx")` 完成手动控制。  
4. **微服务/网关**：在 Spring Cloud Gateway、Zuul 或自建网关中加入 Sa‑Token 的过滤器，实现统一的网关鉴权与 token 续期。  
5. **单点登录（SSO）**：配置统一的认证中心，业务系统通过 `SaOAuth2Util` 或 `SaSsoUtil` 完成跨系统登录态共享。  

**生产可用性**  
- **活跃度高**：截至 2026‑07‑04，GitHub ★18,917、Fork 2,915，最近一次提交在当日，社区活跃、Issue 响应及时。  
- **成熟度**：框架已在多个大型企业的生产环境中使用，支持分布式会话、集群容错、限流防刷等实战特性。  
- **生态兼容**：原生兼容 SpringBoot、Spring Cloud、Dubbo、MyBatis、JPA 等主流技术栈，提供完整的 Starter 与示例项目，降低集成成本。  
- **安全保障**：实现了密码加盐、验证码、防重放、Token 加密、签名校验等安全措施，并提供安全审计日志。  

综合来看，Sa‑Token 具备 **高可用、易集成、功能完整** 的特性，适合作为企业级 Java 项目统一的安全认证与授权解决方案。

## 🧭 Practical evaluation

**Value:** dromara/Sa-Token helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 18917 GitHub stars
- 2915 forks
- updated 2026-07-04
- primary language: Java
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 87/100 |
| stars | 91/100 |
| topics | 75/100 |
| outlook | 87/100 |
| quality | 92/100 |
| recency | 100/100 |
| adoption | 90/100 |
| production | 81/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-04 · [View on GitHub](https://github.com/dromara/Sa-Token) · [← Back to Backend](./README.md)</sub>
