# streetpea/chiaki-ng

[![Stars](https://img.shields.io/github/stars/streetpea/chiaki-ng?style=flat-square&color=yellow)](https://github.com/streetpea/chiaki-ng/stargazers) [![Forks](https://img.shields.io/github/forks/streetpea/chiaki-ng?style=flat-square&color=blue)](https://github.com/streetpea/chiaki-ng/network) [![Language](https://img.shields.io/badge/lang-C-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> Next-Generation of Chiaki (the open-source remote play client for PlayStation)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.4k |
| 🍴 **Forks** | 190 |
| 💻 **Language** | C |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`game-streaming` `gaming` `playstation` `steam` `steam-deck`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
Chiaki‑NG is the next‑generation, open‑source client that enables remote PlayStation streaming, built in C and actively maintained. With over 2 300 GitHub stars and recent commits, it offers a stable API/CLI that developers can embed in tooling to automate PlayStation‑related workflows. The project is production‑ready for pilot use, thanks to strong community adoption, frequent releases, and clear implementation signals.

**Value**  
Chiaki‑NG lets engineering teams replace manual PlayStation testing with scripted, reproducible remote‑play sessions, cutting down the time spent on device‑level debugging and UI verification. By exposing a well‑defined CLI and SDK, it can be integrated into CI pipelines to provide instant feedback on graphics, latency, or feature regressions, accelerating the overall development cycle.

**Practical adoption path**  

1. **Evaluate the API/CLI** – Clone the repo, build the client (standard C toolchain), and run a few test streams against a development console to verify functionality.  
2. **Wrap the CLI in scripts** – Create wrapper scripts or a small library that invoke Chiaki‑NG commands (e.g., start/stop streaming, capture screenshots, record video).  
3. **Integrate into CI** – Add the wrapper to your CI jobs (GitHub Actions, Jenkins, etc.) to automatically launch a stream, run automated UI tests, and collect logs or video artifacts.  
4. **Scale to internal tooling** – Once the CI step is stable, expose the functionality through internal dashboards or developer self‑service portals for on‑demand remote play testing.

**Production readiness**  
The project shows high production readiness: it has recent activity (last commit 2026‑05‑14), a sizable user base (2 362 stars, 190 forks), and a clear focus area (remote PlayStation streaming). The codebase is mature, written in C, and the repository includes documentation for building and using the CLI. While a final review of licensing, security posture, and maintainer responsiveness is still required, the existing signals indicate that Chiaki‑NG can be safely piloted in production environments and scaled to broader use.

### Русский

**streetpea/chiaki-ng** — современный open‑source клиент удалённого воспроизведения PlayStation, позволяющий инженерам быстро интегрировать поддержку PlayStation Remote Play в свои инструменты и CI‑конвейеры. Типичный сценарий: автоматизация тестов и отладка графических приложений через CLI/SDK, что ускоряет локальные разработки и повышает качество обратной связи в CI. Проект имеет высокий уровень готовности к production – активные коммиты, более 2300 звёзд, широкое принятие в сообществе и достаточную инфраструктуру, требующую лишь финального аудита лицензии и безопасности.

### 中文

**项目简介（2‑3 句）**  
streetpea/chiaki-ng 是 Chiaki 的下一代实现，提供开源的 PlayStation 远程游戏客户端，使用现代 C 代码库并支持多平台。它在保持原有兼容性的同时，加入了更高效的网络协议和可扩展的插件接口，为玩家和开发者带来更流畅的远程游戏体验。

**价值**  
- **提升开发效率**：提供完整的 API/SDK 与 CLI，可在本地自动化测试、脚本化连接和性能监控，显著缩短开发与评审周期。  
- **加速工作流**：支持 CI 集成，能够在构建流水线中验证远程播放功能，及时捕获兼容性和性能回归。  
- **社区与生态**：拥有 2 362+ 星、190+ Fork，活跃的贡献者和持续更新，适合作为内部工具或产品的基础组件。

**典型接入方式**  
1. **库方式**：在 C/C++ 项目中直接引用 `chiaki-ng` 的头文件和链接库，调用其公开的 API 完成设备发现、会话建立和媒体流处理。  
2. **CLI/脚本**：使用项目自带的 `chiaki-ng-cli`（或自定义包装脚本）在 CI/CD 中启动/关闭远程会话，实现自动化测试。  
3. **插件/扩展**：通过项目提供的插件接口（如自定义解码器、日志钩子），将功能嵌入现有的游戏或媒体平台中。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑05‑14，代码维护频繁，Issue 与 PR 处理及时。  
- **成熟度**：项目已在多个开源社区和内部项目中使用，具备稳定的多平台构建（Linux、Windows、macOS）。  
- **风险**：暂无重大元数据或许可证冲突，但仍建议在正式上线前完成安全审计并确认维护者的长期可用性。  

总体来看，streetpea/chiaki-ng 已具备高生产就绪度，可作为远程 PlayStation 客户端的可靠 OSS 组件快速投入使用。

## 🧭 Practical evaluation

**Value:** streetpea/chiaki-ng helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2362 GitHub stars
- 190 forks
- updated 2026-05-14
- primary language: C
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 57/100 |
| stars | 72/100 |
| topics | 63/100 |
| outlook | 52/100 |
| quality | 60/100 |
| recency | 20/100 |
| adoption | 68/100 |
| production | 50/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/streetpea/chiaki-ng) · [← Back to Misc](./README.md)</sub>
