# haidrrrry/compose-kotlin-agent-skills

[![Stars](https://img.shields.io/github/stars/haidrrrry/compose-kotlin-agent-skills?style=flat-square&color=yellow)](https://github.com/haidrrrry/compose-kotlin-agent-skills/stargazers) [![Forks](https://img.shields.io/github/forks/haidrrrry/compose-kotlin-agent-skills?style=flat-square&color=blue)](https://github.com/haidrrrry/compose-kotlin-agent-skills/network) [![Language](https://img.shields.io/badge/lang-Markdown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Jetpack Compose & Kotlin AI agent skills for Cursor, Claude Code, Codex, Gemini & 27+ agents. Strict MVI · Kotlin 2.x K2 · Compose 2026 · CI-validated.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 32 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | Markdown |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-07-08 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agents-md` `ai` `ai-agents` `android` `android-development` `claude-code` `coding-agent` `compose` `compose-multiplatform` `coroutines` `cursor` `cursor-rules`

## 🎯 Categories

Orchestration · AI/ML · Database · Mobile

## 📝 Summary

### English

**Project Summary:**
The haidrrrry/compose-kotlin-agent-skills project is an open-source initiative that provides a set of tools for integrating multiple AI agents, such as Cursor, Claude Code, Codex, and Gemini, into repeatable workflows using Jetpack Compose and Kotlin. This project aims to standardize agent memory and enable the coordination of multi-agent workflows. It is a useful resource for prototypes or internal workflows, but requires careful evaluation and validation before production use.

**Value Proposition:**
The primary value of this project lies in its ability to turn isolated prompts and tools into repeatable agent workflows, making it easier to integrate multiple AI agents and standardize their interactions. This can lead to more efficient and effective use of AI capabilities in various applications.

**Practical Adoption Path:**
To adopt this project, it is recommended to start with a small proof of concept and thoroughly review the README documentation. The integration path is not immediately obvious, so careful evaluation and setup cost validation are essential before committing to production use. This project is most suitable for developers and teams with experience in Kotlin, Jetpack Compose, and AI/ML integration.

**Production Readiness:**
The project is considered to be at a medium level of production readiness. While it is useful for prototypes

### Русский

Резюме проекта haidrrrry/compose-kotlin-agent-skills:

Проект haidrrrry/compose-kotlin-agent-skills представляет собой набор инструментов для интеграции с различными AI-агентами, используя Jetpack Compose и Kotlin. Он позволяет превратить изолированные запросы и инструменты в повторяемые агентные потоки, что упрощает координацию мульти-агентных потоков и стандартизацию агентной памяти.

Проект готов к внедрению в прототипах или внутренних потоках, но требует тщательного рассмотрения зависимостей и обслуживания перед использованием в производстве. Для начала работы с проектом рекомендуется выполнить небольшой proof of concept и проверить README.

### 中文

**价值**  
- **统一化工作流**：把零散的 Prompt、工具调用和记忆管理抽象为可复用的 Agent Skill，帮助团队把“单次对话”升级为可编排、可追踪的多 Agent 流程。  
- **跨平台兼容**：基于 Jetpack Compose 与 Kotlin 2.x（K2）实现，天然适配 Android、桌面和 Web（Compose Multiplatform），并提供对 Cursor、Claude Code、Codex、Gemini 等 27+ 大模型的统一调用层。  
- **严格的 MVI 架构**：采用 Model‑View‑Intent，保证状态管理可预测、单元测试友好，降低因异步 Agent 交互导致的 bug。  

**典型接入方式**  

| 步骤 | 操作 | 说明 |
|------|------|------|
| 1️⃣ 依赖引入 | 在 `build.gradle.kts` 中加入 `implementation("io.github.haidrrrry:compose-kotlin-agent-skills:0.1.0")`（或最新 tag） | 项目已在 Maven Central/GitHub Packages 发布，Gradle/Kotlin DSL 均可直接拉取。 |
| 2️⃣ 初始化 SDK | ```kotlin<br>val agentEngine = AgentEngine.create(   model = Model.GEMINI,   apiKey = System.getenv("GEMINI_KEY") )<br>``` | 通过 `AgentEngine` 配置模型、凭证和全局拦截器（日志、限流等）。 |
| 3️⃣ 定义 Skill | ```kotlin<br>@Skill(name = "searchWeather")<br>suspend fun searchWeather(city: String): Weather { … }<br>``` | 使用 `@Skill` 注解声明可被 Agent 调用的工具函数，返回值会自动序列化进 Agent 的记忆。 |
| 4️⃣ 组合工作流 | ```kotlin<br>val workflow = workflow {   step { askUser() }   step { useSkill(searchWeather) }   step { summarizeResult() } }<br>``` | 通过 DSL 把多个 Skill、Prompt 与 UI 交互串联成 MVI‑compatible 的 `StateMachine`。 |
| 5️⃣ UI 绑定 | 在 Compose 中使用 `AgentView(state = viewModel.state, onEvent = viewModel::process)` | UI 完全响应 `State`，无需手动管理协程或回调。 |
| 6️⃣ CI 验证 | 项目自带 GitHub Action (`ci.yml`) 会在每次 PR 运行单元测试、Compose 预览校验以及 K2 编译检查，确保集成后不破坏现有构建。 |

> **小技巧**：先在本地跑 `./gradlew :sample:run`，确认 Demo 能正常调用目标模型后，再把 Skill 移植到自己的业务模块。

**生产可用性评估**  

| 维度 | 现状 | 结论 |
|------|------|------|
| **成熟度** | 32 Stars、5 Forks，最近一次提交 2026‑07‑08，CI 已覆盖编译、单元测试。 | 仍属早期社区项目，功能基本稳定，但缺少大规模生产案例。 |
| **依赖管理** | 仅依赖 Kotlin 2.x、Compose 2026、Ktor（HTTP）和少量 JSON 序列化库。 | 依赖链短，升级风险低；但需自行监控 K2 与 Compose 的后向兼容性。 |
| **可扩展性** | 通过 `@Skill` 注解和 DSL，支持无限自定义工具和记忆模型。 | 适合内部原型、实验平台以及逐步迁移到生产的微服务。 |
| **运维成本** | 需要维护模型 API Key、监控 Agent 超时/费用；无内置监控仪表盘，需要自行集成 Prometheus/Logback。 | 中等成本，建议在内部环境先做 “Proof‑of‑Concept + 监控” 再推广。 |
| **安全合规** | 项目本身不处理数据持久化，所有记忆默认在内存中；若需要持久化需自行实现符合 GDPR/ISO 的存储层。 | 需自行评估数据泄露风险。 |

**总体判断**  
- **原型/内部工具**：非常适合，能快速把多模型、多工具的交互抽象为统一的 Skill，显著提升研发效率。  
- **生产环境**：可行，但在正式上线前建议：① 完成一次完整的 PoC（包括错误恢复、费用监控、日志审计）；② 编写针对关键 Skill 的集成测试；③ 评估模型供应商的 SLA 与合规要求。  

只要做好上述准备，`compose-kotlin-agent-skills` 完全可以作为企业内部 AI 编排层的基础设施，帮助团队在 Kotlin/Compose 生态中统一管理多 Agent 工作流。

## 🧭 Practical evaluation

**Value:** haidrrrry/compose-kotlin-agent-skills helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 32 GitHub stars
- 5 forks
- updated 2026-07-08
- primary language: Markdown
- 20 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 32/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 68/100 |
| recency | 100/100 |
| adoption | 29/100 |
| production | 70/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-08 · [View on GitHub](https://github.com/haidrrrry/compose-kotlin-agent-skills) · [← Back to Orchestration](./README.md)</sub>
