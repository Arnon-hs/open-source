# Piebald-AI/splitrail

[![Stars](https://img.shields.io/github/stars/Piebald-AI/splitrail?style=flat-square&color=yellow)](https://github.com/Piebald-AI/splitrail/stargazers) [![Forks](https://img.shields.io/github/forks/Piebald-AI/splitrail?style=flat-square&color=blue)](https://github.com/Piebald-AI/splitrail/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> Fast, cross-platform, real-time token usage tracker and cost monitor for Gemini CLI / Claude Code / Codex CLI / Qwen Code / Cline / Roo Code / Kilo Code / GitHub Copilot / OpenCode / Pi Agent / Piebald.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 208 |
| 🍴 **Forks** | 18 |
| 💻 **Language** | Rust |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic` `analyzer` `blazing-fast` `ccusage` `claude-code` `cline` `codex` `gcusage` `gemini-cli` `kilo-code` `opencode` `pi-agent`

## 🎯 Categories

AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
SplitRail (Piebald‑AI/splitrail) is a fast, cross‑platform Rust library that monitors token usage and cost in real‑time for a wide range of LLM interfaces (Gemini CLI, Claude Code, Codex CLI, Qwen Code, Cline, Roo Code, Kilo Code, GitHub Copilot, OpenCode, Pi Agent, etc.). It surfaces implementation signals—such as API/SDK calls, language metadata, and topic focus—so developers can prototype AI features, build RAG or agent workflows, and evaluate model tooling without building a monitoring stack from scratch.  

**Value**  
- **Immediate observability**: By tracking token consumption and associated costs across many popular LLM front‑ends, teams gain instant insight into budget impact and usage patterns, preventing surprise overruns.  
- **Unified interface**: A single Rust crate abstracts away the quirks of each vendor’s CLI/SDK, letting developers add usage accounting to any existing AI‑enabled tool with minimal code changes.  
- **Accelerated prototyping**: Because the library is lightweight and cross‑platform, it can be dropped into experimental projects to quickly validate RAG pipelines, agent loops, or custom prompting strategies while keeping cost visibility.  

**Practical Adoption Path**  
1. **Evaluate** – Clone the repo, run the provided examples, and point the library at the target LLM CLI/SDK (e.g., `gemini`, `claude`, `copilot`).  
2. **Integrate** – Add the `splitrail` crate to your Cargo.toml (or use the pre‑built binary for non‑Rust projects) and wrap your existing LLM calls with the provided `track` helpers.  
3. **Configure** – Supply API keys and optional cost‑rate tables via environment variables or a simple TOML config; the library will emit usage metrics to stdout, a file, or a Prometheus endpoint.  
4. **Iterate** – Use the real‑time metrics to tune prompts, batch sizes, or model selections, and optionally feed the data into internal dashboards or alerting systems.  

**Production Readiness**  
- **Maturity**: Medium. The project has 208 stars, recent activity (last commit 2026‑06‑27), and is written in Rust, which offers strong performance and safety guarantees.  
- **Stability**: Suitable for prototypes, internal tooling, and low‑to‑moderate traffic services. Before full production deployment, verify the licensing terms, perform a security audit of the dependency chain, and establish a process for handling upstream updates.  
- **Operational considerations**: Ensure you have a reliable way to store or forward the emitted metrics (e.g., Prometheus, CloudWatch) and monitor the library’s own resource usage, especially if used in high‑throughput environments.  

In short, SplitRail provides a quick, language‑agnostic way to gain cost transparency across many LLM providers, making it a practical addition for teams building AI prototypes and a viable, though not yet battle‑tested, component for production systems after the usual due‑diligence steps.

### Русский

**Piebald‑AI/splitrail** — это быстрый кросс‑платформенный монитор реального времени, который отслеживает количество использованных токенов и стоимость запросов к Gemini CLI, Claude Code, Codex CLI, Qwen Code, Cline, Roo Code, Kilo Code, GitHub Copilot, OpenCode, Pi Agent и другим AI‑инструментам. Он удобен для прототипирования AI‑фич, построения RAG‑ или агентных воркфлоу и оценки разных моделей, поскольку сразу предоставляет сигналы о вызовах API/SDK, метаданные языка и тематические детали. Проект находится на среднем уровне готовности к продакшну: подходит для внутренних прототипов и небольших сервисов, но перед выпуском в продакшн требуется проверка лицензии, безопасности и поддерживаемости.

### 中文

**简短介绍**

Piebald-AI/splitrail 是一个快速、跨平台的实时令牌使用跟踪器和成本监控器，支持多种 AI CLI 工具，包括 Gemini CLI、Claude Code 等。它可以帮助开发者轻松添加 AI 能力。

**价值**

Piebald-AI/splitrail 的价值在于，它可以帮助开发者快速添加 AI 能力，减少从零开始的工作量。它适合用于原型开发、RAG 或代理工作流的构建，以及模型工具的评估。

**典型接入方式**

Piebald-AI/splitrail 支持多种接入方式，包括：

* API/SDK：通过 API 或 SDK 接入
* CLI：通过命令行接口接入
* 语言元数据：通过语言元数据接入
* 焦点主题：通过特定主题接入

**生产可用性**

Piebald-AI/splitrail 的生产可用性为中等。它适合用于原型开发或内部工作流，需要在生产环境中进行依赖性和维护性检查后才能使用。

## 🧭 Practical evaluation

**Value:** Piebald-AI/splitrail helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 208 GitHub stars
- 18 forks
- updated 2026-06-27
- primary language: Rust
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 32/100 |
| stars | 49/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 70/100 |
| recency | 80/100 |
| adoption | 45/100 |
| production | 68/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/Piebald-AI/splitrail) · [← Back to AI/ML](./README.md)</sub>
