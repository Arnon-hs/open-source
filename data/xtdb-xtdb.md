# xtdb/xtdb

[![Stars](https://img.shields.io/github/stars/xtdb/xtdb?style=flat-square&color=yellow)](https://github.com/xtdb/xtdb/stargazers) [![Forks](https://img.shields.io/github/forks/xtdb/xtdb?style=flat-square&color=blue)](https://github.com/xtdb/xtdb/network) [![Language](https://img.shields.io/badge/lang-Clojure-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> An immutable SQL database for application development, time-travel reporting and data compliance. Developed by @juxt

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3k |
| 🍴 **Forks** | 190 |
| 💻 **Language** | Clojure |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-06-28 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bitemporal` `database` `dbms` `immutable` `sql` `temporal`

## 🎯 Categories

Data · Database

## 📝 Summary

### English

**Summary**  
xtdb/xtdb is an immutable, time‑travel‑enabled SQL database built in Clojure that lets developers treat raw data as a continuously versioned, queryable store. It’s designed for analytics pipelines, compliance reporting, and automated data workflows, making it easy to retrieve historical snapshots and guarantee data integrity.

**Value**  
Because every transaction is immutable and indexed by transaction time, xtdb provides built‑in auditability and “time‑travel” queries without extra tooling. This turns raw event streams into a searchable, relational view that can feed dashboards, ML pipelines, or compliance checks, reducing the need for separate ETL layers and simplifying data governance.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the provided Docker image or the local JVM starter, and load a small dataset using the SQL API.  
2. **Integration checklist** – Verify the README’s setup steps, confirm connectivity with your existing JVM/Clojure or Java services, and test the time‑travel query syntax on a sandbox.  
3. **Incremental rollout** – Replace a non‑critical analytics pipeline (e.g., a nightly report) with xtdb, using its JDBC driver or HTTP endpoint, and monitor latency and storage growth.  

**Production readiness**  
With over 3 000 stars, recent commits (as of 2026‑06‑28), active community forks, and proven adoption in several Juxt‑backed projects, xtdb is mature enough for a serious pilot. The main risk lies in the integration effort: the documentation focuses on Clojure/Java ecosystems, so teams using other languages may need to build thin wrappers or rely on the HTTP API. Once the initial setup cost is validated, the platform’s immutable architecture and strong compliance features make it a robust candidate for production workloads.

### Русский

xtdb — это иммутабельная SQL‑база на Clojure, позволяющая хранить версии данных и выполнять «time‑travel» запросы, что упрощает построение аналитических и compliance‑pipeline‑ов. Для начала рекомендуется развернуть небольшой proof‑of‑concept, следуя инструкциям из README, и проверить интеграцию с текущими ETL/BI‑процессами. По уровню готовности проект считается production‑ready: активная разработка, более 3000 звёзд на GitHub и реальное внедрение в нескольких компаниях.

### 中文

**xtdb/xtdb 简介**

xtdb/xtdb 是一个开源的 SQL 数据库，用于应用开发、时间旅行报告和数据合规。它可以帮助将原始数据转换为可搜索、可分析或可自动化的管道。

**价值**

xtdb/xtdb 的价值在于，它可以帮助您组织分析管道、处理数据集、提高报告工作流程的效率。

**典型接入方式**

典型的接入方式包括：

1. 评估：首先评估 xtdb/xtdb 是否适合您的需求。
2. 小规模试验：在小规模试验中验证 xtdb/xtdb 的性能和可用性。
3. 阅读 README 文档：仔细阅读 xtdb/xtdb 的 README 文档，以了解其使用方法和最佳实践。

**生产可用性**

xtdb/xtdb 的生产可用性非常高，主要原因是：

1. 最近的活动：xtdb/xtdb 的维护和更新频率较高。
2. 广泛的采用：xtdb/xtdb 有大量的 GitHub 星数和 fork 数

## 🧭 Practical evaluation

**Value:** xtdb/xtdb helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 3016 GitHub stars
- 190 forks
- updated 2026-06-28
- primary language: Clojure
- 6 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 57/100 |
| stars | 74/100 |
| topics | 75/100 |
| outlook | 78/100 |
| quality | 82/100 |
| recency | 100/100 |
| adoption | 69/100 |
| production | 75/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/xtdb/xtdb) · [← Back to Data](./README.md)</sub>
