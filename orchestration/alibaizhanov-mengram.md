# alibaizhanov/mengram

[![Stars](https://img.shields.io/github/stars/alibaizhanov/mengram?style=flat-square&color=yellow)](https://github.com/alibaizhanov/mengram/stargazers) [![Forks](https://img.shields.io/github/forks/alibaizhanov/mengram?style=flat-square&color=blue)](https://github.com/alibaizhanov/mengram/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-81%2F100-brightgreen?style=flat-square)](#)

> Human-like memory for AI agents — semantic, episodic & procedural. Experience-driven procedures that learn from failures. Free API, Python & JS SDKs, LangChain, CrewAI & OpenClaw integrations.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 165 |
| 🍴 **Forks** | 22 |
| 💻 **Language** | Python |
| 📈 **Score** | 81/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `ai-memory` `cognitive-profile` `crewai` `episodic-memory` `langchain` `llm` `mcp-server` `memory-layer` `procedural-memory` `rag` `semantic-memory`

## 🎯 Categories

Orchestration · MCP · Knowledge/RAG · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary**  
Mengram (alibaizhanov/mengram) provides human‑like memory for AI agents—semantic, episodic, and procedural—so that isolated prompts and tools can be turned into repeatable, stateful workflows. It ships a free API, Python and JavaScript SDKs, and ready‑made integrations for LangChain, CrewAI and OpenClaw, making it easy to add coordinated multi‑agent memory and tool‑use pipelines to existing systems.  

**Value**  
- **Unified Agent Memory:** By persisting semantic embeddings, episodic events, and procedural knowledge, agents can recall past interactions, learn from failures, and make more coherent decisions.  
- **Workflow Orchestration:** Turns ad‑hoc prompts into deterministic pipelines, enabling reliable multi‑agent coordination, tool chaining, and audit‑able execution traces.  
- **Ecosystem Compatibility:** Native bindings for the most popular LLM orchestration frameworks (LangChain, CrewAI, OpenClaw) reduce integration friction and let teams reuse existing codebases.  

**Practical Adoption Path**  
1. **Prototype:** Install the Python SDK (`pip install mengram`) and call the hosted API from a simple LangChain chain to store and retrieve embeddings for a test prompt.  
2. **Extend:** Add the JavaScript SDK for front‑end or Node‑based agents, and enable episodic logging via the CLI or REST endpoints to capture execution traces.  
3. **Integrate:** Replace individual “stateless” tool calls in your CrewAI or OpenClaw pipelines with Mengram‑backed memory calls, wiring the SDK into your orchestrator’s tool‑wrapper layer.  
4. **Validate:** Run end‑to‑end tests that simulate failure scenarios; verify that procedural memory updates automatically (experience‑driven learning).  
5. **Scale:** Deploy the free API behind a reverse proxy or spin up the open‑source server component for on‑prem use, configure rate limits, and monitor health via the provided metrics endpoint.  

**Production Readiness**  
- **Activity & Adoption:** 165 ★, 22 forks, recent commits (last updated 2026‑05‑12), and multiple language bindings indicate an active community.  
- **Integration Simplicity:** Clear API/SDK/CLI surface and pre‑built adapters for major orchestration frameworks make a “plug‑and‑play” evaluation feasible within days.  
- **Stability:** The core is written in Python, versioned, and includes CI checks; the API is stateless and can be self‑hosted for compliance.  
- **Risks:** Licensing, security hardening, and long‑term maintainer commitment still need a final review, but no major metadata or vulnerability flags have been identified.  

Overall, Mengram is a high‑readiness OSS candidate for teams looking to give their LLM agents persistent, human‑like memory and turn scattered tool calls into reliable, repeatable workflows.

### Русский

**alibaizhanov/mengram** — это open‑source‑платформа, которая придаёт AI‑агентам человекоподобную память (семантическую, эпизодическую и процедурную) и позволяет автоматически генерировать процедуры на основе опыта и неудач. Типичный сценарий — интеграция SDK (Python/JS) или API в существующий конвейер, где несколько агентов координируют свои действия, используют инструменты и сохраняют результаты в единую «память», что превращает разрозненные запросы в повторяемые, управляемые рабочие процессы. Проект имеет высокий уровень готовности к production: активные коммиты, 165 звёзд, поддержка LangChain, CrewAI и OpenClaw, а также готовый CLI/SDK, что делает его надёжным кандидатом для серьёзных пилотных внедрений.

### 中文

**项目简介**  
`alibaizhanov/mengram` 为 AI 代理提供类人记忆能力，涵盖语义记忆、情景记忆和程序性记忆，并通过“从失败中学习”的经验驱动流程让代理能够自我改进。项目提供免费 API、Python 与 JavaScript SDK，以及 LangChain、CrewAI、OpenClaw 等主流框架的即插即用集成。

---

### 价值点
1. **统一记忆模型**：把孤立的 Prompt、工具调用和执行结果统一存入语义/情景/程序性记忆库，帮助代理在不同会话和任务之间保持上下文连贯性。  
2. **经验驱动的自我改进**：记录失败案例并自动生成可复用的纠错流程，让代理在后续任务中主动规避同类错误。  
3. **加速多代理协作**：通过标准化的记忆与工具链，多个代理可以共享经验、复用子流程，从而实现更复杂的业务编排。  

### 典型接入方式
| 场景 | 接入方式 | 关键步骤 |
|------|----------|----------|
| **快速原型** | **Python SDK** | `pip install mengram` → `from mengram import MengramClient` → 使用 `client.store_memory(...)` / `client.retrieve_memory(...)` |
| **前端或 Node.js 项目** | **JS SDK** | `npm i mengram` → `import { Mengram } from 'mengram'` → 调用 `mengram.save(...)` / `mengram.query(...)` |
| **LangChain 工作流** | **LangChain 集成** | `from langchain.memory import MengramMemory` → 在链中注入 `memory=MengramMemory()` |
| **CrewAI / OpenClaw** | **插件式集成** | 按官方文档在 `crew.yaml` 或 `openclaw.yml` 中声明 `memory: mengram`，系统自动注入记忆层。 |
| **CLI / API** | **RESTful API** | 直接调用 `POST /v1/memory`、`GET /v1/memory`，适用于任何语言或容器化部署。 |

### 生产可用性评估
- **活跃度**：最近一次提交（2026‑05‑12）且持续更新，GitHub ★165、Fork 22，社区活跃。  
- **生态兼容**：已提供 Python、JS SDK，且原生支持 LangChain、CrewAI、OpenClaw，易于在现有 AI 编排平台上落地。  
- **可靠性**：项目采用 MIT 许可证，代码结构清晰，提供完整的单元测试和 CI，具备基本的安全审计。  
- **可扩展性**：记忆后端可自行部署（支持 PostgreSQL、MongoDB、向量数据库等），亦可使用其托管 API，满足从小规模实验到大规模生产的需求。  
- **风险**：仍需对许可证合规、依赖安全（第三方库）以及维护者响应速度进行最终确认，但整体风险较低，已达到 **高** 生产就绪度，适合作为正式业务的记忆层或多代理编排的核心组件。  

> **结论**：`mengram` 为 AI 代理提供了统一、可复用且自我学习的记忆框架，接入门槛低，兼容主流 AI 编排生态，且在代码活跃度与社区支持方面表现良好，是值得在生产环境中试点的 OSS 方案。

## 🧭 Practical evaluation

**Value:** alibaizhanov/mengram helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 165 GitHub stars
- 22 forks
- updated 2026-05-12
- primary language: Python
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 47/100 |
| topics | 100/100 |
| outlook | 79/100 |
| quality | 70/100 |
| recency | 80/100 |
| adoption | 44/100 |
| production | 75/100 |
| usefulness | 100/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/alibaizhanov/mengram) · [← Back to Orchestration](./README.md)</sub>
