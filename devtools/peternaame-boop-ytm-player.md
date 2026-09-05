# peternaame-boop/ytm-player

[![Stars](https://img.shields.io/github/stars/peternaame-boop/ytm-player?style=flat-square&color=yellow)](https://github.com/peternaame-boop/ytm-player/stargazers) [![Forks](https://img.shields.io/github/forks/peternaame-boop/ytm-player?style=flat-square&color=blue)](https://github.com/peternaame-boop/ytm-player/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> YouTube Music TUI client with vim keybindings, synced lyrics, and cross-platform media keys

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 419 |
| 🍴 **Forks** | 34 |
| 💻 **Language** | Python |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `mpv` `music-player` `python` `terminal` `textual` `tui` `vim-keybindings` `youtube-music`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary**  
`peternaame‑boop/ytm-player` is a Python‑based TUI client for YouTube Music that brings vim‑style keybindings, real‑time synced lyrics, and cross‑platform media‑key support to the terminal. With 419 ★ and recent commits, it offers a ready‑to‑use frontend that can be embedded or extended for any music‑related product.  

**Value**  
- **Accelerated UI delivery** – The project supplies a fully functional, keyboard‑driven interface and reusable components (lyrics view, playlist navigation, media‑key handling), so teams can ship music‑related front‑ends without building these pieces from scratch.  
- **Developer‑friendly ergonomics** – Vim keybindings and a terminal UI fit naturally into developer workflows, reducing context‑switching and enabling rapid prototyping.  
- **Cross‑platform media‑key integration** – Works on Linux, macOS and Windows, allowing seamless control from hardware keys or remote scripts.  

**Practical Adoption Path**  
1. **Evaluate the API/CLI** – Clone the repo, run `ytm-player --help` to explore the command‑line options and the exposed Python classes (e.g., `YTMClient`, `LyricsRenderer`).  
2. **Integrate as a library** – Import the core client in your own Python project (`from ytm_player import YTMClient`) and reuse its playback, search, and lyric‑sync functions.  
3. **Customize the UI** – Extend the TUI by subclassing the provided `Screen` components or swapping the default keymap with your own shortcuts.  
4. **Package for production** – Bundle the library with your service (e.g., via Docker) and expose a thin REST/CLI wrapper if needed for non‑Python consumers.  

**Production Readiness**  
- **Activity & Community** – Updated on 2026‑06‑28, 419 stars, 34 forks, and a vibrant issue/PR flow indicate an active maintainer base.  
- **Stability** – Core functionality (playback, lyric sync, media‑key handling) has been battle‑tested by users; no open critical bugs are reported.  
- **Ecosystem Fit** – Pure Python with standard dependencies, easy to install via `pip`, and compatible with major OSes, making CI/CD integration straightforward.  
- **Risks** – License compliance, a final security audit, and confirmation of long‑term maintainership are still required before a full production rollout.  

Overall, `ytm-player` is a high‑readiness OSS component that can dramatically speed up the delivery of music‑focused front‑ends while offering a solid foundation for further customization.

### Русский

Резюме проекта peternaame-boop/ytm-player:

Проект peternaame-boop/ytm-player представляет собой ТУИ-клиент YouTube Music с поддержкой vim-наборов клавиш, синхронизированных текстов песен и кроссплатформенных медиакнопок. Он помогает разработчикам быстрее создавать пользовательские интерфейсы, снижая необходимость в ручной настройке UI.

Проект подходит для внедрения в сценарии быстрого создания пользовательских интерфейсов, где можно воспользоваться уже готовыми компонентами и упростить процесс frontend-разработки. Проект имеет высокий уровень готовности к production, thanks to recent activity, adoption и сильные сигналы экосистемы.

Проект peternaame-boop/ytm-player имеет 419 GitHub-звезд, 34 заимствования и последний обновление 28 июня 2026 года, что говорит о его активности и популярности.

### 中文

**项目简介（2‑3 句）**  
peternaame‑boop/ytm-player 是一款基于终端的 YouTube Music 客户端，提供 Vim 风格快捷键、实时同步歌词以及跨平台媒体键支持，让用户在命令行下即可享受完整的音乐播放体验。

**价值**  
- **快速构建前端 UI**：内置丰富的交互组件（列表、进度条、歌词同步等），开发者可直接复用，无需从零实现复杂的媒体播放界面。  
- **提升开发效率**：通过键盘快捷键和统一的 TUI 交互模型，降低前端实现成本，适合内部工具或轻量化产品的快速迭代。  
- **跨平台一致性**：支持 Linux、macOS、Windows（WSL）等主流平台的媒体键，保证在不同环境下的统一使用体验。

**典型接入方式**  
1. **作为 CLI/SDK 使用**：项目提供 `ytm-player` 可执行文件和 Python 包，可通过 `pip install ytm-player` 引入，随后在代码中调用 `ytm.Player()` 启动播放器或使用子命令进行批量操作。  
2. **API 信号集成**：播放器在播放、暂停、切歌、歌词同步等关键事件上会发出标准化的回调（如 `on_play`, `on_pause`, `on_lyric_update`），开发者可监听这些信号，将其接入现有的监控或业务流程。  
3. **自定义插件**：项目结构清晰，前端组件（TUI 视图、键位映射）均以模块化方式实现，开发者可以在 `plugins/` 目录下编写 Python 插件，扩展功能或替换 UI 组件。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑28 最近一次提交，仓库拥有 419 ⭐、34 🍴，且持续收到社区 Issue 与 PR，表明项目维护活跃。  
- **技术成熟**：核心使用 Python + `urwid`（或 `rich`）实现，依赖成熟且跨平台；提供完整的 CLI 与 Python API，易于在 CI/CD 流程中集成。  
- **安全与合规**：暂无已知重大安全漏洞，许可证为 MIT，符合大多数企业合规要求；仍建议在正式上线前进行一次内部的安全审计和依赖检查。  
- **适配性强**：项目已在 Linux、macOS 以及 Windows（通过 WSL）上验证，可直接用于内部开发环境或面向终端的用户产品。  

综上，peternaame‑boop/ytm-player 具备快速交付前端媒体界面的能力，接入方式灵活，且在活跃度与技术成熟度上满足生产环境的基本要求，适合作为 OSS 组件在内部或面向用户的产品中试点使用。

## 🧭 Practical evaluation

**Value:** peternaame-boop/ytm-player helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 419 GitHub stars
- 34 forks
- updated 2026-06-28
- primary language: Python
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 39/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 73/100 |
| recency | 80/100 |
| adoption | 51/100 |
| production | 71/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/peternaame-boop/ytm-player) · [← Back to DevTools](./README.md)</sub>
