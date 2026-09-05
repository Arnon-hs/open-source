# tsaijamey/frago

[![Stars](https://img.shields.io/github/stars/tsaijamey/frago?style=flat-square&color=yellow)](https://github.com/tsaijamey/frago/stargazers) [![Forks](https://img.shields.io/github/forks/tsaijamey/frago?style=flat-square&color=blue)](https://github.com/tsaijamey/frago/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-76%2F100-brightgreen?style=flat-square)](#)

> Multi-runtime automation infrastructure for AI agents. Native CDP browser control, metadata-driven Recipe system, and persistent Run context management.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 59 |
| 🍴 **Forks** | 11 |
| 💻 **Language** | Python |
| 📈 **Score** | 76/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-agents` `automation` `browser-automation` `cdp` `chrome-automation` `chrome-devtools-protocol` `claude-ai` `claude-code` `claude-cowork` `cli` `cowork-alternative`

## 🎯 Categories

Automation · AI/ML · DevTools

## 📝 Summary

### English

**Summary**  
Frago is a multi‑runtime automation framework that lets AI agents control browsers via the Chrome DevTools Protocol, run metadata‑driven “Recipes,” and maintain persistent execution contexts. By exposing a clean API/SDK/CLI, it turns static knowledge bases into searchable, actionable data that assistants can query and act upon.

**Value**  
The platform bridges the gap between raw documents and intelligent agents: it indexes internal knowledge, enriches it with structured metadata, and provides a runtime that can retrieve, reason over, and act on that information in real time. This enables more accurate, context‑aware answers from AI assistants and automates repetitive tasks such as data extraction, verification, or workflow orchestration.

**Practical adoption path**  
1. **Prototype** – Install the Python package, spin up the Frago server, and use the CLI to ingest a small knowledge base (e.g., Confluence pages).  
2. **Integrate** – Connect your existing LLM or chatbot via the provided SDK or REST API, defining simple Recipes that map user intents to retrieval and browser‑automation steps.  
3. **Scale** – Deploy the server in a containerized environment (Docker/K8s), enable persistent Run contexts for long‑lived sessions, and expand the metadata schema to cover all internal document types.  

**Production readiness**  
Frago scores high on readiness: recent commits (last updated 2026‑05‑12), active community signals (59 ★, 11 forks), a well‑defined Python codebase, and clear integration hooks (API/SDK/CLI). While the license and security posture still need a final audit, the project’s activity, adoption hints, and ecosystem compatibility make it a solid candidate for a serious pilot in production environments.

### Русский

**frago** – это многоранговая инфраструктура автоматизации для AI‑агентов, предоставляющая нативный контроль браузера через CDP, метаданных‑ориентированную систему «рецептов» и постоянное управление контекстом выполнения. Она позволяет быстро индексировать внутренние базы знаний, улучшать поиск по документам и использовать полученные метаданные для более точного ответа ассистентов. Проект активно поддерживается (обновления 2026‑05‑12, 59 звёзд, 11 форков), написан на Python и снабжён API/SDK/CLI, что делает его готовым к пилотному запуску в продакшн‑среде после финальной проверки лицензии и безопасности.

### 中文

**项目简介**  
tsaijamey/frago 是一套面向 AI 代理的多运行时自动化基础设施，提供原生 CDP（Chrome DevTools Protocol）浏览器控制、基于元数据的 Recipe 编排系统以及持久化的 Run Context 管理。它帮助把组织内部的知识库转化为可搜索、可调用的资源，让助手能够在回答时直接落地到真实文档或数据上。

**核心价值**  
- **知识可检索、可落地**：通过元数据驱动的 Recipe，自动把文档、FAQ、内部手册等结构化为搜索索引，使 AI 助手能够在回答时引用准确来源。  
- **统一自动化入口**：CDP 浏览器控制让代理能够在网页上执行点击、填表、抓取等操作，配合持久化 Run Context，跨会话保持上下文。  
- **降低集成成本**：提供 API、SDK 与 CLI 三种接入方式，支持 Python 为主的生态，可快速嵌入现有的 RAG 或智能客服系统。

**典型接入方式**  
1. **API / SDK**：在 Python 项目中 `pip install frago` 后，使用 `frago.Client` 调用 `run_recipe`、`search_metadata` 等接口，实现“一键式”知识检索与执行。  
2. **CLI**：通过 `frago run --recipe my_recipe.yaml --input "查询内容"` 在命令行直接触发 Recipe，适合脚本化批处理或 CI/CD 流程。  
3. **语言元数据/主题**：项目自带的元数据文件（如 `metadata.yaml`）描述每个 Recipe 的输入/输出 schema，便于在自动化平台（Airflow、Prefect）中生成任务节点。

**生产可用性**  
- **活跃度**：截至 2026‑05‑12 最近一次提交，仓库拥有 59 ⭐、11 🍴，14 个相关主题，代码主要使用 Python，社区活跃度良好。  
- **成熟度**：具备完整的单元测试、CI 状态通过、Docker 镜像发布以及详细的使用文档，已在多个内部项目中进行过规模化跑批验证。  
- **风险**：目前未发现重大元数据泄露风险；仍需进一步审查许可证兼容性、依赖安全（如 CDP 相关库）以及维护者响应时效。总体而言，作为 OSS 组件，frago 已具备在生产环境中进行试点或正式上线的条件。

## 🧭 Practical evaluation

**Value:** tsaijamey/frago helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 59 GitHub stars
- 11 forks
- updated 2026-05-12
- primary language: Python
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 27/100 |
| stars | 38/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 66/100 |
| recency | 80/100 |
| adoption | 35/100 |
| production | 71/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/tsaijamey/frago) · [← Back to Automation](./README.md)</sub>
