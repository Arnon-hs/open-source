# dotnet-presentations/ai-workshop

[![Stars](https://img.shields.io/github/stars/dotnet-presentations/ai-workshop?style=flat-square&color=yellow)](https://github.com/dotnet-presentations/ai-workshop/stargazers) [![Forks](https://img.shields.io/github/forks/dotnet-presentations/ai-workshop?style=flat-square&color=blue)](https://github.com/dotnet-presentations/ai-workshop/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Building GenAI Apps in C#: AI Templates, GitHub Models, Azure OpenAI & More

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 43 |
| 🍴 **Forks** | 26 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`csharp` `mcp-server` `meai` `microsoft-extensions-ai` `workshop`

## 🎯 Categories

Templates · MCP · AI/ML · Backend

## 📝 Summary

### English

**Project Summary:**

The open-source project "dotnet-presentations/ai-workshop" enables developers to connect AI assistants to real tools and data through a standard protocol, making it easier to integrate AI agents with various applications. This project provides a valuable resource for building GenAI apps in C# by offering AI templates, GitHub models, Azure OpenAI, and more. By standardizing integrations, developers can focus on creating innovative AI-powered applications.

**Value Proposition:**

The value proposition of this project lies in its ability to simplify the integration of AI assistants with real tools and data, making it a useful resource for developers working on GenAI applications. This standard protocol allows for seamless communication between AI agents and various applications, reducing the complexity of development and increasing productivity.

**Practical Adoption Path:**

To adopt this project, developers can follow these steps:

1. **Evaluate the project:** Review the project's documentation, codebase, and dependencies to ensure it meets the requirements for the specific use case.
2. **Connect AI agents to tools:** Use the provided templates and APIs to connect AI agents to real tools and data.
3. **Ship Model Context Protocol servers:** Implement the Model Context Protocol servers to enable communication between AI agents and applications.
4. **Standardize integrations:**

### Русский

**dotnet‑presentations/ai‑workshop** — это открытый набор шаблонов и компонентов для быстрой разработки генеративных AI‑приложений на C#: интеграция с GitHub Models, Azure OpenAI и реализация протокола Model Context, позволяющая подключать AI‑агентов к реальным инструментам и данным. Типичный сценарий — создание прототипов или внутренних сервисов, где требуется стандартизировать взаимодействие AI с внешними API/CLI через единый протокол; проект также подходит для развертывания собственного сервера Model Context. Готовность к production — средняя: репозиторий активно поддерживается (обновление 2026‑07‑01, 43 ★, 26 форков), но перед выпуском в продакшн требуется проверка лицензии, безопасности и зависимости.

### 中文

**项目简介**  
dotnet‑presentations/ai‑workshop 是一个面向 .NET 开发者的实战教程仓库，演示如何在 C# 中快速构建生成式 AI 应用，涵盖 AI 模板、GitHub 模型、Azure OpenAI 等完整链路。  

**价值**  
- **统一协议**：提供 Model Context Protocol（MCP）实现，帮助 AI 助手安全、标准化地调用真实工具和业务数据。  
- **端到端示例**：从代码模板到部署脚本，一站式展示从本地开发到 Azure 云端的完整工作流，降低团队学习成本。  
- **可复用组件**：包括 API/SDK/CLI 包装、语言元数据和工具集成示例，便于在自研产品中快速复用或扩展。  

**典型接入方式**  
1. **SDK/CLI**：直接在 C# 项目中引用 `AiWorkshop.SDK`（或通过 npm 包的 JS 示例），使用统一的 `McpClient` 调用模型或工具。  
2. **MCP 服务器**：部署仓库中的 `McpServer`（Docker 镜像或 Azure Functions），作为内部模型/工具的统一入口。  
3. **GitHub 模型**：通过仓库提供的 GitHub Actions 自动拉取并注册模型，配合 Azure OpenAI 进行推理。  

**生产可用性**  
- **成熟度**：当前评分 63/100，适合作为原型或内部工作流的起点。  
- **依赖与维护**：项目依赖 .NET 8、Azure SDK 等主流库，社区活跃（43 星、26 Fork），但仍需自行审查许可证、漏洞报告以及长期维护者的活跃度。  
- **上线建议**：在生产环境部署前，完成以下检查：  
  1. **安全审计**：确认所有外部 API（Azure OpenAI、GitHub）使用的凭证管理符合公司政策。  
  2. **性能评估**：对 MCP 服务器进行压测，确保并发请求满足业务 SLA。  
  3. **监控与日志**：集成 Application Insights 或 Prometheus，监控模型调用时延和错误率。  

综上，dotnet‑presentations/ai‑workshop 为 .NET 团队提供了一个快速上手生成式 AI 的学习与实验平台，具备标准化的工具接入方式，适合在经过安全和性能验证后逐步迁移到生产环境。

## 🧭 Practical evaluation

**Value:** dotnet-presentations/ai-workshop helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 43 GitHub stars
- 26 forks
- updated 2026-07-01
- primary language: JavaScript
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 36/100 |
| stars | 35/100 |
| topics | 63/100 |
| outlook | 54/100 |
| quality | 50/100 |
| recency | 40/100 |
| adoption | 35/100 |
| production | 54/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/dotnet-presentations/ai-workshop) · [← Back to Templates](./README.md)</sub>
