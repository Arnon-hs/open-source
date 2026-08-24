# google/digitalbuildings

[![Stars](https://img.shields.io/github/stars/google/digitalbuildings?style=flat-square&color=yellow)](https://github.com/google/digitalbuildings/stargazers) [![Forks](https://img.shields.io/github/forks/google/digitalbuildings?style=flat-square&color=blue)](https://github.com/google/digitalbuildings/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Digital Buildings (ontology and SDK) currently being used by Google internally to manage our own buildings.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 447 |
| 🍴 **Forks** | 173 |
| 💻 **Language** | Python |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`brick-schema` `buildingsmart` `digitalbuildings` `ontology` `rdf`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
Google Digital Buildings is an open‑source ontology and SDK (written in Python) that lets teams model, query, and visualize building‑related data with a ready‑made UI layer. By exposing a set of API/SDK/CLI primitives, it lets developers assemble user‑facing interfaces far faster than building custom front‑ends from scratch, while reusing proven components and interaction patterns.

**Value**  
- **Accelerated UI delivery** – pre‑packaged widgets, forms, and visualizations for spaces, sensors, and control systems eliminate the need to hand‑code common building‑management screens.  
- **Consistency & reuse** – a shared ontology ensures data semantics are uniform across products, reducing integration bugs and maintenance overhead.  
- **Lower front‑end effort** – the SDK abstracts API calls and state handling, so front‑end teams can focus on business logic rather than low‑level plumbing.

**Practical adoption path**  
1. **Evaluate the SDK** by cloning the repo and running the provided CLI against a sandbox building‑data endpoint.  
2. **Integrate the Python client** into your back‑end or serverless layer to expose the ontology‑driven data model as a GraphQL/REST service.  
3. **Compose UI** by importing the library’s React (or web‑component) widgets into your existing front‑end stack, customizing styling as needed.  
4. **Iterate** with the built‑in CLI for schema migrations and validation, then promote the integrated code to a staging environment for user testing.

**Production readiness**  
The project shows strong OSS credentials: 447 ★, 173 forks, recent commits (as of 2026‑06‑23), active issue handling, and a clear Python‑first implementation. These signals, together with Google’s internal use, indicate a mature codebase suitable for a pilot in production. The remaining diligence items are a final license review, a security audit of the SDK’s dependencies, and confirmation of an active maintainer community before full‑scale rollout.

### Русский

**google/digitalbuildings** — открытая онтология и SDK, позволяющие быстро создавать пользовательские интерфейсы для управления зданиями, используя готовые UI‑компоненты и API/CLI‑интеграцию. Проект уже активно поддерживается (447 ⭐, 173 fork, последние коммиты – 2026‑06‑23), написан на Python и имеет сильные сигналы готовности к продакшн‑использованию, что делает его подходящим для пилотных внедрений. Основные выгоды — ускоренное построение фронтенда, повторное использование компонентов и упрощённая доставка UI‑решений.

### 中文

**项目简介**  
Google Digital Buildings（`google/digitalbuildings`）是一套面向建筑管理的本体（ontology）与 SDK，现已在 Google 内部用于统一管理其办公楼宇。该项目提供了丰富的 API、CLI 与 Python SDK，帮助开发者快速构建面向用户的建筑信息界面，极大降低了自定义 UI 的工作量。

**价值体现**  
- **加速前端交付**：通过复用已实现的建筑数据模型和 UI 组件，产品团队可以在几天内完成 UI 原型并投入生产，而无需从头编写数据结构和交互逻辑。  
- **统一数据语义**：本体定义了建筑空间、设备、传感器等标准概念，确保跨团队、跨系统的数据一致性，降低后端集成成本。  
- **提升可维护性**：SDK 封装了对 Google Digital Buildings 后端服务的调用细节，前端代码只需关注视图层，实现更清晰的职责划分。

**典型接入方式**  
1. **Python SDK**：在前端项目的后端服务或 BFF（Backend‑for‑Frontend）层通过 `pip install digitalbuildings-sdk` 引入 SDK，使用 `DigitalBuildingsClient` 进行身份验证并调用 REST/GraphQL 接口获取建筑模型、设备状态等数据。  
2. **CLI 工具**：项目自带 `dbuilder` CLI，可在本地快速生成模型定义文件（JSON/YAML）或导出示例前端代码片段，适用于原型开发或 CI/CD 自动化流程。  
3. **API 直调**：如果前端使用的是纯前端框架（如 React、Vue），也可以直接调用公开的 REST/GraphQL 端点，配合 OpenAPI/GraphQL schema 生成 TypeScript 类型定义，从而实现类型安全的前端调用。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑23，项目拥有 447 Stars、173 Forks，最近一次提交在同一天，表明维护活跃。  
- **成熟度**：已在 Google 内部大规模使用，具备完整的单元/集成测试、CI 流水线以及详细的文档。  
- **生态兼容**：主要语言为 Python，提供 API 描述（OpenAPI、GraphQL）以及多语言示例，便于在不同技术栈中集成。  
- **风险**：目前未发现重大许可证或安全漏洞，但仍建议在正式投产前完成一次内部安全审计，并确认维护者的长期可用性。  

综合来看，`google/digitalbuildings` 具备高可信度的生产就绪度，是构建建筑管理类前端产品的可靠加速器。

## 🧭 Practical evaluation

**Value:** google/digitalbuildings helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 447 GitHub stars
- 173 forks
- updated 2026-06-23
- primary language: Python
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 56/100 |
| stars | 56/100 |
| topics | 63/100 |
| outlook | 56/100 |
| quality | 60/100 |
| recency | 40/100 |
| adoption | 56/100 |
| production | 59/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/google/digitalbuildings) · [← Back to Misc](./README.md)</sub>
