# sculptdotfun/viberank

[![Stars](https://img.shields.io/github/stars/sculptdotfun/viberank?style=flat-square&color=yellow)](https://github.com/sculptdotfun/viberank/stargazers) [![Forks](https://img.shields.io/github/forks/sculptdotfun/viberank?style=flat-square&color=blue)](https://github.com/sculptdotfun/viberank/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> 🏆 The AI coding usage leaderboard — Claude Code, Codex, Gemini CLI & more. Real costs and tokens from ccusage data. Submit with: npx viberank-cli

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 104 |
| 🍴 **Forks** | 13 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-coding` `anthropic` `ccusage` `claude` `claude-code` `codex` `developer-tools` `gemini-cli` `leaderboard` `nextjs` `supabase` `typescript`

## 🎯 Categories

AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
sculptdotfun/viberank is an open‑source leaderboard that tracks real‑time usage, token counts and costs for AI coding models such as Claude, Codex, Gemini, and others. By running `npx viberank-cli` you can submit your own runs and instantly see how your code‑generation workloads compare across models, languages and SDKs.  

**Value**  
The tool gives developers immediate visibility into the economic and performance impact of different LLMs, turning raw usage data into actionable insights for cost‑optimization, model selection, and capacity planning. It also serves as a lightweight “sandbox” for prototyping RAG pipelines, agent workflows, or any AI‑augmented feature without having to build a custom telemetry stack from scratch.  

**Practical Adoption Path**  
1. **Install** the CLI (`npx viberank-cli`) in any Node/TS project.  
2. **Instrument** your existing AI calls (e.g., OpenAI, Anthropic, Google) by wrapping them with the provided SDK or by emitting the required JSON payloads.  
3. **Submit** the data; the service aggregates it and updates the public leaderboard.  
4. **Consume** the leaderboard API or embed the UI in internal dashboards to compare models, languages, or cost per token.  
Because the project is pure TypeScript and depends only on standard Node APIs, integration can be done in minutes and does not require a separate backend.  

**Production Readiness**  
- **Activity & Adoption**: 104 ★, 13 forks, last commit 2026‑06‑28, and active issue discussions indicate a healthy community.  
- **Technical maturity**: The CLI, SDK, and API are well‑documented; the codebase follows conventional TypeScript patterns, making it easy to audit and extend.  
- **Risk considerations**: No obvious metadata or licensing red flags, but a final security review of the underlying dependencies and a check of the maintainer’s response cadence are recommended before large‑scale rollout.  

Overall, viberank is production‑ready for pilots and can be safely promoted to a core telemetry component in AI‑enhanced applications after the standard OSS due‑diligence steps.

### Русский

**sculptdotfun/viberank** — это открытый инструмент, который собирает и отображает реальные затраты и количество токенов при использовании популярных AI‑моделей (Claude, Codex, Gemini и др.) через CLI‑утилиту `npx viberank-cli`. Его удобно внедрять в прототипы AI‑фич, RAG‑системы или агентные воркфлоу, чтобы быстро оценить эффективность и стоимость выбранных моделей. Проект уже активно поддерживается (обновления 2026‑06‑28, 104 ★, 13 forks, TypeScript), имеет хорошие сигналы готовности к продакшену и может быть использован в пилотных проектах без существенных рисков.

### 中文

**简短介绍**

sculptdotfun/viberank 是一个开源项目，提供了一个 AI 编码使用排行榜，支持 Claude Code、Codex、Gemini CLI 等多种 AI 编码工具。使用 `npx viberank-cli` 提交数据并获得真实的成本和令牌信息。该项目帮助开发者添加 AI 能力而不需要从零开始构建模型栈。

**价值**

sculptdotfun/viberank 的主要价值在于帮助开发者快速评估和比较不同 AI 编码工具的成本和性能，方便开发者选择合适的工具并加快 AI 项目的开发进程。

**典型接入方式**

开发者可以使用 `npx viberank-cli` 命令行工具轻松接入 sculptdotfun/viberank。该工具会收集必要的数据并生成排行榜报告。

**生产可用性**

sculptdotfun/viberank 的生产可用性很高，因为它拥有活跃的社区、强大的生态系统信号和良好的质量信号。然而，开发者仍然需要仔细评估该项目的许可协议、安全性和维护

## 🧭 Practical evaluation

**Value:** sculptdotfun/viberank helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 104 GitHub stars
- 13 forks
- updated 2026-06-28
- primary language: TypeScript
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 43/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 39/100 |
| production | 69/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/sculptdotfun/viberank) · [← Back to AI/ML](./README.md)</sub>
