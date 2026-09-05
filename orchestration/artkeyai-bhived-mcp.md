# ArtKeyAi/bhived-mcp

[![Stars](https://img.shields.io/github/stars/ArtKeyAi/bhived-mcp?style=flat-square&color=yellow)](https://github.com/ArtKeyAi/bhived-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/ArtKeyAi/bhived-mcp?style=flat-square&color=blue)](https://github.com/ArtKeyAi/bhived-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> bhived is an MCP server that gives AI agents shared memory, skills, and tool discovery.   install once, works in Claude Code, Cursor, and 15+ other agents.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 33 |
| 🍴 **Forks** | 3 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-memory` `agent-memory-system` `ai-agent` `ai-agents` `ai-memory` `ai-skill` `mcp` `mcp-server` `model-context-protocol`

## 🎯 Categories

Orchestration · MCP · AI/ML · Backend

## 📝 Summary

### English

**Project Summary**

bhived is an open-source MCP server that enables AI agents to share memory, skills, and tool discovery, allowing for seamless integration with various agents such as Claude Code, Cursor, and 15+ others. This project helps turn isolated prompts and tools into repeatable agent workflows, making it easier to coordinate multi-agent workflows, add tool-use pipelines, and standardize agent memory. With its straightforward evaluation process, bhived is a useful tool for prototypes or internal workflows.

**Value Proposition**

The primary value of bhived lies in its ability to facilitate collaboration among AI agents, promoting efficiency and consistency in workflows. By providing shared memory, skills, and tool discovery, this MCP server enables the creation of repeatable agent workflows, which can be leveraged to streamline tasks and reduce errors.

**Practical Adoption Path**

To adopt bhived, developers can follow these steps:

1. Evaluate the project's documentation and API/SDK/CLI implementation to understand its functionality and integration process.
2. Choose the desired AI agents to integrate with bhived, such as Claude Code, Cursor, or others.
3. Set up the bhived MCP server and configure it to share memory, skills, and tool discovery with the chosen agents.
4. Test and refine the integration to ensure seamless workflow

### Русский

**ArtKeyAi/bhived-mcp** — это сервер‑MCP, предоставляющий AI‑агентам общую память, набор навыков и механизм автоматического обнаружения инструментов; после единой установки он сразу работает в Claude Code, Cursor и более чем 15‑ти других агентных средах. Типичный сценарий — построение повторяемых многопоточных рабочих процессов, где несколько агентов совместно используют инструменты и общую память (например, координация сложных пайплайнов или стандартизация доступа к внешним сервисам). Проект находится на среднем уровне готовности к production: подходит для прототипов и внутренних систем, но перед развёртыванием стоит проверить зависимости, лицензирование и безопасность.

### 中文

**项目简介**  
ArtKeyAi/bhived-mcp 是一个基于 TypeScript 的 MCP（Memory‑Control‑Protocol）服务器，为 Claude Code、Cursor 以及 15+ 其他 AI 代理提供共享记忆、技能库和工具发现能力。一次部署即可让不同的 AI 代理在同一记忆空间中协同工作，轻松构建可复用的多代理工作流。

**价值**  
- **统一记忆**：将孤立的 Prompt 与工具统一到共享记忆中，避免信息碎片化。  
- **技能复用**：通过统一的 Skill/Tool 注册中心，让多个代理直接调用已有能力，提升开发效率。  
- **工作流标准化**：把多代理协作、工具链调用抽象为可配置的流程，便于在原型和内部项目中快速迭代。

**典型接入方式**  
1. **API/SDK**：项目提供 RESTful API 与 TypeScript SDK，业务方只需在代码中引入 `bhived-mcp` 包并配置服务器地址即可。  
2. **CLI**：通过自带的命令行工具快速启动本地或云端实例，适合快速验证。  
3. **语言/主题元数据**：项目在 `package.json` 中声明了 `language: TypeScript` 与多个主题标签，便于在 CI/CD 流水线或插件系统中自动发现并集成。  

**生产可用性**  
- **成熟度**：当前得分 72/100，适合作为原型或内部工作流的核心组件。  
- **依赖与维护**：依赖链相对简单（Node.js、Express），但在投入生产前建议审查其安全漏洞、许可证兼容性以及是否有活跃维护者。  
- **可扩展性**：支持水平扩容的无状态 API 设计，配合容器化部署（Docker）即可在 Kubernetes 等平台上实现高可用。  

总体而言，bhived-mcp 能显著降低多代理协同开发的门槛，适合在实验室或内部业务中先行验证，经过安全与运维审查后即可推进到生产环境。

## 🧭 Practical evaluation

**Value:** ArtKeyAi/bhived-mcp helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 33 GitHub stars
- 3 forks
- updated 2026-06-29
- primary language: TypeScript
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 15/100 |
| stars | 33/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 28/100 |
| production | 68/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/ArtKeyAi/bhived-mcp) · [← Back to Orchestration](./README.md)</sub>
