# Evolveum/midpoint

[![Stars](https://img.shields.io/github/stars/Evolveum/midpoint?style=flat-square&color=yellow)](https://github.com/Evolveum/midpoint/stargazers) [![Forks](https://img.shields.io/github/forks/Evolveum/midpoint?style=flat-square&color=blue)](https://github.com/Evolveum/midpoint/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Evolveum MidPoint: Identity Management (IDM) and Identity Governance (IGA)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 511 |
| 🍴 **Forks** | 229 |
| 💻 **Language** | Java |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-07-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`identity-governance` `identity-management` `idm` `iga` `java`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
Evolveum MidPoint is an open‑source Java platform for Identity Management (IDM) and Identity Governance (IGA). With a modest community (≈ 511 ★, 229 forks) and recent activity, it can serve as a solid foundation for prototypes or internal workflows that need centralized user provisioning, role‑based access control, and lifecycle governance. Its usefulness hinges on aligning the project's README and current feature set with your concrete identity‑related use case.

**Value**  
MidPoint delivers a comprehensive IDM/IGA stack—user provisioning, entitlement management, workflow‑driven approvals, and fine‑grained policy enforcement—without requiring a commercial license. For organizations looking to consolidate disparate identity sources or build custom governance processes, it offers a reusable, extensible code base that can be tailored through its modular architecture and scripting support.

**Practical adoption path**  

1. **Proof‑of‑concept** – Clone the repo, run the supplied Docker or Maven build, and follow the quick‑start guide to provision a few test accounts.  
2. **Fit‑gap analysis** – Compare the README‑listed connectors and workflow templates with the systems you need to integrate (AD, LDAP, SaaS APIs, etc.).  
3. **Pilot integration** – Implement a minimal set of connectors and approval workflows in a sandbox environment, using the built‑in REST/SCIM interfaces for automation.  
4. **Iterative extension** – Extend the platform with custom connectors or scripts as gaps are identified, leveraging the Java SDK and community examples.  

**Production readiness**  
MidPoint sits at a medium readiness level: it is stable enough for internal prototypes and controlled production use, but it requires diligence before full‑scale deployment. Key checks include verifying the licensing (Apache‑2.0), performing a security audit of the deployed version, confirming that active maintainers are responsive, and establishing a process for applying updates and managing dependencies. With these safeguards in place, MidPoint can be a viable core for IDM/IGA in production environments.

### Русский

Evolveum MidPoint – это открытая платформа для управления идентификацией (IDM) и её контроля (IGA), написанная на Java и активно поддерживаемая сообществом (511 звёзд, 229 форков, последние коммиты — июль 2026). Она подходит для создания прототипов и внутренних процессов (например, автоматизированного создания, синхронизации и де‑привилегирования учётных записей) при условии предварительной проверки README и небольшого proof‑of‑concept, после чего можно оценить зависимости и требования к обслуживанию. Готовность к продакшну средняя: проект стабилен, но требует дополнительного аудита лицензий, безопасности и наличия активных мейнтейнеров перед масштабным внедрением.

### 中文

**项目简介**  
Evolveum MidPoint 是一款基于 Java 的开源身份管理（IDM）和身份治理（IGA）平台，提供用户、角色、组织结构的集中化建模、生命周期管理以及合规审计功能。

**价值**  
- **统一身份治理**：通过统一的模型和工作流，实现用户账户的创建、变更、停用以及权限审批的全流程自动化。  
- **高度可扩展**：支持自定义脚本、规则引擎和丰富的连接器，可对接 LDAP、Active Directory、云 SaaS（Azure AD、Okta 等）以及内部业务系统。  
- **合规审计**：内置审计日志、报表和策略检查，帮助组织满足 GDPR、SOX 等合规要求。

**典型接入方式**  
1. **环境准备**：下载源码或使用官方提供的 Docker 镜像，启动 PostgreSQL（或其他支持的数据库）并运行 MidPoint。  
2. **连接器配置**：在管理控制台中添加所需的系统连接器（如 LDAP、REST、SCIM），并映射属性到 MidPoint 的统一模型。  
3. **工作流与策略**：使用内置的 BPMN 工作流编辑器或 Groovy 脚本定义账户生命周期、审批流程和合规规则。  
4. **API 集成**：通过 REST/JSON API 或 Java SDK 将业务系统（HR、ERP、云平台）与 MidPoint 进行双向同步，常见做法是先实现一个小范围的 PoC（如仅同步新入职员工），验证数据映射和同步频率后逐步扩大覆盖范围。

**生产可用性**  
- **成熟度**：项目已有 511+ ⭐、229+ 🍴，活跃维护至 2026‑07‑12，代码基于 Java，社区提供较完整的文档和示例。  
- **适用场景**：适合内部原型、部门级身份治理以及中小规模企业的生产环境；在大规模企业级部署前需进行依赖审计、性能压测以及安全审查。  
- **风险与准备**：需确认许可证（Apache‑2.0）符合公司政策，评估容器化或 Kubernetes 部署的运维成本，并对关键连接器进行安全加固后方可进入正式生产。  

总体而言，MidPoint 在功能完整性和可定制性上具备较高价值，适合作为内部身份治理的核心平台，前期通过小范围 PoC 验证后即可逐步推进至生产使用。

## 🧭 Practical evaluation

**Value:** Evolveum/midpoint may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 511 GitHub stars
- 229 forks
- updated 2026-07-12
- primary language: Java
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 59/100 |
| stars | 58/100 |
| topics | 63/100 |
| outlook | 74/100 |
| quality | 75/100 |
| recency | 100/100 |
| adoption | 58/100 |
| production | 75/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/Evolveum/midpoint) · [← Back to Misc](./README.md)</sub>
