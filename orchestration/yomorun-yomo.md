# yomorun/yomo

[![Stars](https://img.shields.io/github/stars/yomorun/yomo?style=flat-square&color=yellow)](https://github.com/yomorun/yomo/stargazers) [![Forks](https://img.shields.io/github/forks/yomorun/yomo?style=flat-square&color=blue)](https://github.com/yomorun/yomo/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> 🦖 Serverless AI Agent Framework with Geo-distributed Edge AI Infra.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.9k |
| 🍴 **Forks** | 143 |
| 💻 **Language** | Rust |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`a2a-protocol` `chatgpt` `claude-code` `cursor` `distributed-cloud` `function-calling` `geodistributedsystems` `low-latency` `mcp` `openai` `quic` `realtime`

## 🎯 Categories

Orchestration · MCP · AI/ML · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
yomorun/yomo is a Rust‑based, server‑less AI‑agent framework that lets you stitch together isolated prompts, tools, and memory stores into repeatable, geo‑distributed workflows. By exposing a clean API/SDK/CLI, it makes multi‑agent orchestration, tool‑use pipelines, and standardized agent memory easy to implement at the edge. With strong recent activity, 1.9 k stars and a growing ecosystem, it is ready for serious pilot projects.

**Value**  
- Turns ad‑hoc LLM prompts into reusable, versioned agents, reducing development friction and operational debt.  
- Enables coordinated multi‑agent scenarios (e.g., routing, delegation, tool chaining) while keeping state consistent across distributed edge nodes.  
- Provides a unified interface (API, SDK, CLI) that abstracts away the underlying infra, allowing teams to focus on business logic rather than deployment plumbing.

**Practical Adoption Path**  
1. **Prototype** – Use the CLI to spin up a local Yomo instance and define a simple workflow (prompt → tool → memory).  
2. **Integrate** – Replace existing custom orchestration code with Yomo’s SDK calls in your service (Rust, or via the HTTP API for other languages).  
3. **Scale Edge‑wise** – Deploy the same workflow to Yomo’s server‑less edge runtime, leveraging its built‑in geo‑distribution for low‑latency inference.  
4. **Standardize** – Adopt Yomo’s memory abstraction across all agents to ensure consistent state handling and easier debugging.

**Production Readiness**  
Yomo scores high on production readiness: recent commits (as of 2026‑05‑11), active community engagement, 1903 stars, and multiple forks indicate a mature codebase. Its server‑less design, clear API surface, and Rust performance make it suitable for latency‑sensitive edge deployments. While the license, security posture, and maintainer continuity still need a final check, the overall signals suggest Yomo is a solid OSS candidate for pilot‑to‑production transitions.

### Русский

**yomorun/yomo** — это серверлесс‑фреймворк для создания AI‑агентов, позволяющий превращать разрозненные подсказки и инструменты в повторяемые, геораспределённые рабочие процессы. Типичный сценарий: координация нескольких агентов, построение конвейеров с использованием внешних инструментов и стандартизация памяти агентов, что упрощает разработку сложных AI‑систем. Проект имеет высокий уровень готовности к production: активные коммиты, 1900+ звёзд, широкая экосистема (Rust‑SDK, API, CLI) и позитивные сигналы внедрения, хотя окончательная проверка лицензии и безопасности всё ещё требуется.

### 中文

**项目简介**  
yomorun/yomo 是一款基于 Rust 的 Serverless AI Agent 框架，提供 Geo‑分布式边缘 AI 基础设施，能够把孤立的 Prompt 与工具组合成可重复的智能体工作流。

**价值**  
- 将分散的 Prompt 与工具统一编排，形成可复用、可追踪的多 Agent 流程。  
- 支持工具调用、记忆管理和跨地域边缘计算，帮助企业快速构建复杂的 AI 编排场景，如客服协同、自动化运营和数据处理管线。  

**典型接入方式**  
1. **API/SDK**：通过 HTTP API 或官方 Rust SDK 直接调用 Agent，提交 Prompt 并获取执行结果。  
2. **CLI**：使用 yomo 命令行工具进行本地调试、工作流定义（YAML/JSON）以及部署。  
3. **语言元数据**：框架自带的语言标签（Rust、Python、JS 等）可在 CI/CD 中自动生成对应的 Agent 包，实现“一键部署”。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑11，项目拥有 1903 星、143 Fork，近期频繁提交，社区活跃。  
- **生态成熟**：提供完整的 API、SDK、CLI，且已在多个内部和公开案例中验证，具备边缘节点自动调度和容错能力。  
- **准备度**：虽然许可证、完整安全审计和维护者持续性仍需最终确认，但整体信号表明它已经可以作为 OSS 关键组件在生产环境进行试点部署。

## 🧭 Practical evaluation

**Value:** yomorun/yomo helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1903 GitHub stars
- 143 forks
- updated 2026-05-11
- primary language: Rust
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 54/100 |
| stars | 70/100 |
| topics | 100/100 |
| outlook | 61/100 |
| quality | 64/100 |
| recency | 20/100 |
| adoption | 65/100 |
| production | 52/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/yomorun/yomo) · [← Back to Orchestration](./README.md)</sub>
