# open-telemetry/opentelemetry-rust

[![Stars](https://img.shields.io/github/stars/open-telemetry/opentelemetry-rust?style=flat-square&color=yellow)](https://github.com/open-telemetry/opentelemetry-rust/stargazers) [![Forks](https://img.shields.io/github/forks/open-telemetry/opentelemetry-rust?style=flat-square&color=blue)](https://github.com/open-telemetry/opentelemetry-rust/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> The Rust OpenTelemetry implementation

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.6k |
| 🍴 **Forks** | 674 |
| 💻 **Language** | Rust |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`jaeger` `logging` `metrics` `opentelemetry` `prometheus` `tracing` `zipkin`

## 🎯 Categories

Observability

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
OpenTelemetry‑Rust is the official Rust implementation of the OpenTelemetry observability framework, providing APIs and SDKs for distributed tracing, metrics, and logs. With a thriving community (2.6 k ★, 674 forks) and recent activity, it’s a solid choice for instrumenting Rust services to gain insight into production behavior. A small proof‑of‑concept based on the README can quickly validate the integration before scaling it across the codebase.  

**Value**  
By adding OpenTelemetry‑Rust you get a vendor‑agnostic way to collect traces, metrics, and logs from your Rust applications, making it far easier to monitor system health, diagnose latency issues, and understand request flows in production. The unified data model lets you export to any compatible backend (Jaeger, Prometheus, Grafana, etc.), eliminating lock‑in and simplifying root‑cause analysis across microservices.  

**Practical Adoption Path**  

1. **Proof of concept** – Follow the README to add the `opentelemetry` crate to a small service, enable a simple tracer, and export to a local collector (e.g., OTEL Collector or Jaeger).  
2. **Instrumentation** – Use the provided macros (`#[instrument]`) and API calls to add spans around key business logic and async boundaries.  
3. **Export configuration** – Choose an exporter that matches your observability stack (OTLP over HTTP/gRPC, Jaeger, Prometheus). Configure via environment variables or a minimal YAML for the collector.  
4. **Gradual rollout** – Expand instrumentation module‑by‑module, monitoring overhead and data quality.  
5. **CI/CD validation** – Add a test that ensures the tracer initializes without panics and that required spans are emitted.  

**Production Readiness**  
The project scores high on production readiness: it is actively maintained (last commit 2026‑06‑25), widely adopted, and part of the CNCF‑sanctioned OpenTelemetry ecosystem. The extensive community support, multiple exporters, and clear documentation make it suitable for a serious pilot, though the exact integration steps (e.g., collector deployment, exporter selection) need to be validated early to avoid hidden setup costs.

### Русский

open‑telemetry/opentelemetry‑rust — это зрелая реализация OpenTelemetry для Rust, позволяющая собирать трассировки, метрики и логи и тем самым упрощать мониторинг, отладку и оценку состояния сервисов в продакшене. Для начала рекомендуется реализовать небольшой proof‑of‑concept по инструкции в README, после чего расширить покрытие на все критические компоненты. Проект считается готовым к production: активная разработка, более 2600 звёзд, широкое принятие в экосистеме и стабильные релизы.

### 中文

**项目简介**  
OpenTelemetry‑Rust 是 OpenTelemetry 社区在 Rust 语言上的官方实现，提供统一的 API 与 SDK，用于在 Rust 应用中生成、收集和导出分布式追踪、度量和日志数据。

**价值**  
- **可观测性统一化**：一次接入即可同时支持 tracing、metrics 与 logs，避免在不同库之间切换。  
- **调试与故障定位**：通过完整的调用链追踪，帮助快速定位生产环境的性能瓶颈和异常。  
- **生态兼容**：兼容 OpenTelemetry 生态的后端（Jaeger、Prometheus、OTLP、Zipkin 等），便于与现有监控平台无缝集成。

**典型接入方式**  
1. **添加依赖**：在 `Cargo.toml` 中加入 `opentelemetry = { version = "x.y", features = ["rt-tokio"] }`（或 `rt-async-std`）以及对应的 exporter（如 `opentelemetry-otlp`、`opentelemetry-jaeger`）。  
2. **初始化 Tracer/Meter**：在程序入口处创建全局 Tracer（或 Meter），配置采样策略和导出端点。  
   ```rust
   use opentelemetry::sdk::trace::{TracerProvider, Sampler};
   use opentelemetry_otlp::WithExportConfig;

   let tracer = opentelemetry_otlp::new_pipeline()
       .with_endpoint("http://localhost:4317")
       .with_trace_config(opentelemetry::sdk::trace::config().with_sampler(Sampler::AlwaysOn))
       .install_batch(opentelemetry::runtime::Tokio)?;
   ```
3. **在业务代码中创建 Span**：使用 `tracing` 或 OpenTelemetry 原生 API 包装关键函数/请求。  
   ```rust
   let _span = tracer.start("handle_request");
   // 业务逻辑…
   ```
4. **导出与关闭**：在程序结束时调用 `opentelemetry::global::shutdown_tracer_provider();` 确保所有数据被发送。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑25，项目拥有 2630+ 星、674+ Fork，最近一次提交仅数天前，表明社区维护良好。  
- **生态成熟**：已被多家大型企业在生产环境中使用，支持完整的 OTLP、Jaeger、Prometheus 等后端。  
- **风险点**：项目文档侧重 API，完整的端到端部署指南相对分散，建议先在小型 PoC（参考 README）验证集成成本，再推广到全链路。  
- **结论**：在 Rust 生态中，OpenTelemetry‑Rust 已具备高可用性，适合作为生产级可观测性基础设施的核心组件。

## 🧭 Practical evaluation

**Value:** open-telemetry/opentelemetry-rust helps make production behavior easier to inspect and debug.

**Best use cases**

- monitor systems
- debug production behavior
- track service health

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2630 GitHub stars
- 674 forks
- updated 2026-06-25
- primary language: Rust
- 7 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 71/100 |
| stars | 73/100 |
| topics | 88/100 |
| outlook | 59/100 |
| quality | 71/100 |
| recency | 40/100 |
| adoption | 72/100 |
| production | 56/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/open-telemetry/opentelemetry-rust) · [← Back to Observability](./README.md)</sub>
