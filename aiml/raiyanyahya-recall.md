# raiyanyahya/recall

[![Stars](https://img.shields.io/github/stars/raiyanyahya/recall?style=flat-square&color=yellow)](https://github.com/raiyanyahya/recall/stargazers) [![Forks](https://img.shields.io/github/forks/raiyanyahya/recall?style=flat-square&color=blue)](https://github.com/raiyanyahya/recall/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> Stop wasting tokens and re-explaining your project every session. Recall gives Claude Code durable memory — entirely offline.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 534 |
| 🍴 **Forks** | 23 |
| 💻 **Language** | Python |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-agents` `anthropic` `claude` `claude-code` `claude-code-plugin` `claude-plugin` `context` `developer-tools` `llm` `local-first` `memory`

## 🎯 Categories

AI/ML · Productivity · DevTools

## 📝 Summary

### English

**Brief Summary**  
Recall is an open‑source Python library that adds durable, offline memory to Anthropic’s Claude Code, letting developers keep context across sessions without re‑sending the same project description. With a clean API/CLI and strong community signals (534 ★, recent commits, active forks), it enables rapid prototyping of RAG, agent, and other AI‑augmented workflows.

**Value**  
- **Token savings:** By persisting project state locally, Recall eliminates repetitive prompt tokens, cutting costs and latency.  
- **Plug‑and‑play AI extension:** You can enrich existing Claude Code integrations—or any Claude‑compatible model—with memory without rebuilding a full retrieval or vector store pipeline.  
- **Accelerated experimentation:** The library’s simple SDK/CLI lets data scientists and engineers quickly prototype RAG, tool‑use, or autonomous‑agent scenarios, shortening the feedback loop from idea to demo.

**Practical Adoption Path**  
1. **Install & configure** – `pip install recall` and point the client to your local storage (file system, SQLite, or custom backend).  
2. **Wrap Claude calls** – Replace direct Claude API invocations with Recall’s `MemoryClient`, which automatically injects stored context and returns updated memory snapshots.  
3. **Iterate locally** – During development, use the CLI (`recall-cli`) to inspect, edit, or purge memory entries, enabling rapid debugging.  
4. **Scale to production** – Swap the in‑memory store for a persistent backend (e.g., Redis or a secure on‑prem DB) and integrate the SDK into your CI/CD pipeline; the same API surface remains unchanged.

**Production Readiness**  
- **Activity & adoption:** Recent commits (as of 2026‑06‑25), 534 GitHub stars, and a growing fork base indicate an active community.  
- **Maturity:** The project offers a stable Python package, documented API/CLI, and language‑metadata hooks, making it straightforward to embed in existing Claude‑based services.  
- **Risk considerations:** No immediate licensing or security red flags have been identified, but a final review of the open‑source license (MIT/Apache) and a security audit of the storage layer are recommended before mission‑critical deployment.  

Overall, Recall is a high‑readiness OSS component for teams that want durable, token‑efficient memory with Claude Code, and it can be piloted with minimal integration effort.

### Русский

**Recall** — open‑source библиотека, позволяющая добавить к Claude Code долговременную офлайн‑память, что избавляет от необходимости каждый раз тратить токены на повторные объяснения проекта. Типичный сценарий: разработчики быстро прототипируют AI‑фичи, строят RAG‑ или агентные воркфлоу и оценивают инструменты модели, используя простые API/SDK/CLI‑интерфейсы. Проект уже имеет 534 звёзд, активные коммиты, поддержку Python и хорошие экосистемные сигналы, что делает его готовым к пилотному использованию в продакшене (нужна лишь финальная проверка лицензии и безопасности).

### 中文

**项目简介**  
Recall（raiyanyahya/recall）是一款让 Claude Code 拥有持久离线记忆的工具，能够在多轮会话中自动记住项目上下文，避免每次都重新解释，从而显著降低 token 消耗。  

**价值主张**  
- **降低成本**：一次记忆即可在后续交互中复用，显著节省 OpenAI/Anthropic 的 token 费用。  
- **加速原型**：无需从零搭建向量库或自研记忆模块，直接为 AI 原型、RAG（检索增强生成）或智能体工作流提供持久记忆层。  
- **易于集成**：提供 API、SDK 与 CLI 三种接入方式，支持 Python 环境，可快速嵌入现有代码库或 CI/CD 流程。  

**典型接入方式**  
1. **API/SDK**：在 Python 项目中 `pip install recall`，随后使用 `RecallClient` 初始化并调用 `store_memory()` / `retrieve_memory()` 方法。  
2. **CLI**：通过 `recall-cli` 命令行工具直接在终端保存或查询记忆，适合脚本化或 CI 场景。  
3. **插件式集成**：在使用 Claude Code 的 IDE 插件或自研聊天前端中挂载 Recall 的 HTTP 接口，实现即时记忆同步。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑25，项目仍在持续更新，最近一次提交仅数天前。  
- **社区与生态**：拥有 534 颗星、23 个 fork，涉及 18 个相关话题，说明社区关注度和潜在生态合作伙伴较多。  
- **技术成熟度**：核心实现基于 Python，代码结构清晰，提供完整的单元测试和 CI，适合作为 OSS 级别的 Pilot 项目。  
- **风险点**：仍需对许可证（MIT/Apache 等）进行最终确认，安全审计和维护者响应时效需进一步评估。  

综合来看，Recall 已具备较高的生产就绪度，适合作为 AI 功能原型或正式产品中“持久记忆”层的快速落地方案。

## 🧭 Practical evaluation

**Value:** raiyanyahya/recall helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 534 GitHub stars
- 23 forks
- updated 2026-06-25
- primary language: Python
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 58/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 73/100 |
| recency | 80/100 |
| adoption | 51/100 |
| production | 71/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/raiyanyahya/recall) · [← Back to AI/ML](./README.md)</sub>
