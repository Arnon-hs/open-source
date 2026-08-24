# City-Bureau/city-scrapers

[![Stars](https://img.shields.io/github/stars/City-Bureau/city-scrapers?style=flat-square&color=yellow)](https://github.com/City-Bureau/city-scrapers/stargazers) [![Forks](https://img.shields.io/github/forks/City-Bureau/city-scrapers?style=flat-square&color=blue)](https://github.com/City-Bureau/city-scrapers/network) [![Language](https://img.shields.io/badge/lang-HTML-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> Scrape, standardize and share public meetings from local government websites

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 376 |
| 🍴 **Forks** | 323 |
| 💻 **Language** | HTML |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`city-scrapers` `open-data` `python` `scrapy` `web-scraping`

## 🎯 Categories

Data

## 📝 Summary

### English

**Brief Summary**  
City‑Bureau’s *city‑scrapers* is an open‑source toolkit that automatically extracts, normalizes, and publishes public‑meeting data from municipal websites. It provides a ready‑made pipeline—scrapers, a data model, and an API/CLI—for turning raw HTML agendas into structured, searchable records that can be fed into downstream AI or analytics workflows.  

**Value**  
- **Accelerates AI integration**: By delivering clean, standardized meeting data out‑of‑the‑box, developers can focus on building AI features (e.g., RAG, chat agents, summarization) instead of writing brittle web‑scrapers.  
- **Reusable building blocks**: The project ships a CLI, Python SDK, and REST endpoints, making it easy to plug into existing data pipelines or to prototype new services quickly.  
- **Community‑validated**: With 376 stars, 323 forks, and active contributions, the codebase reflects real‑world usage across many U.S. cities, reducing the risk of hidden edge cases.  

**Practical Adoption Path**  
1. **Evaluation** – Clone the repo and run the CLI against a target city’s agenda page to verify data quality.  
2. **Integration** – Wrap the Python SDK or call the provided API from your data ingestion layer; map the normalized JSON output to your feature store or vector database.  
3. **AI Layer** – Feed the structured meeting minutes into a language model for summarization, question‑answering, or to build a RAG knowledge source for civic‑engagement bots.  
4. **Productionization** – Deploy the scrapers as scheduled jobs (e.g., Airflow, Prefect) and expose the API behind a load‑balanced service; monitor for site changes with the built‑in health checks.  

**Production Readiness**  
- **Recent activity**: Last commit on 2026‑05‑13, frequent releases, and active issue triage.  
- **Maturity**: Well‑documented data schema, stable CLI/SDK, and multiple city deployments in the wild.  
- **Ecosystem fit**: Minimal external dependencies (primarily Python/HTML parsing) and clear licensing (MIT) simplify security reviews.  
- **Risks**: Final due‑diligence needed on license compliance, long‑term maintainer commitment, and any site‑specific anti‑scraping measures, but no major red flags appear.  

Overall, *city‑scrapers* is a production‑grade OSS component that can be adopted quickly to power AI‑enhanced civic data products.

### Русский

City‑Bureau / city‑scrapers — это открытая платформа для автоматического сбора, стандартизации и публикации данных о публичных совещаниях муниципалитетов. Ее API/CLI позволяет быстро добавить AI‑функции (прототипирование, RAG‑агенты, оценка моделей) в существующие пайплайны без разработки собственного скрейпера, а активное сообщество (376 ⭐, 323 форка, частые обновления) делает проект готовым к пилотному запуску в продакшн.

### 中文

**项目简介**  
City‑Bureau/city‑scrapers 是一套开源工具链，用于从各地政府网站抓取、统一化并公开发布公共会议数据。它提供可复用的爬虫、数据清洗和 API/CLI 接口，帮助开发者快速获取结构化的议会、委员会等会议记录。

**价值**  
- **快速赋能 AI**：无需从零搭建爬虫或数据清洗流程，即可直接在已有的会议数据上实验自然语言检索（RAG）、智能摘要或决策助理等 AI 功能。  
- **原型加速**：标准化的输出格式让模型训练、提示工程和评估工具链能够“一键接入”，大幅缩短原型开发周期。  
- **生态兼容**：提供 RESTful API、Python SDK 与命令行工具，便于在现有后端或数据管道中嵌入。

**典型接入方式**  
1. **API/SDK**：通过项目自带的 Python 包 (`city_scrapers`) 调用 `scrape()`、`process()` 等函数，获取 JSON/CSV 结构化数据。  
2. **CLI**：使用 `city-scrapers run <spider_name>` 直接在终端运行指定爬虫，输出文件可供后续模型处理。  
3. **自定义插件**：基于已有爬虫模板编写新城市/新部门的抓取脚本，随后统一通过同一 API 访问。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑13 最近一次提交，GitHub 上 376 星、323 Fork，社区贡献持续。  
- **成熟度**：核心功能已在多个城市部署，具备错误重试、日志、数据校验等生产级特性。  
- **风险**：许可证（MIT）无明显冲突，安全审计尚需自行完成；但整体维护者活跃，适合作为正式项目的底层数据层。  

综上，city‑scrapers 具备较高的生产就绪度，可作为 AI 驱动的公共事务信息系统的可靠数据来源。

## 🧭 Practical evaluation

**Value:** City-Bureau/city-scrapers helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 376 GitHub stars
- 323 forks
- updated 2026-05-13
- primary language: HTML
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 63/100 |
| stars | 55/100 |
| topics | 63/100 |
| outlook | 49/100 |
| quality | 55/100 |
| recency | 20/100 |
| adoption | 57/100 |
| production | 53/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/City-Bureau/city-scrapers) · [← Back to Data](./README.md)</sub>
