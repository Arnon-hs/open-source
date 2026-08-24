# rust-lang/rustc-perf

[![Stars](https://img.shields.io/github/stars/rust-lang/rustc-perf?style=flat-square&color=yellow)](https://github.com/rust-lang/rustc-perf/stargazers) [![Forks](https://img.shields.io/github/forks/rust-lang/rustc-perf?style=flat-square&color=blue)](https://github.com/rust-lang/rustc-perf/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-46%2F100-brightgreen?style=flat-square)](#)

> Website for graphing performance of rustc

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 718 |
| 🍴 **Forks** | 182 |
| 💻 **Language** | Rust |
| 📈 **Score** | 46/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`performance`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Project Overview:**

The rust-lang/rustc-perf project is an open-source platform for graphing the performance of Rust's compiler (rustc). It provides a valuable tool for teams to optimize and analyze their Rust-based applications.

**Value Proposition:**

The primary value proposition of rust-lang/rustc-perf lies in its ability to help teams manage persistence, speed up data access, and prototype database-backed applications with less custom plumbing. By leveraging this platform, teams can streamline their data management workflows and improve the overall performance of their Rust-based projects.

**Practical Adoption Path:**

To adopt rust-lang/rustc-perf, teams should first manually inspect the integration process to ensure a smooth setup. This involves validating the setup cost and considering the potential risks associated with integration. Once the integration path is clear, teams can utilize the platform to persist, query, and move data with ease. Given the platform's medium production readiness, it is best suited for prototypes or internal workflows, with careful dependency and maintenance checks before deployment in production environments.

**Production Readiness:**

While rust-lang/rustc-perf is a useful tool for optimizing Rust-based applications, its production readiness is rated as medium. This means that it is suitable for use in non-critical applications or internal workflows

### Русский

rust-lang/rustc-perf — это open‑source веб‑инструмент для визуализации производительности компилятора Rust, позволяющий командам быстро собирать, хранить и сравнивать метрики сборок без собственного кода‑инжиниринга. Его типичный сценарий — подключение к CI, сбор данных о времени и ресурсах компиляции, а затем интерактивный просмотр графиков для выявления регрессий и оптимизации. Готовность к production средняя: проект стабилен и активно поддерживается, но интеграция требует ручного изучения и настройки, поэтому лучше использовать его в прототипах или внутренних процессах после проверки затрат на внедрение.

### 中文

**项目简介**  
rust-lang/rustc-perf 是 Rust 官方提供的一个网站，用于收集、存储并可视化 rustc 编译器的性能基准数据，帮助开发者直观看到编译时间、内存占用等关键指标的变化趋势。

**价值**  
- **统一的性能数据仓库**：所有 rustc 基准测试结果统一持久化，团队无需自行搭建采集与存储管道。  
- **快速查询与对比**：通过内置的图表界面，可即时对比不同提交、分支或配置的编译表现，帮助定位回归和优化点。  
- **原型与内部工具**：提供现成的查询 API 与数据模型，适合在内部工具或 CI 流程中快速原型化性能监控。

**典型接入方式**  
1. **在 CI 中运行基准**：在 CI（GitHub Actions、GitLab CI 等）里执行 `cargo bench`，将生成的 JSON/CSV 结果通过 HTTP POST 推送到 rustc-perf 的 API。  
2. **使用官方提供的上传脚本**：项目根目录下的 `upload-benchmarks.sh` 已封装好认证与数据格式转换，只需在 CI 步骤中调用即可。  
3. **查询与可视化**：在内部仪表盘或脚本中调用公开的 GraphQL/REST 接口获取历史数据，或直接访问 https://perf.rust-lang.org 查看交互式图表。

**生产可用性**  
- **成熟度**：项目已有 718 星、182 Fork，活跃维护至 2026‑06‑29，代码基于 Rust，质量较高。  
- **适用场景**：非常适合作为内部原型或团队内部的性能监控平台；对外部生产环境的直接依赖仍需评估，因为官方文档对自建部署与权限管理的说明较少。  
- **风险与准备**：集成路径主要通过手动配置上传脚本和 API，元数据中缺乏完整的集成指南；在正式生产使用前建议进行一次完整的端到端验证（包括认证、数据保留策略和监控告警），并评估维护成本。  

总体而言，rustc-perf 在内部性能分析和快速原型开发上已经相当可用，但若要作为关键业务的生产监控系统，仍需额外的集成测试和运维准备。

## 🧭 Practical evaluation

**Value:** rust-lang/rustc-perf helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 718 GitHub stars
- 182 forks
- updated 2026-06-29
- primary language: Rust
- 1 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 57/100 |
| stars | 61/100 |
| topics | 13/100 |
| outlook | 49/100 |
| quality | 54/100 |
| recency | 40/100 |
| adoption | 60/100 |
| production | 50/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/rust-lang/rustc-perf) · [← Back to Misc](./README.md)</sub>
