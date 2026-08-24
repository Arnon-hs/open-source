# phuetz/code-buddy

[![Stars](https://img.shields.io/github/stars/phuetz/code-buddy?style=flat-square&color=yellow)](https://github.com/phuetz/code-buddy/stargazers) [![Forks](https://img.shields.io/github/forks/phuetz/code-buddy?style=flat-square&color=blue)](https://github.com/phuetz/code-buddy/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> Open-source multi-provider AI coding agent: terminal TUI, Electron desktop cockpit (Cowork), and a 24/7 autonomous multi-AI fleet that runs free-first on local Ollama. 15 LLM providers (Claude, GPT, Gemini, Grok), ~110 tools, voice + vision companion, MCP.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 21 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic` `ai-agent` `ai-coding-assistant` `autonomous-agents` `chatgpt` `claude` `cli` `coding-agent` `computer-use` `developer-tools` `electron` `free`

## 🎯 Categories

Orchestration · MCP · Automation · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
phuetz/code‑buddy is an open‑source, multi‑provider AI coding agent that lets developers orchestrate up to 15 LLMs, 110+ tools, voice/vision companions, and a 24/7 autonomous fleet from a terminal UI, an Electron desktop cockpit (Cowork), or via API/CLI. It converts ad‑hoc prompts into repeatable, memory‑backed agent workflows, making complex multi‑agent pipelines easy to build and share.

**Value**  
- **Unified orchestration**: One platform to coordinate many LLMs and tools, eliminating the need to stitch together disparate APIs.  
- **Repeatable workflows**: Agent memory and tool‑use pipelines are codified, enabling consistent results across runs and teams.  
- **Flexibility & extensibility**: Works locally with Ollama (free‑first) and can fall back to cloud providers (Claude, GPT, Gemini, Grok, etc.), supporting voice, vision, and custom extensions.  

**Practical Adoption Path**  
1. **Pilot with the TUI** – Clone the repo, run the terminal UI locally, and connect to your preferred LLM (e.g., Ollama) to experiment with prompt‑to‑action flows.  
2. **Integrate via CLI/SDK** – Use the provided CLI or TypeScript SDK to embed Code‑Buddy into CI pipelines, VS Code extensions, or internal tooling.  
3. **Scale with Cowork** – Deploy the Electron “Cockpit” for a shared desktop experience, enabling teams to monitor and manage the autonomous fleet.  
4. **Extend** – Add custom tools or third‑party APIs by following the documented plugin interface; the platform automatically incorporates them into agent reasoning.  

**Production Readiness**  
- **Active maintenance**: Recent commits (as of 2026‑06‑26), 21 stars, and ongoing community forks indicate a healthy open‑source project.  
- **Robust ecosystem**: Supports 15 LLM providers, a large tool catalog, and standard interfaces (API/CLI/SDK), easing integration with existing stacks.  
- **Security & licensing**: No immediate metadata risks, but a final review of the license (likely MIT) and dependency security posture is advisable before a full production rollout.  

Overall, Code‑Buddy is mature enough for a serious pilot in development teams looking to automate multi‑LLM coding workflows while retaining the option to run entirely on‑premise.

### Русский

**phuetz/code-buddy** — это открытый AI‑агент, объединяющий более 15 LLM‑провайдеров (Claude, GPT, Gemini, Grok и др.) с ~110 инструментами, голосовым и визуальным помощником и возможностью работать 24/7 в виде автономного флота агентов (локально через Ollama). Он позволяет превратить разрозненные запросы и утилиты в повторяемые рабочие процессы: координация многокомпонентных агентных сценариев, построение конвейеров с использованием инструментов и стандартизация памяти агентов. Проект находится на высокой стадии готовности к production: активные коммиты, растущее сообщество (21 звезда, 4 форка), поддержка API/SDK/CLI и типичная стек‑технология (TypeScript), что делает его подходящим для пилотного внедрения в оркестрацию, MCP и автоматизацию.

### 中文

**项目简介**  
phuetz/code‑buddy 是一个开源的多供应商 AI 编码助手，提供终端 TUI、Electron 桌面 cockpit（Cowork）以及 24/7 自动化的多 AI 编队。它默认在本地 Ollama 上免费运行，支持 15 家 LLM（Claude、GPT、Gemini、Grok 等），集成约 110 种工具，并配备语音+视觉伙伴以及多租户控制面板（MCP），帮助把零散的 Prompt 与工具组织成可重复的 Agent 工作流。

**核心价值**  
- **统一编排**：把不同 LLM、工具、记忆库统一调度，形成端到端的多 Agent 流程，降低手工拼接的复杂度。  
- **跨平台体验**：从纯终端到图形化桌面，再到后台自动 fleet，满足开发者、运维和产品团队的不同使用场景。  
- **本地优先、成本可控**：默认走本地 Ollama，避免云端调用费用，亦可无缝切换到云供应商。  

**典型接入方式**  
1. **CLI / SDK**：通过项目自带的 `code-buddy` 命令行或 TypeScript SDK 调用 API，快速在脚本或 CI 中嵌入 Agent。  
2. **Electron Cockpit**：在桌面环境下启动 Cowork，直接拖拽工具、配置 Prompt，适合交互式开发。  
3. **MCP（多租户控制面板）**：在企业内部部署一个 HTTP 服务，使用 RESTful 接口或 WebSocket 与外部系统（如 Jira、GitHub Actions）对接，实现全链路自动化。  

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑26，星标 21、fork 4，代码基于 TypeScript，维护频率稳定。  
- **生态兼容**：公开的 API/SDK/CLI、完整的语言元数据以及清晰的主题标签，使评估与集成成本低。  
- **成熟度**：具备完整的工具链、记忆管理和多 AI 编排能力，已可在内部 pilot 项目中使用；唯一待确认的风险是许可证、长期安全维护和维护者承诺，需要在正式生产前完成最终审查。  

综上，code‑buddy 在 OSS 场景下已经具备较高的生产就绪度，适合作为公司内部的 AI 编码编排平台或作为多 Agent 工作流的实验基座。

## 🧭 Practical evaluation

**Value:** phuetz/code-buddy helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 21 GitHub stars
- 4 forks
- updated 2026-06-26
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
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

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/phuetz/code-buddy) · [← Back to Orchestration](./README.md)</sub>
