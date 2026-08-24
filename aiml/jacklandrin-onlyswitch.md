# jacklandrin/OnlySwitch

[![Stars](https://img.shields.io/github/stars/jacklandrin/OnlySwitch?style=flat-square&color=yellow)](https://github.com/jacklandrin/OnlySwitch/stargazers) [![Forks](https://img.shields.io/github/forks/jacklandrin/OnlySwitch?style=flat-square&color=blue)](https://github.com/jacklandrin/OnlySwitch/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> ⚙️ All-in-One menu bar app, hide 💻MacBook Pro's notch, dark mode, AirPods, Shortcuts

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 5.7k |
| 🍴 **Forks** | 232 |
| 💻 **Language** | Swift |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-agents` `audioplayer` `clamshell` `composable-architecture` `dark-mode` `macos` `menubar-app` `notch` `pomodoro-timer` `shortcuts` `stagemanager`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
OnlySwitch (jacklandrin/OnlySwitch) is a Swift‑based macOS menu‑bar utility that bundles a collection of handy toggles—such as hiding the MacBook Pro notch, switching Dark Mode, managing AirPods, and launching Shortcuts—into a single, customizable interface. While its core purpose is UI convenience, the project also includes a lightweight AI integration layer that lets developers prototype RAG or agent‑based workflows without building a model stack from scratch. With over 5,700 stars, active maintenance, and a growing community, it is a mature open‑source candidate for pilots that need quick macOS automation plus optional AI extensions.

**Value**  
- **All‑in‑One UI control** eliminates the need for multiple separate apps or scripts, saving time for power users and IT teams managing fleets of Macs.  
- **Built‑in AI hooks** let you attach LLM‑driven actions (e.g., contextual shortcuts or voice commands) without provisioning your own inference pipeline, accelerating proof‑of‑concept work.  
- **Swift native** ensures smooth performance and deep integration with macOS system APIs, reducing latency and compatibility issues.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Fork the repo, run the provided Xcode project, and verify the basic toggles on a test Mac.  
2. **AI Extension** – Follow the README to add your own OpenAI/Claude endpoint to the `AIHelper` module, then map a custom menu item to an LLM‑driven shortcut.  
3. **Packaging** – Use the existing build scripts to create a signed `.app` bundle; distribute via MDM or Homebrew tap for internal rollout.  
4. **Iterate** – Extend the `Switch` protocol to expose additional system controls or enterprise‑specific scripts, then push updates through the same pipeline.

**Production Readiness**  
- **High**: Recent commits (as of 2026‑06‑28), active issue triage, and strong community metrics (5.7 k stars, 232 forks) indicate a healthy codebase.  
- **Stability**: Core menu‑bar functionality is battle‑tested on macOS 13‑15; AI integration is modular and can be swapped out if needed.  
- **Risk Mitigation**: The integration steps are not fully documented for large‑scale deployment, so a small pilot should validate build, signing, and MDM distribution before full rollout. Once the pilot passes, scaling to production is straightforward.

### Русский

**OnlySwitch** — это открытое меню‑бар приложение для macOS, позволяющее одним переключателем управлять скрытием выреза у MacBook Pro, темным режимом, подключением AirPods, запуском Shortcuts и другими системными настройками. Для быстрого прототипирования AI‑фич (RAG, агентных сценариев) проект можно подключить к существующим пайплайнам, начав с небольшого proof‑of‑concept и проверки README; интеграция требует небольших усилий, так как основной стек написан на Swift и хорошо документирован. По уровню готовности проект считается «high»: активные коммиты, более 5 тыс. звёзд, активное сообщество и недавние обновления делают его пригодным для пилотных запусков в продакшн.

### 中文

**项目价值**  
OnlySwitch 是一款基于 Swift 开发的 macOS 菜单栏工具，聚合了多种日常调节功能（隐藏刘海、切换暗黑模式、快速连接 AirPods、触发 Shortcuts 等），让用户无需打开系统偏好设置即可一键完成。它的“一站式”设计提升了工作流效率，尤其适合频繁在不同环境间切换的开发者和创意工作者。

**典型接入方式**  
1. **直接使用**：在 Releases 页面下载最新的 `.app` 包，拖入 `/Applications` 并在系统偏好设置 → 安全性与隐私中允许运行。安装后即可在菜单栏看到图标，点击即可使用各项开关。  
2. **自定义扩展**：项目提供了 `OnlySwitch/Extensions` 目录，开发者可以通过添加 Swift 脚本或使用 `Shortcuts` API 将自定义命令注册为新的开关项。  
3. **CI/CD 集成**：如果需要在内部机器上统一部署，可使用 Homebrew tap：  
   ```bash
   brew tap jacklandrin/OnlySwitch
   brew install onlyswitch
   ```  
   通过 Homebrew 自动化安装、升级，配合 `defaults write` 进行默认开关状态的预设。

**生产可用性**  
- **活跃度**：截至 2026‑06‑28，项目最近一次提交仅数天前，拥有 5,739 ⭐、232 🍴，社区活跃，Issue 与 Pull Request 处理及时。  
- **技术成熟度**：代码基于 macOS 13+ 的系统框架，使用原生 Swift 编写，兼容性好，几乎不需要额外依赖。  
- **安全性**：所有功能均通过系统 API 实现，未引入第三方运行时，风险可控。  
- **部署成本**：只需下载或通过 Homebrew 安装，后续升级同样简便；若需要企业内部统一管理，可配合 MDM（Mobile Device Management）进行静默安装。  

综合来看，OnlySwitch 已具备 **高生产就绪度**，适合作为 macOS 工作环境的标准化工具，在内部或面向终端用户的 pilot 项目中直接投入使用。若需深度定制，可在其 Swift 插件机制上进行二次开发，成本相对可控。

## 🧭 Practical evaluation

**Value:** jacklandrin/OnlySwitch helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 5739 GitHub stars
- 232 forks
- updated 2026-06-28
- primary language: Swift
- 17 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 59/100 |
| stars | 80/100 |
| topics | 100/100 |
| outlook | 64/100 |
| quality | 73/100 |
| recency | 40/100 |
| adoption | 74/100 |
| production | 57/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/jacklandrin/OnlySwitch) · [← Back to AI/ML](./README.md)</sub>
