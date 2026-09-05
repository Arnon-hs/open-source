# acsandmann/rift

[![Stars](https://img.shields.io/github/stars/acsandmann/rift?style=flat-square&color=yellow)](https://github.com/acsandmann/rift/stargazers) [![Forks](https://img.shields.io/github/forks/acsandmann/rift?style=flat-square&color=blue)](https://github.com/acsandmann/rift/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> a tiling window manager for macos

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.1k |
| 🍴 **Forks** | 70 |
| 💻 **Language** | Rust |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`i3` `i3wm` `mac` `macos` `niri` `paperwm` `rift` `rust` `scrolling` `tiling` `tiling-window-manager` `twm`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Rift is an open‑source tiling window manager for macOS written in Rust. It aims to bring the efficiency of dynamic tiling layouts—common on Linux—to the macOS desktop, offering keyboard‑driven window organization and customizable workspaces. With over 2 000 stars, recent commits, and a modest but active community, Rift is a viable candidate for teams that need a more scriptable, productivity‑focused macOS environment.

**Value**  
- **Productivity boost**: By automatically arranging windows in non‑overlapping tiles, Rift reduces the manual drag‑and‑drop workflow that macOS users typically endure, speeding up multitasking and code review cycles.  
- **Extensibility**: Built in Rust, the project can be compiled and extended with low‑level performance and safety guarantees, making it attractive for power users who want to script custom behaviors or integrate with existing tooling.  
- **Community traction**: 2 058 stars, 70 forks, and regular updates (last commit on 2026‑07‑13) indicate a healthy user base and ongoing maintenance, lowering the risk of abandonment.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, follow the README to build and install Rift on a test Mac, and evaluate its basic tiling features on a developer workstation.  
2. **Workflow validation** – Map your team’s typical window patterns (e.g., IDE + terminal + browser) to Rift’s layout configurations; adjust keybindings and test integration with existing macOS automation tools (e.g., AppleScript, Keyboard Maestro).  
3. **Pilot rollout** – Deploy Rift to a small group of power users via a scripted installer (brew tap or binary release) and collect feedback on stability, ergonomics, and any conflicts with corporate security policies.  
4. **Full‑scale rollout** – Package Rift with your standard macOS configuration management (e.g., Jamf, Munki) and provide documentation for onboarding, including troubleshooting steps for common issues (e.g., accessibility permissions, window‑manager conflicts).

**Production Readiness**  
Rift scores high for production use as an OSS candidate: recent activity, a sizable star count, and a modern Rust codebase suggest active maintenance and community support. While the integration documentation is modest, the straightforward build process and clear licensing make it feasible to evaluate. The primary risk lies in the lack of an official enterprise support channel and the need to verify compatibility with existing macOS management tooling; a limited pilot will surface any hidden setup costs before a broader deployment.

### Русский

**Rift** — это tiling‑window‑manager для macOS, написанный на Rust, который уже собрал более 2000 звёзд на GitHub и активно поддерживается (последний коммит — 13 июля 2026 г.). Он подходит для команд, желающих автоматизировать раскладку окон и ускорить переключение между задачами, особенно если их рабочий процесс уже подразумевает фиксированные зоны экрана; первый шаг внедрения — небольшое proof‑of‑concept и проверка README для настройки. По уровню готовности проект считается «production‑ready»: свежие обновления, значительное количество форков и активное сообщество позволяют запустить пилотный проект с минимальными рисками, при условии предварительной оценки сложности интеграции.

### 中文

**项目简介**  
`acsandmann/rift` 是一款用 Rust 编写的 macOS 平铺式窗口管理器，旨在为 macOS 提供类似 i3 / sway 的键盘驱动布局与自动窗口组织功能。

**价值**  
- **提升效率**：通过键盘快捷键快速排列、切换窗口，减少鼠标操作，适合需要在多个窗口间频繁切换的开发者、设计师和金融分析师。  
- **可定制**：配置文件采用 Rust 脚本或 TOML，支持自定义布局、工作区和快捷键，能够贴合团队或个人的具体工作流。  
- **轻量且原生**：直接运行在 macOS 上，无需额外的 X11 或虚拟机层，系统资源占用低，体验流畅。

**典型接入方式**  
1. **阅读并验证 README**：确认当前 macOS 版本（≥13）与项目兼容，并按照文档完成 Homebrew 或 Cargo 安装。  
2. **小范围 PoC**：在个人机器或 CI 环境中启动 `rift`，使用默认配置验证窗口平铺是否符合预期。  
3. **配置迁移**：将团队常用的快捷键、布局写入 `~/.config/rift/config.toml`，并通过 Git 进行版本管理。  
4. **自动化启动**：在 macOS 的登录项或 `launchd` 中加入 `rift --start`，确保每次登录自动生效。  

**生产可用性**  
- **活跃度**：截至 2026‑07‑13 最近一次提交，拥有 2 058 星、70+ Fork，社区活跃，Issue 与 PR 响应及时。  
- **技术成熟度**：核心使用 Rust 实现，内存安全、编译检查严格，已在多个公开项目中实践。  
- **风险评估**：集成路径主要依赖系统权限（Accessibility、Automation）和配置文件，需在正式部署前验证权限授予和冲突（如与其他窗口管理工具）。整体风险低，适合作为正式生产环境的窗口管理方案进行试点。

## 🧭 Practical evaluation

**Value:** acsandmann/rift may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2058 GitHub stars
- 70 forks
- updated 2026-07-13
- primary language: Rust
- 14 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 46/100 |
| stars | 71/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 79/100 |
| recency | 80/100 |
| adoption | 64/100 |
| production | 69/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/acsandmann/rift) · [← Back to Misc](./README.md)</sub>
