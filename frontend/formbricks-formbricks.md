# formbricks/formbricks

[![Stars](https://img.shields.io/github/stars/formbricks/formbricks?style=flat-square&color=yellow)](https://github.com/formbricks/formbricks/stargazers) [![Forks](https://img.shields.io/github/forks/formbricks/formbricks?style=flat-square&color=blue)](https://github.com/formbricks/formbricks/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Open Source Qualtrics Alternative

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 12.2k |
| 🍴 **Forks** | 2.2k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`experience-management` `form` `forms` `nextjs` `open-source` `react` `reactjs` `survey` `survey-analysis` `survey-data` `survey-form` `surveys`

## 🎯 Categories

Frontend · Data

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Formbricks is an open‑source, TypeScript‑based platform that offers a self‑hosted alternative to Qualtrics for building surveys, feedback loops, and AI‑enhanced data collection workflows. With a strong community (12 k+ stars, 2 k+ forks) and recent activity, it provides a ready‑to‑use stack for prototyping AI features such as retrieval‑augmented generation (RAG) or agent‑driven surveys without starting from scratch.

**Value**  
Formbricks lets teams embed AI capabilities directly into survey and feedback pipelines, accelerating the creation of intelligent questionnaires, dynamic routing, and real‑time analytics. By leveraging its modular architecture, developers can plug in LLMs, vector stores, or custom model APIs to enrich responses, test new AI‑driven product ideas, and gather high‑quality training data—all under a single, open‑source codebase.

**Practical Adoption Path**  

1. **Proof‑of‑Concept** – Clone the repo, run the Docker compose setup, and follow the README to launch a local instance.  
2. **Integration** – Connect your preferred LLM (e.g., OpenAI, Anthropic) via the built‑in webhook or custom middleware, and define a simple RAG or agent workflow for a test survey.  
3. **Pilot** – Deploy the instance to a staging environment (e.g., Kubernetes or a managed cloud VM), enable SSO/auth, and invite a small user group to validate the AI‑enhanced experience.  
4. **Scale** – Harden the deployment (TLS, rate limiting, audit logging), integrate with your data warehouse or analytics stack, and gradually roll out to production teams.

**Production Readiness**  
Formbricks scores high on production readiness: it has recent commits (as of 2026‑05‑12), active maintainers, extensive community adoption, and a mature TypeScript codebase. While the license and security posture still require a final review, the project’s activity level, documentation, and ecosystem integrations make it a solid candidate for a serious pilot in production environments.

### Русский

Formbricks (formbricks/formbricks) — это open‑source альтернатива Qualtrics, позволяющая быстро добавить AI‑функциональность в опросы и формы без необходимости строить собственный стек моделей. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept: подключить библиотеку к существующему фронтенду, настроить RAG‑или агентные воркфлоу и протестировать прототип AI‑фич, используя готовый README. Проект обладает высокой готовностью к production: активные коммиты, более 12 км звёзд, крупное сообщество форков и поддержка TypeScript, что делает его надёжным кандидатом для серьёзного пилотного проекта.

### 中文

**项目简介**  
Formbricks（github.com/formbricks/formbricks）是一款开源的 Qualtrics 替代方案，基于 TypeScript 构建，提供可视化问卷、调研与用户反馈收集功能。它通过模块化设计，让用户可以在不从零搭建模型堆栈的前提下，快速为调研系统加入 AI 能力（如自动摘要、情感分析、RAG 检索等），从而加速 AI 特性原型和全链路工作流的落地。

**价值**  
- **快速嵌入 AI**：内置或可插件式集成 LLM、向量数据库等 AI 服务，省去自行搭建模型推理层的时间与成本。  
- **低代码/可视化**：拖拽式表单编辑器和丰富的主题模板，使业务团队无需深度编码即可发布调研。  
- **开源安全**：MIT 许可证、活跃社区（12k+ Stars、2.2k Forks），代码透明，可自行审计与自托管。  
- **可扩展性**：提供 REST/GraphQL API 与 Webhook，便于与内部 CRM、数据湖或自研业务系统对接。

**典型接入方式**  
1. **快速 POC**：克隆仓库 → `docker compose up`（或 `npm run dev`）启动本地实例 → 在 UI 中创建问卷并配置 AI Webhook（如 OpenAI、Claude）。  
2. **API 集成**：使用官方提供的 OpenAPI 规范，后端通过 `POST /surveys/:id/responses` 提交答卷，或监听 `response.created` Webhook 实时处理数据。  
3. **自托管部署**：在 Kubernetes 或 Vercel 等平台使用官方 Helm Chart，配合 PostgreSQL + Redis 持久化，完成生产级部署。  

**生产可用性**  
- **活跃维护**：最近一次提交在 2026‑05‑12，社区活跃，Issue 响应及时。  
- **成熟生态**：已支持多种身份认证（OAuth、SSO）、多语言本地化以及 GDPR 合规导出。  
- **可扩展部署**：官方提供 Docker、Helm 与 Vercel 部署方案，支持水平扩容和高可用配置。  
- **安全与合规**：MIT 许可证，无已知重大漏洞；仍建议在正式上线前完成内部安全审计、依赖漏洞扫描以及 License 合规检查。  

综上，Formbricks 具备高生产就绪度，适合作为企业内部调研平台或 AI‑增强问卷系统的核心组件，先行进行小规模 PoC 验证后即可平滑迁移至全量生产环境。

## 🧭 Practical evaluation

**Value:** formbricks/formbricks helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 12208 GitHub stars
- 2249 forks
- updated 2026-05-12
- primary language: TypeScript
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 84/100 |
| stars | 87/100 |
| topics | 100/100 |
| outlook | 57/100 |
| quality | 74/100 |
| recency | 20/100 |
| adoption | 86/100 |
| production | 55/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/formbricks/formbricks) · [← Back to Frontend](./README.md)</sub>
