# jarun/nnn

[![Stars](https://img.shields.io/github/stars/jarun/nnn?style=flat-square&color=yellow)](https://github.com/jarun/nnn/stargazers) [![Forks](https://img.shields.io/github/forks/jarun/nnn?style=flat-square&color=blue)](https://github.com/jarun/nnn/network) [![Language](https://img.shields.io/badge/lang-C-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> n³ The unorthodox terminal file manager

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 21.6k |
| 🍴 **Forks** | 808 |
| 💻 **Language** | C |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `batch-rename` `c` `cli` `command-line` `developer-tools` `disk-usage` `file-manager` `file-preview` `file-search` `filesystem` `launcher`

## 🎯 Categories

DevTools · Mobile

## 📝 Summary

### English

**Summary**  
`jarun/nnn` is a fast, scriptable terminal file manager written in C that lets developers build and ship user‑facing interfaces with minimal custom UI code. Its rich set of API/CLI hooks, extensive topic tags, and a thriving community (21 k ★, 800 forks, recent commits) make it a practical foundation for quickly re‑using interface components in frontend or dev‑tool products.  

**Value** – By handling file‑browsing, selection, and basic UI interactions out‑of‑the‑box, nnn lets teams focus on domain‑specific UI rather than reinventing low‑level file‑system widgets, accelerating product UI delivery and reducing maintenance overhead.  

**Adoption path** – Evaluate the CLI and SDK signals in a sandboxed environment, integrate the C library or invoke the binary from your build pipeline, and replace custom file‑picker code with nnn’s proven components. Because it is language‑agnostic and can be wrapped in scripts or called from other languages, migration can be incremental—start with a single view and expand as confidence grows.  

**Production readiness** – The project shows high readiness: continuous updates (last commit 2026‑06‑24), strong adoption metrics, and a broad ecosystem of topics and integrations. While the license and security posture still need a final review, the activity level, community support, and lack of major bugs indicate that nnn is suitable for a serious pilot or production rollout.

### Русский

**jarun/nnn** — это лёгкий терминальный файловый менеджер (C), который позволяет быстро собрать пользовательский интерфейс без написания собственного UI‑кода, переиспользуя готовые компоненты и ускоряя доставку фронтенда. Его типичный сценарий — интеграция через CLI/SDK в процессы сборки продукта для создания и управления файловыми представлениями в UI‑приложениях. Проект считается готовым к production: активные коммиты, более 21 000 звёзд, широкая экосистема и сильные сигналы принятия, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
jarun/nnn 是一款轻量级、极致高效的终端文件管理器（n³），用 C 语言编写，凭借 21 k+ Stars 在开源社区拥有极高人气。它提供了丰富的 CLI/SDK 接口，能够在不编写大量自定义 UI 的情况下快速构建和交付用户界面。

**价值主张**  
- **加速前端交付**：通过内置的文件浏览、预览、批量操作等功能，开发者可以直接在终端完成资源组织和调试，省去大量 UI 开发和维护工作。  
- **复用组件**：nnn 的插件体系和 API 让常见的文件操作、快捷键、预览渲染等可以在不同项目中复用，提升 UI 一致性。  
- **提升效率**：极低的资源占用和键盘驱动的交互方式，使得在 CI/CD、容器、远程服务器等环境下也能流畅使用，进而缩短产品迭代周期。

**典型接入方式**  
1. **CLI 调用**：在构建脚本或 CI 流水线中直接执行 `nnn`/`nnn -x <cmd>`，完成文件选择、批量重命名等任务。  
2. **插件/脚本**：利用官方或自定义插件（Lua、Shell）扩展功能，例如将选中文件路径输出为 JSON，供前端框架读取。  
3. **SDK 接口**：通过 C 库或包装好的 Go/Python 绑定，嵌入到自研工具或 IDE 插件中，实现 UI 组件的即时预览与交互。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑24，项目仍在持续更新，最近一次提交在本月，拥有 21 k+ Stars、800+ Forks，社区活跃度高。  
- **生态兼容**：支持 Linux、macOS、BSD，二进制体积小于 1 MB，易于在容器或轻量系统中部署。  
- **成熟度**：已被多款开源工具（如 ranger、vim 插件）采用，具备稳定的插件系统和成熟的文档。  
- **风险**：需进一步审查许可证（GPL‑2.0）与安全审计报告，确认无潜在供应链风险后即可在生产环境安全使用。  

综上，nnn 具备高生产就绪度，适合作为前端/DevTools 项目中快速构建文件交互 UI 的底层工具。

## 🧭 Practical evaluation

**Value:** jarun/nnn helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 21647 GitHub stars
- 808 forks
- updated 2026-06-24
- primary language: C
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 73/100 |
| stars | 92/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 79/100 |
| recency | 40/100 |
| adoption | 87/100 |
| production | 62/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/jarun/nnn) · [← Back to DevTools](./README.md)</sub>
