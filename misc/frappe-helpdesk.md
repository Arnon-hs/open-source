# frappe/helpdesk

[![Stars](https://img.shields.io/github/stars/frappe/helpdesk?style=flat-square&color=yellow)](https://github.com/frappe/helpdesk/stargazers) [![Forks](https://img.shields.io/github/forks/frappe/helpdesk?style=flat-square&color=blue)](https://github.com/frappe/helpdesk/network) [![Language](https://img.shields.io/badge/lang-Vue-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Modern, Streamlined, Free and Open Source Customer Service Software

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.1k |
| 🍴 **Forks** | 790 |
| 💻 **Language** | Vue |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`customer-support` `foss` `frappe` `helpdesk` `helpscout` `issue-tracker` `javascript` `python` `ticketing` `ticketing-system` `typescript` `vue3`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
frappe/helpdesk is a modern, free and open‑source customer‑service platform built with Vue that lets teams add AI capabilities—such as retrieval‑augmented generation (RAG) or autonomous agent workflows—without having to assemble a model stack from scratch. With over 3 000 stars, frequent commits, and a thriving ecosystem, it is ready for pilot projects and can be evaluated through a small proof‑of‑concept.  

**Value**  
- **Accelerated AI integration** – plug‑in LLM‑driven assistants, knowledge‑base search, or ticket‑routing bots directly into an existing help‑desk UI, saving months of engineering effort.  
- **Open‑source flexibility** – the codebase is fully visible and extensible, allowing teams to customize the AI pipelines, data privacy controls, and UI to match internal policies.  
- **Ecosystem leverage** – built on the Frappe framework, it can reuse existing ERPNext modules, authentication, and reporting tools, reducing duplicate development.  

**Practical Adoption Path**  
1. **Read the README & quick‑start** – spin up the Docker compose setup locally to verify the baseline help‑desk works.  
2. **Proof of concept** – add a minimal AI plugin (e.g., a LangChain‑based RAG endpoint) to a single ticket‑type workflow and test with a sandbox dataset.  
3. **Iterate & secure** – harden the deployment (TLS, secret management), run static security scans, and evaluate licensing compliance.  
4. **Pilot rollout** – deploy to a staging environment, integrate with your existing ticket sources (email, chat), and collect user feedback before scaling.  

**Production Readiness**  
- **Activity & adoption** – recent commits (as of 2026‑05‑11), >3 k stars, ~800 forks, and active community contributions indicate a healthy project.  
- **Stability** – core help‑desk features are mature; AI extensions are optional and can be introduced incrementally.  
- **Risk considerations** – while no major metadata or licensing red flags appear, a final security audit and confirm‑ation of maintainer responsiveness are recommended before full production use.  

Overall, frappe/helpdesk offers a solid, production‑grade foundation for teams that want to prototype and eventually ship AI‑enhanced customer‑service experiences with minimal upfront model engineering.

### Русский

**frappe/helpdesk** — современный, бесплатный и открытый клиентский сервис, построенный на Vue и готовый к расширению AI‑функциональностью без необходимости создавать стек моделей с нуля. Типичный сценарий внедрения: в рамках небольшого proof‑of‑concept добавить RAG‑поиск или агентные воркфлоу, используя готовый README и интеграцию с существующей инфраструктурой. Проект обладает высокой готовностью к production: активные коммиты, более 3000 звёзд, широкое принятие в сообществе и надёжный экосистемный контекст, требующий лишь окончательной проверки лицензии и безопасности.

### 中文

**项目简介**  
frappe/helpdesk 是一款现代化、轻量级且完全开源的客服系统，基于 Vue 前端和 Frappe 框架构建，提供工单管理、自动分配、知识库等完整的客户服务功能。

**价值**  
- **快速赋能 AI**：内置 API 与插件机制，可直接在工单流中接入大模型（如 LLM）实现智能回复、自动分类或 RAG（检索增强生成）等功能，无需从零搭建模型堆栈。  
- **低成本实验平台**：适合作为 AI 客服原型的实验环境，帮助团队快速验证模型效果、调优工作流。  
- **社区与生态**：拥有 3k+ 星、近 800 个 fork，活跃的社区提供丰富的插件、模板和文档，降低二次开发成本。

**典型接入方式**  
1. **小范围 PoC**：在本地或测试环境部署 Helpdesk（Docker Compose / 官方 Helm Chart），先确认系统能正常运行。  
2. **API 调用**：通过 Helpdesk 提供的 REST/Webhook 接口，在工单创建或状态变更时触发外部 AI 服务（如 OpenAI、Claude、Gemini）。  
3. **插件/脚本**：在 Frappe 框架的自定义脚本或 App 中编写调用模型的逻辑，实现自动回复、相似工单检索等功能。  
4. **RAG 集成**：将企业文档同步到向量数据库（如 Pinecone、Qdrant），在工单处理时通过 Helpdesk 的自定义字段或按钮触发检索‑生成流程。

**生产可用性**  
- **活跃维护**：截至 2026‑05‑11 最近一次提交，项目仍在持续更新，社区活跃度高。  
- **成熟度**：核心功能已在多个企业级部署中使用，具备完整的权限体系、审计日志和多语言支持。  
- **可扩展性**：基于 Frappe 的插件机制，能够平滑接入内部身份认证、监控告警以及 CI/CD 流程。  
- **风险**：需进一步确认许可证兼容性（MIT），并对依赖的第三方库进行安全审计；但整体安全姿态良好，已具备在生产环境进行正式试点的条件。

## 🧭 Practical evaluation

**Value:** frappe/helpdesk helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 3127 GitHub stars
- 790 forks
- updated 2026-05-11
- primary language: Vue
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 72/100 |
| stars | 74/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 83/100 |
| recency | 80/100 |
| adoption | 74/100 |
| production | 75/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/frappe/helpdesk) · [← Back to Misc](./README.md)</sub>
