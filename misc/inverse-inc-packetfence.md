# inverse-inc/packetfence

[![Stars](https://img.shields.io/github/stars/inverse-inc/packetfence?style=flat-square&color=yellow)](https://github.com/inverse-inc/packetfence/stargazers) [![Forks](https://img.shields.io/github/forks/inverse-inc/packetfence?style=flat-square&color=blue)](https://github.com/inverse-inc/packetfence/network) [![Language](https://img.shields.io/badge/lang-Perl-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> PacketFence is a fully supported, trusted, Free and Open Source network access control (NAC) solution. Boasting an impressive feature set including a captive-portal for registration and remediation, centralized wired and wireless management, powerful BYOD management options, 802.1X support, layer-2 isolation of problematic devices; PacketFence can be used to effectively secure networks small to very large heterogeneous networks.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.6k |
| 🍴 **Forks** | 319 |
| 💻 **Language** | Perl |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`nac` `network` `packetfence`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
PacketFence is a free, open‑source Network Access Control (NAC) platform that secures wired, wireless and VPN networks through 802.1X authentication, captive‑portal registration, BYOD onboarding, device quarantine, and centralized policy management. It scales from small office setups to large, heterogeneous enterprise environments.

**Value Proposition**  
- **Comprehensive NAC features** in a single package (authentication, remediation, guest access, device profiling).  
- **Extensible, language‑agnostic APIs** and a web UI that let you integrate with existing identity stores (Active Directory, LDAP, RADIUS) and orchestration tools.  
- **Strong community backing** (1.6 k ★, 300+ forks) and regular updates (last commit 2026‑06‑25), making it a viable alternative to commercial NAC solutions.

**Practical Adoption Path**  

| Step | Action | Why it matters |
|------|--------|----------------|
| 1️⃣  | **Evaluate fit** – Review the README, architecture diagram, and supported authentication methods to confirm it matches your network topology (wired, Wi‑Fi, VPN, guest portals). | Avoids costly re‑engineering if core features are missing. |
| 2️⃣  | **Prototype in a sandbox** – Deploy PacketFence using the provided Docker/VM images on a test VLAN. Connect a few test devices and verify 802.1X, captive‑portal, and quarantine workflows. | Quick proof‑of‑concept with minimal impact on production. |
| 3️⃣  | **Integrate identity sources** – Configure LDAP/AD, RADIUS, or SAML connectors; map user groups to VLANs or ACLs. | Ensures seamless single‑sign‑on and policy enforcement. |
| 4️⃣  | **Automate provisioning** – Use the REST API or Ansible modules (if available) to script device registration, policy updates, and reporting. | Reduces manual admin overhead and supports CI/CD pipelines. |
| 5️⃣  | **Run a pilot** – Roll out to a limited user segment (e.g., a single floor or guest network). Monitor logs, quarantine actions, and performance metrics. | Validates scalability and uncovers integration quirks early. |
| 6️⃣  | **Full‑scale rollout & ops hand‑off** – Harden the deployment (TLS, firewall rules, backup of the PostgreSQL database), set up alerting, and document SOPs for updates and troubleshooting. | Guarantees long‑term stability and maintainability. |

**Production Readiness Assessment**  
- **Maturity:** Medium. The project is actively maintained and widely used, but the documentation around modern CI/CD integration and cloud‑native deployments is limited.  
- **Dependencies:** Primarily Perl, PostgreSQL, and a web stack (Apache/Nginx). Verify version compatibility with your OS and container runtime.  
- **Risk Mitigation:** Conduct a cost‑benefit analysis of the initial setup effort (network re‑architecture, RADIUS/LDAP sync) and allocate time for staff training. Consider a fallback to a commercial NAC or existing radius solution during the pilot phase.  

In summary, PacketFence offers a feature‑rich, open‑source NAC solution that can be adopted incrementally—starting with a sandbox test, moving through a controlled pilot, and finally scaling to production—provided you allocate time for integration testing and operational hardening.

### Русский

PacketFence — это полностью открытое решение NAC, позволяющее централизованно управлять доступом к проводным и беспроводным сетям, реализовать captive‑portal, BYOD, 802.1X и изоляцию проблемных устройств; подходит как для небольших офисов, так и для крупных разнородных инфраструктур. Типичный сценарий — интеграция в существующую сеть для автоматической аутентификации, регистрации новых пользователей и быстрого реагирования на нарушения политики безопасности. Готовность к production — средняя: проект стабилен и активно поддерживается (1641 ★, 319 forks, обновления до 2026‑06‑25), однако требуется ручная проверка интеграционных точек и оценка затрат на развёртывание.

### 中文

**项目简介**  
PacketFence（inverse‑inc/packetfence）是一款功能完整、免费开源的网络接入控制（NAC）系统，提供捕获门户、集中式有线/无线管理、BYOD 管理、802.1X 认证以及问题设备的二层隔离等特性，适用于从小型办公室到大型异构网络的安全防护。

**价值**  
- **统一安全策略**：一次配置即可对有线、无线、VPN、访客网络等多种接入方式统一实施身份验证、授权和审计。  
- **灵活的设备登记与整改**：捕获门户支持自助注册、设备合规检查和自动整改，降低运维成本。  
- **强大的可视化与报告**：实时监控、设备指纹、日志与合规报表，帮助安全团队快速定位异常设备。  

**典型接入方式**  
1. **网络层集成**：在交换机/路由器上启用 802.1X、MAC‑Auth 或 VLAN‑Based 控制，将不合规设备的流量重定向到 PacketFence 的 captive‑portal。  
2. **无线控制器集成**：通过 RADIUS 接口让无线 AP 向 PacketFence 进行身份验证与授权。  
3. **外部目录/身份源**：可对接 LDAP、Active Directory、FreeRADIUS、OAuth 等，实现统一身份管理。  
4. **API/脚本**：利用 RESTful API 或 Perl/CLI 脚本实现自动化设备注册、隔离或策略更新。  

**生产可用性**  
- **成熟度**：项目已有 1.6k+ Stars、300+ Fork，活跃维护至 2026‑06‑25，社区和商业版（inverse‑inc）提供正式技术支持。  
- **适用场景**：适合内部原型、实验环境以及中大型企业网络的正式部署。  
- **部署要求**：基于 Perl，需准备 MySQL/MariaDB、Redis、Web 服务器（Apache/Nginx）等依赖；建议在容器或虚拟机中进行预演，确认硬件兼容性（交换机、无线控制器）和 RADIUS 集成细节。  
- **风险**：元数据中集成指引不够完整，实际落地前需进行手动调研和小规模试点，评估配置复杂度、运维成本以及与现有网络设备的兼容性。  

总体而言，PacketFence 在功能完整性和社区活跃度上具备中等至高的生产就绪度，适合作为企业内部 NAC 的核心组件，只要在部署前做好依赖审查和集成测试即可投入生产使用。

## 🧭 Practical evaluation

**Value:** inverse-inc/packetfence may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1641 GitHub stars
- 319 forks
- updated 2026-06-25
- primary language: Perl
- 3 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 63/100 |
| stars | 68/100 |
| topics | 38/100 |
| outlook | 67/100 |
| quality | 71/100 |
| recency | 80/100 |
| adoption | 67/100 |
| production | 66/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/inverse-inc/packetfence) · [← Back to Misc](./README.md)</sub>
