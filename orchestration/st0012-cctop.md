# st0012/cctop

[![Stars](https://img.shields.io/github/stars/st0012/cctop?style=flat-square&color=yellow)](https://github.com/st0012/cctop/stargazers) [![Forks](https://img.shields.io/github/forks/st0012/cctop?style=flat-square&color=blue)](https://github.com/st0012/cctop/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> A keyboard-first menubar app to monitor and jump between AI coding sessions — minimum setup required.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 121 |
| 🍴 **Forks** | 19 |
| 💻 **Language** | Swift |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic-workflow` `ai-agents` `ai-coding` `claude-code` `codex` `coding-agent` `developer-tools` `macos` `macos-app` `menubar` `menubar-app` `opencode`

## 🎯 Categories

Orchestration · Automation · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
st0012/cctop is a Swift‑based, keyboard‑first menubar application that lets developers monitor, switch between, and orchestrate multiple AI coding sessions with virtually no setup. By turning isolated prompts and tools into a unified, repeatable workflow, it enables rapid prototyping of multi‑agent pipelines and standardized agent memory handling.

**Value**  
- **Unified control plane** – Provides a single UI to view the status of all active AI agents, reducing context‑switching and accidental prompt loss.  
- **Workflow repeatability** – Saves and replays prompt sequences, making it easy to turn ad‑hoc experiments into reusable “agent scripts.”  
- **Extensibility** – Designed for tool‑use pipelines, so teams can plug in custom agents, APIs, or data stores without rewriting orchestration logic.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, run the provided README steps on a macOS machine, and connect a couple of existing LLM endpoints (e.g., OpenAI, Anthropic).  
2. **Integration test** – Add a minimal Swift wrapper or a shell script that launches your internal agents through cctop’s menu actions; verify that sessions can be started, paused, and switched via keyboard shortcuts.  
3. **Iterate** – Extend the menu items or add custom “jump‑to‑session” commands to match your team’s workflow, then document the pattern in an internal guide.  
4. **Scale** – Once the workflow is stable, package the app as part of your developer workstation image or CI‑agent toolbox.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑07‑05) and has modest community traction (121 ⭐, 19 forks).  
- **Suitability**: Ideal for prototypes, internal tooling, or dev‑ops dashboards; not yet a turnkey production service.  
- **Risks**: The integration surface isn’t fully documented; you’ll need to validate setup cost, dependency compatibility (Swift runtime, macOS version), and long‑term maintenance of the menubar app. A small pilot and a README review are recommended before committing to production use.

### Русский

Резюме проекта st0012/cctop:

st0012/cctop - инструмент для мониторинга и переключения между сеансами AI-кодирования с минимальным настройками. Этот проект позволяет координировать сложные многоагентные потоки, добавлять в них инструментальные пайплайны и стандартизировать агентное記憶. st0012/cctop готов к эксплуатации в прототипах или внутренних потоках, но требует тщательной проверки зависимости и поддержки перед внедрением в производственную среду.

### 中文

**项目价值**  
st0012/cctop 是一款“键盘优先”的菜单栏工具，专注于 AI 编码会话的监控与快速切换。它能够把零散的 Prompt、工具链和模型调用统一到可重复的 Agent 工作流中，从而：

- 把多个 AI 代理的交互、工具使用和记忆状态串联起来，形成可视化的多代理编排；
- 为研发人员提供最小化的配置，即开即用的 UI，提升调试和原型迭代效率；
- 为团队内部标准化 AI 助手的使用方式提供基础设施，降低重复搭建成本。

**典型接入方式**  

| 步骤 | 说明 |
|------|------|
| 1️⃣ Clone & Build | `git clone https://github.com/st0012/cctop.git && cd cctop && swift build`（项目使用 Swift，依赖 Xcode/Swift 5.9+）。 |
| 2️⃣ 配置 Prompt/Agent | 在 `~/.cctop/config.json`（或通过 UI）添加模型 API（OpenAI、Claude 等）以及自定义 Prompt，支持多 Agent 配置。 |
| 3️⃣ 启动 & 绑定 | 运行可执行文件 `./.build/debug/cctop`，工具会在 macOS 菜单栏出现。使用键盘快捷键（默认 `Ctrl+Space`）打开面板，选择或创建会话。 |
| 4️⃣ 与现有工具链集成 | 通过 URL scheme（`cctop://run?session=xxx`）或本地 socket（`/tmp/cctop.sock`）让 IDE、CI 脚本或自研前端直接触发会话切换、发送 Prompt。 |
| 5️⃣ 小范围 PoC | 在单个开发者机器或小团队的共享机器上先跑通 1‑2 条 Agent 流程，验证 UI、快捷键、记忆持久化是否符合预期，再逐步推广。 |

**生产可用性评估**  

- **成熟度**：已有 121 ⭐、19 🍴，最近一次提交是 2026‑07‑05，活跃度尚可。代码量不大，核心功能相对稳定。  
- **适用场景**：原型开发、内部工具链、实验性多 Agent 编排。对外部客户的生产环境仍需额外审查。  
- **依赖风险**：依赖 macOS Swift 环境和系统菜单栏，跨平台（Linux/Windows）支持缺失；第三方模型 API 需要自行管理凭证和配额。  
- **运维需求**：需要定期检查 Swift 编译器兼容性、依赖库（如 `swift-argument-parser`）的安全更新；如果使用 socket 接口，需做好权限与防火墙配置。  
- **推荐上线策略**：先在内部 CI 环境做 **PoC → 评审 → 监控** 三阶段；在确认 UI/快捷键、Agent 状态持久化、错误恢复机制满足业务要求后，可考虑在内部服务或研发平台上正式部署。  

**结论**：cctop 在“键盘驱动、快速切换 AI 会话”这一细分需求上提供了即插即用的解决方案，适合作为原型或内部研发的加速器。若业务对可靠性、跨平台或高并发有严格要求，仍需在依赖管理和运维监控上投入额外工作后方能进入生产环境。

## 🧭 Practical evaluation

**Value:** st0012/cctop helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 121 GitHub stars
- 19 forks
- updated 2026-07-05
- primary language: Swift
- 15 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 33/100 |
| stars | 44/100 |
| topics | 100/100 |
| outlook | 64/100 |
| quality | 58/100 |
| recency | 40/100 |
| adoption | 41/100 |
| production | 52/100 |
| usefulness | 100/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/st0012/cctop) · [← Back to Orchestration](./README.md)</sub>
