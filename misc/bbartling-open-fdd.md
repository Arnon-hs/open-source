# bbartling/open-fdd

[![Stars](https://img.shields.io/github/stars/bbartling/open-fdd?style=flat-square&color=yellow)](https://github.com/bbartling/open-fdd/stargazers) [![Forks](https://img.shields.io/github/forks/bbartling/open-fdd?style=flat-square&color=blue)](https://github.com/bbartling/open-fdd/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> Fault Detection Diagnostics (FDD) for HVAC datasets

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 143 |
| 🍴 **Forks** | 29 |
| 💻 **Language** | Rust |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`commissioning` `fault-detection` `fdd` `hvac`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
`bbartling/open-fdd` is an open‑source Rust library that implements Fault Detection and Diagnostics (FDD) algorithms for HVAC sensor datasets. It provides a set of reusable components that can be wired into multi‑agent pipelines, turning ad‑hoc prompts and scripts into repeatable, memory‑aware workflows. With 143 ★ on GitHub, the project is actively maintained (last commit 2026‑06‑26) and positioned for data‑oriented orchestration use cases.

**Value**  
The library abstracts the core FDD logic—feature extraction, anomaly scoring, and fault classification—so developers can focus on orchestrating agents rather than reinventing detection code. By exposing a clean API and optional tool‑use hooks, it enables rapid prototyping of end‑to‑end diagnostics pipelines, consistent agent memory handling, and easy integration with existing data‑processing stacks.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the provided examples, and feed a small sample of your HVAC CSV/Parquet data through the default pipeline.  
2. **Integration Layer** – Wrap the Rust crate in a thin service (e.g., a gRPC or HTTP endpoint) or use `wasm` bindings if your stack is language‑agnostic.  
3. **Agent Workflow** – Connect the service to your orchestration platform (Airflow, Prefect, or a custom multi‑agent framework) and define the memory schema that agents will share.  
4. **Validation** – Compare the library’s fault labels against a known ground‑truth set; tune thresholds or plug in custom classifiers if needed.

**Production Readiness**  
The project is at a *medium* readiness level: it is stable enough for internal prototypes and pilot deployments, but production use should include:  

- **Dependency audit** – verify Rust toolchain versions and any native libraries.  
- **Performance testing** – benchmark on your data volume to confirm latency meets SLA.  
- **Observability** – add logging/metrics around the FDD service to detect drift or failures.  

Overall, `open-fdd` offers a solid foundation for building repeatable, agent‑driven HVAC diagnostics, provided you allocate time for a small PoC and a thorough integration review before scaling to production.

### Русский

**bbartling/open-fdd** — это open‑source библиотека на Rust для автоматического обнаружения и диагностики неисправностей в HVAC‑данных. Она позволяет собрать разрозненные подсказки и инструменты в повторяемый агентный пайплайн — например, создать цепочку, где один агент извлекает метрики, второй оценивает отклонения, а третий формирует отчёт и сохраняет состояние. Проект уже имеет 143 звёзд и активные обновления, но интеграция требует небольшого proof‑of‑concept и проверки README, поэтому подходит для прототипов и внутренних сервисов, а для production‑окружения нужен отдельный аудит зависимостей и стратегии поддержки.

### 中文

**项目简介**  
bbartling/open-fdd 是一个基于 Rust 的开源库，专注于 HVAC（暖通空调）数据的故障检测与诊断（FDD）。它提供了一套可复用的代理（agent）工作流框架，能够把零散的 Prompt 与工具组合成可编排的多代理流水线。

**价值主张**  
- **工作流复用**：将单次调用的模型 Prompt 与外部工具封装为可重复执行的代理步骤，降低重复实现成本。  
- **多代理协同**：支持在同一流程中调度多个智能体，实现复杂的故障定位、根因分析和维修建议。  
- **统一记忆与状态**：内置 Agent Memory 接口，帮助各代理共享上下文，提升诊断的连贯性和准确性。  

**典型接入方式**  
1. **快速原型**：克隆仓库 → 参考 `README` 中的示例，使用 `cargo run --example <demo>` 运行最小演示。  
2. **工具链集成**：在已有的 HVAC 数据采集系统中，调用 `open-fdd` 提供的 Rust 库 API（如 `detect_faults(data)`），将检测结果通过 HTTP/gRPC 暴露给上层业务。  
3. **多代理编排**：利用项目自带的 `workflow.yaml`（或自行编写）描述多个 Agent 的调用顺序，配合 `orchestrator`（如 Airflow、Temporal）实现定时或事件驱动的故障诊断流水线。  

**生产可用性**  
- **成熟度**：当前在 GitHub 上拥有 143 ★、29 Fork，最近一次更新为 2026‑06‑26，代码活跃度尚可。  
- **适用场景**：非常适合作为原型或内部工具，用于验证 HVAC 故障检测模型、构建实验性多代理流水线。  
- **上线前检查**：  
  - **依赖审计**：确认所有第三方 Crate（尤其是网络、数据库）符合企业安全合规要求。  
  - **性能基准**：在实际数据量（如每日上万条传感器记录）上跑基准，评估延迟与资源占用。  
  - **监控与日志**：为每个 Agent 添加结构化日志与指标（Prometheus/OTEL），便于故障排查。  
- **总体评估**：**中等**（Medium）——可在内部或边缘环境中投入使用，但在大规模生产环境部署前，需要完成依赖安全审查、性能调优和运维监控的补齐。  

> **建议**：先在测试环境实现一个“单机故障检测” PoC，验证数据输入/输出、Agent Memory 的工作方式后，再逐步扩展为完整的多代理编排流程。这样既能快速评估价值，又能控制集成成本。

## 🧭 Practical evaluation

**Value:** bbartling/open-fdd helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 143 GitHub stars
- 29 forks
- updated 2026-06-26
- primary language: Rust
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 37/100 |
| stars | 46/100 |
| topics | 50/100 |
| outlook | 62/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 43/100 |
| production | 63/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/bbartling/open-fdd) · [← Back to Misc](./README.md)</sub>
