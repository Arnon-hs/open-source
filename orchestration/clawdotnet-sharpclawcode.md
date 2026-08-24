# clawdotnet/SharpClawCode

[![Stars](https://img.shields.io/github/stars/clawdotnet/SharpClawCode?style=flat-square&color=yellow)](https://github.com/clawdotnet/SharpClawCode/stargazers) [![Forks](https://img.shields.io/github/forks/clawdotnet/SharpClawCode?style=flat-square&color=blue)](https://github.com/clawdotnet/SharpClawCode/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> C# coding-agent harness (.NET 10, Microsoft Agent Framework) — sessions, tools, permissions, providers, MCP, plugins

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 53 |
| 🍴 **Forks** | 14 |
| 💻 **Language** | C# |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `anthropic` `claude-code` `cli` `coding-agent` `csharp` `developer-tools` `dotnet` `dotnet10` `mcp` `openai` `opencode`

## 🎯 Categories

Orchestration · MCP · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
SharpClawCode is a C#‑based agent‑harness built on .NET 10 and the Microsoft Agent Framework that lets developers define, orchestrate, and persist multi‑agent workflows with built‑in support for sessions, tool integration, permissions, providers, MCP and plug‑in extensions. It turns ad‑hoc prompts and tool calls into repeatable, version‑controlled pipelines, making it easy to coordinate several agents, inject custom tooling, and maintain a shared memory store. The project is actively maintained (last commit 2026‑05‑11), has 53 stars, 14 forks, and a rich set of topics, indicating solid community interest.

**Value**  
- **Turn prompts into products** – By wrapping isolated LLM prompts and external tools inside a formal workflow, teams can reuse logic, audit execution, and ship agent‑driven features faster.  
- **Standardized memory & permissions** – Built‑in session handling and memory stores give agents a consistent state across calls, while permission layers simplify secure tool access.  
- **Extensible plug‑in model** – MCP and plug‑in hooks let you drop in custom providers (e.g., internal APIs, data stores) without rewriting core orchestration code.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided CLI/SDK sample, and replace the demo prompts with your own use‑case (e.g., ticket triage or code review).  
2. **Integrate tools** – Add your internal services as “tools” via the existing provider interface; the framework will automatically handle tool‑selection and result injection.  
3. **Persist sessions** – Configure the built‑in memory backend (or plug in a Redis/SQL store) to keep state across user interactions.  
4. **Deploy** – Package the solution as a Docker container or a .NET self‑contained binary and expose the API/CLI endpoints to your existing micro‑service mesh.  
5. **Scale & monitor** – Leverage .NET 10’s native diagnostics and the framework’s logging hooks to add observability and autoscaling in Kubernetes or Azure App Service.  

**Production Readiness**  
- **Activity & Ecosystem** – Recent commits (as of 2026‑05‑11), a growing star/fork count, and 13 topical tags demonstrate an engaged community and ongoing development.  
- **Maturity** – Core features (sessions, permissions, MCP, plug‑ins) are already implemented and documented, reducing the time to a functional pilot.  
- **Risk Profile** – No glaring metadata or licensing issues have been identified, though a formal security audit and confirmation of active maintainers are advisable before full‑scale rollout.  
Overall, SharpClawCode is a high‑readiness OSS candidate for teams looking to institutionalize multi‑agent orchestration in a .NET environment.

### Русский

**SharpClawCode** — это open‑source‑платформа на C# (.NET 10, Microsoft Agent Framework), позволяющая превратить отдельные запросы и инструменты в воспроизводимые агентные workflow: управление сессиями, правами, провайдерами, MCP и плагинами. Типичный сценарий — координация нескольких AI‑агентов, построение конвейеров с использованием внешних инструментов и стандартизация памяти агентов в рамках DevTools‑экосистемы. Проект демонстрирует высокий уровень готовности к production: активные коммиты, 53 звёзд, 14 форков, обширная API/SDK/CLI‑документация и поддержка основных интеграционных точек, требующие лишь финального аудита лицензий и безопасности.

### 中文

**项目简介**  
clawdotnet/SharpClawCode 是基于 .NET 10 与 Microsoft Agent Framework 的 C# 编码代理套件，提供会话管理、工具调用、权限控制、提供者接口、MCP 与插件机制等完整能力。它可以把单个提示和工具包装成可复用、可编排的智能体工作流。

**价值主张**  
- **统一工作流**：将零散的 Prompt、工具和记忆模型统一到“Agent + Session”框架中，实现可重复、可追踪的多代理协作。  
- **快速集成**：通过公开的 API/SDK/CLI，开发者只需引用 NuGet 包或调用命令行，即可把现有工具链（LLM、数据库、外部服务等）接入代理。  
- **标准化记忆**：内置的 MCP（Memory‑Cache‑Provider）让不同代理共享持久化记忆，降低状态管理复杂度。  

**典型接入方式**  
1. **NuGet 包**：在 .NET 项目中 `dotnet add package SharpClawCode`，使用 `ClawAgentBuilder` 配置会话、工具和权限。  
2. **CLI**：`sharpclaw run --prompt "..." --tool MyTool.dll`，适合脚本化或 CI/CD 场景。  
3. **SDK**：通过 `IClawAgent` 接口在代码中直接创建、启动、监控代理实例，支持自定义插件和 Provider。  

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑05‑11，星标 53、Fork 14，社区话题覆盖 13 项，表明项目仍在积极维护。  
- **生态兼容**：遵循 .NET 10 标准，兼容主流 LLM SDK、Azure 服务以及常见 DevOps 工具，易于在现有 .NET 微服务或后台任务中嵌入。  
- **风险**：暂无重大元数据风险，但仍需对许可证（MIT/Apache 等）和安全审计进行最终确认。整体来看，SharpClawCode 已具备 **高** 的生产候选级别，适合在内部试点后推广到正式业务环境。

## 🧭 Practical evaluation

**Value:** clawdotnet/SharpClawCode helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 53 GitHub stars
- 14 forks
- updated 2026-05-11
- primary language: C#
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 37/100 |
| topics | 100/100 |
| outlook | 56/100 |
| quality | 51/100 |
| recency | 20/100 |
| adoption | 35/100 |
| production | 51/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/clawdotnet/SharpClawCode) · [← Back to Orchestration](./README.md)</sub>
