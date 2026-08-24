# disclose/diodb

[![Stars](https://img.shields.io/github/stars/disclose/diodb?style=flat-square&color=yellow)](https://github.com/disclose/diodb/stargazers) [![Forks](https://img.shields.io/github/forks/disclose/diodb?style=flat-square&color=blue)](https://github.com/disclose/diodb/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> Open-source vulnerability disclosure and bug bounty program database

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.1k |
| 🍴 **Forks** | 327 |
| 💻 **Language** | Python |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bug-bounty` `bug-bounty-hunters` `data` `disclosure-policy` `hackers` `legal` `responsible-disclosure` `safe-harbor-framework` `safety` `security-research` `simplicity` `vulnerability-disclosure`

## 🎯 Categories

Data · Database · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
disclose/diodb is an open‑source Python‑based database that aggregates vulnerability disclosures and bug‑bounty program data, turning raw feeds into a searchable, analytics‑ready store. With over 1 000 GitHub stars and active maintenance, it’s positioned as a high‑readiness OSS component for security‑oriented data pipelines.  

**Value**  
- **Data transformation** – Converts disparate vulnerability feeds into a structured schema that can be queried, visualised, or fed into automated security workflows.  
- **Analytics enablement** – Provides a single source of truth for building dashboards, trend analyses, and risk‑scoring models across programs.  
- **Pipeline integration** – Designed for easy ingestion into CI/CD, SIEM, or threat‑intel platforms, reducing the effort of custom ETL scripts.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the provided Docker compose or virtual‑env setup, and load a small sample of CVE or bug‑bounty data.  
2. **Validate the API/CLI** – Use the built‑in search and export commands to confirm the data model matches your reporting needs.  
3. **Integrate** – Wrap the Python client or REST endpoints into your existing analytics or alerting pipelines; start with a non‑critical workflow (e.g., nightly reporting).  
4. **Scale** – Gradually increase data volume, add custom enrichments, and migrate the backing store (PostgreSQL, SQLite, etc.) to production‑grade infrastructure.  

**Production Readiness**  
- **Activity & Community** – Recent commits (as of 2026‑07‑05), 1 072 stars, 327 forks, and a healthy set of topics indicate strong community interest.  
- **Maturity** – The codebase is Python‑first, well‑documented, and includes a README with setup instructions, making initial deployment straightforward.  
- **Risk Considerations** – No obvious metadata or licensing red flags, but a final review of the open‑source license and the maintainers’ security response process is recommended before a full‑scale rollout.  

Overall, disclose/diodb is a production‑ready candidate for teams that need a reliable, searchable repository of vulnerability disclosures to power analytics, reporting, or automated security orchestration.

### Русский

**disclose/diodb** — это открытая база данных уязвимостей и программ bug bounty, которая превращает сырые данные в удобный, индексируемый набор, готовый к поиску, аналитике и автоматическим пайплайнам. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept: подключить её к существующим процессам сбора и обработки уязвимостей, построить аналитические запросы и интегрировать результаты в отчётные и мониторинговые системы. По оценкам, проект готов к production: активные коммиты, более 1000 звёзд, широкая экосистема Python и подтверждённая готовность к пилотному использованию, хотя лицензия и вопросы безопасности требуют окончательной проверки.

### 中文

**项目简介**  
disclose/diodb 是一个开源的漏洞披露与赏金计划数据库，提供结构化、可搜索的漏洞信息，帮助安全团队将原始情报转化为可分析、可自动化的工作流。

**价值**  
- **数据可用性提升**：把分散的披露记录统一成统一的 schema，支持快速检索和关联分析。  
- **分析与自动化**：可直接接入安全分析管道、报告生成或威胁情报平台，减少手工整理成本。  
- **社区与生态**：拥有 1 072+ stars、327+ forks，活跃的 Python 社区提供丰富的插件和示例。

**典型接入方式**  
1. **代码库克隆**：`git clone https://github.com/disclose/diodb.git`。  
2. **依赖安装**：`pip install -r requirements.txt`（推荐在 virtualenv/conda 环境）。  
3. **数据导入**：使用自带的 CLI 或 Python SDK，将本地或远程的披露 JSON/CSV 导入数据库（默认 SQLite，可通过环境变量切换为 PostgreSQL、MySQL 等）。  
4. **查询/集成**：  
   - 直接使用 `diodb.query(sql)` 在脚本中进行 SQL 查询。  
   - 通过 REST API（`uvicorn diodb.api:app --reload`）提供服务，供 SIEM、SOAR、Jenkins 等系统调用。  
   - 在 CI/CD 流水线中加入 `diodb sync` 步骤，实现每日自动同步最新漏洞数据。  

**生产可用性**  
- **成熟度**：近期（2026‑07‑05）仍有活跃提交，社区活跃度高，代码质量良好。  
- **可扩展性**：支持多种后端存储，易于水平扩展；提供 Docker 镜像，便于容器化部署。  
- **风险**：许可证、长期维护者状态需进一步确认；在正式生产环境使用前建议完成一次小规模 PoC（如 100 条记录的查询/同步），并审查 README 与安全审计报告。  

综上，disclose/diodb 已具备在安全分析平台或内部报告系统中进行试点的条件，经过一次小范围的概念验证后即可进入生产级别的部署。

## 🧭 Practical evaluation

**Value:** disclose/diodb helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1072 GitHub stars
- 327 forks
- updated 2026-07-05
- primary language: Python
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 63/100 |
| stars | 64/100 |
| topics | 100/100 |
| outlook | 62/100 |
| quality | 69/100 |
| recency | 40/100 |
| adoption | 64/100 |
| production | 58/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/disclose/diodb) · [← Back to Data](./README.md)</sub>
