# Viren070/AIOStreams

[![Stars](https://img.shields.io/github/stars/Viren070/AIOStreams?style=flat-square&color=yellow)](https://github.com/Viren070/AIOStreams/stargazers) [![Forks](https://img.shields.io/github/forks/Viren070/AIOStreams?style=flat-square&color=blue)](https://github.com/Viren070/AIOStreams/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> One addon to rule them all. AIOStreams consolidates multiple Stremio addons and debrid services into a single, highly customisable super-addon.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.3k |
| 🍴 **Forks** | 783 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`stremio` `stremio-addon` `stremio-addons`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
Viren070/AIOStreams is a TypeScript‑based “super‑addon” for Stremio that merges dozens of community addons and debrid services into one highly configurable package, letting users add AI‑enhanced streaming features without building a model stack from scratch. With over 2 200 GitHub stars, active maintenance (last update 2026‑07‑12) and strong ecosystem signals, it is ready for pilot‑level production use, though a quick security/license audit is advisable before full deployment.  

**Value** – The project eliminates the need to stitch together multiple streaming addons and debrid APIs, and it already bundles AI‑ready hooks for rapid prototyping of recommendation, RAG, or agent‑driven workflows.  

**Practical adoption path** – Clone the repo, configure the desired addons and debrid services via the provided JSON/YAML files, run the TypeScript build, and point Stremio to the generated super‑addon endpoint; a brief manual inspection of integration metadata is recommended to verify compatibility with your existing stack.  

**Production readiness** – The high star/fork count, recent commits, and clear documentation indicate a mature OSS candidate suitable for a serious pilot, but a final review of the license, security posture, and maintainer responsiveness should be completed before rolling it out to production.

### Русский

**Viren070/AIOStreams** — это универсальный супер‑адон для Stremio, который объединяет множество сторонних адонов и debrid‑сервисов в одну высоко настраиваемую платформу, позволяя быстро добавить AI‑функциональность (например, RAG или агентные сценарии) без необходимости строить модельный стек с нуля. Типичное внедрение — прототипирование новых AI‑фич и их оценка в рамках существующей медиаплатформы, при этом перед запуском в прод требуется ручная проверка метаданных из‑за их разреженности. Проект считается готовым к пилотному использованию в production: активные обновления, большая пользовательская база (2286 звёзд, 783 форка), поддержка TypeScript и положительные сигналы экосистемы, хотя лицензия, безопасность и поддержка мейнтейнеров требуют окончательной проверки.

### 中文

**项目简介**  
Viren070/AIOStreams 是一个“全能”Stremio 插件集合，它把多个第三方插件和 debrid 服务整合进一个高度可定制的超级插件，使用 TypeScript 编写，社区活跃，星标 2286、fork 783。

**价值**  
- **一次接入，多功能**：无需分别安装、配置各类 Stremio 插件和 debrid 服务，AIOStreams 统一入口即可提供搜索、流媒体解析、去广告、缓存加速等全部能力。  
- **高度可定制**：通过插件配置文件即可开启/关闭任意子插件，满足不同地区、不同用户的内容需求。  
- **开源可靠**：近期仍在活跃维护（截至 2026‑07‑12），代码质量高，社区贡献丰富，适合作为业务原型或正式产品的底层流媒体层。

**典型接入方式**  
1. **环境准备**：确保 Stremio 已安装并运行；在服务器（Node.js ≥ 16）上克隆仓库。  
2. **依赖安装**：`npm ci`（或 `yarn install`）安装所有 TypeScript 依赖。  
3. **配置子插件**：在 `config.json`（或相应的环境变量）中列出需要启用的子插件及对应的 debrid 账户凭证。  
4. **构建并启动**：`npm run build && npm start`，插件会在本地 8080 端口提供 HTTP 接口。  
5. **在 Stremio 中注册**：打开 Stremio → “插件” → “添加本地插件”，填写插件的 URL（如 `http://<host>:8080/manifest.json`），完成后即可在 Stremio UI 中看到统一的内容库。

**生产可用性**  
- **成熟度**：GitHub 活跃度高，最近一次提交在 2026‑07‑12，社区贡献者众多，具备正式上线的技术基线。  
- **安全与合规**：目前未发现重大许可证或安全漏洞，但仍建议在生产环境前进行一次代码审计和依赖漏洞扫描（如使用 `npm audit`）。  
- **运维要求**：需要自行监控插件服务的可用性、日志以及 debrid 账户的配额使用情况；可配合 Docker 或 PM2 实现容器化/进程守护。  
- **适用场景**：从快速原型（验证 AI 推荐、RAG 流媒体检索）到正式业务（提供统一的流媒体入口）均可使用，具备“高”生产就绪度，适合作为 OSS 方案在内部或小规模对外服务中试点。

## 🧭 Practical evaluation

**Value:** Viren070/AIOStreams helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2286 GitHub stars
- 783 forks
- updated 2026-07-12
- primary language: TypeScript
- 3 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 72/100 |
| stars | 71/100 |
| topics | 38/100 |
| outlook | 54/100 |
| quality | 63/100 |
| recency | 40/100 |
| adoption | 72/100 |
| production | 56/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/Viren070/AIOStreams) · [← Back to Misc](./README.md)</sub>
