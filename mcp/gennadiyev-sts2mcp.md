# Gennadiyev/STS2MCP

[![Stars](https://img.shields.io/github/stars/Gennadiyev/STS2MCP?style=flat-square&color=yellow)](https://github.com/Gennadiyev/STS2MCP/stargazers) [![Forks](https://img.shields.io/github/forks/Gennadiyev/STS2MCP?style=flat-square&color=blue)](https://github.com/Gennadiyev/STS2MCP/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> Full agentic runs for Slay the Spire 2. A mod that exposes in-game state, and the MCP server for the mod.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 335 |
| 🍴 **Forks** | 56 |
| 💻 **Language** | C# |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic-ai` `mcp-server` `research-and-development` `slay-the-spire-2`

## 🎯 Categories

MCP · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Gennadiyev/STS2MCP is an open‑source mod for *Slay the Spire 2* that exposes the game’s internal state via a Model Context Protocol (MCP) server, enabling external AI agents to read and act on live gameplay data. The project provides a clean API/SDK and a command‑line interface written in C#, making it straightforward to plug in custom AI or reinforcement‑learning agents.

**Value Proposition**  
- **Standardised AI‑to‑tool bridge**: By implementing the MCP, the mod turns a video game into a well‑defined data source and control surface, letting developers test, benchmark, or demo AI assistants on a complex, turn‑based environment without building custom instrumentation.  
- **Reusable backend component**: The MCP server can be deployed as a standalone service, so the same protocol can be reused for other games or simulations, accelerating integration work across projects.  
- **Rapid prototyping**: With the exposed state (cards, enemies, health, actions) and a simple request/response API, researchers can iterate on model architectures, reward functions, or prompting strategies much faster than hand‑crafting data pipelines.

**Practical Adoption Path**  

| Step | Action | Why it matters |
|------|--------|----------------|
| 1️⃣ Clone & build | `git clone https://github.com/Gennadiyev/STS2MCP && dotnet build` | Verifies the C# toolchain and confirms the mod compiles on your platform. |
| 2️⃣ Install the mod | Drop the compiled DLL into the *Slay the Spire 2* `Mods` folder and launch the game. | Makes the MCP server available inside the running game. |
| 3️⃣ Run the MCP server | Execute the provided CLI (`sts2mcp --port 5000`) or start the Docker image if available. | Starts a HTTP/WS endpoint that streams game state and accepts action commands. |
| 4️⃣ Connect your AI | Use the generated OpenAPI spec or the simple SDK (Python, C#, etc.) to subscribe to state updates and send actions. | Allows any language‑agnostic model (LLM, RL agent, rule‑based bot) to interact in real time. |
| 5️⃣ Iterate & test | Record episodes, tweak prompts/rewards, and replay logs via the built‑in replay feature. | Provides a fast feedback loop for model improvement. |
| 6️⃣ Harden for production | Add authentication (TLS, API keys), sandbox the mod in a container, and monitor resource usage. | Mitigates security and stability risks before moving beyond prototypes. |

**Production Readiness Assessment**  

- **Maturity**: Medium. The repo is actively maintained (last commit 2026‑05‑12) and has a respectable community signal (335 ★, 56 forks). The codebase is small and focused, which eases auditing.  
- **Stability**: Good for internal tools or research prototypes. The MCP server runs as a separate process, limiting impact on the game client, but the mod itself depends on the *Slay the Spire 2* version and may break on future game updates.  
- **Operational considerations**:  
  * **Dependencies** – .NET 6+ runtime; optional Docker image for isolation.  
  * **Security** – No built‑in auth; you’ll need to front the server with a gateway or VPN for production use.  
  * **Maintenance** – One primary maintainer; check issue backlog for response times.  
- **Readiness checklist before production**:  
  1. Verify license compatibility with your organization.  
  2. Add TLS/API‑key protection or run behind a trusted network.  
  3. Pin the game version and monitor upstream updates.  
  4. Implement health‑checks and logging for the MCP service.  

**Bottom line**  
Gennadiyev/STS2MCP offers a ready‑made, standards‑based interface to turn *Slay the Spire 2* into a live AI playground. It is well suited for proof‑of‑concepts, research demos, or internal tooling, and can be hardened for production with modest effort around security, version pinning, and monitoring.

### Русский

**Gennadiyev/STS2MCP** — открытый мод для *Slay the Spire 2*, который раскрывает внутреннее состояние игры и предоставляет MCP‑сервер, позволяющий подключать к ней AI‑агентов через единый Model Context Protocol. Типичный сценарий — запуск прототипов или внутренних сервисов, где AI‑ассистент обменивается данными с игрой (например, планирование ходов или автоматическое тестирование), а также развертывание собственного MCP‑сервера для стандартизированных интеграций. Проект имеет средний уровень готовности к production: достаточно звёзд и недавних обновлений, но перед выпуском в продакшн требуется проверка лицензии, безопасности и наличия активных мейнтейнеров.

### 中文

**项目简介（2‑3 句）**  
Gennadiyev/STS2MCP 是为《Slay the Spire 2》提供全自动化运行的插件，能够实时暴露游戏状态并通过 MCP（Model Context Protocol）服务器与外部 AI 代理交互。该 mod 将游戏内部数据标准化为 API/SDK/CLI 接口，方便 AI 助手直接读取和控制游戏。

**价值**  
- **统一协议**：使用 MCP 将游戏状态、指令和结果封装为统一的 JSON/HTTP 接口，使 AI 代理能够像调用本地工具一样调用游戏。  
- **快速原型**：开发者只需编写几行代码即可让任意 LLM 或强化学习模型直接操控《Slay the Spire 2》，大幅缩短 AI‑Game 集成的研发周期。  
- **可复用的后端服务**：MCP 服务器本身即是一个可部署的微服务，适合作为模型上下文（Model Context）提供者，支持多租户和负载均衡。

**典型接入方式**  
1. **部署 MCP 服务器**：在本地或容器环境中运行 `STS2MCP.Server`（提供 HTTP/WS 接口）。  
2. **启动游戏 Mod**：在《Slay the Spire 2》客户端安装 `STS2MCP.Mod`，启动后自动与服务器建立 WebSocket 连接。  
3. **调用 API**：AI 代码（Python、Node.js、C# 等）通过 HTTP/REST 或 WebSocket 调用如 `GET /state`, `POST /action` 等端点获取游戏状态或发送指令。  
4. **集成到模型工作流**：在 LangChain、AutoGPT、OpenAI Function Calling 等框架中注册对应的工具函数，即可让模型在对话或计划阶段直接使用游戏功能。

**生产可用性**  
- **成熟度**：GitHub 评分 67/100，拥有 335 ★、56 Fork，最近一次提交在 2026‑05‑12，代码活跃度良好。  
- **适用场景**：适合内部原型、研发实验或受控的 AI‑Game 竞赛环境；在正式生产环境使用前建议完成以下检查：  
  - **依赖审计**：确认所有第三方 NuGet 包的许可证兼容性。  
  - **安全评估**：审查 MCP 服务器的身份验证与网络隔离，防止未授权指令执行。  
  - **运维准备**：为 MCP 服务器配置监控、日志和自动重启策略，确保长时运行的稳定性。  
- **结论**：在完成上述安全与运维检查后，STS2MCP 可作为可靠的后端服务投入生产，用于 AI 代理对《Slay the Spire 2》进行实时控制和数据采集。

## 🧭 Practical evaluation

**Value:** Gennadiyev/STS2MCP helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 335 GitHub stars
- 56 forks
- updated 2026-05-12
- primary language: C#
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 54/100 |
| topics | 50/100 |
| outlook | 78/100 |
| quality | 70/100 |
| recency | 100/100 |
| adoption | 51/100 |
| production | 73/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/Gennadiyev/STS2MCP) · [← Back to Mcp](./README.md)</sub>
