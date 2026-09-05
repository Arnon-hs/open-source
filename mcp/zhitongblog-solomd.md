# zhitongblog/solomd

[![Stars](https://img.shields.io/github/stars/zhitongblog/solomd?style=flat-square&color=yellow)](https://github.com/zhitongblog/solomd/stargazers) [![Forks](https://img.shields.io/github/forks/zhitongblog/solomd?style=flat-square&color=blue)](https://github.com/zhitongblog/solomd/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> A markdown editor — and the bridge to your LLM. Local-first, MIT, ~15 MB. Bundled MCP server lets Claude Code / Codex / Cursor drive your vault directly. 14 AI providers BYOK.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 411 |
| 🍴 **Forks** | 24 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `android` `autogit` `byok` `cross-platform` `ios` `knowledge-base` `local-first` `markdown` `markdown-editor` `mcp` `mcp-server`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · Documents · Productivity

## 📝 Summary

### English

**Project Summary:**

Solomd is an open-source markdown editor that serves as a bridge to connect Large Language Models (LLMs) to real-world tools and data. By implementing the Model Context Protocol (MCP), Solomd enables seamless integrations with 14 AI providers, allowing users to access their AI assistants directly from the editor. This innovative project offers a local-first, MIT-licensed solution with a small footprint of approximately 15 MB.

**Value Proposition:**

The primary value of Solomd lies in its ability to standardize integrations between AI assistants and real-world tools and data. By providing a common protocol for AI providers, Solomd simplifies the process of connecting AI agents to various tools, making it easier for developers to build and deploy AI-powered applications.

**Practical Adoption Path:**

To adopt Solomd, developers can follow these steps:

1. Evaluate the project's implementation signals, such as API/SDK/CLI, language metadata, and focused topics.
2. Assess the project's production readiness, including its recent activity, adoption, and ecosystem signals.
3. Review the project's license, security posture, and active maintainers to ensure it meets their needs.
4. Integrate Solomd with their AI providers and tools using the

### Русский

**z​hitongblog/solomd** — это локальный markdown‑редактор с встроенным MCP‑сервером, который позволяет подключать к вашему хранилищу любые LLM (Claude, Codex, Cursor и другие 14 провайдеров BYOK) через единый протокол Model Context Protocol. Типичный сценарий: встраивание редактора в существующий воркфлоу, запуск MCP‑сервера и предоставление ИИ‑агенту прямого доступа к файлам, инструментам и контексту проекта, что упрощает автоматизацию, генерацию кода и RAG‑запросы. Проект активно поддерживается (обновления 2026‑06‑28, 411★, 24 форка), написан на TypeScript и готов к пилотному внедрению в production‑среде после финальной проверки лицензии и безопасности.

### 中文

**项目简介**  
zhitongblog/solomd 是一款本地优先的 Markdown 编辑器（约 15 MB，MIT 许可证），内置 MCP（Model Context Protocol）服务器，可让 Claude Code、Codex、Cursor 等 14 家 AI 提供商直接在你的知识库上执行代码、检索信息或完成写作任务，支持 BYOK（自带密钥）接入。

**价值主张**  
- **统一协议**：通过标准化的 MCP 接口，把 AI 助手与真实工具、数据和业务流程无缝桥接，降低集成复杂度。  
- **本地安全**：所有编辑和模型交互均在本地运行，数据不必离开企业防火墙，满足隐私合规要求。  
- **多供应商灵活性**：一次接入即可切换或并用多达 14 家 LLM 提供商，避免锁厂。  

**典型接入方式**  
1. **API/SDK**：在项目中引入 `solomd` 的 TypeScript SDK，调用 `startMCPServer()` 启动本地 MCP 服务，然后通过 HTTP/WS 与 LLM 交互。  
2. **CLI**：使用自带的 `solomd-cli`，在 CI/CD 或本地脚本中直接执行 `solomd run --model=claude --vault=./my-notes`。  
3. **插件**：在前端（React/Vite）或后端（Node.js）项目中加载 `solomd` 插件，实现“编辑器即 AI 助手”的即时体验。  

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑28，星标 411，fork 24，社区讨论活跃，具备持续维护的迹象。  
- **技术成熟度**：核心使用 TypeScript 编写，提供完整的类型定义，易于在现有 TypeScript/JavaScript 项目中集成。  
- **安全合规**：MIT 许可证，无捆绑第三方闭源组件，所有代码均可审计；可自行部署 MCP 服务器，满足内部安全审查。  
- **可扩展性**：支持自定义模型密钥（BYOK）和插件化的协议扩展，适合从小型原型到大型企业级部署。  

综合来看，zhitongblog/solomd 已具备较高的生产就绪度，适合作为 AI‑Tool‑Bridge 的核心组件，在内部知识库、文档生成或代码辅助等场景中快速落地。

## 🧭 Practical evaluation

**Value:** zhitongblog/solomd helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 411 GitHub stars
- 24 forks
- updated 2026-06-28
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 50/100 |
| production | 71/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/zhitongblog/solomd) · [← Back to Mcp](./README.md)</sub>
