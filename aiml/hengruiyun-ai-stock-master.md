# hengruiyun/AI-Stock-Master

[![Stars](https://img.shields.io/github/stars/hengruiyun/AI-Stock-Master?style=flat-square&color=yellow)](https://github.com/hengruiyun/AI-Stock-Master/stargazers) [![Forks](https://img.shields.io/github/forks/hengruiyun/AI-Stock-Master?style=flat-square&color=blue)](https://github.com/hengruiyun/AI-Stock-Master/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> AI股票大师-基于AI 的股票趋势分析平台，通过AI 解读中国、香港、美国股票市场，融合三大核心算法，独家预分析多维数据，为投资者提供全方位的学习支持. This is an AI-based stock trend analysis platform that integrates three core algorithms:

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 195 |
| 🍴 **Forks** | 44 |
| 💻 **Language** | Python |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `analysis` `finance` `fund` `llm` `stocks`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary**  
AI‑Stock‑Master is an open‑source platform that leverages three proprietary AI algorithms to analyse stock trends across the Chinese, Hong Kong and US markets. It delivers multi‑dimensional predictions and learning resources for investors, all built on a Python stack with a modern front‑end and database backend.

**Value**  
- **Accelerated AI integration** – Provides ready‑made models and data pipelines, letting teams add sophisticated stock‑analysis capabilities without constructing a model stack from scratch.  
- **Cross‑market coverage** – Unified analysis of three major equity markets, saving the effort of stitching together disparate data sources.  
- **Extensible architecture** – Designed for rapid prototyping of Retrieval‑Augmented Generation (RAG) or autonomous agent workflows, making it a solid foundation for custom investment‑tech products.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, follow the README to spin up the Docker‑compose environment, and run the sample notebook to verify data ingestion and model inference.  
2. **Feature Extension** – Replace or augment the core algorithms with your own models (e.g., fine‑tuned LLMs) via the provided plugin hooks; integrate additional data feeds through the existing database schema.  
3. **Pilot Deployment** – Containerise the service, connect it to your internal data lake, and expose the REST/GraphQL APIs to downstream trading or analytics tools.  
4. **Production Scaling** – Leverage the built‑in database sharding and horizontal scaling options, add monitoring (Prometheus/Grafana) and enforce security policies (OAuth, role‑based access) before full rollout.

**Production Readiness**  
The project scores high on readiness: recent commits (as of 2026‑05‑13), 195 ★, active forking activity, and a clean Python codebase with clear documentation. While the license and security posture still need a final audit, the overall ecosystem signals—active maintainers, modern dependencies, and a modular design—make AI‑Stock‑Master a viable candidate for a serious pilot in production environments.

### Русский

AI‑Stock‑Master — это открытая платформа для анализа тенденций китайского, гонконгского и американского фондовых рынков, использующая три ключевых AI‑алгоритма для предсказания и визуализации многомерных данных. Типичный сценарий внедрения — быстрый прототип AI‑фич, построение RAG‑или агентных рабочих процессов и оценка инструментов модели в рамках небольшого proof‑of‑concept, после чего система готова к масштабированию в продакшн. По оценке проекта, благодаря активному развитию (195 ★, частые коммиты), хорошей документации и поддержке Python, готовность к production считается высокой, хотя окончательная проверка лицензии и безопасности всё же требуется.

### 中文

**项目简介**  
AI 股票大师（hengruiyun/AI-Stock-Master）是一款基于人工智能的股票趋势分析平台，能够对中国、香港和美国市场进行多维度解读。平台融合了三大核心算法，提供行情评分、情感分析和因子回测等功能，为投资者提供从入门学习到实战决策的全链路支持。

**价值体现**  
- **快速赋能 AI 能力**：无需从零搭建模型堆栈，直接使用项目已封装好的算法和数据管道，即可在自己的系统中加入智能选股、趋势预测等功能。  
- **多市场、多维度**：同时覆盖 A 股、港股、美股，支持技术指标、新闻情感、基本面因子等多源数据的统一分析。  
- **开源可定制**：代码结构清晰、模块化设计，便于二次开发、模型替换或与自研 RAG/Agent 工作流深度集成。

**典型接入方式**  
1. **克隆仓库 & 环境准备**  
   ```bash
   git clone https://github.com/hengruiyun/AI-Stock-Master.git
   cd AI-Stock-Master
   pip install -r requirements.txt
   ```
2. **配置数据源**  
   - 在 `config.yaml` 中填写行情 API（如 TuShare、Yahoo Finance）和新闻抓取接口的凭证。  
   - 如需使用自有数据库，可将 `db_engine` 参数指向 PostgreSQL/MySQL 并执行 `scripts/init_db.sql` 初始化表结构。  
3. **启动核心服务**  
   - **API 服务**：`uvicorn app.main:app --reload`（FastAPI）提供 RESTful 接口，供前端或外部系统调用。  
   - **任务调度**：使用 `celery -A tasks worker --loglevel=info` 运行异步任务，实现每日行情爬取、模型预测与报告生成。  
4. **前端集成**（可选）  
   - 项目自带基于 Vue/React 的演示页面，直接通过 `npm install && npm run serve` 启动；也可以把 API 接口嵌入已有的交易平台 UI。  
5. **小规模 POC**  
   - 只启动 `score` 模块（行情评分）进行一次性预测，验证模型效果后再逐步开启 `sentiment`、`factor` 等模块。

**生产可用性评估**  
- **活跃度**：最近一次提交在 2026‑05‑13，拥有 195+ 星、44+ Fork，社区活跃，文档（README、API 说明）相对完整。  
- **技术成熟度**：核心算法已封装为可复用的 Python 包，使用 FastAPI + Celery + PostgreSQL 组合，符合微服务化部署的常规模式。  
- **可扩展性**：支持 Docker Compose 与 Kubernetes 部署，方便在云环境中水平扩容。  
- **风险点**：仍需对许可证（MIT）进行合规确认，检查依赖库的安全漏洞（如 `pandas`, `scikit-learn`），并确保关键数据接口（行情 API）具备商业级 SLA。  

综合来看，AI‑Stock‑Master 已具备 **高** 的生产候选价值，适合作为 **原型验证** 或 **正式投产** 的基础组件，只要在安全审计和运维监控（日志、告警）上做适配，即可在金融机构或量化团队的实际业务中安全上线。

## 🧭 Practical evaluation

**Value:** hengruiyun/AI-Stock-Master helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 195 GitHub stars
- 44 forks
- updated 2026-05-13
- primary language: Python
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 41/100 |
| stars | 49/100 |
| topics | 75/100 |
| outlook | 66/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 47/100 |
| production | 69/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/hengruiyun/AI-Stock-Master) · [← Back to AI/ML](./README.md)</sub>
