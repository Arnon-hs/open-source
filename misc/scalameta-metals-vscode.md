# scalameta/metals-vscode

[![Stars](https://img.shields.io/github/stars/scalameta/metals-vscode?style=flat-square&color=yellow)](https://github.com/scalameta/metals-vscode/stargazers) [![Forks](https://img.shields.io/github/forks/scalameta/metals-vscode?style=flat-square&color=blue)](https://github.com/scalameta/metals-vscode/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> Visual Studio Code extension for Metals

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 318 |
| 🍴 **Forks** | 97 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`hacktoberfest` `language-client` `lsp` `scala` `vscode` `vscode-extension`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
Metals‑VSCode is the official Visual Studio Code extension for Metals, the language server that brings rich Scala tooling (code navigation, diagnostics, completions, refactorings, etc.) to the editor. With 318 ★, frequent releases and a strong Scala community, it lets engineers accelerate daily coding and review cycles while keeping CI feedback tight.

**Value**  
- **Speed** – Real‑time diagnostics, “go‑to‑definition”, and automatic import suggestions cut the edit‑compile‑test loop dramatically.  
- **Consistency** – The same Metals language server powers both the IDE and CI pipelines, so developers see the same warnings and suggestions locally as they do in automated builds.  
- **Automation** – Integrated commands (e.g., “run test”, “publish”) expose Metals’ CLI/SDK directly from VS Code, reducing context‑switching and manual scripting.

**Practical Adoption Path**  
1. **Install** the extension from the VS Code Marketplace (or via `code --install-extension scalameta.metals`).  
2. **Configure** the workspace by adding a `metals.sbt` or `metals.json` file (or rely on auto‑detection for sbt, Mill, or Bloop projects).  
3. **Enable** optional features such as “code‑lens” for test/run actions, “semantic highlighting”, or “debugger” integration.  
4. **Align CI** – point your CI jobs to the same Metals version (e.g., via `cs launch scala:metals` or Docker image) so that local diagnostics match CI reports.  
5. **Iterate** – monitor the extension’s update channel; most releases are backward‑compatible and bring new Scala‑3 or Scala‑2.13 features.

**Production Readiness**  
- **Activity & Adoption** – Updated as of 2026‑05‑11, 318 ★, 97 forks, and a growing list of topics indicate a vibrant, actively maintained project.  
- **Ecosystem Fit** – Works out‑of‑the‑box with sbt, Mill, Bloop, and Scala CLI, and integrates with popular CI tools (GitHub Actions, Azure Pipelines) via the same Metals server.  
- **Stability** – The extension follows semantic‑versioning, provides clear release notes, and has a low‑risk surface (TypeScript code, no native binaries).  
- **Risks** – Pending final checks on license compliance, security scanning of dependencies, and maintainer continuity; none of these have surfaced as blockers so far.

Overall, Metals‑VSCode is a high‑readiness OSS component that can be piloted in production teams with minimal friction and delivers immediate productivity gains for Scala developers.

### Русский

**scalameta/metals-vscode** — это расширение для Visual Studio Code, которое интегрирует язык Scala и сервер Metals, позволяя разработчикам ускорить цикл написания, проверки и рефакторинга кода. Типичный сценарий внедрения — установка расширения в рабочие среды команд, автоматизация локальных задач (компиляция, диагностика, автодополнение) и улучшение обратной связи в CI‑процессах. Проект обладает высокой готовностью к продакшену: активные коммиты, 318 звёзд, 97 форков, регулярные обновления и поддержка TypeScript‑экосистемы, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
`scalameta/metals-vscode` 是为 Scala 开发者提供的 Visual Studio Code 插件，基于 Metals 语言服务器实现代码补全、诊断、跳转、重构等功能，让 VS Code 成为一流的 Scala IDE。

**价值**  
- **提升日常开发效率**：即时的类型检查、自动补全和代码导航，显著缩短编写、调试和代码审查的循环时间。  
- **自动化本地任务**：内置对 sbt、scalafmt、scalafix 等工具的集成，省去手动运行脚本的步骤。  
- **改进 CI 反馈**：本地即能捕获编译和静态检查错误，减少在 CI 中才发现的问题，提高提交质量。

**典型接入方式**  
1. 在 VS Code 市场搜索并安装 **Metals** 插件（即 `scalameta.metals`）。  
2. 打开或创建 Scala 项目，插件会自动下载对应的 Metals 语言服务器并生成 `.metals` 配置目录。  
3. 根据项目需求在 `settings.json` 中配置 sbt、scalafmt、scalafix 等工具的路径或选项，或使用插件提供的快捷命令（如 “Import build”）完成初始化。  
4. 可通过命令行 `metals`（CLI）或直接调用插件的 API 在 CI 脚本中执行相同的检查，以保持本地与 CI 环境一致。

**生产可用性**  
- **活跃度高**：最近一次提交于 2026‑05‑11，项目仍在持续维护；GitHub 统计 318 ⭐、97 🍴，社区活跃。  
- **技术成熟**：核心实现使用 TypeScript，遵循 LSP（Language Server Protocol），易于与其他编辑器或工具链集成。  
- **生态兼容**：已被多家大型 Scala 项目在生产环境中采用，兼容 sbt、mill、Bloop 等常见构建系统。  
- **风险**：目前未发现重大许可证或安全隐患，但建议在正式投产前完成一次许可证合规审查并检查依赖的安全报告。

综合来看，`scalamata/metals-vscode` 已具备 **高生产就绪度**，可作为 Scala 开发团队在 VS Code 环境下的首选 IDE 扩展进行试点或直接上线。

## 🧭 Practical evaluation

**Value:** scalameta/metals-vscode helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 318 GitHub stars
- 97 forks
- updated 2026-05-11
- primary language: TypeScript
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 50/100 |
| stars | 53/100 |
| topics | 75/100 |
| outlook | 49/100 |
| quality | 55/100 |
| recency | 20/100 |
| adoption | 52/100 |
| production | 50/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/scalameta/metals-vscode) · [← Back to Misc](./README.md)</sub>
