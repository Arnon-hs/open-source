# dcc-mcp/dcc-mcp-core

[![Stars](https://img.shields.io/github/stars/dcc-mcp/dcc-mcp-core?style=flat-square&color=yellow)](https://github.com/dcc-mcp/dcc-mcp-core/stargazers) [![Forks](https://img.shields.io/github/forks/dcc-mcp/dcc-mcp-core?style=flat-square&color=blue)](https://github.com/dcc-mcp/dcc-mcp-core/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> Core runtime and shared tooling for DCC-MCP: safe, skill-first MCP integration across Maya, Blender, Houdini, Photoshop, and custom DCC hosts.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 28 |
| 🍴 **Forks** | 1 |
| 💻 **Language** | Rust |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `automation` `blender` `dcc` `houdini` `maya` `mcp` `model-context-protocol` `photoshop` `pyo3` `python` `rust`

## 🎯 Categories

MCP · Automation · AI/ML

## 📝 Summary

### English

**Brief Summary**  
dcc‑mcp‑core is the runtime and shared tooling that powers DCC‑MCP, a protocol for safe, “skill‑first” integration of AI assistants with major DCC applications such as Maya, Blender, Houdini, Photoshop, and custom hosts. Written in Rust, the library provides a unified API/SDK and CLI that lets developers expose tool‑specific capabilities to AI agents via the Model Context Protocol (MCP).  

**Value**  
- **Standardized bridge**: By abstracting the quirks of each DCC package behind a common MCP interface, developers can connect AI agents to real creative tools without writing bespoke adapters for every host.  
- **Safety & control**: MCP’s “skill‑first” design lets you expose only vetted commands, reducing the risk of unintended actions by an AI assistant.  
- **Cross‑tool portability**: The same integration code can be reused across Maya, Blender, Houdini, Photoshop, etc., accelerating multi‑tool pipelines and reducing maintenance overhead.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, add the Rust crate to your project, and use the provided SDK to register a few simple commands (e.g., “export current scene”).  
2. **MCP Server** – Deploy a Model Context Protocol server (bundled with the core) that exposes those commands to an AI agent (e.g., a LangChain or OpenAI‑based assistant).  
3. **Iterate** – Extend the command set, map host‑specific APIs, and test with the CLI to verify correct signal flow.  
4. **Productionize** – Containerize the MCP server, integrate it into your CI/CD pipeline, and enforce security policies (e.g., command whitelisting, authentication).  

**Production Readiness**  
- **Maturity**: Medium. The codebase is recent (last commit 2026‑06‑22), has modest community traction (≈28 ★), and is written in Rust, which offers safety and performance.  
- **Strengths**: Clear API/SDK, CLI for rapid testing, and a well‑defined protocol that aligns with emerging AI‑tool integration standards.  
- **Caveats**: Limited external adoption, few forks, and the need for a thorough security review (license compliance, dependency audit, and maintainer activity). Before shipping to customers, perform:  
  * Dependency vulnerability scanning,  
  * License verification,  
  * Load‑testing of the MCP server under realistic tool‑call volumes, and  
  * Implementation of authentication/authorization around exposed commands.  

With those checks in place, dcc‑mcp‑core is a solid foundation for building AI‑augmented DCC workflows and can move from internal prototyping to production use.

### Русский

**d​cc‑mcp/dcc‑mcp‑core** — это ядро‑рантайм и набор общих инструментов для проекта DCC‑MCP, позволяющий безопасно интегрировать AI‑ассистентов с профессиональными DCC‑приложениями (Maya, Blender, Houdini, Photoshop и кастомными хостами) через единый протокол Model Context Protocol. Типичный сценарий — запуск AI‑агента, который через MCP‑сервер управляет инструментами‑плагинами, автоматизирует задачи и получает доступ к данным проекта; такой подход упрощает создание прототипов и внутренних пайплайнов, а также стандартизирует будущие продакшн‑интеграции. Готовность к production — средний уровень: проект стабилен для прототипов и ограниченных рабочих процессов, но требует проверки лицензии, безопасности и поддержки зависимостей перед масштабным внедрением.

### 中文

**项目简介**  
dcc-mcp/dcc-mcp-core 是 DCC‑MCP 的核心运行时与共享工具库，提供安全、以「skill」为中心的模型上下文协议（Model Context Protocol）实现，支持 Maya、Blender、Houdini、Photoshop 以及自定义 DCC 主机的统一集成。

**价值**  
- **AI 与真实工具的桥梁**：通过标准化的协议，将 AI 助手直接连接到专业创作软件的功能和数据，实现「AI‑in‑the‑loop」的自动化工作流。  
- **跨平台统一接口**：一次实现后即可在多种 DCC 环境中复用，降低重复开发成本。  
- **可扩展的插件体系**：提供 API/SDK/CLI，便于在现有管线中快速嵌入自定义 skill 或模型服务。

**典型接入方式**  
1. **依赖引入**：在 Rust 项目中通过 `cargo add dcc-mcp-core` 引入库，或在其他语言（Python、C++）中使用对应的 FFI 包装。  
2. **启动 MCP Server**：使用提供的 CLI (`dcc-mcp-core serve`) 启动 Model Context Protocol 服务器，指定要暴露的 DCC 主机插件。  
3. **注册 Skill**：在服务器配置文件中声明 AI skill（REST、gRPC、WebSocket 等），并绑定到具体的 DCC 命令或脚本。  
4. **客户端调用**：AI 代理通过标准的 MCP 消息（JSON‑RPC/Protobuf）向服务器发送请求，服务器转发到目标 DCC 软件并返回结果。

**生产可用性**  
- **成熟度**：当前评分 74/100，适合作为原型或内部流水线的核心组件。  
- **依赖与维护**：Rust 实现，代码库较小（28⭐），更新活跃（截至 2026‑06‑22），但仍需自行审查许可证、第三方依赖安全性以及维护者响应速度。  
- **上线建议**：在生产环境部署前，进行以下检查：  
  1. 完整的安全审计（尤其是网络接口）。  
  2. 依赖锁定与 CI/CD 自动化测试。  
  3. 监控与日志收集，确保跨 DCC 主机的错误可追溯。  

总体而言，dcc-mcp-core 为 AI 与专业创作工具的深度集成提供了统一、可编程的基础设施，适合希望在现有艺术管线中快速实验 AI‑驱动自动化的团队。

## 🧭 Practical evaluation

**Value:** dcc-mcp/dcc-mcp-core helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 28 GitHub stars
- 1 forks
- updated 2026-06-22
- primary language: Rust
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 8/100 |
| stars | 31/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 61/100 |
| recency | 80/100 |
| adoption | 25/100 |
| production | 67/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/dcc-mcp/dcc-mcp-core) · [← Back to Mcp](./README.md)</sub>
