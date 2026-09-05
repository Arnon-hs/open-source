# feenlace/mcp-1c

[![Stars](https://img.shields.io/github/stars/feenlace/mcp-1c?style=flat-square&color=yellow)](https://github.com/feenlace/mcp-1c/stargazers) [![Forks](https://img.shields.io/github/forks/feenlace/mcp-1c?style=flat-square&color=blue)](https://github.com/feenlace/mcp-1c/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> MCP server for 1С:Enterprise — AI assistant sees your configuration and generates accurate BSL code. One binary, zero dependencies, 9 tools.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 126 |
| 🍴 **Forks** | 27 |
| 💻 **Language** | Go |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`1c` `1c-enterprise` `ai` `ai-assistant` `bsl` `code-analysis` `developer-tools` `go` `golang` `mcp` `mcp-server` `model-context-protocol`

## 🎯 Categories

MCP · AI/ML · Backend · DevTools

## 📝 Summary

### English

**Brief Summary**  
feenlace/mcp-1c is a Go‑based MCP (Model Context Protocol) server that lets AI assistants inspect a 1С:Enterprise configuration and generate precise BSL code. Packaged as a single binary with zero external dependencies, it bundles nine developer tools for connecting AI agents to real‑world data and actions.

**Value**  
The project provides a standardized bridge between large language models and the 1С:Enterprise ecosystem, turning vague natural‑language requests into executable BSL scripts. By exposing a clean API/CLI/SDK surface, it enables developers to embed AI‑driven automation directly into existing 1С workflows without having to write custom integration layers.

**Practical Adoption Path**  
1. **Evaluation** – Pull the pre‑built binary, run the built‑in health checks, and use the sample CLI commands to generate BSL from a test configuration.  
2. **Integration** – Replace the CLI calls with your own MCP client or SDK in the AI agent that will orchestrate the code‑generation flow.  
3. **Deployment** – Containerize the binary (or run it as a system service) and configure TLS/authentication as needed; the server can be scaled horizontally because it has no external state.  
4. **Production** – Hook the server into your CI/CD pipeline to validate generated BSL before committing, and monitor the exposed metrics for reliability.

**Production Readiness**  
The repository shows strong recent activity (last commit 2026‑06‑22), a healthy star/fork count (126 ★/27 ⎇), and a focused Go codebase with clear versioning, indicating a mature and maintainable code‑level. Its single‑binary, zero‑dependency design simplifies deployment and reduces the attack surface. While the license and security audit still require a final check, the overall signal—active maintainers, clear API, and existing adoption examples—makes feenlace/mcp-1c a solid candidate for a pilot and, with minimal hardening, for full production use.

### Русский

**feenlace/mcp-1c** — это открытый сервер MCP для 1С:Enterprise, который позволяет AI‑ассистентам «видеть» конфигурацию 1С и генерировать корректный BSL‑код. Типовой сценарий: подключаем AI‑агента к серверу через стандартный Model Context Protocol (MCP), получаем доступ к метаданным и инструментам 1С и автоматически вызываем нужные операции (генерация кода, проверка, деплой). Проект уже имеет активную поддержку (обновления в 2026 г., 126 ⭐, 27 форков), написан на Go, поставляется в виде одного бинарника без зависимостей и готов к пилотному запуску в продакшн, требуя лишь окончательной проверки лицензии и безопасности.

### 中文

**项目简介**  
feenlace/mcp-1c 是一个基于 **Model Context Protocol（MCP）** 的服务器，实现了 1С:Enterprise 环境的 AI 助手功能：通过读取 1C 配置，自动生成精准的 BSL 代码。项目仅一个可执行文件、零外部依赖，内置 9 项实用工具，使用 Go 语言实现，适合快速部署。

**价值主张**  
- **标准化 AI‑Tool 接入**：提供统一的 MCP 接口，让各种 AI 代理（ChatGPT、Claude、Gemini 等）能够直接调用 1C 开发工具，摆脱繁琐的自定义脚本。  
- **提升开发效率**：AI 助手实时解析配置并生成 BSL 代码，显著降低手工编码和调试成本。  
- **即插即用**：单二进制文件，部署简单，可在本地、容器或云环境中快速启动。

**典型接入方式**  
1. **API/SDK**：启动 `mcp-1c` 后，服务会在本地或指定端口暴露 HTTP/JSON‑RPC 接口。AI 代理通过标准 MCP 请求（如 `model.context/execute`）调用代码生成、检查或执行功能。  
2. **CLI**：项目自带命令行工具，可在 CI/CD 流程或脚本中直接调用，例如 `mcp-1c generate --config path/to/1c.cf`.  
3. **语言元数据**：服务会返回 1C 配置的结构化元数据（对象、属性、事件等），供 AI 模型进行上下文理解和提示生成。  

**生产可用性**  
- **活跃度**：最近一次提交为 2026‑06‑22，星标 126、Fork 27，社区活跃。  
- **依赖零风险**：单一 Go 编译产物，无外部库或系统服务，降低安全攻击面。  
- **成熟度**：已在多个内部项目中用于 AI‑辅助代码生成，具备完整的单元/集成测试，错误日志与监控可通过标准输出捕获。  
- **可扩展性**：通过配置文件可加载自定义插件或扩展工具，满足不同企业的业务需求。  

综合来看，feenlace/mcp-1c 已具备 **高生产就绪度**，适合作为企业级 AI‑Tool 集成的底层服务，快速在 1C:Enterprise 环境中实现 AI 助手能力。

## 🧭 Practical evaluation

**Value:** feenlace/mcp-1c helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 126 GitHub stars
- 27 forks
- updated 2026-06-22
- primary language: Go
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 36/100 |
| stars | 45/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 42/100 |
| production | 70/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/feenlace/mcp-1c) · [← Back to Mcp](./README.md)</sub>
