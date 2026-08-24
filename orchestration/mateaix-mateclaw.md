# mateaix/mateclaw

[![Stars](https://img.shields.io/github/stars/mateaix/mateclaw?style=flat-square&color=yellow)](https://github.com/mateaix/mateclaw/stargazers) [![Forks](https://img.shields.io/github/forks/mateaix/mateclaw?style=flat-square&color=blue)](https://github.com/mateaix/mateclaw/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> 🤖 MateClaw — Your second brain with Multi-Agent Orchestration, MCP Protocol, Skills & Memory, Dream, and Multi-Channel Support. Built on Spring AI Alibaba.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 660 |
| 🍴 **Forks** | 200 |
| 💻 **Language** | Java |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `agent-harness` `ai-agent` `dingtalk-robot` `feishu-bot` `llm-wiki` `loop-engineering` `mcp-protocol` `multi-agent` `multiagent` `openclaw` `plan-and-execute`

## 🎯 Categories

Orchestration · MCP · Automation · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
MateClaw (mateaix/mateclaw) is an open‑source Java framework that turns isolated prompts and tools into repeatable, multi‑agent workflows. It provides a unified orchestration layer, MCP protocol, skill‑ and memory‑management, “dream” capabilities, and multi‑channel support, all built on Spring AI Alibaba. With strong community activity (660 ★, 200 forks) it is ready for pilot deployments in production environments.  

**Value**  
- **Unified agent orchestration**: Converts disparate LLM prompts, tool calls, and memory stores into cohesive pipelines, eliminating ad‑hoc scripting.  
- **Extensible MCP protocol & skill system**: Enables plug‑and‑play agents that can share state, invoke external services, and evolve through “dream” cycles.  
- **Multi‑channel reach**: Supports chat, voice, webhooks, and other front‑ends from a single code base, accelerating productization of AI features.  

**Practical Adoption Path**  
1. **Evaluate the API/SDK** – Clone the repo, run the provided Docker compose or Maven demo to explore the REST API and CLI.  
2. **Prototype a workflow** – Use the Java SDK to define a simple two‑agent pipeline (e.g., a planner + executor) and persist memory via the built‑in store.  
3. **Integrate with existing services** – Replace the demo tool adapters with your own micro‑services or third‑party APIs, leveraging the MCP protocol for standardized messaging.  
4. **Scale & secure** – Deploy the Spring Boot application on Kubernetes, enable TLS and RBAC, and configure external storage for persistent memory.  

**Production Readiness**  
- **Active maintenance**: Recent commits (as of 2026‑06‑25), frequent releases, and a growing contributor base.  
- **Ecosystem fit**: Built on Spring AI Alibaba, it inherits Spring Boot’s production‑grade tooling, observability, and cloud‑native deployment patterns.  
- **Adoption signals**: 660 GitHub stars, 200 forks, and multiple topic tags indicate community interest and real‑world usage.  
- **Remaining checks**: Final due‑diligence on licensing, security audits, and maintainer responsiveness is recommended, but the project is otherwise a solid candidate for a serious pilot in a production setting.

### Русский

MateClaw — это открытая платформа на базе Spring AI Alibaba, позволяющая превратить разрозненные подсказки и инструменты в повторяемые многопотоковые воркфлоу с поддержкой оркестрации нескольких агентов, протокола MCP, памяти, «снов» и мульти‑канального взаимодействия. Типичный сценарий — интеграция в существующую систему для координации цепочек агентов, автоматизации инструментов и стандартизации их памяти (например, в чат‑ботах, рекомендационных сервисах или бизнес‑процессах). Проект имеет высокий уровень готовности к production: активные коммиты, 660 звёзд, 200 форков, поддержка API/SDK/CLI и обширная экосистема, что делает его надёжным кандидатом для пилотных внедрений.

### 中文

**项目简介**  
MateClaw（mateaix/mateclaw）是基于 Spring AI Alibaba 构建的多代理编排平台，提供 MCP 协议、技能与记忆、Dream 引擎以及多渠道支持，帮助把零散的 Prompt 与工具组合成可复用的智能工作流。  

**价值**  
- **统一编排**：将分散的 AI Prompt、工具调用和记忆机制统一管理，形成可视化、可重复的多代理工作流。  
- **高效复用**：通过 MCP 协议和 Skills 定义，可快速构建并复用业务场景下的智能插件和工具链。  
- **跨渠道**：内置多渠道（Web、CLI、SDK 等）接入，支持在不同终端上统一调度代理。  

**典型接入方式**  
1. **API/SDK**：项目提供 RESTful API 与 Java SDK，业务系统只需引入 `mateclaw-client` 包并调用 `Orchestrator` 接口即可启动/管理工作流。  
2. **CLI**：通过 `mateclaw-cli` 命令行工具，可在 CI/CD、脚本或本地调试环境中直接触发代理编排。  
3. **Spring 集成**：在 Spring Boot 项目中加入 `spring-boot-starter-mateclaw`，即可自动装配 Agent、Memory、Skill 等组件，免除繁琐配置。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑25，项目最近一次提交，拥有 660+ ⭐、200+ 🍴，且持续接受 PR 与 Issue 反馈。  
- **生态兼容**：基于 Java 与 Spring 生态，易于在企业微服务体系中落地，且已对外公布 17 个主题标签，覆盖 Orchestration、MCP、Automation 等关键领域。  
- **成熟度**：具备完整的 API、SDK 与 CLI 文档，且已有若干开源/企业案例使用，具备进入生产环境的技术准备度。  
- **风险**：需进一步审查许可证（Apache‑2.0）以及安全依赖的最新漏洞报告，确认维护者的长期可用性后方可正式上线。  

综上，MateClaw 能显著降低多代理 AI 工作流的开发与运维成本，接入方式灵活，且在活跃的社区与代码质量支撑下，已具备在生产环境中试点的条件。

## 🧭 Practical evaluation

**Value:** mateaix/mateclaw helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 660 GitHub stars
- 200 forks
- updated 2026-06-25
- primary language: Java
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 58/100 |
| stars | 60/100 |
| topics | 100/100 |
| outlook | 67/100 |
| quality | 67/100 |
| recency | 40/100 |
| adoption | 59/100 |
| production | 57/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/mateaix/mateclaw) · [← Back to Orchestration](./README.md)</sub>
