# delta-hq/cc-ledger

[![Stars](https://img.shields.io/github/stars/delta-hq/cc-ledger?style=flat-square&color=yellow)](https://github.com/delta-hq/cc-ledger/stargazers) [![Forks](https://img.shields.io/github/forks/delta-hq/cc-ledger?style=flat-square&color=blue)](https://github.com/delta-hq/cc-ledger/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-41%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 41/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
CC‑Ledger is an open‑source utility that logs the token usage and associated cost of Claude (Anthropic) calls on a per‑session and per‑pull‑request basis. It is designed to give developers visibility into how much AI‑assisted code generation is costing their projects, helping them budget and optimize usage.

**Value**  
- **Cost transparency:** By automatically recording token counts and monetary cost for each Claude interaction, teams can track spend in real time and identify expensive patterns (e.g., overly large prompts or redundant calls).  
- **Developer workflow integration:** The per‑PR reporting ties AI usage directly to code changes, making it easy to attribute cost to specific features or bug fixes. This encourages responsible AI usage and supports budgeting or charge‑back models.  
- **Lightweight & language‑agnostic:** The tool is a small CLI/library that can be dropped into existing CI pipelines or local development scripts without requiring a full‑stack rewrite.

**Practical Adoption Path**  
1. **Review repository health:** Clone the project, check the license (ensure it’s compatible), read the README, and verify that recent commits and issue activity indicate active maintenance.  
2. **Prototype locally:** Add the CC‑Ledger package to a sandbox repo, configure your Anthropic API key, and run a few Claude calls to confirm that session and PR logs are generated as expected.  
3. **Integrate into CI:** Add a step in your CI workflow (GitHub Actions, GitLab CI, etc.) that invokes the ledger after each Claude‑driven code generation step, publishing the cost report as an artifact or comment on the PR.  
4. **Validate reporting:** Review the generated logs, adjust any configuration (e.g., token‑price mapping, filtering of internal calls), and ensure the data is stored securely (avoid leaking API keys or cost data).  
5. **Roll out to the team:** Once the prototype is stable, document the usage pattern, add it to your onboarding checklist, and optionally build dashboards or alerts for cost thresholds.

**Production Readiness**  
- **Maturity:** Medium. The project appears maintained (last update 2026‑05‑12) but has limited metadata (few topics, sparse integration signals). It is suitable for prototypes, internal tooling, or cost‑tracking pilots.  
- **Risks:** Potential gaps in documentation, limited community support, and unknown release cadence. Before production use, perform a dependency audit, confirm the licensing terms, and set up monitoring for breaking changes.  
- **Recommendation:** Deploy in a controlled environment first; if the tool proves reliable and the maintainers respond to issues, it can be promoted to a production‑grade component of your CI/CD pipeline.

### Русский

**CC‑Ledger** — это open‑source‑утилита, позволяющая отслеживать затраты токенов Claude в рамках отдельной сессии разработки и каждого Pull Request’а, что упрощает оценку стоимости генеративного кода и планирование бюджета. Типичный сценарий: команда интегрирует скрипт в CI/CD (например, в GitHub Actions), где после каждого PR автоматически собираются метрики расходов и сохраняются в журнале, позволяя быстро сравнивать эффективность разных подходов. Готовность к production — средняя: проект подходит для прототипов и внутренних процессов, но требует проверки лицензии, актуальности зависимостей и наличия поддержки перед масштабным внедрением.

### 中文

**项目简介**  
CC‑Ledger 是一个用于跟踪 Claude（Anthropic）代码生成费用的工具，能够按会话（Session）和 Pull Request（PR）分别记录并统计消耗的 token 与费用。它适合在代码审查或 CI 流程中实时监控 LLM 使用成本。

**价值**  
- **成本可视化**：帮助团队了解每次代码生成或每个 PR 消耗的 Claude 费用，避免意外超支。  
- **预算控制**：配合内部费用分摊或上限警报，实现对 LLM 预算的细粒度管理。  
- **决策依据**：通过历史成本数据，评估不同提示（prompt）或模型版本的性价比，指导后续使用策略。

**典型接入方式**  
1. **CI/CD 集成**：在 GitHub Actions、GitLab CI 或 Jenkins 等流水线中添加一个步骤，调用 CC‑Ledger 的 CLI 或 API，将当前 PR 的代码变更提交给 Claude，并记录返回的 token 用量。  
2. **本地开发插件**：在 IDE（如 VS Code）中安装对应插件或使用预提交钩子（pre‑commit hook），在每次本地提交前自动发送代码片段至 Claude 并写入本地 ledger。  
3. **Webhook 方式**：在仓库设置 webhook，监听 PR 打开/更新事件，后端服务调用 Claude 并把费用信息写入 CC‑Ledger 的持久化存储（如 SQLite、PostgreSQL），再通过仪表盘或 Slack 通知展示。

**生产可用性**  
- **成熟度**：当前评分 41/100，属于 **中等** 级别。代码最近更新于 2026‑05‑12，文档与示例较少，集成信号稀疏。  
- **适用场景**：适合原型、内部工具或成本实验项目；在正式生产环境使用前建议进行以下检查：  
  - **许可证**：确认符合企业合规（MIT、Apache 等）。  
  - **依赖安全**：审计第三方库的安全性和维护状态。  
  - **文档完整度**：补全安装、配置、API 调用示例。  
  - **发布节奏**：观察项目的 issue 响应和版本迭代频率，确保后续能得到维护。  
- **风险**：质量信号有限，可能出现未捕获的错误或缺乏官方支持。建议在内部环境进行充分测试后，再决定是否推广到生产环境。

## 🧭 Practical evaluation

**Value:** CC-Ledger: Claude Code Cost Tracker (Per-Session and Per-PR) may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-05-12
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 54/100 |
| quality | 41/100 |
| recency | 100/100 |
| adoption | 0/100 |
| production | 58/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/delta-hq/cc-ledger) · [← Back to Misc](./README.md)</sub>
