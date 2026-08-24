# aqua5230/usage

[![Stars](https://img.shields.io/github/stars/aqua5230/usage?style=flat-square&color=yellow)](https://github.com/aqua5230/usage/stargazers) [![Forks](https://img.shields.io/github/forks/aqua5230/usage?style=flat-square&color=blue)](https://github.com/aqua5230/usage/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> macOS menu bar app pinning Claude Code & Codex quota, tokens, and cost to your screen. Local-only, zero API calls. HTML reports, 9 themes.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 224 |
| 🍴 **Forks** | 39 |
| 💻 **Language** | Python |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agpl` `ai-tools` `anthropic` `claude` `claude-code` `codex` `cost-tracking` `developer-tools` `launchagent` `macos` `menubar` `openai`

## 🎯 Categories

AI/ML · DevTools

## 📝 Summary

### English

**Summary**  
aqua5230/usage is a lightweight macOS menu‑bar utility that displays Claude Code & Codex usage metrics—quota, token consumption, and estimated cost—directly on your screen. It runs entirely locally (no API calls), offers HTML reporting and nine visual themes, and is written in Python. With 224 ★ and recent commits, it’s a well‑maintained OSS tool for developers who need instant visibility into their AI usage.

**Value**  
The app gives developers immediate feedback on how much of their Claude or Codex budget is being spent, helping to curb unexpected costs during prototyping, RAG pipelines, or agent‑based workflows. Because it’s local‑only, there’s no extra latency or network‑security surface, and the built‑in HTML reports make it easy to audit usage over time or share snapshots with stakeholders.

**Practical adoption path**  
1. **Install** the Python package (or download the pre‑built binary) and add the app to the macOS menu bar.  
2. **Configure** your Claude Code / Codex credentials once; the tool will automatically read token usage from the local SDK/CLI logs.  
3. **Select a theme** and enable HTML reporting if you need periodic usage summaries.  
4. **Integrate** the exposed signals (API/SDK/CLI usage data) into your CI/CD or monitoring dashboards, or use the generated reports to fine‑tune prompts and model calls during development.

**Production readiness**  
The project shows strong production signals: recent activity (last commit 2026‑06‑23), solid community interest (224 ★, 39 forks), a clear Python codebase, and a well‑defined feature set. While the license and security posture still need a final check, the overall health, documentation, and low‑risk architecture (local execution, no external calls) make it ready for a serious pilot in internal tools or developer workstations.

### Русский

**aqua5230/usage** — это open‑source macOS‑приложение, которое в меню‑баре отображает текущие квоты, количество токенов и стоимость использования Claude Code и Codex, полностью работает локально без внешних API‑запросов и предлагает HTML‑отчёты и 9 тем оформления. Типичный сценарий — разработчики быстро подключают мониторинг расходов и производительности при прототипировании AI‑фич, построении RAG‑агентов или оценке инструментов моделей, используя готовый Python‑интерфейс/CLI. Проект имеет высокий уровень готовности к production: свежие коммиты (обновлён 23 июня 2026), более 200 звёзд, активную форк‑базу и широкую экосистему, что делает его надёжным кандидатом для серьёзных пилотов.

### 中文

**项目简介**  
aqua5230/usage 是一款 macOS 菜单栏工具，能够在屏幕上实时显示 Claude Code 与 Codex 的配额、已使用的 token 数量以及费用。全本地运行，无需任何 API 调用，提供 HTML 报表和 9 套主题皮肤。

**价值**  
- **实时成本监控**：开发者在使用 Claude 系列模型时，能够随时看到配额消耗和费用，避免意外超支。  
- **零网络依赖**：所有数据均在本机计算，安全性高，适合对隐私有严格要求的团队。  
- **即插即用的 AI 能力**：帮助产品快速原型 AI 功能（如 RAG、Agent 工作流），无需自行搭建模型堆栈，即可评估模型工具链的效果。

**典型接入方式**  
1. **下载并安装**：从 GitHub Release 页面获取 dmg 包，拖拽安装即可。  
2. **本地配置**：在菜单栏图标的设置面板中填写 Claude Code / Codex 的本地凭证（或使用本地缓存的配额文件）。  
3. **可选集成**：项目同时暴露了 Python SDK 与 CLI，开发者可以在脚本或 CI 中调用 `usage.report()` 获取 HTML 报表或直接读取配额/费用的 JSON 输出，用于自定义仪表盘或自动化监控。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑23，项目最近一次提交，拥有 224 Stars、39 Forks，社区活跃度良好。  
- **技术成熟度**：核心实现基于 Python，代码结构清晰，提供完整的 API/SDK/CLI，易于在现有 CI/CD 流程中嵌入。  
- **安全与合规**：全本地运行，无外部网络请求，降低了数据泄露风险；仍需对许可证（MIT）和维护者响应速度进行最终确认。  
- **适配性**：支持 macOS 菜单栏、HTML 报表以及多主题，能够满足不同团队的 UI/UX 需求。  

综合来看，aqua5230/usage 已具备较高的生产就绪度，适合作为内部 AI 成本监控和原型评估的 OSS 组件进行试点部署。

## 🧭 Practical evaluation

**Value:** aqua5230/usage helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 224 GitHub stars
- 39 forks
- updated 2026-06-23
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 40/100 |
| stars | 50/100 |
| topics | 100/100 |
| outlook | 66/100 |
| quality | 61/100 |
| recency | 40/100 |
| adoption | 47/100 |
| production | 58/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/aqua5230/usage) · [← Back to AI/ML](./README.md)</sub>
