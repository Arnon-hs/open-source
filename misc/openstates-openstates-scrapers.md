# openstates/openstates-scrapers

[![Stars](https://img.shields.io/github/stars/openstates/openstates-scrapers?style=flat-square&color=yellow)](https://github.com/openstates/openstates-scrapers/stargazers) [![Forks](https://img.shields.io/github/forks/openstates/openstates-scrapers?style=flat-square&color=blue)](https://github.com/openstates/openstates-scrapers/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> source for Open States scrapers

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 907 |
| 🍴 **Forks** | 511 |
| 💻 **Language** | Python |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-07-08 |
| 🔍 **Source** | github |

## 🏷️ Topics

`government` `hacktoberfest` `python` `scrapers` `states` `united-states`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
OpenStates Scrapers is a Python‑based open‑source library that harvests legislative data (bills, votes, legislators, etc.) from state government websites and feeds it into the OpenStates platform. With over 900 ★, frequent commits (last update 2026‑07‑08) and a sizable fork network, the project is actively maintained and already used by the OpenStates community.

**Value**  
The scrapers give developers a ready‑made, well‑documented pipeline for pulling structured, up‑to‑date state‑level political data without having to write custom parsers for each jurisdiction. Because the codebase follows the OpenStates data model, the output can be dropped directly into downstream analytics, civic‑tech dashboards, or research pipelines that already expect OpenStates‑compatible JSON.

**Practical adoption path**  
1. **Read the README** – verify the supported states and required dependencies.  
2. **Run a small proof‑of‑concept**: clone the repo, install the Python requirements, and execute a single‑state scraper (e.g., `python -m scrapers.run ca`).  
3. **Integrate**: pipe the generated JSON into your existing data store or ETL process, adjusting only configuration (API keys, storage paths).  
4. **Scale**: once the POC is validated, orchestrate multiple scrapers via a task scheduler (Airflow, Prefect) and monitor for changes in source websites.

**Production readiness**  
Given its recent activity, strong community adoption (907 ★, 511 forks), and alignment with the OpenStates ecosystem, the project is mature enough for a serious pilot. The primary remaining checks are a formal license review, a quick security audit of dependencies, and confirmation that at least one maintainer is responsive to issues—once those are cleared, the scrapers can be considered production‑ready for ingesting state legislative data at scale.

### Русский

**Краткое резюме:**  
`openstates/openstates-scrapers` — это открытый набор Python‑скриптов для массового сбора и нормализации данных о законодательных органах США, активно поддерживаемый сообществом (907 ★, 511 fork, обновления до 2026‑07‑08). Его типичный сценарий — автоматическое извлечение актуальной информации о законопроектах, заседаниях и депутатах в рамках ETL‑конвейера или аналитической платформы. По уровню готовности проект считается production‑ready: стабильный код, широкое использование и активные контрибьюторы позволяют начать с небольшого proof‑of‑concept и быстро масштабировать интеграцию в продуктивную среду.

### 中文

**openstates/openstates-scrapers 简介**

openstates/openstates-scrapers 是一个开源项目，提供了 Open States 抓取器的源代码。该项目可以帮助开发者抓取政府数据和信息，具有高生产可用性和强大的生态系统支持。

**价值**

openstates/openstates-scrapers 的价值在于，它提供了一个稳定的和易于使用的抓取器，能够帮助开发者快速获取政府数据和信息。该项目的 README 和活动信息匹配了一个具体的工作流程，能够满足开发者的需求。

**典型接入方式**

为了接入 openstates/openstates-scrapers，开发者可以按照以下步骤进行：

1. 阅读 README 文档，了解项目的使用方法和注意事项。
2. 检查项目的活动和更新记录，确保项目是活跃维护的。
3. 开始一个小的测试项目，以评估项目的可行性和适用性。

**生产可用性**

openstates/openstates-scrapers 具有高生产可用性，适合用于生产环境。项目的最近活动、采用率和生态系统信号

## 🧭 Practical evaluation

**Value:** openstates/openstates-scrapers may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 907 GitHub stars
- 511 forks
- updated 2026-07-08
- primary language: Python
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 68/100 |
| stars | 63/100 |
| topics | 75/100 |
| outlook | 77/100 |
| quality | 80/100 |
| recency | 100/100 |
| adoption | 64/100 |
| production | 79/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-08 · [View on GitHub](https://github.com/openstates/openstates-scrapers) · [← Back to Misc](./README.md)</sub>
