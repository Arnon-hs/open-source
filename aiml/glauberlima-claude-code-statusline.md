# glauberlima/claude-code-statusline

[![Stars](https://img.shields.io/github/stars/glauberlima/claude-code-statusline?style=flat-square&color=yellow)](https://github.com/glauberlima/claude-code-statusline/stargazers) [![Forks](https://img.shields.io/github/forks/glauberlima/claude-code-statusline?style=flat-square&color=blue)](https://github.com/glauberlima/claude-code-statusline/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Supercharge your Claude Code CLI experience with a powerful statusline that displays key session metrics (Git state, context usage, model info and cost) at a glance — minimal setup, maximum insight.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 40 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | Rust |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bash` `claude` `claude-code` `cli` `cost-tracking` `developer-experience` `developer-tools` `git` `observability` `open-source` `productivity` `statusline`

## 🎯 Categories

AI/ML · Productivity · Frontend · DevTools · Observability

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
glauberlima/claude-code-statusline is a Rust‑based add‑on for the Claude Code CLI that injects a compact, configurable status line into the terminal. It surfaces real‑time session data—Git branch/state, token‑usage context, model details and estimated cost—so developers can monitor their work without leaving the command line.

**Value**  
- **Immediate insight**: All the most‑relevant metrics are visible at a glance, reducing context‑switching and helping developers keep track of budget‑sensitive LLM usage.  
- **Reusable UI component**: The status line is a ready‑made front‑end element that can be dropped into any Claude‑based tool, cutting the time needed to build custom dashboards or status bars.  
- **Low‑overhead integration**: It hooks into the existing Claude Code CLI via simple configuration flags or environment variables, so no major code changes are required.

**Practical Adoption Path**  
1. **Add the crate** – Include the `claude-code-statusline` dependency in your Cargo.toml (or install the pre‑built binary).  
2. **Configure** – Enable the status line through the CLI flag `--statusline` or by setting `CLAUDE_STATUSLINE=1` and optionally customize which fields to show via a TOML/YAML config file.  
3. **Test locally** – Run a few Claude Code sessions to verify that the line updates correctly for Git state, token usage, model name and cost.  
4. **Integrate into CI/CD** – Add the same flag to any scripts that invoke Claude Code in CI pipelines or internal tooling, ensuring consistent observability across environments.  
5. **Iterate** – Adjust the displayed fields or styling (colors, symbols) to match your team’s workflow, and optionally fork the repo if you need deeper customisation.

**Production Readiness**  
- **Maturity**: Medium. The project has 40 stars, 5 forks, and was refreshed as of 2026‑06‑23, indicating recent activity but a modest community footprint.  
- **Dependencies**: Pure Rust with a small dependency tree, making it easy to audit and lock versions.  
- **Stability**: Suitable for prototypes, internal tools, or staging environments; before a critical production rollout, perform a short security/license audit and confirm that the maintainers are responsive to issues.  
- **Risk**: No major metadata concerns, but the license, long‑term maintainer commitment, and any hidden security implications should be verified during the audit phase.

Overall, the status line offers a quick win for teams that already use Claude Code, delivering richer observability with minimal UI effort, while the modest community size suggests a cautious but feasible path to production after standard due‑diligence checks.

### Русский

**glauberlima/claude-code-statusline** — это лёгкий Rust‑компонент, который добавляет к Claude Code CLI статусную строку с информацией о состоянии Git, использованном контексте, модели и стоимости запросов, позволяя разработчикам мгновенно видеть ключевые метрики без написания собственного UI. Типичный сценарий — подключение библиотеки к существующему CLI‑инструменту или прототипу продукта для ускорения создания пользовательского интерфейса и улучшения наблюдаемости. Готовность к production — средняя: проект уже стабилен и обновлён, но перед релизом в продакшн рекомендуется проверить лицензию, безопасность зависимостей и наличие активных мейнтейнеров.

### 中文

**项目简介**  
glauberlima/claude-code-statusline 为 Claude Code CLI 添加了一个信息丰富的状态栏，能够在一行内实时展示 Git 状态、上下文使用量、模型信息和费用等关键指标。只需极简配置，即可在终端中获得完整的会话概览，提升开发者的可观测性与效率。

---

### 价值点
1. **加速 UI 开发**：提供即插即用的状态栏组件，省去自行实现 UI 监控的工作，让团队把更多精力放在业务功能上。  
2. **实时洞察**：在命令行层面即可看到 Git 变更、上下文消耗、模型版本和费用等信息，帮助开发者快速定位问题并控制成本。  
3. **统一体验**：统一的状态展示规范，适用于内部工具、原型以及面向用户的 CLI 产品，提升产品的一致性和专业感。

---

### 典型接入方式
| 步骤 | 操作 | 说明 |
|------|------|------|
| 1️⃣ | **添加依赖** | 在 Rust 项目 `Cargo.toml` 中加入 `claude-code-statusline = "x.y"`（或直接克隆仓库）。 |
| 2️⃣ | **初始化** | 在 CLI 主入口调用 `statusline::init()`，传入当前会话的上下文对象（Git repo、Claude API 客户端等）。 |
| 3️⃣ | **注册信号** | 使用提供的 `Signal` API（如 `GitSignal`, `ContextSignal`, `ModelSignal`）向状态栏推送实时数据。 |
| 4️⃣ | **渲染** | 在每次命令执行结束或需要刷新时调用 `statusline::render()`，状态栏会自动在终端底部更新。 |
| 5️⃣ | **可选扩展** | 若需自定义展示内容，可实现 `StatusItem` trait 并注册到 `StatusLineBuilder`。 |

> **集成要点**：项目对外暴露的是纯 Rust 库和 CLI 插件，兼容任何基于 `clap`/`structopt` 的命令行框架；若使用其他语言的包装层，只需通过 FFI 调用或使用其提供的二进制可执行文件。

---

### 生产可用性评估
| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | ★★☆☆☆（中等） | 目前已有 40+ stars、5 forks，最近一次提交在 2026‑06‑23，活跃度尚可。 |
| **依赖风险** | 中等 | 依赖 Rust 生态的几个核心库（`git2`, `reqwest`），需检查其安全审计报告和许可证兼容性。 |
| **维护者** | 待确认 | 项目主要维护者为单一贡献者，建议在生产环境使用前与其沟通或自行 fork 维护。 |
| **安全/合规** | 初步通过 | 未发现明显的许可证或安全漏洞，但仍需进行内部的 SBOM 与漏洞扫描。 |
| **适用场景** | 原型、内部工具、成本监控面板 | 对外部用户的高可用需求建议先在内部验证并加入额外的容错/监控。 |
| **上线建议** | 1️⃣ 进行依赖审计 2️⃣ 添加单元/集成测试 3️⃣ 在预生产环境做压力与回滚演练 | 完成上述步骤后方可视为生产就绪。 |

**结论**：`glauberlima/claude-code-statusline` 是一款能够快速提升 Claude Code CLI 可观测性的轻量级插件，适合用于原型和内部工作流。若在生产环境使用，需要对依赖安全、许可证合规以及维护策略进行进一步审查和补强。

## 🧭 Practical evaluation

**Value:** glauberlima/claude-code-statusline helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 40 GitHub stars
- 5 forks
- updated 2026-06-23
- primary language: Rust
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 34/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 64/100 |
| recency | 80/100 |
| adoption | 30/100 |
| production | 66/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/glauberlima/claude-code-statusline) · [← Back to AI/ML](./README.md)</sub>
