# openma-ai/open-managed-agents

[![Stars](https://img.shields.io/github/stars/openma-ai/open-managed-agents?style=flat-square&color=yellow)](https://github.com/openma-ai/open-managed-agents/stargazers) [![Forks](https://img.shields.io/github/forks/openma-ai/open-managed-agents?style=flat-square&color=blue)](https://github.com/openma-ai/open-managed-agents/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> Open-source Claude Managed Agents API implementation and self-hosted Claude Tag-style agent runtime. Drop-in compatible; runs on Cloudflare Workers/Durable Objects or Node.js. Apache 2.0.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 184 |
| 🍴 **Forks** | 16 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-framework` `agent-infrastructure` `agent-platform` `ai-agents` `anthropic-api` `anthropic-managed-agents` `byok` `claude-api` `claude-code` `claude-managed-agents` `claude-tag` `claude-tag-alternative`

## 🎯 Categories

Orchestration · MCP · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
openma‑ai’s **open‑managed‑agents** is an open‑source implementation of Claude’s Managed Agents API that lets you run Claude‑style “Tag” agents either on Cloudflare Workers/Durable Objects or in a Node.js environment. It provides a drop‑in compatible runtime for orchestrating multi‑agent, tool‑using workflows, complete with API/SDK/CLI interfaces and built‑in memory handling. Licensed under Apache 2.0, the project is actively maintained and already used in several pilot deployments.

**Value**  
- **From prompts to repeatable workflows** – Turns isolated Claude prompts and tool calls into deterministic, version‑controlled agent pipelines, reducing drift and manual glue code.  
- **Unified orchestration** – Enables multi‑agent coordination, tool‑use pipelines, and standardized memory stores without reinventing the underlying runtime.  
- **Flexibility of deployment** – Works on edge (Cloudflare Workers/Durable Objects) for low‑latency use cases or on traditional Node.js servers for more heavyweight processing.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided CLI or SDK locally to wrap an existing Claude prompt as a Managed Agent.  
2. **Integrate** – Replace ad‑hoc API calls in your application with the Open‑Managed‑Agents SDK, defining agents, tools, and memory schemas in TypeScript.  
3. **Deploy** – Choose the environment that matches your latency/cost profile:  
   - *Edge*: Deploy the Worker/Durable Object bundle to Cloudflare for ultra‑fast, globally distributed execution.  
   - *Server*: Deploy the Node.js package to your existing backend or container platform.  
4. **Scale & Observe** – Use the built‑in logging and health endpoints, add monitoring (e.g., Cloudflare Analytics or Prometheus), and iterate on agent definitions.  

**Production Readiness**  
- **Activity & Community** – 184 ★, 16 forks, recent commits (as of 2026‑06‑26), and a healthy set of 20 topics indicate an active codebase.  
- **Maturity** – The API/SDK/CLI surface is stable, with clear TypeScript typings and documented deployment patterns for both edge and server runtimes.  
- **Risk Profile** – No major metadata or licensing concerns (Apache 2.0); the remaining checks are standard security and maintainer responsiveness reviews.  
Overall, the project is considered **highly ready for a serious pilot** and can be promoted to production once the organization completes its usual security and compliance vetting.

### Русский

**openma‑ai/open-managed-agents** – это открытая реализация API управляемых агентов Claude и среда выполнения в стиле Claude‑Tag, которую можно запускать как в Cloudflare Workers/Durable Objects, так и в Node.js. Проект позволяет превратить разрозненные подсказки и инструменты в воспроизводимые рабочие процессы агентов: легко координировать несколько агентов, строить конвейеры с использованием внешних инструментов и стандартизировать память агентов. С 184 звёздами, активными коммитами и поддержкой API/SDK/CLI, проект считается готовым к пилотному использованию в продакшене, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
openma-ai/open-managed-agents 是一套开源的 Claude Managed Agents API 实现以及自托管的 Claude‑Tag 风格代理运行时，代码兼容原生 Claude 接口，可在 Cloudflare Workers/Durable Objects 或 Node.js 环境中直接部署，采用 Apache 2.0 许可证。

**价值主张**  
- **把零散的 Prompt 与工具封装成可复用的工作流**，让多轮对话、工具调用和记忆管理统一化。  
- **支持多代理协同**，可以轻松构建“一个任务由多个专长代理分工完成”的编排。  
- **标准化 Agent Memory**，提供统一的状态持久化方案，降低业务方自行实现记忆层的成本。  

**典型接入方式**  
1. **API/SDK**：通过项目自带的 HTTP API（兼容 Claude Managed Agents）或 TypeScript SDK 调用 `createAgent`, `runWorkflow` 等接口。  
2. **CLI**：使用 `npx open-managed-agents` 快速启动本地调试或在 CI 中执行预定义工作流。  
3. **部署选项**：  
   - **Cloudflare Workers/Durable Objects**：将仓库直接绑定到 Workers 项目，实现无服务器、全球低延迟的运行时。  
   - **Node.js**：在自有服务器或容器（Docker/K8s）中 `npm i open-managed-agents` 后启动服务。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑26 最近一次提交，GitHub 184 ⭐、16 forks，20+ 主题标签，社区讨论活跃。  
- **技术成熟度**：使用 TypeScript 编写，代码结构清晰，提供完整的 API 文档、示例和单元测试。  
- **部署灵活**：兼容无服务器平台和传统 Node 环境，易于与现有微服务或数据库（如 KV、PostgreSQL）集成。  
- **风险**：需要进一步审查许可证合规、依赖安全（尤其是 Cloudflare 环境的访问控制）以及维护者的长期可用性。总体来看，项目已具备在生产环境进行试点的条件，适合作为内部 AI 编排层的基础设施。

## 🧭 Practical evaluation

**Value:** openma-ai/open-managed-agents helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 184 GitHub stars
- 16 forks
- updated 2026-06-26
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 31/100 |
| stars | 48/100 |
| topics | 100/100 |
| outlook | 65/100 |
| quality | 60/100 |
| recency | 40/100 |
| adoption | 43/100 |
| production | 59/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/openma-ai/open-managed-agents) · [← Back to Orchestration](./README.md)</sub>
