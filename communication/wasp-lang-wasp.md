# wasp-lang/wasp

[![Stars](https://img.shields.io/github/stars/wasp-lang/wasp?style=flat-square&color=yellow)](https://github.com/wasp-lang/wasp/stargazers) [![Forks](https://img.shields.io/github/forks/wasp-lang/wasp?style=flat-square&color=blue)](https://github.com/wasp-lang/wasp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> The batteries-included full-stack framework for the AI era. Develop JS/TS web apps (React, Node.js, and Prisma) using declarative code that abstracts away complex full-stack features like auth, background jobs, RPC, email sending, end-to-end type safety, single-command deployment, and more.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 18.4k |
| 🍴 **Forks** | 1.5k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`javascript` `node` `open-source` `prisma` `react` `wasp` `web-app`

## 🎯 Categories

Communication · Frontend · Security

## 📝 Summary

### English

**Brief Summary**  
Wasp is a batteries‑included, full‑stack framework that lets developers build React/Node.js/Prisma web applications with a single declarative language. It abstracts away common back‑end concerns—authentication, background jobs, RPC, email, end‑to‑end type safety, and one‑command deployment—so teams can focus on adding AI capabilities such as RAG or autonomous agents without wiring the underlying stack from scratch.

**Value**  
- **Accelerated AI prototyping** – By handling the heavy lifting of full‑stack infrastructure, Wasp lets data scientists and engineers embed LLMs, retrieval‑augmented generation pipelines, or agent orchestration directly into a production‑grade web app.  
- **End‑to‑end type safety** – The same TypeScript types flow from the front‑end UI through the API to the database, reducing runtime bugs that often plague AI‑centric services.  
- **Unified deployment** – A single CLI command builds, containers, and deploys the whole stack, simplifying CI/CD for AI experiments and reducing operational overhead.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, follow the README to generate a minimal “Hello World” app, and replace the placeholder business logic with a simple AI call (e.g., OpenAI completion).  
2. **Incremental Integration** – Add Wasp modules for existing services (auth, Prisma models, background workers) to the current codebase, keeping the original UI while gradually migrating routes to Wasp’s declarative DSL.  
3. **Feature Expansion** – Leverage built‑in background jobs and RPC to orchestrate longer‑running model inference or RAG pipelines, and use the built‑in email/notification hooks for AI‑driven alerts.  
4. **Production Roll‑out** – Use Wasp’s single‑command deployment to push the fully integrated stack to your preferred cloud provider (e.g., Vercel, Railway, or a self‑hosted Kubernetes cluster).

**Production Readiness**  
- **Community & Activity** – 18 k+ stars, 1.5 k forks, recent commits (as of 2026‑06‑25) and an active issue tracker indicate a healthy ecosystem.  
- **Maturity** – The framework already supports authentication, Prisma ORM, background jobs, and type‑safe RPC, all of which are essential for production AI services.  
- **Risk Considerations** – No major licensing or metadata concerns were identified, but a final security audit of dependencies and confirmation of active maintainers is advisable before a large‑scale rollout.  

Overall, Wasp is production‑ready for pilots and can serve as a solid foundation for AI‑enhanced web applications, offering a fast path from prototype to a maintainable, fully managed stack.

### Русский

**wasp-lang/wasp** — это полнофункциональный open‑source фреймворк для разработки современных JS/TS‑приложений (React, Node.js, Prisma) с поддержкой AI‑фич, который скрывает сложную инфраструктуру (аутентификация, фоновые задачи, RPC, отправка писем, сквозная типобезопасность, однокомандный деплой) за декларативным кодом. Типичный сценарий — быстрый прототип AI‑функционала (RAG, агентные воркфлоу, оценка инструментов моделей) в небольшом proof‑of‑concept, после чего проект легко масштабируется до продакшн‑готового сервиса. По показателям активности (18447 звёзд, 1453 форка, регулярные обновления, сильный экосистемный отклик) и наличию типовой документации фреймворк считается готовым к серьёзным пилотным внедрениям, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句）**  
wasp‑lang/wasp 是面向 AI 时代的「电池全配」全栈框架，使用声明式 TypeScript/JavaScript 代码即可同时生成 React 前端、Node.js 后端以及 Prisma 数据层。它抽象并自动化了身份认证、后台任务、RPC、邮件发送、端到端类型安全、单命令部署等复杂功能，让开发者专注于 AI 功能本身。

**价值**  
- **快速落地 AI 能力**：无需从零搭建模型服务、数据库、认证等基础设施，直接在已有的全栈项目中加入 RAG、Agent 工作流或模型调用。  
- **端到端类型安全**：前后端共享同一套 TypeScript 类型，降低因类型不匹配导致的运行时错误。  
- **一键部署 & 运维简化**：通过单条 CLI 命令即可将完整的全栈应用部署到云平台，省去繁琐的 CI/CD 配置。  

**典型接入方式**  
1. **阅读 README 并创建最小示例**：使用 `wasp new my-app` 生成一个包含 React、Node、Prisma 的基础项目。  
2. **在业务模块中声明 AI 功能**：在 `.wasp` 文件里添加模型调用或 RAG 流程的声明式代码，框架会自动生成对应的 API 与前端 Hook。  
3. **本地运行 & 验证**：`wasp start` 启动完整的开发环境，前端、后端和数据库即刻可用，验证 AI 接口是否按预期工作。  
4. **单命令部署**：完成验证后，使用 `wasp deploy` 将应用推送到 Vercel、Fly.io 等支持的云平台，进入生产环境。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑25，项目拥有 18 447 ⭐、1 453 🍴，最近一次提交在同一天，说明社区和维护者仍在积极迭代。  
- **技术成熟度**：核心语言为 TypeScript，框架本身即提供完整的类型链，且已在多个公开案例中用于生产环境的 AI 原型与内部工具。  
- **安全与合规**：暂无重大元数据风险，仍需进一步审查许可证（MIT）以及依赖的安全报告，但整体安全姿态良好。  
- **适配度**：可通过小型 PoC（如仅实现一个模型调用）快速评估，与现有 React/Node/Prisma 项目无缝集成，风险可控。  

**结论**：wasp‑lang/wasp 具备高生产就绪度，适合作为 AI 功能的快速原型平台，也能在经过一次小规模验证后直接用于正式业务的全栈部署。

## 🧭 Practical evaluation

**Value:** wasp-lang/wasp helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 18447 GitHub stars
- 1453 forks
- updated 2026-06-25
- primary language: TypeScript
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 79/100 |
| stars | 91/100 |
| topics | 88/100 |
| outlook | 80/100 |
| quality | 88/100 |
| recency | 80/100 |
| adoption | 88/100 |
| production | 74/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/wasp-lang/wasp) · [← Back to Communication](./README.md)</sub>
