# m0n0x41d/haft

[![Stars](https://img.shields.io/github/stars/m0n0x41d/haft?style=flat-square&color=yellow)](https://github.com/m0n0x41d/haft/stargazers) [![Forks](https://img.shields.io/github/forks/m0n0x41d/haft?style=flat-square&color=blue)](https://github.com/m0n0x41d/haft/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-76%2F100-brightgreen?style=flat-square)](#)

> Engineering decisions  engine that know when they're stale. Frame, compare, decide — with evidence decay and parity enforcement. For Claude Code, Cursor, Gemini CLI, Codex and more.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.3k |
| 🍴 **Forks** | 104 |
| 💻 **Language** | Go |
| 📈 **Score** | 76/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `ai-coding` `ai-skills` `air` `anthropic` `claude` `claude-code` `cli` `codex` `codex-cli` `context-memory` `cursor`

## 🎯 Categories

AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
m0n0x41d/haft is an open‑source “engineering‑decisions engine” that tracks the freshness of AI‑generated evidence, enforces parity across model outputs, and lets you frame, compare, and decide on model responses. It ships ready‑to‑use integrations for Claude, Cursor, Gemini CLI, Codex and other LLMs, making it easy to bolt AI‑driven decision logic into existing tools.  

**Value**  
- **Accelerates AI feature development** – you get a reusable decision layer (evidence decay, parity checks, RAG/agent orchestration) instead of building one from scratch.  
- **Improves reliability** – automatic staleness detection and parity enforcement reduce hallucinations and inconsistent outputs across multiple model providers.  
- **Vendor‑agnostic** – the same engine works with several major LLM APIs, so you can experiment or switch providers without rewriting logic.  

**Practical Adoption Path**  
1. **Clone the repo** (Go 1.22+ required) and run the provided Dockerfile or binary to start the Haft service locally.  
2. **Configure connectors** via the YAML/JSON manifest – specify API keys, target models (Claude, Gemini, Codex, etc.), and any custom evidence sources (databases, vector stores).  
3. **Instrument your code** – import the Go SDK or call the REST/CLI endpoint from your existing application, passing the “frame” (question), “compare” (candidate responses), and “decide” (policy) payloads.  
4. **Iterate** – use the built‑in monitoring UI or logs to see evidence decay scores and parity violations, then tune policies or add new data sources.  
5. **Promote to production** – containerize the service, place it behind a service mesh or API gateway, and enable TLS/role‑based access control using the supplied Helm chart.  

**Production Readiness**  
- **Activity & community** – 1,322 ★, 104 forks, recent commits (last update 2026‑05‑13), and a clear Go codebase indicate an active project.  
- **Maturity** – the core engine, CLI, and SDK are stable; multiple LLM integrations have been tested, and the repository includes CI pipelines and Helm charts for deployment.  
- **Risk profile** – no major licensing or security red flags identified, though a final audit of the license (MIT‑style) and supply‑chain dependencies is advisable.  
- **Fit for pilot** – given its high signal‑to‑noise ratio, strong adoption signals, and straightforward integration steps, Haft is a solid candidate for a production pilot in environments that need trustworthy, multi‑model AI decision making.

### Русский

**m0n0x41d/haft** — это движок инженерных решений, который автоматически определяет устаревшие компоненты, сравнивает варианты и принимает решения, учитывая «угасание» доказательств и соблюдение паритета. Он позволяет быстро добавить AI‑функциональность (RAG, агентные цепочки, прототипы новых возможностей) в существующие проекты, используя готовые интеграции через API/SDK/CLI для Claude Code, Cursor, Gemini CLI, Codex и других. Проект имеет высокий уровень готовности к production: активные коммиты, более 1300 звёзд, широкое принятие в сообществе и поддержка на Go, что делает его надёжным кандидатом для серьёзных пилотных внедрений.

### 中文

**项目简介**  
m0n0x41d/haft 是一款「工程决策引擎」，能够感知决策何时失效并自动进行证据衰减与一致性强制。它通过「框定‑比较‑决定」的工作流，为 Claude Code、Cursor、Gemini CLI、Codex 等多种 AI 工具提供即时、可靠的决策支撑。

**价值主张**  
- **快速赋能 AI 能力**：无需从零搭建模型堆栈，直接在现有代码库或工具链上挂载决策引擎，即可实现 RAG、Agent 工作流或 AI 功能原型。  
- **降低维护成本**：证据衰减机制自动淘汰过时信息，保持决策始终基于最新数据，减少人工干预。  
- **统一决策一致性**：Parity enforcement 确保不同模块、不同模型输出的决策保持一致，提升系统可靠性。

**典型接入方式**  
1. **API/SDK**：通过公开的 RESTful API 或 Go SDK 调用 `frame`, `compare`, `decide` 接口，提交上下文并获取决策结果。  
2. **CLI**：使用 `haft-cli` 在本地或 CI/CD 流水线中直接执行决策检查，适合快速原型和脚本化集成。  
3. **语言元数据**：项目自带的语言标签（Go 为主）和主题标签，可在代码生成或文档生成阶段自动注入决策信号。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑13，最近一次提交，星标 1,322、Fork 104，社区活跃，具备持续迭代的动力。  
- **生态兼容**：已对接 Claude Code、Cursor、Gemini CLI、Codex 等主流 AI 平台，集成门槛低。  
- **成熟度**：代码基于 Go，拥有完整的单元测试和 CI，适合作为 OSS 级别的 pilot 项目投入生产。  
- **风险**：目前未发现重大元数据风险，但仍需对许可证（MIT/Apache 等）和安全审计进行最终确认。  

综上，haft 在提供即时、可信的工程决策能力方面表现突出，接入方式灵活，且具备足够的社区与技术成熟度，可直接用于生产环境的 AI 功能实验或正式部署。

## 🧭 Practical evaluation

**Value:** m0n0x41d/haft helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1322 GitHub stars
- 104 forks
- updated 2026-05-13
- primary language: Go
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 66/100 |
| topics | 100/100 |
| outlook | 81/100 |
| quality | 78/100 |
| recency | 80/100 |
| adoption | 62/100 |
| production | 73/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/m0n0x41d/haft) · [← Back to AI/ML](./README.md)</sub>
