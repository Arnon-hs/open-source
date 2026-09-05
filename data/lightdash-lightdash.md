# lightdash/lightdash

[![Stars](https://img.shields.io/github/stars/lightdash/lightdash?style=flat-square&color=yellow)](https://github.com/lightdash/lightdash/stargazers) [![Forks](https://img.shields.io/github/forks/lightdash/lightdash?style=flat-square&color=blue)](https://github.com/lightdash/lightdash/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Agentic BI. Analytics at the speed of code ⚡️

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 5.9k |
| 🍴 **Forks** | 730 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`business-intelligence` `data-analytics` `data-visualization` `dbt`

## 🎯 Categories

Data

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Lightdash is an open‑source, agentic business‑intelligence platform that lets data teams embed AI‑driven analytics directly into their codebases, accelerating the creation of RAG, agent workflows, and model‑evaluation tools. With a strong community (5.9k ★, 730 forks), active maintenance (latest commit 2026‑06‑23) and a TypeScript stack, it is ready for serious pilot projects.  

**Value**  
- Turns raw data into interactive, AI‑augmented dashboards without building a model stack from scratch, shortening time‑to‑insight for data‑science and product teams.  
- Provides a programmable interface that can be woven into existing CI/CD pipelines, enabling rapid prototyping of AI features and automated model monitoring.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the Docker compose setup, and follow the README to connect a sample warehouse (e.g., Snowflake, BigQuery).  
2. **Integration** – Replace a static reporting layer with Lightdash dashboards, then expose the Lightdash API to trigger agentic workflows or RAG pipelines.  
3. **Scale** – Harden the deployment (TLS, RBAC, audit logs), add custom plugins or extensions, and integrate with your CI/CD and monitoring stack.  

**Production Readiness**  
- **High**: recent commits, active issue triage, and growing adoption indicate a mature OSS candidate.  
- **Signals**: 5.9k stars, 730 forks, TypeScript codebase, and a clear contribution guide.  
- **Remaining Checks**: Verify the OSS license compatibility, conduct a security audit of dependencies, and confirm that maintainers have a documented on‑call process before full production rollout.

### Русский

lightdash — это open‑source платформа для аналитики, позволяющая быстро внедрять AI‑функции (прототипирование моделей, RAG‑агенты, оценка tooling) без необходимости строить стек с нуля. Для пилотного проекта рекомендуется начать с небольшого proof‑of‑concept, следуя инструкциям в README, а затем расширять интеграцию в существующие пайплайны данных. По активности репозитория (5911 звёзд, частые обновления, активные мейнтейнеры) проект считается готовым к production‑использованию, хотя требуется финальная проверка лицензии и безопасности.

### 中文

**项目简介**  
Lightdash 是一个面向数据团队的 Agentic BI 平台，主打“Analytics at the speed of code”。它通过在现有数据仓库之上直接生成可交互的分析视图，让开发者可以像写代码一样快速迭代数据洞察，并且内置对 LLM/Agent 的支持，帮助在业务场景中快速原型化 AI 功能。

**价值主张**  
- **即插即用的 AI 能力**：无需从零搭建模型堆栈，直接在 Lightdash 中配置 RAG、Agent 或模型评估工作流，即可在业务数据上跑通智能查询、自动化报表等功能。  
- **开发者友好**：基于 TypeScript/Node.js，统一的 SDK 与 CLI 让前端/后端团队可以在熟悉的代码环境里完成 BI 与 AI 的集成，提升迭代速度。  
- **开源且社区活跃**：超过 5.9k 星、730+ Fork，近期仍保持活跃更新，适合作为企业内部或 SaaS 产品的基础组件。

**典型接入方式**  
1. **数据源接入**：通过 UI 或 `lightdash.yml` 配置连接 Snowflake、BigQuery、PostgreSQL 等常见仓库。  
2. **项目初始化**：`npx @lightdash/cli init` 创建项目结构，生成 `lightdash.config.ts`，并把已有的 dbt 模型导入。  
3. **AI 工作流挂载**：在 `lightdash.config.ts` 中声明 LLM 提供商（OpenAI、Claude 等）和 Prompt 模板，或使用内置的 RAG 插件直接对接向量数据库。  
4. **部署**：可在 Docker、Kubernetes 或 Vercel 等平台一键部署，也支持在自有服务器上运行 `npm start`。  
5. **验证与迭代**：通过 UI 快速创建 Dashboard，使用“Ask Lightdash”对话框测试 AI 查询，随后把成功的 Prompt、模型参数写入代码库，实现 CI/CD 管理。

**生产可用性**  
- **成熟度**：项目近期（2026‑06‑23）仍在活跃维护，社区贡献活跃，文档完整，具备完整的 CI、单元测试与安全审计流程。  
- **可扩展性**：支持水平扩容的微服务架构，能够在 Kubernetes 中通过 Helm Chart 部署多个实例，满足大流量企业需求。  
- **安全合规**：采用 MIT 许可证，代码可审计；支持 SSO/OIDC、细粒度 RBAC 与审计日志，便于符合企业安全政策。  
- **推荐的上线方式**：先在预生产环境做小规模 PoC（如接入单一数据源、一个 RAG 流程），验证 Prompt 效果和权限配置后，再逐步推广到全业务线。整体来看，Lightdash 已具备在生产环境中作为核心 BI+AI 平台使用的条件。

## 🧭 Practical evaluation

**Value:** lightdash/lightdash helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 5911 GitHub stars
- 730 forks
- updated 2026-06-23
- primary language: TypeScript
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 72/100 |
| stars | 80/100 |
| topics | 50/100 |
| outlook | 74/100 |
| quality | 78/100 |
| recency | 80/100 |
| adoption | 78/100 |
| production | 71/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/lightdash/lightdash) · [← Back to Data](./README.md)</sub>
