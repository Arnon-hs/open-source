# event-catalog/eventcatalog

[![Stars](https://img.shields.io/github/stars/event-catalog/eventcatalog?style=flat-square&color=yellow)](https://github.com/event-catalog/eventcatalog/stargazers) [![Forks](https://img.shields.io/github/forks/event-catalog/eventcatalog?style=flat-square&color=blue)](https://github.com/event-catalog/eventcatalog/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-77%2F100-brightgreen?style=flat-square)](#)

> The discovery and governance layer for event-driven systems. Document your domains, services, events and schemas — for your teams and your AI agents.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.8k |
| 🍴 **Forks** | 266 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 77/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `architecture` `asyncapi` `ddd` `distributed-systems` `documentation` `domain-driven-design` `event-catalog` `event-driven-architecture` `microservices`

## 🎯 Categories

AI/ML · Documents · Design

## 📝 Summary

### English

**Event Catalog Project Summary**

The event-catalog/eventcatalog is an open-source project that serves as a discovery and governance layer for event-driven systems. It enables teams to document their domains, services, events, and schemas, making it easier to integrate with AI agents. By using this project, teams can add AI capabilities without starting from scratch, making it an ideal choice for prototyping AI features and building workflows.

**Value Proposition**

The event-catalog/eventcatalog project provides significant value by:

* Enabling teams to document and standardize their event-driven systems, making it easier to integrate with AI agents.
* Providing a foundation for building AI capabilities without starting from a blank model stack.
* Supporting the development of prototype AI features, RAG (Return, Amplify, Grow) or agent workflows, and evaluating model tooling.

**Practical Adoption Path**

To adopt the event-catalog/eventcatalog project, follow these steps:

1. Evaluate the project's implementation signals, such as API/SDK/CLI, language metadata, or focused topics.
2. Assess the project's quality signals, including GitHub stars, forks, and recent activity.
3. Review the project's license, security posture, and active maintainers to ensure they align with your organization's requirements.
4. Integrate the

### Русский

**event-catalog/eventcatalog** — это открытая платформа‑слой обнаружения и управления событиями в event‑driven архитектурах, позволяющая документировать домены, сервисы, события и их схемы как для команд, так и для AI‑агентов. Типичный сценарий — быстрое прототипирование AI‑фич, построение RAG‑ или агентных воркфлоу и оценка инструментов моделирования, используя готовый API/SDK/CLI и метаданные о языках и тематиках. Проект имеет высокий уровень готовности к продакшену: активные обновления, более 2700 звёзд, множество форков и широкую экосистему, хотя окончательная проверка лицензии и безопасности всё ещё требуется.

### 中文

**项目简介（2‑3 句）**  
event-catalog（GitHub event-catalog/eventcatalog）是面向事件驱动系统的发现与治理层，帮助团队统一记录业务域、微服务、事件以及数据 schema，并对外提供机器可读的接口，方便 AI 代理和检索增强生成（RAG）等智能应用直接消费。

**价值**  
- **快速赋能 AI**：在已有的事件元数据上即可构建检索、提示或自动化工作流，无需从零搭建模型或数据湖。  
- **统一治理**：通过可视化目录和机器可读的 API/SDK，提升跨团队对事件流的可见性、合规性和变更追踪。  
- **加速原型**：开发者可以直接基于目录中的 schema 与事件定义，快速原型化 AI 功能（如异常检测、自动事件路由、业务智能问答等）。

**典型接入方式**  
1. **API/SDK**：项目提供 RESTful API 与 TypeScript/JavaScript SDK，业务系统可在运行时查询事件、域、服务信息。  
2. **CLI**：通过 `eventcatalog-cli` 可以在 CI/CD 流程中自动同步代码库中的事件定义或生成文档。  
3. **元数据导入**：支持从 OpenAPI、AsyncAPI、GraphQL、Protobuf 等常见规范导入，或直接读取代码注解。  
4. **插件/集成**：可与 Kafka、NATS、AWS EventBridge 等事件总线插件配合，把运行时的事件注册到目录中。

**生产可用性**  
- **活跃度**：截至 2026‑06‑29，项目拥有 2754 星、266 Fork，最近一次提交在同一天，说明维护活跃。  
- **技术成熟度**：使用 TypeScript 编写，提供完整的类型定义，便于在现代前后端项目中直接使用。  
- **生态兼容**：已发布 NPM 包，支持 Docker 镜像部署，且提供 Helm Chart，可在 K8s 环境中快速上线。  
- **风险**：目前未发现重大元数据泄露风险，但仍需进一步审查许可证（MIT）兼容性、依赖安全漏洞以及维护者的长期可用性。  

综合来看，event-catalog 在 OSS 生态中具备较高的生产就绪度，适合作为企业内部事件治理与 AI 赋能的底层平台进行试点乃至正式上线。

## 🧭 Practical evaluation

**Value:** event-catalog/eventcatalog helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2754 GitHub stars
- 266 forks
- updated 2026-06-29
- primary language: TypeScript
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 61/100 |
| stars | 73/100 |
| topics | 100/100 |
| outlook | 80/100 |
| quality | 81/100 |
| recency | 80/100 |
| adoption | 70/100 |
| production | 77/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/event-catalog/eventcatalog) · [← Back to AI/ML](./README.md)</sub>
