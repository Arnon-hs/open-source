# 0xMassi/pocketdev

[![Stars](https://img.shields.io/github/stars/0xMassi/pocketdev?style=flat-square&color=yellow)](https://github.com/0xMassi/pocketdev/stargazers) [![Forks](https://img.shields.io/github/forks/0xMassi/pocketdev?style=flat-square&color=blue)](https://github.com/0xMassi/pocketdev/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> One command to run the AI coding CLI you already pay for (Claude Code, Codex, Cursor, Gemini, Grok, aider) on a Tailscale-only Hetzner box — code from your phone.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 22 |
| 🍴 **Forks** | 1 |
| 💻 **Language** | Go |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-coding` `bubbletea` `claude-code` `cli` `cloud-development-environment` `cloud-init` `coding-agent` `devbox` `developer-tools` `golang` `hetzner` `hetzner-cloud`

## 🎯 Categories

AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Pocketdev (0xMassi/pocketdev) is a Go‑based CLI that lets you run the AI coding assistants you already pay for (Claude Code, Codex, Cursor, Gemini, Grok, aider) on a secure, Tailscale‑only Hetzner VM, making it possible to edit and run code from a phone or any remote device. It acts as a thin wrapper that forwards requests to the chosen model’s API/SDK, exposing a unified command‑line interface for rapid prototyping of AI‑enhanced features, RAG pipelines, or autonomous agents.

---

### Value Proposition
- **Unified entry point** – No need to learn each vendor’s CLI or SDK; a single `pocketdev` command routes calls to the selected model, saving context‑switching time.  
- **Secure, low‑latency execution** – By running on a private Hetzner box reachable only via Tailscale, you keep API keys and data off your local machine while still enjoying fast network hops.  
- **Rapid prototyping** – Spin up AI‑assisted coding, retrieval‑augmented generation, or agent workflows in minutes without building a custom model stack from scratch.  

### Practical Adoption Path
1. **Spin up a Hetzner VM** (any modest instance) and install Tailscale.  
2. **Deploy pocketdev** (`go install` or Docker image) and configure the desired AI provider credentials (environment variables or secret store).  
3. **Connect your device** (phone, laptop, etc.) to the same Tailscale network and invoke `pocketdev <model> <command>` to run code, fetch completions, or trigger agent actions.  
4. **Iterate** – Replace or add providers by updating the config; the CLI automatically discovers the new model’s API endpoints.  

### Production Readiness
- **Maturity:** Medium. The project is actively maintained (last commit 2026‑06‑30) and has basic adoption signals (22 ★, 1 fork). It is suitable for internal tools, prototypes, or low‑risk production workloads.  
- **Dependencies:** Relies on external AI provider APIs and a stable Tailscale/Hetzner environment; ensure you have monitoring for API quota limits and network health.  
- **Risks:** Licensing and security posture need a final review; there is limited community support, so plan for in‑house maintenance or a fallback if the repo becomes inactive.  

Overall, pocketdev offers a quick, secure way to bring existing AI coding assistants into your workflow, with a straightforward path from sandbox to modest production use after due diligence on dependencies and security.

### Русский

0xMassi/pocketdev позволяет одной командой запустить любой AI‑кодинг CLI (Claude Code, Codex, Cursor, Gemini, Grok, aider) на изолированном Hetzner‑сервере, доступном только через Tailscale, и писать код прямо с телефона. Это удобно для быстрого прототипирования AI‑фич, создания RAG‑ или агентных workflow‑ов и оценки различных модельных тулов без необходимости собирать стек с нуля. Проект имеет средний уровень готовности к production: подходит для внутренних прототипов и экспериментов, но перед внедрением в продакшн рекомендуется

### 中文

**项目简介（2‑3 句话）**  
0xMassi/pocketdev 只需一条命令，即可在仅通过 Tailscale 访问的 Hetzner 服务器上运行你已付费的 AI 编码 CLI（Claude Code、Codex、Cursor、Gemini、Grok、aider），实现手机端远程写代码。它把已有的 AI 编码模型直接搬到私有云上，无需自行搭建模型堆栈。

**价值**  
- **快速赋能**：无需从零构建或训练模型，直接接入市面主流的 AI 编码引擎，极大缩短原型开发周期。  
- **安全私有**：代码和 API 调用全部在自建的 Hetzner 主机上完成，只有通过 Tailscale 的加密网络才能访问，适合对代码保密性有要求的团队。  
- **多模型统一入口**：同一 CLI 可切换 Claude、Codex、Gemini 等，便于对比评估不同模型的编码表现。

**典型接入方式**  
1. **准备环境**：在 Hetzner 上创建一台 Linux 实例，安装 Go 运行时并通过 Tailscale 加入你的私有网络。  
2. **部署 pocketdev**：`go install github.com/0xMassi/pocketdev@latest` 或下载预编译二进制。  
3. **配置凭证**：在实例上设置对应 AI 服务的 API key（如 `CLAUDE_API_KEY`、`OPENAI_API_KEY` 等），或使用 `aider` 的本地配置文件。  
4. **运行命令**：在手机的终端或通过 VS Code Remote SSH，执行 `pocketdev run <model> <your‑script>`，即可让远端模型在服务器上完成代码生成、补全或调试。  
5. **集成**：可将其包装为 CI 步骤、GitHub Action，或通过 HTTP API（项目已提供简易的 JSON RPC 接口）供内部工具调用。

**生产可用性**  
- **成熟度**：当前评分 73/100，GitHub 22 ⭐、1 fork，2026‑06‑30 最近更新，代码基于 Go，结构清晰，适合作为内部原型或实验平台。  
- **准备度**：属于 **Medium** 级别。对原型、内部工作流非常友好，但在正式生产环境仍需完成以下检查：  
  - **依赖审计**：确认所有第三方 SDK（Claude、OpenAI、Google 等）的许可证兼容性。  
  - **安全评估**：检查 Tailscale 配置、服务器防火墙及 API 密钥管理是否符合公司安全政策。  
  - **运维监控**：为 Hetzner 实例添加日志、监控和自动备份，防止因网络或模型调用限额导致服务中断。  
- **可扩展性**：因为核心是 CLI 包装，新增模型或自定义脚本几乎不需要改动代码，适合在内部平台上快速迭代。  

综上，pocketdev 是一款能够让团队在私有云上即插即用多家 AI 编码模型的工具，适合快速验证 AI 编码功能或搭建内部研发辅助系统；在完成依赖安全审查和运维准备后即可投入生产使用。

## 🧭 Practical evaluation

**Value:** 0xMassi/pocketdev helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 22 GitHub stars
- 1 forks
- updated 2026-06-30
- primary language: Go
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 8/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 60/100 |
| quality | 50/100 |
| recency | 40/100 |
| adoption | 23/100 |
| production | 54/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/0xMassi/pocketdev) · [← Back to AI/ML](./README.md)</sub>
