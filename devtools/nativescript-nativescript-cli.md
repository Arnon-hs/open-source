# NativeScript/nativescript-cli

[![Stars](https://img.shields.io/github/stars/NativeScript/nativescript-cli?style=flat-square&color=yellow)](https://github.com/NativeScript/nativescript-cli/stargazers) [![Forks](https://img.shields.io/github/forks/NativeScript/nativescript-cli?style=flat-square&color=blue)](https://github.com/NativeScript/nativescript-cli/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> NativeScript CLI - command-line tools

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.1k |
| 🍴 **Forks** | 203 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `cli` `cross-platform` `hacktoberfest` `ios` `mobile` `nativescript`

## 🎯 Categories

DevTools · Mobile

## 📝 Summary

### English

**Summary**  
NativeScript CLI is a JavaScript‑based command‑line toolkit that streamlines the build, test, and deployment cycles for NativeScript mobile apps. By automating routine engineering tasks and providing rich API/SDK signals, it helps developers accelerate daily workflows and obtain faster CI feedback. With strong recent activity, a solid star/fork count, and broad ecosystem adoption, it is ready for serious pilot projects.

**Value**  
The CLI eliminates repetitive manual steps (project scaffolding, platform preparation, live‑sync, and packaging), cutting development iteration time and reducing human error. Its built‑in diagnostics and extensible plug‑in model give teams immediate visibility into build health, which translates into quicker code reviews and more reliable CI pipelines.

**Practical adoption path**  
1. **Evaluate** – Clone the repo, run `npm install -g nativescript` and try the `tns create` and `tns run` commands on a sample app.  
2. **Integrate** – Replace existing shell scripts with the CLI’s `tns build`, `tns test`, and `tns deploy` commands in local dev environments and CI pipelines (e.g., GitHub Actions, Azure Pipelines).  
3. **Extend** – Leverage the provided SDK hooks or write custom plug‑ins for organization‑specific tooling (e.g., linting, code signing).  
4. **Roll out** – Pilot on a single product team, collect feedback, then propagate the standardized CLI configuration across all NativeScript projects.

**Production readiness**  
The project shows high production readiness: it is actively maintained (last commit 2026‑06‑26), has a healthy community (≈1 k stars, 200+ forks), and is written in a widely‑supported language (JavaScript). While the license and security posture still need a final compliance check, the combination of recent activity, strong adoption signals, and mature feature set makes it a solid candidate for production use and broader enterprise pilots.

### Русский

NativeScript CLI — это набор командных утилит, позволяющих ускорить цикл разработки мобильных приложений на NativeScript: автоматизировать локальные задачи, ускорить сборку и тестирование, а также улучшить обратную связь в CI. Проект активно поддерживается (обновления 2026‑06‑26, 1052 звёзд, 203 форка), имеет сильные сигналы принятия в экосистеме и готов к использованию в продакшене после финального аудита лицензии и безопасности.

### 中文

**项目简介**  
NativeScript CLI（NativeScript/nativescript-cli）是一套基于 JavaScript 的命令行工具，专为 NativeScript 移动应用的创建、构建、调试和发布而设计。它提供统一的 API/SDK 接口，帮助开发者在本地快速完成日常开发、自动化任务以及 CI 流水线的反馈。

**价值**  
- **提升开发效率**：一键生成项目骨架、热重载、自动化打包，显著缩短编码‑调试‑预览的循环时间。  
- **支持自动化**：可在脚本或 CI 环境中调用 CLI 完成构建、签名、发布等重复性工作，降低人为错误。  
- **生态兼容**：与 NativeScript 框架、插件以及常见的前端工具链（npm、webpack、Gradle、Xcode）无缝集成，减少学习成本。

**典型接入方式**  
1. **本地开发**：`npm i -g @nativescript/cli` 后，使用 `ns create|run|build|deploy` 等子命令直接在终端操作项目。  
2. **CI/CD 流程**：在构建脚本（如 GitHub Actions、GitLab CI、Azure Pipelines）中安装 CLI 并执行 `ns build android|ios --release`，配合环境变量完成签名和上传。  
3. **自定义脚本**：通过 Node.js 调用 `child_process.exec` 或直接使用 CLI 提供的 JavaScript API（如 `@nativescript/cli/lib`），实现更细粒度的自动化任务（例如批量插件升级、代码质量检查）。

**生产可用性**  
- **活跃度**：截至 2026‑06‑26，项目仍在持续更新，拥有 1 052+ 星、203+ 分叉，且最近一次提交在当天完成。  
- **成熟度**：核心功能（项目创建、跨平台构建、热重载、发布）已在多个大型企业和开源项目中验证，社区文档和示例丰富。  
- **风险**：暂无重大元数据风险，但仍需在正式使用前审查许可证兼容性、依赖安全审计以及维护者响应速度。总体而言，NativeScript CLI 已具备高生产就绪度，适合作为移动端开发与 CI 自动化的关键组件进行试点或正式上线。

## 🧭 Practical evaluation

**Value:** NativeScript/nativescript-cli helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1052 GitHub stars
- 203 forks
- updated 2026-06-26
- primary language: JavaScript
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 58/100 |
| stars | 64/100 |
| topics | 88/100 |
| outlook | 77/100 |
| quality | 76/100 |
| recency | 80/100 |
| adoption | 62/100 |
| production | 70/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/NativeScript/nativescript-cli) · [← Back to DevTools](./README.md)</sub>
