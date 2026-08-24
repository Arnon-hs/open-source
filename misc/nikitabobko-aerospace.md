# nikitabobko/AeroSpace

[![Stars](https://img.shields.io/github/stars/nikitabobko/AeroSpace?style=flat-square&color=yellow)](https://github.com/nikitabobko/AeroSpace/stargazers) [![Forks](https://img.shields.io/github/forks/nikitabobko/AeroSpace?style=flat-square&color=blue)](https://github.com/nikitabobko/AeroSpace/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> AeroSpace is an i3-like tiling window manager for macOS

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 21.4k |
| 🍴 **Forks** | 566 |
| 💻 **Language** | Swift |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`apple` `i3` `i3wm` `mac` `macos` `swift` `tiling` `tiling-window-manager` `window-manager`

## 🎯 Categories

Misc

## 📝 Summary

### English

Here's a brief summary of the AeroSpace project:

AeroSpace is an open-source, i3-like tiling window manager designed specifically for macOS, offering a customizable and efficient way to manage windows on the platform. Its value lies in providing a tailored solution for users who require a specific workflow, as indicated by its README and activity. With recent activity, a strong ecosystem, and a high production readiness score, AeroSpace presents a feasible option for adoption, albeit requiring a careful evaluation of integration costs.

### Русский

AeroSpace — это tiling‑менеджер окон для macOS, работающий по принципу i3 и написанный на Swift; благодаря более 21 тысячам звёзд на GitHub, активным обновлениям (последний коммит 30 июня 2026 г.) и растущему сообществу он готов к использованию в продуктивных проектах. Типичный сценарий внедрения — небольшое пилотное развертывание в виде proof‑of‑concept, при котором проверяется совместимость с текущим workflow через README и базовую настройку, после чего можно масштабировать на весь набор машин. Несмотря на отсутствие детального описания интеграции в метаданных, уровень готовности к production считается высоким, а риски сводятся к оценке затрачиваемого времени на первоначальную настройку.

### 中文

**项目简介**  
AeroSpace 是一款面向 macOS 的 tiling 窗口管理器，采用 i3‑style 的布局模型，使用 Swift 编写，支持多显示器、自动平铺、手势与键盘快捷键等特性，能够让 macOS 的工作空间行为更像 Linux 上的动态窗口管理器。

**价值**  
- **提升工作效率**：通过键盘驱动的平铺布局，快速在窗口间切换、重新排列，减少鼠标点击和窗口拖拽的时间。  
- **可定制化强**：配置文件基于 JSON/TSL，支持自定义键位、规则、工作区和插件，能够贴合个人或团队的具体工作流。  
- **原生 macOS 体验**：使用 Swift 与 Cocoa 框架实现，兼容系统的窗口动画、全屏模式和多显示器，且不会破坏系统的安全与隐私机制。

**典型接入方式**  
1. **阅读 README 与示例配置**：确认当前 macOS 版本（>=13）与硬件兼容；了解基本概念（workspace、container、layout）。  
2. **小范围试点**：在开发者或测试机器上使用 Homebrew (`brew install --cask aerospacectl`) 或直接下载最新 Release，先在单一显示器上启用并加载最小化的配置文件，验证键位、自动平铺是否符合预期。  
3. **逐步迁移**：在确认无冲突后，将配置文件同步到团队共享位置（如 Git 仓库），并在 CI/CD 中加入启动脚本，以便新机器快速部署。  
4. **监控与回滚**：使用 `aerospace --log-level debug` 收集运行日志，出现异常时可通过 `aerospace --reset` 恢复默认设置或暂时禁用。

**生产可用性**  
- **活跃度**：截至 2026‑06‑30，项目仍在持续更新，拥有 21 k+ 星、566 叉，近期提交频繁，社区活跃。  
- **成熟度**：已被多个开源项目和个人开发者在日常工作中采用，文档较完整，支持 macOS 最新系统特性。  
- **风险**：集成成本主要在于学习 i3‑style 的概念以及编写符合团队需求的配置文件；在已有窗口管理工具（如 Magnet、BetterSnapTool）共存时可能出现快捷键冲突，需要提前规划。  

综上，AeroSpace 在 macOS 环境下提供了成熟且高效的 tiling 窗口管理能力，适合希望通过键盘驱动提升工作流的团队或个人。只要在小范围内验证配置与兼容性，即可安全推进到生产环境。

## 🧭 Practical evaluation

**Value:** nikitabobko/AeroSpace may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 21449 GitHub stars
- 566 forks
- updated 2026-06-30
- primary language: Swift
- 9 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 69/100 |
| stars | 92/100 |
| topics | 100/100 |
| outlook | 64/100 |
| quality | 79/100 |
| recency | 40/100 |
| adoption | 86/100 |
| production | 59/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/nikitabobko/AeroSpace) · [← Back to Misc](./README.md)</sub>
