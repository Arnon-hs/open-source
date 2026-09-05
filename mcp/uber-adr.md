# uber/ADR

[![Stars](https://img.shields.io/github/stars/uber/ADR?style=flat-square&color=yellow)](https://github.com/uber/ADR/stargazers) [![Forks](https://img.shields.io/github/forks/uber/ADR?style=flat-square&color=blue)](https://github.com/uber/ADR/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> ADR secures enterprise AI agents through observability, security benchmarking, and threat detection. Deployed at Uber.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 22 |
| 🍴 **Forks** | 2 |
| 💻 **Language** | Python |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-security` `ai-agents` `ai-security` `benchmark` `claude` `claude-code` `codex` `cursor` `llm-security` `mcp` `model-context-protocol` `prompt-injection`

## 🎯 Categories

MCP · AI/ML · Observability · Security

## 📝 Summary

### English

**Project Summary:**
uber/ADR is an open-source project that secures enterprise AI agents through observability, security benchmarking, and threat detection. It enables the connection of AI assistants to real tools and data through a standard protocol, making it a valuable tool for organizations with AI and ML systems. By standardizing integrations, uber/ADR facilitates the deployment of AI agents in production environments.

**Value:**
The primary value proposition of uber/ADR lies in its ability to connect AI agents to real tools and data through a standard protocol, thereby streamlining the integration process and enhancing the overall security and observability of AI systems.

**Practical Adoption Path:**
To adopt uber/ADR, organizations can start by connecting their AI agents to tools using the standard protocol. This can be done by deploying the Model Context Protocol servers and standardizing integrations. While the project appears straightforward to evaluate, it's essential to conduct a thorough review of the license, security posture, and active maintainers before production.

**Production Readiness:**
uber/ADR has a medium production readiness score, indicating that it's suitable for prototypes or internal workflows but requires additional checks and maintenance before being deployed in production environments. This means that organizations can use the project for proof-of-concepts or internal testing, but

### Русский

Резюме проекта uber/ADR:

Проект uber/ADR обеспечивает безопасность корпоративных агентов AI через наблюдаемость, оценку безопасности и обнаружение угроз. Он помогает подключать AI-ассистентов к реальным инструментам и данным через стандартный протокол. Проект готов к внедрению в прототипах или внутренних потоках, но требует проверки зависимостей и поддержки до запуска в производстивном режиме.

### 中文

**项目简介**

uber/ADR 是一个开源项目，旨在通过可观察性、安全基准和威胁检测来保护企业级 AI 代理。它已经在 Uber 部署。

**价值**

uber/ADR 的价值在于，它帮助连接 AI 助手到真实的工具和数据通过一个标准协议。通过使用这个项目，可以让 AI 代理更好地与其他系统集成。

**典型接入方式**

uber/ADR 的接入方式包括：

1. 连接 AI 代理到工具：通过使用 Model Context Protocol（MCP），可以让 AI 代理与其他系统进行通信。
2. 部署 Model Context Protocol 服务器：通过部署 MCP 服务器，可以让 AI 代理与其他系统进行交互。
3. 标准化集成：通过使用 MCP，可以让 AI 代理与其他系统进行标准化的集成。

**生产可用性**

uber/ADR 的生产可用性为中等（Medium）。它适合用于原型或内部工作流程，需要在生产环境中进行依赖性和维护检查。

## 🧭 Practical evaluation

**Value:** uber/ADR helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 22 GitHub stars
- 2 forks
- updated 2026-07-31
- primary language: Python
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 12/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 69/100 |
| quality | 61/100 |
| recency | 80/100 |
| adoption | 24/100 |
| production | 67/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-07-31 · [View on GitHub](https://github.com/uber/ADR) · [← Back to Mcp](./README.md)</sub>
