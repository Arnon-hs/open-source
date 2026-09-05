# quarkusio/quarkus-workshop-langchain4j

[![Stars](https://img.shields.io/github/stars/quarkusio/quarkus-workshop-langchain4j?style=flat-square&color=yellow)](https://github.com/quarkusio/quarkus-workshop-langchain4j/stargazers) [![Forks](https://img.shields.io/github/forks/quarkusio/quarkus-workshop-langchain4j?style=flat-square&color=blue)](https://github.com/quarkusio/quarkus-workshop-langchain4j/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Quarkus Langchain4J Workshop

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 83 |
| 🍴 **Forks** | 65 |
| 💻 **Language** | Java |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `chatbot` `langchain` `llm` `mcp` `mcp-server` `quarkus` `workshop`

## 🎯 Categories

Orchestration · MCP · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The **quarkusio/quarkus‑workshop‑langchain4j** repository is a Quarkus‑based tutorial that demonstrates how to compose isolated prompts, tools, and memory into reusable LangChain4j agent workflows. It showcases patterns for coordinating multi‑agent pipelines, adding tool‑use steps, and standardising agent state, making it a practical entry point for teams that want to prototype AI‑driven orchestration on the JVM.

**Value**  
By turning ad‑hoc prompt calls into repeatable, composable agents, the project accelerates the development of robust AI/ML back‑ends, reduces duplication, and provides a clear blueprint for integrating external tools (e.g., search, databases) into LangChain4j‑powered services.

**Practical Adoption Path**  
1. **Explore the workshop** – clone the repo and run the provided Quarkus examples locally to understand the core concepts (prompt chaining, tool adapters, memory handling).  
2. **Prototype a workflow** – replace the sample prompts/tools with your own domain logic, leveraging the same Quarkus extensions and LangChain4j APIs.  
3. **Integrate into your service** – embed the generated agent code into an existing Quarkus microservice, expose it via the built‑in REST/GraphQL endpoints, and iterate on the workflow using the same development cycle.  
4. **Validate and test** – add unit/integration tests for each agent step, and use Quarkus DevMode for rapid feedback before promoting to a CI pipeline.

**Production Readiness**  
The project is **medium‑ready**: it is actively maintained (last update 2026‑05‑11), written in Java, and already has a modest community (≈ 83 stars, 65 forks). It is suitable for prototypes, internal tooling, or as a reference implementation, but production use should include a formal security review, license verification, and dependency hygiene (e.g., checking for vulnerable transitive libraries) before deployment.

### Русский

Quarkus Langchain4J Workshop (quarkusio/quarkus-workshop-langchain4j) позволяет быстро собрать повторяемые рабочие процессы агентов, объединяя отдельные промпты и инструменты в единые цепочки с поддержкой памяти и многоканального взаимодействия. Типовой сценарий — создание и оркестрация multi‑agent пайплайнов (например, чат‑боты, автоматизированные справочные системы) с возможностью подключения кастомных инструментов через простой API/SDK. Готовность к production — средняя: проект стабилен для прототипов и внутренних сервисов, но требует проверки лицензии, безопасности и подтверждения активности поддерживающих разработчиков перед масштабным внедрением.

### 中文

**项目简介（2‑3 句话）**  
Quarkus Langchain4J Workshop（quarkusio/quarkus-workshop-langchain4j）是一个基于 Quarkus 的示例仓库，演示如何使用 LangChain4J 将单个 Prompt 与外部工具组合成可复用的智能体工作流。它提供了完整的代码示例，帮助开发者快速上手多代理协作、工具调用和记忆管理等 AI/ML 场景。

**价值**  
- **把孤立的 Prompt 和工具转化为可重复的 Agent 流程**，降低 AI 应用的研发成本。  
- 支持 **多代理编排、工具链集成、统一记忆存储**，适合构建复杂业务逻辑的对话系统或自动化流程。  
- 基于 Quarkus 的轻量高效运行时，使得部署成本低、启动快，适合微服务和 serverless 场景。

**典型接入方式**  
1. **依赖方式**：在 Quarkus 项目 `pom.xml` 中加入 `io.quarkus:quarkus-langchain4j`（或直接引用本仓库的模块）即可获得 Prompt、Chain、Tool、Memory 等 API。  
2. **SDK/CLI**：仓库提供了示例 CLI（`quarkus-langchain4j-cli`），可快速生成 Agent 项目骨架或在本地测试 Prompt。  
3. **REST 接口**：示例中已经实现了基于 HTTP 的 Agent 服务，直接通过 `curl` 或 OpenAPI 客户端调用，方便与现有后端系统对接。  

**生产可用性**  
- **成熟度**：当前评分 63/100，属于 **中等** 级别。代码已在 2026‑05‑11 更新，拥有 83 Stars、65 Forks，活跃度尚可。  
- **适用场景**：非常适合作为 **原型、内部工具或实验性服务** 的起点；在正式生产环境使用前，需要完成以下检查：  
  - 依赖安全审计（尤其是 LangChain4J 与底层模型提供商的 SDK）。  
  - 评估许可证兼容性（项目采用 Apache‑2.0）。  
  - 对关键组件（如记忆存储、工具调用）进行性能与容错测试。  
- **运维要求**：Quarkus 本身具备原生镜像构建和 Kubernetes 原生支持，配合适当的监控（Micrometer）和配置管理，可实现较为可靠的生产部署。  

综上，quarkus-workshop-langchain4j 为构建多 Agent、工具化 AI 工作流提供了完整的参考实现，适合作为快速验证和内部平台化的基石，经过安全与运维评估后即可在生产环境中使用。

## 🧭 Practical evaluation

**Value:** quarkusio/quarkus-workshop-langchain4j helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 83 GitHub stars
- 65 forks
- updated 2026-05-11
- primary language: Java
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 41/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 42/100 |
| production | 68/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/quarkusio/quarkus-workshop-langchain4j) · [← Back to Orchestration](./README.md)</sub>
