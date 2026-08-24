# warp-tech/warpgate

[![Stars](https://img.shields.io/github/stars/warp-tech/warpgate?style=flat-square&color=yellow)](https://github.com/warp-tech/warpgate/stargazers) [![Forks](https://img.shields.io/github/forks/warp-tech/warpgate?style=flat-square&color=blue)](https://github.com/warp-tech/warpgate/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Fully transparent SSH, HTTPS, Kubernetes, MySQL and Postgres bastion/PAM that doesn't need additional client-side software

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 7k |
| 🍴 **Forks** | 272 |
| 💻 **Language** | Rust |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bastion` `bastion-host` `https` `https-proxy` `infrastructure` `kubectl` `kubernetes` `mysql` `mysql-proxy` `pam` `postgresql-proxy` `privileged-access-management`

## 🎯 Categories

Backend · Database · DevOps/Infra

## 📝 Summary

### English

**Summary**  
warp‑tech/warpgate is a Rust‑based, fully transparent bastion that proxies SSH, HTTPS, Kubernetes, MySQL and PostgreSQL traffic without requiring any special client‑side software. It lets teams reuse a single, centrally‑managed gateway for multiple protocols, cutting the need to build and maintain bespoke access‑control layers. With a strong community (≈7 k stars, active commits) it is ready for serious pilot projects.

**Value**  
- **Unified access point** – One bastion handles all common backend protocols, simplifying network topology and reducing the surface area for security misconfigurations.  
- **Zero‑client friction** – Users connect with their existing SSH, curl, kubectl, mysql, or psql tools; no custom agents or SDKs are needed, which accelerates onboarding and lowers operational overhead.  
- **Reusability & standardization** – Teams can adopt a single, audited gateway across services, freeing developers to focus on business logic rather than recreating authentication, audit logging, and session management.

**Practical adoption path**  
1. **Evaluate the API/CLI** – Clone the repo, run the provided Docker compose or binary, and point a test service to the bastion to verify protocol passthrough.  
2. **Integrate with existing IAM** – Configure Warpgate to use your organization’s PAM, LDAP, OIDC, or SSH key store; the project supplies ready‑made adapters and example configs.  
3. **Gradual rollout** – Start with a low‑risk service (e.g., an internal MySQL instance), monitor logs and audit trails, then expand to Kubernetes clusters and external APIs.  
4. **Automation** – Use the supplied SDK or CLI to provision users, roles, and session policies as part of your CI/CD pipelines.

**Production readiness**  
- **Activity & adoption** – Recent commits (as of 2026‑05‑12), >6 900 stars, and dozens of forks indicate a healthy ecosystem.  
- **Maturity** – Core features (protocol tunneling, PAM integration, audit logging) are stable; the Rust codebase is type‑safe and performant.  
- **Risk considerations** – License compliance, formal security audit, and maintainer responsiveness should be confirmed before full‑scale deployment, but the overall signal is strong enough for a production pilot.

### Русский

**warp-tech/warpgate** — это полностью прозрачный bastion‑прокси для SSH, HTTPS, Kubernetes, MySQL и Postgres, реализованный на Rust и не требующий установки дополнительного клиентского ПО. Он позволяет командам быстро подключать новые API‑сервисы к уже существующей инфраструктуре, стандартизировать доступ к базам и кластерам и тем самым сократить дублирование бекенд‑компонентов. Проект имеет высокий уровень готовности к production: активные коммиты, более 6 тыс. звёзд на GitHub, широкая экосистема интеграций и подтверждённое использование в реальных проектах, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
warp-tech/warpgate 是一款基于 Rust 实现的 **全透明** Bastion / PAM 解决方案，支持 SSH、HTTPS、Kubernetes、MySQL 与 Postgres 等协议。它无需在客户端额外安装任何软件，只需通过标准的网络工具即可安全地访问内部服务。

**价值主张**  
- **复用现有基础设施**：团队可以直接在已有的服务网关、身份认证与审计体系上挂载 Warpgate，而不必重新开发统一的入口层。  
- **加速业务交付**：统一的访问入口让 API、数据库或 K8s 集群的内部调用变得即插即用，显著缩短后端服务的交付周期。  
- **标准化运维模式**：统一的审计、授权与审计日志，帮助组织在安全合规、审计追踪上保持一致性。

**典型接入方式**  
1. **部署方式**：以容器（Docker/OCI）或二进制方式运行 Warpgate，配置好后端目标（SSH 主机、K8s API、数据库实例）以及身份提供者（LDAP、OAuth、PAM 等）。  
2. **客户端使用**：  
   - **SSH**：`ssh -J warpgate.example.com user@target`（使用 SSH Jump）  
   - **HTTPS / API**：直接请求 `https://warpgate.example.com/<service>`，Warpgate 会根据路径转发到对应的内部服务。  
   - **Kubernetes**：在 `kubeconfig` 中将 `server` 指向 Warpgate，并使用已有的 kube‑auth 机制。  
   - **MySQL / Postgres**：在客户端连接字符串中把主机改为 Warpgate 地址，Warpgate 完成协议级转发。  
3. **自动化集成**：项目提供 RESTful API、CLI (`warpgate-cli`) 与 Rust SDK，可在 CI/CD、Terraform、Ansible 等工具链中实现动态注册、策略更新与监控。

**生产可用性**  
- **活跃度**：截至 2026‑05‑12，项目拥有 **6,967** 星、**272** Fork，最近一次提交在同一天，表明维护活跃。  
- **技术成熟度**：核心使用 Rust 编写，具备内存安全与高并发特性；已在多个公开案例中作为生产级 Bastion 使用。  
- **生态兼容**：提供标准协议的透明转发，兼容现有 SSH、HTTPS、K8s、MySQL、Postgres 客户端，无需改动业务代码。  
- **风险点**：仍需对许可证（Apache‑2.0/MIT 等）和安全审计报告进行最终确认；建议在正式投产前进行渗透测试并配置审计日志的持久化。  

综上，warp-tech/warpgate 具备 **高可用、易集成、无需客户端改造** 的特性，是在内部网络中统一访问控制与审计的可靠 OSS 选项，适合作为企业级生产环境的入口层。

## 🧭 Practical evaluation

**Value:** warp-tech/warpgate helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 6967 GitHub stars
- 272 forks
- updated 2026-05-12
- primary language: Rust
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 61/100 |
| stars | 82/100 |
| topics | 100/100 |
| outlook | 58/100 |
| quality | 69/100 |
| recency | 20/100 |
| adoption | 76/100 |
| production | 56/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/warp-tech/warpgate) · [← Back to Backend](./README.md)</sub>
