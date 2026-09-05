# shaurcasm/nirnam

[![Stars](https://img.shields.io/github/stars/shaurcasm/nirnam?style=flat-square&color=yellow)](https://github.com/shaurcasm/nirnam/stargazers) [![Forks](https://img.shields.io/github/forks/shaurcasm/nirnam?style=flat-square&color=blue)](https://github.com/shaurcasm/nirnam/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-46%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 46/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Orchestration · AI/ML

## 📝 Summary

### English

Here's a brief summary and explanation of the project:

**Summary:** Nirnam is an open-source, browser-native message bus and AI agent framework designed for Micro Frontends (MFEs). It enables the creation of repeatable agent workflows by coordinating multi-agent interactions, standardizing agent memory, and integrating tool-use pipelines.

**Value:** The primary value proposition of Nirnam lies in its ability to turn isolated prompts and tools into cohesive, repeatable workflows. This makes it an attractive solution for organizations seeking to streamline their AI agent interactions and improve overall efficiency.

**Practical Adoption Path:** To adopt Nirnam, developers should first manually inspect the project to understand its integration requirements and potential limitations. Once familiar with the framework, they can start building prototypes or internal workflows to test its capabilities. Before moving to production, it's essential to verify the project's license, maintenance, documentation, issue history, and release cadence to ensure it meets the organization's needs.

**Production Readiness:** Nirnam is considered production-ready at a medium level, indicating that it's suitable for use in prototypes or internal workflows with proper dependency and maintenance checks. However, due to limited quality signals and sparse integration metadata, it's crucial to exercise caution and thoroughly evaluate the project before deploying it in a production environment.

### Русский

Show HN : Nirnam – это браузерный message‑bus и фреймворк для создания AI‑агентов, позволяющий превращать разрозненные подсказки и инструменты в повторяемые многокомпонентные (MFE) рабочие процессы, например координацию нескольких агентов, построение пайплайнов с использованием внешних утилит и унификацию памяти агентов. Проект подходит для прототипов и внутренних систем, однако перед выводом в продакшн требуется ручная проверка интеграции, оценка лицензии, активности разработки и наличия документации. Готовность к production – средняя: функционал стабилен, но необходимо убедиться в надёжности зависимостей и поддержке проекта.

### 中文

**项目简介（2‑3 句话）**  
Show HN: Nirnam 是一个在浏览器环境下运行的消息总线和 AI 代理框架，专为微前端（MFE）场景设计。它能够把分散的 Prompt 与工具组合成可复用的多代理工作流，从而实现跨模块的协同与记忆共享。

**价值**  
- 将孤立的 AI Prompt 与外部工具（API、数据库、UI 元素等）统一编排，形成可重复、可追踪的业务流程。  
- 为多代理系统提供统一的消息总线和共享记忆层，降低跨模块通信的复杂度。  
- 通过浏览器原生实现，省去后端服务的额外部署成本，适合快速原型和内部工具。

**典型接入方式**  
1. **依赖安装**：在前端项目中通过 `npm i nirnam` 引入库。  
2. **初始化总线**：在根微前端或宿主应用中创建 `NirnamBus` 实例，并在需要的子应用中通过 `bus.subscribe()` / `bus.publish()` 进行消息订阅/发布。  
3. **定义 Agent**：使用 `createAgent({prompt, tools, memory})` 声明业务代理，并将其注册到总线上。  
4. **工作流编排**：利用 `bus.chain([...agents])` 或自定义的 `pipeline` 将多个 Agent 链接成完整流程。  
5. **调试与监控**：在开发环境下打开浏览器调试面板的 “Nirnam” 插件，可实时查看消息流、状态和记忆内容。

**生产可用性**  
- **成熟度**：目前评分 49/100，属于 **中等** 稳定性，仅适合原型、内部工具或受控环境。  
- **风险**：元数据稀少，需自行检查许可证、维护频率、文档完整度以及 Issue 处理情况。  
- **准备工作**：在正式上线前进行手动代码审查、依赖安全扫描，并在预生产环境进行集成测试，确保消息总线与 Agent 记忆的持久化方案符合业务容错要求。  

总体而言，Nirnam 对需要在前端快速搭建多代理协作工作流的团队非常有价值，但在生产环境使用前建议完成充分的审查与测试。

## 🧭 Practical evaluation

**Value:** Show HN: Nirnam – a browser-native message bus and AI agent framework for MFEs helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-06-27
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 53/100 |
| quality | 36/100 |
| recency | 80/100 |
| adoption | 0/100 |
| production | 51/100 |
| usefulness | 74/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/shaurcasm/nirnam) · [← Back to Orchestration](./README.md)</sub>
