# EveryInc/hands-on-deck

[![Stars](https://img.shields.io/github/stars/EveryInc/hands-on-deck?style=flat-square&color=yellow)](https://github.com/EveryInc/hands-on-deck/stargazers) [![Forks](https://img.shields.io/github/forks/EveryInc/hands-on-deck?style=flat-square&color=blue)](https://github.com/EveryInc/hands-on-deck/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> Agent-native PowerPoint manipulation — one CLI lets AI agents inspect, edit, create, and verify .pptx files through atomic JSON patches. Packaged as an Agent Skill.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 114 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | Python |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-skills` `ai-agents` `claude` `powerpoint` `pptx` `python`

## 🎯 Categories

Orchestration · AI/ML

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
EveryInc’s *hands‑on‑deck* is a Python‑based Agent Skill that lets AI agents work with PowerPoint files via a single CLI. It exposes atomic JSON‑patch operations for inspecting, editing, creating, and verifying *.pptx* documents, turning ad‑hoc prompt‑driven manipulations into repeatable, scriptable workflows.

**Value**  
- **Agent‑native tooling**: By providing a deterministic, JSON‑patch interface, the project lets multiple agents share a common “memory” of slide content and coordinate changes without custom parsing logic.  
- **Workflow composability**: The CLI can be chained with other tools (LLM calls, data fetchers, validation steps), enabling end‑to‑end pipelines such as automated report generation, multi‑agent review cycles, or content compliance checks.  
- **Rapid prototyping**: With only a single dependency (Python) and a clear command‑line contract, teams can prototype complex PowerPoint automation in days rather than weeks.

**Practical adoption path**  
1. **Evaluate the CLI** – Run the supplied `hands-on-deck` commands on a sample *.pptx* to verify the JSON‑patch semantics match your use case.  
2. **Wrap as an Agent Skill** – Register the CLI endpoint in your orchestration platform (e.g., LangChain, CrewAI, or custom agent framework) using the provided SDK stub.  
3. **Integrate into pipelines** – Combine the skill with other agents (data extraction, summarization, validation) via a workflow engine (Airflow, Prefect, or a simple bash/Makefile).  
4. **Add tests & monitoring** – Write unit tests for the JSON patches you rely on and instrument the CLI’s exit codes for health checks.

**Production readiness**  
- **Maturity**: Medium. The repo is actively maintained (last update 2026‑06‑26), has 114 stars and 8 forks, and the codebase is small enough for quick audit.  
- **Dependencies**: Pure‑Python with standard PPTX libraries, but you should verify compatibility with your runtime environment and pin versions.  
- **Risks**: License and security posture need a final review; the maintainer count is low, so plan for an internal fallback or contribution plan if long‑term support is required.  
- **Recommendation**: Suitable for internal prototypes, pilot projects, or as a component of larger agent orchestration systems; for production use, perform a security audit, add CI/CD testing, and consider a maintenance agreement or fork to guarantee continuity.

### Русский

**EveryInc/hands‑on‑deck** — это open‑source‑инструмент, позволяющий AI‑агентам программно работать с PowerPoint: просматривать, редактировать, создавать и проверять *.pptx*‑файлы через атомарные JSON‑патчи, упакованные в виде Agent Skill. Типичный сценарий — построение повторяемых многокомпонентных пайплайнов, где несколько агентов последовательно используют один и тот же набор инструментов (например, генерация слайдов, их проверка и финальная сборка), что упрощает координацию и стандартизацию памяти агентов. Готовность к production — средняя: проект подходит для прототипов и внутренних воркфлоу, но перед выпуском в продакшн требуется проверка лицензии, безопасности и поддерживаемости зависимостей.

### 中文

**项目简介（2‑3 句）**  
EveryInc/hands‑on‑deck 是一个面向 AI 代理的 PowerPoint 操作库，提供唯一的 CLI，支持通过原子 JSON Patch 对 *.pptx* 文件进行检查、编辑、创建和校验，并以 Agent Skill 形式打包供调用。  

**价值**  
- **把零散的提示与工具统一成可复用的工作流**：代理可以在同一流水线中读取、修改、生成 PPT，省去手工脚本和多语言转换的麻烦。  
- **支持多代理协同**：在多 agent 场景下，可用同一套 JSON Patch 描述共享的 PPT 状态，实现“记忆”同步与结果校验。  
- **标准化、可审计的文档编辑**：每一次改动都以 JSON Patch 记录，便于回滚、审计和自动化测试。  

**典型接入方式**  
1. **CLI 调用**：在脚本或容器中直接执行 `hands-on-deck <command> --input file.pptx --patch patch.json`，适合快速原型或 CI/CD 步骤。  
2. **Python SDK**：通过 `import hands_on_deck` 调用 `load_pptx()、apply_patch()、export_pptx()` 等函数，便于在自定义 Agent 代码中嵌入。  
3. **REST/SDK 包装**：将 CLI 或 SDK 包装成 HTTP 接口，供语言无关的 Agent 框架（如 LangChain、AutoGPT）通过 API 调用。  

**生产可用性**  
- **成熟度**：当前评分 68/100，已在 GitHub 获得 114 星、8 次 Fork，最近一次更新为 2026‑06‑26，代码基于 Python，具备基本的社区活跃度。  
- **适用范围**：适合原型、内部工具或受控环境的自动化 PPT 处理；在正式生产环境使用前，需要完成以下检查：  
  - **依赖安全审计**：确认第三方库（如 `python-pptx`）的安全漏洞和许可证兼容性。  
  - **维护者沟通**：确认项目维护者的响应速度，或自行 fork 并制定内部维护计划。  
  - **容错与监控**：为 CLI/SDK 加装超时、重试和日志上报，以防止因文件损坏或网络波动导致的任务卡死。  
- **结论**：在做好安全与运维审查后，hands‑on‑deck 可作为内部或受限生产环境的可靠组件，帮助团队把“AI 代理 + PPT”这一碎片化需求转化为可重复、可审计的工作流。

## 🧭 Practical evaluation

**Value:** EveryInc/hands-on-deck helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 114 GitHub stars
- 8 forks
- updated 2026-06-26
- primary language: Python
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 44/100 |
| topics | 75/100 |
| outlook | 56/100 |
| quality | 53/100 |
| recency | 40/100 |
| adoption | 38/100 |
| production | 55/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/EveryInc/hands-on-deck) · [← Back to Orchestration](./README.md)</sub>
