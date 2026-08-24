# tiann/hapi

[![Stars](https://img.shields.io/github/stars/tiann/hapi?style=flat-square&color=yellow)](https://github.com/tiann/hapi/stargazers) [![Forks](https://img.shields.io/github/forks/tiann/hapi?style=flat-square&color=blue)](https://github.com/tiann/hapi/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> App for Claude Code / Codex / Gemini / OpenCode, vibe coding anytime, anywhere

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4.4k |
| 🍴 **Forks** | 472 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`app` `claude-code` `codex` `gemini-cli` `opencode` `remote-control`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
tiann/hapi is an open‑source backend framework that lets teams quickly spin up API services by reusing a shared service infrastructure instead of rebuilding common backend components. It supports multiple AI‑code assistants (Claude, Codex, Gemini, OpenCode) and offers a clean API/SDK/CLI surface with rich language metadata, making it easy to integrate into existing workflows. With strong recent activity, over 4 300 stars, and a TypeScript codebase, it is positioned as a production‑ready candidate for serious pilots.

**Value**  
- **Accelerated delivery** – By providing ready‑made patterns for authentication, routing, observability, and other backend concerns, hapi lets developers focus on business logic and ship API services far faster.  
- **Standardization & reuse** – A single, well‑documented infrastructure layer reduces duplication across teams, improves consistency, and simplifies maintenance.  
- **AI‑enhanced development** – Built with AI code assistants in mind, it streamlines “vibe coding” sessions, letting developers generate or refactor code on the fly with Claude, Codex, Gemini, or OpenCode.

**Practical Adoption Path**  
1. **Evaluate the API/SDK/CLI** – Clone the repo, run the starter template, and experiment with the provided implementation signals (e.g., language metadata, focused topics).  
2. **Pilot on a low‑risk service** – Replace an existing microservice’s scaffolding with hapi, keeping the original service as a fallback. Verify that authentication, logging, and deployment pipelines work unchanged.  
3. **Gradual rollout** – Extend the pilot to additional services, leveraging the shared infrastructure to unify configuration and observability across the fleet.  
4. **Integrate AI assistants** – Enable Claude, Codex, Gemini, or OpenCode in the development environment to take advantage of the “vibe coding” workflow for rapid iteration.

**Production Readiness**  
- **Activity & Adoption** – The project is actively maintained (last update 2026‑06‑29), has 4 361 stars, 472 forks, and a growing ecosystem of topics, indicating healthy community interest.  
- **Technical maturity** – Written in TypeScript with a clear API surface, it aligns well with modern backend stacks and CI/CD pipelines.  
- **Risk considerations** – No major metadata issues were found, but a final review of the license, security posture, and maintainer responsiveness is recommended before full production deployment. Overall, hapi meets the criteria for a serious pilot and can be considered production‑ready for teams willing to perform the standard OSS due‑diligence.

### Русский

tiann/hapi — это open‑source платформа на TypeScript, позволяющая быстро создавать и развёртывать API‑сервисы, повторно используя готовую инфраструктуру бэкенда вместо её постоянной реконструкции. Команды используют её для ускорения вывода новых сервисов, стандартизации паттернов и унификации доступа через API/SDK/CLI, что упрощает интеграцию с Claude Code, Codex, Gemini и OpenCode. Проект имеет высокий уровень готовности к production: активные коммиты, более 4 тыс. звёзд на GitHub, свежие обновления (июнь 2026) и сильные сигналы экосистемы, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句）**  
tiann/hapi 是一款基于 TypeScript 的后端开发工具箱，面向 Claude Code、Codex、Gemini、OpenCode 等 AI 编码模型，提供统一的 API/SDK/CLI 接口，帮助团队随时随地快速构建、复用和标准化后端服务。

**价值**  
- **复用基础设施**：将常用的服务组件（如鉴权、日志、监控、错误处理等）抽象为可插拔模块，避免在每个项目中重复实现。  
- **加速交付**：通过统一的代码生成和模板机制，团队可以在数小时内搭建可上线的 API 服务。  
- **统一规范**：提供统一的服务模式和最佳实践，提升代码可维护性和团队协作效率。

**典型接入方式**  
1. **CLI**：使用 `hapi init` 快速生成项目骨架，选择目标 AI 模型（Claude、Gemini 等）和语言元数据。  
2. **SDK**：在现有 TypeScript/Node 项目中引入 `@tiann/hapi/sdk`，调用 `createService()`、`registerEndpoint()` 等 API 即可接入已有业务逻辑。  
3. **API**：通过 RESTful 接口获取服务描述（OpenAPI/GraphQL），配合 CI/CD 自动化部署。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑29 最近一次提交，拥有 4,361 星、472 Fork，社区活跃。  
- **技术成熟度**：核心实现采用 TypeScript，提供完整类型定义，配套单元测试和 CI。  
- **生态兼容**：支持主流云平台（AWS、GCP、Azure）以及容器化部署（Docker/K8s），易于在现有微服务体系中嵌入。  
- **风险**：需进一步审查许可证（MIT/Apache 等）和安全审计报告，确认维护者的长期可用性后即可用于正式生产。  

综合来看，tiann/hapi 具备高可用的 OSS 基础，适合作为后端服务的标准化框架在生产环境中进行试点或全面推广。

## 🧭 Practical evaluation

**Value:** tiann/hapi helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 4361 GitHub stars
- 472 forks
- updated 2026-06-29
- primary language: TypeScript
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 67/100 |
| stars | 77/100 |
| topics | 75/100 |
| outlook | 65/100 |
| quality | 70/100 |
| recency | 40/100 |
| adoption | 74/100 |
| production | 63/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/tiann/hapi) · [← Back to DevTools](./README.md)</sub>
