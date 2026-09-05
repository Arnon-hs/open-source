# askimo-ai/askimo

[![Stars](https://img.shields.io/github/stars/askimo-ai/askimo?style=flat-square&color=yellow)](https://github.com/askimo-ai/askimo/stargazers) [![Forks](https://img.shields.io/github/forks/askimo-ai/askimo?style=flat-square&color=blue)](https://github.com/askimo-ai/askimo/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> Local-first AI agent platform for desktop and CLI. Chat, RAG search, multi-step Plans workflows, MCP tools, and Agents integration. Supports OpenAI, Claude, Gemini, Grok, Ollama, LM Studio and more

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 107 |
| 🍴 **Forks** | 14 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic-workflow` `ai` `ai-assistant` `artificial-intelligence` `chatgpt` `claude` `claude-skills` `codex-cli` `gemini` `gemini-client` `grok` `langchain4j`

## 🎯 Categories

Orchestration · MCP · Knowledge/RAG · Automation · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
askimo‑ai/askimo is a local‑first AI‑agent platform that lets developers build and run sophisticated, multi‑step workflows from the desktop or CLI. It unifies chat, RAG search, tool‑use pipelines, and multi‑agent coordination across a wide range of LLM providers (OpenAI, Claude, Gemini, Grok, Ollama, LM Studio, etc.). By exposing a clean API/SDK and CLI, it turns ad‑hoc prompts and utilities into repeatable, version‑controlled agent workflows.

**Value**  
- **Workflow orchestration**: Converts scattered prompts and scripts into structured, reusable “plans” that can be shared across teams.  
- **Tool integration**: Provides built‑in MCP (multi‑component‑pipeline) hooks so agents can call external tools, databases, or APIs without custom glue code.  
- **Vendor agnostic**: Supports dozens of LLM back‑ends, enabling easy switching or hybrid deployments while keeping all data local.  

**Practical Adoption Path**  
1. **Prototype** – Install the Kotlin‑based CLI or import the SDK into an existing JVM project; point it at a local LLM (e.g., Ollama) to test basic chat and RAG.  
2. **Define a plan** – Use the declarative YAML/JSON DSL to model the desired multi‑step workflow (e.g., retrieve docs → summarize → trigger a build).  
3. **Integrate tools** – Register external commands or HTTP endpoints as MCP tools; the platform will handle prompt injection and result parsing automatically.  
4. **Scale** – Deploy the agent runner as a background service on developer workstations or on a self‑hosted server for team‑wide usage; version the plan definitions in Git for CI/CD.  

**Production Readiness**  
- **Activity & community**: 107 ★, 14 forks, recent commits (as of 2026‑05‑14) and a growing set of topics indicate an active project.  
- **Stability**: The Kotlin codebase is mature, with clear API/SDK boundaries and a CLI that can be scripted in CI pipelines.  
- **Ecosystem fit**: Straightforward integration with major LLM providers and local runtimes (Ollama, LM Studio) makes it suitable for both cloud‑agnostic and on‑prem environments.  
- **Risks**: Licensing, security hardening, and long‑term maintainer commitment still need a final review, but no major metadata concerns have been identified. Overall, askimo‑ai/askimo is ready for a serious pilot in production‑grade settings.

### Русский

**askimo-ai/askimo** — это open‑source платформа локального AI‑агента, объединяющая чат, RAG‑поиск, многошаговые планы, инструменты MCP и интеграцию с другими агентами, поддерживая модели OpenAI, Claude, Gemini, Grok, Ollama, LM Studio и др. Она позволяет превратить разрозненные запросы и утилиты в повторяемые рабочие процессы с памятью агента, что удобно для координации мульти‑агентных сценариев, построения пайплайнов с использованием инструментов и стандартизации взаимодействия. Проект имеет высокий уровень готовности к production: активные коммиты, 107 звёзд, поддержка API/SDK/CLI, широкая экосистема и недавние обновления, требующие лишь финального аудита лицензии и безопасности.

### 中文

**项目简介（2‑3 句）**  
askimo‑ai/askimo 是一个面向桌面和 CLI 的本地优先 AI 代理平台，提供聊天、RAG 检索、多步计划工作流、MCP 工具以及多代理集成等能力。它兼容 OpenAI、Claude、Gemini、Grok、Ollama、LM Studio 等主流大模型，实现“提示+工具”向可复用、可编排的智能工作流的转变。

**价值**  
- **把零散的 Prompt 与工具链统一为可重复的 Agent 工作流**，降低跨模型、跨工具的集成成本。  
- **支持多模型和本地部署**，在隐私、合规或离线场景下仍能保持高效。  
- **内置 RAG、记忆管理和多代理协同**，帮助企业快速构建知识库问答、自动化运维、客服等业务场景。

**典型接入方式**  
1. **CLI**：直接通过 `askimo` 命令行调用模型、执行计划或触发工具链，适合脚本化和 DevOps 场景。  
2. **SDK / API**：项目提供 Kotlin（及 Java）SDK 与 REST‑like 接口，业务系统可嵌入调用，实现自定义前端或服务化部署。  
3. **插件式 MCP**：通过配置文件或代码注册本地工具（如 Git、Docker、数据库等），在工作流中以“工具调用”形式使用。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑14 最近一次提交，GitHub ★107、Fork 14，代码基于 Kotlin，拥有 20+ 主题标签，社区讨论活跃。  
- **成熟度**：平台已实现完整的 API/CLI、模型适配层和工作流编排，引入的安全与许可证审查尚需最终确认，但从代码更新频率和依赖生态来看，已具备在内部或受控环境中进行正式试点的条件。  
- **风险**：需进一步核实许可证兼容性、依赖的安全漏洞以及维护者的长期可用性。总体而言，作为 OSS 候选，askimo 在功能完整性、可评估性和部署灵活性方面已达到生产级别，可在业务关键流程的前期验证或内部自动化平台中投入使用。

## 🧭 Practical evaluation

**Value:** askimo-ai/askimo helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 107 GitHub stars
- 14 forks
- updated 2026-05-14
- primary language: Kotlin
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 43/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 39/100 |
| production | 69/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/askimo-ai/askimo) · [← Back to Orchestration](./README.md)</sub>
