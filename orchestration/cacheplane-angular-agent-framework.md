# cacheplane/angular-agent-framework

[![Stars](https://img.shields.io/github/stars/cacheplane/angular-agent-framework?style=flat-square&color=yellow)](https://github.com/cacheplane/angular-agent-framework/stargazers) [![Forks](https://img.shields.io/github/forks/cacheplane/angular-agent-framework?style=flat-square&color=blue)](https://github.com/cacheplane/angular-agent-framework/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> Angular SDK for Building Agentic Apps + Generative UI

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 101 |
| 🍴 **Forks** | 11 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agents` `ai` `angular` `framework` `typescript`

## 🎯 Categories

Orchestration · AI/ML · Frontend · Libraries & SDKs

## 📝 Summary

### English

**Project Summary:**

cacheplane/angular-agent-framework is an open-source Angular SDK designed to help developers build agentic apps with generative UI capabilities. This framework enables the creation of repeatable agent workflows by integrating isolated prompts and tools. It's a useful tool for prototyping or internal workflows, with potential for standardizing agent memory and coordinating multi-agent workflows.

**Value Proposition:**

The primary value of cacheplane/angular-agent-framework lies in its ability to turn isolated prompts and tools into repeatable agent workflows. This allows developers to create more efficient and standardized workflows, particularly in environments where multiple agents need to collaborate.

**Practical Adoption Path:**

1. **Evaluation:** The framework's straightforward integration and exposure of implementation signals make it easy to evaluate and assess its fit for a project.
2. **Prototype Development:** cacheplane/angular-agent-framework is suitable for prototyping or internal workflows, allowing developers to test and refine their agentic app ideas.
3. **Standardization:** As the framework is used, developers can standardize agent memory and create reusable workflows, reducing complexity and increasing efficiency.
4. **Production Readiness:** Before deploying the framework in production, developers should conduct thorough dependency and maintenance checks to ensure its stability and security.

**Production Readiness:**

cacheplane/angular-agent-framework is

### Русский

**cacheplane/angular-agent-framework** — это TypeScript‑SDK для Angular, позволяющий быстро собрать агентные приложения и генеративный UI, превращая отдельные промпты и инструменты в повторяемые рабочие процессы агентов. Типичный сценарий — координация многоагентных цепочек, построение пайплайнов с использованием внешних инструментов и стандартизация памяти агентов, что делает фреймворк удобным для прототипов и внутренних автоматизаций. Готовность к production — средняя: проект уже имеет 101 звезду, активные обновления и базовый набор API/CLI, но перед масштабным внедрением стоит проверить лицензию, безопасность зависимостей и наличие постоянных мейнтейнеров.

### 中文

**项目简介**  
cacheplane/angular-agent-framework 是一套基于 Angular 的 SDK，旨在帮助开发者把单个 Prompt 与工具封装成可复用的“Agent”，从而快速构建具备记忆、工具调用和多 Agent 协作的生成式 UI 应用。  

**价值**  
- **工作流标准化**：把零散的 Prompt 与工具统一抽象为 Agent，形成可组合、可重复的工作流。  
- **多 Agent 协同**：内置调度与消息路由，轻松实现多个 Agent 之间的协作与信息共享。  
- **工具链集成**：提供统一的 Tool 接口，支持把外部 API、CLI、数据库等资源直接纳入生成式交互流。  
- **记忆管理**：封装了 Agent‑Memory 模块，帮助在会话或跨会话之间持久化上下文。  

**典型接入方式**  
1. **安装 SDK**：`npm i @cacheplane/angular-agent-framework`。  
2. **在 Angular 模块中导入**：在 `AppModule` 中 `import { AgentFrameworkModule } from '@cacheplane/angular-agent-framework';` 并在 `imports` 中注册。  
3. **定义 Agent**：使用 `createAgent({ name, prompt, tools, memory })` 创建 Agent 实例。  
4. **在组件中调用**：通过注入的 `AgentService` 调用 `run(agentId, input)`，获取生成结果并绑定到 UI。  
5. **可选 CLI**：框架自带 `agf` CLI，可在本地快速生成 Agent 模板、调试工作流或导出配置。  

**生产可用性**  
- **成熟度**：当前评分 72/100，适合作为原型或内部业务系统的基础设施。  
- **依赖与维护**：项目使用 TypeScript，依赖 Angular 官方生态，近期（2026‑07‑09）有更新，GitHub 具 101 星、11 Fork，社区活跃度尚可。  
- **风险**：需进一步审查许可证、第三方依赖的安全报告以及维护者的长期可用性；在正式生产环境部署前建议进行依赖审计并加入单元/集成测试。  

总体而言，cacheplane/angular-agent-framework 为 Angular 开发者提供了一套“Prompt‑to‑Agent” 的抽象层，能够显著降低构建多 Agent、工具驱动的生成式 UI 的门槛，适合作为内部平台或 MVP 的核心技术栈。

## 🧭 Practical evaluation

**Value:** cacheplane/angular-agent-framework helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 101 GitHub stars
- 11 forks
- updated 2026-07-09
- primary language: TypeScript
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 27/100 |
| stars | 43/100 |
| topics | 63/100 |
| outlook | 72/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 38/100 |
| production | 67/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-07-09 · [View on GitHub](https://github.com/cacheplane/angular-agent-framework) · [← Back to Orchestration](./README.md)</sub>
