# microsoft/mcp-dotnet-samples

[![Stars](https://img.shields.io/github/stars/microsoft/mcp-dotnet-samples?style=flat-square&color=yellow)](https://github.com/microsoft/mcp-dotnet-samples/stargazers) [![Forks](https://img.shields.io/github/forks/microsoft/mcp-dotnet-samples?style=flat-square&color=blue)](https://github.com/microsoft/mcp-dotnet-samples/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> A comprehensive set of samples of creating and using MCP servers and clients with .NET

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 183 |
| 🍴 **Forks** | 55 |
| 💻 **Language** | C# |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`dotnet` `mcp` `mcp-client` `mcp-server`

## 🎯 Categories

MCP · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The *microsoft/mcp-dotnet-samples* repository provides a rich collection of .NET examples that demonstrate how to build and consume Model Context Protocol (MCP) servers and clients. By offering ready‑to‑run code for both sides of the protocol, it gives developers a concrete reference for wiring AI assistants to real tools, data stores, and services using a standardized interface.

**Value**  
- **Accelerates integration** – Developers can copy‑paste or adapt sample projects instead of starting from scratch, dramatically shortening the time to connect AI agents with existing back‑ends.  
- **Standardizes communication** – All samples follow the MCP specification, helping teams adopt a common protocol that eases future interoperability across different tools and vendors.  
- **Learning resource** – The code showcases best practices for authentication, request handling, and streaming, serving as both a tutorial and a sanity‑check for custom implementations.

**Practical Adoption Path**  
1. **Explore the samples** – Clone the repo and run the “HelloWorld” client/server to verify the development environment (requires .NET 8+).  
2. **Map to your use case** – Identify which sample (e.g., tool‑invocation, data‑retrieval, streaming) aligns with the functionality you need to expose to an AI assistant.  
3. **Customize the implementation** – Replace the placeholder logic with your own business logic, data connectors, or external APIs while preserving the MCP contract.  
4. **Package & test** – Containerize the server (Dockerfile is included) and run integration tests against your AI agent or the MCP SDK.  
5. **Deploy** – Deploy the server to your preferred cloud (Azure, AWS, on‑prem) and point the client/assistant to the new endpoint, adjusting any authentication secrets.

**Production Readiness**  
- **Maturity**: Medium. The repository is actively maintained (last update 2026‑05‑11) and has modest community traction (≈180 ★, 55 forks). It is suitable for prototypes, internal tools, and early‑stage production after a thorough review.  
- **Considerations before production**:  
  - Verify the licensing terms and ensure they fit your organization’s policy.  
  - Conduct a security audit of the sample code and any third‑party dependencies.  
  - Implement robust logging, monitoring, and scaling (the samples are minimal and need production‑grade extensions).  
  - Confirm long‑term maintainership or be prepared to fork and sustain the code internally.  

With these steps, teams can quickly leverage the MCP .NET samples to bring AI‑driven tooling into production while mitigating the typical risks of adopting open‑source starter kits.

### Русский

**microsoft/mcp-dotnet-samples** — открытый набор образцов, демонстрирующих создание и использование серверов и клиентов Model Context Protocol (MCP) на платформе .NET. Он позволяет быстро подключить AI‑ассистентов к реальным инструментам и данным через единый протокол, упрощая разработку прототипов и внутренних сервисов, а также ускоряя вывод в продакшн собственных MCP‑серверов. Проект имеет средний уровень готовности: подходит для прототипов и ограниченных рабочих процессов, но перед выпуском в продакшн требуется проверка лицензии, безопасности и поддержки зависимостей.

### 中文

**项目简介**  
Microsoft 的 **mcp-dotnet-samples** 提供了一整套基于 .NET 的 Model Context Protocol（MCP）服务器与客户端示例，帮助开发者快速了解并实现 AI 助手与真实工具、数据的标准化交互。

**价值**  
- **统一协议**：通过 MCP 为 AI 代理与后端服务、工具链之间搭建统一的通信层，降低集成成本。  
- **加速原型**：完整的服务器、客户端、CLI 示例让团队在几分钟内即可跑通 AI‑to‑Tool 场景，缩短 PoC 周期。  
- **可复用组件**：示例代码覆盖身份验证、流式调用、错误处理等常见需求，可直接迁移到生产项目中。

**典型接入方式**  
1. **直接引用 SDK**：在已有的 .NET 项目中通过 NuGet 引入 `Microsoft.Mcp`（或示例项目自带的库），按示例代码实现 `IMcpServer` / `IMcpClient` 接口。  
2. **使用 CLI**：项目提供的命令行工具可快速启动本地 MCP 服务器，用于调试或与外部 AI 平台（如 Azure OpenAI）对接。  
3. **容器化部署**：示例中附带 Dockerfile，支持将 MCP 服务器打包为容器，配合 Kubernetes 或 Azure Container Apps 进行弹性伸缩。  

**生产可用性**  
- **成熟度**：代码已在多个内部原型中验证，GitHub 统计 183 星、55 Fork，最近一次提交在 2026‑05‑11，活跃度尚可。  
- **适用场景**：非常适合作为 **原型**、**内部工作流** 或 **边缘服务** 的起点；在正式生产环境使用前，需要完成以下检查：  
  - 依赖版本锁定与安全审计（尤其是网络、身份验证库）。  
  - 评估许可证兼容性（MIT/Apache 等）并确认满足企业合规。  
  - 加入监控、日志、限流等生产级运维措施。  
- **总体评估**：**中等**（Medium）— 具备快速验证和迭代的能力，但在大规模、对安全合规要求高的场景下仍需额外的审查与增强。

## 🧭 Practical evaluation

**Value:** microsoft/mcp-dotnet-samples helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 183 GitHub stars
- 55 forks
- updated 2026-05-11
- primary language: C#
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 48/100 |
| topics | 50/100 |
| outlook | 49/100 |
| quality | 49/100 |
| recency | 20/100 |
| adoption | 47/100 |
| production | 48/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/microsoft/mcp-dotnet-samples) · [← Back to Mcp](./README.md)</sub>
