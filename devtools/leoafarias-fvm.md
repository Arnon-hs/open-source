# leoafarias/fvm

[![Stars](https://img.shields.io/github/stars/leoafarias/fvm?style=flat-square&color=yellow)](https://github.com/leoafarias/fvm/stargazers) [![Forks](https://img.shields.io/github/forks/leoafarias/fvm?style=flat-square&color=blue)](https://github.com/leoafarias/fvm/network) [![Language](https://img.shields.io/badge/lang-Dart-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> Flutter Version Management: A simple CLI to manage Flutter SDK versions.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 5.5k |
| 🍴 **Forks** | 280 |
| 💻 **Language** | Dart |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `dart` `flutter` `flutter-releases` `flutter-sdk-versions` `fvm` `sdk`

## 🎯 Categories

DevTools · Libraries & SDKs · Mobile

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`leoafarias/fvm` (Flutter Version Management) is a lightweight command‑line tool that lets developers install, switch, and pin specific Flutter SDK versions per project. By centralising version control, it streamlines local development, CI pipelines, and code‑review cycles, reducing “works on my machine” friction. The project is actively maintained, widely adopted (5.4k ★), and written in Dart, making it a solid OSS candidate for production use.

**Value**  
- **Time savings:** Engineers can instantly switch to the exact Flutter version required for a branch or CI job, eliminating manual SDK installs and version mismatches.  
- **Consistent environments:** Projects can lock a Flutter version in `fvm_config.json`, ensuring every team member and CI runner builds with the same toolchain, which improves reproducibility and reduces flaky builds.  
- **Workflow automation:** FVM integrates with common CI systems (GitHub Actions, GitLab CI, Bitrise, etc.) and can be scripted to fetch the correct SDK before each build, delivering faster feedback loops.

**Practical Adoption Path**  
1. **Pilot:** Add `fvm` as a dev dependency in a single repository; run `fvm install <version>` and update the project’s `flutter` commands to `fvm flutter …`.  
2. **CI integration:** Include `fvm install` and `fvm use` steps in the CI pipeline configuration; cache the `.fvm` directory to speed up subsequent runs.  
3. **Team rollout:** Distribute a short onboarding script (or use a package manager like Homebrew/Brew) to install the `fvm` CLI on developers’ machines; enforce the version lock via a repository‑wide `fvm_config.json`.  
4. **Scale:** Extend the same pattern across all Flutter projects in the organization, optionally publishing a shared internal Docker image that pre‑installs the required SDKs.

**Production Readiness**  
- **Activity & community:** 5.4 k stars, 280 forks, recent commits (as of 2026‑06‑24), and a vibrant issue/PR flow indicate strong community support.  
- **Stability:** The CLI is mature, with clear documentation and a stable API; no breaking changes have been reported in recent releases.  
- **Ecosystem fit:** Written in Dart, it works natively on the platforms developers already use for Flutter, and it provides straightforward hooks for CI/CD tools.  
- **Risks:** Licensing (MIT) and security posture appear clean, but a final audit of the repository’s dependency tree and maintainers’ activity is recommended before a full production rollout.  

Overall, `leoafarias/fvm` is production‑ready for a serious pilot and can be scaled organization‑wide with minimal friction.

### Русский

**leoafarias/fvm** — это CLI‑утилита для управления версиями Flutter SDK, позволяющая разработчикам быстро переключаться между разными версиями фреймворка, автоматизировать локальные задачи и ускорять CI‑потоки. Типичный сценарий внедрения: в CI/CD и на рабочих станциях команды устанавливают FVM, задают требуемую версию Flutter в конфигурационном файле и используют единый набор команд для сборки и тестирования, что сокращает время на настройку окружения и повышает согласованность результатов. Проект считается готовым к production‑использованию: активная поддержка (обновления до 2026‑06‑24), более 5 000 звёзд, широкое принятие в сообществе и стабильный набор функций, однако финальная проверка лицензии, безопасности и наличия активных мейнтейнеров всё‑ещё требуется.

### 中文

**项目简介**  
leoafarias/fvm（Flutter Version Management）是一款轻量级的命令行工具，用于在同一台机器上快速切换和管理多个 Flutter SDK 版本。它通过统一的 CLI 接口，让开发者无需手动下载、解压或修改环境变量，即可在不同项目间使用对应的 Flutter 版本。

**价值**  
- **提升开发效率**：一条命令即可切换 SDK，避免因版本不匹配导致的编译错误和调试时间浪费。  
- **自动化本地任务**：在 CI/CD 流水线或本地脚本中直接指定 Flutter 版本，确保构建环境始终一致。  
- **加速代码评审**：评审者可以快速复现提交者的环境，减少因版本差异产生的沟通成本。

**典型接入方式**  
1. **本地使用**：`fvm install <version>` 下载指定版本；`fvm use <version>` 为当前项目设定默认版本；`fvm flutter <args>` 直接以该版本运行 Flutter 命令。  
2. **CI 集成**：在 CI 脚本（如 GitHub Actions、GitLab CI）中添加 `fvm install` 与 `fvm use` 步骤，随后所有 `flutter` 命令均通过 `fvm flutter` 调用，确保构建使用正确的 SDK。  
3. **IDE 插件**：多数主流 IDE（VS Code、Android Studio）已提供 FVM 插件，可在 UI 中配置项目的 Flutter 版本，实现“一键切换”。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑24，项目拥有 5,466+ 星、280+ Fork，最近一次提交在同一天，表明维护活跃。  
- **生态兼容**：基于 Dart 实现，天然兼容 Flutter 生态；已被多家企业和开源项目在生产环境中采用。  
- **成熟度**：提供完整的 CLI、API 文档及示例，支持 Windows、macOS、Linux 三大平台，具备完整的错误报告与回滚机制。  
- **风险**：目前未发现重大许可证或安全漏洞，但建议在正式上线前进行一次许可证合规审查，并监控依赖的 Dart 包安全报告。  

综合来看，FVM 已具备在生产环境中大规模推广的技术成熟度和社区支持，是提升 Flutter 开发与 CI 流程效率的可靠工具。

## 🧭 Practical evaluation

**Value:** leoafarias/fvm helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 5466 GitHub stars
- 280 forks
- updated 2026-06-24
- primary language: Dart
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 61/100 |
| stars | 80/100 |
| topics | 88/100 |
| outlook | 80/100 |
| quality | 82/100 |
| recency | 80/100 |
| adoption | 74/100 |
| production | 74/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/leoafarias/fvm) · [← Back to DevTools](./README.md)</sub>
