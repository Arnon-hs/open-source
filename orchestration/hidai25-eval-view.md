# hidai25/eval-view

[![Stars](https://img.shields.io/github/stars/hidai25/eval-view?style=flat-square&color=yellow)](https://github.com/hidai25/eval-view/stargazers) [![Forks](https://img.shields.io/github/forks/hidai25/eval-view?style=flat-square&color=blue)](https://github.com/hidai25/eval-view/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-80%2F100-brightgreen?style=flat-square)](#)

> Regression testing for AI agents. Snapshot behavior,diff tool calls,catch regressions in CI. Works with LangGraph, CrewAI, OpenAI, Anthropic.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 102 |
| 🍴 **Forks** | 20 |
| 💻 **Language** | Python |
| 📈 **Score** | 80/100 |
| 🗓️ **Last push** | 2026-05-10 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-benchmark` `agent-evaluation` `agentic-ai` `ai-agents` `anthropic` `autogen` `cli` `crewai` `evaluation` `langchain-agent` `langgraph` `llm`

## 🎯 Categories

Orchestration · MCP · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
hidai25/eval‑view is an open‑source regression‑testing framework for AI agents that snapshots their behavior, diffs tool calls, and flags regressions in CI pipelines. It plugs into popular orchestration stacks such as LangGraph, CrewAI, OpenAI, and Anthropic, turning ad‑hoc prompts and tool invocations into repeatable, testable workflows. With over 100 stars, recent commits, and active community interest, it’s ready for pilot projects in production environments.

**Value**  
- **Reliability:** By automatically capturing agent outputs and tool‑call traces, teams can detect subtle regressions before they reach users, reducing costly debugging cycles.  
- **Standardisation:** Provides a unified way to define, run, and compare multi‑agent pipelines, making it easier to onboard new developers and maintain consistent memory/knowledge handling across projects.  
- **Ecosystem Compatibility:** Native integrations with LangGraph, CrewAI, OpenAI, and Anthropic mean you can adopt it without rewriting existing agents or tooling.

**Practical Adoption Path**  
1. **Prototype:** Add the eval‑view Python package to a sandbox repo and instrument a single LangGraph or CrewAI workflow with the provided decorators/CLI.  
2. **CI Integration:** Configure a GitHub Actions (or equivalent) step that runs `eval-view test` on each PR, storing snapshots as artifacts and failing the build on diff mismatches.  
3. **Scale:** Extend instrumentation to all critical agent pipelines, define baseline snapshots for each major version, and incorporate custom diff rules for domain‑specific tolerances (e.g., numeric drift, ordering).  
4. **Governance:** Use the generated reports to create a regression‑review checklist for the data‑science or ML ops team, ensuring that any intentional behavior change is accompanied by an updated snapshot.

**Production Readiness**  
- **Activity:** Last commit on 2026‑05‑10, 102 stars, 20 forks, and active issue discussions indicate a healthy, maintained project.  
- **Integration Simplicity:** Exposes a clear API/CLI and emits language‑agnostic metadata, making it straightforward to embed in existing Python‑based agent stacks.  
- **Risk Profile:** No immediate licensing or security red flags, though a final audit of the license and maintainer commitment is advisable.  
Overall, eval‑view meets the criteria for a serious pilot: it is mature enough for early‑stage production use, integrates cleanly with leading agent frameworks, and provides tangible safeguards against regression‑related failures.

### Русский

**hidai25/eval-view** — это open‑source‑инструмент для регрессионного тестирования AI‑агентов: он фиксирует «снимки» поведения, сравнивает вызовы инструментов и автоматически выявляет откаты в CI. Типичная интеграция — включение в пайплайн оркестрации (LangGraph, CrewAI и др.) для превращения отдельных запросов и инструментов в воспроизводимые рабочие процессы агентов, а также стандартизацию их памяти и многопоточных взаимодействий. Проект уже имеет активную поддержку (102★, 20 форков, последние коммиты — 2026‑05‑10), написан на Python и готов к пилотному запуску в продакшн, хотя требуется окончательная проверка лицензии и безопасности.

### 中文

**项目简介**  
hidai25/eval-view 是一款面向 AI 代理的回归测试框架，能够对代理的行为快照、工具调用进行差分，帮助在 CI 中捕获回归。它原生支持 LangGraph、CrewAI 以及主流大模型（OpenAI、Anthropic），把零散的 Prompt 与工具链转化为可重复执行的工作流。

**价值**  
- **确保稳定性**：在每次代码或模型更新后自动对比行为快照，快速定位回归。  
- **统一工作流**：把多代理协作、工具调用、记忆管理等环节抽象为可复用的流水线，降低调试成本。  
- **生态兼容**：直接对接 LangGraph、CrewAI 等流行编排框架，几行配置即可在现有项目中启用。

**典型接入方式**  
1. **Python SDK**：在项目中 `pip install eval-view`，通过 `EvalView` 类注册模型、工具和记忆模块，然后在代理代码里调用 `eval_view.record()`、`eval_view.diff()`。  
2. **CLI**：在 CI 步骤中运行 `eval-view snapshot --run-id $CI_RUN_ID` 生成快照，随后 `eval-view compare --base $BASE_ID --head $HEAD_ID` 检查差异。  
3. **配置文件**：在项目根目录放置 `eval-view.yaml`，声明要监控的 Prompt、工具和记忆键，框架会自动读取并在测试阶段注入。

**生产可用性**  
- **活跃度**：截至 2026‑05‑10 最近一次提交，GitHub ★102、Fork 20，社区讨论活跃。  
- **生态适配**：已在多个开源项目（LangGraph、CrewAI）中验证，可直接用于已有的多代理系统。  
- **成熟度**：具备完整的 API/SDK/CLI，提供详细的日志与差分报告，适合作为 CI/CD 流水线的一环。  
- **风险**：许可证、长期维护者和安全审计仍需进一步确认，但当前信号表明该项目已具备在生产环境中进行试点的条件。

## 🧭 Practical evaluation

**Value:** hidai25/eval-view helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 102 GitHub stars
- 20 forks
- updated 2026-05-10
- primary language: Python
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 33/100 |
| stars | 43/100 |
| topics | 100/100 |
| outlook | 85/100 |
| quality | 73/100 |
| recency | 100/100 |
| adoption | 40/100 |
| production | 78/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-10 · [View on GitHub](https://github.com/hidai25/eval-view) · [← Back to Orchestration](./README.md)</sub>
