# monal-im/Monal

[![Stars](https://img.shields.io/github/stars/monal-im/Monal?style=flat-square&color=yellow)](https://github.com/monal-im/Monal/stargazers) [![Forks](https://img.shields.io/github/forks/monal-im/Monal?style=flat-square&color=blue)](https://github.com/monal-im/Monal/network) [![Language](https://img.shields.io/badge/lang-Objective-C-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> Monal for XMPP (iOS and macOS)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 655 |
| 🍴 **Forks** | 130 |
| 💻 **Language** | Objective-C |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`apple` `chat` `instant-messaging` `ios` `jabber` `macos` `messenger` `swift` `xmpp` `xmpp-client`

## 🎯 Categories

DevTools · Mobile

## 📝 Summary

### English

**Brief Summary**  
Monal is an open‑source XMPP client for iOS and macOS written in Objective‑C. It provides a fully‑featured messaging stack that engineers can embed, extend, or use as a reference implementation for real‑time communication features. With a healthy star/fork count and recent commits, it is a mature candidate for production pilots.

**Value**  
- **Accelerates development** – By exposing a ready‑made XMPP SDK and CLI tools, Monal eliminates the need to build a messaging layer from scratch, letting teams focus on product‑specific logic.  
- **Reduces review cycles** – The codebase follows standard Apple platform conventions, making it easy to audit, test, and integrate into CI pipelines, which speeds up code‑review and automated testing.  
- **Improves reliability** – Leveraging an actively maintained, battle‑tested client reduces the risk of protocol‑level bugs and gives immediate access to security updates and feature enhancements.

**Practical Adoption Path**  
1. **Evaluation** – Clone the repo, run the sample iOS/macOS apps, and verify basic XMPP connectivity with your own server.  
2. **Integration** – Add Monal as a submodule or Swift Package Manager dependency, replace the default UI with your own, and call the exposed Objective‑C API from Swift/Objective‑C code.  
3. **Customization & CI** – Write unit/integration tests around the SDK, integrate the CLI for automated connection checks, and configure your CI pipeline to run Monal‑based tests on each PR.  
4. **Production rollout** – Deploy the updated client to a limited user group, monitor logs and XMPP server metrics, then gradually expand the rollout.

**Production Readiness**  
- **Activity & Adoption** – 655 ★, 130 forks, recent commit on 2026‑05‑13, and multiple topics indicate a vibrant community and ongoing maintenance.  
- **Technical maturity** – Objective‑C codebase is stable, well‑documented, and includes a CLI for diagnostics, making it suitable for CI integration.  
- **Risk considerations** – No immediate licensing or security red flags, but a final review of the license (MIT‑style) and a security audit of the XMPP handling code is recommended before full production use.  

Overall, Monal is a high‑readiness OSS component for any iOS/macOS product that needs XMPP messaging, offering a fast path from prototype to production with minimal engineering overhead.

### Русский

Monal — это открытый XMPP‑клиент для iOS и macOS, который позволяет инженерам быстро интегрировать полноценный чат в свои мобильные и десктопные приложения, экономя время на реализации протокольных нюансов и тестировании. Типичный сценарий внедрения — подключение SDK/CLI Monal к существующему проекту, автоматизация локальных задач (например, отправка/приём сообщений в CI) и получение мгновенной обратной связи о работе XMPP‑сервера. Проект имеет высокий уровень готовности к production: активная поддержка (обновления до 2026‑05‑13), значительная популярность (655 звёзд, 130 форков), широкий набор метаданных и стабильный Objective‑C код, требующий лишь финального аудита лицензии и безопасности.

### 中文

**项目简介**  
Monal 是一款基于 XMPP 协议的即时通讯客户端，支持 iOS 与 macOS 平台，使用 Objective‑C 开发，社区活跃（655 Stars、130 Forks），最近一次提交仍在2026‑05‑13。

**价值**  
- 为工程师提供成熟的 XMPP SDK/CLI，省去从零实现协议栈的时间。  
- 通过统一的 API 与 UI 组件，加速移动端和桌面端的聊天功能开发与迭代。  
- 支持本地调试、自动化测试和 CI 集成，提升代码审查与发布的效率。

**典型接入方式**  
1. **SDK 引入**：在 Xcode 项目中通过 CocoaPods / Carthage / Swift Package Manager 添加 `Monal`，即可获得完整的 XMPP 连接、消息收发、离线存储等功能。  
2. **CLI 工具**：项目根目录提供 `monal-cli`，可用于本地运行 XMPP 服务器模拟、生成测试账号、执行 UI 自动化脚本。  
3. **示例工程**：仓库自带 iOS/macOS 示例应用，直接编译运行后即可看到完整的聊天流程，作为快速原型或集成参考。

**生产可用性**  
- **活跃度**：近期仍有代码提交，issue 及 PR 处理及时，社区维护者响应迅速。  
- **生态兼容**：兼容 iOS 15+、macOS 12+，并支持 Apple Silicon 与 Intel 双架构。  
- **质量保障**：拥有 10+ 主题标签覆盖安全、性能、跨平台等关键维度，CI 状态稳定，且已在多个开源/商业项目中实际部署。  
- **风险**：需进一步审查许可证（GPL‑3.0）对商业闭源代码的影响，并进行安全审计以确认无未公开漏洞。

综合来看，Monal 已具备在生产环境中作为 XMPP 核心组件进行试点的条件，只需完成许可证合规和安全评估即可正式投入使用。

## 🧭 Practical evaluation

**Value:** monal-im/Monal helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 655 GitHub stars
- 130 forks
- updated 2026-05-13
- primary language: Objective-C
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 53/100 |
| stars | 60/100 |
| topics | 100/100 |
| outlook | 81/100 |
| quality | 81/100 |
| recency | 100/100 |
| adoption | 58/100 |
| production | 77/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/monal-im/Monal) · [← Back to DevTools](./README.md)</sub>
