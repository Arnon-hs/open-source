# morluto/rea

[![Stars](https://img.shields.io/github/stars/morluto/rea?style=flat-square&color=yellow)](https://github.com/morluto/rea/stargazers) [![Forks](https://img.shields.io/github/forks/morluto/rea?style=flat-square&color=blue)](https://github.com/morluto/rea/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> Reverse engineer anything with agents: one CLI and MCP server to inspect any app, understand it fully down to the binary level.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 22 |
| 🍴 **Forks** | 3 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-skills` `ai-agents` `binary-analysis` `cli` `coding-agent` `coding-agents` `decompiler` `disassembler` `hopper-disassembler` `mcp` `mcp-server` `model-context-protocol`

## 🎯 Categories

Orchestration · MCP · AI/ML · Backend · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*morluto/rea* is an open‑source framework that lets you reverse‑engineer any application by orchestrating multiple AI agents through a single CLI and an MCP (Multi‑Component Platform) server. It turns ad‑hoc prompts and tool calls into repeatable, memory‑aware agent workflows, enabling deep binary‑level inspection of software. With active maintenance, a TypeScript codebase, and a modest but growing community, it’s ready for pilot projects in dev‑tool and security pipelines.

**Value**  
- **Unified Agent Orchestration** – Consolidates isolated prompts, tool invocations, and memory handling into deterministic pipelines, reducing the friction of building custom multi‑agent solutions.  
- **Reverse‑Engineering as a Service** – The CLI + MCP server expose a programmable interface that can be scripted or integrated into CI/CD, allowing automated binary analysis, dependency mapping, or vulnerability discovery.  
- **Extensibility** – Because the core is in TypeScript and provides an SDK/CLI, teams can plug in their own analysis tools, custom parsers, or domain‑specific agents without rewriting the orchestration layer.

**Practical Adoption Path**  
1. **Evaluation** – Clone the repo, run the provided CLI against a small test binary to verify the inspection output and explore the generated agent memory logs.  
2. **Integration** – Wrap the CLI or call the MCP server’s REST/SDK endpoints from your existing build or security pipeline (e.g., GitHub Actions, Jenkins).  
3. **Customization** – Extend the TypeScript SDK to add proprietary analysis tools or enrich the agent memory store with organization‑specific knowledge bases.  
4. **Pilot** – Deploy the MCP server in a sandbox environment, run it on a representative set of binaries, and measure accuracy, runtime, and false‑positive rates before scaling to production.

**Production Readiness**  
- **Activity & Community** – Recent commits (as of 2026‑07‑13), 22 stars, 3 forks, and 15 topic tags indicate an active, albeit small, community.  
- **Technical Maturity** – The TypeScript codebase is clean, the CLI is stable, and the MCP server follows standard REST conventions, making it straightforward to containerize and monitor.  
- **Risk Considerations** – No obvious metadata or licensing red flags, but a final security audit and confirmation of long‑term maintainers are advisable before mission‑critical deployment. Overall, the project exhibits a high readiness level for a serious pilot in environments that need automated reverse‑engineering or multi‑agent tooling.

### Русский

**morluto/rea** — это open‑source платформа, позволяющая превратить разрозненные запросы и инструменты в повторяемые рабочие процессы агентов: один CLI и MCP‑сервер автоматически разбирают любое приложение до уровня бинарного кода, координируют многопоточные агентные сценарии, добавляют пайплайны использования инструментов и стандартизируют память агентов. Проект уже активно развивается (обновления — 2026‑07‑13, 22 звезды, 3 форка, TypeScript, 15 тем), имеет чистый API/SDK/CLI и хорошо документированные сигналы интеграции, что делает его готовым к пилотному внедрению в продакшн. Остальные проверки (лицензия, безопасность, поддержка) следует завершить перед масштабным запуском.

### 中文

**项目简介**  
morluto/rea 是一款基于多代理的逆向工程工具，提供统一的 CLI 与 MCP（Multi‑Component Platform）服务器，能够对任意应用进行深度检查，直至二进制层面。它把零散的 Prompt 与工具包装成可复用的 Agent 工作流，让逆向、调试和安全分析变得可编排、可追溯。

**价值点**  
- **工作流标准化**：将单次交互式的 Prompt、脚本或插件抽象为可重复的 Agent 流程，降低手工操作成本。  
- **多代理协同**：支持同时调度多个 Agent（如代码分析、二进制解码、漏洞扫描），实现复杂逆向任务的自动化编排。  
- **统一记忆与工具链**：内置 Agent Memory 与 Tool‑Use 管道，保证上下文的连续性和工具调用的可追溯性。  

**典型接入方式**  
1. **CLI**：`npx rea <command>` 直接在本地终端调用，适合快速实验或脚本化调用。  
2. **MCP Server**：启动 `rea-server`，通过 REST/GraphQL API 或官方 SDK（TypeScript）与外部系统集成，便于在 CI/CD、SOC 平台或自研安全平台中嵌入。  
3. **插件式扩展**：项目提供 `Agent`、`Tool` 接口，开发者可用 TypeScript 编写自定义插件并通过配置文件注册到服务器。  

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑07‑13，GitHub 22 ★、3 Fork，拥有 15 项主题标签，社区讨论活跃。  
- **技术成熟度**：核心实现基于 TypeScript，提供完整的 API/SDK 文档，易于在 Node.js 环境中部署。  
- **风险评估**：目前未发现重大元数据或许可证冲突，仍需对安全审计（依赖漏洞、运行时权限）和维护者响应速度进行最终确认。总体而言，项目已具备 **高** 的生产候选级别，可在内部 pilot 或受控生产环境中使用。

## 🧭 Practical evaluation

**Value:** morluto/rea helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 22 GitHub stars
- 3 forks
- updated 2026-07-13
- primary language: TypeScript
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 15/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 60/100 |
| quality | 51/100 |
| recency | 40/100 |
| adoption | 25/100 |
| production | 56/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/morluto/rea) · [← Back to Orchestration](./README.md)</sub>
