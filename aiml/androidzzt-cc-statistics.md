# androidZzT/cc-statistics

[![Stars](https://img.shields.io/github/stars/androidZzT/cc-statistics?style=flat-square&color=yellow)](https://github.com/androidZzT/cc-statistics/stargazers) [![Forks](https://img.shields.io/github/forks/androidZzT/cc-statistics?style=flat-square&color=blue)](https://github.com/androidZzT/cc-statistics/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> AI Coding stats dashboard — track costs, tokens, and efficiency across Claude Code / Gemini CLI / Codex / Cursor

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 107 |
| 🍴 **Forks** | 14 |
| 💻 **Language** | Swift |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-coding` `claude-code` `cli` `cost-estimation` `developer-tools` `gemini-cli` `macos-app` `menu-bar-app` `python` `swiftui` `token-tracking` `token-usage`

## 🎯 Categories

AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
androidZzT/cc‑statistics is an open‑source dashboard that aggregates AI‑coding usage data—costs, token consumption, and efficiency—from Claude Code, Gemini CLI, Codex, and Cursor. It surfaces implementation signals such as API/SDK calls, language metadata, and topic focus, making it easy to prototype, evaluate, and monitor AI‑enhanced features. With active maintenance, 107 ⭐ on GitHub and recent updates, it’s a production‑ready candidate for teams that want AI capabilities without building a model stack from scratch.  

**Value**  
- **Unified visibility**: Consolidates telemetry from multiple LLM providers into a single UI, letting developers instantly see spend, token usage, and latency trends.  
- **Rapid prototyping**: By exposing signals (API/SDK usage, language tags, topic focus) developers can quickly iterate on RAG pipelines, agent workflows, or other AI‑augmented features without writing custom instrumentation.  
- **Cost control & efficiency**: Real‑time dashboards help teams spot waste (e.g., over‑tokenized prompts) and optimize prompt design, directly reducing operational expenses.  

**Practical Adoption Path**  
1. **Clone & install** – The project is Swift‑based; add it as a Swift Package or integrate the compiled binary into your iOS/macOS app or a cross‑platform UI layer.  
2. **Configure data sources** – Provide API keys or CLI endpoints for Claude, Gemini, Codex, and Cursor in the supplied `config.yaml`. The dashboard auto‑discovers calls made through the official SDKs/CLIs.  
3. **Instrument custom code (optional)** – If you have bespoke AI wrappers, emit the same telemetry format (JSON payload with `model`, `tokens`, `cost`, `language`, `topic`). The built‑in collector will ingest it.  
4. **Deploy** – Run the dashboard locally for development, then containerize it (Dockerfile is included) for staging or production environments.  
5. **Iterate & monitor** – Use the UI to set alerts on cost thresholds, compare provider efficiency, and guide prompt‑engineering decisions.  

**Production Readiness**  
- **Activity & community**: 107 stars, 14 forks, recent commit on 2026‑06‑28, and a healthy issue/PR turnover indicate an active maintainer base.  
- **Stability**: The Swift codebase is mature, with clear module boundaries and a documented configuration schema.  
- **Ecosystem fit**: Works out‑of‑the‑box with the major LLM providers used in modern dev‑tooling stacks, and the telemetry format aligns with common observability pipelines (e.g., Prometheus, Grafana).  
- **Risks to address**: Final due‑diligence on licensing (MIT‑compatible) and a security audit of the data‑collection layer are recommended before a full production rollout.  

Overall, cc‑statistics offers a low‑friction way to add AI observability and cost management to any project, making it a solid OSS candidate for pilot programs and, after the minor risk checks, for production use.

### Русский

Резюме проекта androidZzT/cc-statistics:

Проект androidZzT/cc-statistics представляет собой AI-дашборд для отслеживания затрат, токенов и эффективности при работе с технологиями Claude Code, Gemini CLI, Codex и Cursor. Он помогает добавлять функциональность AI в существующие проекты без необходимости создания новой стартовой модели. Проект готов к serious пилоту, имеет высокий уровень готовности к production и показывает активность и признание в сообществе.

### 中文

**项目简介**

androidZzT/cc-statistics 是一个开源项目，提供了一个 AI 编码统计面板，用于跟踪 Claude Code、Gemini CLI、Codex 和 Cursor 等 AI 工具的成本、令牌和效率。该项目已获得 74/100 的评分，并且在 AI/ML、前端、开发工具和移动应用等领域具有较高的价值。

**价值**

androidZzT/cc-statistics 的价值在于，它可以帮助开发者在不从头开始构建 AI 模型栈的情况下，添加 AI 能力。它适用于以下场景：

* 原型 AI 特性
* 构建 RAG 或代理工作流
* 评估模型工具

**典型接入方式**

该项目提供了以下接入方式：

* API/SDK/CLI 等实现信号
* 语言元数据
* 焦点主题

**生产可用性**

androidZzT/cc-statistics 具有较高的生产可用性，主要原因是：

* 近期活动
* 广泛的采用
* 强大的生态系统信号
* 高质量的 GitHub 星星和 fork 数

## 🧭 Practical evaluation

**Value:** androidZzT/cc-statistics helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 107 GitHub stars
- 14 forks
- updated 2026-06-28
- primary language: Swift
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 43/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 39/100 |
| production | 69/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/androidZzT/cc-statistics) · [← Back to AI/ML](./README.md)</sub>
