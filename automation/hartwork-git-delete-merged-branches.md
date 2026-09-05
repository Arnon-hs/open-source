# hartwork/git-delete-merged-branches

[![Stars](https://img.shields.io/github/stars/hartwork/git-delete-merged-branches?style=flat-square&color=yellow)](https://github.com/hartwork/git-delete-merged-branches/stargazers) [![Forks](https://img.shields.io/github/forks/hartwork/git-delete-merged-branches?style=flat-square&color=blue)](https://github.com/hartwork/git-delete-merged-branches/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-75%2F100-brightgreen?style=flat-square)](#)

> :fire: Command-line tool to delete merged Git branches

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 913 |
| 🍴 **Forks** | 21 |
| 💻 **Language** | Python |
| 📈 **Score** | 75/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`automation` `cleanup` `cli` `cli-tool` `command-line` `command-line-tool` `developer-tool` `developer-tools` `git` `housekeeping` `python` `python3`

## 🎯 Categories

Automation · DevTools

## 📝 Summary

### English

**Summary**  
Hartwork’s **git-delete-merged-branches** is a lightweight Python CLI that automates the safe removal of Git branches that have already been merged, eliminating a repetitive manual step in typical development workflows. With over 900 stars, recent commits, and a clear command‑line interface, it is ready for production use in both ad‑hoc scripts and scheduled automation pipelines.

**Value**  
- **Time savings:** One command replaces dozens of manual `git branch -d` operations, freeing developers to focus on coding rather than housekeeping.  
- **Reliability:** The tool checks merge status before deletion, reducing the risk of accidentally dropping active work.  
- **Integrability:** It can be invoked from CI/CD jobs, cron tasks, or any orchestration platform, enabling repeatable, auditable branch‑cleanup processes.

**Practical adoption path**  
1. **Trial:** Install via `pip install git-delete-merged-branches` and run `git-delete-merged-branches --dry-run` on a test repository to verify the selection logic.  
2. **Pilot:** Add the command to a pre‑merge or nightly pipeline (e.g., GitHub Actions, Jenkins) with appropriate branch filters and safety flags.  
3. **Scale:** Wrap the CLI in a wrapper script or container, schedule it with cron or a workflow orchestrator, and optionally integrate with notification tools (Slack, email) to report cleaned branches.

**Production readiness**  
- **Active maintenance:** Last commit on 2026‑06‑28, 913 stars, and 21 forks indicate a healthy community.  
- **Maturity:** Simple, well‑scoped Python codebase with clear CLI semantics; no complex runtime dependencies.  
- **Risk considerations:** License and security review are still required, but no major metadata or vulnerability flags have been reported. Overall, the project is a strong candidate for production deployment after a brief internal validation.

### Русский

**hartwork/git-delete-merged-branches** — это CLI‑утилита на Python, автоматизирующая удаление уже смёрженных веток в Git, избавляя разработчиков от повторяющихся ручных операций и позволяя включать очистку в CI/CD‑потоки или планировать её как периодическую задачу. Проект имеет высокий уровень готовности к продакшну: 913 звёзд, активные коммиты (последнее обновление 28 июня 2026 г.), широкую поддержку в экосистеме и ясный API/CLI, что делает его надёжным кандидатом для интеграции в любые автоматизированные рабочие процессы.

### 中文

**简短介绍**
hartwork/git-delete-merged-branches 是一个开源的命令行工具，用于删除合并的 Git 分支。它可以帮助开发者自动化重复的工作流程，减少手动操作的工作量。

**价值**
该工具的价值在于，它可以帮助开发者:

* 去除重复的手动操作
* 连接工具到可重复的流程
* 计划操作任务

**典型接入方式**
该工具可以通过以下方式接入:

* 命令行工具：直接在命令行中使用工具的命令来删除合并的 Git 分支。
* 脚本：将工具的命令写入脚本中，定时执行以自动化删除合并的 Git 分支。
* CI/CD 工具：将工具集成到 CI/CD 工具中，自动化删除合并的 Git 分支。

**生产可用性**
该工具的生产可用性非常高，原因如下：

* 最近的活动：工具最近更新（2026-06-28），表明它仍然活跃。
* 适度的采用：工具有 913 个 GitHub 星星和 21 个

## 🧭 Practical evaluation

**Value:** hartwork/git-delete-merged-branches helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 913 GitHub stars
- 21 forks
- updated 2026-06-28
- primary language: Python
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 63/100 |
| topics | 100/100 |
| outlook | 80/100 |
| quality | 75/100 |
| recency | 80/100 |
| adoption | 55/100 |
| production | 72/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/hartwork/git-delete-merged-branches) · [← Back to Automation](./README.md)</sub>
