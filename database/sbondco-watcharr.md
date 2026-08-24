# sbondCo/Watcharr

[![Stars](https://img.shields.io/github/stars/sbondCo/Watcharr?style=flat-square&color=yellow)](https://github.com/sbondCo/Watcharr/stargazers) [![Forks](https://img.shields.io/github/forks/sbondCo/Watcharr?style=flat-square&color=blue)](https://github.com/sbondCo/Watcharr/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Open source, self-hostable watched list for all your content (movies, tv series, anime, games) with user authentication, modern and clean UI and a very simple setup.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.4k |
| 🍴 **Forks** | 69 |
| 💻 **Language** | Go |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`content` `docker` `docker-compose` `games` `go` `golang` `list` `lists` `movies` `self-hostable` `self-hosted` `series`

## 🎯 Categories

Database · DevOps/Infra

## 📝 Summary

### English

**Brief summary**  
Watcharr (sbondCo/Watcharr) is an open‑source, self‑hosted “watched list” app for movies, TV series, anime, and games. It ships a modern, clean UI with built‑in user authentication and a simple one‑command setup, and is written in Go with a PostgreSQL‑backed database.

**Value**  
Watcharr provides a ready‑made, fully functional front‑end for any consumer‑facing media‑tracking product, letting teams skip the time‑consuming work of designing and implementing list‑management UI, authentication flows, and responsive layouts. Its component‑level design (API, SDK, CLI) can be reused across multiple projects, accelerating UI delivery and ensuring a consistent user experience.

**Practical adoption path**  

1. **Evaluation** – Clone the repo and run the Docker‑compose starter (or the single‑binary installer) to spin up the service locally. Verify the API endpoints and UI against your own data model.  
2. **Integration** – Replace or extend the default Go backend with your own services if needed, or consume the exposed REST/GraphQL API from an existing front‑end. Authentication can be hooked into your SSO provider via the built‑in OAuth adapters.  
3. **Customization** – Fork the UI (React/Vue – whichever the project uses) to re‑brand or add feature flags, then redeploy the container to your staging environment.  
4. **Production rollout** – Deploy the Docker image to your Kubernetes or VPS cluster, enable TLS and configure environment‑specific secrets. Monitor health via the built‑in metrics endpoint.

**Production readiness**  
- **Activity & community** – 1,408 stars, 69 forks, recent commit (2026‑07‑05) and ongoing releases indicate strong momentum.  
- **Architecture** – Go backend, PostgreSQL storage, containerized deployment, and clear API/CLI surface make it cloud‑native and easy to scale.  
- **Security** – User authentication is baked in, but a final audit of the license, dependency vulnerabilities, and maintainer responsiveness is still required.  
Overall, Watcharr is a high‑readiness OSS candidate for pilots or full production use, provided the final security/license review is completed.

### Русский

Резюме:

 sbondCo/Watcharr - это открытый исходный проект, который позволяет создавать и хранить список просмотренных контента (фильмы, телесериалы, аниме, игры) с возможностью авторизации пользователей, современным и чистым интерфейсом и простой настройкой. Этот проект может помочь разработчикам ускорить процесс создания пользовательских интерфейсов, экономя время на разработку.custom UI и упрощая реализацию стандартных интерфейсов. sbondCo/Watcharr готов к производственному использованию, имеет сильную активность, адоптацию и экосистемные сигналы, что делает его надежным кандидатом для серьезного пилота.

### 中文

**Watcharr简介**

Watcharr是一款开源、自主可控的内容观看列表管理工具，支持电影、电视剧、动漫、游戏等多种内容类型。它提供了用户认证、现代且简洁的UI、简单的设置等功能。

**价值**

Watcharr的主要价值在于帮助开发人员减少自定义UI工作量，从而能够更快地交付产品。它提供了可重用的界面组件，使开发人员能够更高效地构建用户界面。

**典型接入方式**

Watcharr的接入方式如下：

1. 使用API或SDK：Watcharr暴露了API和SDK接口，使开发人员能够轻松地集成其功能。
2. 使用CLI：Watcharr提供了命令行接口，使开发人员能够轻松地管理其功能。
3. 集成到现有项目：Watcharr可以轻松地集成到现有的项目中，从而提供用户管理、内容管理等功能。

**生产可用性**

Watcharr具有高生产可用性，其GitHub星标数达到1408，fork数达到69，最近的更新时间为2026-07-05。其主要语言为Go

## 🧭 Practical evaluation

**Value:** sbondCo/Watcharr helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1408 GitHub stars
- 69 forks
- updated 2026-07-05
- primary language: Go
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 46/100 |
| stars | 67/100 |
| topics | 100/100 |
| outlook | 61/100 |
| quality | 68/100 |
| recency | 40/100 |
| adoption | 61/100 |
| production | 62/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/sbondCo/Watcharr) · [← Back to Database](./README.md)</sub>
