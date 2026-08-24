# schpet/linear-cli

[![Stars](https://img.shields.io/github/stars/schpet/linear-cli?style=flat-square&color=yellow)](https://github.com/schpet/linear-cli/stargazers) [![Forks](https://img.shields.io/github/forks/schpet/linear-cli?style=flat-square&color=blue)](https://github.com/schpet/linear-cli/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> linear without leaving the command line: list, start, and create PRs for linear issues. agent friendly.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 701 |
| 🍴 **Forks** | 75 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `linear` `linearapp`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`schpet/linear-cli` is a TypeScript‑based command‑line tool that lets you interact with Linear directly from the terminal – you can list issues, start work, and open pull‑request drafts without leaving your shell. It’s designed to be “agent‑friendly,” making it easy to script or integrate with AI agents for automated issue handling and workflow automation. With over 700 ★ on GitHub and recent commits, it’s a mature open‑source utility ready for pilot projects.

**Value**  
The CLI adds a thin, scriptable layer over Linear’s API, enabling rapid prototyping of AI‑driven features such as automated issue triage, RAG‑based knowledge retrieval, or end‑to‑end agent workflows. By avoiding a full SDK or custom HTTP client, teams can embed Linear actions into existing CI pipelines, bots, or internal tools with minimal code.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run `npm install`, and follow the README to generate a personal API token; use simple commands like `linear list` to verify connectivity.  
2. **Integration** – Wrap the CLI calls in shell scripts or Node.js wrappers inside your AI agent or automation framework; the output is JSON‑friendly for downstream processing.  
3. **Scaling** – Replace ad‑hoc scripts with a small npm package that imports the CLI’s underlying library (if needed) and add unit tests for the specific actions you require.

**Production Readiness**  
The project shows strong production signals: recent activity (last commit 2026‑05‑14), 701 stars, 75 forks, and a clear TypeScript codebase. While licensing and security reviews are still required, the overall health, community adoption, and active maintainers make it a solid candidate for a serious pilot in production environments.

### Русский

**schpet/linear-cli** — это open‑source утилита, позволяющая управлять задачами Linear (просматривать, создавать и закрывать их, открывать PR) полностью из терминала, что упрощает интеграцию AI‑агентов и RAG‑воркфлоу без необходимости писать собственный API‑клиент. Типичный сценарий: в прототипе AI‑фичи скрипт вызывает `linear-cli` для получения списка открытых тикетов, автоматически создаёт задачу и открывает pull‑request, после чего результаты передаются в модель для дальнейшей обработки. Проект считается готовым к production‑использованию: активные коммиты, 701 звезда, 75 форков, свежий релиз (14 мая 2026) и хорошая экосистема TypeScript делают его надёжным кандидатом для пилотных внедрений, хотя окончательная проверка лицензии и безопасности всё же рекомендуется.

### 中文

**项目简介**  
schpet/linear-cli 是一款基于命令行的 Linear 客户端，能够在终端直接列出任务、启动工作流并为 Linear Issue 创建 Pull Request，天然适配 AI 代理使用场景。  

**价值**  
- **快速赋能 AI 工作流**：无需自行搭建模型堆栈，直接在 CLI 中调用 Linear 数据，为 RAG、自动化客服或代码生成等 AI 场景提供任务来源。  
- **提升开发效率**：开发者可以在本地终端完成任务查询、分配和 PR 创建，省去切换 UI 的时间，特别适合 CI/CD 或脚本化的自动化流程。  
- **易于集成**：采用 TypeScript 编写，提供 npm 包和可执行二进制，能够在任意 Node.js 环境或容器中直接调用。  

**典型接入方式**  
1. **npm 安装**：`npm i -g @schpet/linear-cli`，全局安装后即可在终端使用 `linear` 命令。  
2. **环境配置**：在项目根目录或 CI 环境中配置 `LINEAR_API_KEY`（或通过 `linear login` 完成 OAuth），确保 CLI 能访问 Linear API。  
3. **脚本化调用**：在 Bash、PowerShell 或 CI/CD pipeline（如 GitHub Actions、GitLab CI）中直接运行 `linear list`, `linear start <issue-id>`，或 `linear pr create <issue-id>`，将返回的 JSON 结果作为后续 AI 代理或 RAG 系统的输入。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑14，项目拥有 701 星、75 Fork，最近一次提交在同一天，说明维护活跃。  
- **技术成熟度**：使用 TypeScript 编写，拥有完整的 README、示例和错误处理，易于在企业内部审计。  
- **风险评估**：暂无重大元数据或许可证风险，但仍建议在正式投产前进行一次安全审计（依赖库漏洞扫描）并确认维护者的响应速度。  
- **适配度**：对需要在 CI 中自动化处理 Linear Issue 的团队（尤其是构建 AI 代理或 RAG 流程的组织）可以直接进行小规模 PoC，验证后即可在生产环境推广。  

综上，schpet/linear-cli 具备高可用性、易集成的特性，是在命令行层面为 Linear 加入 AI 能力的实用工具。

## 🧭 Practical evaluation

**Value:** schpet/linear-cli helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 701 GitHub stars
- 75 forks
- updated 2026-05-14
- primary language: TypeScript
- 3 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 47/100 |
| stars | 61/100 |
| topics | 38/100 |
| outlook | 50/100 |
| quality | 51/100 |
| recency | 20/100 |
| adoption | 57/100 |
| production | 49/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/schpet/linear-cli) · [← Back to DevTools](./README.md)</sub>
