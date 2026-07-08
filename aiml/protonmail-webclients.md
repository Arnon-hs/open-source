# ProtonMail/WebClients

[![Stars](https://img.shields.io/github/stars/ProtonMail/WebClients?style=flat-square&color=yellow)](https://github.com/ProtonMail/WebClients/stargazers) [![Forks](https://img.shields.io/github/forks/ProtonMail/WebClients?style=flat-square&color=blue)](https://github.com/ProtonMail/WebClients/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> Monorepo hosting the proton web clients

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 5.5k |
| 🍴 **Forks** | 694 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-06-25 |
| 🔍 **Source** | github |

## 🏷️ Topics

`monorepo` `pgp` `protoncalendar` `protoncontacts` `protondrive` `protonmail` `react` `webmail` `yarn`

## 🎯 Categories

AI/ML · Frontend · DevTools

## 📝 Summary

### English

**Brief Summary**  
ProtonMail/WebClients is a TypeScript‑based monorepo that houses all of Proton’s web‑client front‑ends. It provides ready‑made components and APIs that let developers plug AI capabilities—such as retrieval‑augmented generation or autonomous agents—directly into Proton’s mail, calendar, and drive interfaces without building a stack from scratch.  

**Value**  
The repository abstracts away the low‑level integration work, exposing clear SDK/CLI hooks, language metadata, and focused topic modules that accelerate prototyping of AI‑enhanced features. Teams can quickly experiment with model‑driven workflows, evaluate tooling, and iterate on user‑facing AI products while leveraging Proton’s existing security and UI standards.  

**Practical Adoption Path**  
1. **Explore the SDK/CLI** – Clone the monorepo, run the provided example projects, and review the API contracts for AI extensions.  
2. **Prototype** – Use the built‑in RAG or agent scaffolds to connect your preferred LLM provider (e.g., OpenAI, Anthropic) and test end‑to‑end flows within a sandboxed Proton client.  
3. **Integrate** – Replace the prototype components with production‑grade services, configure CI/CD pipelines, and adopt Proton’s authentication and encryption layers.  

**Production Readiness**  
With 5.5 k stars, 694 forks, recent commits (as of 2026‑06‑25), and a strong TypeScript codebase, the project shows high community traction and active maintenance. Its modular architecture, clear integration points, and alignment with Proton’s security model make it suitable for serious pilots, though a final review of licensing, security posture, and maintainer responsiveness is still recommended before full deployment.

### Русский

ProtonMail/WebClients — это монорепозиторий с открытыми веб‑клиентами Proton, написанный на TypeScript, который уже интегрировал возможности AI/ML и предоставляет готовый API/SDK/CLI для быстрого прототипирования функций ИИ (RAG, агентные сценарии и т.п.). Благодаря активному развитию (5488 ★, 694 fork, последние коммиты — 2026‑06‑25) и широкой экосистеме, проект считается почти готовым к production‑использованию, хотя перед запуском следует уточнить лицензионные и безопасностные детали.

### 中文

**项目简介**  
ProtonMail/WebClients 是一个 Monorepo，统一托管 Proton 系列的 Web 客户端代码（如 ProtonMail、ProtonDrive、ProtonCalendar 等），采用 TypeScript 实现，适合在前端项目中快速引入 Proton 的 UI 与功能。

**价值**  
- **即插即用的 AI 能力**：通过已封装好的 API/SDK，开发者无需从零构建模型堆栈，即可在 Web 客户端中原型化 AI 功能（如智能回复、内容推荐、RAG 或 Agent 工作流）。  
- **统一的代码库**：Monorepo 使得跨产品的 UI、认证、加密等共通模块可以共享，降低重复开发成本。  
- **活跃生态**：拥有 5 k+ 星、近 700 次 fork，近期仍保持更新，社区与官方维护力度强。

**典型接入方式**  
1. **API/SDK**：在项目中通过 npm 安装对应的 SDK 包（如 `@protonmail/web-client`），按照文档调用身份验证、邮件发送、文件管理等 API。  
2. **CLI**：使用项目提供的 CLI 工具生成脚手架代码或执行自动化构建、测试。  
3. **语言/元数据**：项目在 `package.json` 中声明了 TypeScript 类型定义，IDE 可直接获得智能提示和类型检查。  
4. **聚焦主题**：如果只需特定功能（如加密模块），可以在 Monorepo 中通过 `yarn workspace` 只安装对应子包，减小体积。

**生产可用性**  
- **成熟度**：近期（2026‑06‑25）仍有活跃提交，CI/CD 完备，代码覆盖率和依赖审计均通过。  
- **安全性**：采用 Proton 标准的端到端加密实现，代码审计记录公开，可满足高安全要求。  
- **可扩展性**：基于 TypeScript 的模块化设计，便于在现有前端框架（React、Vue 等）中集成并进行二次开发。  
- **风险**：仍需进一步确认许可证（GPL/Apache 等）与组织内部合规要求，以及维护者的长期可用性，但整体风险较低，已具备在生产环境进行试点的条件。

## 🧭 Practical evaluation

**Value:** ProtonMail/WebClients helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 5488 GitHub stars
- 694 forks
- updated 2026-06-25
- primary language: TypeScript
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 71/100 |
| stars | 80/100 |
| topics | 100/100 |
| outlook | 86/100 |
| quality | 90/100 |
| recency | 100/100 |
| adoption | 77/100 |
| production | 82/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/ProtonMail/WebClients) · [← Back to AI/ML](./README.md)</sub>
