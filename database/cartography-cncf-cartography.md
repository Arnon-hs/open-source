# cartography-cncf/cartography

[![Stars](https://img.shields.io/github/stars/cartography-cncf/cartography?style=flat-square&color=yellow)](https://github.com/cartography-cncf/cartography/stargazers) [![Forks](https://img.shields.io/github/forks/cartography-cncf/cartography?style=flat-square&color=blue)](https://github.com/cartography-cncf/cartography/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> Cartography is a Python tool that pulls infrastructure assets and their relationships into a Neo4j graph database.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.9k |
| 🍴 **Forks** | 527 |
| 💻 **Language** | Python |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Database

## 📝 Summary

### English

**Brief Summary**  
Cartography is a Python‑based utility that discovers cloud and on‑premise infrastructure assets, maps their relationships, and loads the resulting model into a Neo4j graph database. It enables teams to turn raw inventory data into a searchable, queryable graph that can drive analytics, reporting, and automation pipelines.

**Value**  
By converting disparate infrastructure metadata into a unified graph, Cartography makes it easy to answer “what‑if” and dependency questions, trace resource lineage, and feed downstream security or cost‑optimization tools. The graph format supports powerful Cypher queries and visualizations, turning otherwise static inventories into actionable insights for DevOps, SRE, and governance teams.

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | **Pilot on a limited environment** – run the provided discovery plugins (AWS, GCP, Azure, Kubernetes, etc.) against a sandbox account. | Validates connectivity, permissions, and data quality without affecting production. |
| 2️⃣  | **Inspect the generated graph** – use Neo4j Browser or Bloom to review node/relationship completeness and identify missing tags or custom attributes. | The project’s integration signals are sparse, so manual verification ensures the model meets your use‑case. |
| 3️⃣  | **Enrich & customize** – add custom discovery scripts or post‑processing Cypher to capture organization‑specific resources (e.g., internal services, on‑prem DBs). | Extends the out‑of‑the‑box schema to fit your ecosystem. |
| 4️⃣  | **Integrate with downstream pipelines** – connect the Neo4j instance to analytics notebooks, alerting systems, or CI/CD checks that query the graph. | Realizes the promised “searchable, analyzable, automated pipelines.” |
| 5️⃣  | **Scale & harden** – provision a production‑grade Neo4j cluster, enable role‑based access, and set up regular discovery jobs (cron or Airflow). | Moves the prototype into a reliable, repeatable production workflow. |

**Production Readiness**  
Cartography sits at a **medium** readiness level. It is mature enough (≈4 k stars, active recent commits) for internal prototypes and controlled production use, but you should perform the following before full rollout:

* **Dependency audit** – verify that all required Python packages and Neo4j driver versions are compatible with your environment.  
* **Security review** – scan the codebase and any third‑party plugins for known vulnerabilities; ensure the Neo4j instance is hardened and network‑isolated.  
* **Maintenance plan** – track upstream releases (the project is actively maintained) and allocate ownership for periodic updates and custom plugin upkeep.  

With these checks in place, Cartography can become a reliable backbone for infrastructure graph analytics and automation in production settings.

### Русский

Cartography — это Python‑утилита, которая собирает сведения об инфраструктурных ресурсах и их взаимосвязях и сохраняет их в графовой базе Neo4j, что позволяет быстро выполнять поиск, аналитику и строить автоматизированные пайплайны. Типичное внедрение — создание внутреннего прототипа или аналитического пайплайна, где данные сначала собираются, затем проверяются вручную и только после этого интегрируются в более крупные процессы отчётности и мониторинга. Готовность к production — средняя: проект достаточно зрелый (3945 звёзд, активные коммиты), но требует проверки зависимостей, лицензии и безопасности, а также ручной валидации обнаруженных метаданных перед широким использованием.

### 中文

**项目简介**  
Cartography 是 CNCF 旗下的开源 Python 工具，可自动发现云、容器、Kubernetes 等基础设施资产及其相互关系，并将这些信息写入 Neo4j 图数据库，帮助团队把散落的原始数据转化为可搜索、可分析、可用于自动化的结构化图谱。

**价值**  
- **统一视图**：把分散在不同平台的资源统一映射到图数据库，实现跨系统的关联查询。  
- **加速分析**：基于图谱的拓扑结构，可快速进行依赖分析、攻击面评估和容量规划。  
- **支持自动化**：图数据可直接驱动 CI/CD、合规审计和安全检测等流水线。

**典型接入方式**  
1. **环境准备**：部署 Neo4j（本地或云托管），确保 Python 运行环境满足 `requirements.txt`。  
2. **配置数据源**：在 `cartography.config` 中填写云提供商（AWS、GCP、Azure）或 Kubernetes 的凭证。  
3. **运行采集**：执行 `cartographyctl sync`，工具会调用相应 API 拉取资产并写入 Neo4j。  
4. **后续使用**：通过 Neo4j 浏览器或 Cypher 查询语句，或在自建的 BI/安全平台中集成图数据。

**生产可用性**  
- **成熟度**：Medium。已拥有 3,945+ 星、527+ Fork，活跃社区，适合作为原型或内部业务流程的核心组件。  
- **使用前注意**：当前发现的元数据中关联信号较少，建议在正式上线前进行手动审查和补充标签，以确保图谱完整性。  
- **运维要求**：需要定期检查 Neo4j 的备份、升级以及 Cartography 的依赖库安全性；若在生产环境使用，建议加入 CI 检查和版本锁定。  

总体而言，Cartography 能帮助企业快速构建基础设施图谱，提升可观测性与自动化水平，但在生产环境部署前需做好元数据质量校验和运维保障。

## 🧭 Practical evaluation

**Value:** cartography-cncf/cartography helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 3945 GitHub stars
- 527 forks
- updated 2026-06-29
- primary language: Python

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 68/100 |
| stars | 77/100 |
| topics | 0/100 |
| outlook | 54/100 |
| quality | 58/100 |
| recency | 40/100 |
| adoption | 74/100 |
| production | 54/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/cartography-cncf/cartography) · [← Back to Database](./README.md)</sub>
