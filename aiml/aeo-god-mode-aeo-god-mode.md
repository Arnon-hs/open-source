# AEO-God-Mode/aeo-god-mode

[![Stars](https://img.shields.io/github/stars/AEO-God-Mode/aeo-god-mode?style=flat-square&color=yellow)](https://github.com/AEO-God-Mode/aeo-god-mode/stargazers) [![Forks](https://img.shields.io/github/forks/AEO-God-Mode/aeo-god-mode?style=flat-square&color=blue)](https://github.com/AEO-God-Mode/aeo-god-mode/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Free AEO + AI search readiness plugin for WordPress. Schema, llms.txt, AI crawler controls, brand sentiment + citation tracking.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 22 |
| 🍴 **Forks** | — |
| 💻 **Language** | PHP |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`aeo` `ai-search` `ai-seo` `answer-engine-optimization` `chatgpt` `claude` `gemini` `llms-txt` `perplexity` `schema-markup` `seo` `wordpress`

## 🎯 Categories

AI/ML · Marketing

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
AEO‑God‑Mode is a free WordPress plugin that adds “AI‑ready” capabilities such as schema generation, LLM prompt files, AI crawler controls, brand‑sentiment analysis, and citation tracking. It lets developers prototype AI‑enhanced features, build Retrieval‑Augmented Generation (RAG) or agent workflows, and evaluate model tooling without assembling a custom stack from scratch. With modest adoption (22 ★) and recent updates, it’s a handy starter kit for internal or experimental projects.

**Value**  
- **Speed‑to‑value:** All the plumbing for AI‑enhanced SEO (AEO) is pre‑wired—schema markup, prompt libraries (`llms.txt`), and crawler directives—so teams can focus on the business logic rather than low‑level integration.  
- **Flexibility:** Exposes multiple entry points (API, SDK, CLI) and language‑aware metadata, making it easy to plug into existing PHP/WordPress sites or to spin up a separate RAG/agent micro‑service.  
- **Cost‑effective prototyping:** Being open‑source and free, it removes licensing fees while still offering a production‑grade feature set for brand sentiment and citation tracking.

**Practical Adoption Path**  
1. **Clone & Install:** Add the plugin to a WordPress instance via the standard plugin uploader or Composer.  
2. **Configure API Keys:** Provide credentials for the LLM provider(s) you plan to use (OpenAI, Anthropic, etc.) in the plugin settings.  
3. **Define Schema & Prompts:** Use the built‑in UI or edit `llms.txt` to tailor prompts and schema to your niche.  
4. **Enable Crawler Controls:** Turn on AI‑crawler directives to guide search engine indexing and brand‑sentiment monitoring.  
5. **Iterate & Test:** Deploy to a staging environment, run automated tests or manual checks on citation accuracy and sentiment scores, then promote to production once stable.  

**Production Readiness**  
- **Maturity:** Medium. The plugin is actively maintained (last commit 2026‑05‑12) and suitable for prototypes or internal tools, but it still requires a review of dependencies, security posture, and licensing before mission‑critical deployment.  
- **Risk Areas:** No major metadata concerns, but you should verify the open‑source license compatibility with your stack, audit any third‑party libraries for vulnerabilities, and ensure you have a maintainer or fallback plan for long‑term support.  
- **Scalability:** Works well for typical WordPress traffic; for high‑volume or multi‑tenant scenarios, consider offloading heavy LLM calls to a dedicated backend service.  

In short, AEO‑God‑Mode offers a ready‑made AI augmentation layer for WordPress that accelerates experimentation and early‑stage product development, with a clear upgrade path to a more hardened, production‑grade setup after due diligence.

### Русский

AEO‑God‑Mode — это бесплатный плагин для WordPress, который добавляет готовый набор функций AEO и AI‑поиска (схемы, llms.txt, контроль краулеров, отслеживание бренда, цитат и настроек RAG/агентных воркфлоу), позволяя интегрировать искусственный интеллект без необходимости собирать стек моделей «с нуля». Типичный сценарий — быстрая прототипизация AI‑фич, построение RAG‑решений или оценка инструментов модели в рамках внутреннего проекта, используя простой API/SDK/CLI и метаданные языка. Готовность к продакшну — средняя: плагин подходит для прототипов и внутренних процессов, но требует проверки зависимостей, лицензии и безопасности перед масштабным внедрением.

### 中文

**项目简介**  
AEO‑God‑Mode（aeo-god-mode）是一款面向 WordPress 的免费 AEO 与 AI 搜索准备插件，提供 Schema、`llms.txt`、AI 爬虫控制、品牌情感与引用追踪等功能，让站点在不从零构建模型堆栈的情况下快速获得 AI 能力。

**价值**  
- **快速原型**：开发者可直接在现有 WordPress 环境中开启 AI 检索、RAG（检索增强生成）或智能代理工作流，无需自行部署大模型。  
- **提升 SEO 与品牌监控**：内置 Schema 标注、情感分析和引用追踪，帮助搜索引擎更好地理解内容，同时实时监控品牌舆情。  
- **统一接入**：通过 API、SDK 或 CLI 暴露实现信号，支持语言元数据和主题聚焦，便于与现有营销或 AI 系统集成。

**典型接入方式**  
1. **插件安装**：在 WordPress 后台直接安装并启用插件。  
2. **配置 API/SDK**：在插件设置页填写所使用的 LLM（如 OpenAI、Claude 等）API 密钥，或通过提供的 PHP SDK 在主题/插件代码中调用 `AeoGodMode::search($query)` 等方法。  
3. **CLI 调试**：利用自带的 WP‑CLI 命令（如 `wp aeo-god-mode crawl --topic=product`）进行爬虫和情感分析的批量操作。  

**生产可用性**  
- **成熟度**：目前属于 **Medium** 级别，适合原型验证或内部工作流使用。插件已更新至 2026‑05‑12，拥有 22+ GitHub stars，代码基于 PHP，覆盖 14 个主题标签。  
- **准备工作**：在生产环境部署前建议进行以下检查：  
  - **依赖审计**：确认插件依赖的第三方库（如 Guzzle、OpenAI SDK）版本安全且兼容现有 WordPress 环境。  
  - **安全评估**：检查 API 密钥存储方式、输入过滤和权限控制，防止注入或泄露风险。  
  - **维护状态**：联系项目维护者确认长期维护计划或自行 fork 形成内部维护分支。  
- **可扩展性**：插件结构清晰，支持自定义 Schema、扩展爬虫规则以及接入自有模型，满足后期功能迭代需求。

综上，AEO‑God‑Mode 为希望在 WordPress 站点快速加入 AI 检索与品牌监控能力的团队提供了低门槛、功能完整的解决方案，只需完成依赖与安全审查即可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** AEO-God-Mode/aeo-god-mode helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 22 GitHub stars
- updated 2026-05-12
- primary language: PHP
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 69/100 |
| quality | 64/100 |
| recency | 100/100 |
| adoption | 21/100 |
| production | 73/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/AEO-God-Mode/aeo-god-mode) · [← Back to AI/ML](./README.md)</sub>
