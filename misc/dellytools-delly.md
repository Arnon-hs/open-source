# dellytools/delly

[![Stars](https://img.shields.io/github/stars/dellytools/delly?style=flat-square&color=yellow)](https://github.com/dellytools/delly/stargazers) [![Forks](https://img.shields.io/github/forks/dellytools/delly?style=flat-square&color=blue)](https://github.com/dellytools/delly/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> DELLY2: Structural variant discovery by integrated paired-end and split-read analysis

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 527 |
| 🍴 **Forks** | 138 |
| 💻 **Language** | C++ |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cancer-genomics` `delly` `delly-users` `genomic` `germline` `rearrangement` `structural-variation` `sv-discovery` `svs` `tumor`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary**  
DELLY2 is an open‑source C++ toolkit for discovering structural variants in genomic data by jointly analysing paired‑end and split‑read signals. The project provides a mature, command‑line‑driven pipeline that can be scripted or wrapped in higher‑level workflows, making it a solid foundation for adding AI‑driven variant interpretation or RAG/agent‑based analysis on top of raw SV calls.  

**Value**  
- **AI‑ready data source** – DELLY2 produces high‑quality SV calls that can be fed directly into machine‑learning models for phenotype prediction, variant prioritisation, or downstream knowledge‑graph retrieval.  
- **Accelerates prototyping** – Instead of building a variant caller from scratch, teams can focus on the AI layer (e.g., feature extraction, model training, RAG integration) while relying on DELLY2’s proven detection algorithms.  

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the provided example on a small test BAM/CRAM dataset, and verify the output against the README.  
2. **Wrap the CLI** – Create a thin wrapper (Python subprocess, Docker image, or Nextflow/CWL module) that exposes the SV call step as a reproducible component.  
3. **Integrate AI** – Feed the VCF output into your model pipeline (e.g., feature engineering, embedding generation, or a RAG index) and iterate on the AI component.  
4. **Scale & automate** – Once the wrapper is stable, embed it in a larger workflow manager (Snakemake, WDL, Airflow) for batch processing of production datasets.  

**Production readiness**  
- **Maturity**: 527 ⭐, 138 🍴, recent commit (2026‑07‑03) and active C++ codebase indicate a stable core.  
- **Readiness level**: *Medium* – suitable for internal prototypes or semi‑automated pipelines, but requires a small integration effort (containerisation, dependency pinning, validation of runtime resources).  
- **Risks**: The integration steps are not fully documented; you’ll need to confirm build requirements (Boost, HTSlib, etc.) and assess maintenance overhead before committing to a production environment.  

Overall, DELLY2 offers a reliable genomic SV detection engine that can be quickly leveraged as the data‑generation layer for AI‑enhanced bioinformatics workflows, provided you allocate time for a modest proof‑of‑concept and dependency validation.

### Русский

**dellytools/delly** — это открытый C++‑инструмент для обнаружения структурных вариаций (SV) в геномных данных с помощью комбинированного анализа парных концов и сплит‑ридов. Он подходит для быстрого прототипирования AI‑фич в биоинформатике (например, построения RAG‑ или агентных пайплайнов, оценки новых моделей), при этом интеграция лучше начинать с небольшого proof‑of‑concept и проверки README. Готовность к продакшн — средняя: проект стабилен (527★, активные обновления), но требует проверки зависимостей и уточнения пути интеграции перед масштабным использованием.

### 中文

**简短介绍**

Delly是一个用于结构变异发现的开源工具，通过整合配对末端和分裂读分析来实现。它可以帮助开发者在没有从头搭建模型栈的情况下添加AI能力。

**价值**

Delly的价值在于它可以帮助开发者快速构建AI特性、创建RAG或代理工作流以及评估模型工具。

**典型接入方式**

典型的接入方式包括：

1. 评估：通过阅读README文档和创建一个小的原型来评估Delly的接入路径。
2. 原型开发：使用Delly构建AI特性和RAG或代理工作流。
3. 集成：在生产环境中集成Delly，确保依赖项和维护成本。

**生产可用性**

Delly的生产可用性为中等（Medium），因为它适合用于原型开发或内部工作流，但在生产环境中需要进行依赖项和维护成本的检查。

**注意**

在接入Delly之前，需要注意以下风险：

1.  集成路径不明显：需要仔细阅读README文档和进行小规模

## 🧭 Practical evaluation

**Value:** dellytools/delly helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 527 GitHub stars
- 138 forks
- updated 2026-07-03
- primary language: C++
- 10 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 54/100 |
| stars | 58/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 76/100 |
| recency | 80/100 |
| adoption | 57/100 |
| production | 68/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/dellytools/delly) · [← Back to Misc](./README.md)</sub>
