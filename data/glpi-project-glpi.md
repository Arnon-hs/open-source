# glpi-project/glpi

[![Stars](https://img.shields.io/github/stars/glpi-project/glpi?style=flat-square&color=yellow)](https://github.com/glpi-project/glpi/stargazers) [![Forks](https://img.shields.io/github/forks/glpi-project/glpi?style=flat-square&color=blue)](https://github.com/glpi-project/glpi/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> GLPI is a Free Asset and IT Management Software package, Data center management, ITIL Service Desk, licenses tracking and software auditing.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 6k |
| 🍴 **Forks** | 1.7k |
| 💻 **Language** | PHP |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`asset-manager` `assets-management` `cmdb` `data-center` `dcim` `glpi` `hacktoberfest` `helpdesk` `impact-analysis` `inventory` `itam` `itil`

## 🎯 Categories

Data

## 📝 Summary

### English

**Brief Summary**  
GLPI (glpi‑project/glpi) is an open‑source IT asset and service‑desk platform that combines inventory, data‑center management, ITIL‑based ticketing, license tracking, and software audit capabilities. With a large community (6 k+ stars) and active development, it can serve as the backbone for searchable, analyzable IT data pipelines and automated reporting workflows.

**Value**  
- Turns raw inventory and service‑desk data into a structured, searchable repository, enabling dashboards, compliance reports, and automated alerts.  
- Provides built‑in ITIL processes, so organizations can standardise incident, problem, and change management without buying a commercial ITSM suite.  
- Extensible via plugins and a REST API, allowing integration with monitoring tools, CMDBs, or custom analytics pipelines.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Deploy the official Docker image or quick‑install script in a sandbox environment; follow the README to get the web UI up and import a small sample of assets.  
2. **Integration Pilot** – Connect GLPI to an existing LDAP/Active Directory for user sync, enable the REST API, and build a simple script that pulls asset data into your analytics stack (e.g., PowerBI, Grafana, or a Python ETL).  
3. **Scale‑up** – Harden the deployment (HTTPS, backup strategy, role‑based access), enable the plugin ecosystem (e.g., FusionInventory for auto‑discovery), and migrate production data in phases.

**Production Readiness**  
GLPI scores high on readiness: recent commits (as of 2026‑06‑24), a vibrant ecosystem, and widespread adoption in enterprises and public sector organisations. The PHP codebase is mature, and the project maintains regular releases and security patches. The main risk lies in the integration effort—documentation for complex pipelines is sparse—so a small‑scale trial is advisable before committing to a full‑scale rollout.

### Русский

GLPI (glpi-project/glpi) — это открытая система управления ИТ‑активами и сервис‑деском, позволяющая централизованно вести учёт оборудования, лицензий и программ, а также автоматизировать аналитические и отчётные пайплайны. Типичный сценарий внедрения — развёртывание небольшого proof‑of‑concept в тестовой среде, интеграция с существующими базами данных и построение автоматизированных отчётов, после чего система масштабируется до полного production‑использования. Проект обладает высокой готовностью к продакшн: активная разработка, более 6 000 звёзд на GitHub, регулярные обновления и широкая экосистема, однако требуется уточнить детали интеграции и оценить затраты на начальную настройку.

### 中文

**简短介绍**  
GLPI（glpi-project/glpi）是一款开源的资产与 IT 管理平台，涵盖数据中心管理、ITIL 服务台、许可证追踪和软件审计等功能。它能够把散落的 IT 资产数据统一收集、归类并提供可搜索、可分析的视图，帮助企业构建自动化的运维和报表流水线。

**价值**  
- **统一资产视图**：将硬件、软件、网络设备、许可证等信息集中管理，避免信息孤岛。  
- **提升运营效率**：内置 ITIL 流程（工单、变更、问题管理）和自定义工作流，可实现自动化审批、通知和报告生成。  
- **数据驱动决策**：提供丰富的查询、过滤和导出功能，支持将资产数据直接喂入 BI 或监控系统进行分析。  

**典型接入方式**  
1. **直接部署**：在公司内部服务器或容器（Docker、Kubernetes）上部署 GLGLPI，使用其自带的 MySQL/MariaDB 数据库。  
2. **API 集成**：通过 RESTful API（/apirest.php）读取或写入资产、工单、许可证等数据，适用于已有的 CMDB、监控或报表系统。  
3. **插件扩展**：利用官方或社区插件（如 LDAP、Active Directory、FusionInventory）实现自动发现和同步资产。  
4. **小规模 PoC**：先在测试环境部署，使用 README 中的快速启动脚本（docker‑compose）验证功能，再逐步迁移生产数据。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑24，项目拥有 6032 星、1712 Fork，最近一次提交仅数天前，表明社区维护积极。  
- **成熟生态**：提供完整的文档、Docker 镜像、官方插件以及多语言支持，适合企业级部署。  
- **风险提示**：虽然功能完整，但完整的集成路径（如与现有 CMDB、监控平台的对接）需要自行设计和测试，建议先进行小规模概念验证（PoC）并评估部署、备份、升级成本。  

综合来看，GLPI 具备高生产就绪度，适合作为企业资产与 IT 服务管理的核心平台，并可通过 API 与数据分析或自动化流水线无缝对接。

## 🧭 Practical evaluation

**Value:** glpi-project/glpi helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 6032 GitHub stars
- 1712 forks
- updated 2026-06-24
- primary language: PHP
- 15 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 81/100 |
| stars | 80/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 86/100 |
| recency | 80/100 |
| adoption | 81/100 |
| production | 72/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/glpi-project/glpi) · [← Back to Data](./README.md)</sub>
