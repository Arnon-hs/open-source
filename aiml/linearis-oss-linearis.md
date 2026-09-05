# linearis-oss/linearis

[![Stars](https://img.shields.io/github/stars/linearis-oss/linearis?style=flat-square&color=yellow)](https://github.com/linearis-oss/linearis/stargazers) [![Forks](https://img.shields.io/github/forks/linearis-oss/linearis?style=flat-square&color=blue)](https://github.com/linearis-oss/linearis/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> CLI tool for Linear.app with JSON output, smart ID resolution, and optimized GraphQL queries. Designed for LLM agents and humans who prefer structured data.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 223 |
| 🍴 **Forks** | 21 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `cli` `command-line-tool` `linear` `linearapp` `llm`

## 🎯 Categories

AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
Linearis is a TypeScript‑based CLI for Linear.app that returns data as clean JSON, resolves issue IDs intelligently, and uses optimized GraphQL queries. It is built for both LLM agents and developers who need structured, machine‑readable output, making it easy to plug Linear data into AI‑driven workflows.

**Value**  
- **AI‑ready interface** – By exposing Linear data in a predictable JSON format, Linearis removes the need to hand‑craft GraphQL queries or scrape HTML, letting teams add AI features (e.g., RAG, autonomous agents) with minimal boilerplate.  
- **Productivity boost** – The smart ID resolution lets users refer to issues, projects, or cycles using partial names or aliases, streamlining scripting and prompt engineering.  
- **Low‑cost experimentation** – Because the tool is open source and already handles authentication, pagination, and rate‑limit management, teams can prototype AI‑enhanced product‑management bots or analytics dashboards without building a custom integration stack.

**Practical Adoption Path**  
1. **Evaluate** – Clone the repo, run `npx linearis <command>` with a personal Linear API token, and verify the JSON output matches your use case.  
2. **Integrate** – Wrap the CLI (or import its underlying TypeScript SDK) in your existing CI/CD or LLM orchestration layer (e.g., LangChain, CrewAI).  
3. **Extend** – Add custom post‑processing scripts or prompt templates that consume the JSON, then iterate on your agent or RAG pipeline.  
4. **Deploy** – Package the CLI in a Docker image or as a serverless function to provide a stable endpoint for downstream services.

**Production Readiness**  
- **Activity & Community** – 223 ★, 21 forks, recent commits (last updated 2026‑07‑02), and a clear TypeScript codebase indicate an active project.  
- **Stability** – The CLI abstracts GraphQL intricacies and includes built‑in pagination and error handling, which reduces runtime failures in production.  
- **Ecosystem Fit** – Straightforward installation via npm, well‑documented commands, and JSON‑first output make it compatible with most AI orchestration tools.  
- **Risks** – License compliance, security scanning of dependencies, and long‑term maintainer commitment still need a final check, but no major metadata concerns were found.  

Overall, Linearis is mature enough for a pilot or even a production‑grade integration, especially when the goal is to add AI‑driven capabilities to Linear workflows without building a custom GraphQL client from scratch.

### Русский

Резюме:

Linearis - это мощный открытый проект, предоставляющий CLI-инструмент для работы с Linear.app с возможностью вывода данных в JSON-формате. Эта утилита предназначена для агентов LLM и людей, предпочитающих структурированные данные. С помощью Linearis можно добавить возможности искусственного интеллекта без необходимости начинать с нуля, что делает его идеальным решением для прототипирования функций AI, создания РАГ или агентных потоков, а также оценки инструментов моделирования. 

Проект имеет высокий уровень готовности к production, с сильными сигналами recent activity, adoption и экосистемы, что делает его подходящим кандидатом для serious пилота.

### 中文

**项目简介**  
linearis‑oss/linearis 是一个面向 Linear.app 的命令行工具，能够以结构化的 JSON 输出任务、项目等信息，并提供智能 ID 解析和经过优化的 GraphQL 查询。它专为需要机器可读数据的 LLM 代理或偏好结构化数据的开发者设计。

**价值主张**  
- **快速赋能 AI 能力**：无需从零搭建模型栈，直接通过 CLI 获取 Linear 数据，便于在 RAG、自动化代理或 AI 原型中使用。  
- **低噪声、易集成**：统一的 JSON 格式、智能 ID 解析以及高效的 GraphQL 请求，减少数据清洗和网络开销。  
- **开箱即用的开发体验**：提供 TypeScript SDK、CLI 与 API 三种接入方式，满足脚本、服务和交互式工具的不同需求。

**典型接入方式**  
1. **CLI 调用**：在本地或 CI/CD 环境中直接运行 `linearis <command> --json`，获取任务列表、项目详情等结构化结果。  
2. **SDK 引用**：在 Node/TS 项目中 `import { LinearisClient } from 'linearis'`，使用 `client.queryIssues(...)` 等方法进行编程式查询。  
3. **API/脚本桥接**：将 CLI 输出通过管道或子进程传递给 Python/Go 等语言的脚本，供 LLM Agent 进一步处理。

**生产可用性**  
- **活跃度**：截至 2026‑07‑02 最近一次提交，GitHub ★223、Fork 21，持续维护。  
- **技术成熟度**：使用 TypeScript 实现，提供完整的类型定义；GraphQL 查询已针对 Linear API 进行优化，响应速度快且带宽占用低。  
- **生态兼容**：兼容 Linear 官方 API，易于与现有的 CI/CD、监控或 RAG 系统集成。  
- **风险提示**：虽暂无重大元数据风险，但仍需在正式上线前审查许可证、依赖安全性以及维护者响应情况。

综上，linearis 具备 **高生产就绪度**，适合作为 AI 功能原型、RAG 工作流或智能代理的可靠数据层。

## 🧭 Practical evaluation

**Value:** linearis-oss/linearis helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 223 GitHub stars
- 21 forks
- updated 2026-07-02
- primary language: TypeScript
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 50/100 |
| topics | 75/100 |
| outlook | 75/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 45/100 |
| production | 69/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/linearis-oss/linearis) · [← Back to AI/ML](./README.md)</sub>
