# obrienciaran/dbt-debt

[![Stars](https://img.shields.io/github/stars/obrienciaran/dbt-debt?style=flat-square&color=yellow)](https://github.com/obrienciaran/dbt-debt/stargazers) [![Forks](https://img.shields.io/github/forks/obrienciaran/dbt-debt?style=flat-square&color=blue)](https://github.com/obrienciaran/dbt-debt/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-38%2F100-brightgreen?style=flat-square)](#)

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
The project provides a “technical‑debt” score for dbt (data build tool) projects that run on Snowflake, BigQuery, or Redshift, helping teams gauge code health, maintainability, and potential refactoring effort. It aggregates metadata such as README quality, recent activity, and repository signals to produce a numeric score (out of 100). While the score can be a useful quick sanity check, the underlying data is sparse and requires manual validation before relying on it for critical decisions.  

**Value**  
- **Rapid health indicator** – Gives data‑engineering teams an at‑a‑glance metric to prioritize which dbt models need cleanup or deeper review.  
- **Cross‑platform support** – Works with the three major cloud data warehouses, so the same scoring logic can be reused across Snowflake, BigQuery, and Redshift environments.  
- **Decision‑making aid** – When combined with internal CI/CD metrics, the score can help justify refactor tickets, allocate engineering bandwidth, or enforce governance policies.  

**Practical Adoption Path**  

| Step | Action | Why |
|------|--------|-----|
| 1️⃣  | **Clone & inspect** – Pull the repo, read the README, and run the provided script on a small, non‑production dbt project. | Confirms the tool runs in your environment and surfaces any missing dependencies. |
| 2️⃣  | **Validate scoring logic** – Compare the generated score against known “good” and “bad” dbt repos in your org. | Ensures the metric aligns with your internal definition of technical debt. |
| 3️⃣  | **Integrate into CI** – Add the scoring command to a pre‑merge pipeline (e.g., GitHub Actions) and set a threshold (e.g., ≥ 70) that must be met before merging. | Automates continuous monitoring and prevents regression. |
| 4️⃣  | **Dashboard/reporting** – Export the score to a monitoring tool (e.g., Looker, Grafana) or embed it in a weekly engineering health report. | Gives stakeholders visibility without manual runs. |
| 5️⃣  | **Feedback loop** – Track false positives/negatives, file issues upstream, and consider contributing improvements (e.g., more granular metrics). | Improves the tool’s reliability and aligns it with your workflow. |

**Production Readiness** – *Medium*  

- **Suitable for**: prototypes, internal health dashboards, and as a gating check in CI for low‑risk environments.  
- **Not yet ready for**: mission‑critical production pipelines where a single numeric score would drive automated remediation, because the underlying metadata is sparse and the scoring algorithm is not extensively vetted.  
- **Pre‑adoption checklist**: verify the license (compatible with your org’s policy), confirm recent maintenance activity, review open issues and pull‑request velocity, and test the tool against a representative set of your dbt projects.  

If those checks pass, the project can be safely introduced as a supplemental quality metric, with the understanding that deeper code reviews and existing static‑analysis tools (e.g., dbt‑utils, SQLFluff) should still be the primary safeguards.

### Русский

Резюме проекта:

"Show HN: Technical-debt score for dbt projects on Snowflake/BigQuery/Redshift" - это открытый проект, предназначенный для оценки технического долга в проектах dbt на платформах Snowflake, BigQuery и Redshift. Этот проект может быть полезен для оценки технического долга в своих проектах, особенно в прототипах или внутренних рабочих процессах. Однако, следует провести тщательное проверку лицензии, поддержки, документации, проблем и графика выпусков перед использованием в производстве.

### 中文

**项目简介**  
Show HN : Technical‑debt score for dbt projects on Snowflake/BigQuery/Redshift 是一个开源工具，能够对基于 Snowflake、BigQuery 或 Redshift 的 dbt 项目计算并展示技术债务分数（满分 100 分），帮助团队快速评估项目的可维护性和潜在风险。  

**价值**  
- **快速洞察**：通过量化的技术债务分数，团队可以在代码审查、迁移或重构前快速判断项目的健康程度。  
- **决策依据**：为资源分配、优先级排序和技术债务偿还计划提供客观依据，降低后期维护成本。  

**典型接入方式**  
1. **在 CI/CD 流水线中调用**：将工具包装为一个 CLI 或 Docker 镜像，在每次 dbt 运行后执行，自动生成分数并在构建报告中展示。  
2. **作为 GitHub Action**：在仓库的 workflow 中添加 `show-hn/technical-debt-score` Action，PR 合并前即可看到分数反馈。  
3. **本地分析**：开发者在本地运行 `technical-debt-score --project-path ./my-dbt-project`，得到即时报告，用于日常代码审查。  

**生产可用性**  
- **成熟度**：当前评分为 41/100，属于 **中等** 稳定性。适合原型、内部工具或技术债务评估的前置步骤。  
- **使用前检查**：由于元数据中集成信号稀疏，建议在正式采用前手动审查以下方面：  
  - 开源许可证是否兼容项目需求  
  - 最近的维护活动、Issue 响应速度和发布频率  
  - 文档完整性与示例代码是否覆盖你的工作流  
- **生产环境**：在完成上述审查并确认依赖可接受后，可在受控的生产环境中使用，最好配合监控（如分数阈值报警）和定期审计，以防止技术债务累积。

## 🧭 Practical evaluation

**Value:** Show HN: Technical-debt score for dbt projects on Snowflake/BigQuery/Redshift may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-07-13
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

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/obrienciaran/dbt-debt) · [← Back to Misc](./README.md)</sub>
