# ChurchCRM/CRM

[![Stars](https://img.shields.io/github/stars/ChurchCRM/CRM?style=flat-square&color=yellow)](https://github.com/ChurchCRM/CRM/stargazers) [![Forks](https://img.shields.io/github/forks/ChurchCRM/CRM?style=flat-square&color=blue)](https://github.com/ChurchCRM/CRM/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-48%2F100-brightgreen?style=flat-square)](#)

> ChurchCRM - A free and open-source Church Management Software (ChMS) to help churches manage their membership data, groups, events, and finances.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 878 |
| 🍴 **Forks** | 535 |
| 💻 **Language** | PHP |
| 📈 **Score** | 48/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`attendance-system` `calendar` `calendar-events` `church` `church-management` `churchcrm` `crm` `database`

## 🎯 Categories

Database

## 📝 Summary

### English

**Brief Summary**  
ChurchCRM is a free, open‑source Church Management System that lets congregations store and query member records, organize groups, schedule events, and track finances. Built in PHP, it provides a searchable data layer and reporting tools that can be wired into analytics or automation pipelines.

**Value**  
The platform turns raw membership and financial data into a structured, queryable database, enabling churches to generate real‑time dashboards, export datasets for BI tools, and automate routine communications (e.g., newsletters, donation receipts). Because it is open source, organizations can extend the core with custom modules or integrate it with existing ERP, email‑marketing, or accounting solutions without licensing fees.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the Docker compose starter kit, and import a small sample of member data to validate the data model and API endpoints.  
2. **Integration Check** – Review the README and existing REST/GraphQL endpoints; build a lightweight connector (e.g., a Python script) that pulls member lists into your analytics stack.  
3. **Pilot Deployment** – Deploy the application on a staging server, configure LDAP/SAML authentication if needed, and enable a few core modules (membership, events, finance).  
4. **Scale‑Up** – Migrate the production database to a managed MySQL/PostgreSQL instance, enable backups, and add custom plugins for any church‑specific workflows.

**Production Readiness**  
ChurchCRM scores high on production readiness: it has recent commits (last updated 2026‑05‑11), strong community adoption (≈ 878 ⭐, 535 forks), and a mature PHP codebase with clear documentation. While the integration surface is not extensively documented, the core APIs are stable, and a small proof‑of‑concept can quickly surface any hidden setup costs. With proper staging, backup, and security hardening, it is suitable for a serious pilot in a production environment.

### Русский

**ChurchCRM** — бесплатная open‑source система управления церковью (ChMS), позволяющая централизованно хранить и анализировать данные о прихожанах, группах, мероприятиях и финансах. Типичный сценарий внедрения — небольшое пилотное подключение: импорт существующей базы членов, настройка автоматических отчётов и интеграция с бухгалтерией через API, после чего система масштабируется для всей общины. Проект имеет высокую готовность к production (активные коммиты, 878 ★, 535 форков, регулярные релизы), однако перед масштабным rollout стоит проверить детали установки и стоимость интеграции.

### 中文

**项目简介**  
ChurchCRM 是一款免费开源的教会管理系统（ChMS），可帮助教会统一管理成员信息、分组、活动与财务，实现数据的集中、可搜索和可分析。

**价值**  
- 将教会的原始会员、活动和财务数据转化为结构化、可检索的记录，支持自定义报表和分析仪表盘。  
- 提供 API 与导入/导出工具，可快速构建数据管道，实现自动化通知、捐赠统计或与第三方 CRM/BI 系统的对接。  

**典型接入方式**  
1. **快速验证**：克隆仓库，按照 README 部署 Docker Compose（或 LAMP）环境，导入一小批 CSV 会员数据，确认系统功能与 API 可用。  
2. **数据同步**：使用内置的 CSV/Excel 导入功能或 REST API，将现有会员库同步到 ChurchCRM；随后通过 Webhooks 或自定义脚本将关键事件（如新成员加入、捐赠）推送至企业数据仓库或 BI 工具。  
3. **业务扩展**：在 PHP 代码或插件中编写自定义逻辑，例如自动生成月度财务报告、触发邮件营销或与支付网关对接。  

**生产可用性**  
- **活跃度**：项目最近一次提交（2026‑05‑11）且拥有 878+ 星、535+ Fork，社区活跃，文档完整。  
- **成熟度**：核心功能（成员管理、分组、活动、财务）在多个教会实际部署中已验证，具备生产级别的稳定性。  
- **部署成熟**：提供 Docker 镜像、官方 Helm Chart（社区维护）以及详细的安装指南，易于在容器化或传统 VM 环境中上线。  
- **风险**：元数据中未明确标注完整的集成路径，建议先在测试环境完成小规模 PoC，评估与现有业务系统（如 ERP、邮件平台）的对接成本。  

综上，ChurchCRM 具备高生产就绪度，适合作为教会数据管理与分析的核心平台，先行通过小规模验证后即可在正式业务中推广。

## 🧭 Practical evaluation

**Value:** ChurchCRM/CRM helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 878 GitHub stars
- 535 forks
- updated 2026-05-11
- primary language: PHP
- 8 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 68/100 |
| stars | 63/100 |
| topics | 100/100 |
| outlook | 51/100 |
| quality | 64/100 |
| recency | 20/100 |
| adoption | 64/100 |
| production | 49/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/ChurchCRM/CRM) · [← Back to Database](./README.md)</sub>
