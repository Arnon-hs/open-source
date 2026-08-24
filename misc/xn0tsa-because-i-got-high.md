# xn0tsa/because-i-got-high

[![Stars](https://img.shields.io/github/stars/xn0tsa/because-i-got-high?style=flat-square&color=yellow)](https://github.com/xn0tsa/because-i-got-high/stargazers) [![Forks](https://img.shields.io/github/forks/xn0tsa/because-i-got-high?style=flat-square&color=blue)](https://github.com/xn0tsa/because-i-got-high/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-31%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 31/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Misc

## 📝 Summary

### English

Here's a brief summary of the open-source project:

The PuffPal disclosure project provides a dataset of 1.08 million cannabis users, allowing users to convert raw data into searchable, analyzable, or automated pipelines. This project offers practical use cases for organizing analytics pipelines, processing datasets, and improving reporting workflows. However, due to sparse integration signals and limited quality signals, users must perform manual inspection and verification before adopting it for production use.

In terms of adoption, the practical path involves:

1. **Manual inspection**: Carefully review the project's metadata, documentation, and issues to ensure it meets your needs and is well-maintained.
2. **Dependency and maintenance checks**: Verify the project's dependencies and maintenance requirements to ensure they align with your production environment.
3. **Prototype or internal workflow testing**: Use the project in a controlled environment to test its functionality and performance.
4. **Production readiness evaluation**: Assess the project's readiness for production use, considering factors like scalability, security, and reliability.

Regarding production readiness, the project is rated as "Medium", indicating that it's suitable for prototypes or internal workflows but requires careful evaluation and verification before adoption in production environments.

### Русский

Резюме:

Проект "1.08M cannabis users data leaked in PuffPal disclosure" предлагает преобразование raw данных в поисковые, анализируемые или автоматизированные потоки. Этот проект может быть полезен для организации аналитических потоков, обработки наборов данных и улучшения процессов отчетности. Однако, перед внедрением необходимо провести тщательное осмотр и проверку лицензии, поддержки, документации, проблем и графика выпусков. 

Уровень готовности к production: средний, что делает его подходить для прототипов или внутренних потоков, с обязательными проверками зависимостей и поддержки перед релизом в производство.

### 中文

**项目简介**  
1.08M cannabis users data leaked in PuffPal disclosure 是一份约 108 万条大麻用户记录的泄露数据集，来源于 Hacker News（github‑mentions）。该数据可直接用于构建可搜索、可分析或自动化的数据管线，帮助团队快速搭建用户行为分析、风险监控或报告生成等原型。

**价值**  
- **快速获取真实用户画像**：一次性获取大规模真实用户记录，省去自行爬取或采集的成本。  
- **加速分析与建模**：数据结构化后即可用于统计分析、机器学习特征工程或行为分群。  
- **支撑业务决策**：为合规审计、市场研究或反欺诈等场景提供可信的底层原始材料。

**典型接入方式**  
1. **手动审查**：下载原始 CSV/JSON 文件后，用 Pandas、Spark 或 DuckDB 等工具检查字段完整性、敏感信息脱敏情况。  
2. **ETL 导入**：将清洗后的数据写入内部数据湖（如 S3、HDFS）或关系型数据库（PostgreSQL、ClickHouse），并在 Airflow、Dagster 等调度平台上构建每日/每周的处理流水线。  
3. **搜索/分析层**：在 Elasticsearch、OpenSearch 或 ClickHouse 上建立全文/聚合索引，以支持即时查询和仪表盘（Grafana、Superset）展示。  
> **注意**：项目元数据的集成信号稀疏，建议在正式接入前完成一次完整的质量评估（字段校验、缺失率、合法性）并记录审计日志。

**生产可用性**  
- **成熟度**：Medium。适合作为原型、内部数据科学实验或一次性报告的输入数据；在投入生产前需完成依赖检查、持续维护计划以及合规审计。  
- **准备工作**：  
  - 验证数据许可证和隐私合规性（GDPR/CCPA）。  
  - 建立自动化的清洗/脱敏脚本，防止敏感字段泄露。  
  - 监控数据更新频率和来源可靠性，避免因元数据稀疏导致的集成中断。  
- **后续维护**：由于项目维护和文档较少，建议自行维护 fork，定期同步上游变更并记录 issue。  

总体而言，该数据集在原型开发和内部分析场景下价值突出，但在生产环境使用前必须完成严格的质量、合规和运维审查。

## 🧭 Practical evaluation

**Value:** 1.08M cannabis users data leaked in PuffPal disclosure helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-06-29
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 33/100 |
| quality | 26/100 |
| recency | 40/100 |
| adoption | 0/100 |
| production | 38/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/xn0tsa/because-i-got-high) · [← Back to Misc](./README.md)</sub>
