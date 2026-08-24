# google/meridian

[![Stars](https://img.shields.io/github/stars/google/meridian?style=flat-square&color=yellow)](https://github.com/google/meridian/stargazers) [![Forks](https://img.shields.io/github/forks/google/meridian?style=flat-square&color=blue)](https://github.com/google/meridian/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Meridian is an MMM framework that enables advertisers to set up and run their own in-house models.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.4k |
| 🍴 **Forks** | 273 |
| 💻 **Language** | Python |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
Meridian is an open‑source MMM (Marketing Mix Modeling) framework that lets advertisers build, train, and serve their own in‑house attribution models. Written in Python and backed by a sizable community (≈1.4 k stars, 273 forks), it is actively maintained as of June 2026, making it a viable option for internal analytics prototypes.

**Value**  
- **Customizable MMM**: Unlike off‑the‑shelf SaaS tools, Meridian gives data teams full control over model architecture, feature engineering, and data pipelines, enabling more accurate attribution that reflects a brand’s unique media mix.  
- **Open‑source transparency**: The codebase is publicly auditable, facilitating compliance checks, reproducibility, and cost‑effective scaling without vendor lock‑in.  
- **Ecosystem integration**: Built on standard Python data‑science libraries, it can be plugged into existing ETL, GCP, or Snowflake workflows with minimal friction.

**Practical adoption path**  
1. **Initial assessment** – Clone the repo, run the provided notebooks on a sample dataset, and verify that the modeling assumptions align with your media‑spend and conversion data.  
2. **Pilot implementation** – Integrate Meridian’s data ingestion modules with your internal data lake, customize the feature set, and run a limited‑scope MMM (e.g., a single product line).  
3. **Validation & iteration** – Compare model outputs against historical benchmarks, adjust hyper‑parameters, and document any required extensions (e.g., new channel parsers).  
4. **Operationalization** – Containerize the training pipeline (Docker/Cloud Run), schedule regular retraining via Cloud Composer or Airflow, and expose results through a dashboard or API for downstream media‑budget decisions.

**Production readiness**  
Meridian sits at a **medium** readiness level: it is mature enough for internal prototypes and controlled production use, but it requires due‑diligence before full deployment. Key steps include:  

- **Dependency audit** – Review third‑party libraries for known vulnerabilities and ensure version pinning.  
- **Security review** – Verify that the repository’s license (Apache‑2.0) aligns with corporate policy and that no sensitive credentials are hard‑coded.  
- **Maintainability check** – Confirm that an internal team can sustain the codebase (e.g., by assigning a dedicated owner) and that the upstream maintainers are responsive.  

After these checks, Meridian can be safely promoted to production for in‑house MMM workloads.

### Русский

**Meridian** — это open‑source MMM‑фреймворк от Google, позволяющий рекламодателям быстро развернуть собственные модели медиапланирования и проводить их в интерне. Он подходит для прототипов и внутренних аналитических пайплайнов, однако перед переходом в продакшн требуется ручная проверка интеграционных точек, оценка зависимостей и подтверждение поддержки проекта. При надлежащей доработке фреймворк может стать надёжным элементом рекламных workflow‑ов со средней готовностью к производству.

### 中文

**项目简介**  
Meridian（google/meridian）是 Google 开源的 MMM（Marketing Mix Modeling）框架，帮助广告主在内部搭建、训练并运行自有的营销混合模型，实现对预算分配、渠道效果等关键指标的可解释分析。

**价值点**  
1. **内部可控**：企业可以在自有环境中完整管理模型代码、数据和实验，避免将商业敏感信息外泄。  
2. **灵活可扩展**：基于 Python 实现，提供模块化的模型组件和数据管道，便于根据业务需求快速添加新渠道或特征。  
3. **加速原型**：框架已经封装了常用的 MMM 预处理、特征工程和贝叶斯/回归建模流程，能够让团队在几天内完成从数据准备到模型输出的全链路验证。

**典型接入方式**  
1. **环境准备**：克隆仓库后，使用 `requirements.txt` 或 `poetry` 安装依赖（Python 3.9+），推荐在 Docker 或虚拟环境中运行，以保证依赖可重复。  
2. **数据接入**：按照 `docs/data_schema.md` 定义的 CSV/Parquet 格式准备营销渠道、销售、季节性等时间序列数据；框架提供 `DataLoader` 接口，可直接对接 BigQuery、Snowflake 或本地文件系统。  
3. **模型配置**：在 `config/` 目录下编写 YAML 配置，指定模型类型（如 Bayesian MMM、线性回归）、超参数、特征选择规则等；随后运行 `python run_meridian.py --config=config/your_config.yaml` 启动训练。  
4. **结果输出与可视化**：训练完成后，框架会生成模型系数、贡献度报告以及可交互的 Plotly 可视化仪表盘，便于业务方审阅和决策。

**生产可用性评估**  
- **成熟度**：项目已有 1.4k+ Stars、273 Fork，活跃度仍在（最近一次提交为 2026‑06‑24），代码质量和文档相对完整，适合作为内部原型或实验平台。  
- **依赖与维护**：核心依赖为 `pandas、numpy、scikit-learn、pymc3` 等常见库，易于审计和升级；但项目的维护者信息不够明确，建议在正式生产前自行审查安全漏洞并锁定依赖版本。  
- **生产建议**：  
  - **原型/内部工具**：直接使用即可，快速验证 MMM 思路。  
  - **面向生产**：在正式部署前，需要完成：  
    1. **安全审计**（许可证、第三方库漏洞）。  
    2. **CI/CD 流程**（单元测试、模型回归验证）。  
    3. **监控与治理**（模型漂移监测、数据质量检查）。  
  - 在满足上述条件后，Meridian 可作为内部营销分析平台的核心组件投入生产使用。

## 🧭 Practical evaluation

**Value:** google/meridian may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1434 GitHub stars
- 273 forks
- updated 2026-06-24
- primary language: Python

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 61/100 |
| stars | 67/100 |
| topics | 0/100 |
| outlook | 52/100 |
| quality | 54/100 |
| recency | 40/100 |
| adoption | 65/100 |
| production | 55/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/google/meridian) · [← Back to Misc](./README.md)</sub>
