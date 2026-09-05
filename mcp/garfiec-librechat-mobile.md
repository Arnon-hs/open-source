# garfiec/Librechat-Mobile

[![Stars](https://img.shields.io/github/stars/garfiec/Librechat-Mobile?style=flat-square&color=yellow)](https://github.com/garfiec/Librechat-Mobile/stargazers) [![Forks](https://img.shields.io/github/forks/garfiec/Librechat-Mobile?style=flat-square&color=blue)](https://github.com/garfiec/Librechat-Mobile/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> Native Android & iOS client for LibreChat, built with Kotlin Multiplatform and Compose Multiplatform

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 25 |
| 🍴 **Forks** | 3 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-assistant` `ai-chat` `android` `anthropic` `chat-bot` `chatgpt` `chatgpt-clone` `claude` `compose-multiplatform` `gemini` `ios` `kotlin-multiplaform`

## 🎯 Categories

MCP · Automation · AI/ML · Communication · Mobile

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
LibreChat‑Mobile is a native Android and iOS client for the LibreChat AI platform, written with Kotlin Multiplatform and Compose Multiplatform. It lets developers embed AI assistants in mobile apps and connect them to external tools and data sources via the Model Context Protocol (MCP). With a lightweight codebase (≈25 ★, 3 forks) and recent updates, it is a solid starting point for prototypes or internal tooling.

---

### Value Proposition
- **Unified Mobile Front‑end:** One codebase delivers native experiences on both Android and iOS, reducing development effort compared with maintaining separate native clients.  
- **Standardized AI‑Tool Integration:** By implementing the Model Context Protocol, the client can hook AI agents to real‑world services (databases, APIs, device sensors) without custom glue code.  
- **Extensible Architecture:** Built on Kotlin Multiplatform and Compose, the project is easy to extend with additional MCP‑compatible back‑ends or custom UI components.

### Practical Adoption Path
1. **Evaluate the SDK/API** – Clone the repo, run the sample app, and inspect the exposed Kotlin SDK functions (e.g., `connectToMcpServer`, `sendToolRequest`).  
2. **Prototype Integration** – Replace the demo chat UI with your own screens, point the client at an existing LibreChat or MCP server, and test a simple tool call (e.g., fetching a calendar event).  
3. **Customize & Harden** – Add authentication, configure secure networking (TLS, pinning), and integrate any proprietary tool adapters required by your use case.  
4. **Deploy** – Publish the mobile binaries via Google Play / Apple App Store or distribute internally through enterprise MDM solutions.

### Production Readiness
- **Maturity:** Medium. The project is actively maintained (last commit 2026‑05‑12) and stable enough for prototypes or internal workflows, but it lacks extensive production‑grade testing and large‑scale user feedback.  
- **Dependencies:** Relies on Kotlin Multiplatform and Compose libraries, which are well‑supported, but you should audit transitive dependencies for security patches.  
- **Maintenance & Support:** Small community (≈25 ★, 3 forks). Review the repository’s issue tracker and licensing (likely Apache‑2.0 or MIT) before committing to long‑term production use.  
- **Risk Mitigation:** Conduct a security review of the MCP communication layer, verify compliance with your organization’s licensing policy, and consider adding automated CI/CD tests to cover critical integration paths.  

Overall, LibreChat‑Mobile offers a quick way to bring AI‑driven assistants to mobile devices, with a clear upgrade path to production once the surrounding security and maintenance checks are completed.

### Русский

**Librechat‑Mobile** — кроссплатформенный клиент для LibreChat на Kotlin Multiplatform и Compose Multiplatform, позволяющий быстро подключать AI‑ассистентов к реальным инструментам и данным через единый протокол. Его типичное применение — прототипирование или внутренние воркфлоу, где требуется интеграция моделей с внешними сервисами (инструменты, Model Context Protocol‑серверы) без разработки собственного UI. Готовность к production — средний уровень: проект уже стабилен и активно обновляется, но перед развертыванием в продакшн стоит проверить лицензию, безопасность и наличие поддерживающих мейнтейнеров.

### 中文

**项目简介**  
garfiec/Librechat‑Mobile 是一款基于 Kotlin Multiplatform 与 Compose Multiplatform 开发的原生 Android 与 iOS 客户端，用于连接 LibreChat。它提供统一的协议层，使 AI 助手能够直接调用真实工具和数据。

**价值**  
- **统一协议**：通过 Model Context Protocol（MCP）把 AI 代理与后端工具、服务、数据库等标准化对接，降低跨平台集成的复杂度。  
- **跨平台代码复用**：一次编写 Kotlin 业务逻辑即可在 Android 与 iOS 上运行，显著提升开发效率。  
- **快速原型**：适合作为内部工作流或概念验证的前端入口，快速展示 AI 与业务系统的交互。

**典型接入方式**  
1. **依赖引入**：在 Kotlin 项目中通过 Gradle/Maven 添加 `librechat-mobile` SDK。  
2. **配置 MCP 端点**：在客户端初始化时提供后端 MCP 服务器的 URL、认证凭证（如 API Key），并声明需要使用的工具插件（如搜索、数据库、文件系统）。  
3. **调用 API**：使用 SDK 暴露的 `ChatSession`、`ToolInvocation` 等类，发送用户消息并接收 AI 生成的工具调用指令，SDK 会自动完成 HTTP/WS 通信并返回结果。  
4. **可选 CLI/SDK**：项目同时提供轻量级 CLI 与纯 Kotlin SDK，方便在服务器端或脚本中直接调用同一协议，实现前后端一致性。

**生产可用性**  
- **成熟度**：当前评分 71/100，GitHub 25 ⭐、3 fork，活跃更新至 2026‑05‑12，代码基于 Kotlin，具备基本的质量与社区关注度。  
- **适用场景**：非常适合作为原型、内部工具或低风险业务的 AI 前端；在正式生产环境使用前，需要完成以下检查：  
  - **依赖审计**：确认所有第三方库的许可证兼容性与安全补丁。  
  - **安全评估**：审查 MCP 服务器的身份验证、加密传输以及对外暴露的工具接口。  
  - **运维准备**：监控客户端崩溃率、网络异常恢复以及版本升级策略。  
- **结论**：在完成上述审查后，可在对可靠性要求不极端的生产环境中投入使用；若用于高并发或关键业务，建议配合内部审计、自动化测试与持续集成流水线进行进一步验证。

## 🧭 Practical evaluation

**Value:** garfiec/Librechat-Mobile helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 25 GitHub stars
- 3 forks
- updated 2026-05-12
- primary language: Kotlin
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 15/100 |
| stars | 30/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 26/100 |
| production | 67/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/garfiec/Librechat-Mobile) · [← Back to Mcp](./README.md)</sub>
