# datahub-project/datahub

[![Stars](https://img.shields.io/github/stars/datahub-project/datahub?style=flat-square&color=yellow)](https://github.com/datahub-project/datahub/stargazers) [![Forks](https://img.shields.io/github/forks/datahub-project/datahub?style=flat-square&color=blue)](https://github.com/datahub-project/datahub/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> The Context Platform for your Data and AI Stack

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 11.9k |
| 🍴 **Forks** | 3.5k |
| 💻 **Language** | Python |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-platform` `context-management` `data-catalog` `data-discovery` `data-governance` `data-observability` `datahub` `metadata`

## 🎯 Categories

AI/ML · Data · Observability

## 📝 Summary

### English

**Brief Summary**  
DataHub (datahub-project/datahub) is an open‑source metadata platform that unifies data, AI, and observability assets into a single “context hub” for your stack. With strong community adoption (12 k+ stars, 3 k+ forks) and active Python‑centric development, it lets teams prototype AI features—such as RAG pipelines or agent workflows—without building a metadata layer from scratch.

**Value**  
DataHub supplies a ready‑made catalog of datasets, models, pipelines, and lineage information, enabling rapid experimentation and governance across the entire AI lifecycle. By exposing rich context through a searchable UI and APIs, it accelerates feature prototyping, model evaluation, and downstream integration, reducing the time‑to‑value for AI initiatives.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the Docker‑compose starter, and follow the README to ingest a small sample of your existing data assets.  
2. **Connector Integration** – Leverage the built‑in ingestion connectors (e.g., Snowflake, BigQuery, MLflow) or write a lightweight custom connector for your proprietary sources.  
3. **Workflow Hook‑up** – Connect DataHub’s GraphQL/REST APIs to your RAG or agent orchestration layer to surface relevant context at runtime.  
4. **Scale‑Up** – Gradually expand ingestion coverage, enable access controls, and integrate with existing CI/CD pipelines for continuous metadata updates.

**Production Readiness**  
The project scores high on production readiness: recent commits (as of 2026‑05‑14), robust community activity, and a growing ecosystem of plugins indicate stability. While the license and security posture still require a formal review, the maturity of the codebase, extensive documentation, and proven adoption in multiple enterprises make DataHub a solid candidate for a serious pilot or full‑scale deployment.

### Русский

DataHub — это открытая платформа‑контекст для управления данными и AI‑стеком, позволяющая быстро добавить возможности ИИ (прототипировать модели, строить RAG‑ и агентные пайплайны, оценивать инструменты) без необходимости создавать всё с нуля. Для внедрения рекомендуется начать с небольшого proof‑of‑concept, следуя инструкциям в README, а затем расширять интеграцию в существующие пайплайны данных. Проект имеет высокий уровень готовности к production: активные обновления, более 11 тыс. звёзд на GitHub, широкое принятие в сообществе и зрелую экосистему, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句话）**  
DataHub（datahub‑project/datahub）是面向数据与 AI 堆栈的统一上下文平台，提供元数据目录、血缘追踪和可观测性功能，帮助团队在已有数据资产上快速构建 AI 能力。它通过丰富的插件体系实现对数据仓库、机器学习模型、向量库等多源数据的统一治理和发现。

**价值**  
- **快速赋能 AI**：无需从零搭建模型管理体系，直接在统一的元数据层上原型化 AI 功能（如 RAG、Agent 工作流）。  
- **统一治理 & 可观测**：跨数据湖、数据仓库、模型注册中心等实现血缘、标签、访问控制等元数据统一管理，提升数据可信度与合规性。  
- **生态兼容**：提供超过 30 种开箱即用的连接器（Kafka、Snowflake、BigQuery、MLflow、LangChain 等），便于在现有技术栈中嵌入。

**典型接入方式**  
1. **小规模 PoC**：先克隆仓库，使用官方 Docker‑Compose 或 Helm chart 部署单节点实例，按照 README 完成基本的元数据摄取（如接入 Snowflake + dbt）。  
2. **插件化集成**：在已有数据管道或模型服务中加入 DataHub 的 Ingestion SDK（Python/Java）或使用预构建的 Airflow / Dagster 任务，将元数据实时写入平台。  
3. **API/GraphQL 调用**：通过 DataHub 提供的 GraphQL/REST 接口查询血缘、标签或搜索向量，供前端 UI、LLM 检索或监控系统使用。

**生产可用性**  
- **成熟度**：活跃度高（近 12k 星、3.5k Fork，2026‑05‑14 最近提交），社区和商业化背书（LinkedIn、Airbnb 等已在生产使用）。  
- **可部署性**：支持 Kubernetes、Helm、Docker Compose，具备高可用、水平扩展和 RBAC 安全控制。  
- **风险**：需进一步审查许可证（Apache‑2.0）兼容性、容器镜像安全扫描以及维护者响应时效，但整体已具备进入正式生产环境的条件，适合作为企业级元数据治理和 AI 研发的核心组件。

## 🧭 Practical evaluation

**Value:** datahub-project/datahub helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 11912 GitHub stars
- 3482 forks
- updated 2026-05-14
- primary language: Python
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 89/100 |
| stars | 87/100 |
| topics | 100/100 |
| outlook | 81/100 |
| quality | 89/100 |
| recency | 80/100 |
| adoption | 87/100 |
| production | 77/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/datahub-project/datahub) · [← Back to AI/ML](./README.md)</sub>
