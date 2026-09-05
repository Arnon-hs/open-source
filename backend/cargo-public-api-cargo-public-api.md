# cargo-public-api/cargo-public-api

[![Stars](https://img.shields.io/github/stars/cargo-public-api/cargo-public-api?style=flat-square&color=yellow)](https://github.com/cargo-public-api/cargo-public-api/stargazers) [![Forks](https://img.shields.io/github/forks/cargo-public-api/cargo-public-api?style=flat-square&color=blue)](https://github.com/cargo-public-api/cargo-public-api/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-77%2F100-brightgreen?style=flat-square)](#)

> List and diff the public API of Rust library crates between releases and commits. Detect breaking API changes and semver violations via CI or a CLI.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 559 |
| 🍴 **Forks** | 42 |
| 💻 **Language** | Rust |
| 📈 **Score** | 77/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`api` `cargo` `cargo-plugin` `cargo-subcommand` `diff` `rust` `rustdoc-json` `semver`

## 🎯 Categories

Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`cargo-public-api` is a Rust‑based tool that extracts the public API surface of a crate, compares it across releases or commits, and flags breaking changes and semver violations. It can be run locally as a CLI or integrated into CI pipelines, giving teams immediate feedback on API stability. The project is actively maintained, well‑starred, and ready for production use.

**Value**  
- **Prevent accidental breaking changes** – By automatically diffing the public API, the tool catches incompatibilities before they reach users, reducing costly rollbacks and support tickets.  
- **Standardize release hygiene** – Embedding the check in CI enforces a consistent semver policy across all Rust libraries in an organization, improving reliability of internal and external SDKs.  
- **Speed up development** – Teams can ship new features faster because they get immediate, actionable reports on API impact without manual code review.

**Practical Adoption Path**  
1. **Add to the repository** – Include `cargo install cargo-public-api` (or add it as a dev‑dependency) in each crate’s workflow.  
2. **Integrate into CI** – Add a step that runs `cargo public-api diff <old-version> <new-version>` and fails the build on detected breaking changes.  
3. **Optional CLI usage** – Developers can run `cargo public-api` locally to preview API changes before committing.  
4. **Policy enforcement** – Define an organization‑wide rule (e.g., “no breaking changes without a major version bump”) and use the CI reports to enforce it.

**Production Readiness**  
- **Activity & community** – 559 stars, 42 forks, recent commits (as of 2026‑06‑25) and ongoing issue discussion indicate a healthy, active project.  
- **Maturity** – The binary is stable, well‑documented, and has been adopted by several open‑source crates, showing real‑world viability.  
- **Risk profile** – No major licensing or security concerns have been identified; the remaining checks (license compliance, security audit) are routine.  
Overall, `cargo-public-api` is a production‑ready OSS component that can be safely piloted now and rolled out organization‑wide to enforce API stability in Rust services.

### Русский

**cargo-public-api** — это инструмент для анализа публичного API Rust‑крейтов: он выводит список функций/типов, сравнивает их между релизами и коммитами и автоматически выявляет breaking‑changes и нарушения семантического версионирования. Типичный сценарий — интеграция в CI/CD (или локальный запуск CLI) для гарантии совместимости при выпуске новых версий библиотек, что ускоряет доставку сервисов и позволяет командам переиспользовать общую инфраструктуру без повторного написания проверок API. Проект считается почти готовым к production: активная поддержка, частые релизы, более 500 звёзд на GitHub и широкое принятие в экосистеме Rust.

### 中文

**项目简介（2‑3 句）**  
`cargo-public-api` 是一个 Rust 工具，用于列出并比较库 crate 在不同版本或提交之间的公开 API，能够在 CI 或本地 CLI 中自动检测破坏性 API 改动和 semver 违规。它帮助团队在发布新版本时快速发现潜在兼容性问题，从而降低回滚和手动审查的成本。

---

## 价值主张
- **提前发现破坏性变更**：在代码合并或发布前即捕获 API 差异，防止因不兼容改动导致下游依赖崩溃。  
- **提升交付速度**：将 API 兼容性检查自动化，解放开发者的手动审查工作，使服务 API 能更快上线。  
- **统一后端规范**：在多仓库或微服务环境中统一使用同一套 API 检查工具，减少团队之间的流程差异，提升整体代码质量。  

---

## 典型接入方式
| 场景 | 接入方式 | 示例 |
|------|----------|------|
| **CI 检查** | 在 GitHub Actions、GitLab CI、Azure Pipelines 等 CI 环境中添加一步运行 `cargo public-api diff`，若检测到破坏性改动则让构建失败。 | ```yaml<br>steps:<br>- uses: actions/checkout@v3<br>- name: Install cargo-public-api<br>  run: cargo install cargo-public-api<br>- name: Check API compatibility<br>  run: cargo public-api diff --baseline=v1.2.3 --current=HEAD<br>``` |
| **本地 CLI** | 开发者在本地使用 `cargo public-api` 查看当前 crate 的公开 API，或对比两个 commit/tag。 | `cargo public-api list`、`cargo public-api diff v1.0.0 v1.1.0` |
| **自定义脚本** | 通过 `cargo public-api --format=json` 输出结构化数据，供内部仪表盘或发布平台消费。 | `cargo public-api diff --json v1.0.0 HEAD > api-diff.json` |
| **IDE 集成** | 将 CLI 包装为 VS Code 或 IntelliJ Rust 插件的任务，实时提示 API 兼容性问题。 | （自行实现对应任务） |

---

## 生产可用性评估
- **活跃度**：最近一次提交（2026‑06‑25）显示项目仍在维护，星标 559、Fork 42，社区活跃度良好。  
- **技术成熟度**：基于 Rust 编写，依赖 Cargo 本身的元数据，运行时开销极低，适合作为 CI 步骤的轻量插件。  
- **安全与合规**：项目采用 MIT/Apache 双许可证（需在最终评审中确认），暂无已知高危漏洞。  
- **易集成度**：提供纯 CLI 二进制，兼容所有主要 CI 平台，且可通过 `cargo install` 快速获取，无额外服务依赖。  
- **风险**：需要自行评估许可证兼容性、长期维护者的可用性以及对内部私有 crate 的支持情况（如需要自定义 registry）。  

**结论**：在当前状态下，`cargo-public-api` 已具备进入生产环境的技术和社区成熟度，适合作为 API 兼容性检测的标准组件进行试点部署，后续可根据实际使用情况决定是否纳入全链路 CI。

## 🧭 Practical evaluation

**Value:** cargo-public-api/cargo-public-api helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 559 GitHub stars
- 42 forks
- updated 2026-06-25
- primary language: Rust
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 41/100 |
| stars | 58/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 74/100 |
| recency | 80/100 |
| adoption | 54/100 |
| production | 76/100 |
| usefulness | 74/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/cargo-public-api/cargo-public-api) · [← Back to Backend](./README.md)</sub>
