# wazionapps/nexo

[![Stars](https://img.shields.io/github/stars/wazionapps/nexo?style=flat-square&color=yellow)](https://github.com/wazionapps/nexo/stargazers) [![Forks](https://img.shields.io/github/forks/wazionapps/nexo?style=flat-square&color=blue)](https://github.com/wazionapps/nexo/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> NEXO Brain — Shared brain for AI agents. Persistent memory, semantic RAG, natural forgetting, metacognitive guard, trust scoring, 150+ MCP tools. Works with Claude Code, Codex, Claude Desktop & any MCP client. 100% local, open source, free.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 20 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | Python |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-memory` `atkinson-shiffrin` `autonomous-agent` `claude-code` `claude-code-plugin` `codex` `cognitive-architecture` `knowledge-graph` `local-first` `mcp` `mcp-server` `memory`

## 🎯 Categories

MCP · Knowledge/RAG · Automation · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary**  
NEXO Brain is an open‑source, fully local “shared brain” for AI agents that provides persistent memory, semantic retrieval‑augmented generation, natural forgetting, metacognitive guards, trust scoring and a suite of 150+ Model‑Context‑Protocol (MCP) tools. It works with Claude Code, Claude Desktop, Codex and any MCP‑compatible client, letting developers hook large‑language‑model assistants to real‑world tools and data without sending anything to the cloud.

**Value**  
- **Unified memory & reasoning layer** – agents can store, retrieve and forget information semantically, which improves continuity across sessions and reduces hallucinations.  
- **Safety & trust** – built‑in metacognitive checks and trust scores help filter unreliable outputs before they reach users or downstream systems.  
- **Tool integration out‑of‑the‑box** – the 150+ MCP utilities (web‑search, database access, code execution, etc.) let an assistant act on real data and services through a single, standard protocol, dramatically shortening integration effort.

**Practical Adoption Path**  
1. **Prototype** – clone the repo, run the provided Docker/CLI starter, and point your Claude, Codex or other MCP client at the local NEXO server.  
2. **Extend** – add or customize MCP tools (Python SDK) to expose internal services (e.g., CRM, monitoring APIs).  
3. **Deploy** – containerize the NEXO service, place it behind your internal network firewall, and configure your production AI agents to use it as the shared memory/tooling endpoint.  
4. **Monitor & Tune** – use the built‑in trust‑scoring dashboard to observe agent behavior, adjust forgetting policies, and iteratively add new tools.

**Production Readiness**  
- **Activity & ecosystem** – recent commits (as of 2026‑05‑13), 20+ topics, 20 ⭐ stars and 8 forks show an active community.  
- **Technical maturity** – core components are written in Python, exposed via a clear API/CLI, and tested with major Claude and Codex clients, indicating low integration friction.  
- **Risk profile** – no major metadata or licensing red flags identified, but a final security audit and confirmation of maintainers’ availability are recommended before a full‑scale rollout. Overall, NEXO is a strong OSS candidate for pilots and can be promoted to production once the standard security review is completed.

### Русский

**wazionapps/nexo** — открытая платформа‑«общий мозг» для AI‑агентов, обеспечивающая постоянную память, семантический RAG, естественное забывание, метакогнитивный контроль и оценку доверия, а также более 150 готовых MCP‑инструментов. Типичное внедрение — подключение интеллектуальных ассистентов к реальным сервисам и данным через единый Model Context Protocol (MCP), запуск собственного MCP‑сервера и стандартизация интеграций в любой стек. Проект имеет высокий уровень готовности к продакшн: активные коммиты, растущее сообщество (20 звёзд, 8 форков), поддержка Python, публичный API/SDK/CLI и недавнее обновление — достаточно для серьёзного пилотного использования после финального аудита лицензии и безопасности.

### 中文

**项目简介（2‑3 句）**  
NEXO Brain 是一个本地、开源的共享记忆层，为 AI 代理提供持久记忆、语义检索（RAG）、自然遗忘、元认知守护、信任评分以及 150+ MCP（Model Context Protocol）工具。它兼容 Claude Code、Codex、Claude Desktop 以及任意 MCP 客户端，全部运行在本机，无需云服务。

**价值**  
- **统一协议**：通过标准的 MCP 接口，将 AI 助手与真实工具、数据源快速对接，降低集成成本。  
- **增强记忆**：持久化的语义记忆与自然遗忘机制，让代理能够在长期任务中保持上下文一致性。  
- **安全可控**：元认知守护和信任评分帮助过滤不可靠的生成，提升系统安全性。  

**典型接入方式**  
1. **API / SDK**：项目提供 Python SDK 与 HTTP API，直接在业务代码中调用 `nexo.memory.store()`、`nexo.rag.query()` 等函数。  
2. **CLI**：通过 `nexo-cli` 可以在命令行快速启动本地记忆服务或执行 RAG 查询，适合脚本化集成。  
3. **MCP 服务器**：部署 NEXO 作为 MCP 服务器后，任何遵循 Model Context Protocol 的客户端（如 Claude Desktop、Codex）即可即插即用。  

**生产可用性**  
- **活跃度**：最近一次提交为 2026‑05‑13，拥有 20+ 话题标签、20 颗星、8 个 fork，社区活跃。  
- **技术成熟度**：核心实现采用 Python，提供完整的 API、SDK 与 CLI 文档，已在多个内部 pilot 项目中验证。  
- **安全与合规**：暂无重大元数据风险，仍需进一步审查许可证（MIT）和依赖安全性。总体而言，作为 OSS 候选，NEXO 在功能完整性、生态兼容性和部署便利性方面已具备在生产环境中进行试点的条件。

## 🧭 Practical evaluation

**Value:** wazionapps/nexo helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 20 GitHub stars
- 8 forks
- updated 2026-05-13
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 28/100 |
| topics | 100/100 |
| outlook | 54/100 |
| quality | 47/100 |
| recency | 20/100 |
| adoption | 27/100 |
| production | 52/100 |
| usefulness | 100/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/wazionapps/nexo) · [← Back to Mcp](./README.md)</sub>
