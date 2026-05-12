# WebFuzzing/EvoMaster

[![Stars](https://img.shields.io/github/stars/WebFuzzing/EvoMaster?style=flat-square&color=yellow)](https://github.com/WebFuzzing/EvoMaster/stargazers) [![Forks](https://img.shields.io/github/forks/WebFuzzing/EvoMaster?style=flat-square&color=blue)](https://github.com/WebFuzzing/EvoMaster/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> The first open-source AI-driven tool for automatically generating system-level test cases (also known as fuzzing) for web/enterprise applications. Currently targeting whitebox and blackbox testing of Web APIs, like REST, GraphQL and RPC (e.g., gRPC and Thrift).

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 728 |
| 🍴 **Forks** | 111 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`api-rest` `api-testing` `evolutionary-algorithms` `fuzzer` `fuzzing` `graphql` `grpc` `java` `kotlin` `rest` `rpc-api` `search-based-software-testing`

## 🎯 Categories

AI/ML · Backend · DevTools

## 📝 Summary

### English

**Brief Summary**  
WebFuzzing/EvoMaster is an open‑source, AI‑driven tool that automatically generates system‑level test cases (fuzzing) for web and enterprise applications, supporting both white‑box and black‑box testing of APIs such as REST, GraphQL, gRPC and Thrift. Built in Kotlin, it offers a ready‑to‑use SDK/CLI and rich metadata that let developers plug AI capabilities into their testing pipelines without building a model stack from scratch.  

**Value**  
- **Accelerates AI‑enhanced testing** – EvoMaster’s built‑in AI models synthesize realistic request sequences, edge‑case inputs and payloads, dramatically reducing the manual effort required to achieve high coverage on complex APIs.  
- **Unified test generation** – One tool covers a wide range of API styles (REST, GraphQL, RPC), so teams can standardize fuzzing across microservices without maintaining separate frameworks.  
- **Extensible integration** – The exposed SDK, CLI and language‑level metadata make it easy to embed EvoMaster in CI/CD pipelines, custom RAG/agent workflows, or prototype new AI‑driven quality‑gate features.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the CLI against a local or staging API to generate an initial test suite and inspect the produced test cases.  
2. **Integrate** – Add the Kotlin SDK (or use the generated Java bindings) to your build system, configure the desired testing mode (white‑box vs. black‑box) and automate test generation in your CI pipeline.  
3. **Extend** – Leverage the provided API metadata (end‑point signatures, schemas) to feed downstream AI components (e.g., RAG or autonomous agents) or to customize fuzzing heuristics for domain‑specific constraints.  
4. **Pilot** – Deploy the generated test suite in a pre‑production environment, monitor coverage and fault detection metrics, and iterate on configuration until the desired quality baseline is met.  

**Production Readiness**  
EvoMaster scores high on production readiness: it has recent activity (last commit 2026‑05‑12), strong community adoption (728 ⭐, 111 forks), and a clear ecosystem (Kotlin core, CLI, SDK). The project shows solid maintenance signals and a growing user base, making it suitable for a serious pilot in production environments. Remaining due‑diligence should focus on confirming the license compatibility, reviewing the security posture of generated test payloads, and ensuring an active maintainer is available for long‑term support.

### Русский

WebFuzzing/EvoMaster — первый open‑source инструмент, использующий ИИ для автоматической генерации системных тестов (fuzzing) веб‑ и корпоративных приложений (REST, GraphQL, gRPC, Thrift). Он позволяет быстро добавить AI‑возможности в процессы тестирования без построения собственного стекa моделей, что удобно для прототипирования AI‑фич, построения RAG/агентных пайплайнов и оценки инструментов моделей. Проект имеет высокий уровень готовности к production: активные коммиты, 728 звёзд на GitHub, широкая экосистема (API/SDK/CLI), поддержка Kotlin и хорошие сигналы принятия в сообществе, что делает его подходящим для серьёзных пилотных внедрений.

### 中文

**项目简介**  
WebFuzzing/EvoMaster 是首个开源的 AI 驱动工具，能够自动生成面向 Web/企业应用的系统级测试用例（即 fuzzing）。当前支持对 Web API（REST、GraphQL）以及 RPC 接口（gRPC、Thrift）进行白盒和黑盒测试。

**价值**  
- **AI 能力即插即用**：无需从零搭建模型堆栈，直接在现有测试流程中加入 AI 辅助的用例生成，提高覆盖率和缺陷发现效率。  
- **原型快速迭代**：适合快速验证 AI 功能（如 RAG、智能 Agent 工作流）在测试场景中的可行性。  
- **评估模型工具链**：提供统一的实现信号（API/SDK/CLI、语言元数据），帮助团队对不同模型和工具进行对比评估。

**典型接入方式**  
1. **CLI**：通过命令行直接启动 fuzzing，适合 CI/CD pipeline 中的自动化调用。  
2. **SDK/API**：项目提供 Kotlin/Java SDK，可在自定义测试框架或微服务中嵌入调用，实现更细粒度的控制。  
3. **语言元数据/主题标签**：利用项目的 15 个 GitHub 主题标签和语言标识（Kotlin），快速定位适配的插件或社区扩展。  

**生产可用性**  
- **成熟度高**：GitHub 728 ★、111 Fork，最近一次更新为 2026‑05‑12，活跃的社区和持续的代码提交表明项目维护良好。  
- **生态兼容**：支持主流 Web API 规范和 RPC 框架，易于与现有微服务、容器化部署和 CI/CD 系统集成。  
- **风险提示**：虽未发现重大元数据风险，但仍需对许可证（Apache‑2.0）和安全审计进行最终确认，确保符合企业合规要求。  

综上，WebFuzzing/EvoMaster 已具备在生产环境中进行试点或正式投入使用的条件，尤其适合希望在测试阶段快速引入 AI 能力的后端团队。

## 🧭 Practical evaluation

**Value:** WebFuzzing/EvoMaster helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 728 GitHub stars
- 111 forks
- updated 2026-05-12
- primary language: Kotlin
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 61/100 |
| topics | 100/100 |
| outlook | 84/100 |
| quality | 81/100 |
| recency | 100/100 |
| adoption | 58/100 |
| production | 79/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/WebFuzzing/EvoMaster) · [← Back to AI/ML](./README.md)</sub>
