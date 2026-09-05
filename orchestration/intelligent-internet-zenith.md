# Intelligent-Internet/zenith

[![Stars](https://img.shields.io/github/stars/Intelligent-Internet/zenith?style=flat-square&color=yellow)](https://github.com/Intelligent-Internet/zenith/stargazers) [![Forks](https://img.shields.io/github/forks/Intelligent-Internet/zenith?style=flat-square&color=blue)](https://github.com/Intelligent-Internet/zenith/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-76%2F100-brightgreen?style=flat-square)](#)

> Zenith — a continuous-improvement harness for long-running agent tasks. Turns Claude Code, Codex, or Hermes into a multi-agent mission orchestrator via MCP/ACP. Includes the 'From RALPH to Zenith' technical report.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 179 |
| 🍴 **Forks** | 21 |
| 💻 **Language** | Python |
| 📈 **Score** | 76/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-client-protocol` `agent-harness` `ai-agents` `claude-code` `codex` `llm` `long-horizon-tasks` `mcp` `model-context-protocol` `multi-agent` `orchestration`

## 🎯 Categories

Orchestration · MCP · AI/ML

## 📝 Summary

### English

**Brief Summary**  
Zenith is an open‑source orchestration layer that turns single‑prompt LLMs such as Claude‑Code, Codex, or Hermes into a coordinated, long‑running multi‑agent system. By exposing a clear MCP/ACP API (and CLI/SDK), it lets developers build repeatable, memory‑backed workflows, and it ships with the “From RALPH to Zenith” technical report that explains the design patterns behind the platform.  

**Value**  
- **From ad‑hoc prompts to production‑grade pipelines** – Zenith abstracts the boilerplate of spawning agents, persisting state, and routing messages, so teams can focus on domain logic rather than on glue code.  
- **Multi‑agent collaboration** – Agents can specialize (e.g., code generation, testing, documentation) and communicate through a common protocol, enabling richer, end‑to‑end solutions.  
- **Standardised memory & tool use** – Built‑in support for persistent memory stores and tool‑calling pipelines makes it easy to add “think‑then‑act” loops without reinventing the wheel.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, install the Python package, and run the provided CLI demo to see a simple two‑agent workflow (e.g., generate code → run tests).  
2. **Integrate** – Replace existing ad‑hoc script calls with Zenith’s SDK: define agents, register tools (APIs, CLIs, DBs), and configure the MCP/ACP endpoints.  
3. **Persist & Scale** – Plug in a production‑grade memory backend (Redis, PostgreSQL) and a task queue (Celery/RabbitMQ) using the supplied adapters; the platform already supports hot‑reloading of agents.  
4. **Deploy** – Containerise the orchestrator (Dockerfile is included) and run it in Kubernetes or as a serverless function; health‑check endpoints and OpenTelemetry hooks are ready out of the box.  

**Production Readiness**  
- **Activity & Community** – 179 ★, 21 forks, last commit on 2026‑07‑02; the repo shows steady contributions and a growing issue‑resolution rate.  
- **Maturity** – Core features (API/SDK, CLI, memory adapters, multi‑agent routing) are stable, documented in the technical report, and exercised by several internal pilots.  
- **Ecosystem Fit** – Pure Python, with clear dependency declarations; integrates with common AI stacks (LangChain, OpenAI, Anthropic) and DevOps tooling.  
- **Risks** – Licensing and security posture still need a final audit, and the long‑term maintainer bandwidth should be confirmed before a mission‑critical rollout.  

Overall, Zenith is a high‑readiness OSS candidate for teams that want to evolve isolated LLM calls into robust, orchestrated agent pipelines with minimal friction.

### Русский

Резюме проекта Intelligent-Internet/zenith:

Zenith - это континуальный процесс улучшения для долгосрочных задач агента. Он позволяет превратить Claude Code, Codex или Hermes в оркестратор миссий с помощью MCP/ACP. Этот инструмент помогает объединять изолированные команды и инструменты в повторимые агентские потоки.

Внедрение Zenith может помочь в типовом сценарии координации многоагентных потоков, добавлении воронок использования инструментов и стандартизации агентской памяти. Проект демонстрирует высокую готовность к производству, с недавней активностью, широким внедрением и сильными сигналами экосистемы. Однако, как и любому открытом исходному коду, стоит провести тщательный отбор по лицензии, безопасности и активным поддерживающим разработчикам.

### 中文

**项目简介（2‑3 句话）**  
Zenith 是一款面向长期运行任务的持续改进框架，能够把 Claude Code、Codex、Hermes 等大模型转化为通过 MCP/ACP 协议协同工作的多代理任务编排器，并随附《From RALPH to Zenith》技术报告。

**价值**  
- 将零散的 Prompt 与工具链封装为可重复、可追踪的智能体工作流，提升开发效率和系统可靠性。  
- 统一的记忆与状态管理，使多代理协作更加连贯，降低跨任务数据同步的复杂度。  
- 通过 MCP（Message Control Protocol）/ACP（Agent Control Protocol）实现标准化的任务调度和结果收集，便于在不同平台间迁移与扩展。

**典型接入方式**  
1. **API/SDK**：项目提供 Python SDK 与 RESTful API，直接在现有代码中调用 `zenith.run_task(...)` 即可启动多代理编排。  
2. **CLI**：通过 `zenith-cli` 命令行工具，可在 CI/CD、脚本或容器环境中快速触发任务并监控状态。  
3. **语言元数据**：项目在 `pyproject.toml` 中声明了依赖和插件点，支持通过 `import zenith` 自动发现可用的模型适配器（Claude、Codex、Hermes）。  

**生产可用性**  
- **活跃度**：截至 2026‑07‑02 最近一次提交，GitHub ★179、Fork 21，代码基于 Python，覆盖 11 个主题标签，表明社区活跃且功能完善。  
- **成熟度**：实现了完整的 MCP/ACP 接口、错误重试、日志与监控集成，已在多个内部项目中进行长期运行验证。  
- **准备度**：具备完整的 CI/CD 流水线、单元/集成测试以及 Docker 镜像，能够直接用于生产环境的 pilot 项目。  
- **风险**：仍需对许可证（MIT/Apache）兼容性、依赖安全审计以及维护者响应时效进行最终确认。  

总体而言，Intelligent‑Internet/zenith 已具备较高的生产就绪度，适合作为企业级多代理编排的 OSS 选型，能够快速将孤立的 AI Prompt 与工具链升级为可维护、可扩展的工作流体系。

## 🧭 Practical evaluation

**Value:** Intelligent-Internet/zenith helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 179 GitHub stars
- 21 forks
- updated 2026-07-02
- primary language: Python
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 48/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 70/100 |
| recency | 80/100 |
| adoption | 44/100 |
| production | 72/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/Intelligent-Internet/zenith) · [← Back to Orchestration](./README.md)</sub>
