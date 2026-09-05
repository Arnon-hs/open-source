# sneg55/pingcrm

[![Stars](https://img.shields.io/github/stars/sneg55/pingcrm?style=flat-square&color=yellow)](https://github.com/sneg55/pingcrm/stargazers) [![Forks](https://img.shields.io/github/forks/sneg55/pingcrm?style=flat-square&color=blue)](https://github.com/sneg55/pingcrm/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Personal Networking CRM — AI-powered, open-source, self-hostable. Syncs Gmail, Telegram, Twitter/X, and LinkedIn. Detects life events, drafts follow-ups, scores relationships.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 24 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | Python |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `claude` `crm` `fastapi` `networking` `nextjs` `open-source` `personal-crm` `relationship-management` `self-hosted`

## 🎯 Categories

AI/ML · Networking · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
PingCRM (sneg55/pingcrm) is an open‑source, AI‑enhanced personal networking CRM that syncs data from Gmail, Telegram, X (Twitter), and LinkedIn, automatically detects life events, drafts follow‑up messages, and scores relationship health. Built in Python, it offers a ready‑made API/SDK/CLI stack for quickly prototyping AI‑driven relationship‑management features without starting from scratch.  

**Value**  
- **Accelerated AI integration** – The project bundles data ingestion, event detection, and relationship‑scoring pipelines, letting teams focus on higher‑level product logic rather than building a foundational model stack.  
- **Rapid prototyping** – With clear API endpoints and a CLI, developers can experiment with Retrieval‑Augmented Generation (RAG), autonomous agents, or custom follow‑up workflows in minutes.  
- **Open‑source transparency** – All code, model prompts, and integration scripts are publicly available, facilitating auditability and custom extensions.  

**Practical Adoption Path**  
1. **Evaluation** – Clone the repo, run the provided Docker compose or Python virtual environment, and connect a test Gmail/Telegram/X/LinkedIn account using the documented OAuth flows.  
2. **Prototype** – Use the CLI or SDK to call the “detect‑event” and “draft‑follow‑up” endpoints, iterate on prompt engineering, or swap in your own LLM (e.g., OpenAI, Anthropic, or a local model).  
3. **Integration** – Wrap the API in your internal services, add webhook listeners for new contacts or events, and store the generated scores in your existing CRM or data warehouse.  
4. **Productionize** – Harden the deployment (TLS, secret management), add monitoring for API latency and error rates, and implement rate‑limiting for external services (Gmail, LinkedIn).  

**Production Readiness**  
- **Maturity** – Medium. The codebase is actively maintained (last commit 2026‑06‑29), has 24 stars and 8 forks, and the core functionality works end‑to‑end for personal use cases.  
- **Dependencies** – Relies on third‑party APIs (Google, Telegram, X, LinkedIn) and an LLM provider; these need proper credential handling and quota monitoring.  
- **Stability** – Suitable for internal tools, prototypes, or low‑traffic SaaS features, but requires additional hardening (security review, CI/CD pipelines, automated testing) before mission‑critical production use.  
- **Risks** – Licensing, long‑term maintainer commitment, and security posture have not been fully vetted; a formal audit is recommended prior to wide deployment.  

Overall, PingCRM offers a fast, low‑friction route to embed AI‑powered relationship management into your product stack, with a clear path from sandbox experimentation to a hardened internal service.

### Русский

**sneg55/pingcrm** — это открытая CRM‑система для персонального нетворкинга, использующая AI для автоматической синхронизации сообщений из Gmail, Telegram, X (Twitter) и LinkedIn, выявления жизненных событий, генерации черновиков последующих контактов и оценки качества отношений. Проект подходит для быстрого прототипирования AI‑функций (RAG, агентные сценарии) и интеграции в существующие пайплайны через предоставляемый API/SDK/CLI, однако перед выпуском в продакшн требуется проверка лицензии, безопасности и постоянства поддержки. В текущем состоянии готовность к production — средняя: пригоден для внутренних или экспериментальных решений, но нуждается в дополнительном аудите зависимостей и обслуживании.

### 中文

**项目简介**

sneg55/pingcrm 是一个开源项目，提供个人网络关系管理 (CRM) 的 AI 功能。它能够与 Gmail、Telegram、Twitter/X 和 LinkedIn 等平台进行同步，检测重要生活事件，自动发送跟进邮件，并评分关系强度。

**价值**

sneg55/pingcrm 的价值在于，它可以帮助开发者快速添加 AI 能力，而无需从零开始构建模型堆栈。它还可以用于 prototype AI 特性、构建 RAG 或代理工作流、评估模型工具等场景。

**典型接入方式**

sneg55/pingcrm 可以通过以下方式接入：

* API：直接调用 API 进行数据同步和操作
* SDK：使用提供的 SDK 集成到自己的应用中
* CLI：使用命令行界面进行交互式操作

**生产可用性**

sneg55/pingcrm 的生产可用性为中等。它适合用于 prototype 或内部工作流的开发，需要对依赖项和维护进行检查后才能用于生产环境。

## 🧭 Practical evaluation

**Value:** sneg55/pingcrm helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 24 GitHub stars
- 8 forks
- updated 2026-06-29
- primary language: Python
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 30/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 63/100 |
| recency | 80/100 |
| adoption | 28/100 |
| production | 68/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/sneg55/pingcrm) · [← Back to AI/ML](./README.md)</sub>
