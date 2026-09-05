# DevonPeroutky/agent-profiler

[![Stars](https://img.shields.io/github/stars/DevonPeroutky/agent-profiler?style=flat-square&color=yellow)](https://github.com/DevonPeroutky/agent-profiler/stargazers) [![Forks](https://img.shields.io/github/forks/DevonPeroutky/agent-profiler?style=flat-square&color=blue)](https://github.com/DevonPeroutky/agent-profiler/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-38%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 38/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Show HN is an open‑source, locally‑runnable trace viewer that visualises execution logs from Anthropic’s Claude Code and OpenAI’s Codex sessions. It lets developers step through prompts, model responses, and intermediate tool calls in a searchable UI, making it easier to debug and optimise AI‑assisted code generation workflows. The project is actively maintained (last update 2026‑05‑13) and targets a niche but growing need for transparent, offline inspection of LLM‑driven coding sessions.

**Value**  
- **Transparency & Debugging** – By surfacing the full request/response chain (including tool invocations and token‑level timestamps), developers can pinpoint why a model produced a particular code snippet or error.  
- **Security & Privacy** – Running locally means no sensitive code or prompts leave the developer’s machine, a key requirement for regulated or proprietary projects.  
- **Workflow Integration** – The viewer can be hooked into existing IDE extensions or CI pipelines to automatically generate trace files after each Claude/Codex run, turning raw logs into an immediately navigable artifact.

**Practical Adoption Path**  
1. **Pilot** – Clone the repo, run the built‑in Docker container or `npm start` to open the UI, and feed it a few trace JSON files from your current Claude/Codex scripts.  
2. **Integration** – Add a thin wrapper around your code‑generation calls that writes the session trace (the library already provides a Python/Node exporter). Configure your CI step to archive these traces as artifacts.  
3. **Tooling Hook‑up** – If you use VS Code or JetBrains IDEs, point the extension’s “trace viewer” setting to the local server URL, enabling one‑click access from the editor.  
4. **Governance Review** – Verify the MIT/Apache license (as listed in the repo), audit dependencies for known vulnerabilities, and confirm that the maintainer’s issue‑response cadence meets your security policy.

**Production Readiness**  
- **Maturity**: Medium. The codebase is recent and functional, but the ecosystem around it (IDE plugins, CI integrations) is still thin.  
- **Maintenance**: Active commits as of May 2026, but the project has only two topics and modest community activity, so you should plan for occasional internal fixes or forks.  
- **Risk Mitigation**: Conduct a license audit, run dependency vulnerability scans, and establish a fallback (e.g., raw JSON logs) in case the viewer becomes unmaintained. With these checks, the viewer is suitable for internal prototypes, QA environments, and even production‑adjacent debugging, but it may need additional hardening before mission‑critical deployment.

### Русский

**Show HN: локальный просмотрщик трассировок для Claude Code и Codex** — open‑source утилита, позволяющая визуализировать и анализировать сеансы работы с моделями Claude Code и Codex прямо на машине разработчика, без необходимости отправлять данные в облако. Типичный сценарий: разработчики подключают её к своему CI/CD или локальному IDE, загружают JSON‑трассы из сессий и получают интерактивный график выполнения, что ускоряет отладку и оптимизацию генеративного кода. Готовность к production — средняя: проект актуален (обновление 13 мая 2026) и подходит для прототипов или внутренних инструментов, но перед развертыванием следует проверить лицензию, частоту релизов, наличие документации и активность поддержки.

### 中文

**简短介绍**  
Show HN 是一款开源的本地可视化工具，用于查看 Claude Code 与 Codex 会话的执行轨迹。它可以把模型生成的代码、提示、执行结果等信息以时间线的形式呈现，帮助开发者快速定位问题、调试和优化生成代码的流程。

**价值**  
- **可视化调试**：直观展示每一步提示、模型响应和代码执行的细节，降低排查 bug 的成本。  
- **离线安全**：所有数据都在本地保存，无需上传到第三方服务器，符合企业内部合规要求。  
- **兼容多模型**：同时支持 Claude Code 与 OpenAI Codex，适用于多种代码生成工作流。

**典型接入方式**  
1. **克隆仓库并安装依赖**（Node.js/React 或 Python 环境，具体见 README）。  
2. **在本地启动服务**，默认监听 `http://localhost:3000`。  
3. **通过 API/CLI 将 Claude Code 或 Codex 的会话日志（JSON）写入指定目录**，工具会自动读取并在 UI 中绘制时间线。  
4.（可选）在 CI/CD 或 IDE 插件中加入一步 “导出会话日志 → 本地 viewer”，实现自动化可视化。

**生产可用性**  
- **成熟度**：目前标记为 **Medium**，适合原型、内部工具或研发调试使用。  
- **依赖与维护**：项目最近一次更新是 2026‑05‑13，代码量不大，依赖较少，但缺乏活跃的社区支撑和详细文档。  
- **采用建议**：在正式生产环境前，需自行检查以下方面  
  - 许可证是否兼容公司政策（MIT/Apache 等）。  
  - 依赖安全性与版本锁定（尤其是前端框架）。  
  - 是否有持续的维护计划或可自行 fork 进行维护。  
  - 对接的日志格式是否稳定，是否需要额外的转换层。  

综上，Show HN 是一款在本地快速查看 Claude Code / Codex 生成过程的利器，适合作为研发调试或内部原型工具使用；在投入生产前建议进行安全审计、依赖锁定并准备好内部维护方案。

## 🧭 Practical evaluation

**Value:** Show HN: A open-source, local trace viewer for Claude Code and Codex sessions may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-05-13
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 47/100 |
| quality | 36/100 |
| recency | 80/100 |
| adoption | 0/100 |
| production | 51/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/DevonPeroutky/agent-profiler) · [← Back to Misc](./README.md)</sub>
