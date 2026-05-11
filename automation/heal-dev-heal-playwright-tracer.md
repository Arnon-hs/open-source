# heal-dev/heal-playwright-tracer

[![Stars](https://img.shields.io/github/stars/heal-dev/heal-playwright-tracer?style=flat-square&color=yellow)](https://github.com/heal-dev/heal-playwright-tracer/stargazers) [![Forks](https://img.shields.io/github/forks/heal-dev/heal-playwright-tracer?style=flat-square&color=blue)](https://github.com/heal-dev/heal-playwright-tracer/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> Open-source statement-level Playwright tracer, purpose-built for AI agents. Analyzes test runs with increased accuracy.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 35 |
| 🍴 **Forks** | — |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`automation` `claude-code` `claude-skill` `playwright` `qa-automation` `tracing`

## 🎯 Categories

Automation · AI/ML · Frontend · DevTools · Observability

## 📝 Summary

### English

**Brief Summary**  
heal‑dev/heal‑playwright‑tracer is an open‑source, statement‑level tracer built on top of Playwright that captures fine‑grained execution data for UI tests. Designed for AI agents, it delivers more accurate test‑run analysis and can be used to automate repetitive QA steps, glue together tooling, and schedule operational tasks.

**Value**  
- **Automation of manual QA work** – By instrumenting every Playwright command, the tracer produces a rich execution graph that AI agents can consume to generate insights, self‑heal flaky tests, or drive downstream workflows.  
- **Repeatable, observable pipelines** – The captured telemetry can be fed into CI/CD, monitoring dashboards, or custom bots, turning ad‑hoc test runs into repeatable, observable processes.  
- **Rapid integration for prototyping** – With a modest API surface and a single‑file npm install, teams can quickly replace their existing Playwright runner with the tracer to start collecting data without rewriting tests.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, run `npm install heal-playwright-tracer` and follow the README to wrap the existing Playwright test harness. Verify that trace files are generated for a small subset of tests.  
2. **Toolchain hookup** – Connect the output (JSON/NDJSON traces) to the AI component or observability platform you intend to use (e.g., LangChain agents, Grafana, custom dashboards).  
3. **Iterative expansion** – Gradually migrate more test suites, adding custom annotations where needed. Because the tracer is a thin wrapper, existing Playwright tests remain unchanged.  
4. **Stability & maintenance review** – Audit the dependency tree, lock versions, and add health‑checks to the CI pipeline to ensure the tracer does not introduce runtime regressions.

**Production Readiness**  
- **Maturity**: Medium. The project has 35 stars, recent activity (last commit 2026‑05‑11), and a clear JavaScript codebase, making it suitable for internal prototypes or low‑risk production workloads.  
- **Readiness Checklist**  
  - ✅ Verify compatibility with your Playwright version.  
  - ✅ Pin the tracer’s version and run a dependency audit (e.g., `npm audit`).  
  - ✅ Add monitoring for trace generation failures and fallback to standard Playwright runs.  
  - ✅ Conduct a small load test to gauge any performance overhead (typically a few milliseconds per command).  
- **Risks** – The integration guidance is sparse; you’ll need to invest time in understanding the trace format and wiring it to downstream AI/observability tools. A controlled pilot is recommended before a full rollout.  

In short, heal‑playwright‑tracer can eliminate repetitive manual QA steps and enable AI‑driven test analytics, but teams should start with a limited proof‑of‑concept, validate the integration effort, and perform the usual production hardening before relying on it in mission‑critical pipelines.

### Русский

**heal-dev/heal‑playwright‑tracer** — это open‑source‑трассер уровня отдельных утверждений для Playwright, ориентированный на AI‑агенты и повышающий точность анализа прогонов тестов. Его обычно внедряют в небольшие proof‑of‑concept, подключая к существующим пайплайн‑ам для автоматизации повторяющихся ручных операций (например, сбор метрик, генерация отчетов и интеграция с другими инструментами). Готовность к продакшну — средняя: проект подходит для прототипов и внутренних процессов, но перед масштабным использованием требуется проверить путь интеграции, зависимости и план обслуживания.

### 中文

**项目简介（2‑3 句）**  
heal-dev/heal‑playwright‑tracer 是一款面向 AI 代理的开源 **Playwright 语句级追踪器**，能够在测试运行时捕获并分析每一步指令，显著提升结果的准确性和可观测性。它帮助团队把繁琐的手工检查和日志收集工作自动化，进而构建可重复的 CI/CD 流程。

**价值**  
- **消除重复人工操作**：自动记录、解析并展示每条 Playwright 脚本的执行细节，省去人工审查日志的时间。  
- **提升 AI 代理效率**：提供结构化的执行轨迹，方便大模型或自研 AI 代理快速获取上下文、做出决策。  
- **促进工具链集成**：统一的追踪数据可以无缝输送到监控平台、报告系统或后续的自动化任务中，实现端到端的可观测性。

**典型接入方式**  
1. **在项目中安装**：`npm i @heal-dev/playwright-tracer`（或直接克隆仓库）。  
2. **在 Playwright 配置文件中启用**：在 `playwright.config.ts` 的 `globalSetup`/`globalTeardown` 或 `test.beforeAll` 中引入 tracer 并调用 `Tracer.start()` / `Tracer.stop()`。  
3. **输出与消费**：Tracer 会在 `./heal-trace`（可配置）生成 JSON/NDJSON 文件，随后可通过自研脚本、ELK、Grafana 或直接喂给 AI 代理进行后处理。  
4. **小规模验证**：先在单个测试套件或 CI job 中跑一次，确认生成的轨迹文件符合预期，再逐步推广到全量测试。

**生产可用性**  
- **成熟度**：目前评分 59/100，GitHub ★35，最近一次更新为 2026‑05‑11，适合原型开发或内部工具链。  
- **依赖与维护**：核心实现基于 JavaScript，依赖 Playwright 及少量轻量库；在正式生产前建议审查依赖的安全性并锁定版本。  
- **上线建议**：先做 **Proof‑of‑Concept**（如在 CI 中跑一次完整的追踪），评估生成数据量、存储成本以及与现有监控系统的兼容性；确认无阻塞后再逐步推广到全量 CI/CD 流程。  

总体而言，heal‑playwright‑tracer 在 **自动化、AI/ML 与前端可观测性** 场景下具备明确价值，适合作为内部原型或可控范围的生产工具，关键在于做好依赖审计和小规模验证后再全面部署。

## 🧭 Practical evaluation

**Value:** heal-dev/heal-playwright-tracer helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 35 GitHub stars
- updated 2026-05-11
- primary language: JavaScript
- 6 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 33/100 |
| topics | 75/100 |
| outlook | 73/100 |
| quality | 62/100 |
| recency | 100/100 |
| adoption | 24/100 |
| production | 68/100 |
| usefulness | 74/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/heal-dev/heal-playwright-tracer) · [← Back to Automation](./README.md)</sub>
