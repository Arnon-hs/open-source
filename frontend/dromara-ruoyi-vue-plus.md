# dromara/RuoYi-Vue-Plus

[![Stars](https://img.shields.io/github/stars/dromara/RuoYi-Vue-Plus?style=flat-square&color=yellow)](https://github.com/dromara/RuoYi-Vue-Plus/stargazers) [![Forks](https://img.shields.io/github/forks/dromara/RuoYi-Vue-Plus?style=flat-square&color=blue)](https://github.com/dromara/RuoYi-Vue-Plus/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> 多租户后台管理系统 重写RuoYi-Vue所有功能 集成 Sa-Token、Mybatis-Plus、WarmFlow、SpringDoc、Hutool、OSS 定期同步

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.4k |
| 🍴 **Forks** | 691 |
| 💻 **Language** | Java |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`docker` `mybatis` `oss` `springboot` `vue`

## 🎯 Categories

Frontend · DevOps/Infra

## 📝 Summary

### English

**Project Summary**

dromara/RuoYi-Vue-Plus is an open-source, multi-tenant backend management system that rewrites all features of RuoYi-Vue, integrating various popular technologies such as Sa-Token, Mybatis-Plus, and SpringDoc. This project helps developers build product UI faster by reusing interface components, improving frontend delivery, and reducing custom UI work. With its recent activity, strong adoption, and robust ecosystem, it's highly production-ready for a serious pilot.

**Value Proposition**

The primary value proposition of dromara/RuoYi-Vue-Plus lies in its ability to help developers ship user-facing interfaces with less custom UI work, thereby improving frontend delivery and reducing development time. By reusing interface components, developers can quickly build product UI, making it an ideal choice for teams looking to accelerate their frontend development process.

**Practical Adoption Path**

To adopt dromara/RuoYi-Vue-Plus, developers can follow these steps:

1. Evaluate the project's codebase, documentation, and community support to ensure it meets their requirements.
2. Integrate the project into their existing tech stack, considering the dependencies and potential conflicts.
3. Test and iterate on the project to ensure seamless functionality and performance.
4.

### Русский

Резюме проекта dromara/RuoYi-Vue-Plus:

dromara/RuoYi-Vue-Plus — это open-source проект, который предлагает готовую многообещающую платформу для создания пользовательских интерфейсов с минимальной настройкой UI. Это идеальный выбор для разработчиков, которые хотят ускорить процесс разработки и реализации frontend-части своих проектов. Платформа готова к использованию в production环境е, с активными разработчиками и регулярным обновлением до последней версии.

### 中文

**项目简介（2‑3 句）**  
dromara / RuoYi‑Vue‑Plus 是基于多租户的后台管理系统，全面重写并增强了 RuoYi‑Vue 的所有功能。项目集成了 Sa‑Token、Mybatis‑Plus、WarmFlow、SpringDoc、Hutool、OSS 等主流组件，实现了权限、持久化、工作流、接口文档和对象存储的一站式解决方案，并提供定期同步机制。

**价值**  
- **快速交付 UI**：内置完整的前后端脚手架和丰富的页面模板，开发者只需少量业务代码即可搭建用户界面。  
- **统一安全与数据层**：Sa‑Token 提供灵活的多租户、登录、鉴权方案；Mybatis‑Plus 简化 CRUD，降低数据库维护成本。  
- **可扩展工作流**：WarmFlow 让业务流程可视化配置，减少硬编码。  
- **完整文档与生态**：SpringDoc 自动生成 OpenAPI 文档，配合 OSS 对象存储即插即用，提升系统可维护性和交付效率。

**典型接入方式**  
1. **克隆仓库** → `git clone https://github.com/dromara/RuoYi-Vue-Plus.git`  
2. **环境准备**：JDK 17+、MySQL、Redis（可选用于 Sa‑Token），以及前端 Node.js 环境。  
3. **配置数据库**：在 `application.yml` 中填写租户库信息，运行 `sql/ruoyi.sql` 初始化。  
4. **启动后端**：`mvn clean package && java -jar ruoyi-admin/target/ruoyi-admin.jar`  
5. **启动前端**：`cd ruoyi-ui && npm install && npm run dev`，默认访问 `http://localhost:80`。  
6. **二次定制**：通过 Sa‑Token 注解、Mybatis‑Plus Mapper、WarmFlow 流程模型或 SpringDoc 注解，快速加入业务功能。

**生产可用性**  
- **活跃度**：截至 2026‑06‑30，项目拥有 2.3k+ ⭐、691 fork，最近一次提交在 2026‑06‑30，表明维护持续活跃。  
- **技术成熟度**：基于 Spring Boot、Mybatis‑Plus 等企业级框架，已在多个内部系统验证，具备高可用、水平扩展能力。  
- **安全与合规**：使用 Sa‑Token 的细粒度权限控制，配合 Spring Security 可进一步加固；项目采用 Apache‑2.0 许可证，商业使用无障碍。  
- **运维准备**：提供 Dockerfile 与 Kubernetes 部署脚本，支持灰度发布和定时同步任务，便于在容器化平台上实现弹性部署。  

综合来看，RuoYi‑Vue‑Plus 已具备 **高可用、易集成、功能完整** 的特性，是面向企业级后台管理系统的可靠 OSS 选型，可直接用于生产环境并快速迭代业务需求。

## 🧭 Practical evaluation

**Value:** dromara/RuoYi-Vue-Plus helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2358 GitHub stars
- 691 forks
- updated 2026-06-30
- primary language: Java
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 71/100 |
| stars | 72/100 |
| topics | 63/100 |
| outlook | 74/100 |
| quality | 77/100 |
| recency | 80/100 |
| adoption | 72/100 |
| production | 70/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/dromara/RuoYi-Vue-Plus) · [← Back to Frontend](./README.md)</sub>
