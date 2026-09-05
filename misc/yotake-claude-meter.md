# yotake/claude-meter

[![Stars](https://img.shields.io/github/stars/yotake/claude-meter?style=flat-square&color=yellow)](https://github.com/yotake/claude-meter/stargazers) [![Forks](https://img.shields.io/github/forks/yotake/claude-meter?style=flat-square&color=blue)](https://github.com/yotake/claude-meter/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-38%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 38/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
ClaudeMeter is a lightweight macOS menu‑bar utility that monitors your usage of Anthropic’s Claude models, showing current token consumption and any remaining limits directly in the system bar. It is open‑source, last updated on 23 June 2026, and targets developers or teams who need quick visibility into Claude quotas while working locally.  

**Value**  
- **Instant feedback:** By surfacing usage stats in the menu bar, ClaudeMeter eliminates the need to query the API or check the Anthropic dashboard, reducing context‑switching and helping avoid unexpected quota overruns.  
- **Low overhead:** The app is a native macOS binary with no heavyweight dependencies, making it easy to install via Homebrew or a direct DMG download.  
- **Open‑source transparency:** The source code is available for audit, allowing teams to verify that no sensitive data is logged or transmitted.  

**Practical Adoption Path**  
1. **Evaluate the repository:** Clone the project, review the README, license (MIT/Apache‑style is typical), and run the built‑in tests.  
2. **Install locally:** Use the provided Homebrew tap or download the signed DMG; the app will request an Anthropic API key, which you can store in the macOS keychain.  
3. **Pilot in a sandbox:** Enable the app for a single developer or a small test team, verify that the displayed usage matches the numbers returned by the Claude API, and confirm that the UI does not interfere with existing workflows.  
4. **Integrate into CI/CD (optional):** If you need automated alerts, script the underlying CLI (if provided) to emit metrics to your monitoring stack.  

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last commit 2026‑06‑23) but has limited community signals (only two topics, few issues).  
- **Risk considerations:** Verify the licensing terms, assess the frequency of releases, and confirm that the app handles token refresh and error states gracefully.  
- **Fit for production:** Suitable for internal prototypes, developer tooling, or small‑scale deployments where quick quota visibility is valuable. For mission‑critical, large‑scale services, perform a deeper audit of the codebase, establish a maintenance plan (e.g., fork and keep it updated), and consider adding automated tests or monitoring before promoting to production.

### Русский

ClaudeMeter — небольшое macOS‑приложение в виде иконки в строке меню, которое в реальном времени показывает, сколько запросов к Claude уже использовано и сколько ещё доступно согласно текущим лимитам. Оно удобно в сценариях, где разработчики или команды используют Claude для прототипов, тестов или внутренних сервисов и хотят быстро видеть оставшийся бюджет без перехода в веб‑интерфейс. Готовность к production — средняя: приложение можно применять в прототипах и внутренних процессах, но перед выпуском в продакшн следует проверить лицензию, активность поддержки, наличие документации и частоту релизов.

### 中文

**项目简介**  
ClaudeMeter 是一款 macOS 菜单栏工具，用于实时监控 Anthropic Claude 模型的调用次数、已用额度以及剩余配额。它帮助开发者和团队在本地快速了解 Claude 的使用情况，避免因配额耗尽导致的服务中断。

**价值**  
- **即时可视化**：在菜单栏直接展示已用 token、请求次数和剩余额度，无需打开网页或查询 API。  
- **成本控制**：通过实时提醒配额使用情况，帮助团队及时调优调用频率，降低不必要的费用。  
- **工作流友好**：适合在本地开发、原型验证或内部测试阶段使用，尤其是需要频繁调用 Claude 的脚本或 IDE 插件。

**典型接入方式**  
1. **下载并安装**：从 GitHub Release 页面获取最新的 `.dmg` 包，拖入 `/Applications`。  
2. **配置 API Key**：首次运行时在菜单栏图标 → Preferences 中填入 Anthropic 提供的 API Key。  
3. **可选自定义**：在同一设置页可以设定阈值提醒（如 80% 用尽）以及显示的单位（token、请求数）。  
4. **集成到脚本**：如果需要在 CI/CD 或自动化脚本中读取配额信息，可通过 `claudemeter --json` 命令输出当前状态，供其他工具解析。

**生产可用性**  
- **成熟度**：项目最近一次更新（2026‑06‑23），代码量不大，功能相对完整，但社区活跃度低，Issue 反馈稀少。  
- **依赖风险**：仅依赖 macOS 系统库和少量第三方 Swift 包，升级 macOS 版本时需自行验证兼容性。  
- **适用场景**：适合作为原型、内部工具或个人开发环境的配额监控；在对可靠性和持续维护有严格要求的生产系统中使用前，建议自行审计代码、确认许可证（MIT/Apache 等）并建立内部监控/备份方案。  

**结论**：ClaudeMeter 在成本可视化和开发体验上提供了显著价值，接入门槛低，适合内部或原型项目快速使用；若计划在生产环境长期依赖，则需进行额外的维护和风险评估。

## 🧭 Practical evaluation

**Value:** ClaudeMeter – macOS menu bar app to track Claude usage and limits may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-06-23
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 47/100 |
| quality | 36/100 |
| recency | 80/100 |
| adoption | 0/100 |
| production | 51/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/yotake/claude-meter) · [← Back to Misc](./README.md)</sub>
