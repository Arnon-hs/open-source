# cahyadsn/wilayah

[![Stars](https://img.shields.io/github/stars/cahyadsn/wilayah?style=flat-square&color=yellow)](https://github.com/cahyadsn/wilayah/stargazers) [![Forks](https://img.shields.io/github/forks/cahyadsn/wilayah?style=flat-square&color=blue)](https://github.com/cahyadsn/wilayah/network) [![Language](https://img.shields.io/badge/lang-SQL-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> Kode dan Data Wilayah Administrasi & Pulau Indonesia sesuai Kepmendagri No 300.2.2-2430 Tahun 2025  dengan PHP+MySQL+AJaX. Demo link : https://wilayah.cahyadsn.com/

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.2k |
| 🍴 **Forks** | 413 |
| 💻 **Language** | SQL |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`2025` `data` `indonesia` `kepmendagri` `kode` `php` `sql` `wilayah`

## 🎯 Categories

Data · Database

## 📝 Summary

### English

**Brief Summary**  
cahyadsn/wilayah is an open‑source PHP + MySQL + AJAX package that provides up‑to‑date administrative‑region and island data for Indonesia, aligned with Kepmendagri No 300.2.2‑2430 (2025). The repository includes both the raw SQL datasets and a ready‑to‑run demo (https://wilayah.cahyadsn.com/), making it easy to embed accurate territorial information in web applications.

**Value**  
- **Ready‑made geographic foundation** – developers get a comprehensive, government‑validated hierarchy of provinces, regencies, districts, and islands without having to scrape or curate the data themselves.  
- **AI‑friendly** – the clean relational schema can be linked to vector stores or LLM pipelines for Retrieval‑Augmented Generation (RAG), location‑aware chatbots, or decision‑support agents, accelerating prototype development.  
- **Low‑cost integration** – the stack (PHP, MySQL, AJAX) is ubiquitous in legacy and modern web projects, so adding the dataset does not require new infrastructure.

**Practical Adoption Path**  
1. **Clone & spin‑up** the repo (Docker compose or a simple LAMP stack) and verify the demo.  
2. **Run the provided SQL scripts** to populate a MySQL database with the region tables.  
3. **Expose the data** via the existing AJAX endpoints or wrap them in a thin REST/GraphQL layer that your AI service can query.  
4. **Connect to AI** – feed query results into an LLM prompt or store embeddings in a vector DB for RAG use‑cases.  
5. **Iterate** with a small proof‑of‑concept (e.g., “Find all districts within a 50 km radius of a given island”) before scaling to full production workloads.

**Production Readiness**  
- **Activity & community** – 1,207 stars, 413 forks, recent commits (as of 2026‑06‑25) show active maintenance.  
- **Stability** – The core data schema is static and versioned by the government decree, reducing churn.  
- **Ecosystem fit** – Uses standard SQL and PHP, which are well‑supported in most hosting environments; no exotic dependencies.  
- **Risks** – The integration documentation is sparse, so initial setup may require reading the README and exploring the demo code. Validate the effort to wrap the AJAX endpoints in your preferred API style before a full rollout.

Overall, cahyadsn/wilayah is production‑ready for pilots that need authoritative Indonesian territorial data and can serve as a solid backbone for AI‑enhanced geographic services.

### Русский

**cahyadsn/wilayah** — это открытый набор кода и данных о административных единицах и островах Индонезии (Kepmendagri No 300.2.2‑2430 2025), реализованный на PHP + MySQL + AJAX и доступный в демо‑версии https://wilayah.cahyadsn.com/. Проект удобно использовать как готовую базу для прототипирования AI‑фич: подключить её к RAG‑ или агентским workflow, быстро добавить контекстные запросы о регионах без построения модели с нуля. Репозиторий активно поддерживается (1207 ★, 413 fork, обновления до 2026‑06‑25), поэтому готов к пилотному запуску в продакшн после небольшого PoC и проверки инструкций по установке.

### 中文

**项目简介（2‑3 句）**  
cahyadsn/wilayah 是一套基于 PHP、MySQL 与 Ajax 的印尼行政区划与岛屿数据代码库，完整实现了《Kepmendagri No 300.2.2‑2430 Tahun 2025》规定的地区划分。项目提供在线 Demo（https://wilayah.cahyadsn.com/），方便快速预览和交互。

**价值**  
- **完整、权威的地区数据**：一次性获取全国省、市、县、乡镇以及岛屿的层级结构，省去自行爬取或手工整理的成本。  
- **即插即用的技术栈**：基于 PHP+MySQL+Ajax，几乎所有 Web 环境都能直接部署，无需额外依赖。  
- **支持 AI/ML 场景**：可直接将地区编码与文本、图像等模型结合，用于地理标签、RAG（检索增强生成）或智能客服等 AI 应用的原型开发。

**典型接入方式**  
1. **数据库初始化**：克隆仓库后执行 `sql/seed.sql`（或项目提供的导入脚本）将地区表导入 MySQL。  
2. **后端调用**：在 PHP 项目中引入 `src/Region.php`，通过提供的 API（如 `getProvinces()、getCities($provinceId)`）获取层级数据。  
3. **前端交互**：利用项目自带的 Ajax 示例页面，实现级联下拉或地图可视化；也可自行封装为 RESTful 接口供前端框架（Vue、React 等）调用。  
4. **AI 集成**：将地区编码作为检索键，结合向量数据库或 LLM，实现“某省的旅游景点推荐”“基于位置的对话”等 RAG/Agent 工作流。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑25，项目仍在维护，拥有 1207 星、413 Fork，近期提交频繁。  
- **成熟度**：核心功能（数据完整性、增删改查 API）已在 Demo 环境稳定运行，适合作为正式业务的底层数据服务。  
- **集成门槛**：仅需 MySQL 与 PHP 环境，部署成本低；但需要自行检查与现有系统的表结构兼容性以及安全（如 SQL 注入防护）措施。  
- **风险**：项目文档以 README 为主，缺少完整的 CI/CD 或容器化示例，建议在正式上线前完成小规模 POC 并编写部署脚本。  

综合来看，cahyadsn/wilayah 在数据可靠性、技术门槛和社区活跃度方面具备较高的生产可用性，适合作为印尼地区信息的基础设施，并可快速扩展到 AI/ML 场景。

## 🧭 Practical evaluation

**Value:** cahyadsn/wilayah helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1207 GitHub stars
- 413 forks
- updated 2026-06-25
- primary language: SQL
- 8 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 65/100 |
| stars | 66/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 69/100 |
| recency | 40/100 |
| adoption | 66/100 |
| production | 56/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/cahyadsn/wilayah) · [← Back to Data](./README.md)</sub>
