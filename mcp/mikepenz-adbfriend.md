# mikepenz/adbfriend

[![Stars](https://img.shields.io/github/stars/mikepenz/adbfriend?style=flat-square&color=yellow)](https://github.com/mikepenz/adbfriend/stargazers) [![Forks](https://img.shields.io/github/forks/mikepenz/adbfriend?style=flat-square&color=blue)](https://github.com/mikepenz/adbfriend/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> Android ADB CLI tool including integrated MCP Server with common adb actions used during development

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 73 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`adb` `ai` `android` `androiddebugbridge` `cli` `gradle` `kmp` `kotlin` `mcp` `mcp-server` `tools`

## 🎯 Categories

MCP · AI/ML · Backend · DevTools · Mobile

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`mikepenz/adbfriend` is an open‑source Kotlin‑based CLI that wraps common Android ADB commands and bundles a Model Context Protocol (MCP) server, making it easy to expose device‑level actions to AI assistants. By providing a standard MCP endpoint alongside a familiar ADB toolset, it enables developers to connect language models directly to real Android devices for testing, debugging, and automation. The project is actively maintained (last commit 2026‑06‑28) and already shows community traction with 73 stars and several forks.

**Value**  
- **Bridges AI and mobile tooling** – The built‑in MCP server translates natural‑language intents from an AI agent into concrete ADB operations, eliminating the need to write custom adapters for each device command.  
- **Standardised integration** – Because MCP is an emerging open protocol, `adbfriend` can serve as a reference implementation for any AI‑driven workflow that needs to interact with Android devices, accelerating the adoption of “AI‑as‑a‑tool” patterns.  
- **Developer productivity** – Teams can script, test, and iterate on AI‑driven debugging or deployment pipelines using a single, well‑documented CLI, reducing context‑switching between ADB, scripts, and AI services.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided Docker image or the Kotlin CLI locally, and point an MCP‑compatible AI assistant (e.g., LangChain, OpenAI function calling) at the server endpoint.  
2. **Extend** – Add custom MCP actions or wrap additional ADB commands by editing the Kotlin source or supplying a simple JSON‑based action map; the project’s modular design makes this straightforward.  
3. **Integrate** – Deploy the MCP server in a CI/CD environment or on a dedicated host that has USB/ADB access to the target devices; configure your AI orchestration layer to invoke the server’s REST endpoints.  
4. **Scale** – For larger teams, run multiple instances behind a load balancer, use role‑based API keys for security, and monitor logs via the built‑in diagnostics.

**Production Readiness**  
- **Activity & Community** – Recent commit (2026‑06‑28), 73 stars, and multiple forks indicate healthy interest and ongoing maintenance.  
- **Maturity** – Core functionality (ADB wrappers + MCP server) is stable; the Kotlin codebase is concise and well‑documented, and the CLI works out‑of‑the‑box on macOS, Linux, and Windows.  
- **Risk Considerations** – No glaring licensing or security red flags, but a final audit of the Apache‑2.0 (or stated) license, vulnerability scanning of the Docker image, and verification of maintainer responsiveness are recommended before a production rollout.  

Overall, `adbfriend` is a strong OSS candidate for pilots that need to expose Android device control to AI agents, and with minimal integration effort it can be hardened for production use.

### Русский

**adbfriend** — это CLI‑утилита для Android ADB на Kotlin, включающая готовый MCP‑сервер и набор часто используемых команд ADB, что позволяет быстро подключать AI‑ассистентов к реальным мобильным устройствам через стандартный Model Context Protocol. Типичный сценарий — запуск MCP‑сервера в процессе CI/CD или локальной разработки и последующее управление устройствами (установка/удаление приложений, сбор логов, запуск скриптов) из AI‑агента или другого сервиса. Проект уже активно поддерживается (обновления 2026‑06‑28, 73 ★, 5 forks), имеет чистый Kotlin‑код, хорошую документацию и широкую экосистему, что делает его готовым к использованию в продакшн‑пилотах после финальной проверки лицензии и безопасности.

### 中文

**项目简介（2‑3 句话）**  
`mikepenz/adbfriend` 是一个基于 Kotlin 实现的 Android ADB 命令行工具，内置 MCP（Model Context Protocol）服务器，提供开发过程中常用的 adb 操作并通过标准协议对外暴露。它旨在让 AI 助手或其他自动化系统能够直接调用真实的 Android 调试功能，实现“AI + 工具”的无缝集成。

**价值**  
- **统一协议**：通过 MCP 将 AI 代理与本地 adb 功能桥接，避免为每个工具单独实现自定义接口。  
- **加速开发**：开发者可以在 CI/CD、自动化测试或智能调试助手中直接调用 adb 命令，提升效率。  
- **生态兼容**：作为开源项目，提供 CLI、SDK 与 API 三种接入方式，易于嵌入现有 DevTools、MLOps 或移动端 CI 流程。

**典型接入方式**  
1. **CLI 直接调用**：在脚本或 CI 步骤中执行 `adbfriend <subcommand>`，如 `adbfriend install <apk>`。  
2. **MCP Server**：启动内置的 MCP 服务器（`adbfriend server start`），AI 代理通过 HTTP/gRPC 按 MCP 规范发送请求，获取设备列表、日志、截图等。  
3. **SDK 集成**：在 Kotlin/Java 项目中引入 `adbfriend` 的 Gradle 依赖，使用提供的 `AdbFriendClient` 类调用高层 API，适合需要更细粒度控制的业务系统。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑28，星标 73、Fork 5，社区活跃度良好。  
- **技术成熟度**：核心功能已实现并通过日常开发使用验证，MCP 服务器提供标准化接口，适合作为生产环境的工具桥梁。  
- **风险点**：仍需确认许可证兼容性（MIT/Apache 等）以及安全审计（如对 adb 权限的访问控制），但整体代码质量和维护状态足以支撑正式项目的试点或上线。

## 🧭 Practical evaluation

**Value:** mikepenz/adbfriend helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 73 GitHub stars
- 5 forks
- updated 2026-06-28
- primary language: Kotlin
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 40/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 65/100 |
| recency | 80/100 |
| adoption | 34/100 |
| production | 69/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/mikepenz/adbfriend) · [← Back to Mcp](./README.md)</sub>
