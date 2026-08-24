# deltachat/deltachat-ios

[![Stars](https://img.shields.io/github/stars/deltachat/deltachat-ios?style=flat-square&color=yellow)](https://github.com/deltachat/deltachat-ios/stargazers) [![Forks](https://img.shields.io/github/forks/deltachat/deltachat-ios?style=flat-square&color=blue)](https://github.com/deltachat/deltachat-ios/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> Decentralized private messenger with chat-shared tools and games for iOS

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 443 |
| 🍴 **Forks** | 79 |
| 💻 **Language** | Swift |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`deltachat` `email` `ios` `messenger`

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
DeltaChat iOS is an open‑source, decentralized messenger for Apple devices that embeds chat‑shared tools and games while offering a ready‑made foundation for adding AI capabilities. With a modest 60 / 100 score, the Swift codebase (443 ★, 79 forks) is actively maintained and can serve as a sandbox for prototyping Retrieval‑Augmented Generation (RAG) or autonomous‑agent workflows on mobile.  

**Value**  
- **AI‑ready foundation** – The app already ships a functional messaging stack, so developers can focus on plugging in language models, tool‑calling, or RAG pipelines instead of building a messenger from scratch.  
- **Rapid prototyping** – Because the UI, networking, and encryption layers are in place, teams can quickly iterate on AI‑driven features (e.g., smart replies, in‑chat assistants, game‑based interactions) and evaluate model performance on real user flows.  

**Practical Adoption Path**  
1. **Clone & run the demo** – Follow the README to build the iOS app and confirm the baseline messenger works on a test device.  
2. **Isolate a PoC module** – Create a small Swift package that wraps the desired LLM (e.g., OpenAI, Cohere, or an on‑device model) and expose a simple API (e.g., `generateReply(to: Message)`).  
3. **Integrate via the existing chat pipeline** – Hook the new API into the message‑receive handler; start with a toggle flag so the original messenger remains functional.  
4. **Iterate & benchmark** – Use the built‑in chat UI to collect latency, token usage, and UX feedback; refine prompt engineering or RAG components as needed.  
5. **Scale** – Once the PoC proves stable, extract the AI layer into a reusable framework, add error handling, and optionally replace the local model with a server‑side endpoint for production workloads.  

**Production Readiness**  
- **Maturity**: Medium. The codebase is actively maintained (last commit 2026‑06‑30) and well‑documented for a Swift project, but AI integration points are not part of the core repository, so extra engineering effort is required.  
- **Risks**: The integration path is not explicit; developers must invest time to understand the messaging architecture and ensure compliance with privacy/encryption guarantees. Dependency management (e.g., Swift Package Manager, third‑party model SDKs) should be audited.  
- **Recommendation**: Treat DeltaChat iOS as a **prototype‑grade** platform—ideal for internal pilots, feature demos, or beta‑tested user studies. Before moving to production, perform a thorough dependency audit, add robust error handling, and validate that the AI component meets latency, security, and scalability requirements.

### Русский

DeltaChat iOS — это децентрализованный приватный мессенджер с поддержкой чат‑инструментов и игр, написанный на Swift. Он позволяет быстро добавить AI‑функциональность (например, RAG‑поиск или агентные сценарии) без создания модели с нуля, что делает его удобным для прототипирования и внутренних экспериментов; для начала рекомендуется реализовать небольшой proof‑of‑concept и проверить README. Готовность к продакшну — средняя: проект достаточно зрелый для прототипов, но требует проверки зависимостей, поддержки и уточнения пути интеграции перед масштабным внедрением.

### 中文

**开源项目简介**

deltachat/deltachat-ios 是一个开源的去中心化私人通讯应用，支持聊天工具和游戏，适用于iOS平台。

**价值**

deltachat/deltachat-ios 帮助开发者在现有的模型堆栈中添加 AI 能力，适用于 Prototyping AI 特性、构建 RAG 或代理工作流、评估模型工具。

**典型接入方式**

开发者可以通过以下步骤接入 deltachat/deltachat-ios：

1. 阅读 README 文档，了解项目的基本信息和集成步骤。
2. 构建一个小的 PoC（Proof of Concept），验证集成的可行性和成本。
3. 验证项目的依赖和维护成本，确保项目在生产环境中可用。

**生产可用性**

deltachat/deltachat-ios 的生产可用性为中等（Medium），适用于 Prototyping 或内部工作流。开发者需要在接入前验证项目的依赖和维护成本，以确保项目在生产环境中可用。

## 🧭 Practical evaluation

**Value:** deltachat/deltachat-ios helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 443 GitHub stars
- 79 forks
- updated 2026-06-30
- primary language: Swift
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 48/100 |
| stars | 56/100 |
| topics | 50/100 |
| outlook | 54/100 |
| quality | 57/100 |
| recency | 40/100 |
| adoption | 54/100 |
| production | 51/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/deltachat/deltachat-ios) · [← Back to Mobile](./README.md)</sub>
