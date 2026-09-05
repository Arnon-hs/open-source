# Manavarya09/public-apis-live

[![Stars](https://img.shields.io/github/stars/Manavarya09/public-apis-live?style=flat-square&color=yellow)](https://github.com/Manavarya09/public-apis-live/stargazers) [![Forks](https://img.shields.io/github/forks/Manavarya09/public-apis-live?style=flat-square&color=blue)](https://github.com/Manavarya09/public-apis-live/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-78%2F100-brightgreen?style=flat-square)](#)

> Every public API in one place — aggregated, deduped, and auto-checked for reachability. Refreshed daily. npm + Claude plugin + live search.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 128 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 78/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`api` `api-list` `apis` `claude` `developer-tools` `free-apis` `mcp` `nextjs` `npm-package` `public-apis`

## 🎯 Categories

MCP · AI/ML · Backend · DevTools

## 📝 Summary

### English

**Brief Summary**  
Manavarya09/public-apis-live aggregates every publicly available API into a single, deduplicated, daily‑refreshed dataset that is automatically checked for reachability. The project ships an npm package, a Claude AI plugin, and a live‑search UI, making it easy for developers and AI assistants to discover and invoke real‑world services through a standard protocol.

**Value**  
- **One‑stop catalog**: Eliminates the need to hunt across scattered API lists, giving AI agents and developers a reliable source of live endpoints.  
- **Auto‑validated reachability**: Daily health checks ensure the listed APIs are actually callable, reducing integration failures.  
- **Standardized access**: By exposing API metadata (SDK/CLI, language support, topics) in a uniform format, it enables Model Context Protocol (MCP) servers and other AI‑agent frameworks to plug‑and‑play tools without custom adapters.  

**Practical Adoption Path**  
1. **Explore & select** – Use the live‑search UI or the npm package (`public-apis-live`) to query APIs by language, category, or capability.  
2. **Integrate** – Pull the JSON catalog into your AI‑assistant codebase or MCP server; the metadata includes endpoint URLs, auth hints, and SDK links.  
3. **Connect** – Generate client wrappers (or use existing SDKs) based on the provided signals, then register the API as a tool in your assistant’s tool‑calling registry (e.g., Claude plugin, LangChain, or custom MCP implementation).  
4. **Monitor** – Rely on the project’s daily health checks; any endpoint that becomes unreachable is automatically flagged in the catalog, letting you react quickly.  

**Production Readiness**  
- **Activity & community**: 128 ★ on GitHub, recent commits (last updated 2026‑06‑23), and an active issue/PR flow indicate a healthy maintainer presence.  
- **Technical maturity**: Implemented in TypeScript, with clear npm distribution, a ready‑to‑use Claude plugin, and a searchable web UI—no hidden build steps.  
- **Reliability**: Daily reachability verification and deduplication reduce runtime errors and maintenance overhead.  
- **Risk considerations**: License compliance, security audit of the underlying API endpoints, and long‑term maintainer commitment should be confirmed before a large‑scale rollout, but the current signals suggest the project is solid enough for a pilot or production integration.

### Русский

Manavarya09/public-apis-live — это открытый каталог всех публичных API, автоматически агрегируемый, дедуплицированный и проверяемый на доступность каждый день; он поставляется как npm‑пакет, Claude‑плагин и сервис с живым поиском, что упрощает подключение AI‑ассистентов к реальным инструментам через единый протокол. Типичный сценарий — интеграция AI‑агентов или Model Context Protocol серверов с внешними сервисами без ручного поиска и валидации API, используя готовые метаданные (язык, тип SDK/CLI, тематика). Проект имеет высокий уровень готовности к production: активные коммиты (обновлён 23 июня 2026), 128 звёзд, TypeScript‑база, поддержка npm и плагинов, а также положительные сигналы экосистемы, требующие лишь окончательной проверки лицензии и безопасности.

### 中文

**项目简介**  
Manavarya09/public-apis-live 将全球公开的 API 汇总、去重并每日自动检测可达性，提供 npm 包、Claude 插件以及实时搜索功能，帮助开发者和 AI 助手快速发现并调用可靠的公共接口。

**价值**  
- **统一入口**：一次性获取数千个公开 API，免去自行搜集、去重的繁琐。  
- **实时可达性**：每日自动检测，保证列表中的接口都是可用的，降低调用失败风险。  
- **AI 友好**：配合 Model Context Protocol（MCP）等标准协议，方便 AI 代理直接发现并使用真实工具和数据。  

**典型接入方式**  
1. **npm 包**：`npm install public-apis-live` 后在代码中通过提供的 SDK 查询、过滤并调用感兴趣的 API。  
2. **Claude 插件**：在 Claude AI 中启用插件，即可让对话式 AI 通过自然语言检索并调用对应的公共 API。  
3. **Live Search API**：直接调用 RESTful 搜索端点（如 `GET https://api.public-apis.live/search?q=weather`），适用于 CLI、脚本或自建服务。  

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑23，星标 128、Fork 8，社区活跃。  
- **技术成熟度**：使用 TypeScript 编写，提供完整的类型定义，易于集成到现代前后端项目。  
- **可靠性**：每日自动健康检查确保列表中 API 的可达性，降低生产环境的调用错误。  
- **风险**：目前未发现重大元数据或安全问题，但仍需对许可证、长期维护者以及潜在依赖漏洞进行最终审查。  

总体来看，public-apis-live 已具备较高的生产就绪度，适合作为 AI 助手、模型上下文服务或任何需要统一公共 API 接入的后端系统的基础设施。

## 🧭 Practical evaluation

**Value:** Manavarya09/public-apis-live helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 128 GitHub stars
- 8 forks
- updated 2026-06-23
- primary language: TypeScript
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 45/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 39/100 |
| production | 74/100 |
| usefulness | 90/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/Manavarya09/public-apis-live) · [← Back to Mcp](./README.md)</sub>
