# cBioPortal/cbioportal

[![Stars](https://img.shields.io/github/stars/cBioPortal/cbioportal?style=flat-square&color=yellow)](https://github.com/cBioPortal/cbioportal/stargazers) [![Forks](https://img.shields.io/github/forks/cBioPortal/cbioportal?style=flat-square&color=blue)](https://github.com/cBioPortal/cbioportal/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> cBioPortal for Cancer Genomics

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1k |
| 🍴 **Forks** | 861 |
| 💻 **Language** | Java |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-07-06 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cancer-genomics` `precision-medicine` `science` `visualization`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
cBioPortal is an open‑source web platform for visualizing, analyzing, and sharing cancer genomics data. It provides interactive dashboards, mutation/clinical query tools, and integration with public datasets such as TCGA, making it a go‑to resource for researchers and clinicians who need to explore large‑scale cancer genomics studies. With a mature Java codebase, active community contributions, and recent updates (as of July 2026), it can serve as a solid foundation for internal data portals or prototype analytics pipelines.

**Value**  
- **Domain‑specific functionality**: Pre‑built visualizations (oncoprints, mutation maps, survival plots) and cohort‑level query engines eliminate the need to develop custom bioinformatics dashboards from scratch.  
- **Data integration**: Supports import of standard formats (MAF, VCF, clinical XML/TSV) and can be linked to external APIs, enabling rapid ingestion of institutional sequencing results alongside public datasets.  
- **Community & extensibility**: Over 1 000 stars and a large fork base indicate active maintenance; plugins and a REST API allow extensions for downstream analysis or integration with other tools (e.g., Jupyter, R/Shiny).

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, run the Docker compose stack, and load a small public dataset (e.g., a TCGA cohort) following the README. Verify that the UI and API meet your exploratory needs.  
2. **Pilot integration** – Build a custom data‑import pipeline to translate your internal variant/clinical files into the portal’s schema; use the REST endpoints to embed portal visualizations into an existing internal portal or notebook environment.  
3. **Scale & harden** – Containerize the service for Kubernetes, configure persistent storage, enable LDAP/OAuth for authentication, and set up automated backups of the MySQL/PostgreSQL backend.  

**Production Readiness**  
- **Maturity**: Medium. The platform is battle‑tested in many academic and industry settings, but it is primarily designed as a research portal rather than a turnkey clinical decision‑support system.  
- **Dependencies**: Java, Maven, MySQL/PostgreSQL, and a set of front‑end libraries; all are well‑supported, but version alignment should be verified before deployment.  
- **Maintenance**: Regular upstream releases (last commit July 2026) reduce technical debt, yet you’ll need to allocate resources for security patching, database migrations, and monitoring of the web service.  

Overall, cBioPortal offers high immediate value for prototyping and internal analytics, with a clear, incremental path to production if you invest in proper container orchestration, authentication, and ongoing maintenance.

### Русский

cBioPortal — это открытая платформа для визуализации и анализа онкологических геномных данных, позволяющая исследователям быстро исследовать мутации, копийные изменения и клинические характеристики пациентов через веб‑интерфейс. Для внедрения обычно достаточно развернуть контейнер/VM с предустановленным сервером, подключить собственные наборы данных и интегрировать API в аналитический пайплайн, начиная с небольшого прототипа, чтобы проверить совместимость с текущей инфраструктурой. Готовность к production умеренная: проект стабилен и активно поддерживается (1020 звёзд, недавние коммиты), но требует проверки зависимостей, настройки безопасности и планового обслуживания перед использованием в критически важных продукционных системах.

### 中文

**价值**  
cBioPortal 是癌症基因组学领域的旗舰可视化与分析平台，能够快速查询、展示和比较 TCGA、ICGC 等大型肿瘤数据集的突变、拷贝数、表达、临床特征等信息。它为科研人员、临床医生以及药物研发团队提供“一站式”交互式探索环境，帮助发现潜在的驱动基因、关联突变和患者分层方案，从而加速生物标志物发现和精准治疗的设计。

**典型接入方式**  

| 场景 | 接入方式 | 关键步骤 |
|------|----------|----------|
| **内部原型 / 数据探索** | 直接克隆源码，使用 Docker Compose 或官方提供的 `docker-compose.yml` 启动完整服务（包括 PostgreSQL、cBioPortal 前后端） | 1. `git clone https://github.com/cBioPortal/cbioportal.git` <br>2. `cd cbioportal` <br>3. `docker compose up -d` <br>4. 将本地或公开的癌症数据（MAF、CNV、表达矩阵等）放入 `data/` 并在 `config` 中配置 `study.xml` | 
| **业务系统嵌入** | 通过 REST API（`/api/`）或 GraphQL（自 2025 版起支持）调用查询结果，或使用 Java SDK（`cbioportal-client`）在后端服务中直接访问 | 1. 在已有的微服务中添加 `cbioportal-client` 依赖 <br>2. 配置 API 访问凭证 <br>3. 调用如 `getMutationsByGene(studyId, geneSymbol)` 获取结构化数据，后自行渲染或与业务报表集成 |
| **自定义前端** | 利用开源的 React 组件库（`@cbioportal/ui`）或直接复用 `portal-frontend` 中的 UI 组件，实现专属仪表盘 | 1. `npm i @cbioportal/ui` <br>2. 按需引入 `MutationTable`, `OncoPrint`, `SurvivalPlot` 等组件 <br>3. 通过后端 API 注入项目自己的数据集 |

**生产可用性**  

- **成熟度**：GitHub ★1020，活跃维护（最近一次提交 2026‑07‑06），拥有完整的 CI/CD、单元/集成测试以及详细的部署文档。  
- **部署难度**：中等。官方提供的 Docker Compose 方案可在 10 分钟内部署完整环境；在 Kubernetes 环境下可使用 Helm chart（社区维护）进行弹性扩容。  
- **运维要求**：需要监控 PostgreSQL（或 MariaDB）存储容量、定期备份数据集、以及前端/后端服务的日志与健康检查。对安全合规有要求的组织应自行实现 LDAP/OIDC 鉴权（平台已提供插件）。  
- **适用场景**：  
  - **原型/内部分析**：直接使用官方镜像即可快速上线，几乎不需要额外开发。  
  - **生产系统**：在完成以下工作后可投入生产：① 数据质量与标准化（MAF/VCF、CNV、表达矩阵统一格式）；② 鉴权与审计日志集成；③ 高可用部署（多副本 DB + 负载均衡）；④ 定期安全补丁更新。  

综上，cBioPortal 在癌症基因组学的数据探索与可视化方面价值突出，接入方式灵活（Docker、API、前端组件），在完成基本运维准备后即可达到生产级别，适合作为内部科研平台或面向客户的基因组报告系统的核心组件。

## 🧭 Practical evaluation

**Value:** cBioPortal/cbioportal may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1020 GitHub stars
- 861 forks
- updated 2026-07-06
- primary language: Java
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 73/100 |
| stars | 64/100 |
| topics | 50/100 |
| outlook | 75/100 |
| quality | 77/100 |
| recency | 100/100 |
| adoption | 67/100 |
| production | 73/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/cBioPortal/cbioportal) · [← Back to Misc](./README.md)</sub>
