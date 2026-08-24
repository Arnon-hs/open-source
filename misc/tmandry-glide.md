# tmandry/glide

[![Stars](https://img.shields.io/github/stars/tmandry/glide?style=flat-square&color=yellow)](https://github.com/tmandry/glide/stargazers) [![Forks](https://img.shields.io/github/forks/tmandry/glide?style=flat-square&color=blue)](https://github.com/tmandry/glide/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-43%2F100-brightgreen?style=flat-square)](#)

> A tiling window manager for macOS

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 620 |
| 🍴 **Forks** | 18 |
| 💻 **Language** | Rust |
| 📈 **Score** | 43/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
Glide is a tiling window manager written in Rust for macOS, offering a lightweight way to automatically arrange application windows in a grid‑like layout. With over 600 stars on GitHub and recent activity (last commit 2026‑06‑25), it shows modest community interest but limited documentation on integration.

**Value**  
For teams that spend a lot of time juggling multiple macOS windows—e.g., developers, designers, or data analysts—Glide can streamline the workspace by enforcing a predictable, keyboard‑driven layout, reducing mouse‑click overhead and visual clutter. Its Rust implementation promises good performance and a small binary footprint.

**Practical adoption path**  

1. **Initial vetting** – Clone the repo, build the binary (`cargo build --release`), and run the demo configuration on a test Mac to confirm that the tiling behavior matches your workflow.  
2. **Configuration** – Edit the provided TOML/YAML config (or create one) to map keybindings, define screen zones, and whitelist/blacklist applications.  
3. **Integration** – Add the binary to your login items or launch it via a launch agent so it starts automatically.  
4. **Testing** – Verify interaction with existing tools (e.g., Spotlight, window‑snapping utilities) and ensure no conflicts with macOS security/privacy prompts.  

**Production readiness**  
Glide sits at a *medium* readiness level: it is functional enough for prototypes or internal tooling, but the integration surface is thin—there is no package manager distribution, no extensive docs, and no official support channel. Before deploying to production, teams should:

* Conduct a dependency audit (Rust toolchain, required macOS version).  
* Set up a sandboxed pilot to measure stability and any performance impact.  
* Establish a maintenance plan for updates, as community activity is modest and bug‑fix turnaround may be slow.  

If those checks pass, Glide can be a viable, low‑overhead addition to a macOS‑centric workflow; otherwise, consider more mature tiling managers (e.g., yabai) for mission‑critical environments.

### Русский

tmandry/glide — это tiling‑window‑менеджер для macOS, написанный на Rust, который позволяет организовать окна в сетку и ускорить переключение между задачами. Подойдёт для прототипов или внутренних рабочих процессов, где требуется гибкая раскладка экранов, однако перед внедрением следует вручную проверить совместимость и оценить затраты на настройку, так как интеграционные детали в репозитории скудны. Готовность к production — средняя: проект имеет 620 звёзд, активные обновления и небольшое количество форков, но требует дополнительного аудита зависимостей и поддержки.

### 中文

**项目简介**  
`tmandry/glide` 是一款基于 Rust 实现的 macOS 平铺式窗口管理器，旨在为 macOS 提供类似 i3、bspwm 等 Linux 下的窗口平铺体验。

**价值**  
- **提升工作效率**：通过键盘驱动的平铺布局，快速在多个窗口间切换，适合需要频繁查看和对比多窗口内容的开发、设计或运维场景。  
- **轻量且可定制**：核心使用 Rust 编写，二进制体积小，配置文件采用简洁的 TOML/JSON 语法，便于根据个人工作流进行深度定制。  
- **开源社区支持**：已有 620+ Stars、18+ Forks，活跃度较高，能够快速获取社区的 bug 修复和功能补丁。

**典型接入方式**  
1. **依赖准备**：在 macOS 上安装 Rust（`rustup`）或直接下载项目发布的预编译二进制。  
2. **源码编译**（可选）：`git clone https://github.com/tmandry/glide && cd glide && cargo build --release`，生成的可执行文件位于 `target/release/glide`。  
3. **配置**：在 `$HOME/.config/glide/config.toml`（或项目 README 中指定的路径）编写布局、快捷键、启动程序等规则。  
4. **启动**：将 `glide` 加入登录项或使用 `launchctl` 创建守护进程，使其在用户登录时自动运行。  
5. **集成测试**：在测试机器或容器（如 macOS 虚拟机）中验证快捷键、窗口行为是否符合既有工作流，再决定是否在正式工作站上推广。

**生产可用性**  
- **成熟度**：项目近期（2026‑06‑25）仍在活跃维护，代码基于 Rust，具备较好的安全性和性能。  
- **适用场景**：适合内部原型、研发工作站或对窗口管理有特殊需求的团队；不建议直接在对可靠性要求极高的生产环境（如金融交易终端）中使用，除非完成充分的内部测试。  
- **风险与注意事项**：  
  - **集成路径不明确**：官方文档和示例相对简略，需自行梳理启动方式、权限（Accessibility）授权等细节。  
  - **依赖维护**：需关注 Rust 生态的更新以及 macOS 系统升级对键盘事件拦截的兼容性。  
  - **运维成本**：建议在正式部署前编写自动化的健康检查脚本，监控进程是否异常退出并自动重启。  

综上，`tmandry/glide` 在提升 macOS 工作站窗口管理效率方面具有明显价值，接入成本主要集中在环境准备和配置调优。经过内部验证后，可在研发或内部工具环境中安全使用；若需在更高可靠性要求的生产环境使用，则需额外进行稳定性验证和运维保障。

## 🧭 Practical evaluation

**Value:** tmandry/glide may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 620 GitHub stars
- 18 forks
- updated 2026-06-25
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 32/100 |
| stars | 59/100 |
| topics | 0/100 |
| outlook | 45/100 |
| quality | 48/100 |
| recency | 40/100 |
| adoption | 52/100 |
| production | 48/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/tmandry/glide) · [← Back to Misc](./README.md)</sub>
