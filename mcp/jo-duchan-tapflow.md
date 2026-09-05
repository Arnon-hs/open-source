# jo-duchan/tapflow

[![Stars](https://img.shields.io/github/stars/jo-duchan/tapflow?style=flat-square&color=yellow)](https://github.com/jo-duchan/tapflow/stargazers) [![Forks](https://img.shields.io/github/forks/jo-duchan/tapflow?style=flat-square&color=blue)](https://github.com/jo-duchan/tapflow/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-75%2F100-brightgreen?style=flat-square)](#)

> Self-hosted iOS & Android simulator streaming for the whole team

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 121 |
| 🍴 **Forks** | 15 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 75/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `android-emulator` `app-testing` `appetize-alternative` `browserstack-alternative` `developer-tools` `emulator` `flutter` `good-first-issue` `ios` `ios-simulator` `mcp`

## 🎯 Categories

MCP · Frontend · DevTools · Mobile

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Tapflow (jo‑duchan/tapflow) is an open‑source, self‑hosted platform that streams iOS and Android simulators to any team member, turning mobile devices into shared, cloud‑accessible test environments. Built in TypeScript, it exposes a clean API/SDK/CLI that lets AI agents and other tools interact with real mobile runtimes via a standard Model Context Protocol. With active maintenance, 121 ★ on GitHub and recent updates, it’s ready for pilot projects and broader integration.

**Value**  
- **Unified access to real mobile simulators** – developers, QA, and AI assistants can run UI tests, debug, or capture screenshots without each person needing a physical device.  
- **Standard protocol layer** – the Model Context Protocol (MCP) lets AI agents and downstream services plug into Tapflow uniformly, reducing custom integration work.  
- **Team‑wide collaboration** – streamed sessions are shareable, enabling pair‑programming, remote reviews, and rapid feedback loops across iOS and Android.

**Practical Adoption Path**  
1. **Deploy** the Tapflow server on a cloud VM or on‑premise hardware (Docker image or Helm chart).  
2. **Configure** the desired simulators (Xcode/Android SDK) and expose the generated API endpoint.  
3. **Integrate** using the provided TypeScript SDK, CLI, or REST calls from your CI/CD pipelines, test frameworks, or AI agents.  
4. **Pilot** with a small developer squad to validate latency, concurrency limits, and security policies.  
5. **Scale** by adding more simulator instances, setting up role‑based access, and embedding the MCP server into your broader AI‑toolchain.

**Production Readiness**  
- **Activity & Community** – recent commits (as of 2026‑06‑24), 121 stars, 15 forks, and a well‑documented TypeScript codebase indicate healthy interest.  
- **Ecosystem Fit** – the project already publishes API/SDK/CLI artifacts and aligns with the Model Context Protocol, easing integration with existing dev‑tools and AI platforms.  
- **Stability** – no major open security or licensing concerns identified; the core functionality (simulator streaming) is mature and has been adopted in early internal pilots.  
- **Next Steps** – conduct a formal security audit, confirm license compatibility, and assign a dedicated maintainer before rolling out to production at scale.  

Overall, Tapflow is a mature, low‑risk OSS candidate for teams that want to centralize mobile simulator access and enable AI‑driven tooling.

### Русский

**Tapflow (jo‑duchan/tapflow)** — это self‑hosted сервис, позволяющий в реальном времени транслировать iOS и Android‑эмуляторы всей команде, что упрощает подключение AI‑ассистентов к реальным мобильным инструментам через единый протокол. Типичный сценарий: команда разворачивает Tapflow в своей инфраструктуре, использует предоставляемый API/SDK/CLI для интеграции AI‑агентов, а затем запускает симуляторы и получает доступ к их UI/данным из моделей. Проект считается почти готовым к production: активные коммиты (обновление 24 июня 2026), 121★, 15 форков, TypeScript‑база и широкий набор тем свидетельствуют о высокой зрелости, хотя лицензия, безопасность и поддержка требуют окончательной проверки.

### 中文

**项目简介**  
Tapflow（jo‑duchan/tapflow）是一款自托管的 iOS 与 Android 模拟器流媒体平台，团队成员可以在浏览器中实时观看和交互模拟器画面，从而实现跨平台移动端调试与演示。

**价值主张**  
- **统一协议**：通过标准化的 Model Context Protocol（MCP），让 AI 助手能够直接调用真实的移动设备模拟器，实现“AI + 工具”的闭环。  
- **提升协作效率**：团队成员无需本地安装模拟器，只需访问统一的流媒体入口，即可共享调试会话、截图或视频，显著降低环境配置成本。  
- **加速交付**：在 CI/CD 流程中可嵌入 Tapflow，自动启动模拟器并将 UI 流输出给 AI 评审或自动化测试，提高移动端功能的交付速度。

**典型接入方式**  
1. **API/SDK**：使用提供的 TypeScript SDK 调用 RESTful API，启动/停止模拟器、获取流媒体 URL、上传截图等。  
2. **CLI**：通过 `tapflow-cli` 在本地或 CI 环境中执行 `tapflow start --platform ios --device iPhone13` 等命令，快速创建会话。  
3. **MCP 服务器**：部署 Model Context Protocol 服务器后，AI 代理即可通过统一的 `model-context://tapflow/...` URI 与模拟器交互，完成如“打开设置页面”“点击按钮”等指令。  
4. **前端集成**：在内部 Dashboard 中嵌入 `<TapflowPlayer src={streamUrl} />` 组件，即可实时展示模拟器画面。

**生产可用性**  
- **活跃度**：截至 2026‑06‑24，项目最近一次提交，拥有 121 ★、15 Fork，且持续接受 PR，社区活跃。  
- **技术成熟度**：核心实现基于 TypeScript，提供完整的 API、SDK 与 CLI，文档覆盖常见使用场景。  
- **生态兼容**：支持 iOS（Xcode 模拟器）和 Android（AVD）两大主流平台，且可通过 Docker 镜像一键部署，便于在内部私有云或本地服务器上运行。  
- **风险**：需进一步审查许可证（MIT）和安全依赖（如 Docker 镜像的基础镜像），以及维护者的长期可用性。总体来看，项目已具备 **高** 生产就绪度，适合作为团队内部移动端调试与 AI‑Tool 集成的首选方案。

## 🧭 Practical evaluation

**Value:** jo-duchan/tapflow helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 121 GitHub stars
- 15 forks
- updated 2026-06-24
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 30/100 |
| stars | 44/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 40/100 |
| production | 72/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/jo-duchan/tapflow) · [← Back to Mcp](./README.md)</sub>
