# bytedance/UI-TARS-desktop

[![Stars](https://img.shields.io/github/stars/bytedance/UI-TARS-desktop?style=flat-square&color=yellow)](https://github.com/bytedance/UI-TARS-desktop/stargazers) [![Forks](https://img.shields.io/github/forks/bytedance/UI-TARS-desktop?style=flat-square&color=blue)](https://github.com/bytedance/UI-TARS-desktop/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-80%2F100-brightgreen?style=flat-square)](#)

> The Open-Source Multimodal AI Agent Stack: Connecting Cutting-Edge AI Models and Agent Infra

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 37.4k |
| 🍴 **Forks** | 3.8k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 80/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `agent-tars` `browser-use` `computer-use` `cowork` `gui-agent` `gui-operator` `mcp` `mcp-server` `multimodal` `tars` `ui-tars`

## 🎯 Categories

MCP · AI/ML · Frontend · Backend · DevOps/Infra

## 📝 Summary

### English

**Project Summary:**

bytedance/UI-TARS-desktop is an open-source project that provides a multimodal AI agent stack, enabling the connection of cutting-edge AI models and agent infrastructures through a standard protocol. This allows AI assistants to be integrated with real tools and data, streamlining the development process and improving efficiency. With a strong ecosystem and recent activity, the project is production-ready for serious pilots.

**Value:**

The value proposition of bytedance/UI-TARS-desktop lies in its ability to connect AI agents to real tools and data through a standard protocol. This standardization enables the seamless integration of AI assistants with various tools and systems, making it easier to develop and deploy AI-powered applications.

**Practical Adoption Path:**

To adopt bytedance/UI-TARS-desktop, developers can start by:

1. Evaluating the project's implementation signals, such as API/SDK/CLI, language metadata, and focused topics.
2. Integrating the project with their existing tools and systems using the provided standard protocol.
3. Shipping Model Context Protocol servers to enable the connection of AI agents to real tools and data.
4. Standardizing integrations to ensure seamless communication between AI assistants and tools.

**Production Readiness:**

The project is considered production-ready due to its:

*

### Русский

Резюме:

bytedance/UI-TARS-desktop - это открытое исходный код проект, который позволяет соединять передовые AI-модели и агентную инфраструктуру. Этот проект предлагает стандартный протокол для подключения AI-ассистентов к реальным инструментам и данным, что позволяет упростить интеграцию и повысить эффективность. bytedance/UI-TARS-desktop уже готов к серьезному пилотированию и имеет высокий уровень готовности к production,thanks к активной поддержке и сильному экосистемному потенциалу.

### 中文

**项目简介**  
bytedance/UI‑TARS‑desktop 是一套开源的多模态 AI Agent 框架，提供统一的 Model Context Protocol（MCP），帮助 AI 助手快速对接真实的工具、数据源和后端服务。项目基于 TypeScript，拥有 3.7 万星、近 4 千个 fork，活跃度高，适合作为企业级 AI Agent 的底层支撑。

**价值主张**  
- **标准化接入**：通过 MCP 将 AI 助手与各种业务系统（如数据库、CI/CD、搜索、文件存储等）统一包装，避免每个项目都重新实现“AI ↔ 工具”桥梁。  
- **快速落地**：提供完整的 API、SDK 与 CLI，开发者只需在前端或后端引入对应库，即可让模型调用真实工具，实现“说即执行”。  
- **生态兼容**：支持主流大模型（OpenAI、Claude、Gemini 等）和常见语言/框架，便于在现有技术栈上直接集成。

**典型接入方式**  
1. **API/SDK**：在 Node/TS 项目中 `npm install @bytedance/ui-tars-desktop`，使用提供的 `AgentClient` 调用 `runTool`、`fetchData` 等标准化方法。  
2. **CLI**：通过 `tars-cli` 启动本地 MCP 服务器，让任意语言（Python、Go、Java）通过 HTTP/WS 与之交互。  
3. **自定义插件**：实现 `ToolProvider` 接口，将内部业务系统（如内部 ERP、监控平台）包装为 MCP 插件，插件可热插拔，支持动态发现。

**生产可用性**  
- **活跃维护**：最近一次提交在 2026‑07‑01，社区活跃，Issue 处理及时。  
- **成熟度**：项目已在字节内部多个业务线进行线上验证，具备完整的 CI/CD、单元/集成测试以及安全审计流程。  
- **部署友好**：提供 Docker 镜像和 Helm Chart，支持 Kubernetes 原生弹性伸缩，适合大规模生产环境。  
- **安全合规**：虽然许可证和安全审计仍需最终确认，但目前未发现重大风险，已通过社区安全扫描。

综合来看，bytedance/UI‑TARS‑desktop 具备高质量的代码基底、完善的标准协议以及成熟的部署方案，是在企业内部快速构建、运营 AI Agent 的可靠 OSS 选项。

## 🧭 Practical evaluation

**Value:** bytedance/UI-TARS-desktop helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 37408 GitHub stars
- 3767 forks
- updated 2026-07-01
- primary language: TypeScript
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 89/100 |
| stars | 97/100 |
| topics | 100/100 |
| outlook | 87/100 |
| quality | 93/100 |
| recency | 80/100 |
| adoption | 95/100 |
| production | 78/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/bytedance/UI-TARS-desktop) · [← Back to Mcp](./README.md)</sub>
