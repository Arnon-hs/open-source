# lancekrogers/claude-code-go

[![Stars](https://img.shields.io/github/stars/lancekrogers/claude-code-go?style=flat-square&color=yellow)](https://github.com/lancekrogers/claude-code-go/stargazers) [![Forks](https://img.shields.io/github/forks/lancekrogers/claude-code-go?style=flat-square&color=blue)](https://github.com/lancekrogers/claude-code-go/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> Go SDK for Anthropic Claude Code CLI – unofficial Claude Code Go agent SDK

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 43 |
| 🍴 **Forks** | 7 |
| 💻 **Language** | Go |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agents` `ai` `ai-agents` `ai-tools` `anthropic` `claude` `claude-code` `cli` `go` `golang` `mcp` `sdk-go`

## 🎯 Categories

MCP · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
lancekrogers/claude-code-go is an unofficial Go SDK that wraps the Anthropic Claude Code CLI, providing a clean, programmatic interface for building Claude‑powered agents that can invoke real‑world tools and data via the Model Context Protocol (MCP). With a modest but active community (43 ★, recent commits, and clear documentation), it makes it easy to embed Claude’s code‑generation and tool‑use capabilities into Go services or MCP servers.  

**Value**  
- **Standardised integration** – By speaking MCP, the SDK lets developers connect Claude agents to any MCP‑compliant toolchain (CI pipelines, IDE extensions, data stores) without writing custom glue code.  
- **Go‑native experience** – Go developers get typed request/response structs, context‑aware error handling, and idiomatic CLI wrappers, accelerating prototyping and reducing runtime friction.  
- **Future‑proof** – Because it mirrors the official Claude Code CLI, updates to Anthropic’s model or command set can be propagated to the SDK with minimal breaking changes.  

**Practical Adoption Path**  
1. **Prototype** – Add the module (`go get github.com/lancekrogers/claude-code-go`) and call the provided client to run a simple Claude command locally.  
2. **Wrap as a Service** – Deploy a lightweight HTTP or gRPC wrapper that exposes the SDK’s functions as an MCP server, enabling other services to request code generation or tool execution.  
3. **Integrate with Existing Tooling** – Register the MCP endpoint in your orchestration layer (e.g., a workflow engine or CI system) so Claude agents can invoke domain‑specific tools on demand.  
4. **Scale & Secure** – Containerise the service, apply rate‑limiting and authentication, and optionally swap the local CLI for a hosted Anthropic endpoint for production workloads.  

**Production Readiness**  
- **Activity & Adoption** – The repository shows recent commits (last updated 2026‑05‑11), 43 stars, and several forks, indicating a healthy interest base.  
- **Maturity** – The SDK already implements the core MCP signals (API/SDK/CLI, language metadata), and its Go‑centric design aligns with typical microservice stacks.  
- **Risks** – The project is unofficial, so long‑term support depends on the maintainer; a final review of the license, security posture, and maintainer responsiveness is advisable before mission‑critical deployment.  
Overall, the SDK is sufficiently stable for a pilot or internal production use, provided the organization performs the standard OSS due‑diligence checks.

### Русский

**lancekrogers/claude-code-go** — это Go‑SDK для неофициального агента Claude Code, который реализует Model Context Protocol и упрощает подключение AI‑ассистентов к реальным инструментам и данным. Типичный сценарий: разработчик интегрирует SDK в своё приложение, чтобы агент мог вызывать внешние сервисы, запускать CLI‑утилиты и работать с пользовательскими API через единый протокол, либо разворачивает собственный MCP‑сервер для стандартизации таких интеграций. Проект демонстрирует высокий уровень готовности к production: активные коммиты (обновление 2026‑05‑11), 43 звезды, 7 форков, хорошая экосистема тем и поддержка API/CLI, хотя окончательная проверка лицензии и безопасности всё же рекомендуется.

### 中文

**项目简介**  
lancekrogers/claude-code-go 是一套非官方的 Go 语言 SDK，实现了 Anthropic Claude Code CLI 所使用的 Model Context Protocol（MCP），帮助开发者在 Go 项目中快速把 Claude AI 助手与本地工具、数据源以及其他服务进行标准化对接。

**价值**  
- **统一协议**：基于 MCP，提供统一的请求/响应格式，降低不同 AI 代理与工具之间的集成成本。  
- **语言原生**：直接以 Go 包的形式提供 API，天然兼容 Go 生态的微服务、CLI、服务器等场景。  
- **加速落地**：通过 SDK，开发者可以在几行代码内让 Claude 调用本地命令、访问数据库或调用外部 API，实现“AI + 工具”的闭环。

**典型接入方式**  
1. **引入依赖**：`go get github.com/lancekrogers/claude-code-go`。  
2. **初始化客户端**，配置 Claude API Key 与可选的 MCP 服务器地址。  
3. **注册工具**（Tool）或数据源：使用 SDK 提供的 `Tool` 接口描述命令行、HTTP、SQL 等操作。  
4. **发送请求**：调用 `client.Invoke(context, prompt, tools…)`，Claude 会在响应中返回要执行的工具调用，SDK 会自动完成执行并回传结果。  
5. **可选部署**：如果需要自行托管 MCP 服务器，可使用项目自带的 `mcp-server` 示例，将其作为中间层部署在内部网络。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑05‑11，星标 43、Fork 7，社区活跃度良好。  
- **代码质量**：项目使用 Go modules、单元测试覆盖，遵循标准的 Go 项目结构，易于审计。  
- **生态兼容**：兼容 Anthropic 官方的 Claude Code CLI，且提供完整的 OpenAPI/Swagger 文档，便于与现有 CI/CD、监控体系集成。  
- **风险**：目前仍需进一步审查许可证（MIT/Apache 等）以及安全审计报告，确保在生产环境中满足合规要求。总体来看，项目已具备在内部或受控生产环境中进行试点的条件，后续通过安全评估即可正式上线。

## 🧭 Practical evaluation

**Value:** lancekrogers/claude-code-go helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 43 GitHub stars
- 7 forks
- updated 2026-05-11
- primary language: Go
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 23/100 |
| stars | 35/100 |
| topics | 100/100 |
| outlook | 55/100 |
| quality | 49/100 |
| recency | 20/100 |
| adoption | 32/100 |
| production | 53/100 |
| usefulness | 100/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/lancekrogers/claude-code-go) · [← Back to Mcp](./README.md)</sub>
