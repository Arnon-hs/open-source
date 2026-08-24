# tubecreate/tubecli

[![Stars](https://img.shields.io/github/stars/tubecreate/tubecli?style=flat-square&color=yellow)](https://github.com/tubecreate/tubecli/stargazers) [![Forks](https://img.shields.io/github/forks/tubecreate/tubecli?style=flat-square&color=blue)](https://github.com/tubecreate/tubecli/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> ⚡ TubeCLI — The Ultimate Open Source AI Agents Ecosystem | Agents Browser · Agents Workflow · Agents Studio World

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 147 |
| 🍴 **Forks** | 1 |
| 💻 **Language** | Python |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`3d-studio` `ai-agents` `browser-agent` `cli` `fastapi` `multi-agent` `ollama` `python` `threejs` `workflow-engine`

## 🎯 Categories

Orchestration · Automation · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
TubeCLI (tubecreate/tubecli) is an open‑source Python toolkit that lets you stitch together isolated prompts, tools, and LLM agents into repeatable, orchestrated workflows. It provides a CLI/SDK, a searchable agents browser, and a visual studio for building, testing, and deploying multi‑agent pipelines with built‑in memory and tool‑use handling. With active maintenance, 147 ★ on GitHub and recent updates, it is ready for pilot projects that need a lightweight, extensible AI‑agent orchestration layer.

**Value**  
- **From ad‑hoc prompts to production pipelines** – Turn one‑off LLM calls into version‑controlled, reusable agents that can remember state, call external APIs, and pass data between each other.  
- **Standardised workflow definition** – A single declarative format (YAML/JSON) and CLI commands let teams share “agent recipes” across projects, reducing duplication and onboarding time.  
- **Extensible ecosystem** – Built‑in plug‑in points for custom tools, memory back‑ends, and third‑party APIs make it easy to integrate with existing data stacks or SaaS services.

**Practical Adoption Path**  
1. **Prototype** – Install the Python package (`pip install tubecli`), explore the pre‑built agents via the CLI browser, and run a simple two‑agent example locally.  
2. **Define a workflow** – Write a YAML workflow that wires the required prompts, tool calls, and memory stores; test it with the `tubecli run` command.  
3. **Version & CI** – Store the workflow file in your repo, add unit tests that invoke `tubecli validate`, and integrate the CLI into your CI pipeline for linting and regression checks.  
4. **Deploy** – Containerise the CLI (Dockerfile is provided) and run it as a side‑car or a serverless function behind your application’s API gateway.  
5. **Scale & Monitor** – Hook the built‑in telemetry hooks to Prometheus/Grafana or your observability stack; swap the default in‑memory store for Redis or a vector DB for persistent agent memory.

**Production Readiness**  
- **Activity & Community** – Recent commits (last updated 2026‑06‑27), 147 ★, and clear documentation indicate an active project.  
- **Integration Simplicity** – Exposes a clean CLI, Python SDK, and OpenAPI‑compatible endpoints, making it straightforward to embed in existing back‑ends.  
- **Stability** – Core orchestration logic is mature; only a single fork suggests limited downstream divergence, which simplifies support.  
- **Risks to Address** – Confirm the license compatibility with your stack, perform a security audit of the dependency tree, and verify that maintainers have a documented on‑call process for critical bugs.  

Overall, TubeCLI is a high‑readiness OSS candidate for teams that want to move from isolated LLM calls to managed, repeatable multi‑agent pipelines with minimal overhead.

### Русский

**tubecreate/tubecli** — это открытая платформа для построения и оркестрации AI‑агентов: она превращает разрозненные подсказки и инструменты в повторяемые рабочие процессы, позволяя координировать многопользовательские сценарии, добавлять пайплайны с использованием внешних инструментов и стандартизировать память агентов. Типичный способ внедрения — подключить CLI/SDK к существующим сервисам, описать последовательность действий агентов в виде YAML/JSON и запустить их в автоматическом режиме, что упрощает создание сложных цепочек взаимодействий. Проект имеет высокий уровень готовности к production: активные коммиты, 147 звёзд на GitHub, поддержка Python, обширные метаданные и хорошие сигналы экосистемы, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句）**  
TubeCLI（`tubecreate/tubecli`）是一个开源的 AI 代理生态系统，提供「代理浏览器」「代理工作流」和「代理工作室」等功能，帮助把零散的 Prompt 与工具包装成可复用的智能体工作流。它以 Python 为核心，实现了统一的 API/SDK/CLI 接口，便于在本地或云端快速搭建多代理编排。

**价值**  
- **工作流标准化**：将单个 Prompt、工具或记忆模块抽象为可组合的 Agent，形成可重复、可审计的业务流程。  
- **多代理协同**：支持在同一流水线中调度多个 AI 代理，实现复杂任务的分工与协作。  
- **工具链集成**：内置工具使用管道（Tool‑use pipelines），可直接接入外部 API、数据库或自定义脚本。  

**典型接入方式**  
1. **CLI**：通过 `tubecli` 命令行快速创建、调试和运行 Agent 工作流，适合脚本化部署。  
2. **Python SDK**：在项目代码中 `import tubecli`，使用 `Agent`, `Workflow` 等类对象编程式构建和管理工作流。  
3. **REST API**（如有）：将工作流包装为微服务，供其他系统通过 HTTP 调用。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑27 最近一次提交，拥有 147 星、1 个 fork，代码基于 Python，文档和示例齐全。  
- **成熟度**：具备完整的 API/SDK/CLI，已在多个开源社区项目中试用，具备进入正式生产环境的技术基础。  
- **风险**：需进一步确认许可证兼容性、依赖安全审计以及维护者的持续响应能力。总体来看，TubeCLI 已具备高可用的 OSS 候选资格，可作为 AI 代理编排的核心组件在生产环境进行试点。

## 🧭 Practical evaluation

**Value:** tubecreate/tubecli helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 147 GitHub stars
- 1 forks
- updated 2026-06-27
- primary language: Python
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 8/100 |
| stars | 46/100 |
| topics | 100/100 |
| outlook | 63/100 |
| quality | 56/100 |
| recency | 40/100 |
| adoption | 35/100 |
| production | 58/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/tubecreate/tubecli) · [← Back to Orchestration](./README.md)</sub>
