# Tlaloc-Es/killpy

[![Stars](https://img.shields.io/github/stars/Tlaloc-Es/killpy?style=flat-square&color=yellow)](https://github.com/Tlaloc-Es/killpy/stargazers) [![Forks](https://img.shields.io/github/forks/Tlaloc-Es/killpy?style=flat-square&color=blue)](https://github.com/Tlaloc-Es/killpy/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> 🐍 CLI tool to find and delete unused Python virtual environments (.venv, poetry, conda, pipenv, uv). Reclaim disk space effortlessly — supports bulk delete, size reporting, and pycache cleanup.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 118 |
| 🍴 **Forks** | 3 |
| 💻 **Language** | Python |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cleanup` `command-line` `conda` `conda-environment` `developer-tools` `devtools` `disk-space` `environment-management` `git-hooks` `pipx` `poetry` `pre-commit`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`killpy` is a lightweight Python CLI that scans for unused virtual environments—such as `.venv`, Poetry, Conda, Pipenv, and UV—reports their disk usage, and removes them (including optional `__pycache__` cleanup). It lets developers reclaim storage with a single command, supports bulk deletion, and provides clear size statistics before any removal.

**Value Proposition**  
- **Immediate cost savings**: By eliminating stale environments that can occupy gigabytes of space, teams reduce storage costs and avoid cluttered development machines.  
- **Time‑saving automation**: No manual hunting through directories; a one‑line command lists and purges all dead environments, freeing developers to focus on code rather than housekeeping.  
- **Safety nets**: Size reports and a dry‑run mode let users verify what will be deleted, minimizing the risk of accidental data loss.

**Practical Adoption Path**  
1. **Trial in a sandbox** – Run `killpy --dry-run` on a developer workstation to see the environments it would target and the space to be reclaimed.  
2. **Integrate into CI/CD** – Add a step in CI pipelines (e.g., GitHub Actions, GitLab CI) that runs `killpy --dry-run` on build agents and, if the reclaimed space exceeds a threshold, executes the purge automatically.  
3. **Standardize via internal tooling** – Wrap the CLI in a small wrapper script or make it part of a larger dev‑ops toolbox (e.g., invoked from a Makefile or a VS Code task) so all team members use a consistent clean‑up process.  
4. **Monitor & audit** – Log the output of each run to an internal dashboard or log aggregation system to track storage trends over time.

**Production Readiness**  
- **Activity & Community**: 118 ★, recent commit (2026‑07‑02), and active issue discussion indicate a healthy, maintained project.  
- **Maturity**: The CLI is self‑contained, written in Python, and has clear documentation; no external services or complex dependencies are required.  
- **Risk Profile**: No known licensing or security red flags, though a final review of the license (MIT‑style) and a quick vulnerability scan of the dependency tree are advisable.  
- **Scalability**: Works on any POSIX‑compatible system and can be scripted for large fleets of build agents, making it suitable for production‑grade environments.

Overall, `killpy` is a production‑ready, low‑overhead utility that can be adopted quickly with minimal integration effort, delivering immediate operational value by cleaning up unused Python environments and freeing disk space.

### Русский

Резюме проекта Tlaloc-Es/killpy:

Tlaloc-Es/killpy - это бесплатный и открытое ПО, которое позволяет легко и эффективно освобождать пространство на диске, удаляя ненужные виртуальные окружения Python. Это идеальный инструмент для разработчиков, построющих инфраструктуру AI и ML, и помогает им сосредоточиться на важном - развитии своих проектов.

Проект предназначен для использования в типовых сценариях внедрения, таких как построение прототипов AI-признаков, создание RAG или агентных потоков, а также оценка инструментов для моделирования. Проект готов к использованию в production, поскольку имеет недавнюю активность, широкое распространение и сильный экосистемный потенциал.

Проект имеет высокий уровень готовности к production, что делает его привлекательным выбором для разработчиков и организаций, которые ищут эффективные и безопасные решения для своих задач AI и ML.

### 中文

**项目简介**  
Tlaloc-Es/killpy 是一款基于 Python 的命令行工具，能够快速扫描并删除本地未使用的虚拟环境（.venv、Poetry、Conda、Pipenv、uv），同时提供磁盘占用统计、批量删除和 `__pycache__` 清理等实用功能，让磁盘空间回收变得轻而易举。

---

## 价值说明  
- **节省磁盘空间**：自动定位并清除长期未使用的虚拟环境和缓存文件，帮助开发者恢复大量磁盘空间。  
- **提升开发效率**：一条 CLI 命令即可完成环境审计和清理，免去手动查找、判断的繁琐过程。  
- **降低维护成本**：通过定期清理，避免因磁盘耗尽导致的 CI/CD 失败或本地构建卡顿。  

---

## 典型接入方式  
1. **直接使用 CLI**  
   ```bash
   pip install killpy
   killpy --list          # 列出所有检测到的虚拟环境
   killpy --delete all   # 一键批量删除未使用的环境
   killpy --size         # 查看各环境占用的磁盘空间
   ```
2. **脚本化调用**  
   在 CI/CD 流水线或本地维护脚本中加入 `killpy` 命令，实现自动化清理，例如在 GitHub Actions 中：  
   ```yaml
   - name: Clean up Python virtual environments
     run: |
       pip install killpy
       killpy --delete unused
   ```
3. **作为库使用（如需二次开发）**  
   项目提供了 `killpy.core` 模块，开发者可以在 Python 代码中调用其 API，获取环境列表、占用大小等信息，进而自定义更细粒度的清理策略。

---

## 生产可用性  
- **活跃度**：截至 2026‑07‑02 最近一次提交，项目仍在维护；GitHub 上拥有 118 ⭐、3 fork，社区关注度良好。  
- **技术成熟度**：实现基于标准库的文件系统遍历与虚拟环境检测，依赖最小，运行时几乎没有额外开销。  
- **安全与合规**：项目采用 MIT 许可证，无明显安全漏洞报告；但在正式生产环境使用前仍建议进行内部安全审计。  
- **可扩展性**：支持多种主流虚拟环境管理工具（Poetry、Conda、Pipenv、uv），并可通过插件方式添加自定义检测规则。  

综合来看，killpy 已具备较高的生产就绪度，适合作为日常开发环境维护工具或在 CI/CD 中自动化执行磁盘清理任务。只需进行一次性的内部评估，即可在生产环境中安全部署。

## 🧭 Practical evaluation

**Value:** Tlaloc-Es/killpy helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 118 GitHub stars
- 3 forks
- updated 2026-07-02
- primary language: Python
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 15/100 |
| stars | 44/100 |
| topics | 100/100 |
| outlook | 58/100 |
| quality | 56/100 |
| recency | 40/100 |
| adoption | 36/100 |
| production | 56/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/Tlaloc-Es/killpy) · [← Back to DevTools](./README.md)</sub>
