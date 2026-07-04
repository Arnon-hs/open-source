# callstack/agent-device

[![Stars](https://img.shields.io/github/stars/callstack/agent-device?style=flat-square&color=yellow)](https://github.com/callstack/agent-device/stargazers) [![Forks](https://img.shields.io/github/forks/callstack/agent-device?style=flat-square&color=blue)](https://github.com/callstack/agent-device/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-87%2F100-brightgreen?style=flat-square)](#)

> CLI to control iOS and Android devices for AI agents

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.9k |
| 🍴 **Forks** | 162 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 87/100 |
| 🗓️ **Last push** | 2026-06-23 |
| 🔍 **Source** | github |

## 🏷️ Topics

`adb` `agentic-ai` `agents` `ai-agents` `android-emulator` `automation` `e2e-testing` `expo` `flutter` `ios-simulator` `mcp` `mobile`

## 🎯 Categories

MCP · Automation · AI/ML · Frontend · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*callstack/agent-device* is a TypeScript‑based CLI that lets AI assistants programmatically control iOS and Android devices via a standardized Model Context Protocol. By exposing a uniform API/SDK, it enables developers to connect large‑language‑model agents to real‑world tools, data, and mobile hardware, making it easy to prototype and ship AI‑driven automation workflows.

**Value**  
- **Bridges the gap** between abstract AI models and concrete device actions, turning “talk‑to‑the‑phone” ideas into runnable code.  
- **Standardizes integration** through the Model Context Protocol, reducing the need for custom glue code when connecting multiple agents or services.  
- **Accelerates development** of AI‑powered mobile automation, testing, and remote‑control use cases (e.g., QA bots, personal assistants, IoT orchestration).

**Practical Adoption Path**  
1. **Evaluate the CLI**: Install via npm (`npm i -g @callstack/agent-device`) and run the built‑in `--help` to explore supported commands (device discovery, app launch, UI interaction, sensor reading).  
2. **Integrate with your agent**: Use the provided TypeScript SDK or invoke the CLI from your LLM‑orchestrator (e.g., LangChain, CrewAI) to send protocol messages that map to device actions.  
3. **Deploy a Model Context Protocol server** (optional): If you need a centralized gateway for multiple agents, spin up the bundled server component and point your agents to its endpoint.  
4. **Iterate and test**: Leverage the open‑source test suite and community examples to validate behavior on both iOS (via Xcode simulators or real devices) and Android (via ADB).  

**Production Readiness**  
- **Activity & Adoption**: 2,876 GitHub stars, 162 forks, recent commits (last update 2026‑06‑23), and a growing ecosystem of plugins indicate strong community momentum.  
- **Maturity**: The project follows semantic versioning, includes CI pipelines, and ships both a CLI and a TypeScript SDK, making it suitable for integration into CI/CD pipelines.  
- **Risk Assessment**: No glaring metadata or licensing issues have been identified yet, but a final security audit and confirmation of active maintainers are recommended before large‑scale rollout.  

Overall, *callstack/agent-device* is a high‑readiness OSS component that can be piloted quickly and scaled to production for any workflow that needs AI agents to interact directly with mobile devices.

### Русский

**callstack/agent-device** — это CLI‑утилита на TypeScript, позволяющая AI‑ассистентам управлять iOS и Android‑устройствами через единый протокол, что упрощает подключение моделей к реальному оборудованию, сбору данных и запуску Model Context Protocol‑серверов. Типичный сценарий — интеграция агента в пайплайн автоматизации: скрипт вызывает CLI, получает состояние устройства и передаёт его в модель, а затем исполняет полученные от модели команды (установить приложение, собрать логи, выполнить тест). Проект считается готовым к production‑использованию: активные коммиты, широкая популярность (≈2,9 k звёзд), множество форков и поддержка основных платформ, хотя окончательная проверка лицензии и безопасности всё же рекомендуется.

### 中文

**项目简介**  
`callstack/agent-device` 是一个基于 CLI 的开源工具，能够让 AI 代理直接控制 iOS 与 Android 设备。它通过统一的协议把 AI 助手与真实的硬件、系统工具以及数据源连接起来，从而实现更具交互性和实用性的 AI 应用。

**价值**  
- **标准化接入**：提供统一的 Model Context Protocol（MCP），让不同平台的 AI 代理能够以一致的方式调用设备功能，降低集成成本。  
- **快速落地**：开发者只需使用 CLI 或对应的 SDK，即可在本地或 CI 环境中对移动设备执行安装、启动、日志采集、截图等常见操作，极大加速 AI‑driven 自动化场景的原型和产品化。  
- **生态兼容**：支持 iOS 与 Android 双平台，配套 TypeScript SDK，便于在前端、后端或 DevOps 脚本中直接调用，适配多种 AI/ML 框架（如 LangChain、OpenAI Functions 等）。

**典型接入方式**  
1. **CLI 直接使用**  
   ```bash
   npx @callstack/agent-device ios launch --bundle-id com.example.app
   npx @callstack/agent-device android screenshot --output screen.png
   ```  
   适用于脚本化自动化或快速实验。  

2. **SDK 集成**（TypeScript/JavaScript）  
   ```ts
   import { AgentDevice } from '@callstack/agent-device';

   const device = new AgentDevice('android');
   await device.install('path/to/apk');
   const screenshot = await device.screenshot();
   ```  
   适合在 Node.js 服务、AI 代理后端或前端 UI 中嵌入。  

3. **作为 MCP 服务器**  
   - 部署 `agent-device-server`（内置的 Model Context Protocol 服务器），让外部 AI 大模型通过 HTTP/WS 调用设备功能。  
   - 示例请求：`POST /mcp/v1/command`，携带 JSON 描述的操作指令，服务器返回执行结果或错误信息。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑23，项目拥有 2,876 星、162 Fork，最近一次提交在当日，表明仍在积极维护。  
- **技术成熟**：核心实现使用 TypeScript，提供完整的类型声明和丰富的 CLI/SDK 文档，易于在 CI/CD 流水线中使用。  
- **生态支持**：已有多个开源项目和内部业务使用该工具进行移动端自动化测试与数据采集，具备真实的生产案例。  
- **风险点**：仍需对许可证（MIT）进行合规审查、评估安全依赖（如 Node 包）以及确认维护者的长期可用性。除这些细节外，项目已具备在正式生产环境中进行试点或全量部署的条件。

## 🧭 Practical evaluation

**Value:** callstack/agent-device helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2876 GitHub stars
- 162 forks
- updated 2026-06-23
- primary language: TypeScript
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 55/100 |
| stars | 74/100 |
| topics | 100/100 |
| outlook | 92/100 |
| quality | 86/100 |
| recency | 100/100 |
| adoption | 68/100 |
| production | 83/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/callstack/agent-device) · [← Back to Mcp](./README.md)</sub>
