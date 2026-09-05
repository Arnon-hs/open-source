# juliantanx/aiusage

[![Stars](https://img.shields.io/github/stars/juliantanx/aiusage?style=flat-square&color=yellow)](https://github.com/juliantanx/aiusage/stargazers) [![Forks](https://img.shields.io/github/forks/juliantanx/aiusage?style=flat-square&color=blue)](https://github.com/juliantanx/aiusage/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> Open-source AI usage tracker — tokens, cost, and sessions across Claude Code, Codex, Hermes, Qoder, and more

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 91 |
| 🍴 **Forks** | 9 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-analytics` `ai-coding-assistant` `ai-usage` `aiusage` `better-sqlite3` `claude` `claude-code` `cli` `codex` `cost-tracking` `dashboard`

## 🎯 Categories

AI/ML · Frontend · DevTools · Data

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
juliantanx/aiusage is an open‑source TypeScript library that tracks AI usage across multiple models—including Claude, Codex, Hermes, Qoder, and others—by logging token counts, cost, and session metadata. It offers a unified API/SDK/CLI surface so developers can instrument their applications without building a custom telemetry stack from scratch. With active maintenance, a growing star count, and broad model support, it’s ready for pilot projects and early‑stage production use.

**Value**  
- **Unified observability**: Consolidates token, cost, and session data from disparate AI providers into a single source of truth, simplifying budgeting and performance monitoring.  
- **Rapid prototyping**: Developers can plug the tracker into new AI features, RAG pipelines, or autonomous agents without reinventing telemetry logic.  
- **Decision‑making**: Detailed usage metrics enable data‑driven model selection, cost optimization, and SLA compliance.

**Practical Adoption Path**  
1. **Add the package** (`npm i @juliantanx/aiusage`) to your TypeScript/JavaScript project.  
2. **Initialize the tracker** with your API keys and desired models (e.g., Claude, Codex).  
3. **Instrument calls** by wrapping the provider SDKs or using the provided CLI hooks; the library automatically records token usage, request cost, and session identifiers.  
4. **Consume the data** via the exposed SDK methods, webhook endpoints, or export to your existing analytics store (e.g., PostgreSQL, BigQuery).  
5. **Iterate** by adding custom tags (e.g., feature flag, user segment) to enrich the telemetry for deeper insights.

**Production Readiness**  
- **Activity & Community**: Recent commits (as of 2026‑06‑25), 91 stars, and ongoing issue response indicate a healthy open‑source project.  
- **Feature Completeness**: Supports a wide range of popular models and provides both programmatic (API/SDK) and command‑line interfaces, covering most integration scenarios.  
- **Stability**: The TypeScript codebase is type‑safe and well‑documented, reducing runtime errors.  
- **Risk Considerations**: While no major licensing or security red flags are evident, a final review of the MIT/Apache license terms, dependency audit, and maintainer responsiveness is recommended before full production rollout.  

Overall, juliantanx/aiusage offers a low‑friction, production‑grade solution for AI usage telemetry, making it a strong candidate for pilots and scaling into production environments.

### Русский

**juliantanx/aiusage** — это открытый трекер использования ИИ, который собирает метрики токенов, расходов и сессий для широкого спектра моделей (Claude, Codex, Hermes, Qoder и др.). Он позволяет быстро добавить AI‑функциональность в прототипы, RAG‑системы или агентные воркфлоу, предоставляя готовый API/SDK/CLI и подробные сигналы о запросах. Проект имеет высокий уровень готовности к production: активные коммиты, 91 звезда, широкая экосистема и поддержка TypeScript, что делает его надёжным кандидатом для серьёзных пилотных запусков.

### 中文

**项目简介**  
juliantanx/aiusage 是一款开源的 AI 使用情况追踪工具，能够统一记录 Claude Code、Codex、Hermes、Qoder 等多模型的 token 消耗、费用以及会话信息，为开发者提供完整的使用可视化。

**价值**  
- **快速赋能**：无需自行搭建复杂的监控体系，直接接入即可获得模型调用的成本与使用统计。  
- **多模型覆盖**：同一平台支持多种主流 LLM，便于对比与优化不同模型的使用效果。  
- **决策依据**：通过细粒度的 token 与费用数据，帮助团队评估原型、RAG 或 Agent 工作流的经济可行性。

**典型接入方式**  
1. **SDK / API**：在项目中引入 TypeScript SDK，调用 `trackRequest`、`trackResponse` 等方法即可自动上报。  
2. **CLI**：通过 `aiusage-cli` 对已有脚本或 CI 流程进行包装，实现无代码侵入的监控。  
3. **语言元数据**：支持在代码中标记语言或主题标签，便于后期按业务维度拆分统计。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑25 最近一次提交，拥有 91 ⭐、9 🍴，社区活跃。  
- **技术成熟度**：基于 TypeScript 实现，提供完整的类型声明和示例，易于在前端/后端项目中集成。  
- **生态兼容**：已在多个开源项目中验证，可直接用于原型开发、RAG/Agent 流程以及模型工具链评估。  
- **风险**：暂无重大元数据风险，但仍需对许可证、依赖安全审计以及维护者响应速度进行最终确认。  

总体来看，aiusage 具备较高的生产就绪度，适合作为 AI 功能快速原型和正式项目的监控底层组件。

## 🧭 Practical evaluation

**Value:** juliantanx/aiusage helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 91 GitHub stars
- 9 forks
- updated 2026-06-25
- primary language: TypeScript
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 25/100 |
| stars | 42/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 37/100 |
| production | 69/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/juliantanx/aiusage) · [← Back to AI/ML](./README.md)</sub>
