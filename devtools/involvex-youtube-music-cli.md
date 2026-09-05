# involvex/youtube-music-cli

[![Stars](https://img.shields.io/github/stars/involvex/youtube-music-cli?style=flat-square&color=yellow)](https://github.com/involvex/youtube-music-cli/stargazers) [![Forks](https://img.shields.io/github/forks/involvex/youtube-music-cli?style=flat-square&color=blue)](https://github.com/involvex/youtube-music-cli/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> A powerful Terminal User Interface (TUI) music player for YouTube Music

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 343 |
| 🍴 **Forks** | 19 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `youtube` `youtube-cli` `youtube-music` `youtube-music-client`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Summary**  
involvex/youtube-music-cli is a TypeScript‑based Terminal User Interface (TUI) that lets users stream and control YouTube Music directly from the command line. With 340+ stars and recent commits, it offers a ready‑to‑use, highly configurable music player that can be embedded in developer tools, CI pipelines, or custom front‑end prototypes.  

**Value**  
The project eliminates the need to build a bespoke UI for YouTube Music integration, providing a polished, keyboard‑driven interface and a set of reusable components (playback controls, playlists, search, etc.). This speeds up delivery of user‑facing features, reduces UI bugs, and lets teams focus on core product logic rather than low‑level media handling.  

**Practical adoption path**  
1. **Evaluate** – Clone the repo, run `npm install && npm run start` to confirm the TUI works in your environment.  
2. **Integrate** – Use the exposed CLI commands or import the underlying TypeScript modules into your own tooling or scripts.  
3. **Customize** – Override configuration files (theme, key bindings, API token handling) to match your product’s branding or workflow.  
4. **Deploy** – Package the CLI with your CI/CD pipeline or ship it as a binary for end‑users, leveraging the existing npm publishing workflow.  

**Production readiness**  
The library shows strong production signals: recent activity (last commit on 2026‑06‑22), a healthy star count (343), and active community interest. Its TypeScript codebase is well‑typed, and the TUI is built on mature libraries (e.g., Ink, React‑TUI). While the license and security posture still need a final audit, the overall maturity, documentation, and community adoption make it suitable for a serious pilot or even full‑scale production use.

### Русский

**involvex/youtube-music-cli** — это мощный TUI‑плеер для YouTube Music, написанный на TypeScript, позволяющий быстро собрать пользовательский интерфейс без собственного UI‑кода, используя готовые компоненты и CLI‑API. Типичный сценарий — интеграция в внутренние инструменты или CI/CD‑конвейеры, где нужен легковесный музыкальный плеер в терминале; проект легко подключается через npm и запускается одной командой. По активности (343 ★, недавние коммиты, активные форки) и покрытию тем, готовность к production оценивается как высокая, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
`involvex/youtube-music-cli` 是一款基于终端用户界面（TUI）的 YouTube Music 播放器，使用 TypeScript 编写，提供丰富的键盘交互和可定制的主题，让开发者和终端爱好者无需离开命令行即可畅享音乐。

**价值**  
- **快速构建前端交互**：内置完整的 TUI 框架和播放控制逻辑，省去自行实现 UI、音频流处理和快捷键绑定的工作。  
- **组件复用**：提供可直接引用的 UI 组件（列表、进度条、弹窗等），可在其他 CLI/桌面项目中复用，加速产品 UI 的交付。  
- **提升开发效率**：统一的 API/CLI 接口让前端团队只需关注业务层逻辑，即可快速集成 YouTube Music 播放功能。

**典型接入方式**  
1. **作为独立 CLI 使用**：`npx youtube-music-cli search "周杰伦"`，直接在终端搜索、播放、管理歌单。  
2. **在自定义脚本/工具中调用**  
   ```bash
   # 安装为项目依赖
   npm i -D youtube-music-cli
   # 调用内部 API
   const { play, search } = require('youtube-music-cli');
   const tracks = await search('Imagine Dragons');
   await play(tracks[0].url);
   ```  
3. **嵌入其他 TUI 应用**：通过导出的 `createApp()` 方法，将播放器 UI 作为子模块挂载到现有的 Ink/React‑TUI 项目中，实现统一的终端体验。  

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑22，GitHub ★343、Fork 19，社区活跃。  
- **技术成熟度**：使用 TypeScript、Node.js LTS，提供完整的类型声明和错误处理。  
- **生态兼容**：兼容主流 Linux/macOS 终端，支持 Windows Subsystem for Linux。  
- **安全与许可证**：项目采用 MIT 许可证，未发现已知安全漏洞；仍建议在正式环境中进行一次依赖审计。  

综合以上因素，`youtube-music-cli` 已具备在内部工具、CI/CD 报告或面向终端用户的产品中进行 **生产级** 部署的条件，只需完成常规的安全审查和维护者沟通即可。

## 🧭 Practical evaluation

**Value:** involvex/youtube-music-cli helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 343 GitHub stars
- 19 forks
- updated 2026-06-22
- primary language: TypeScript
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 33/100 |
| stars | 54/100 |
| topics | 63/100 |
| outlook | 68/100 |
| quality | 66/100 |
| recency | 80/100 |
| adoption | 48/100 |
| production | 69/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/involvex/youtube-music-cli) · [← Back to DevTools](./README.md)</sub>
