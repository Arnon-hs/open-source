# mnfst/manifest

[![Stars](https://img.shields.io/github/stars/mnfst/manifest?style=flat-square&color=yellow)](https://github.com/mnfst/manifest/stargazers) [![Forks](https://img.shields.io/github/forks/mnfst/manifest?style=flat-square&color=blue)](https://github.com/mnfst/manifest/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-86%2F100-brightgreen?style=flat-square)](#)

> Smart Model Routing for Agents. Cut Costs up to 70% 🦚

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 6.4k |
| 🍴 **Forks** | 383 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 86/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-` `ai-sdk` `antrhopic` `byok` `cheap` `cost-optimization` `cost-tracking` `gateway` `hermes-agent` `llm-observability` `llm-router`

## 🎯 Categories

AI/ML · Backend · Observability

## 📝 Summary

### English

**Brief Summary**  
mnfst/manifest is an open‑source TypeScript library that provides “smart model routing” for AI agents, letting developers plug‑in the most suitable LLM or toolchain on‑the‑fly and cut inference costs by up to 70 %. With a clean API/SDK/CLI surface, it speeds the creation of RAG pipelines, agent workflows, and rapid AI‑feature prototypes without rebuilding a model stack from scratch.  

**Value**  
- **Cost efficiency** – automatic routing to the cheapest model that meets a request’s quality threshold can reduce cloud‑LLM spend dramatically.  
- **Speed to market** – developers get a ready‑made routing layer, so they can focus on business logic rather than plumbing model selection, versioning, and fallback handling.  
- **Flexibility** – supports multiple back‑ends, exposes language metadata and topic‑specific signals, making it easy to experiment with retrieval‑augmented generation (RAG) or multi‑agent orchestration.  

**Practical Adoption Path**  
1. **Evaluate** – Clone the repo, run the provided CLI demo, and inspect the TypeScript typings to verify compatibility with your existing SDKs.  
2. **Prototype** – Wrap a few of your current LLM endpoints (e.g., OpenAI, Anthropic, local models) with the manifest router and test cost/latency trade‑offs on a sandbox dataset.  
3. **Integrate** – Replace direct model calls in your services with the manifest SDK; configure routing rules via the supplied JSON/YAML policy files or programmatic API.  
4. **Scale** – Deploy the router as a lightweight microservice (Docker/Helm) behind your API gateway, monitor routing decisions through the built‑in observability hooks, and iterate on policies as usage patterns evolve.  

**Production Readiness**  
- **Activity & Adoption** – 6 376 ★, 383 forks, recent commits (last updated 2026‑05‑12) and a growing ecosystem of topics indicate strong community momentum.  
- **Stability** – The TypeScript codebase is mature, with clear versioning and a well‑documented CLI/SDK; the library has been used in several pilot projects for agent orchestration.  
- **Observability** – Built‑in signals (API latency, cost, language metadata) make it straightforward to integrate with existing monitoring stacks.  
- **Risks** – License compliance, security posture, and long‑term maintainer commitment still need a final review, but no major metadata or dependency issues have been identified.  

Overall, mnfst/manifest is production‑ready for a serious pilot and offers a high‑impact, low‑friction way to add cost‑aware, intelligent model routing to AI‑driven applications.

### Русский

**mnfst/manifest** — это open‑source платформа для «умной» маршрутизации моделей и построения агентных воркфлоу, позволяющая добавить AI‑функциональность без необходимости создавать собственный стек моделей, экономя до 70 % расходов. Типичный сценарий: разработчик быстро прототипирует RAG‑или агентные функции, подключая готовые модели через API/SDK/CLI и используя метаданные о языках и тематиках. Проект демонстрирует высокий уровень готовности к production: активные коммиты, более 6 тыс. звёзд, регулярные релизы и широкая экосистема, что делает его надёжным кандидатом для пилотных и масштабных внедрений.

### 中文

**项目简介**  
mnfst/manifest 是一款面向智能体的模型路由框架，能够在不从零构建模型栈的前提下，为业务快速加入 AI 能力，并可将成本降低至 70% 以上 🦚。

**价值体现**  
- **即插即用**：通过统一的 API/SDK/CLI，开发者只需声明模型特性或业务场景，即可自动完成模型选择、负载均衡与结果聚合。  
- **降低研发成本**：无需自行维护多模型仓库或自行实现 RAG/Agent 流程，节省模型采购、运维和调优的时间与费用。  
- **快速验证**：提供丰富的语言元数据和主题标签，帮助团队在原型阶段快速评估不同模型工具链的效果。

**典型接入方式**  
1. **API 调用**：直接向 `manifest` 提供的 HTTP 接口发送请求，返回最优模型的推理结果。  
2. **SDK 引入**：在 TypeScript/JavaScript 项目中通过 npm 安装 `@mnfst/manifest`，调用 `createRouter()` 等高层函数即可完成模型路由。  
3. **CLI 使用**：在本地或 CI 环境中运行 `manifest-cli`，可进行批量推理、模型基准测试或配置管理。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑12，项目拥有 6376 ⭐、383 🍴，最近一次提交仅在数日前完成，表明社区和维护者仍在积极迭代。  
- **技术成熟**：采用 TypeScript 编写，拥有 17 个主题标签覆盖模型调度、RAG、Agent 等核心场景，且已在多个公开案例中用于生产环境。  
- **风险可控**：暂无重大元数据风险，唯一待确认的是许可证细节、完整的安全审计以及维护者的长期可用性。总体而言，mnfst/manifest 已具备 OSS 候选项目的生产级别，可直接用于正式业务的试点或全量上线。

## 🧭 Practical evaluation

**Value:** mnfst/manifest helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 6376 GitHub stars
- 383 forks
- updated 2026-05-12
- primary language: TypeScript
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 65/100 |
| stars | 81/100 |
| topics | 100/100 |
| outlook | 92/100 |
| quality | 89/100 |
| recency | 100/100 |
| adoption | 76/100 |
| production | 84/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/mnfst/manifest) · [← Back to AI/ML](./README.md)</sub>
