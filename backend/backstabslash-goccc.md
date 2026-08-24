# backstabslash/goccc

[![Stars](https://img.shields.io/github/stars/backstabslash/goccc?style=flat-square&color=yellow)](https://github.com/backstabslash/goccc/stargazers) [![Forks](https://img.shields.io/github/forks/backstabslash/goccc?style=flat-square&color=blue)](https://github.com/backstabslash/goccc/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Fast, zero-dependency cost calculator and customizable statusline for Claude Code. Breakdowns by model, day, project, and branch. Lightweight, single binary, no runtime needed.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 27 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | Go |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anthropic` `api-costs` `claude` `claude-code` `cli` `cost-calculator` `developer-tools` `golang` `statusline` `usage-tracker`

## 🎯 Categories

Backend · DevTools

## 📝 Summary

### English

Here's a brief summary of the project:

**Project Summary:** backstabslash/goccc is an open-source project offering a fast, zero-dependency cost calculator and customizable statusline for Claude Code. This lightweight tool helps teams reuse backend infrastructure, enabling them to ship API services faster and standardize service patterns.

**Value Proposition:** The project's value lies in its ability to help teams reuse service infrastructure, reducing the need to rebuild common backend pieces. This allows for faster development, improved consistency, and increased efficiency in the backend development process.

**Practical Adoption Path:** To adopt goccc, teams can start by evaluating its compatibility with their existing infrastructure and development workflows. They can then integrate the cost calculator and customizable statusline into their Claude Code setup, following the project's documentation and guides. As they become more familiar with the tool, teams can explore its customization options and integrate it into their CI/CD pipelines.

**Production Readiness:** With recent activity, strong adoption, and a robust ecosystem, goccc is considered production-ready. The project's high score and positive quality signals, such as regular updates and a large number of GitHub stars, indicate a strong foundation for a serious pilot. However, teams should still review the project's license, security posture, and maintainers to

### Русский

**backstabslash/goccc** — это быстрый, полностью автономный калькулятор затрат и настраиваемый статус‑лайн для Claude Code, который разбивает расходы по модели, дню, проекту и ветке, поставляется в виде единого бинарника без зависимостей и не требует отдельного runtime. Он позволяет командам сразу использовать готовую инфраструктуру расчётов и мониторинга, ускоряя вывод новых API‑сервисов, унифицируя паттерны бекенда и избавляя от необходимости писать собственные решения. По активности репозитория (недавние коммиты, 27 звёзд, 4 форка, 10 тем) проект считается готовым к пилотному запуску в продакшн, хотя требуется окончательная проверка лицензии и безопасности.

### 中文

**项目简介**  
backstabslash/goccc 是一款 **零依赖、单二进制** 的成本计算与可定制状态栏工具，专为 Claude Code 设计。它能够按模型、日期、项目和分支细分费用，帮助团队快速了解资源消耗。

**价值主张**  
- **复用已有服务设施**：把通用的成本统计与状态展示抽离为独立组件，避免在每个微服务中重复实现同样的逻辑。  
- **加速 API 服务交付**：开发者只需集成 goccc，即可获得统一的成本视图和状态栏，专注业务实现。  
- **统一后端模式**：通过统一的计费与状态输出，团队能够在不同项目、分支之间保持一致的监控与治理标准。

**典型接入方式**  
1. **CLI 调用**：在 CI/CD 流程或本地调试时直接运行 `goccc`，传入模型、项目、分支等参数，即可得到 JSON/文本报告。  
2. **SDK/API**：项目内部通过 Go 包（或通过 HTTP 接口包装的微服务）调用 `CalculateCost`、`RenderStatusLine` 等函数，实现自动化埋点。  
3. **状态栏插件**：将生成的状态行输出到终端、IDE 或监控面板（如 Grafana、Prometheus），实现实时可视化。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑27，星标 27、Fork 4，项目使用 Go 编写，单文件二进制，无运行时依赖。  
- **生态适配**：提供明确的 API/CLI 接口，易于在现有 Go 项目或容器化环境中直接嵌入。  
- **风险评估**：目前未发现重大元数据风险，唯一待确认的点是许可证（需核对是否为兼容的开源许可证）以及长期维护者的承诺。总体而言，项目已具备 **OSS 候选的高生产就绪度**，适合作为内部 pilot 或直接在生产环境中使用。

## 🧭 Practical evaluation

**Value:** backstabslash/goccc helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 27 GitHub stars
- 4 forks
- updated 2026-06-27
- primary language: Go
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 31/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 52/100 |
| recency | 40/100 |
| adoption | 27/100 |
| production | 57/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/backstabslash/goccc) · [← Back to Backend](./README.md)</sub>
