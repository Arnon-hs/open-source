# djmunro/hush

[![Stars](https://img.shields.io/github/stars/djmunro/hush?style=flat-square&color=yellow)](https://github.com/djmunro/hush/stargazers) [![Forks](https://img.shields.io/github/forks/djmunro/hush?style=flat-square&color=blue)](https://github.com/djmunro/hush/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-41%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 41/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Hush is a macOS‑only, push‑to‑talk dictation tool that runs entirely locally—no audio is sent to the cloud—and inserts the transcribed text directly at the current cursor position. It targets users who need quick, on‑the‑fly speech‑to‑text without the privacy concerns of online services, making it handy for writers, developers, or anyone who prefers a seamless, offline workflow.

**Value**  
- **Privacy‑first**: All speech processing stays on the user’s machine, eliminating the risk of data leakage to external servers.  
- **Instant insertion**: The transcription is pasted exactly where the cursor is, removing the need to copy‑paste from a separate window.  
- **Low friction**: A single hotkey activates dictation, giving a “push‑to‑talk” experience that feels native to macOS.

**Practical Adoption Path**  
1. **Clone & build** – Pull the repository, follow the README to install any required dependencies (e.g., a local speech‑recognition engine).  
2. **Configure hotkey** – Set up the preferred keyboard shortcut in the app’s preferences or via macOS’s Keyboard Shortcuts pane.  
3. **Trial run** – Test in a sandbox document (e.g., TextEdit) to verify that transcription accuracy and cursor insertion meet your expectations.  
4. **Integrate** – If the tool works, create a small internal guide (hotkey, supported languages, known limitations) for the team.  
5. **Monitor** – Keep an eye on the repo for updates, and log any bugs or feature requests in your own issue tracker.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last update 2026‑05‑14) but has limited documentation, few usage examples, and sparse community signals.  
- **Risks**: Potential licensing ambiguities, unknown long‑term maintenance, and limited support for edge‑case languages or macOS versions.  
- **Recommendation**: Suitable for prototypes, internal tools, or personal workflows after a short validation period. For mission‑critical production use, conduct a deeper audit of the license, test across all target macOS versions, and consider a fallback dictation solution in case the project becomes unmaintained.

### Русский

**Hush** — это локальное приложение push‑to‑talk для диктовки на macOS, которое полностью работает без облака и вставляет распознанный текст прямо в позицию курсора. Оно удобно в сценариях, где нужен быстрый ввод речи в любые программы (например, написание кода, ответы в чатах или заполнение форм), без риска утечки данных и без необходимости настраивать внешние сервисы. Готовность к production — средняя: проект активен (обновление 14 мая 2026), но перед внедрением следует проверить лицензию, частоту релизов, наличие документации и открытых проблем.

### 中文

**项目简介（2‑3 句）**  
Hush 是一款面向 macOS 的本地“按键说话”语音输入工具，所有识别在本机完成，不会上传云端，识别结果直接粘贴到光标所在位置，适合对隐私和即时性有要求的用户。

**价值**  
- **本地离线**：语音识别在本机运行，数据不离开设备，满足企业或个人的隐私合规需求。  
- **即点即写**：识别完毕后自动粘贴到当前光标位置，无需额外的复制粘贴步骤，提高文本录入效率。  
- **轻量快捷**：只需按住快捷键即可开始/结束录音，适合作为日常笔记、代码注释或快速回复的辅助工具。

**典型接入方式**  
1. **下载安装**：从 GitHub Release 页面下载对应 macOS 版本的二进制或通过 Homebrew（`brew install hush`）安装。  
2. **配置快捷键**：在系统偏好设置 → 键盘 → 快捷键中为 Hush 指定“按键说话”触发键（默认可为 `⌥+空格`），或在 Hush 的偏好面板中自定义。  
3. **调用方式**：在任何可编辑文本框中将光标定位后，按下快捷键开始说话，松开后识别结果会自动粘贴。  
4. **可选集成**：通过 AppleScript 或 Automator 调用 `hush --paste` 命令，实现与自定义工作流（如 Xcode、Notes、Slack）深度集成。

**生产可用性**  
- **成熟度**：项目最近一次更新于 2026‑05‑14，活跃度一般（仅 2 个话题），代码库规模小，适合作为原型或内部工具使用。  
- **依赖与维护**：依赖 macOS 原生语音框架，外部依赖少；但需自行检查许可证（MIT / Apache 等）以及后续 macOS 系统升级的兼容性。  
- **风险与建议**：由于社区反馈和 issue 记录有限，建议在正式部署前进行以下检查：  
  - 许可证是否符合贵公司合规要求；  
  - 最近的 issue 与 PR 是否活跃，是否有未解决的关键 bug；  
  - 是否提供足够的文档或示例脚本，便于内部维护。  

综上，Hush 在对隐私有严格要求且需要快速文本输入的 macOS 环境中具有明显价值，适合作为内部原型或低风险业务流程的语音输入方案；在投入生产前建议完成一次完整的功能与兼容性评估。

## 🧭 Practical evaluation

**Value:** Hush – local push-to-talk dictation for macOS, no cloud, pastes at cursor may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-05-14
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 54/100 |
| quality | 41/100 |
| recency | 100/100 |
| adoption | 0/100 |
| production | 58/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/djmunro/hush) · [← Back to Misc](./README.md)</sub>
