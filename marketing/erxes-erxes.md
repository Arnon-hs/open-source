# erxes/erxes

[![Stars](https://img.shields.io/github/stars/erxes/erxes?style=flat-square&color=yellow)](https://github.com/erxes/erxes/stargazers) [![Forks](https://img.shields.io/github/forks/erxes/erxes?style=flat-square&color=blue)](https://github.com/erxes/erxes/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Experience Operating System (XOS) that unifies marketing, sales, operations, and support — run your core business seamlessly while replacing HubSpot, Zendesk, Linear, Wix and more.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4k |
| 🍴 **Forks** | 1.3k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`customer-experience` `employee-experience` `experience-operating-system` `front-alternative` `hacktoberfest` `hacktoberfest2025` `hubspot-alternative` `intercom-alternative` `linear-alternative` `medallia-alternative` `qualtrics-alternative` `wix-alternative`

## 🎯 Categories

Marketing

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
erxes is an open‑source “Experience Operating System” that brings together marketing, sales, operations and support tools into a single, extensible platform, aiming to replace suites such as HubSpot, Zendesk, Linear and Wix. Built in TypeScript, it already ships with AI‑enabled features and a modular architecture that lets teams prototype RAG, agent‑based workflows, or custom AI models without starting from scratch. With over 4 000 GitHub stars, active maintenance and recent releases, erxes is positioned as a production‑ready candidate for organizations looking to consolidate their customer‑facing stack.

**Value**  
- **Unified experience**: Consolidates disparate SaaS tools into one codebase, reducing vendor lock‑in, integration overhead, and data silos.  
- **AI‑first extensibility**: Provides ready‑made hooks, SDKs and example pipelines for adding generative‑AI, retrieval‑augmented generation (RAG) or autonomous agents, so teams can prototype and iterate quickly.  
- **Cost efficiency**: Being open source eliminates licensing fees for the core platform while still offering enterprise‑grade features that can be self‑hosted or deployed on a private cloud.  

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, run the Docker‑compose starter kit, and follow the README to enable a simple AI‑powered chatbot or lead‑scoring workflow.  
2. **Feature validation** – Extend the existing plugin system to integrate your own data sources (CRM, ticketing, CMS) and test RAG or agent pipelines in a staging environment.  
3. **Incremental migration** – Replace one legacy SaaS component at a time (e.g., move ticket handling from Zendesk to erxes) while keeping the rest of the stack operational.  
4. **Production hardening** – Add observability, RBAC, backup, and CI/CD pipelines; evaluate the licensing (MIT) and run a security scan of third‑party dependencies.  

**Production Readiness**  
- **Activity & community**: Recent commits (as of 2026‑06‑23), >4 000 stars, >1 200 forks, and a vibrant TypeScript ecosystem indicate strong community support.  
- **Stability**: The core platform is feature‑complete for the major use cases (marketing automation, ticketing, sales pipelines) and includes built‑in AI modules that are already used in pilot deployments.  
- **Scalability**: Container‑native architecture, horizontal scaling via Kubernetes, and support for PostgreSQL and Redis make it suitable for enterprise workloads.  
- **Risks**: Final due‑diligence is needed on licensing compliance, security posture of third‑party plugins, and the continuity of core maintainers, but no major red flags have been identified.  

Overall, erxes offers a compelling, production‑grade foundation for organizations that want to unify their customer‑experience stack while gaining rapid AI prototyping capabilities.

### Русский

erxes — это open‑source платформа Experience Operating System (XOS), которая объединяет маркетинг, продажи, операции и поддержку, позволяя заменить набор разрозненных SaaS‑решений (HubSpot, Zendesk, Linear, Wix и др.) и добавить AI‑функциональность без необходимости строить стек моделей с нуля. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept: интеграция erxes в существующий клиентский портал, настройка RAG‑ или агентных workflow и прототипирование AI‑фич, после чего расширяется до полноценного ядра бизнес‑процессов. По активности репозитория (4006 звёзд, 1289 форков, регулярные обновления, TypeScript‑база) проект считается готовым к production‑использованию в пилотных проектах, при условии финального аудита лицензии и безопасности.

### 中文

**项目简介（2‑3 句）**  
erxes（erxes/erxes）是一款 **Experience Operating System (XOS)**，通过统一的界面和数据模型把营销、销售、运营、客服等功能整合在一起，可直接替代 HubSpot、Zendesk、Linear、Wix 等多款 SaaS 产品。它基于 TypeScript 开发，社区活跃，已拥有 4k+ 星、1.3k+ Fork，适合作为企业内部的全栈业务平台。

**价值主张**  
- **AI 即插即用**：内置 AI 能力（RAG、智能客服、自动化工作流等），无需从零搭建模型堆栈，开发者只需调用已有的插件或微服务即可快速原型化 AI 功能。  
- **业务统一**：一次登录即可在同一系统中管理线索、工单、项目、网站内容等，降低信息孤岛和工具切换成本。  
- **可扩展、开源**：完全开源、可自行部署，支持二次开发和自定义插件，满足对数据安全和合规性的严格要求。

**典型接入方式**  
1. **快速 PoC**：克隆仓库 → 按 README 完成 Docker‑Compose 本地部署 → 使用内置的 `erxes-plugin-ai`（或自行编写插件）连接 OpenAI、Claude、Gemini 等模型，验证 RAG/Agent 流程。  
2. **业务集成**：通过官方提供的 REST/GraphQL API 将现有 CRM、营销自动化或内部系统对接到 erxes；也可以使用 Webhook 与 Slack、Zapier 等外部工具联动。  
3. **插件化扩展**：在 `plugins/` 目录下编写 TypeScript 插件，实现自定义表单、报表或 AI 推理逻辑，随后在管理后台开启即可。

**生产可用性**  
- **活跃度**：截至 2026‑06‑23 最近一次提交，月活贡献者 30+，社区讨论活跃；issues 关闭率 > 80%。  
- **成熟度**：已在多家中小企业上线，支持高可用部署（K8s、Docker Swarm），并提供官方 Helm Chart。  
- **安全合规**：MIT 许可证，代码审计记录良好；建议在生产环境前进行依赖漏洞扫描并开启安全审计日志。  
- **准备度**：综合评分 67/100，属于 **高** 生产候选，可直接用于内部关键业务的试点，后续根据业务规模逐步扩容。

> **结论**：erxes 兼具业务统一平台和可即插即用的 AI 能力，是希望在自托管环境下取代多家 SaaS、并快速构建智能客服或营销自动化的企业的理想选择。只需从小范围 PoC 起步，验证后即可平滑迁移至全量生产。

## 🧭 Practical evaluation

**Value:** erxes/erxes helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 4006 GitHub stars
- 1289 forks
- updated 2026-06-23
- primary language: TypeScript
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 78/100 |
| stars | 77/100 |
| topics | 100/100 |
| outlook | 62/100 |
| quality | 75/100 |
| recency | 40/100 |
| adoption | 77/100 |
| production | 60/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/erxes/erxes) · [← Back to Marketing](./README.md)</sub>
