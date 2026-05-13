# open-telemetry/opentelemetry-java-instrumentation

[![Stars](https://img.shields.io/github/stars/open-telemetry/opentelemetry-java-instrumentation?style=flat-square&color=yellow)](https://github.com/open-telemetry/opentelemetry-java-instrumentation/stargazers) [![Forks](https://img.shields.io/github/forks/open-telemetry/opentelemetry-java-instrumentation?style=flat-square&color=blue)](https://github.com/open-telemetry/opentelemetry-java-instrumentation/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> OpenTelemetry auto-instrumentation and instrumentation libraries for Java

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.5k |
| 🍴 **Forks** | 1.1k |
| 💻 **Language** | Java |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Observability

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
OpenTelemetry Java Instrumentation provides auto‑instrumentation agents and library modules that automatically generate traces, metrics, and logs from Java applications without code changes. It enables developers to gain visibility into production behavior, debug issues, and monitor service health across a wide range of Java runtimes and frameworks. The project is actively maintained (≈2.5 k stars, recent updates) but its integration metadata is sparse, so a careful validation step is recommended before full‑scale adoption.  

**Value**  
- **Zero‑code observability** – the Java agent can be attached at startup, instantly emitting OpenTelemetry‑compatible telemetry for HTTP servers, database clients, messaging systems, and more.  
- **Unified data model** – traces, metrics, and logs are produced in a single, vendor‑agnostic format, simplifying downstream analysis and reducing lock‑in.  
- **Broad ecosystem support** – works with popular frameworks (Spring, Micronaut, Quarkus, etc.) and can be extended with custom instrumentation libraries.  

**Practical Adoption Path**  

| Step | Action | Why |
|------|--------|-----|
| 1️⃣ Evaluate | Run the agent on a staging copy of the service (`-javaagent:/path/to/opentelemetry-javaagent.jar`). Capture a few minutes of traffic and inspect the exported spans/metrics. | Confirms compatibility with your runtime (JDK version, container base image) and reveals any missing signals. |
| 2️⃣ Configure Exporter | Add an exporter configuration (OTLP, Jaeger, Prometheus, etc.) via environment variables or a `otel-config.yaml`. | Ensures data lands in your existing observability stack. |
| 3️⃣ Tune Instrumentation | Enable/disable specific instrumentations via the `OTEL_JAVAAGENT_ENABLED_INSTRUMENTATIONS` property; add custom instrumentation libraries if needed. | Reduces overhead and avoids noisy data. |
| 4️⃣ CI/CD Integration | Add the agent jar to your build pipeline (e.g., Dockerfile `COPY` + `ENTRYPOINT ["java","-javaagent:/otel/agent.jar",…]`). | Guarantees the same observability surface in every deployment. |
| 5️⃣ Validate & Iterate | Compare telemetry before and after, verify key business‑critical traces appear, and monitor CPU/memory impact. | Provides confidence before promoting to production. |

**Production Readiness**  
- **Maturity:** Medium. The project is widely used (2.5 k ★) and receives regular updates, but the automatically discovered metadata is limited, making the integration path less straightforward than fully documented SDKs.  
- **Suitability:** Good for prototypes, internal services, or as a first‑step observability layer. For mission‑critical production workloads, perform a dedicated pilot to assess performance impact, verify that all required signals are captured, and establish a maintenance plan for agent upgrades.  
- **Risks:** Sparse integration signals may require manual verification and possibly custom instrumentation; the operational cost of managing agent versions and exporter configurations should be accounted for.  

In short, OpenTelemetry Java Instrumentation can dramatically accelerate observability for Java services, provided you allocate time for a pilot validation and establish clear processes for configuration, monitoring, and version management before scaling to production.

### Русский

OpenTelemetry Java Instrumentation — это набор автоинструментов и библиотек, позволяющих быстро добавить наблюдаемость в Java‑приложения: сбор метрик, трассировок и логов для мониторинга, отладки и оценки здоровья сервисов. Типичный сценарий — включить автоматическую инструментировку в существующий сервис, собрать данные в выбранную бек‑энд‑систему и использовать их для диагностики продакшн‑поведения. Проект имеет средний уровень готовности к production: подходит для прототипов и внутренних сервисов, но требует предварительной проверки интеграции и оценки затрат на настройку, так как сигналы в метаданных ограничены.

### 中文

**项目简介**  
OpenTelemetry Java Instrumentation（`open-telemetry/opentelemetry-java-instrumentation`）提供了面向 Java 应用的自动化埋点和手动埋点库，帮助开发者在不改动业务代码的前提下收集分布式追踪、指标和日志，实现对生产环境行为的可观测性。

**价值**  
- **快速可观测**：通过自动注入探针，即可捕获 HTTP、数据库、消息队列等常见库的调用链，省去手动埋点的繁琐。  
- **统一数据模型**：遵循 OpenTelemetry 标准，采集的数据可直接送往 Jaeger、Prometheus、Grafana Cloud、AWS X‑Ray 等后端，统一监控、调试和故障排查流程。  
- **降低调试成本**：在生产环境中实时查看请求的完整路径、延迟分布和错误率，快速定位性能瓶颈和异常根因。

**典型接入方式**  
1. **自动化（Auto‑Instrumentation）**  
   - 下载对应平台的 `opentelemetry-javaagent.jar`（或使用 Maven/Gradle 插件）。  
   - 在启动 JVM 时添加 `-javaagent:/path/to/opentelemetry-javaagent.jar` 参数。  
   - 通过环境变量或系统属性（如 `OTEL_EXPORTER_OTLP_ENDPOINT`、`OTEL_TRACES_SAMPLER`）配置导出端点、采样率、资源属性等。  

2. **手动库（Instrumentation Libraries）**  
   - 在 Maven/Gradle 中加入 `io.opentelemetry:opentelemetry-api`、`opentelemetry-sdk` 以及对应的 **instrumentation‑library**（如 `opentelemetry-instrumentation-spring-boot`）。  
   - 在代码中创建 `OpenTelemetrySdk`，并使用 `Tracer`、`Meter`、`Logger` 手动生成自定义 Span、Metric 和日志。  

**生产可用性**  
- **成熟度**：社区活跃（>2500 Stars），每月都有更新，已在多个大型云原生项目中验证。  
- **适用场景**：非常适合原型、内部工具以及逐步迁移到全链路可观测的生产系统。  
- **风险与注意事项**  
  - 自动探针的覆盖范围受限于已实现的库列表，部分自研或较冷门的框架可能需要手动埋点。  
  - 引入 agent 会增加 JVM 启动时间和轻微的运行时开销，建议在预发布环境进行性能基准测试。  
  - 依赖版本需与业务代码的 JDK 与框架保持兼容，升级前务必检查兼容性矩阵。  

总体而言，`opentelemetry-java-instrumentation` 在 **中等** 生产就绪度上表现良好，适合作为观察性能力的快速落地方案，只要在正式上线前完成一次完整的集成验证和性能评估即可。

## 🧭 Practical evaluation

**Value:** open-telemetry/opentelemetry-java-instrumentation helps make production behavior easier to inspect and debug.

**Best use cases**

- monitor systems
- debug production behavior
- track service health

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 2531 GitHub stars
- 1092 forks
- updated 2026-05-13
- primary language: Java

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 76/100 |
| stars | 72/100 |
| topics | 0/100 |
| outlook | 72/100 |
| quality | 73/100 |
| recency | 100/100 |
| adoption | 73/100 |
| production | 72/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/open-telemetry/opentelemetry-java-instrumentation) · [← Back to Observability](./README.md)</sub>
