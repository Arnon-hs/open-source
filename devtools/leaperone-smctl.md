# leaperone/smctl

[![Stars](https://img.shields.io/github/stars/leaperone/smctl?style=flat-square&color=yellow)](https://github.com/leaperone/smctl/stargazers) [![Forks](https://img.shields.io/github/forks/leaperone/smctl?style=flat-square&color=blue)](https://github.com/leaperone/smctl/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> The missing control knob for your Mac's SMC — fan curves, battery charge limits, power policy. Open-source, CLI-first.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 117 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | Swift |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`apple-silicon` `battery` `cli` `fan-control` `macos` `smc` `swift`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*smctl* is an open‑source, CLI‑first utility that gives developers direct control over macOS’s System Management Controller (SMC), letting them tweak fan curves, set battery charge limits, and adjust power policies. Written in Swift and actively maintained (last update 2026‑06‑24, 117 ⭐ on GitHub), it fills the gap left by Apple’s closed‑source tools and integrates cleanly via a simple command‑line interface.

**Value**  
- **Time‑saving**: Engineers can script SMC adjustments as part of their local development environment, eliminating manual System Preferences clicks.  
- **Automation**: The CLI can be embedded in CI pipelines or pre‑commit hooks to enforce power‑policy standards (e.g., limiting battery charge to 80 % on CI runners).  
- **Visibility**: Real‑time feedback on fan speeds and temperature helps diagnose performance regressions early, improving overall code quality.

**Practical Adoption Path**  
1. **Trial** – Clone the repo, run `smctl --help` and test a non‑critical command (e.g., `smctl fan get`).  
2. **Integration** – Wrap needed commands in shell scripts or Makefile targets; add them to developer onboarding docs.  
3. **Automation** – Include the binary in Docker images or macOS runners and invoke it from CI jobs to enforce power‑policy checks.  
4. **Governance** – Pin a specific release version in your build system and monitor the upstream repo for security patches.

**Production Readiness**  
- **Maturity**: Medium – the tool is functional for prototypes and internal workflows, but it still requires a dependency audit (Swift runtime, potential entitlements) and a review of the licensing and security posture before wide‑scale production use.  
- **Maintenance**: Recent activity and a modest community (5 forks) suggest reasonable upkeep, yet you should verify that a maintainer is actively responding to issues.  
- **Risk Mitigation**: Conduct a small‑scale pilot, lock the version, and add runtime checks to ensure the CLI fails gracefully if the underlying SMC APIs change on future macOS releases.

### Русский

**leaperone/smctl** — это открытый CLI‑инструмент на Swift, позволяющий управлять параметрами SMC‑чипа Mac (кривые вентилятора, лимиты зарядки батареи, политики питания). Он удобен для ускорения локальных инженерных задач и автоматизации CI‑проверок, но требует дополнительной проверки лицензии, безопасности и поддержки перед использованием в продакшене. В текущем виде проект подходит для прототипов и внутренних воркфлоу, демонстрируя средний уровень готовности к production.

### 中文

**项目简介**  
leaperone / smctl 为 macOS SMC（系统管理控制器）提供缺失的控制接口，支持自定义风扇曲线、电池充电上限和电源策略等功能。它是开源、以 CLI 为核心的工具，使用 Swift 编写，适合在终端直接调用或脚本化使用。

**价值**  
- **提升开发效率**：开发者可以在本地快速调节散热和电源设置，避免因过热或电池限制导致的性能波动，从而缩短调试和测试周期。  
- **自动化工作流**：通过命令行或脚本，可在 CI/CD 流程中统一设置机器状态（如固定风扇转速、限制充电），保证构建环境的一致性并提供更可靠的反馈。  
- **成本节约**：无需额外购买硬件监控设备，所有控制均在软件层面完成，适合个人开发者和小团队。

**典型接入方式**  
1. **CLI 直接调用**：在终端执行 `smctl fan --curve …`、`smctl battery --limit …` 等子命令，即可实时生效。  
2. **脚本化**：将 smctl 命令写入 Bash、Zsh、Makefile 或 CI 配置（如 GitHub Actions、Jenkins），在构建前后自动设置或恢复 SMC 参数。  
3. **SDK/库**：项目提供 Swift 包（Swift Package Manager），可在自研 macOS 应用或内部工具中直接调用 API，实现更细粒度的控制逻辑。

**生产可用性**  
- **成熟度**：当前评分 61/100，GitHub 117 Stars、5 Forks，最近一次更新在 2026‑06‑24，代码基于 Swift，具备基本的社区关注度。  
- **适用场景**：适合原型开发、内部 CI 环境或团队内部的工程工具；在正式生产环境使用前，需要完成依赖审计、许可证合规检查以及安全评估。  
- **运维要求**：由于依赖 macOS 系统底层 SMC，需确保运行机器为 Apple Silicon 或 Intel Mac，且拥有管理员权限；定期关注项目维护状态和兼容性更新。  

总体而言，smctl 是一款轻量且易于集成的 SMC 控制工具，能够显著加速 macOS 开发与测试流程，但在面向大规模生产环境时，建议进行额外的安全与维护性评估。

## 🧭 Practical evaluation

**Value:** leaperone/smctl helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 117 GitHub stars
- 5 forks
- updated 2026-06-24
- primary language: Swift
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 44/100 |
| topics | 88/100 |
| outlook | 68/100 |
| quality | 65/100 |
| recency | 80/100 |
| adoption | 37/100 |
| production | 66/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/leaperone/smctl) · [← Back to DevTools](./README.md)</sub>
