# frappe/hrms

[![Stars](https://img.shields.io/github/stars/frappe/hrms?style=flat-square&color=yellow)](https://github.com/frappe/hrms/stargazers) [![Forks](https://img.shields.io/github/forks/frappe/hrms?style=flat-square&color=blue)](https://github.com/frappe/hrms/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> Open Source HR and Payroll Software

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 8.1k |
| 🍴 **Forks** | 2.4k |
| 💻 **Language** | Python |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`attendance` `employee` `erpnext` `exits` `frappe` `frappe-framework` `hcm` `hr` `hris` `hrms` `javascript` `leave-management`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
frappe/hrms is an open‑source HR and payroll platform that lets teams ship user‑facing interfaces quickly by reusing a rich set of pre‑built UI components. Its strong community activity (8 k+ stars, 2.4 k forks, recent commits) and solid integration notes make it a viable candidate for a production pilot, especially for organizations looking to accelerate UI delivery without heavy custom front‑end work.  

**Value** – By providing ready‑made forms, tables, dashboards and workflow widgets, frappe/hrms cuts the amount of custom UI code developers must write, enabling faster product launches and more consistent user experiences.  

**Adoption path** – Start with a small proof‑of‑concept that follows the project’s README (e.g., spin up the demo site, connect to an existing database, and replace a single HR screen). Once the component fits the existing stack, incrementally replace other HR/Payroll pages, leveraging the same component library across the product.  

**Production readiness** – The project shows high readiness: recent activity (updated 2026‑06‑25), strong ecosystem signals, and a sizable contributor base. While a final check of licensing, security posture, and maintainer responsiveness is still required, the overall health and community support make frappe/hrms suitable for a serious pilot in production.

### Русский

**frappe/hrms** — это открытое HR‑ и payroll‑приложение, которое ускоряет создание пользовательских интерфейсов за счёт готовых UI‑компонентов и готовой бизнес‑логики. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept, интеграция через README и последующее расширение для полного продукта, позволяя быстрее вывести на рынок новые HR‑фичи. Проект считается почти готовым к продакшену: активные коммиты, 8 128 звёзд, 2 415 форков и сильная экосистема — остаётся лишь окончательная проверка лицензии, безопасности и поддержки мейнтейнеров.

### 中文

**项目简介**  
frappe/hrms 是一套开源的人力资源与薪酬管理系统，基于 Frappe 框架构建，提供完整的员工信息、考勤、假期、薪资等功能。它通过可复用的前端组件和统一的数据模型，让开发者能够快速搭建面向用户的 HR 界面，省去大量自定义 UI 的工作。

**价值**  
- **加速 UI 开发**：内置丰富的表单、列表、仪表盘等前端组件，可直接复用，显著缩短产品界面的交付周期。  
- **统一数据层**：基于 Frappe 的强大 ORM 与 REST API，前端与后端数据同步无缝，降低了数据一致性维护成本。  
- **生态共享**：作为 Frappe 生态的一部分，能够共享其他 Frappe 应用的插件、工作流和权限体系，提升整体开发效率。

**典型接入方式**  
1. **代码层面集成**：在已有的 Frappe/ERPNext 项目中通过 `bench get-app hrms` 安装，随后在 `bench install-app hrms` 完成注册，即可在现有站点上直接使用 HR 模块的 UI 与 API。  
2. **微服务/前端独立接入**：通过 HRMS 提供的 RESTful API（如 `/api/resource/Employee`、`/api/method/payroll.process`）在独立的前端框架（React、Vue 等）中调用，实现 UI 与后端的松耦合。  
3. **小规模 PoC**：先在本地或测试环境创建一个最小化站点，仅启用 `Employee`、`Attendance`、`Salary Slip` 等核心 DocType，验证业务流程后再逐步扩展。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑25，项目拥有 8,128+ 星、2,415+ Fork，近期仍在持续更新，社区活跃度和维护者响应速度均良好。  
- **成熟度**：已在多个企业级部署中使用，具备完整的权限、审计和多币种薪资计算能力，符合企业生产环境的基本要求。  
- **风险点**：需进一步审查许可证兼容性（MIT/AGPL 等）、安全补丁的及时性以及核心维护者的长期可用性。总体而言，frappe/hrms 已具备足够的可靠性，可作为正式生产环境的候选方案，建议先在非关键业务做小规模试点，确认后再全面推广。

## 🧭 Practical evaluation

**Value:** frappe/hrms helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 8128 GitHub stars
- 2415 forks
- updated 2026-06-25
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 85/100 |
| stars | 83/100 |
| topics | 100/100 |
| outlook | 80/100 |
| quality | 88/100 |
| recency | 80/100 |
| adoption | 84/100 |
| production | 74/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/frappe/hrms) · [← Back to Misc](./README.md)</sub>
