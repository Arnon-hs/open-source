# pouriamrt/claude-mesh

[![Stars](https://img.shields.io/github/stars/pouriamrt/claude-mesh?style=flat-square&color=yellow)](https://github.com/pouriamrt/claude-mesh/stargazers) [![Forks](https://img.shields.io/github/forks/pouriamrt/claude-mesh?style=flat-square&color=blue)](https://github.com/pouriamrt/claude-mesh/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> Networked Claude-to-Claude messaging over HTTP + MCP channels — DM, broadcast, thread, and permission-relay between Claude Code instances via a self-hosted relay + MCP channel bridge.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 23 |
| 🍴 **Forks** | — |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-07-25 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anthropic` `claude` `claude-code` `hono` `mcp` `mesh-networking` `messaging` `model-context-protocol` `multi-agent` `self-hosted` `sse` `typescript`

## 🎯 Categories

Orchestration · MCP · AI/ML

## 📝 Summary

### English

pouriamrt/claude-mesh enables isolated Claude Code instances to communicate via HTTP and MCP channels, supporting direct messages, broadcasts, threaded conversations, and permission‑relayed interactions so agents can coordinate multi‑step workflows, share tool‑use pipelines, and maintain a common memory. Adoption is straightforward—self‑host the relay, bridge MCP channels, and use the provided API/SDK/CLI to wire agents together—making it ideal for prototyping or internal automation. While the project shows solid signals (TypeScript, regular updates, clear integration points), its production readiness is medium; teams should review licensing, security posture, and maintainer activity before deploying at scale.

### Русский

pouriamrt/claude-mesh позволяет объединять отдельные экземпляры Claude Code в сеть, обеспечивая обмен сообщениями через HTTP и MCP‑каналы (личные сообщения, рассылки, потоки и передачу прав), что превращает разрозненные запросы и инструменты в повторяемые многоагентные рабочие процессы. Типичный сценарий — развернуть самодостаточный релей‑сервер и подключить к нему несколько инстансов Claude Code для координации цепочек вызовов инструментов, обмена контекстом и построения стандартных пайплайнов агентов. Проект находится на среднем уровне готовности к production: подходит для прототипов и внутренних workflows, но перед промышленным использованием требуется проверка зависимостей, лицензии и уровня поддержки мейнтейнеров.

### 中文

pouria mrt/claude‑mesh 通过自托管的 HTTP+MCP 中继实现 Claude 实例之间的点对点、广播、线程和权限转发消息，帮助将孤立的 Prompt 和工具转化为可重复的多代理工作流。典型接入方式是部署其 relay 服务并通过提供的 API/SDK/CLI（TypeScript）将本地或云端的 Claude Code 实例连接到 mesh 中。该项目目前处于中等成熟度，适用于原型或内部工作流，但在投入生产前仍需检查依赖、维护频率以及许可和安全情况。

## 🧭 Practical evaluation

**Value:** pouriamrt/claude-mesh helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 23 GitHub stars
- updated 2026-07-25
- primary language: TypeScript
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 65/100 |
| recency | 100/100 |
| adoption | 21/100 |
| production | 73/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-25 · [View on GitHub](https://github.com/pouriamrt/claude-mesh) · [← Back to Orchestration](./README.md)</sub>
