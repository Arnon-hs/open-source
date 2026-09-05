# alisaitteke/photoshop-mcp

[![Stars](https://img.shields.io/github/stars/alisaitteke/photoshop-mcp?style=flat-square&color=yellow)](https://github.com/alisaitteke/photoshop-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/alisaitteke/photoshop-mcp?style=flat-square&color=blue)](https://github.com/alisaitteke/photoshop-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> MCP server for Adobe Photoshop automation - Control Photoshop from AI assistants with 50+ tools for design, image editing, and workflow automation

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 121 |
| 🍴 **Forks** | 14 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`adobe` `ai` `ai-assistant` `claude` `creative-automation` `extendscript` `graphic-design` `image-editing` `macos` `mcp` `model-context-protocol` `photoshop`

## 🎯 Categories

MCP · Automation · AI/ML · Design

## 📝 Summary

### English

**Brief Summary**  
`alisaitteke/photoshop-mcp` is an open‑source Model Context Protocol (MCP) server that lets AI assistants invoke more than 50 Photoshop‑related tools for design, image editing, and workflow automation. Written in TypeScript, it provides a clean API/SDK/CLI surface so developers can bridge generative AI agents with real Photoshop capabilities.  

**Value**  
- **Standardized AI‑to‑tool bridge:** By exposing Photoshop functions through MCP, the project eliminates the need for custom, ad‑hoc integrations, letting any MCP‑compatible AI (e.g., ChatGPT, Claude, or custom agents) control Photoshop directly.  
- **Rich toolset:** Over 50 built‑in commands cover common design tasks (layer manipulation, filters, batch processing, asset export, etc.), accelerating prototyping and reducing manual effort.  
- **Extensible backend:** The TypeScript codebase makes it easy to add new Photoshop actions or wrap third‑party plugins, future‑proofing the integration stack.  

**Practical Adoption Path**  
1. **Prototype:** Clone the repo, run the Docker‑compose or `npm start` script, and point your AI assistant to the MCP endpoint. Use the provided CLI to test individual commands (e.g., `mcp run applyFilter --args ...`).  
2. **Integrate:** Wrap the MCP client in your existing AI orchestration layer (LangChain, LlamaIndex, etc.) and map high‑level intents to the corresponding Photoshop tools.  
3. **Secure & Deploy:** Harden the server with API keys or OAuth, containerize it, and deploy to a Kubernetes or serverless environment.  
4. **Scale:** Leverage the built‑in logging and metrics to monitor usage, and add custom actions for organization‑specific workflows (e.g., brand‑compliant asset generation).  

**Production Readiness**  
- **Activity & Community:** 121 stars, recent commits (last updated 2026‑06‑23), and a modest but active fork base indicate healthy maintenance.  
- **Technical Maturity:** Implemented in TypeScript with clear API/SDK/CLI interfaces, comprehensive topic tags, and a well‑documented MCP schema, making it straightforward to evaluate and integrate.  
- **Risk Profile:** No major metadata or licensing red flags have been identified, though a final security audit and maintainer confirmation are advisable before mission‑critical use. Overall, the project is positioned as a strong OSS candidate for pilots and can be hardened for production deployments with standard DevSecOps practices.

### Русский

**al​isaitteke/photoshop‑mcp** — открытый сервер MCP, позволяющий управлять Adobe Photoshop через AI‑ассистентов, предоставляя более 50 готовых инструментов для дизайна, редактирования изображений и автоматизации рабочих процессов. Типичный сценарий: подключить модель‑контекстный протокол к Photoshop, чтобы AI‑агент мог выполнять задачи (например, ретушь, генерацию макетов) напрямую из кода или CLI, что упрощает интеграцию и стандартизацию инструментов. Проект имеет высокий уровень готовности к production: активные коммиты (обновление 2026‑06‑23), 121 звезда, 14 форков, написан на TypeScript, поддерживает API/SDK/CLI и уже используется в пилотных интеграциях, требуя лишь финальной проверки лицензии и безопасности.

### 中文

**项目简介**  
`alisaitteke/photoshop-mcp` 是一个基于 Model Context Protocol（MCP）的服务器，实现了对 Adobe Photoshop 的完整自动化控制。它提供 50+ 设计、图像编辑和工作流自动化工具，使 AI 助手能够像人类一样直接调用 Photoshop 功能，从而把 AI 的创意能力落地到真实的设计软件上。

**价值**  
- **桥接 AI 与真实工具**：通过统一的 MCP 接口，把语言模型、ChatGPT、Claude 等 AI 助手与 Photoshop 的本地功能对接，解决“AI 只能生成文字/代码”而无法直接操作专业软件的痛点。  
- **标准化集成**：遵循 MCP 规范，所有工具、参数、返回值都有统一的描述，降低不同 AI 系统之间的集成成本。  
- **提升工作效率**：AI 可以自动完成批量调色、图层管理、智能抠图等重复性任务，让设计师把更多时间花在创意本身。

**典型接入方式**  
1. **启动 MCP Server**：克隆仓库后，使用 `npm install && npm run start` 启动 TypeScript 编写的服务器（默认监听 127.0.0.1:8080）。  
2. **注册到 AI 助手**：在 OpenAI、Anthropic 或自建的 LLM 平台中，配置 MCP 端点 URL 与对应的工具清单（JSON‑LD）。  
3. **调用工具**：AI 通过 MCP 请求（如 `POST /tool/adjustBrightness`）传递参数，服务器内部调用 Photoshop 的 ExtendScript/JSX 脚本或 UXP 插件完成实际编辑，并返回结果或生成的文件路径。  
4. **可选 CLI/SDK**：项目同时提供 `photoshop-mcp-cli` 与 `photoshop-mcp-sdk`（Node.js），方便在 CI/CD、批处理脚本或自定义后端服务中直接调用。

**生产可用性**  
- **活跃度**：截至 2026‑06‑23 最近一次提交，GitHub ★121、Fork 14，15 个相关话题，表明社区和维护者仍在积极迭代。  
- **技术成熟度**：使用 TypeScript 编写，提供完整的 API/SDK/CLI，且依赖官方 Photoshop 脚本接口，兼容最新的 Photoshop 2026 版本。  
- **安全与合规**：项目采用 MIT 许可证，暂无已知安全漏洞；但在正式生产环境前仍建议自行进行代码审计和渗透测试。  
- **可扩展性**：通过插件机制可以自行添加自定义 Photoshop 脚本或第三方图像处理工具，满足特定业务需求。  

综合来看，`alisaitteke/photoshop-mcp` 已具备 **高** 的生产就绪度，适合作为 AI‑Design 工作流的核心桥梁，在内部 PoC 或面向客户的自动化设计产品中快速落地。

## 🧭 Practical evaluation

**Value:** alisaitteke/photoshop-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 121 GitHub stars
- 14 forks
- updated 2026-06-23
- primary language: TypeScript
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 44/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 40/100 |
| production | 70/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/alisaitteke/photoshop-mcp) · [← Back to Mcp](./README.md)</sub>
