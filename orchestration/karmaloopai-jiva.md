# KarmaloopAI/Jiva

[![Stars](https://img.shields.io/github/stars/KarmaloopAI/Jiva?style=flat-square&color=yellow)](https://github.com/KarmaloopAI/Jiva/stargazers) [![Forks](https://img.shields.io/github/forks/KarmaloopAI/Jiva?style=flat-square&color=blue)](https://github.com/KarmaloopAI/Jiva/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-78%2F100-brightgreen?style=flat-square)](#)

> Jiva is a CLI-first, open source autonomous AI agent and open alternative to Claude. Written in TypeScript with native support for Sarvam-105B and gpt-oss-120b, it autonomously plans and executes tasks from your terminal. Supports MCP servers, a built-in Skills system, and Jiva Personas - a plugin framework fully compatible with Claude Plugins.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 35 |
| 🍴 **Forks** | 6 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 78/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `autonomous` `claude-plugins` `claude-skills` `cli` `gpt-oss-120b` `mcp-servers` `sarvam-105b`

## 🎯 Categories

Orchestration · MCP · Automation · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
Jiva is a TypeScript‑based, CLI‑first autonomous AI agent that rivals Claude while offering native support for the Sarvam‑105B and gpt‑oss‑120b models. It can plan and execute tasks from the terminal, integrates with MCP servers, provides a built‑in Skills system, and extends functionality through Jiva Personas—a plugin framework fully compatible with Claude Plugins.

**Value**  
Jiva bridges the gap between large‑language‑model assistants and real‑world tools by exposing a standard Model Context Protocol (MCP) interface. This lets developers plug AI agents into existing tooling, data stores, or custom services without writing bespoke adapters, and it re‑uses the growing ecosystem of Claude‑compatible plugins through the Personas framework.

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | **Spin up a local Jiva instance** (via the provided CLI or Docker image) | Quick, low‑risk sandbox to evaluate model support and CLI workflow. |
| 2️⃣  | **Connect to your preferred LLM** (Sarvam‑105B, gpt‑oss‑120b, or any MCP‑compatible server) | Demonstrates Jiva’s “plug‑and‑play” model selection and validates latency/throughput for your workload. |
| 3️⃣  | **Add required Skills** (e.g., file system, HTTP, DB access) using the built‑in Skills catalog or custom TypeScript modules | Shows how business‑specific actions become first‑class commands for the agent. |
| 4️⃣  | **Integrate a Persona or Claude Plugin** (e.g., calendar, ticketing) | Confirms compatibility with existing Claude Plugin ecosystem and reduces development effort. |
| 5️⃣  | **Run pilot tasks** (automated ticket triage, report generation, CI/CD orchestration) from the terminal or CI pipelines | Validates end‑to‑end autonomy, error handling, and observability. |
| 6️⃣  | **Wrap with your production CI/CD** (Docker, Helm, or serverless) and monitor via the CLI logs or exported metrics | Moves the prototype into a repeatable, production‑grade deployment. |

**Production Readiness**  
- **Activity & Community** – Updated as of 2026‑06‑30, 35 ★, 6 forks, and an active issue/PR flow indicate a healthy, maintained codebase.  
- **Architecture** – Written in TypeScript, exposing a clear API/SDK and a CLI, making integration straightforward for both frontend and backend teams.  
- **Ecosystem Fit** – Supports MCP servers, a modular Skills system, and Claude‑compatible Personas, covering most integration scenarios without custom glue code.  
- **Risk Profile** – No immediate licensing or security red flags, though a final audit of the open‑source license and dependency vulnerabilities is advisable before a full production rollout.  

Overall, Jiva is a mature OSS candidate ready for pilot projects, and with the outlined adoption steps it can be elevated to production use in environments that need autonomous AI agents tightly coupled to existing tools and data pipelines.

### Русский

**KarmaloopAI/Jiva** — это CLI‑ориентированный open‑source агент искусственного интеллекта, написанный на TypeScript и поддерживающий модели Sarvam‑105B и gpt‑oss‑120b. Он автоматически планирует и выполняет задачи из терминала, подключаясь к реальным инструментам и данным через стандартный Model Context Protocol, а также предлагает расширяемую систему Skills и плагинов‑персон (совместимых с Claude Plugins). Проект находится на высокой стадии готовности к продакшну: активные коммиты, растущее сообщество (35 звёзд, 6 форков), поддержка MCP‑серверов и готовый API/SDK/CLI делают его подходящим для быстрого пилотного внедрения в сценариях интеграции AI‑агентов с корпоративными инструментами.

### 中文

**项目价值**  
KarmaloopAI/Jiva 把强大的大模型（Sarvam‑105B、gpt‑oss‑120b 等）包装成一个 **CLI‑first 的自主 AI 代理**，能够在终端直接接收指令、自动规划并执行任务。它通过 **Model Context Protocol（MCP）** 为 AI 助手提供统一的工具和数据接入层，解决了“AI + 业务系统”之间的碎片化集成问题，同时提供可插件化的 **Skills** 与 **Jiva Personas**（兼容 Claude Plugins），让开发者可以快速扩展功能。

**典型接入方式**  

| 场景 | 接入方式 | 关键步骤 |
|------|----------|----------|
| **在本地或 CI/CD 环境使用** | 直接通过 npm 安装并调用 CLI | `npm i -g @karmaloopai/jiva` → `jiva run <task>` |
| **在自研平台对接业务系统** | 调用 Jiva 提供的 Node.js SDK / HTTP API | `import { JivaClient } from '@karmaloopai/jiva'` → `client.execute(task)` |
| **部署 MCP 服务器** | 启动 Jiva 自带的 MCP Server，供其他 AI 代理或微服务调用 | `jiva mcp start --port 8080` → 通过标准 MCP 协议发送 `tool`、`data` 请求 |
| **扩展功能** | 编写 Skills 或 Personas 插件（TS/JS）并注册 | `jiva plugin add ./my-skill.ts` → 在任务中使用 `@my-skill` |

**生产可用性**  
- **活跃度**：截至 2026‑06‑30 最近一次提交，GitHub ★35、Fork 6，社区已有基本的 issue/PR 交互。  
- **技术成熟度**：使用 TypeScript 编写，提供完整的 CLI、SDK 与 REST 接口，且兼容 Claude Plugins，降低迁移成本。  
- **安全与合规**：当前未发现重大元数据风险，仍需进一步审查许可证（MIT/Apache）和依赖安全报告。  
- **适配性**：支持 MCP、内置 Skills 系统以及可自定义 Personas，能够快速对接企业内部工具、数据库或第三方 API，适合作为 **OSS 级别的 Pilot** 项目在生产环境中验证。  

综合来看，Jiva 已具备 **高可用的框架和扩展机制**，在经过一次内部安全审计后即可在生产环境中用于 AI‑agent 与业务系统的标准化集成。

## 🧭 Practical evaluation

**Value:** KarmaloopAI/Jiva helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 35 GitHub stars
- 6 forks
- updated 2026-06-30
- primary language: TypeScript
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 21/100 |
| stars | 33/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 63/100 |
| recency | 80/100 |
| adoption | 30/100 |
| production | 72/100 |
| usefulness | 100/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/KarmaloopAI/Jiva) · [← Back to Orchestration](./README.md)</sub>
