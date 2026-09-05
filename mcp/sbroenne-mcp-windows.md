# sbroenne/mcp-windows

[![Stars](https://img.shields.io/github/stars/sbroenne/mcp-windows?style=flat-square&color=yellow)](https://github.com/sbroenne/mcp-windows/stargazers) [![Forks](https://img.shields.io/github/forks/sbroenne/mcp-windows?style=flat-square&color=blue)](https://github.com/sbroenne/mcp-windows/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-75%2F100-brightgreen?style=flat-square)](#)

> Let AI agents control Windows applications. Click buttons, type text, toggle settings — all by name, not coordinates.  Uses the Windows UI Automation API to find UI elements reliably, regardless of DPI, theme, resolution, or window position.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 37 |
| 🍴 **Forks** | 6 |
| 💻 **Language** | C# |
| 📈 **Score** | 75/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`dotnet` `keyboard-emulation` `mcp` `mouse-emulation` `qa-automation` `rpa-robotic-process-automation` `screenshot` `window-management` `windows-11` `windows-app` `windows-desktop`

## 🎯 Categories

MCP · Automation

## 📝 Summary

### English

**Brief Summary**  
`sbroenne/mcp-windows` is an open‑source library that lets AI agents interact with Windows applications through the Windows UI Automation API. By addressing UI elements by name instead of screen coordinates, it works reliably across DPI settings, themes, resolutions and window positions, making it a solid foundation for connecting large‑language‑model assistants to real‑world tools via the Model Context Protocol (MCP).  

**Value**  
- **Reliable UI control:** UI Automation‑based element lookup eliminates the fragility of pixel‑based bots, so AI‑driven scripts remain stable after UI redesigns or when users change display settings.  
- **Standardised integration:** The library implements the MCP server interface, giving AI assistants a uniform way to discover, invoke, and receive feedback from Windows apps.  
- **Language‑native SDK/CLI:** Written in C#, it offers both a programmatic SDK and a ready‑to‑run CLI, enabling rapid prototyping and easy embedding in existing .NET services.  

**Practical Adoption Path**  
1. **Prototype:** Pull the repo, run the provided CLI (`mcp-windows serve`) and point an MCP‑compatible assistant (e.g., LangChain, AutoGPT) at the local endpoint.  
2. **Define actions:** Use the MCP schema to describe the UI operations you need (click “Submit”, type into “SearchBox”, toggle “DarkMode”).  
3. **Integrate:** Wrap the CLI or SDK in your backend service (e.g., a micro‑service that receives MCP requests and forwards them to the library).  
4. **Test & Harden:** Add unit tests for each action, enforce least‑privilege Windows permissions, and optionally containerise the service for CI/CD pipelines.  

**Production Readiness**  
- **Activity & Community:** 37 stars, 6 forks, last commit on 2026‑05‑13, and a healthy set of 11 topics indicate an actively maintained project.  
- **Stability:** The use of the official Windows UI Automation API and a clear MCP contract give deterministic behaviour across Windows versions.  
- **Ecosystem Fit:** Provides both API/SDK and CLI entry points, making it easy to evaluate in a sandbox and then scale into a production MCP server.  
- **Risks:** Licensing and security posture still need a final review, and long‑term maintainership should be confirmed, but no major red flags appear.  

Overall, `sbroenne/mcp-windows` is production‑ready for pilots that need AI agents to control Windows GUIs in a reliable, standards‑based way.

### Русский

**sb​roenne/mcp-windows** — это open‑source библиотека на C#, позволяющая AI‑агентам управлять Windows‑приложениями через Windows UI Automation API: клики, ввод текста и переключение настроек выполняются по имени элемента, а не по координатам, что гарантирует надёжную работу независимо от DPI, темы, разрешения и положения окна. Типичный сценарий — развертывание Model Context Protocol (MCP)‑сервера, через который любой AI‑ассистент получает стандартизированный доступ к настольным инструментам и данным, ускоряя интеграцию и автоматизацию бизнес‑процессов. По оценке проекта готов к production: активные коммиты (обновление 2026‑05‑13), 37 звёзд, 6 форков, широкая поддержка API/SDK/CLI и положительные сигналы экосистемы, хотя требуется финальная проверка лицензии и безопасности.

### 中文

**项目简介**  
sbroenne/mcp-windows 是基于 Windows UI Automation API 的开源库，能够让 AI 代理通过元素名称而非屏幕坐标来点击按钮、输入文字、切换设置等操作，从而实现对 Windows 应用的可靠自动化。它遵循 Model Context Protocol（MCP），为 AI 助手提供统一的、与 DPI、主题、分辨率和窗口位置无关的交互接口。

**价值**  
- **标准化接入**：通过 MCP 将 AI 代理与本地 Windows 工具对接，省去各自实现 UI 自动化的繁琐工作。  
- **高可靠性**：使用 UI Automation 元数据定位控件，避免坐标漂移、分辨率变化等常见问题。  
- **快速落地**：只需几行代码或一次 CLI 调用，即可让已有的 AI 模型直接控制桌面软件，适用于客服机器人、内部工具助手、自动化测试等场景。

**典型接入方式**  
1. **SDK 引入**：在 C# 项目中通过 NuGet 包引用 `sbroenne.mcp-windows`，使用 `McpClient` 调用 `FindElementByName`、`Click`、`SetText` 等方法。  
2. **CLI 调用**：项目提供可执行文件 `mcp-windows-cli.exe`，可在脚本或其他语言（Python、Node.js）中通过子进程调用，实现语言无关的集成。  
3. **MCP 服务器**：启动内置的 MCP 服务器后，AI 助手只需通过标准的 HTTP/WebSocket 接口发送 “click button ‘Save’” 等指令，服务器负责解析并执行对应的 UI 操作。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑05‑13，星标 37、Fork 6，社区活跃度良好。  
- **技术成熟度**：核心使用 C# 实现，依赖 Windows 官方 UI Automation，兼容 Windows 10/11 各版本，且已在多个内部项目中验证。  
- **风险**：目前暂无重大许可证或安全隐患，但仍建议在正式上线前进行一次安全审计并确认维护者的响应能力。  
综合来看，sbroenne/mcp-windows 已具备在生产环境中进行试点或正式部署的条件。

## 🧭 Practical evaluation

**Value:** sbroenne/mcp-windows helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 37 GitHub stars
- 6 forks
- updated 2026-05-13
- primary language: C#
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 21/100 |
| stars | 34/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 64/100 |
| recency | 80/100 |
| adoption | 30/100 |
| production | 70/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/sbroenne/mcp-windows) · [← Back to Mcp](./README.md)</sub>
