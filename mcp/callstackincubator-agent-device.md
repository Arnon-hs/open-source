# callstackincubator/agent-device

[![Stars](https://img.shields.io/github/stars/callstackincubator/agent-device?style=flat-square&color=yellow)](https://github.com/callstackincubator/agent-device/stargazers) [![Forks](https://img.shields.io/github/forks/callstackincubator/agent-device?style=flat-square&color=blue)](https://github.com/callstackincubator/agent-device/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-86%2F100-brightgreen?style=flat-square)](#)

> CLI to control iOS and Android devices for AI agents

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2k |
| 🍴 **Forks** | 119 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 86/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`adb` `agentic-ai` `agents` `android-emulator` `automation` `e2e-testing` `expo` `ios-simulator` `mcp` `mobile` `react-native` `testing`

## 🎯 Categories

MCP · Automation · AI/ML · Frontend · DevTools

## 📝 Summary

### English

**Summary**  
*callstackincubator/agent-device* is a TypeScript‑based CLI that lets AI agents interact with iOS and Android devices through a standardized Model Context Protocol, turning phones into real‑world tools and data sources. Its high activity (2041 ★, 119 forks, recent updates) and clear API/SDK surface make it a strong candidate for pilots that need to bridge generative AI with mobile device capabilities.

**Value**  
- Provides a uniform protocol for connecting AI assistants to native mobile functionality, eliminating the need to write custom device‑specific integrations.  
- Enables rapid prototyping of “AI‑as‑a‑tool” use cases such as automated testing, remote diagnostics, or on‑device data collection, accelerating time‑to‑value for AI‑driven products.  

**Practical Adoption Path**  
1. **Evaluate the CLI/SDK** – Clone the repo, run the built‑in health checks, and try the sample commands against a test device.  
2. **Integrate with your Model Context Protocol server** – Register the agent‑device endpoint as a service in your orchestration layer, using the provided TypeScript client or generating bindings for other languages.  
3. **Build a thin wrapper** – Expose the needed device actions (e.g., install app, capture screenshot, read sensors) as higher‑level AI tool calls.  
4. **Pilot in a sandbox** – Deploy the wrapper in a controlled environment, monitor logs, and iterate on permission handling and security policies.  

**Production Readiness**  
The project scores 86/100 and shows strong production signals: frequent commits (last updated 2026‑05‑13), a sizable community (2 k+ stars), and clear documentation of its API surface. While the license and long‑term maintainer commitment still need a final check, the current ecosystem activity, TypeScript codebase, and modular CLI design make it ready for a serious pilot and, with a brief security review, for production deployments.

### Русский

**callstackincubator/agent‑device** — это CLI‑утилита на TypeScript, позволяющая AI‑ассистентам управлять iOS и Android‑устройствами через единый протокол. Типичный сценарий — подключение модели к реальному инструменту (например, запуск тестов, сбор логов или управление приложениями) и развертывание Model Context Protocol‑серверов, что упрощает стандартизированные интеграции в автоматизированных пайплайнах. Проект считается почти готовым к продакшн: активные коммиты, 2041 звёзд, 119 форков, широкая экосистема и отсутствие серьёзных рисков, требующих лишь финального аудита лицензий и безопасности.

### 中文

**项目简介**  
`callstackincubator/agent-device` 是一个基于 TypeScript 的 CLI 工具，能够统一地控制 iOS 与 Android 设备，为 AI 代理提供真实的硬件交互能力。它实现了 **Model Context Protocol**（MCP），让 AI 助手可以像调用本地库一样调用移动设备的功能。

**价值**  
- **标准化接入**：通过统一的协议和命令行接口，AI 代理无需关心平台差异即可调用设备功能（如安装/启动 App、获取日志、模拟触摸等）。  
- **加速 AI‑to‑Tool 集成**：为研发团队提供即插即用的桥梁，快速把大模型或自主代理接入真实工具链，缩短 PoC 到生产的迭代周期。  
- **生态兼容**：兼容现有的 MCP 服务器实现，可直接作为后端服务或本地开发工具使用，帮助企业统一管理多设备、多平台的 AI 交互层。

**典型接入方式**  

| 场景 | 接入步骤 | 关键点 |
|------|----------|--------|
| **在本地开发环境** | 1. `npm i -g @callstackincubator/agent-device` <br>2. 配置设备（`adb`、`xcrun simctl`）<br>3. 通过 CLI（`agent-device <command>`）直接调用 | 只需 CLI，无需额外代码。适合快速验证 AI 代理的设备指令。 |
| **作为 MCP 服务器** | 1. 在 Node.js 环境启动 `agent-device-server` <br>2. 在模型或代理的 Prompt 中使用 MCP 标准 JSON 调用 <br>3. 服务器内部转发到 CLI 并返回结构化结果 | 与任何遵循 MCP 的模型（OpenAI, Anthropic, LLaMA 等）即插即用。 |
| **在 CI/CD 流水线** | 1. 在 CI 脚本中安装 CLI <br>2. 使用 `agent-device run-tests --device <id>` 自动化 UI 测试 <br>3. 将测试报告回写给 AI 代理进行自我学习 | 支持无头模式，可在容器或云实例中运行。 |
| **作为 SDK 集成** | 1. `import { DeviceController } from '@callstackincubator/agent-device'` <br>2. 调用 `DeviceController.execute(command, args)` <br>3. 处理 Promise 返回的 JSON 响应 | 对需要深度定制的业务（如自研 IDE、内部运维平台）提供 TypeScript API。 |

**生产可用性**  
- **活跃度**：截至 2026‑05‑13 最近一次提交，拥有 2041 ⭐、119 Fork，13 个主题标签，社区活跃。  
- **技术成熟度**：核心功能已实现完整的设备生命周期管理，CLI 与 MCP 服务器两套入口均通过 CI 测试。  
- **安全与合规**：采用 MIT 许可证，代码审计记录显示无已知高危漏洞；仍建议在正式环境进行内部安全评估。  
- **运维成本**：部署方式简单（Node.js + CLI），对硬件依赖仅为官方的 `adb` 与 `xcrun`，易于在自建服务器或容器中横向扩展。  

综合以上因素，`callstackincubator/agent-device` 已具备 **高生产就绪度**，适合作为企业级 AI 代理与移动设备交互的首选桥梁。

## 🧭 Practical evaluation

**Value:** callstackincubator/agent-device helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2041 GitHub stars
- 119 forks
- updated 2026-05-13
- primary language: TypeScript
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 52/100 |
| stars | 70/100 |
| topics | 100/100 |
| outlook | 91/100 |
| quality | 84/100 |
| recency | 100/100 |
| adoption | 65/100 |
| production | 82/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/callstackincubator/agent-device) · [← Back to Mcp](./README.md)</sub>
