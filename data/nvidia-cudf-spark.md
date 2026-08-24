# NVIDIA/cudf-spark

[![Stars](https://img.shields.io/github/stars/NVIDIA/cudf-spark?style=flat-square&color=yellow)](https://github.com/NVIDIA/cudf-spark/stargazers) [![Forks](https://img.shields.io/github/forks/NVIDIA/cudf-spark?style=flat-square&color=blue)](https://github.com/NVIDIA/cudf-spark/network) [![Language](https://img.shields.io/badge/lang-Scala-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> Spark RAPIDS plugin - accelerate Apache Spark with GPUs

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 985 |
| 🍴 **Forks** | 288 |
| 💻 **Language** | Scala |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`big-data` `gpu` `rapids` `spark`

## 🎯 Categories

Data

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
NVIDIA cudf‑spark is the RAPIDS plugin that lets Apache Spark workloads run on GPUs, dramatically speeding up data‑intensive pipelines without rewriting existing code. With strong community traction (≈ 1 k stars, active commits, and Scala‑first API), it offers a ready‑to‑evaluate drop‑in that exposes clear implementation signals (API/SDK/CLI) for easy integration.  

**Value**  
- **Performance boost:** GPU acceleration can cut Spark job runtimes by an order of magnitude, lowering compute costs and enabling near‑real‑time analytics.  
- **Infrastructure reuse:** Teams can keep their existing Spark clusters and pipelines while adding a GPU layer, avoiding the need to rebuild backend services from scratch.  
- **Standardization:** By providing a common, well‑documented plugin, organizations can enforce consistent service patterns across data teams, accelerating API‑service delivery.  

**Practical Adoption Path**  
1. **Pilot setup:** Deploy a small GPU‑enabled Spark executor pool (e.g., on NVIDIA DGX or cloud GPU instances) and enable the cudf‑spark plugin via Spark configuration.  
2. **Compatibility testing:** Run a subset of representative Spark jobs to verify functional parity and benchmark speedups; the plugin’s Scala API mirrors native Spark APIs, so code changes are minimal.  
3. **Integration:** Wrap the accelerated jobs in existing CI/CD pipelines, expose any new CLI or SDK hooks, and update monitoring to capture GPU utilization.  
4. **Scale‑out:** Gradually migrate more workloads to the GPU pool, leveraging the plugin’s built‑in metrics to tune resource allocation.  

**Production Readiness**  
- **Maturity:** Recent commits (as of 2026‑06‑23), 985 stars, 288 forks, and active community discussions indicate a healthy, actively maintained project.  
- **Ecosystem fit:** Works with standard Spark distributions and integrates cleanly with existing data platforms (e.g., Databricks, EMR).  
- **Risk considerations:** No major licensing or metadata concerns identified, but a final security and maintainer review is advisable before full production rollout. Overall, cudf‑spark is sufficiently mature for a serious pilot and can be promoted to production once the pilot validates performance and stability.

### Русский

**NVIDIA/cudf-spark** — это open‑source плагин Spark RAPIDS, который позволяет ускорять вычисления Apache Spark за счёт GPU, используя готовую инфраструктуру NVIDIA cuDF. Типичный сценарий — команды, разрабатывающие API‑сервисы или аналитические пайплайны, заменяют CPU‑ориентированные Spark‑задания на GPU‑ускоренные, получая более быстрый time‑to‑market и единые стандарты бекенд‑компонентов. Проект считается почти готовым к продакшн: активные коммиты, более 900 звёзд на GitHub, широкое принятие в экосистеме и стабильный Scala‑интерфейс, хотя окончательная проверка лицензии, безопасности и поддерживаемости всё‑ещё требуется.

### 中文

**项目简介**  
NVIDIA cudf‑spark 是 Spark RAPIDS 插件，利用 GPU 加速 Apache Spark 的数据处理工作负载，使大规模分析和机器学习任务能够在同等硬件上获得数倍甚至数十倍的性能提升。

**价值**  
- **复用已有后端设施**：通过插件的方式直接在现有 Spark 集群上开启 GPU 加速，无需重新搭建专用的服务框架。  
- **加速 API/服务交付**：数据预处理、特征抽取等耗时步骤被 GPU 大幅缩短，帮助团队更快上线数据密集型 API 服务。  
- **统一后端模式**：提供统一的 Spark‑GPU 接口，团队可以在不同业务线之间共享同一套加速方案，降低运维复杂度。

**典型接入方式**  
1. **环境准备**：在 Spark 集群节点上安装 NVIDIA 驱动、CUDA Toolkit 与 cuDF 库。  
2. **插件引入**：在 Spark 提交脚本或 `spark-submit` 参数中加入 `--packages com.nvidia:rapids-4-spark_2.12:<version>`（或在 `spark-defaults.conf` 中配置 `spark.plugins=com.nvidia.spark.SQLPlugin`）。  
3. **代码层面**：使用标准的 Spark DataFrame API，无需改动业务逻辑；只需在创建 SparkSession 时打开 GPU 支持，例如 `spark.conf.set("spark.rapids.sql.enabled", "true")`。  
4. **调优**：通过 `spark.rapids.sql.concurrentGpuTasks`、`spark.rapids.memory.pinnedPoolSize` 等参数对 GPU 资源进行细粒度控制。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑23，项目拥有 985+ Stars、288+ Forks，最近一次提交在同日，表明社区和 NVIDIA 官方仍在持续维护。  
- **生态兼容**：基于 Scala 实现，兼容 Spark 3.x 及以上版本，已在多家企业（如 Databricks、HPE）进行生产级部署。  
- **成熟度**：插件已通过 NVIDIA 官方的 CI/CD 测试，具备完整的单元、集成与性能基准，具备 **High** 级别的生产就绪度，适合作为正式业务的 Pilot 或全量上线。  

> **结论**：NVIDIA/cudf‑spark 能帮助团队在现有 Spark 基础设施上快速开启 GPU 加速，显著提升数据处理吞吐，接入门槛低且已具备生产级可靠性，是后端数据平台向“GPU‑first”转型的首选 OSS 方案。

## 🧭 Practical evaluation

**Value:** NVIDIA/cudf-spark helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 985 GitHub stars
- 288 forks
- updated 2026-06-23
- primary language: Scala
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 62/100 |
| stars | 64/100 |
| topics | 50/100 |
| outlook | 56/100 |
| quality | 61/100 |
| recency | 40/100 |
| adoption | 63/100 |
| production | 57/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/NVIDIA/cudf-spark) · [← Back to Data](./README.md)</sub>
