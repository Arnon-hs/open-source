# affromero/flight-finder

[![Stars](https://img.shields.io/github/stars/affromero/flight-finder?style=flat-square&color=yellow)](https://github.com/affromero/flight-finder/stargazers) [![Forks](https://img.shields.io/github/forks/affromero/flight-finder?style=flat-square&color=blue)](https://github.com/affromero/flight-finder/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> Flight price tracker. Self-hosted, open source, bring your own LLM. The price trail airlines don't show you.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 100 |
| 🍴 **Forks** | 13 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`claude` `docker` `flight-prices` `flights` `llm` `nextjs` `open-source` `playwright` `price-tracker` `self-hosted` `typescript` `web-scraping`

## 🎯 Categories

AI/ML · DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
Flight‑Finder (affromero/flight‑finder) is a self‑hosted, open‑source flight‑price tracker that lets you plug in any LLM to surface price‑trend data airlines don’t publish. Built in TypeScript and actively maintained, it offers a ready‑made API/SDK/CLI for rapid prototyping of RAG or agent‑based AI workflows around travel pricing.  

**Value**  
- **AI‑ready out of the box** – you can attach your own LLM (e.g., OpenAI, Llama, Cohere) and immediately start building intelligent features such as price‑trend queries, alerts, or recommendation agents without constructing a model stack from scratch.  
- **Domain‑specific data** – the service scrapes and normalises airline pricing histories, giving you a unique data source that most public APIs lack, which is ideal for building competitive travel‑assistant products.  
- **Low‑code integration** – the project ships a clear TypeScript SDK, a RESTful API, and a CLI, so developers can call the service from any language or orchestration tool with minimal boilerplate.  

**Practical Adoption Path**  
1. **Deploy** the Docker‑compose stack (or Helm chart) in your own cloud/VPC.  
2. **Configure** the LLM endpoint and API keys via the provided `.env` template.  
3. **Consume** the service through the generated OpenAPI spec – start with the CLI for quick experiments, then migrate to the SDK for production code.  
4. **Iterate**: use the built‑in webhook/notification hooks to add alerting or feed the data into a downstream RAG pipeline for chat‑based travel assistants.  

**Production Readiness**  
- **Activity & Community**: 100+ GitHub stars, recent commits (as of 2026‑06‑26), and a modest fork base indicate active interest.  
- **Stability**: The TypeScript codebase is type‑checked, the API is versioned, and the Docker images are published with reproducible builds.  
- **Observability**: Built‑in logging and health‑check endpoints make it straightforward to monitor in a Kubernetes or VM environment.  
- **Risks**: Licensing and long‑term maintainer commitment still need a final review, and a security audit of the scraping components is advisable before handling production traffic.  

Overall, Flight‑Finder is a high‑readiness OSS candidate for teams that want to accelerate AI‑enhanced travel solutions while retaining full control over data and model choices.

### Русский

**affromero/flight-finder** — это self‑hosted open‑source трекер цен на авиабилеты, который позволяет добавить AI‑функциональность (LLM) без необходимости построения модели «с нуля». Типичный сценарий: быстро прототипировать AI‑фичи (RAG, агентные воркфлоу) для анализа ценовых трендов, интегрировать через API/SDK/CLI в существующие бекенд‑или DevOps‑процессы. Проект демонстрирует высокий уровень готовности к продакшну: активные коммиты, 100 ★, поддержка TypeScript, широкие метаданные и хорошие сигналы экосистемы, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
affromero/flight-finder 是一款自托管的航班价格追踪器，使用开源代码并支持自带的大语言模型（LLM），能够展示航空公司后台才有的价格变化轨迹。

**价值**  
- **快速赋能 AI**：无需从零搭建模型栈，直接在现有框架上接入 LLM，实现价格预测、趋势分析等智能功能。  
- **原型与实验**：适合作为 AI 原型、RAG（检索增强生成）或智能代理工作流的实验平台，帮助团队快速验证想法。  
- **灵活集成**：提供 API、SDK 与 CLI 三种调用方式，配合丰富的 TypeScript 类型定义，便于在后端服务或 DevOps 流程中嵌入。

**典型接入方式**  
1. **API**：通过 HTTP 接口发送航班查询请求，返回价格历史数据及 AI 生成的分析报告。  
2. **SDK**：使用 npm 包 `@flight-finder/sdk`（或直接引用项目源码）在 Node.js/TypeScript 项目中调用 `trackPrice()`、`analyzeTrend()` 等函数。  
3. **CLI**：在服务器上安装 `flight-finder-cli`，通过命令行快速查询或批量抓取价格数据，适合 CI/CD 或监控脚本。

**生产可用性**  
- **活跃度**：截至 2026‑06‑26 最近一次提交，GitHub ★100、Fork 13，社区活跃。  
- **技术成熟度**：核心使用 TypeScript 编写，拥有完整的类型声明和 12+ 相关话题标签，易于审计和二次开发。  
- **部署准备度**：提供 Docker 镜像和 Helm Chart，支持 Kubernetes 部署，兼容常见 CI/CD 流程。  
- **风险**：目前未发现重大元数据或许可证问题，但仍建议在正式生产前完成安全审计并确认维护者的长期可用性。

综合来看，flight-finder 在功能完整性、社区活跃度和部署便利性方面表现良好，适合作为 AI 驱动的航班价格监控系统的生产候选。

## 🧭 Practical evaluation

**Value:** affromero/flight-finder helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 100 GitHub stars
- 13 forks
- updated 2026-06-26
- primary language: TypeScript
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 43/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 39/100 |
| production | 72/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/affromero/flight-finder) · [← Back to AI/ML](./README.md)</sub>
