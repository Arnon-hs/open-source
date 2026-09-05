# yotsuda/PowerShell.MCP

[![Stars](https://img.shields.io/github/stars/yotsuda/PowerShell.MCP?style=flat-square&color=yellow)](https://github.com/yotsuda/PowerShell.MCP/stargazers) [![Forks](https://img.shields.io/github/forks/yotsuda/PowerShell.MCP?style=flat-square&color=blue)](https://github.com/yotsuda/PowerShell.MCP/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> The universal MCP server for Claude Code and other MCP-compatible clients. One installation gives AI access to 10,000+ PowerShell modules and any CLI tool. You and AI collaborate in the same console with full transparency. Supports Windows, Linux, and macOS.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 74 |
| 🍴 **Forks** | 7 |
| 💻 **Language** | C# |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `ai-integration` `mcp` `mcp-server` `powershell`

## 🎯 Categories

MCP · AI/ML · Backend

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
PowerShell.MCP is a universal Model‑Context‑Protocol (MCP) server that lets Claude Code and any MCP‑compatible AI client invoke over 10 000 PowerShell modules and arbitrary CLI tools from a shared console. It works on Windows, Linux and macOS, enabling a transparent, bidirectional collaboration between a human and an AI assistant. The project is written in C# and is actively maintained as of June 2026.

**Value**  
- **Real‑world tool access:** By exposing the full PowerShell ecosystem (and any installed CLI), the server gives LLMs concrete, up‑to‑date capabilities instead of relying on static knowledge bases.  
- **Standardised integration:** MCP is a vendor‑agnostic protocol, so the same server can serve Claude, other LLMs, or custom agents without code changes.  
- **Cross‑platform consistency:** A single installation works on Windows, Linux and macOS, simplifying ops for mixed‑environment teams.

**Practical adoption path**  
1. **Prototype:** Clone the repo, run the provided Docker image or binary, and point your MCP‑compatible client (e.g., Claude Code) at the server’s endpoint. Verify that the AI can list, import, and execute a few PowerShell modules.  
2. **Secure the surface:** Add authentication (e.g., API‑key or mutual TLS), restrict the allowed modules/CLI tools, and enable audit logging.  
3. **Integrate into CI/CD:** Package the server as a container or a system service, configure environment‑specific module sets, and expose the endpoint to your internal AI orchestration layer.  
4. **Scale & monitor:** Deploy multiple replicas behind a load balancer, use Prometheus metrics (if instrumented) for health, and establish alerts for abnormal command patterns.

**Production readiness**  
- **Maturity:** Medium. The project has recent commits, a modest star count (≈74) and basic documentation, making it suitable for internal prototypes and controlled production use.  
- **Dependencies:** Relies on the host’s PowerShell installation and any external CLI tools you expose; these must be vetted and kept up‑to‑date.  
- **Risks:** No formal security review or enterprise‑grade hardening is included; licensing and maintainer activity need confirmation before a public‑facing rollout. With proper sandboxing, authentication, and monitoring, PowerShell.MCP can be safely promoted to production for internal workflows.

### Русский

**PowerShell.MCP** — универсальный сервер Model Context Protocol, позволяющий подключать Claude Code и любые MCP‑совместимые клиенты к более 10 000 модулей PowerShell и к любым CLI‑утилитам, обеспечивая совместную работу человека и ИИ в одном консольном окне на Windows, Linux и macOS. Типичный сценарий — быстрое прототипирование или внутренние автоматизированные воркфлоу, где AI получает прямой доступ к реальным инструментам и данным через стандартизированный протокол. Готовность к production — средняя: проект уже стабилен для прототипов, но требует проверки зависимостей, лицензии и поддержки перед масштабным внедрением.

### 中文

**项目简介**  
yotsuda/PowerShell.MCP 是一套通用的 MCP（Model Context Protocol）服务器，实现了 Claude Code 与其他兼容 MCP 的客户端的对接。一次部署即可让 AI 直接调用 10,000+ PowerShell 模块以及任意本地 CLI 工具，用户与 AI 在同一个终端中协同工作，支持 Windows、Linux 与 macOS。

**价值点**  
- **标准化桥接**：通过统一的 MCP 协议，AI 助手可以像调用本地函数一样安全、透明地使用真实的系统工具和数据。  
- **工具覆盖广**：一次安装即接入 PowerShell 生态的全部模块以及任意可执行的 CLI，极大扩展了 AI 的实际操作能力。  
- **协同透明**：AI 与人类在同一控制台交互，所有指令、输出都可见，便于审计与调试。  

**典型接入方式**  
1. **部署服务器**：在目标机器上运行 `dotnet run`（或使用提供的 Docker 镜像）启动 MCP 服务。  
2. **注册客户端**：在 Claude Code、Auto‑GPT、LangChain 等支持 MCP 的客户端配置服务器地址（如 `http://localhost:8000`）并完成身份验证。  
3. **调用工具**：客户端通过 MCP 发起 `execute` 请求，指定 PowerShell 模块或 CLI 命令，服务器在本机执行并返回结构化结果。  

**生产可用性评估**  
- **成熟度**：目前在 GitHub 上拥有 74 颗星、7 个 Fork，最近一次提交在 2026‑06‑23，代码基于 C#，项目结构清晰，适合原型和内部工作流快速落地。  
- **依赖与运维**：依赖 .NET 6+ 运行时和 PowerShell 环境，跨平台支持良好；但需要自行审查所调用的外部 CLI 的安全风险，并做好权限隔离。  
- **风险点**：许可证、长期维护者活跃度以及安全加固（如沙箱、审计日志）尚未完成完整评估，建议在生产环境前进行安全审计并制定更新策略。  

**结论**  
PowerShell.MCP 为 AI 与真实系统工具的对接提供了一个简洁、统一的协议层，适合作为原型或内部自动化平台的核心组件。经过安全加固和运维流程确认后，可逐步推广至生产环境。

## 🧭 Practical evaluation

**Value:** yotsuda/PowerShell.MCP helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 74 GitHub stars
- 7 forks
- updated 2026-06-23
- primary language: C#
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 23/100 |
| stars | 40/100 |
| topics | 63/100 |
| outlook | 73/100 |
| quality | 60/100 |
| recency | 80/100 |
| adoption | 35/100 |
| production | 67/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/yotsuda/PowerShell.MCP) · [← Back to Mcp](./README.md)</sub>
