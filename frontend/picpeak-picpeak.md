# PicPeak/picpeak

[![Stars](https://img.shields.io/github/stars/PicPeak/picpeak?style=flat-square&color=yellow)](https://github.com/PicPeak/picpeak/stargazers) [![Forks](https://img.shields.io/github/forks/PicPeak/picpeak?style=flat-square&color=blue)](https://github.com/PicPeak/picpeak/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-76%2F100-brightgreen?style=flat-square)](#)

> 🚀 Self-hosted photo sharing platform for photographers & events. Open-source alternative to PicDrop/Scrapbook with time-limited galleries, password protection, custom branding & no monthly fees. Built with React + Node.js 📸

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 243 |
| 🍴 **Forks** | 44 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 76/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`client-gallery` `docker` `event-photography` `gallery` `gallery-management` `nodejs` `open-source` `photo-gallery` `photo-hosting` `photo-sharing` `photography` `photography-business`

## 🎯 Categories

Frontend · Backend · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
PicPeak is a self‑hosted photo‑sharing platform built with React and Node.js that lets photographers and event organizers create time‑limited, password‑protected galleries with custom branding—offering an open‑source alternative to services like PicDrop or Scrapbook without recurring fees. The project ships a ready‑to‑use API/SDK and CLI, making it easy to prototype AI‑enhanced features such as automatic tagging, visual search, or RAG‑based photo assistants. With active maintenance, a growing community (≈ 240 ★), and TypeScript‑first code, PicPeak is positioned as a production‑grade OSS candidate.

**Value**  
- **AI‑ready foundation** – The clean TypeScript API and modular architecture let developers plug in vision models (e.g., CLIP, GPT‑4‑V) for auto‑tagging, similarity search, or chat‑based photo assistants without rebuilding the core upload, storage, and gallery logic.  
- **Cost‑effective hosting** – No monthly SaaS fees; you run it on your own infra, keeping data private and controlling scaling.  
- **Feature richness out of the box** – Time‑limited links, password protection, custom branding, and multi‑tenant support reduce the need for custom development.

**Practical Adoption Path**  
1. **Spin‑up a dev environment** – Clone the repo, run `docker compose up` (or use the provided CLI) to launch the React front‑end, Node API, and a PostgreSQL DB.  
2. **Integrate AI services** – Add a small wrapper that calls your preferred vision model (e.g., an Azure Computer Vision endpoint) from the existing API hooks; expose the results via the SDK or a new endpoint.  
3. **Customize branding & auth** – Replace the default UI theme and configure password or OAuth providers through the config file.  
4. **Deploy to production** – Move the Docker stack to your cloud/K8s environment, enable TLS, and point a domain to the service.  
5. **Iterate** – Use the built‑in CLI to create time‑limited galleries, then layer AI‑driven features (auto‑tag suggestions, search, RAG agents) on top.

**Production Readiness**  
- **Activity & community** – Recent commit (2026‑06‑29), 240+ stars, 44 forks, and 19 relevant topics indicate healthy interest and ongoing maintenance.  
- **Tech stack** – TypeScript + React/Node.js provides strong type safety and modern dev tooling; the Dockerized deployment simplifies scaling and isolation.  
- **Security & licensing** – No immediate metadata risks, but a final review of the open‑source license (MIT‑style) and any third‑party dependencies is recommended before a wide‑scale rollout.  
- **Scalability** – The separation of front‑end, API, and PostgreSQL allows horizontal scaling; you can swap the DB for a managed service if needed.  

Overall, PicPeak offers a robust, AI‑friendly baseline for photo‑sharing applications, with a clear, low‑friction path from prototype to production.

### Русский

PicPeak — это self‑hosted платформа для обмена фотографиями, позволяющая быстро создавать временные галереи с защитой паролем, фирменным брендингом и без ежемесячных расходов; её стек (React + Node.js, TypeScript) делает интеграцию простой через готовый API/CLI. Типичный сценарий — организация фотосессий, мероприятий или клиентских подборок, где требуется мгновенный приватный доступ и возможность добавить AI‑фичи (например, поиск по изображению или генерацию описаний) без построения модели с нуля. Проект считается почти готовым к production: активные коммиты, 243 звёзд, широкая экосистема и открытая документация, однако перед внедрением стоит проверить лицензию, безопасность и наличие поддерживающих мейнтейнеров.

### 中文

**简短介绍**

PicPeak/picpeak 是一个开源的照片共享平台，适合摄影师和事件组织者。它提供了时间限制的画廊、密码保护、自定义品牌和无月费功能。PicPeak/picpeak 使用 React 和 Node.js 构建，提供了一个开源的替代方案。

**价值**

PicPeak/picpeak 帮助开发者添加 AI 能力，没有从零开始的模型堆栈。它可以用于以下用例：

* prototype AI 特性
* 构建 RAG 或代理工作流
* 评估模型工具

**典型接入方式**

PicPeak/picpeak 提供了 API、SDK 和 CLI 的接口，让开发者可以方便地接入。它还暴露了语言元数据和专注话题的信息。

**生产可用性**

PicPeak/picpeak 的生产可用性非常高。它有活跃的社区，最近有更新，语言是 TypeScript，支持 19 个话题。 GitHub 上有 243 个星星和 44 个分支。它的保密性、安全性和活跃维护者仍需要进一步审查。

## 🧭 Practical evaluation

**Value:** PicPeak/picpeak helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 243 GitHub stars
- 44 forks
- updated 2026-06-29
- primary language: TypeScript
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 41/100 |
| stars | 51/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 48/100 |
| production | 73/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/PicPeak/picpeak) · [← Back to Frontend](./README.md)</sub>
