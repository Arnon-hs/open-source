# bruin-data/ingestr

[![Stars](https://img.shields.io/github/stars/bruin-data/ingestr?style=flat-square&color=yellow)](https://github.com/bruin-data/ingestr/stargazers) [![Forks](https://img.shields.io/github/forks/bruin-data/ingestr?style=flat-square&color=blue)](https://github.com/bruin-data/ingestr/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> ingestr is a CLI tool to copy data between any databases with a single command seamlessly.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.7k |
| 🍴 **Forks** | 137 |
| 💻 **Language** | Go |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bigquery` `copy-database` `data-ingestion` `data-integration` `data-pipeline` `duckdb` `ingestion-pipeline` `mssql` `postgresql` `snowflake`

## 🎯 Categories

Data · Database

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
ingestr is a Go‑based CLI that lets you copy data between any databases with a single command, making data migration and synchronization as simple as running `ingestr copy`. With 3.7 k ★, recent commits, and broad topic coverage, it’s a mature open‑source tool that can be dropped into AI/ML pipelines to feed data into RAG, agent workflows, or prototype model‑driven features.

**Value**  
- **Speed‑to‑experiment:** eliminates the need to hand‑craft ETL scripts, so teams can prototype AI features or evaluate model tooling in minutes rather than days.  
- **Universal connectivity:** supports a wide range of source and target databases, letting you stitch together heterogeneous data stores without custom adapters.  
- **CLI‑first workflow:** fits naturally into CI/CD pipelines, container images, or local dev environments, enabling reproducible data moves for training, inference, or evaluation.

**Practical Adoption Path**  
1. **Trial:** Install the binary (`go install github.com/bruin-data/ingestr@latest`) and run a simple copy command between two test databases to verify connectivity and performance.  
2. **Integration:** Wrap the CLI in a script or Makefile step within your data‑preparation pipeline; alternatively, invoke the underlying Go SDK if tighter programmatic control is needed.  
3. **Automation:** Add the command to CI/CD jobs (GitHub Actions, GitLab CI) to keep staging/production datasets in sync before model training or inference runs.  
4. **Scaling:** For large‑scale migrations, combine `ingestr` with parallel execution or container orchestration (Kubernetes Jobs) and monitor logs via the built‑in verbose mode.

**Production Readiness**  
- **Activity & Community:** 3,747 stars, 137 forks, last update on 2026‑07‑02, and a healthy set of topics indicate an active project with responsive maintainers.  
- **Stability:** The CLI is written in Go, offering static binaries, low runtime overhead, and easy cross‑platform deployment.  
- **Risk Assessment:** No immediate licensing or security red flags, though a final review of the license (MIT/Apache) and a quick vulnerability scan of the binary are recommended before enterprise rollout.  

Overall, ingestr is production‑grade for pilots and can be promoted to full‑scale data pipelines once the brief security/license audit is completed.

### Русский

Резюме проекта ingestr:

ingestr - инструмент командной строки для копирования данных между любыми базами данных с помощью единой команды. Это позволяет легко добавлять функциональность AI без создания от начала до конца моделирующего стека. Проект готов к сериозному пилоту, имея высокий уровень готовности к production, активное развитие и сильную экосистему.

### 中文

**ingestr 简介**

ingestr 是一个命令行工具，能够通过单个命令轻松地将数据从任意数据库复制到另一个数据库。

**价值**

ingestr 的价值在于，它可以帮助开发者快速添加 AI 能力，而无需从头开始搭建模型栈。它可以用于各种场景，例如：

* 快速 prototyping AI 特性
* 构建 RAG 或 agent 工作流
* 评估模型工具

**典型接入方式**

ingestr 支持多种接入方式，包括：

* API/SDK：通过 API 或 SDK 接入 ingestr
* CLI：直接通过命令行接入 ingestr
* 语言 metadata：支持多种编程语言的 metadata 接入

**生产可用性**

ingestr 的生产可用性非常高，原因有：

* 近期活跃：ingestr 的维护者最近才更新了代码
* 强大的社区：ingestr 有超过 3747 个 GitHub 星标和 137 个分支
* 强大的生态系统：ingestr 支持多种数据库和编程语言
* 高风险评估：风险评估为 81/

## 🧭 Practical evaluation

**Value:** bruin-data/ingestr helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 3747 GitHub stars
- 137 forks
- updated 2026-07-02
- primary language: Go
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 53/100 |
| stars | 76/100 |
| topics | 100/100 |
| outlook | 69/100 |
| quality | 71/100 |
| recency | 40/100 |
| adoption | 70/100 |
| production | 61/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/bruin-data/ingestr) · [← Back to Data](./README.md)</sub>
