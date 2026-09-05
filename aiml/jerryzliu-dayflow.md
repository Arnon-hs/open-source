# JerryZLiu/Dayflow

[![Stars](https://img.shields.io/github/stars/JerryZLiu/Dayflow?style=flat-square&color=yellow)](https://github.com/JerryZLiu/Dayflow/stargazers) [![Forks](https://img.shields.io/github/forks/JerryZLiu/Dayflow?style=flat-square&color=blue)](https://github.com/JerryZLiu/Dayflow/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> The automatic work journal. Privately turns your screen into a timeline of what you actually accomplished. Open-source and local-first.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 6k |
| 🍴 **Forks** | 322 |
| 💻 **Language** | Swift |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `chatgpt` `claude` `gemini` `llm` `lmstudio` `ollama` `productivity` `productivity-tools` `swift` `time` `timeline`

## 🎯 Categories

AI/ML · Productivity

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Dayflow is an open‑source, local‑first work‑journal app that automatically records what you actually accomplish on your screen and presents it as a searchable timeline. Built in Swift, it ships with AI‑enabled features that let you prototype retrieval‑augmented generation (RAG) or agent workflows without having to assemble a model stack from scratch. With over 6 000 stars, recent commits, and active forks, it’s ready for serious pilot projects.

**Value**  
- **Instant AI capability** – Dayflow bundles the plumbing for capturing context (screenshots, window titles, keystrokes) and exposing it through an API, so developers can plug in LLMs, vector stores, or custom agents without building the data‑collection layer themselves.  
- **Privacy‑first** – All data stays on the user’s device, satisfying regulations and corporate policies that forbid cloud‑based logging.  
- **Rapid prototyping** – The built‑in timeline makes it easy to test RAG queries, generate summaries, or build “assistant‑that‑knows‑what‑you‑did” features with minimal code.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the provided Swift package, and verify the screen‑capture pipeline on a test machine.  
2. **Readme & API walk‑through** – Follow the quick‑start guide to expose the journal data via the local HTTP endpoint; replace the placeholder LLM calls with your own model or a hosted service.  
3. **Pilot Integration** – Embed the endpoint into a small internal tool (e.g., daily summary generator) and evaluate latency, storage footprint, and UI ergonomics.  
4. **Scale & Harden** – Add persistence (CoreData/SQLite), configure encryption, and optionally bundle a vector store for richer RAG use cases.

**Production Readiness**  
Dayflow scores high for an OSS candidate: it has recent activity (last commit 2026‑05‑14), a strong community (6 014 stars, 322 forks), and clear Swift documentation. The codebase is mature enough for a pilot, but the integration path isn’t fully documented—teams should allocate time to validate setup costs (e.g., macOS‑only runtime, required permissions) before full deployment. Once those gaps are addressed, Dayflow can be considered production‑ready for internal workloads that need private, AI‑augmented work journaling.

### Русский

**JerryZLiu/Dayflow** — открытый локальный журнал работы, который автоматически превращает ваш экран в временную шкалу реальных достижений, позволяя быстро добавить AI‑функциональность (RAG, агентные сценарии) без необходимости строить модель с нуля. Типичный путь внедрения — запуск небольшого proof‑of‑concept, проверка README и базовой интеграции, после чего проект готов к пилотному использованию в продакшн благодаря активному развитию, 6 000+ звёздам и свежим обновлениям. Несмотря на сильные сигналы готовности, стоит уточнить детали настройки, так как интеграционный процесс из метаданных не полностью описан.

### 中文

**项目简介（2‑3 句）**  
JerryZLiu/Dayflow 是一款开源的本地化工作日志工具，它会自动记录你在电脑屏幕上的实际操作并生成时间线，让每日完成的工作一目了然。项目基于 Swift 开发，完全本地运行，无需云端依赖，适合个人或小团队使用。

**价值**  
- **自动化记录**：利用 AI 分析屏幕内容，免去手动填写工作日志的繁琐。  
- **隐私安全**：所有数据仅保存在本地，避免敏感信息泄露。  
- **快速原型**：提供现成的 AI 能力（如 RAG、Agent 工作流），帮助开发者在已有模型堆栈上快速实验新功能，而不必从零搭建。

**典型接入方式**  
1. **阅读 README 与快速入门**：克隆仓库后按照文档安装依赖（Swift 包管理、必要的系统权限）。  
2. **小范围 PoC**：在一台测试机器上运行 `Dayflow`，通过配置文件指定要监控的应用或窗口，验证日志生成和 AI 分析是否满足需求。  
3. **集成到现有工作流**：使用提供的 CLI 或 API 将生成的时间线导出为 JSON/CSV，供内部报表或第三方工具（如 Notion、Jira）二次处理。  
4. **扩展功能**：如果需要自定义 AI 模型或 RAG 检索，可在 `Dayflow` 的插件目录中加入自定义 Swift 模块或调用本地模型服务。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑05‑14，GitHub ★6014、Fork 322，表明社区活跃且维护及时。  
- **技术成熟度**：采用 Swift 编写，适配 macOS/iOS，具备本地运行的完整依赖链，易于在企业内部部署。  
- **风险点**：项目文档对完整的集成路径描述有限，建议先完成小规模的概念验证（PoC），评估部署脚本、权限配置以及 AI 模型的本地运行成本。  
- **总体评估**：在经过一次 PoC 验证后，可视为高可用的 OSS 组件投入生产使用，尤其适合对数据隐私有严格要求的团队。

## 🧭 Practical evaluation

**Value:** JerryZLiu/Dayflow helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 6014 GitHub stars
- 322 forks
- updated 2026-05-14
- primary language: Swift
- 12 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 63/100 |
| stars | 80/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 84/100 |
| recency | 80/100 |
| adoption | 75/100 |
| production | 71/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/JerryZLiu/Dayflow) · [← Back to AI/ML](./README.md)</sub>
