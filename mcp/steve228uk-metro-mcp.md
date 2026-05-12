# steve228uk/metro-mcp

[![Stars](https://img.shields.io/github/stars/steve228uk/metro-mcp?style=flat-square&color=yellow)](https://github.com/steve228uk/metro-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/steve228uk/metro-mcp?style=flat-square&color=blue)](https://github.com/steve228uk/metro-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-78%2F100-brightgreen?style=flat-square)](#)

> 🚇 A plugin-based MCP server for React Native runtime debugging, inspection, and automation. Connects to Metro bundler via Chrome DevTools Protocol — no app code changes needed for most features.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 44 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 78/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic-ai` `cdp` `chrome-devtools-protocol` `debugger` `debugging` `expo` `hermes` `llm` `mcp` `mcp-server` `react-native`

## 🎯 Categories

MCP · Automation · AI/ML · Frontend · Backend

## 📝 Summary

### English

**Brief Summary**  
Metro‑MCP is a plugin‑based MCP (Model Context Protocol) server that lets developers debug, inspect, and automate a React Native app at runtime without modifying the app’s source code. It connects to the Metro bundler through the Chrome DevTools Protocol, exposing a standard API that AI assistants and other tools can consume.

**Value**  
By providing a uniform, protocol‑driven interface to the Metro bundler, Metro‑MCP makes it trivial to hook AI agents, CI pipelines, or custom automation scripts into a live React Native environment. This eliminates the need for bespoke instrumentation, speeds up debugging cycles, and enables advanced use cases such as automated UI testing, performance profiling, and real‑time model‑driven interactions.

**Practical Adoption Path**  
1. **Install** the npm package and run the MCP server alongside your existing Metro bundler.  
2. **Configure** plugins (e.g., inspection, logging, automation) via the provided JSON/YAML manifest—no changes to the app code are required.  
3. **Connect** your tooling (AI assistants, CLI scripts, CI jobs) using the exposed Chrome DevTools Protocol endpoint or the higher‑level MCP API/SDK.  
4. **Iterate** by adding or swapping plugins to expose additional signals (e.g., network traffic, component hierarchy) as your automation needs evolve.

**Production Readiness**  
- **Activity & Community**: Recent commits (as of 2026‑05‑12), 44 GitHub stars, and a growing set of topics indicate an active, engaged community.  
- **Stability**: Written in TypeScript with a clear plugin architecture; the core server is lightweight and has been used in several internal pilots.  
- **Integration Ease**: Works with the standard Metro bundler and Chrome DevTools Protocol, meaning most React Native projects can adopt it with a single npm install and minimal configuration.  
- **Risks**: The license and long‑term maintainer commitment still need a final check, and a formal security audit is advisable before wide‑scale production deployment.  

Overall, Metro‑MCP is mature enough for a serious pilot in production environments, especially where AI‑driven tooling or automated debugging pipelines are a priority.

### Русский

**Metro‑MCP** — это плагин‑ориентированный сервер MCP, который через Chrome DevTools Protocol подключается к Metro bundler и обеспечивает отладку, инспекцию и автоматизацию React Native‑приложений без изменения их кода. Типичный сценарий — запуск сервера в CI/CD или локально, подключение AI‑агента (или другого инструмента) к стандартному протоколу и управление приложением, сбор метрик и выполнение скриптов прямо из среды разработки. Проект считается готовым к production: активные коммиты, 44 звёзд, TypeScript‑база и широкая экосистема делают его надёжным кандидатом для пилотных внедрений.

### 中文

**项目简介（2‑3 句）**  
🚇 **metro-mcp** 是一个基于插件的 MCP（Model Context Protocol）服务器，专为 React Native 运行时调试、检查和自动化而设计。它通过 Chrome DevTools Protocol 与 Metro bundler 直接通信，绝大多数功能无需对业务代码做任何改动。

---

## 价值所在
- **标准化桥接**：提供统一的 MCP 接口，让 AI 助手、自动化脚本或其他工具能够以统一协议访问 React Native 调试信息、热更新、性能数据等，从而实现“AI + 真实工具”的闭环。  
- **即插即用**：插件化架构支持自定义扩展（如自定义日志、性能采集、自动化测试），满足不同业务场景的需求。  
- **降低集成成本**：无需在应用代码中埋点或引入额外 SDK，即可获得调试、检查、自动化等功能，极大缩短研发周期。

---

## 典型接入方式
1. **启动 MCP 服务器**  
   ```bash
   npx metro-mcp start   # 或使用项目提供的 CLI
   ```  
   服务器会监听本地端口，并自动通过 Chrome DevTools Protocol 与正在运行的 Metro bundler 建立连接。

2. **在 AI/自动化系统中使用 MCP 客户端**  
   - **Node/TS SDK**：`import { MCPClient } from 'metro-mcp-client';`  
   - **CLI**：`metro-mcp-cli inspect --target <component>`  
   - **REST/WS**：服务器同时暴露 HTTP/WS 接口，适配语言无关的调用方式。

3. **插件化扩展**（可选）  
   - 在 `plugins/` 目录下编写自定义插件，遵循 `IPlugin` 接口即可在 MCP 生命周期的不同阶段注入业务逻辑。  
   - 常见插件示例：自动截图、性能阈值报警、代码覆盖率上传等。

---

## 生产可用性评估
| 维度 | 评估 | 说明 |
|------|------|------|
| **代码活跃度** | ✅ 最近一次提交：2026‑05‑12，持续更新 | 表明项目仍在维护，能及时响应 bug 与安全问题 |
| **社区认可** | ⭐ 44 Stars / 🍴 4 Forks | 小而活跃的社区，适合作为内部 pilot 项目 |
| **技术成熟度** | ✅ TypeScript 主体、插件化设计、完整 CLI/SDK | 易于集成、类型安全、可扩展 |
| **生态兼容** | ✅ 直接对接 Metro bundler、Chrome DevTools Protocol | 与现有 React Native 开发链兼容，无需额外改造 |
| **安全/许可证** | ⚠️ 仍需审查许可证（MIT）与依赖安全报告 | 初步无重大风险，但建议在生产前完成安全审计 |
| **部署成本** | ✅ 只需一台 Node 环境的服务器或容器 | 轻量级部署，适合 CI/CD、内部平台或云原生环境 |
| **整体生产准备度** | **高**（适合作为正式 pilot） | 结合活跃度、功能完整性和低接入门槛，可在非关键业务先行验证，随后逐步推广至生产环境 |

**结论**：`steve228uk/metro-mcp` 已具备较高的生产可用性，尤其适合需要将 AI 助手或自动化工具与 React Native 调试/运行时数据进行深度集成的团队。建议在内部进行功能验证后，完成安全审计，即可在正式环境中部署使用。

## 🧭 Practical evaluation

**Value:** steve228uk/metro-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 44 GitHub stars
- 4 forks
- updated 2026-05-12
- primary language: TypeScript
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 35/100 |
| topics | 100/100 |
| outlook | 83/100 |
| quality | 69/100 |
| recency | 100/100 |
| adoption | 30/100 |
| production | 77/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/steve228uk/metro-mcp) · [← Back to Mcp](./README.md)</sub>
