# SciSharp/BotSharp

[![Stars](https://img.shields.io/github/stars/SciSharp/BotSharp?style=flat-square&color=yellow)](https://github.com/SciSharp/BotSharp/stargazers) [![Forks](https://img.shields.io/github/forks/SciSharp/BotSharp?style=flat-square&color=blue)](https://github.com/SciSharp/BotSharp/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> AI Multi-Agent Framework in .NET

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.1k |
| 🍴 **Forks** | 638 |
| 💻 **Language** | C# |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `chatbot` `multi-agent`

## 🎯 Categories

Orchestration · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
SciSharp / BotSharp is an open‑source .NET framework that lets developers stitch together isolated LLM prompts, tools, and memory stores into reusable multi‑agent workflows. By providing a common orchestration layer, it makes it easy to build, test, and iterate on complex AI pipelines without reinventing the coordination logic.

**Value**  
- **Unified agent orchestration** – Turns ad‑hoc prompts and utilities into repeatable, composable agents, reducing duplicated code and speeding up experimentation.  
- **Tool‑use pipelines & memory** – Built‑in support for invoking external services and persisting context, which is essential for sophisticated conversational or decision‑making bots.  
- **C# ecosystem integration** – Fits naturally into existing .NET stacks, allowing teams to leverage familiar tooling, CI pipelines, and enterprise libraries.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the sample projects, and replace the example prompts/tools with your own. The clear C# API lets you iterate quickly.  
2. **Validate integration** – Because metadata on integration points is sparse, manually review the `BotSharp` configuration files and source to map required services (e.g., vector stores, external APIs). Write a small integration test that exercises your specific tool‑use case.  
3. **Wrap & standardize** – Once the core workflow is stable, extract common patterns (memory handling, error handling, logging) into reusable modules within your codebase.  
4. **Governance** – Add version pinning, CI checks, and automated security scans for BotSharp’s dependencies before promoting to a shared library.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last update 2026‑06‑26) and has a solid community signal (≈3 k stars, 638 forks), but the integration surface is not well‑documented.  
- **Suitability**: Ideal for internal prototypes, proof‑of‑concepts, or internal tooling where you can afford a short “integration validation” sprint.  
- **Considerations before production**:  
  * Perform a dependency audit (check for transitive NuGet packages).  
  * Implement robust monitoring and fallback logic for external tool calls.  
  * Validate performance and scalability of the chosen memory store under realistic load.  

In short, BotSharp offers a powerful way to build multi‑agent AI systems in .NET, but teams should allocate time for manual integration testing and dependency management before treating it as a production‑grade component.

### Русский

SciSharp/BotSharp — это open‑source фреймворк на .NET, позволяющий объединять отдельные подсказки и инструменты в повторяемые многопользовательские AI‑агенты, упрощая оркестрацию сложных workflows, добавление пайплайнов с инструментами и стандартизацию памяти агентов. Он подходит для прототипов и внутренних автоматизаций, где требуется координация нескольких агентов, но перед выводом в production следует вручную проверить интеграцию и оценить затраты на настройку. Проект имеет средний уровень готовности: активные обновления, более 3 тыс. звёзд на GitHub, но путь интеграции неочевиден и требует дополнительного анализа.

### 中文

**项目简介**  
SciSharp/BotSharp 是一个基于 .NET 的 AI 多智能体框架，能够把零散的 Prompt 与工具组合成可复用的智能体工作流。它适用于多智能体协同、工具调用流水线以及统一的记忆管理。

**价值**  
- **工作流化**：将单独的 Prompt、API 调用或工具封装为可编排的智能体节点，降低重复开发成本。  
- **可扩展的多智能体协作**：支持在同一流程中调度多个智能体，实现复杂任务的分工与协同。  
- **统一记忆层**：提供可插拔的记忆实现，帮助智能体在长对话或跨会话场景中保持上下文一致性。  

**典型接入方式**  
1. **引用 NuGet 包**：在 .NET 项目中添加 `SciSharp.BotSharp` 包。  
2. **定义 Agent 与 Tool**：使用框架提供的 `AgentBuilder` 与 `ToolProvider` 接口，实现业务 Prompt 与外部工具（如数据库、REST API）的适配。  
3. **编排工作流**：通过 `WorkflowBuilder` 将多个 Agent/Tool 按有向图或状态机方式串联，生成 `IBotWorkflow` 实例。  
4. **运行与监控**：在应用启动时注入工作流实例，利用内置的日志/指标插件进行运行时监控。  

> **注意**：项目的元数据中缺少明确的集成示例，建议在正式接入前先在测试环境完成一次端到端的原型验证，确认依赖、配置和自定义记忆实现的兼容性。

**生产可用性**  
- **成熟度**：GitHub 3079 星、638 Fork，最近一次提交在 2026‑06‑26，代码活跃度尚可。  
- **适用场景**：非常适合作为原型、内部工具或业务流程的快速验证平台。  
- **上线前检查**：  
  - 核实所有第三方工具（如数据库、外部 API）的兼容性。  
  - 评估依赖的 .NET 版本与公司现有技术栈的匹配度。  
  - 对记忆存储（如 Redis、SQL）进行可靠性与安全性审计。  
- **总体评估**：**中等**（Medium）— 在完成上述依赖和维护审查后，可用于生产环境，但仍需持续监控框架的更新与安全补丁。

## 🧭 Practical evaluation

**Value:** SciSharp/BotSharp helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 3079 GitHub stars
- 638 forks
- updated 2026-06-26
- primary language: C#
- 3 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 70/100 |
| stars | 74/100 |
| topics | 38/100 |
| outlook | 61/100 |
| quality | 64/100 |
| recency | 40/100 |
| adoption | 73/100 |
| production | 54/100 |
| usefulness | 74/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/SciSharp/BotSharp) · [← Back to Orchestration](./README.md)</sub>
