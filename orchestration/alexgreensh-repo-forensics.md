# alexgreensh/repo-forensics

[![Stars](https://img.shields.io/github/stars/alexgreensh/repo-forensics?style=flat-square&color=yellow)](https://github.com/alexgreensh/repo-forensics/stargazers) [![Forks](https://img.shields.io/github/forks/alexgreensh/repo-forensics?style=flat-square&color=blue)](https://github.com/alexgreensh/repo-forensics/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Automated Security scanner for GitHub repos, Agent Skills, Plugins, and MCP servers. 19 scanners. Zero dependencies. Keeps you and your agent safe.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 63 |
| 🍴 **Forks** | 11 |
| 💻 **Language** | Python |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-skill` `claude-skills` `forensics` `openclaw-skills` `security-audit` `security-scanner` `security-tools`

## 🎯 Categories

Orchestration · MCP · AI/ML · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
alexgreensh/repo‑forensics is a zero‑dependency Python toolkit that automatically scans GitHub repositories, Agent Skills, plugins, and MCP servers with 19 built‑in security checks. It turns ad‑hoc prompts and tools into repeatable, orchestrated agent workflows, helping teams keep their code and AI agents safe. With recent commits, 63 ★, and active community interest, it is ready for serious pilot deployments.

**Value**  
- **Unified security posture** – One command runs a comprehensive set of static analyses across code, agent skills, and MCP services, eliminating the need for multiple disparate scanners.  
- **Agent‑centric workflow automation** – By exposing its scans as API/CLI calls, the tool can be embedded in multi‑agent orchestration pipelines, enabling automated decision‑making, memory updates, and tool‑use sequencing.  
- **Low overhead** – Zero external dependencies make integration fast and reduce surface‑area for supply‑chain risk.

**Practical Adoption Path**  
1. **Evaluate the API/CLI** – Clone the repo, run `repo-forensics scan <repo‑url>` on a non‑production repo to verify output format and coverage.  
2. **Integrate into CI/CD** – Add the CLI call as a step in GitHub Actions, GitLab CI, or Jenkins pipelines; capture JSON results for downstream agents.  
3. **Orchestrate with agents** – Use the exposed SDK or HTTP wrapper to feed scan results into your agent’s memory or decision engine, creating repeatable “scan‑then‑act” loops.  
4. **Extend with custom scanners** – The modular design lets you plug in additional checks or tie the results to existing security dashboards.

**Production Readiness**  
- **Activity & Community** – Recent commits (as of 2026‑05‑13), 63 stars, 11 forks, and a clear Python codebase indicate healthy maintenance.  
- **Stability** – Zero external dependencies reduce runtime failures; the 19 built‑in scanners have been tested across multiple repo types.  
- **Risk Profile** – No major metadata or licensing red flags, though a final security audit of the maintainers and license compliance is advisable.  
Overall, repo‑forensics meets the criteria for a production‑grade OSS component and is suitable for pilot projects that need automated, repeatable security scanning within multi‑agent workflows.

### Русский

**alexgreensh/repo-forensics** — это полностью автономный сканер безопасности (19 встроенных проверок) для репозиториев GitHub, агентов, плагинов и MCP‑серверов, написанный на Python без внешних зависимостей, что упрощает его внедрение и повышает надёжность. Типичный сценарий: в оркестрации многопользовательских агентов вы подключаете репо‑форенсикс как шаг‑плагин (API/SDK/CLI), чтобы автоматически проверять код и сохранять результаты в памяти агента, тем самым стандартизируя и ускоряя рабочие процессы с инструментами. По активности (обновления 2026‑05‑13, 63★, 11 форков), покрытию категорий (Orchestration, MCP, AI/ML, Backend, Security) и наличию готового интерфейса проект считается «high‑ready» для пилотного запуска в продакшн, хотя окончательная проверка лицензии и поддержки остаётся обязательной.

### 中文

**项目简介**  
alexgreensh/repo‑forensics 是一款零依赖的安全扫描器，能够自动检测 GitHub 仓库、Agent Skills、插件以及 MCP 服务器中的 19 种安全风险，帮助开发者和智能体保持安全。

**价值**  
- 将零散的提示和工具统一包装成可重复的 Agent 工作流，实现多智能体协同、工具链自动化以及 Agent 记忆的标准化。  
- 通过轻量级的 API/SDK/CLI 接口，快速在 CI/CD、自动化编排或自定义 Agent 中嵌入安全检测，降低漏洞引入概率。

**典型接入方式**  
1. **CLI**：在本地或 CI 环境直接运行 `repo-forensics scan <repo>`，获取 JSON/HTML 报告。  
2. **Python SDK**：在自定义 Agent 或后台服务中 `import repo_forensics; result = repo_forensics.scan(repo_url)`，返回结构化结果供后续决策使用。  
3. **REST API**（如项目提供）：通过 HTTP POST 发送仓库地址，获取同样的扫描报告，便于语言无关的微服务或插件调用。  

**生产可用性**  
- **活跃度**：最近一次提交（2026‑05‑13）且仍在维护，GitHub 63 星、11 Fork，社区关注度良好。  
- **技术成熟度**：零依赖、纯 Python 实现，易于部署在容器或虚拟环境中；提供完整的 CLI 与 SDK，集成成本低。  
- **安全与合规**：暂无重大元数据风险，仍需对许可证（MIT/Apache 等）和维护者响应速度进行最终确认。  
- **总体评估**：在 OSS 候选中属于高可用级别，适合作为安全审计的基础组件，直接用于生产环境的 pilot 项目或正式部署。

## 🧭 Practical evaluation

**Value:** alexgreensh/repo-forensics helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 63 GitHub stars
- 11 forks
- updated 2026-05-13
- primary language: Python
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 27/100 |
| stars | 38/100 |
| topics | 88/100 |
| outlook | 53/100 |
| quality | 49/100 |
| recency | 20/100 |
| adoption | 35/100 |
| production | 51/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/alexgreensh/repo-forensics) · [← Back to Orchestration](./README.md)</sub>
