# vrc-get/vrc-get

[![Stars](https://img.shields.io/github/stars/vrc-get/vrc-get?style=flat-square&color=yellow)](https://github.com/vrc-get/vrc-get/stargazers) [![Forks](https://img.shields.io/github/forks/vrc-get/vrc-get?style=flat-square&color=blue)](https://github.com/vrc-get/vrc-get/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Fast Open Source command line (vrc-get) and graphical (ALCOM) client of VRChat Package Manager (VRChat Creator Companion)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 553 |
| 🍴 **Forks** | 54 |
| 💻 **Language** | Rust |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`vpm` `vrchat` `vrchat-creator-companion` `vrchat-package-manager`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary**  
vrc-get/vrc-get is an open‑source Rust‑based CLI (vrc-get) and optional GUI (ALCOM) client for the VRChat Package Manager, designed to accelerate the day‑to‑day workflow of VRChat creators and engineers. By providing fast, scriptable access to package installation, versioning, and dependency resolution, it helps teams shorten development and review cycles and can be integrated into CI pipelines for automated feedback.

**Value**  
- **Time savings:** One‑command package installs, updates, and audits replace manual UI steps, cutting repetitive work for developers and reviewers.  
- **Automation‑ready:** The CLI outputs machine‑readable signals (API/SDK metadata, version info, error codes) that can be consumed by build scripts, CI jobs, or custom tooling, enabling continuous integration and automated quality gates.  
- **Cross‑platform consistency:** Because it runs on any platform that supports Rust binaries, teams get identical behavior locally and in CI environments, reducing “works on my machine” issues.

**Practical Adoption Path**  
1. **Pilot:** Clone the repo, install the `vrc-get` binary (via Cargo or pre‑built release), and replace manual package manager steps in a small feature branch.  
2. **Script Integration:** Wrap the CLI in npm/Yarn or PowerShell scripts that run during `npm run build` or CI stages (e.g., GitHub Actions, Azure Pipelines).  
3. **GUI Rollout (optional):** Deploy the ALCOM desktop client to non‑technical artists who prefer a visual interface, while keeping the CLI as the source of truth for automation.  
4. **Policy & Security Review:** Verify the MIT/Apache license, run a vulnerability scan on the binary, and add the repository to the organization’s allowlist.  
5. **Full‑scale rollout:** Standardize on `vrc-get` in the team’s developer onboarding docs and CI templates, deprecating the legacy VRChat Creator Companion UI for routine tasks.

**Production Readiness**  
- **Maturity:** Medium. The project has 553 stars, recent activity (last commit 2026‑06‑23), and a small but active Rust codebase, indicating functional stability for prototyping and internal tooling.  
- **Risks:** The repository lacks a formal security audit and the long‑term maintainer commitment is unclear; licensing and dependency updates should be validated before production use.  
- **Recommendation:** Suitable for internal pipelines, CI automation, and developer tooling after a brief security and dependency review. For mission‑critical production environments, consider adding a fallback to the official VRChat Creator Companion or contributing fixes upstream to improve maintainability.

### Русский

**vrc-get/vrc-get** — это быстрый open‑source клиент для VRChat Package Manager, доступный как CLI‑утилита (vrc‑get) и графический интерфейс (ALCOM). Он ускоряет ежедневные циклы разработки и ревью, позволяя автоматизировать локальные задачи и улучшать обратную связь в CI‑процессах. Проект находится на среднем уровне готовности к production: подходит для прототипов и внутренних пайплайнов, но перед масштабным внедрением рекомендуется проверить лицензирование, безопасность и наличие активных мейнтейнеров.

### 中文

**项目简介（2‑3 句）**  
vrc-get 是一款用 Rust 编写的开源工具，提供快速的命令行客户端（vrc-get）和图形化客户端（ALCOM）来管理 VRChat 包（VRChat Package Manager / VRChat Creator Companion）。它通过统一的 API/SDK/CLI 接口，让开发者在本地即可完成包的搜索、下载、构建和发布，显著提升开发与调试效率。

**价值**  
- **节省时间**：一键完成包的依赖解析、构建与上传，缩短每日的开发与代码审查循环。  
- **自动化**：可在 CI/CD 流程中调用 CLI，实现包的自动化发布、版本对齐和回滚，提升反馈速度。  
- **统一体验**：同时提供命令行和图形化界面，满足不同使用习惯的开发者。

**典型接入方式**  
1. **CLI 集成**：在项目的 `Cargo.toml` 或 CI 脚本中直接调用 `vrc-get`，如 `vrc-get install <package>`、`vrc-get publish`。  
2. **SDK 调用**：通过其公开的 Rust 库或生成的语言绑定（如 Python、Node）在自定义工具或 IDE 插件中嵌入包管理功能。  
3. **图形化客户端**：在本地机器上运行 ALCOM，使用可视化面板进行包的搜索、预览和批量操作，适合非技术人员或快速原型验证。

**生产可用性**  
- **成熟度**：项目已有 553+ 星、54+ Fork，活跃更新至 2026‑06‑23，代码基于 Rust，具备良好的性能和安全特性。  
- **适用场景**：适合内部原型、团队内部工具链或中小规模的生产环境；在大规模生产环境使用前建议进行依赖审计、许可证合规检查以及安全漏洞扫描。  
- **准备度**：当前评估为 **Medium**，具备基本的可用性和文档，但仍需确认维护者的持续活跃度以及对关键安全问题的响应速度后方可在关键业务线上全面推广。

## 🧭 Practical evaluation

**Value:** vrc-get/vrc-get helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 553 GitHub stars
- 54 forks
- updated 2026-06-23
- primary language: Rust
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 58/100 |
| topics | 50/100 |
| outlook | 68/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 54/100 |
| production | 67/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/vrc-get/vrc-get) · [← Back to DevTools](./README.md)</sub>
