# mihaigalos/dusage

[![Stars](https://img.shields.io/github/stars/mihaigalos/dusage?style=flat-square&color=yellow)](https://github.com/mihaigalos/dusage/stargazers) [![Forks](https://img.shields.io/github/forks/mihaigalos/dusage?style=flat-square&color=blue)](https://github.com/mihaigalos/dusage/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> 💾 A command line disk usage information tool.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 120 |
| 🍴 **Forks** | 3 |
| 💻 **Language** | Rust |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bash` `cli` `command-line` `command-line-tool` `commandline-tool` `df` `fish` `rust` `shell` `zsh`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary**  
mihaigalos/dusage is a lightweight, Rust‑based command‑line tool that reports detailed disk‑usage statistics. It is positioned as a fast, script‑friendly utility that can be integrated into AI/ML pipelines to provide storage‑aware context for data‑intensive workflows.

**Value**  
- **AI‑aware resource management** – By exposing precise disk‑usage metrics, dusage lets developers programmatically monitor and react to storage constraints when training models, serving embeddings, or running retrieval‑augmented generation (RAG) pipelines.  
- **Rapid prototyping** – Its simple CLI and clear exit codes make it easy to embed in shell scripts, CI jobs, or orchestration tools (e.g., Airflow, Prefect), enabling quick “disk‑health” checks before launching expensive AI jobs.  
- **Zero‑model overhead** – Unlike full‑blown monitoring stacks, dusage adds only a single binary with minimal dependencies, keeping the overall AI stack lightweight.

**Practical Adoption Path**  
1. **Evaluation** – Clone the repo, compile with Cargo, and run `dusage --help` to verify output formats (JSON, CSV, human‑readable).  
2. **Integration** – Wrap the binary in a small wrapper script or invoke it directly from your AI pipeline (e.g., as a pre‑step in a training Dockerfile or a Lambda function).  
3. **Automation** – Use the exit status or parsed JSON to trigger alerts, auto‑scale storage, or prune old artifacts before starting a new model run.  
4. **Extensibility** – Because it’s written in Rust, you can add custom reporters (e.g., Prometheus exporter) or extend the CLI without pulling in heavyweight libraries.

**Production Readiness**  
- **Maturity** – Medium. The project has 120 stars, recent commits (as of 2026‑05‑11), and a clean Rust codebase, indicating reasonable stability for internal use.  
- **Dependencies** – Minimal (standard Rust crates), which eases security vetting and container image sizing.  
- **Maintenance** – The repo shows activity but lacks a large contributor base; a short review of the license, issue backlog, and response times is advisable before committing to long‑term production.  
- **Risk Mitigation** – Conduct a security scan of the compiled binary, pin the exact version in your CI/CD pipeline, and implement fallback monitoring (e.g., OS‑level `df`) in case the tool becomes unavailable.  

Overall, dusage is a practical, low‑overhead addition for teams that need storage awareness in AI workflows, with a clear path from prototype to production after a brief security and maintenance review.

### Русский

**mihaigalos/dusage** — это лёгкий CLI‑инструмент на Rust для быстрой оценки использования дискового пространства, который можно подключить к прототипам AI‑сервисов (RAG, агентные воркфлоу) для получения метрик о файлах и каталогах без необходимости писать собственный парсер. Типичный сценарий — запуск `dusage` в пайплайнах CI/CD или внутри контейнеров, где полученные данные передаются в модели или скрипты анализа. Готовность к production — средняя: проект имеет 120 звёзд, активные коммиты и поддерживается, но перед развёртыванием в продакшн следует проверить лицензию, безопасность зависимостей и наличие активных мейнтейнеров.

### 中文

**项目简介**  
mihaigalos/dusage 是一款基于 Rust 实现的命令行磁盘使用情况查询工具，能够快速、直观地展示文件系统的空间占用信息。

**价值**  
- 通过轻量级的 CLI，帮助开发者和运维人员在本地或 CI 环境中快速定位磁盘占用热点，提升故障排查和资源规划效率。  
- 兼容多平台（Linux、macOS），可直接集成到脚本、自动化流水线或监控系统中，降低手动检查的成本。

**典型接入方式**  
1. **直接调用 CLI**：在终端或脚本中执行 `dusage [options] <path>`，获取人类可读的磁盘使用报告。  
2. **作为子进程嵌入**：在 CI/CD、Kubernetes Init 容器或自定义监控脚本里通过 `std::process::Command`（或等价语言的子进程调用）捕获输出并进行后续处理。  
3. **结合 Rust 库**：项目同时提供 `libdusage`，可在 Rust 应用中直接调用 API，获取结构化的磁盘使用数据用于自定义仪表盘或告警系统。

**生产可用性**  
- **成熟度**：GitHub 120 星、最近一次更新在 2026‑05‑11，活跃度尚可，适合作为内部原型或中小规模生产环境的磁盘监控组件。  
- **依赖与维护**：依赖主要为 Rust 标准库和少量轻量级 crate，安全风险相对低，但在正式上线前建议审计许可证（MIT/Apache 双许可）并进行一次安全扫描。  
- **可扩展性**：因为是纯 CLI/库实现，易于容器化部署或与 Prometheus、Grafana 等监控体系对接，具备从原型到生产的平滑迁移路径。  

综上，dusage 适合作为快速磁盘使用诊断的工具，接入方式灵活，经过适当的审计和监控后即可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** mihaigalos/dusage helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 120 GitHub stars
- 3 forks
- updated 2026-05-11
- primary language: Rust
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 15/100 |
| stars | 44/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 66/100 |
| recency | 80/100 |
| adoption | 36/100 |
| production | 67/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/mihaigalos/dusage) · [← Back to DevTools](./README.md)</sub>
