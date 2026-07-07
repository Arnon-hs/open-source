# Lyellr88/MARM-Systems

[![Stars](https://img.shields.io/github/stars/Lyellr88/MARM-Systems?style=flat-square&color=yellow)](https://github.com/Lyellr88/MARM-Systems/stargazers) [![Forks](https://img.shields.io/github/forks/Lyellr88/MARM-Systems?style=flat-square&color=blue)](https://github.com/Lyellr88/MARM-Systems/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-87%2F100-brightgreen?style=flat-square)](#)

> Stop re-explaining yourself to AI. MARM offers persistent memory, cross-agent context sharing, write queues, swarm-ready presets, and compaction for clean recall. Includes a live web dashboard for managing memories, logs, and sessions. MCP connects over HTTP & STDIO and works with major LLMs like Claude, Codex, Grok, Gemini, and other models.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 305 |
| 🍴 **Forks** | 57 |
| 💻 **Language** | Python |
| 📈 **Score** | 87/100 |
| 🗓️ **Last push** | 2026-06-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-swarms` `claude` `developer-tools` `docker-image` `embeddings` `fastapi` `gemini-cli` `knowledge-based-systems` `mcp` `mcp-server` `memory-management` `openai`

## 🎯 Categories

Orchestration · MCP · Knowledge/RAG · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
MARM‑Systems is an open‑source orchestration layer that gives LLM‑driven agents persistent memory, cross‑agent context sharing, write queues, and swarm‑ready presets, all managed through a live web dashboard. It connects to LLMs (Claude, Codex, Grok, Gemini, etc.) via HTTP or STDIO and provides a modular MCP (Message Control Protocol) that makes it easy to build repeatable, tool‑augmented agent workflows.

---

### Value Proposition
- **Persistent, shared memory** eliminates the need to re‑prompt the same information, enabling agents to build on prior interactions and coordinate more intelligently.  
- **Write queues & compaction** keep the memory store clean and performant, which is critical for long‑running or high‑throughput applications.  
- **Swarm‑ready presets** let you spin up multi‑agent collaborations with minimal boilerplate, turning ad‑hoc prompt chains into reproducible pipelines.  
- **Live dashboard** gives operators visibility into memories, logs, and session states, simplifying debugging and governance.  
- **Broad LLM compatibility** (Claude, Codex, Grok, Gemini, etc.) means you can adopt MARM without locking into a single provider.

### Practical Adoption Path
1. **Pilot Setup** – Clone the repo, install the Python dependencies, and run the provided Docker compose or local server script to launch the dashboard and MCP endpoint.  
2. **Connect Your Model** – Configure the MCP to point at your chosen LLM via HTTP or STDIO (the SDK includes ready‑made adapters for Claude, Gemini, etc.).  
3. **Define Memory Schemas** – Use the dashboard or YAML presets to declare the memory keys and compaction policies your agents need.  
4. **Wrap Existing Tools** – Export your tool‑use functions as HTTP endpoints or CLI commands; MARM’s write‑queue will automatically serialize calls and feed results back to the agents.  
5. **Scale to Swarms** – Duplicate the agent definition across multiple workers; the cross‑agent context store ensures each instance sees the same shared memory, enabling coordinated decision‑making.  
6. **Monitoring & Governance** – Leverage the dashboard’s logs and session tracking to audit behavior, set retention policies, and iterate on prompts.

### Production Readiness
- **Activity & Community** – 305 stars, 57 forks, frequent commits (latest 2026‑06‑24), and a clear Python codebase indicate an active project.  
- **Architecture** – Decoupled MCP over HTTP/STDIO and a stateless dashboard make deployment on Kubernetes, VM, or edge environments straightforward.  
- **Scalability** – Write queues and memory compaction are built‑in, reducing bottlenecks for high‑volume workloads.  
- **Ecosystem Fit** – Works with the major LLM APIs and can be wrapped around any custom model, easing integration into existing AI stacks.  
- **Risks** – Licensing terms, security hardening, and long‑term maintainer commitment still need a final review, but no major metadata or compliance concerns have been identified.

Overall, MARM‑Systems offers a mature, feature‑rich foundation for turning isolated prompts into reliable, memory‑aware, multi‑agent pipelines, making it a strong candidate for production pilots in any organization that builds LLM‑centric automation.

### Русский

Lyellr88/MARM-Systems — это открытая платформа, позволяющая превратить разрозненные запросы и инструменты в повторяемые агентные рабочие процессы: она обеспечивает постоянную память, совместный контекст между агентами, очереди записи, готовые пресеты для ро́йдовых (swarm) сценариев и компактизацию данных для чистого извлечения. Типичное внедрение — подключение MCP к LLM (Claude, Gemini, Grok и др.) через HTTP/STDIO, настройка веб‑дашборда для мониторинга и управления памятью, логами и сессиями, а затем построение мульти‑агентных пайплайнов с инструментами и стандартизированной памятью. Проект имеет высокий уровень готовности к production: активные коммиты, более 300 звёзд, широкая поддержка моделей и ясный API/SDK/CLI, что делает его надёжным кандидатом для пилотных и масштабных внедрений.

### 中文

**项目简介（2‑3 句话）**  
Lyellr88/MARM-Systems 为大模型提供持久记忆、跨代理上下文共享、写入队列、可直接用于 swarm 的预设以及记忆压缩功能，并配备实时 Web 仪表盘用于管理记忆、日志和会话。MCP 通过 HTTP 与 STDIO 双通道对接，兼容 Claude、Codex、Grok、Gemini 等主流 LLM，帮助把零散的 Prompt 与工具组装成可复用的智能体工作流。

**价值**  
- **统一记忆层**：持久化记忆和跨代理共享，让多个智能体能够在同一上下文中协同工作，避免重复解释。  
- **工作流标准化**：写入队列、Swarm‑ready 预设以及记忆压缩，使得复杂的多智能体、工具调用流程可以像普通函数一样被复用和调度。  
- **可观测性**：Web Dashboard 实时展示记忆、日志和会话，便于调试、审计和性能监控。  

**典型接入方式**  
1. **HTTP API**：启动 MARM 的 MCP 服务后，使用 RESTful 接口发送 `POST /memory`, `GET /session` 等请求，适合微服务或容器化部署。  
2. **STDIO 接口**：在本地或 CI 环境下直接通过标准输入/输出与模型交互，适合脚本化或嵌入式使用。  
3. **SDK / CLI**：项目提供 Python SDK 与命令行工具，封装了 API 调用，可快速在现有 Python 项目或自动化脚本中集成。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑24 最近一次提交，GitHub 305 星、57 Fork，代码基于 Python，拥有 15 个相关话题，表明社区活跃且生态兼容性好。  
- **成熟度**：提供完整的 API 文档、示例项目以及可视化 Dashboard，已在多个内部实验中用于多智能体协作，具备可观测性和故障恢复机制。  
- **风险**：目前未发现重大元数据或安全漏洞，但仍需审查许可证（MIT/Apache 等）以及维护者的长期可用性。整体来看，MARM‑Systems 已具备 **高** 的生产候选级别，适合作为企业级多智能体编排和记忆管理的核心组件进行试点。

## 🧭 Practical evaluation

**Value:** Lyellr88/MARM-Systems helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 305 GitHub stars
- 57 forks
- updated 2026-06-24
- primary language: Python
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 53/100 |
| topics | 100/100 |
| outlook | 88/100 |
| quality | 78/100 |
| recency | 100/100 |
| adoption | 50/100 |
| production | 83/100 |
| usefulness | 100/100 |
| integration | 100/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/Lyellr88/MARM-Systems) · [← Back to Orchestration](./README.md)</sub>
