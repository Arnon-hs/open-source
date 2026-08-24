# Agents365-ai/pi-plugin-cc

[![Stars](https://img.shields.io/github/stars/Agents365-ai/pi-plugin-cc?style=flat-square&color=yellow)](https://github.com/Agents365-ai/pi-plugin-cc/stargazers) [![Forks](https://img.shields.io/github/forks/Agents365-ai/pi-plugin-cc?style=flat-square&color=blue)](https://github.com/Agents365-ai/pi-plugin-cc/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-49%2F100-brightgreen?style=flat-square)](#)

> Claude Code plugin that routes /pi:review, /pi:rescue, etc. through the Pi coding agent (default: DeepSeek V4). Adapted from codex-plugin-cc.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 27 |
| 🍴 **Forks** | 2 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 49/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`claude-code` `claude-code-plugin` `code-review` `coding-agent` `deepseek` `pi-coding-agent`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Agents365‑ai/pi‑plugin‑cc is a Claude‑compatible code‑assistant plugin that forwards special commands such as `/pi:review` and `/pi:rescue` to a Pi coding agent (by default DeepSeek V4). It is a lightweight adaptation of the original codex‑plugin‑cc, exposing a simple JavaScript API/CLI that lets developers inject AI‑powered code‑review, rescue, and other assistance capabilities into their tools without building a model stack from scratch.

**Value**  
- **Fast AI enablement** – By reusing an existing, high‑performing LLM (DeepSeek V4) the plugin eliminates the need to train or host a custom model, accelerating prototype development.  
- **Plug‑and‑play integration** – The exposed API/SDK and clear command syntax let teams add code‑review, debugging, or RAG‑style assistance to IDEs, CI pipelines, or internal bots with only a few lines of JavaScript.  
- **Extensible workflow** – Because the plugin routes through a generic “Pi” agent, developers can swap the backend model or extend the command set without altering their surrounding code.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run `npm install`, and call the provided CLI or import the SDK in a test project.  
2. **Integrate** – Map your existing tooling (e.g., GitHub Actions, VS Code extensions, or internal chat bots) to the `/pi:*` commands, using the supplied language‑metadata helpers to route the right payloads.  
3. **Validate** – Run a controlled evaluation against your codebase to measure review accuracy, latency, and token cost; adjust the backend model (e.g., switch from DeepSeek V4 to another Pi‑compatible model) via the simple configuration file.  
4. **Secure & Harden** – Conduct a security audit of the dependency chain, verify the license compatibility, and add monitoring/logging around the API calls before promoting the integration to production.

**Production Readiness**  
- **Maturity** – Medium. The plugin is functional and actively updated (last commit 2026‑07‑13) with 27 GitHub stars, but the ecosystem is still small (2 forks) and maintainer activity is modest.  
- **Suitability** – Ideal for internal prototypes, proof‑of‑concepts, or low‑risk workflows (e.g., automated code linting or pre‑merge checks).  
- **Considerations before production** – Perform a thorough dependency audit, confirm the licensing terms for DeepSeek V4 and any transitive libraries, and establish fallback mechanisms (e.g., a backup model or graceful degradation) to mitigate service outages. Once those checks are in place, the plugin can be promoted to internal production use, with the expectation of occasional updates as the underlying Pi agents evolve.

### Русский

**Agents365‑ai/pi‑plugin‑cc** — это open‑source плагин для Claude Code, который перенаправляет запросы `/pi:review`, `/pi:rescue` и др. к кодирующему агенту Pi (по умолчанию DeepSeek V4), позволяя быстро добавить AI‑функциональность без построения собственного стека моделей. Типичный сценарий — прототипирование AI‑фич, построение RAG‑ или агентных воркфлоу и оценка инструментов модели через простой API/SDK/CLI; проект уже имеет базовую готовность (27 звёзд, активные обновления, JavaScript‑реализация), что делает его подходящим для внутренних прототипов и ограниченных продакшн‑использований после проверки лицензий, безопасности и поддержки.

### 中文

**项目简介**  
Agents365‑ai/pi-plugin-cc 是基于 Claude Code 的插件，能够把 `/pi:review`、`/pi:rescue` 等指令转发给 Pi 编码代理（默认使用 DeepSeek V4），实现代码审查、错误救援等功能。项目改编自 codex‑plugin‑cc，采用 JavaScript 编写，已在 GitHub 获得 27 星、2 Fork，最近一次更新于 2026‑07‑13。

**价值**  
- **快速赋能**：无需自行搭建模型堆栈，只需接入插件即可让现有系统具备代码审查、自动修复等 AI 能力。  
- **原型与实验**：非常适合在内部原型、RAG（检索增强生成）或多代理工作流中快速验证想法。  
- **统一入口**：统一的 `/pi:*` 路由让前端或 CLI 调用保持一致，降低集成复杂度。

**典型接入方式**  
1. **API/SDK**：通过插件暴露的 HTTP API（或对应的 Node.js SDK）发送 `/pi:review`、`/pi:rescue` 等请求。  
2. **CLI**：在本地或 CI 环境中直接调用插件提供的命令行工具，适合脚本化批量处理。  
3. **语言/主题元数据**：插件会返回代码语言、文件路径等元信息，便于后续 RAG 或多代理编排。  

**生产可用性**  
- **成熟度**：目前评估为 *Medium*，适合原型、内部工具或受控环境使用。  
- **准备工作**：在生产环境部署前，需要检查以下事项：  
  - 依赖版本（Node.js、DeepSeek V4 API）是否与现有系统兼容。  
  - 安全审计：确认插件的许可证、第三方库的安全状况以及 API 密钥管理。  
  - 维护者活跃度：虽然最近有更新，但仍建议与项目维护者沟通确认长期支持计划。  

总体而言，Agents365‑ai/pi-plugin-cc 为想在现有产品中快速加入代码相关 AI 功能的团队提供了低门槛、可扩展的解决方案，只要完成依赖与安全审查，即可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** Agents365-ai/pi-plugin-cc helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 27 GitHub stars
- 2 forks
- updated 2026-07-13
- primary language: JavaScript
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 12/100 |
| stars | 31/100 |
| topics | 75/100 |
| outlook | 49/100 |
| quality | 48/100 |
| recency | 40/100 |
| adoption | 26/100 |
| production | 50/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/Agents365-ai/pi-plugin-cc) · [← Back to AI/ML](./README.md)</sub>
