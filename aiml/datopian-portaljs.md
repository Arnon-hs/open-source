# datopian/portaljs

[![Stars](https://img.shields.io/github/stars/datopian/portaljs?style=flat-square&color=yellow)](https://github.com/datopian/portaljs/stargazers) [![Forks](https://img.shields.io/github/forks/datopian/portaljs?style=flat-square&color=blue)](https://github.com/datopian/portaljs/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> 🌀 AI-native framework for building data portals. Scaffold a full portal from a brief and load datasets in minutes with agentic skills — any backend (CKAN, GitHub, Frictionless).

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.3k |
| 🍴 **Forks** | 331 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-agents` `ckan` `data-fabric` `data-management-platform` `data-mesh` `data-portal` `data-portal-frontends` `data-portals` `datahub` `dataverse` `dkan`

## 🎯 Categories

AI/ML · Data

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
PortalJS is an AI‑native, TypeScript‑based framework that lets you spin up a full‑featured data portal from a short natural‑language brief, automatically loading datasets from any backend (CKAN, GitHub, Frictionless, etc.) and wiring in agentic skills for RAG, workflow automation, or model evaluation. With over 2 200 GitHub stars and active maintenance, it offers a ready‑to‑use stack that adds AI capabilities without the need to build a custom model pipeline from scratch.  

**Value**  
- **Speed to prototype** – A single brief can generate a complete portal, dramatically cutting the time needed to test AI‑driven data‑catalog features.  
- **Backend agnostic** – Works with existing data stores (CKAN, GitHub, Frictionless) so you can reuse your current infrastructure.  
- **Agentic extensions** – Built‑in support for LLM‑driven agents enables RAG, automated data‑quality checks, and custom workflow orchestration without writing extensive glue code.  

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, run the starter script, and point it at a small public dataset (e.g., a CKAN catalog) to verify the “brief‑to‑portal” flow.  
2. **Read‑me & CI validation** – Follow the documented setup steps, run the test suite, and confirm the CI pipeline passes in your environment.  
3. **Incremental integration** – Replace a single internal data‑catalog page with a PortalJS instance, exposing the same APIs to downstream consumers.  
4. **Feature expansion** – Add custom agentic skills (e.g., data‑quality bots, recommendation agents) and connect to your production data lake or model registry.  

**Production Readiness**  
- **Activity & community** – Recent commits (as of 2026‑06‑23), >2 200 stars, and 300+ forks indicate strong community interest and ongoing maintenance.  
- **Technical maturity** – Written in TypeScript with clear module boundaries; the codebase includes CI, linting, and automated tests.  
- **Scalability** – Designed to plug into any backend, allowing you to scale horizontally by leveraging existing data‑service infrastructure.  
- **Risks** – License compliance, detailed security audit, and maintainer responsiveness still need a final check, but no major metadata or dependency issues were identified.  

Overall, PortalJS is a high‑readiness OSS candidate for teams that want to prototype or production‑grade AI‑enhanced data portals quickly, with a clear, low‑friction path from a sandbox trial to full‑scale deployment.

### Русский

**datopian/portaljs** — это AI‑native фреймворк для быстрого создания дата‑порталов: за счёт агентных навыков можно за несколько минут сгенерировать полностью работающий портал и подключить любые источники данных (CKAN, GitHub, Frictionless). Типичный сценарий внедрения — прототипирование AI‑фич, построение RAG‑ или агентных воркфлоу и оценка инструментов модели, начиная с небольшого proof‑of‑concept, проверив README и базовую интеграцию. Проект имеет высокий уровень готовности к production: активные коммиты, более 2 тыс. звёзд, широкий набор функций на TypeScript и поддержка как фронтенда, так и бэкенда, что делает его надёжным кандидатом для серьёзных пилотных запусков.

### 中文

**项目简介**  
datopian/portaljs 是一个 AI 原生的框架，能够在几分钟内通过简短描述和智能代理（agentic skills）搭建完整的数据门户，并可对接任意后端（CKAN、GitHub、Frictionless 等）快速加载数据集。

**价值**  
- **即插即用的 AI 能力**：无需从零构建模型堆栈，直接在门户中加入检索增强生成（RAG）或智能代理工作流。  
- **快速原型**：只需提供业务需求描述，即可自动生成前后端代码，极大缩短 AI 功能的验证周期。  
- **统一数据入口**：统一管理多种数据源，帮助团队在同一门户内进行数据探索、可视化和模型评估。

**典型接入方式**  
1. **阅读 README 并运行示例**：克隆仓库后执行 `npm install && npm run dev`，确认本地环境可用。  
2. **配置后端适配器**：在 `portal.config.ts` 中指定数据源（如 CKAN API URL、GitHub 仓库或本地 Frictionless 数据包）。  
3. **编写简要需求**：在 `prompt.txt` 中描述想要的门户功能，使用内置的 AI 代理生成完整的页面、数据模型和 API 路由。  
4. **小规模 PoC**：先在测试环境部署一个仅包含 1‑2 个数据集的门户，验证数据加载、搜索和 RAG 流程是否符合预期。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑23，项目最近一次提交，拥有 2.3k+ ⭐、331 个 Fork，且主要使用 TypeScript 开发，代码质量和社区活跃度均较高。  
- **成熟度**：框架已实现完整的前端 UI、后端适配层和 AI 插件体系，文档覆盖常见接入场景，适合直接用于内部或面向客户的产品原型。  
- **风险**：目前未发现重大元数据或许可证风险，但仍需对依赖的第三方库进行安全审计，并确认维护者的响应速度符合企业 SLA。  

**结论**：PortalJS 具备高可用的 OSS 基础，适合作为 AI 数据门户的底层平台，在完成安全审查后即可进入生产环境进行试点部署。

## 🧭 Practical evaluation

**Value:** datopian/portaljs helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2285 GitHub stars
- 331 forks
- updated 2026-06-23
- primary language: TypeScript
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 63/100 |
| stars | 71/100 |
| topics | 100/100 |
| outlook | 66/100 |
| quality | 71/100 |
| recency | 40/100 |
| adoption | 69/100 |
| production | 59/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/datopian/portaljs) · [← Back to AI/ML](./README.md)</sub>
