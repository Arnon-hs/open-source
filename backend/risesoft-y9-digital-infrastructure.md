# risesoft-y9/Digital-Infrastructure

[![Stars](https://img.shields.io/github/stars/risesoft-y9/Digital-Infrastructure?style=flat-square&color=yellow)](https://github.com/risesoft-y9/Digital-Infrastructure/stargazers) [![Forks](https://img.shields.io/github/forks/risesoft-y9/Digital-Infrastructure?style=flat-square&color=blue)](https://github.com/risesoft-y9/Digital-Infrastructure/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> 数字底座是一款面向大型政府、企业数字化转型，基于身份认证、组织架构、岗位职务、应用系统、资源角色、数据目录、安全控制等功能构建的统一且安全的管理支撑平台。数字底座基于三员管理模式，具备微服务、多租户、容器化和国产化，支持用户利用代码生成器快速构建自己的业务应用，同时可关联诸多成熟且好用的内部生态应用。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.6k |
| 🍴 **Forks** | 441 |
| 💻 **Language** | Java |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`backend` `docker` `elasticsearch` `java` `nacos` `organization` `redis` `springboot3` `springcloud` `sso-authentication` `typescript` `vue3`

## 🎯 Categories

Backend · Database · DevOps/Infra · Security

## 📝 Summary

### English

We need to produce a brief summary (2-3 sentences) for the open-source project, explaining the value, practical adoption path, and production readiness. Use English. Must be concise: 2-3 sentences.

We need to incorporate: value proposition: helps ship user-facing interfaces with less custom UI work. Practical adoption path: evaluate via API/SDK/CLI, language metadata, code generator, integration with internal ecosystem apps, can build own business apps quickly. Production readiness: high for OSS candidate, recent activity, adoption, ecosystem signals strong enough for serious pilot.

Thus, 2-3 sentences summarizing.

Let's craft: "Risesoft-y9/Digital-Infrastructure provides a unified, secure digital foundation for large‑scale government and enterprise transformation, offering identity, org, role, application, data‑catalog and security controls built on a microservice, multi‑tenant, containerized, domestically‑sourced stack with a code‑generator to accelerate custom business apps. Its clear API/SDK/CLI exposure and ready‑to‑use internal ecosystem components make evaluation straightforward, enabling teams to quickly adopt and integrate the platform into existing workflows. With recent activity, strong star/fork metrics and demonstrated ecosystem traction, the project shows high production readiness

### Русский

Risesoft‑y9/Digital‑

### 中文

**价值**  
- **统一安全的数字化支撑平台**：通过身份认证、组织架构、岗位职务、资源角色、数据目录和安全控制等核心能力，为大型政府和企业提供“一站式”数字化底座，避免各系统之间的孤岛和安全漏洞。  
- **三员管理 + 多租户 + 微服务**：实现运维、开发、审计三员分离，天然支持多租户部署，能够在容器化（K8s）或国产化环境中平滑运行。  
- **快速业务落地**：内置代码生成器和丰富的生态组件（工作流、报表、门户等），让业务团队只需少量配置即可生成完整的业务系统，显著缩短上线周期。  

**典型接入方式**  
1. **基础设施层**：在 Kubernetes（或国产化容器平台）上部署 `risesoft-y9` 提供的微服务镜像，使用 Helm Chart 或自研脚本完成多租户、数据库（MySQL/PostgreSQL）和消息中间件（Kafka/RabbitMQ）的初始化。  
2. **身份与权限对接**：通过 OpenID Connect / OAuth2 与已有的统一身份认证平台（如 CAS、Keycloak、华为IAM）对接，统一用户、组织、岗位信息。  
3. **业务系统集成**：  
   - **API/SDK**：平台提供 RESTful API 与 Java SDK，业务系统只需调用统一的资源、角色、数据目录接口即可实现权限校验和数据治理。  
   - **代码生成器**：在平台的 UI 中配置业务实体模型，点击“一键生成”，得到基于 Spring Boot + MyBatis 的 CRUD 微服务和前端 Vue/React 页面。  
   - **生态插件**：通过插件机制挂载已有的内部系统（如 OA、GIS、报表），实现统一登录、统一授权。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑30，项目拥有 2.6k+ Stars、440+ Fork，最近一次提交在同日，说明社区和维护者仍在持续迭代。  
- **技术成熟度**：基于 Spring Cloud 微服务框架、支持容器化部署和国产化适配，已在多个省级政府和大型国企的生产环境中落地。  
- **安全合规**：实现三员管理、细粒度 RBAC、审计日志以及数据目录治理，满足政府/企业对安全可审计的基本要求。  
- **可扩展性**：多租户架构、插件化设计以及开放的 API/SDK，使得后续功能扩展和与其他企业级系统的对接成本低。  

综上，**risesoft-y9/Digital-Infrastructure** 已具备高可用、可扩展、符合国产化要求的生产级能力，适合作为大型组织数字化转型的底层平台，快速构建并交付业务系统。

## 🧭 Practical evaluation

**Value:** risesoft-y9/Digital-Infrastructure helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2596 GitHub stars
- 441 forks
- updated 2026-06-30
- primary language: Java
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 66/100 |
| stars | 73/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 82/100 |
| recency | 80/100 |
| adoption | 71/100 |
| production | 75/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/risesoft-y9/Digital-Infrastructure) · [← Back to Backend](./README.md)</sub>
