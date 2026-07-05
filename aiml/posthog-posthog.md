# PostHog/posthog

[![Stars](https://img.shields.io/github/stars/PostHog/posthog?style=flat-square&color=yellow)](https://github.com/PostHog/posthog/stargazers) [![Forks](https://img.shields.io/github/forks/PostHog/posthog?style=flat-square&color=blue)](https://github.com/PostHog/posthog/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> 🦔 PostHog is an all-in-one developer platform for building successful products. We offer product analytics, web analytics, session replay, error tracking, feature flags, experimentation, surveys, data warehouse, a CDP, and an AI product assistant to help debug your code, ship features faster, and keep all your usage and customer data in one stack.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 35.1k |
| 🍴 **Forks** | 2.9k |
| 💻 **Language** | Python |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-06-23 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ab-testing` `ai-analytics` `analytics` `cdp` `data-warehouse` `experiments` `feature-flags` `javascript` `product-analytics` `python` `react` `session-replay`

## 🎯 Categories

AI/ML · Frontend · DevTools · Data · Database

## 📝 Summary

### English

**Brief Summary**  
PostHog is an open‑source, all‑in‑one developer platform that bundles product analytics, session replay, error tracking, feature flags, experimentation, surveys, a data warehouse, a CDP, and an AI‑powered product assistant. It lets teams keep every usage and customer signal in a single stack while adding AI capabilities without building a model stack from scratch.

**Value**  
- **Unified data & tooling** – eliminates the need for multiple SaaS products; developers can collect, analyze, and act on product data from one codebase.  
- **AI‑enabled insights** – the built‑in AI assistant can surface bugs, suggest feature improvements, and help generate code, accelerating development cycles.  
- **Extensible & self‑hosted** – because it’s open source and written in Python, teams can run it on‑premise, customize pipelines, and integrate with existing data warehouses or CDPs.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – clone the repo, follow the quick‑start README, and run the Docker compose stack locally to ingest a small amount of event data.  
2. **Pilot integration** – add the PostHog SDK to one or two services (frontend and backend) to stream real events; enable the AI assistant for debugging and feature‑flag experiments.  
3. **Scale & customize** – connect PostHog to your data warehouse or CDP, configure feature flags, and optionally extend the AI workflows (e.g., RAG or agent pipelines) using the provided plugin framework.  
4. **Full production rollout** – migrate the Docker deployment to a managed Kubernetes or on‑premise environment, set up role‑based access, monitoring, and backup policies.

**Production Readiness**  
- **High**: 35 k+ GitHub stars, 2.9 k forks, recent commits (as of 2026‑06‑23), active community, and a mature Python codebase.  
- **Signals**: Strong adoption across startups and enterprises, comprehensive documentation, and built‑in security features (e.g., GDPR‑compliant data handling).  
- **Remaining checks**: Verify licensing compatibility, conduct a security audit of third‑party dependencies, and confirm long‑term maintainer commitment before a mission‑critical launch.  

Overall, PostHog offers a production‑grade, open‑source platform that consolidates analytics and AI assistance, making it a solid candidate for a serious pilot and eventual full‑scale deployment.

### Русский

PostHog — это открытая платформа‑единорог, объединяющая аналитику продукта, отслеживание ошибок, feature‑flags, эксперименты, опросы и AI‑ассистента, позволяя хранить все данные о пользователях и использовании в едином стеке. Типичный сценарий — запуск небольшого proof‑of‑concept, например прототипа AI‑фичи или RAG‑агента, с последующей интеграцией через готовый README и API. По оценке готовности к продакшну проект находится на высоком уровне: активные коммиты, более 35 тыс. звёзд, широкое сообщество и стабильный Python‑бэкенд делают его надёжным кандидатом для серьёзного пилотного внедрения.

### 中文

**项目简介**  
PostHog 是一站式的开发者平台，提供产品分析、会话回放、错误追踪、功能开关、实验、调查、数据仓库、CDP 以及 AI 助手等能力，帮助团队快速调试代码、发布新功能，并在同一套栈中统一管理所有使用和客户数据。

**价值**  
- **全链路可观测**：从埋点到分析再到实验，所有数据在同一系统内闭环，降低了工具碎片化带来的运营成本。  
- **AI 能力即插即用**：内置 AI 助手可以直接在平台上进行代码调试、功能推荐或 RAG/Agent 工作流原型，免去自行搭建模型堆栈的前期投入。  
- **自托管与云端双选**：开源代码可自行部署，满足合规和隐私要求；同时提供托管 SaaS，快速上线。  

**典型接入方式**  
1. **安装 SDK**：在前端（JavaScript/TypeScript）或后端（Python、Node、Go 等）项目中引入对应的 PostHog SDK，配置项目 API key 与服务器地址。  
2. **定义事件**：通过 `posthog.capture(eventName, properties)` 记录业务关键事件；可选开启会话回放、错误捕获等插件。  
3. **开启功能模块**：在 PostHog 控制台打开 Feature Flags、Experiments、Surveys 等模块，使用 UI 或 API 动态控制功能发布与 A/B 测试。  
4. **AI 助手集成**：在项目代码或 CI/CD 流程中调用 PostHog 提供的 AI API（如 `POST /api/ai/debug`），实现自动化调试或生成分析报告。  

**生产可用性**  
- **活跃度高**：35145+ 星、2884+ Fork，最近一次提交在 2026‑06‑23，社区和官方维护者均保持活跃。  
- **成熟度**：提供完整的文档、Docker/Helm 部署方案以及多语言 SDK，已在多家互联网公司生产环境中使用。  
- **安全与合规**：开源许可证为 MIT，代码审计和安全报告公开，可自行审查或使用官方托管版的安全保障。  
- **推荐做法**：先在非关键业务做一个小型 PoC（如埋点 + 基础分析），确认数据流和 AI 助手的效果后，再逐步扩展到全链路监控与实验平台。  

综上，PostHog 具备高生产可用性，适合作为企业内部的统一数据与 AI 平台，接入门槛低，且能够在保持数据自主可控的前提下快速交付产品洞察和智能化功能。

## 🧭 Practical evaluation

**Value:** PostHog/posthog helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 35145 GitHub stars
- 2884 forks
- updated 2026-06-23
- primary language: Python
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 87/100 |
| stars | 97/100 |
| topics | 100/100 |
| outlook | 87/100 |
| quality | 97/100 |
| recency | 100/100 |
| adoption | 94/100 |
| production | 85/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/PostHog/posthog) · [← Back to AI/ML](./README.md)</sub>
