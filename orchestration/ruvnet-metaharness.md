# ruvnet/metaharness

[![Stars](https://img.shields.io/github/stars/ruvnet/metaharness?style=flat-square&color=yellow)](https://github.com/ruvnet/metaharness/stargazers) [![Forks](https://img.shields.io/github/forks/ruvnet/metaharness?style=flat-square&color=blue)](https://github.com/ruvnet/metaharness/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> 🛠️ The meta-harness for AI agents — scaffold your own focused, branded agent harness with its own npx CLI, MCP server, memory, learning loop, and witness-signed releases. Works with Claude Code, Codex, pi.dev, Hermes, OpenClaw, and RVM (hardware-isolated sandbox).

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 344 |
| 🍴 **Forks** | 35 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-harness` `agent-harness-generator` `agent-scaffolding` `agentic-ai` `agentic-framework` `autonomous-agents` `claude-code` `codex` `create-agent-harness` `hermes-agent` `mcp` `mcp-server`

## 🎯 Categories

Orchestration · MCP · Automation · AI/ML · Backend

## 📝 Summary

### English

**Summary:**
The ruvnet/metaharness project is an open-source framework that enables users to create custom, branded AI agent harnesses for automating workflows and standardizing agent memory. This meta-harness provides a scaffold for building repeatable agent workflows, integrating with various AI tools, and exposing implementation signals for evaluation. With its high production readiness and strong ecosystem signals, it is suitable for serious piloting.

**Value:**
The value proposition of ruvnet/metaharness lies in its ability to turn isolated prompts and tools into repeatable agent workflows, making it easier to coordinate multi-agent workflows, add tool-use pipelines, and standardize agent memory. This framework helps users create a focused, branded agent harness with its own npx CLI, MCP server, memory, learning loop, and witness-signed releases.

**Practical Adoption Path:**
To adopt ruvnet/metaharness, users can start by evaluating its implementation signals, such as API/SDK/CLI, language metadata, or focused topics. They can then integrate the framework with their existing AI tools, such as Claude Code, Codex, pi.dev, Hermes, OpenClaw, and RVM. With its straightforward integration process, users can quickly get started with building their custom AI agent harnesses.

**Production

### Русский

**r​uvnet/metaharness** — это открытый фреймворк‑скелетон для создания брендированных AI‑агентов с собственным CLI (npx), сервером MCP, памятью, циклом обучения и подписью релизов. Он позволяет быстро превратить отдельные промпты и инструменты (Claude Code, Codex, pi.dev, Hermes, OpenClaw, RVM) в повторяемые, масштабируемые рабочие процессы с координацией нескольких агентов, пайплайнами инструментов и стандартизированной памятью. Проект уже имеет 344 ★, активные коммиты (последний — 2026‑06‑29), поддержку TypeScript и богатую экосистему, что делает его готовым к пилотному внедрению в production, при условии финального аудита лицензии и безопасности.

### 中文

**项目简介**  
ruvnet/metaharness 是一套面向 AI 代理的元‑harness，提供 npx CLI、MCP 服务器、记忆库、学习循环以及见证签名发布等完整脚手架。它即插即用，兼容 Claude Code、Codex、pi.dev、Hermes、OpenClaw 以及硬件隔离的 RVM 沙箱，让开发者能够快速构建品牌化、可复用的智能代理。

**价值**  
- **从碎片化 Prompt 到可重复的工作流**：把单个提示词和工具链封装成完整的代理流程，提升开发效率和可维护性。  
- **统一记忆与学习机制**：内置持久记忆和自我学习循环，帮助代理在多轮交互中保持上下文并逐步改进。  
- **多代理协同与工具管线**：支持多代理协作、工具调用链和自定义插件，适用于复杂业务编排。  

**典型接入方式**  
1. **CLI 安装**：`npx @ruvnet/metaharness init` 快速生成项目骨架。  
2. **SDK 调用**：在 TypeScript/JavaScript 项目中引入 `@ruvnet/metaharness` 包，使用其 API 创建、管理 MCP 实例和记忆库。  
3. **MCP 服务部署**：将生成的 MCP 服务器容器化（Docker）或直接在 Kubernetes 中运行，即可对外提供统一的代理调度接口。  
4. **工具链集成**：通过配置文件声明外部工具（Claude、Codex、pi.dev 等），框架会自动生成对应的工具调用适配层。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑29 最近一次提交，拥有 344 Stars、35 Forks，社区讨论活跃。  
- **技术成熟**：采用 TypeScript 编写，提供完整的 API/CLI 文档，且已在多个内部项目中验证。  
- **安全与合规**：使用硬件隔离的 RVM 沙箱，可在受限环境中安全运行代码；但仍建议在正式上线前完成许可证和安全审计。  
- **适配度强**：兼容主流 LLM 与代码生成模型，易于在现有 AI 基础设施中嵌入。  

综上，ruvnet/metaharness 已具备较高的生产就绪度，适合作为企业级 AI 代理编排的底层框架进行试点或正式部署。

## 🧭 Practical evaluation

**Value:** ruvnet/metaharness helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 344 GitHub stars
- 35 forks
- updated 2026-06-29
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 39/100 |
| stars | 54/100 |
| topics | 100/100 |
| outlook | 66/100 |
| quality | 62/100 |
| recency | 40/100 |
| adoption | 50/100 |
| production | 60/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/ruvnet/metaharness) · [← Back to Orchestration](./README.md)</sub>
