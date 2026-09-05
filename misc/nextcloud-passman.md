# nextcloud/passman

[![Stars](https://img.shields.io/github/stars/nextcloud/passman?style=flat-square&color=yellow)](https://github.com/nextcloud/passman/stargazers) [![Forks](https://img.shields.io/github/forks/nextcloud/passman?style=flat-square&color=blue)](https://github.com/nextcloud/passman/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> 🔐 Open source password manager with Nextcloud integration

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 821 |
| 🍴 **Forks** | 114 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`hacktoberfest` `nextcloud` `passman` `password-manager`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
nextcloud/passman is an open‑source password manager that stores credentials directly inside a Nextcloud instance, letting teams share and synchronize passwords through the familiar Nextcloud UI. With ~820 GitHub stars and recent activity, it offers a JavaScript‑based solution that can be trialled quickly for internal tools or prototype workflows.

**Value**  
- **Seamless Nextcloud integration**: Leverages an existing Nextcloud deployment, eliminating the need for a separate vault service and providing native access controls, sharing, and audit trails.  
- **Open‑source transparency**: The code is publicly available, allowing you to audit security, customize features, and avoid vendor lock‑in.  
- **Collaborative password sharing**: Teams can store, retrieve, and rotate credentials together, which is especially useful for DevOps, CI/CD pipelines, or shared SaaS logins.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, follow the README to install the app on a non‑production Nextcloud instance, and test basic CRUD operations on passwords.  
2. **Security review** – Verify encryption handling, audit the storage format, and confirm that TLS is enforced for all client‑server traffic.  
3. **Pilot rollout** – Deploy the app to a small internal group (e.g., a dev team) and integrate it with a simple script or CI job to fetch secrets.  
4. **Documentation & training** – Capture the exact installation steps, permission model, and usage guidelines for broader adoption.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last update 2026‑06‑27) and has a healthy community (821 stars, 114 forks), but the integration documentation is modest and the deployment workflow is not fully automated.  
- **Considerations before production**:  
  * Verify compatibility with your Nextcloud version and any custom apps.  
  * Assess the maintenance burden of the JavaScript codebase and plan for regular updates.  
  * Perform a security audit of the encryption implementation and define backup/restore procedures for the password database.  
- **Fit for production**: Suitable for internal prototypes, sandbox environments, or small‑to‑medium teams that already run Nextcloud, provided you conduct the above checks and allocate resources for ongoing maintenance.

### Русский

nextcloud/passman — это открытый менеджер паролей, тесно интегрированный с Nextcloud, позволяющий хранить и синхронизировать учетные данные прямо в вашем облачном хранилище. Его типичный сценарий — небольшие команды или внутренние проекты, где требуется простой способ совместного доступа к паролям без отдельного сервиса; рекомендуется начать с небольшого proof‑of‑concept, проверив README и базовую настройку в тестовой среде. Готовность к production среднему уровню: проект имеет активную поддержку (обновления, 821★), но интеграционный путь не полностью документирован, поэтому перед запуском в продакшн следует оценить зависимости и затраты на настройку.

### 中文

**项目简介（2‑3 句）**  
nextcloud/passman 是一款开源密码管理器，专为 Nextcloud 环境设计，支持在云端安全保存、共享和自动填充密码。它通过 Nextcloud 应用框架实现数据同步和访问控制，适合团队内部或个人的密码管理需求。

**价值**  
- **统一管理**：所有密码统一存储在 Nextcloud，利用已有的用户、权限和文件同步机制，无需额外的服务。  
- **安全可审计**：数据加密存储，且所有操作都有 Nextcloud 的审计日志，可满足合规要求。  
- **开源透明**：社区维护、可自行审计代码，避免供应链黑箱。

**典型接入方式**  
1. **在 Nextcloud 实例中安装**：通过 Nextcloud 应用市场或手动上传 `passman` 应用，启用后即可在用户界面中看到密码管理入口。  
2. **API/CLI 集成**：Passman 暴露 REST API，可在自定义脚本或 CI/CD 流程中调用，实现自动生成或更新凭据。  
3. **浏览器插件**：配合官方或社区提供的浏览器扩展，实现网页自动填充，提升使用体验。  
4. **小范围 PoC**：在测试环境先部署一两个用户，验证同步、加密和权限配置是否符合业务流程，再推广到全员。

**生产可用性**  
- **成熟度**：已有 800+ 星、100+ Fork，最近一次更新在 2026‑06‑27，社区活跃度中等。  
- **适用场景**：适合内部原型、研发环境或中小团队的密码管理；对外部客户或高安全合规（如 PCI‑DSS）仍需额外审计和硬化。  
- **风险与准备**：  
  - 依赖 Nextcloud 版本，需要确认当前平台兼容性。  
  - 部署前需评估加密密钥管理、备份恢复流程以及用户权限模型。  
  - 生产环境建议开启 HTTPS、双因素认证，并定期审计代码和依赖库。  

综上，nextcloud/passman 在已有 Nextcloud 基础设施的组织中，可快速实现统一密码管理，适合作为内部原型或中等规模生产使用，但在正式上线前需完成安全评估和运维准备。

## 🧭 Practical evaluation

**Value:** nextcloud/passman may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 821 GitHub stars
- 114 forks
- updated 2026-06-27
- primary language: JavaScript
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 52/100 |
| stars | 62/100 |
| topics | 50/100 |
| outlook | 69/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 59/100 |
| production | 65/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/nextcloud/passman) · [← Back to Misc](./README.md)</sub>
