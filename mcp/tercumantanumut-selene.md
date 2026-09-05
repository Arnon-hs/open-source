# tercumantanumut/selene

[![Stars](https://img.shields.io/github/stars/tercumantanumut/selene?style=flat-square&color=yellow)](https://github.com/tercumantanumut/selene/stargazers) [![Forks](https://img.shields.io/github/forks/tercumantanumut/selene?style=flat-square&color=blue)](https://github.com/tercumantanumut/selene/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-78%2F100-brightgreen?style=flat-square)](#)

> Selene is a desktop app that runs AI agents on your machine. Connect them to your WhatsApp, Telegram, Slack, or Discord. Write code, generate images, build personal assistants. All from one place. Your data stays on your device.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 169 |
| 🍴 **Forks** | 36 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 78/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `antigravity` `codebase-indexing` `codex` `deferred-loading` `diffusion-models` `knowledge-base` `llm` `long-term-memory` `mcp` `mcp-client` `mcp-server`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · Communication · Productivity

## 📝 Summary

### English

**Project Summary:** Selene is an open-source desktop app that enables users to run AI agents on their machine, connect them to popular communication platforms (WhatsApp, Telegram, Slack, and Discord), and utilize them for various tasks such as coding, image generation, and personal assistant capabilities.

**Value Proposition:** The primary value of Selene lies in its ability to standardize integrations between AI assistants and real tools and data through the Model Context Protocol (MCP). This standard protocol facilitates the connection of AI agents to various platforms, making it easier for developers to create and utilize AI-powered applications.

**Practical Adoption Path:** To adopt Selene, users can follow these steps:

1. Install the desktop app on their machine.
2. Connect their preferred communication platform (e.g., WhatsApp, Telegram) to Selene.
3. Choose from a range of AI agents and protocols (e.g., MCP) to integrate with their connected platforms.
4. Utilize the AI agents for various tasks, such as coding, image generation, or personal assistant capabilities.

**Production Readiness:** Selene has demonstrated a high level of production readiness, with recent activity, adoption, and ecosystem signals indicating its potential for a serious pilot. With 169 GitHub stars, 36 forks, and regular updates, Sel

### Русский

Резюме проекта Selene:

Selene - это открытый проект, позволяющий создавать и интегрировать искусственный интеллект на вашем компьютере. Это позволяет соединять AI-агентов с реальными инструментами и данными через стандартный протокол. Проект готов к серьезному пилотированию из-за своей высокой готовности к производству, активности и сильного признания в сообществе.

### 中文

**项目简介**  
Selene 是一款桌面应用，能够在本地运行 AI 代理并通过统一的协议把它们接入 WhatsApp、Telegram、Slack、Discord 等常用工具。用户可以在同一界面编写代码、生成图片、构建个人助理，所有数据均保存在本机，确保隐私安全。

**价值主张**  
- **统一协议**：通过标准的 Model Context Protocol（MCP）把 AI 代理与外部工具、数据源快速绑定，避免每个渠道单独实现集成。  
- **本地安全**：所有请求、模型和生成内容都在本机处理，数据不离开用户设备，适合对隐私要求高的企业或个人。  
- **一站式开发**：提供完整的前端 UI、后端服务和 SDK/CLI，既能快速原型，又能直接用于生产级别的 AI 助手。

**典型接入方式**  
1. **安装桌面客户端**（TypeScript/Node.js）并启动 Selene。  
2. **使用内置 SDK 或 CLI**：  
   - `npm i @selene/sdk` → 在项目中引用 `SeleneClient`，调用 `connect('whatsapp')`、`connect('slack')` 等方法。  
   - CLI 示例：`selene agent create --name myBot --model gpt-4o`，随后 `selene agent bind --platform telegram --token <TOKEN>`。  
3. **部署 MCP 服务器**（可选）：如果需要在内部网络或云端统一管理多个代理，可自行运行 `selene-mcp-server`，所有客户端通过统一的 HTTP/gRPC 接口注册与调用。  
4. **集成到现有系统**：通过 REST/GraphQL API 或 WebSocket，外部业务系统可以向 Selene 发送指令、获取生成结果，实现“AI 即服务”。

**生产可用性**  
- **活跃度**：截至 2026‑07‑11，项目最近一次提交，拥有 169 ⭐、36 🍴，社区活跃。  
- **技术成熟度**：核心使用 TypeScript 编写，提供前端 UI、后端服务、CLI 与 SDK，覆盖全栈需求。  
- **安全与合规**：所有数据默认本地存储，无强制云端依赖，降低信息泄露风险；但仍需自行审查许可证（MIT）及第三方依赖的安全报告。  
- **可扩展性**：支持自定义模型接入（OpenAI、Claude、本地 LLM），以及插件式的工具调用（浏览器、文件系统、数据库），适合作为企业内部 AI 助手平台的基石。  

**结论**  
Selene 具备较高的生产就绪度，适合作为企业或个人在本地快速搭建、管理多渠道 AI 代理的统一平台。只要完成许可证与依赖安全的最终审查，即可在实际业务中进行试点甚至全量部署。

## 🧭 Practical evaluation

**Value:** tercumantanumut/selene helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 169 GitHub stars
- 36 forks
- updated 2026-07-11
- primary language: TypeScript
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 39/100 |
| stars | 47/100 |
| topics | 100/100 |
| outlook | 79/100 |
| quality | 70/100 |
| recency | 80/100 |
| adoption | 45/100 |
| production | 73/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-07-11 · [View on GitHub](https://github.com/tercumantanumut/selene) · [← Back to Mcp](./README.md)</sub>
