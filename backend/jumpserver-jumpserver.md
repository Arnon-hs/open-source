# jumpserver/jumpserver

[![Stars](https://img.shields.io/github/stars/jumpserver/jumpserver?style=flat-square&color=yellow)](https://github.com/jumpserver/jumpserver/stargazers) [![Forks](https://img.shields.io/github/forks/jumpserver/jumpserver?style=flat-square&color=blue)](https://github.com/jumpserver/jumpserver/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> JumpServer is an open-source Privileged Access Management (PAM) platform that provides DevOps and IT teams with on-demand and secure access to SSH, RDP, Kubernetes, Database and RemoteApp endpoints through a web browser.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 30.4k |
| 🍴 **Forks** | 5.7k |
| 💻 **Language** | Python |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bastion-host` `cyberark` `django` `jumpserver` `pam` `python` `ssh-server` `teleport` `terminal`

## 🎯 Categories

Backend · Database · DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
JumpServer is an open‑source Privileged Access Management (PAM) platform that lets DevOps and IT teams securely access SSH, RDP, Kubernetes, databases, and RemoteApp resources from a web browser. With over 30 k stars and active maintenance, it offers a mature, Python‑based backend that can replace custom-built PAM components. The project scores 77/100, indicating strong community adoption and a solid foundation for production use.

**Value**  
JumpServer provides a turnkey PAM solution, eliminating the need for teams to build and maintain their own authentication, session‑recording, and audit infrastructure. By reusing a common backend for access control, organizations can accelerate API service delivery, enforce consistent security policies, and reduce operational overhead across cloud, on‑prem, and hybrid environments.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, follow the README to spin up the Docker‑compose demo, and validate connectivity to a few test assets (e.g., an SSH host and a Kubernetes cluster).  
2. **Integration** – Connect JumpServer to existing identity providers (LDAP, AD, OAuth) and configure asset inventory via its API or UI.  
3. **Pilot** – Deploy the platform in a staging environment, enable session recording and audit logging, and migrate a limited set of privileged accounts.  
4. **Full Rollout** – Gradually expand coverage to all critical endpoints, enforce role‑based access policies, and integrate with CI/CD pipelines for automated asset onboarding.

**Production Readiness**  
The project shows high production readiness: recent commits (as of 2026‑05‑13), a large and active community (30 k+ stars, 5 k+ forks), and a mature Python codebase. While the license and security posture still require a final review, the strong activity signals, extensive documentation, and existing enterprise adopters make JumpServer suitable for serious pilots and eventual production deployment.

### Русский

JumpServer — это открытая PAM‑платформа, позволяющая DevOps и IT‑командам безопасно предоставлять on‑demand доступ к SSH, RDP, Kubernetes, базам данных и RemoteApp через веб‑браузер, экономя время на построении собственного бекенда. Типичный сценарий — запуск небольшого proof‑of‑concept, интеграция через готовый README и последующее масштабирование для централизованного управления привилегированным доступом в продакшн‑окружениях. Проект имеет высокий уровень готовности: активные коммиты, более 30 тыс. звёзд, широкое сообщество и зрелый стек Python, что делает его надёжным кандидатом для серьёзных пилотных внедрений.

### 中文

**项目简介**  
JumpServer（jumpserver/jumpserver）是一款开源的特权访问管理（PAM）平台，能够通过浏览器为 DevOps 与 IT 团队提供 SSH、RDP、Kubernetes、数据库以及 RemoteApp 等终端的按需安全访问。

**价值**  
- **复用现有基础设施**：统一的访问网关让团队无需自行开发或维护各类协议的审计、凭证管理和审计日志，从而把精力集中在业务功能上。  
- **提升交付速度**：提供即插即用的 API 与 UI，帮助快速搭建内部工具或对外服务的安全访问层，缩短 API 服务的上线周期。  
- **标准化安全治理**：统一的权限模型、审计日志和多因素认证，使跨项目、跨部门的特权操作遵循统一的合规标准。

**典型接入方式**  
1. **部署方式**：支持 Docker‑Compose、Kubernetes Helm Chart 以及离线安装包，可在私有云或公有云环境中快速启动。  
2. **身份认证集成**：通过 LDAP/AD、OAuth2、SAML、OIDC 等方式同步企业用户；也可使用本地账号。  
3. **资源接入**：在 JumpServer 控制台或 API 中登记目标主机/容器/K8s 集群，配置资产分组、授权策略后，即可通过 Web 或 SSH 客户端进行访问。  
4. **二次开发**：提供 RESTful API 与 Webhook，便于在 CI/CD、自动化运维或自研门户中嵌入“一键登录”功能。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑13，项目拥有 30,445 星、5,697 Fork，最近一次提交在同一天，社区活跃且有多家企业在生产环境使用。  
- **技术成熟**：核心使用 Python 开发，配套的 MySQL/PostgreSQL、Redis、RabbitMQ 等组件均为业界成熟方案。  
- **可评估路径**：建议先在测试环境通过官方提供的 Docker‑Compose 快速搭建一个 PoC，验证 LDAP、审计日志及 API 调用是否满足业务需求，再逐步迁移到生产集群（可使用 Helm 进行高可用部署）。  
- **风险**：需进一步审查许可证（GPL‑3.0）与安全漏洞响应情况，确保符合公司合规要求。  

综合来看，JumpServer 在特权访问管理领域具备完整的功能、活跃的社区和成熟的部署方案，是一个可以直接用于生产的 OSS 候选。

## 🧭 Practical evaluation

**Value:** jumpserver/jumpserver helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 30445 GitHub stars
- 5697 forks
- updated 2026-05-13
- primary language: Python
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 94/100 |
| stars | 95/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 78/100 |
| recency | 20/100 |
| adoption | 95/100 |
| production | 61/100 |
| usefulness | 42/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/jumpserver/jumpserver) · [← Back to Backend](./README.md)</sub>
