# nanvon/cc-bar

[![Stars](https://img.shields.io/github/stars/nanvon/cc-bar?style=flat-square&color=yellow)](https://github.com/nanvon/cc-bar/stargazers) [![Forks](https://img.shields.io/github/forks/nanvon/cc-bar?style=flat-square&color=blue)](https://github.com/nanvon/cc-bar/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-44%2F100-brightgreen?style=flat-square)](#)

> Native macOS menu bar app: track quota, usage and cost for Codex (multi-account) and Claude Code, from your menu bar or a desktop floating HUD.  原生 macOS 菜单栏 App：支持 Codex 多账号与 Claude Code，在菜单栏或桌面悬浮窗实时查看额度、本地用量与消费。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 85 |
| 🍴 **Forks** | 3 |
| 💻 **Language** | Swift |
| 📈 **Score** | 44/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anthropic` `claude` `claude-code` `codex` `macos` `menu-bar` `multi-account` `openai` `quota` `usage-tracking`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
nanvon/cc‑bar is a native macOS menu‑bar (and floating‑HUD) utility written in Swift that lets you monitor quota, usage and spending for OpenAI Codex (multi‑account) and Anthropic Claude Code in real time. It provides a quick, always‑on‑screen view of AI credit balances, local consumption and cost, helping developers keep AI expenses under control.

**Value**  
- **Visibility & Cost Control** – By surfacing quota and cost data in the menu bar, teams can instantly see when they are approaching limits, preventing surprise bills.  
- **Multi‑account support** – Handles several Codex accounts simultaneously, a common need for agencies or developers testing different keys.  
- **Zero‑code integration** – No SDK or model‑hosting required; the app simply reads the relevant API‑key usage endpoints, so you get AI‑budget awareness without altering existing codebases.  

**Practical Adoption Path**  
1. **Quick Proof‑of‑Concept** – Clone the repo, run the Swift project, and add your OpenAI/Anthropic API keys in the UI. Verify that the menu‑bar shows correct quota data for one account.  
2. **Scale to Multiple Accounts** – Add additional keys via the app’s settings and confirm that each account’s usage is displayed correctly.  
3. **Integrate into Workflow** – Deploy the compiled app on developers’ Macs or on a shared workstation. Optionally, script the app’s launch at login for continuous monitoring.  
4. **Automate Alerts (optional)** – Pair the app with macOS notifications or a simple shell script that reads the same endpoints to trigger email/SMS alerts when thresholds are crossed.  

**Production Readiness**  
- **Maturity** – Medium. The project is actively maintained (last update 2026‑06‑25), has 85 ★ and a modest number of forks, indicating community interest but limited real‑world testing.  
- **Stability** – Core functionality (API calls, UI rendering) is straightforward and written in Swift, a first‑class language for macOS, so the binary is likely stable on recent macOS releases.  
- **Risks** –  
  * Integration steps are not fully documented; you’ll need to explore the README and possibly the source to understand how API keys are stored and refreshed.  
  * Dependency on external quota APIs means any changes in OpenAI/Anthropic endpoints could break the app; a small monitoring effort is required.  
  * No built‑in alerting or enterprise‑grade logging, so additional tooling is needed for production monitoring.  

**Bottom Line**  
nanvon/cc‑bar is a handy, low‑effort tool for teams that want immediate visibility into AI credit consumption on macOS. It is suitable for prototypes, internal dashboards, or as a cost‑awareness add‑on, provided you perform a brief PoC, verify the multi‑account workflow, and add any missing alerting or logging before rolling it out to a broader production environment.

### Русский

**nanvon/cc-bar** — это нативное macOS‑приложение для меню‑бара (и плавающего HUD), которое в реальном времени отображает квоты, использованные ресурсы и расходы по нескольким аккаунтам Codex и Claude Code. Его обычно внедряют как лёгкий мониторинг AI‑расходов в прототипах, RAG‑ или агентных воркфлоу, начиная с небольшого proof‑of‑concept и проверки README; при этом проект уже имеет средний уровень готовности к production (Swift‑код, 85 звёзд, актуальное обновление), но требует проверки зависимостей и уточнения процесса интеграции.

### 中文

**项目简介（2‑3 句）**  
nanvon/cc-bar 是一款原生 macOS 菜单栏工具，能够实时在菜单栏或桌面悬浮窗中展示 Codex（支持多账号）和 Claude Code 的配额、使用量以及费用。它帮助开发者和产品团队在本地快速监控 AI 资源消耗，避免意外超额。

**价值**  
- **即时可视化**：无需打开控制台或登录平台，随时在菜单栏看到配额剩余和费用累计。  
- **多账号管理**：同一界面即可切换和对比多个 Codex 账户，适合团队或个人多项目使用。  
- **成本控制**：帮助研发团队在原型阶段就能把握模型调用成本，降低后期预算风险。  

**典型接入方式**  
1. **Clone & Build**：`git clone https://github.com/nanvon/cc-bar && cd cc-bar && xcodebuild -scheme cc-bar`，使用 Xcode 编译生成 `.app`。  
2. **配置 API Key**：在应用首选项或系统钥匙串中添加 Codex/Claude 的 API Key（支持多个键值对），可通过 UI 添加或编辑。  
3. **启动并验证**：运行 `.app`，在菜单栏出现图标后点击查看配额；若需要在桌面悬浮窗展示，可在偏好设置中启用 “HUD”。  
4. **CI/CD 集成（可选）**：将编译产物打包为 `.pkg`，通过企业 MDM 分发，确保所有开发者机器统一安装。  

**生产可用性**  
- **成熟度**：已有 85 ⭐、3 个 fork，最近一次提交为 2026‑06‑25，代码基于 Swift，符合 macOS 原生体验。  
- **适用场景**：适合内部原型、研发监控以及成本审计；在正式业务中使用前建议进行以下检查：  
  - **依赖审计**：确认第三方库（如 Alamofire、SwiftUI）符合公司安全合规要求。  
  - **错误容错**：为网络异常或 API 限流添加重试/降级逻辑，避免 UI 卡死。  
  - **配置管理**：使用企业钥匙串或安全存储统一管理 API Key，防止泄露。  
- **生产准备度**：**中等**。功能已可用，但仍需自行进行安全、可观测性和升级路径的评估后方可在生产环境大规模部署。  

> **总结**：cc-bar 为 macOS 开发者提供了“一键式” AI 配额监控，接入成本低，适合作为原型或内部工具使用；在正式生产环境部署前，请完成依赖审计、容错处理和安全配置，以提升可靠性。

## 🧭 Practical evaluation

**Value:** nanvon/cc-bar helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 85 GitHub stars
- 3 forks
- updated 2026-06-25
- primary language: Swift
- 10 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 15/100 |
| stars | 41/100 |
| topics | 100/100 |
| outlook | 51/100 |
| quality | 55/100 |
| recency | 40/100 |
| adoption | 34/100 |
| production | 51/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/nanvon/cc-bar) · [← Back to Misc](./README.md)</sub>
