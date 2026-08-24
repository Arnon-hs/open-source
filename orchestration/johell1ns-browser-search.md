# Johell1NS/browser-search

[![Stars](https://img.shields.io/github/stars/Johell1NS/browser-search?style=flat-square&color=yellow)](https://github.com/Johell1NS/browser-search/stargazers) [![Forks](https://img.shields.io/github/forks/Johell1NS/browser-search?style=flat-square&color=blue)](https://github.com/Johell1NS/browser-search/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> A skill for AI agents: search the web with SearXNG, browse with Camofox, bypass protections with CloakBrowser. Anti-hallucination by design. Self-hosted, free, unlimited.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 214 |
| 🍴 **Forks** | 22 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-skills` `ai-agent` `ai-tools` `browser-automation` `camoufox` `cloakbrowser` `deep-research` `opencode` `searxng` `web-scraping` `web-search`

## 🎯 Categories

Orchestration · Automation · AI/ML · Design

## 📝 Summary

### English

**Brief Summary**  
Johell1NS/browser‑search is an open‑source skill that equips AI agents with reliable web‑search, browsing, and protection‑bypass capabilities using SearXNG, Camofox, and CloakBrowser. It is self‑hosted, free, and designed to eliminate hallucinations by grounding agent actions in real‑time web data, making it ideal for building repeatable, multi‑agent workflows.

**Value**  
- **Deterministic grounding** – By routing every query through SearXNG and rendering pages with Camofox (or CloakBrowser when needed), the skill supplies agents with verifiable, up‑to‑date information, dramatically reducing hallucinations.  
- **Workflow orchestration** – The skill exposes a clean API/CLI/SDK that can be chained with other tools, enabling complex pipelines such as “search → extract → store in memory → act”.  
- **Cost‑effective scaling** – Because it runs on your own infrastructure, you avoid per‑request fees and retain full control over data privacy and rate limits.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the Docker‑compose stack (SearXNG + Camofox + CloakBrowser) locally, and call the provided REST endpoints from a sandboxed LLM (e.g., OpenAI, Anthropic).  
2. **Integration** – Wrap the endpoints in your agent framework (LangChain, Auto‑GPT, CrewAI) using the supplied JavaScript SDK or a thin HTTP client in your preferred language.  
3. **Testing & Tuning** – Validate that the agent’s responses contain citations from the fetched pages; adjust timeout, user‑agent strings, and CloakBrowser options to handle site‑specific protections.  
4. **Production rollout** – Deploy the stack to a managed Kubernetes or VM environment, enable TLS, add rate‑limiting and monitoring, and integrate with your existing agent memory store (vector DB, Redis, etc.).

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last update 2026‑06‑29), has 214 ⭐ on GitHub and 22 forks, and provides multiple integration hooks (API, SDK, CLI).  
- **Strengths**: Self‑hosted architecture, clear separation of concerns, and a design that explicitly mitigates hallucination.  
- **Open issues**: Licensing and security posture still need a formal review; dependencies (SearXNG, Camofox, CloakBrowser) must be kept up‑to‑date, and you should implement monitoring for potential anti‑scraping blocks.  
- **Recommendation**: Suitable for internal prototypes, pilot projects, or production systems where you can allocate resources for dependency management and security vetting. With proper hardening, it can become a reliable backbone for enterprise‑grade AI agent pipelines.

### Русский

Johell1NS/browser-search — open‑source‑набор, который позволяет AI‑агентам автоматически искать информацию в SearXNG, просматривать результаты через Camofox и обходить защитные механизмы с помощью CloakBrowser, обеспечивая минимизацию галлюцинаций. Он идеален для построения повторяемых рабочих потоков: координации нескольких агентов, создания пайплайнов с инструментами и стандартизации памяти агента. Готовность к production — средняя: проект уже стабилен и активно поддерживается (214 звёзд, обновление 2026‑06‑29), но перед запуском в продакшн рекомендуется проверить лицензию, безопасность зависимостей и наличие постоянных мейнтейнеров.

### 中文

**简短介绍**

Johell1NS/browser-search 是一个开源项目，提供了一个技能，让 AI 代理可以通过 SearXNG 搜索网页，使用 Camofox 浏览网页，并使用 CloakBrowser 抑制保护措施。它是一款自主托管的、免费且无限的工具，旨在防止 AI 代理产生虚假信息。

**价值**

Johell1NS/browser-search 的主要价值在于，它可以帮助将孤立的提示和工具组合成可重复的代理工作流程，使得 AI 代理能够协调多个代理工作流程、添加工具使用的管道以及标准化代理记忆。

**典型接入方式**

该项目提供了 API/SDK/CLI 等实现信号，可以方便地接入其他系统。语言元数据和专注话题也提供了对项目的额外信息。

**生产可用性**

该项目的生产可用性为中等。它适合用于原型或内部工作流程，但在生产环境中使用之前，需要进行依赖项和维护检查。

## 🧭 Practical evaluation

**Value:** Johell1NS/browser-search helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 214 GitHub stars
- 22 forks
- updated 2026-06-29
- primary language: JavaScript
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 50/100 |
| topics | 100/100 |
| outlook | 65/100 |
| quality | 60/100 |
| recency | 40/100 |
| adoption | 45/100 |
| production | 55/100 |
| usefulness | 100/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/Johell1NS/browser-search) · [← Back to Orchestration](./README.md)</sub>
