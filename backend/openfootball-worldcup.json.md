# openfootball/worldcup.json

[![Stars](https://img.shields.io/github/stars/openfootball/worldcup.json?style=flat-square&color=yellow)](https://github.com/openfootball/worldcup.json/stargazers) [![Forks](https://img.shields.io/github/forks/openfootball/worldcup.json?style=flat-square&color=blue)](https://github.com/openfootball/worldcup.json/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> Free open public domain football data for the world cups (national teams & clubs) in JSON incl. Canada/USA/Mexico 2026, USA 2025, Qatar 2022, Russia 2018 and more - No API key required ;-)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 438 |
| 🍴 **Forks** | 68 |
| 💻 **Language** | Unknown |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`api` `clubworldcup` `football` `json` `opendata` `qatar2022` `russia2018` `usa2025` `worldcup` `worldcup2018` `worldcup2022` `worldcup2026`

## 🎯 Categories

Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
openfootball/worldcup.json is an open‑source repository that provides free, public‑domain JSON datasets covering every FIFA World Cup—national teams, clubs, and upcoming editions (Canada/USA/Mexico 2026, USA 2025, Qatar 2022, Russia 2018, etc.). The data can be consumed without an API key, making it ideal for quickly prototyping AI/ML features such as retrieval‑augmented generation (RAG), chat‑agent knowledge bases, or analytics dashboards. With over 400 stars, recent commits, and active community interest, it is a production‑ready candidate for pilot projects.

**Value**  
- **Instant, high‑quality football knowledge**: eliminates the need to scrape, clean, or license World Cup data, letting teams focus on model engineering rather than data collection.  
- **AI‑ready format**: JSON structure maps naturally to vector stores and prompt templates, accelerating RAG, recommendation, or question‑answering pipelines.  
- **Zero‑cost, no‑auth integration**: eliminates API‑key management and usage‑based fees, reducing operational overhead for PoCs and internal tooling.

**Practical Adoption Path**  
1. **Read the README & explore the data** – verify schema (tournaments, matches, teams, venues, scores).  
2. **Create a small proof‑of‑concept**: ingest a subset (e.g., the 2022 tournament) into your vector database (e.g., Pinecone, Weaviate, or local Chroma).  
3. **Build a simple RAG endpoint**: combine the indexed JSON with a language model (OpenAI, LLaMA, etc.) to answer “Who won the 2022 final?” or “List all Canadian players in 2026”.  
4. **Iterate and expand**: add more editions, join with external stats (player ratings, betting odds), and wrap the logic in a micro‑service or serverless function.  
5. **Productionize**: lock the repository version via a Git tag or hash, set up CI to pull updates, and monitor data integrity with schema validation.

**Production Readiness**  
- **Activity & community**: 438 GitHub stars, 68 forks, recent commit (2026‑06‑29), and 12 relevant topics indicate an active, maintained project.  
- **Stability**: JSON files are static assets; no runtime service is required, minimizing failure modes.  
- **Risk assessment**: No immediate metadata or licensing concerns (public domain), but a final review of the repository’s LICENSE file and a quick security scan of the CI pipeline are advisable.  
- **Scalability**: The data size is modest (tens of MB), so it can be cached in memory or stored in any standard vector store without performance bottlenecks.  

Overall, openfootball/worldcup.json offers a low‑friction, high‑value data source that can be integrated into AI workflows with a simple proof‑of‑concept, and its community signals make it ready for serious pilot deployments.

### Русский

**openfootball/worldcup.json** — открытый набор данных в формате JSON о всех чемпионатах мира по футболу (национальные сборные и клубы), включающий предстоящие турниры (Канада/США/Мексика 2026, США 2025, Катар 2022, Россия 2018 и др.). Он позволяет быстро добавить футбольный контекст в прототипы AI‑приложений (RAG, агентные цепочки, оценка моделей) без необходимости создавать собственный датасет или использовать API‑ключи. Проект имеет высокий уровень готовности к production: активные коммиты, 438 звёзд, 68 форков, свежие обновления и широкая поддержка в сообществе, что делает его надёжным вариантом для пилотных внедрений после небольшого proof‑of‑concept и проверки README.

### 中文

**项目简介**

openfootball/worldcup.json 是一个开源项目，提供了足球世界杯数据（国家队和俱乐部）以 JSON 格式，包括 2026 年加拿大/美国/墨西哥世界杯、2025 年美国世界杯、2022 年卡塔尔世界杯等。该项目无需 API 密钥即可使用。

**价值**

该项目的价值在于，它可以帮助开发者快速构建足球领域的 AI 应用程序，节省了从零开始构建模型的时间。它可以用于以下场景：

* 快速 prototyping AI 特性
* 构建决策支持系统（RAG 或 agent 工作流）
* 评估模型工具

**典型接入方式**

由于该项目提供了 JSON 格式的数据，因此可以通过以下方式接入：

1. 直接从 GitHub 下载 JSON 文件
2. 使用 API（如果提供）访问数据
3. 根据 README 文件中的指示进行集成

**生产可用性**

该项目具有高生产可用性，理由如下：

* 近期活动：最近一次更新为 2026 年 6 月 29 日
* 强大的

## 🧭 Practical evaluation

**Value:** openfootball/worldcup.json helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 438 GitHub stars
- 68 forks
- updated 2026-06-29
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 46/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 64/100 |
| recency | 40/100 |
| adoption | 53/100 |
| production | 56/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/openfootball/worldcup.json) · [← Back to Backend](./README.md)</sub>
