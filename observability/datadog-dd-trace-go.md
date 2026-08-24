# DataDog/dd-trace-go

[![Stars](https://img.shields.io/github/stars/DataDog/dd-trace-go?style=flat-square&color=yellow)](https://github.com/DataDog/dd-trace-go/stargazers) [![Forks](https://img.shields.io/github/forks/DataDog/dd-trace-go?style=flat-square&color=blue)](https://github.com/DataDog/dd-trace-go/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> Datadog Go Library including APM tracing, profiling, and security monitoring.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 847 |
| 🍴 **Forks** | 535 |
| 💻 **Language** | Go |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`apm` `appsec` `datadog` `distributed-tracing` `monitoring` `opentelemetry` `opentracing` `otel` `performance` `profiling` `tracing`

## 🎯 Categories

Observability · Security

## 📝 Summary

### English

**Project Summary:**

DataDog/dd-trace-go is an open-source Go library that enables APM (Application Performance Monitoring) tracing, profiling, and security monitoring. This project helps organizations convert raw data into actionable insights, allowing for better analytics pipelines, dataset processing, and reporting workflows. With its strong adoption and recent activity, it's a suitable candidate for a serious pilot in production environments.

**Value Proposition:**

The primary value of DataDog/dd-trace-go lies in its ability to transform raw data into searchable, analyzable, or automated pipelines. This enables organizations to:

* Organize analytics pipelines more efficiently
* Process datasets with greater ease
* Improve reporting workflows for better decision-making

**Practical Adoption Path:**

To adopt DataDog/dd-trace-go, follow these steps:

1. **Evaluate and Review:** Assess the project's integration feasibility by starting with a small proof of concept and reviewing the README documentation.
2. **Integration Pilot:** Begin with a small-scale integration to test the library's functionality and identify potential issues.
3. **Production Deployment:** Once successful, deploy the library in a production environment, monitoring its performance and making adjustments as needed.

**Production Readiness:**

DataDog/dd-trace-go is considered production-ready due to its:

* Recent

### Русский

Резюме проекта DataDog/dd-trace-go:

Проект DataDog/dd-trace-go представляет собой открытое программное обеспечение для мониторинга данных, профилирования и обеспечения безопасности в приложениях на языке Go. Он позволяет конвертировать необработанные данные в поисковые, анализируемые или автоматизированные потоки данных. Проект готов к внедрению в производственную среду, имея сильное присутствие в экосистеме и регулярную поддержку, что делает его подходящей опцией для серьезных пилотов.

### 中文

**项目简介**  
DataDog/dd-trace-go 是 Datadog 官方提供的 Go 语言 SDK，集合了 APM（分布式追踪）、性能分析（Profiling）以及安全监控等功能，帮助开发者在 Go 应用中快速实现可观测性与安全防护。

**价值**  
- **统一可观测性**：通过自动采集调用链、执行时长、错误率等指标，直接上报到 Datadog 平台，实现端到端的性能追踪和瓶颈定位。  
- **安全监控**：内置安全事件捕获（如异常请求、敏感信息泄漏），配合 Datadog Security Monitoring 可实现实时威胁检测。  
- **降低运维成本**：无需自行搭建追踪、分析基础设施，借助 Datadog 完整的仪表盘和告警体系即可快速得到可操作的洞察。

**典型接入方式**  
1. **依赖引入**  
   ```bash
   go get gopkg.in/DataDog/dd-trace-go.v1/ddtrace
   ```
2. **初始化 Tracer**（通常在 `main` 函数或服务启动入口）  
   ```go
   import (
       "gopkg.in/DataDog/dd-trace-go.v1/ddtrace/tracer"
   )

   func main() {
       tracer.Start(
           tracer.WithServiceName("my-go-service"),
           tracer.WithEnv("prod"),
           tracer.WithVersion("1.2.3"),
       )
       defer tracer.Stop()
       // 启动业务逻辑...
   }
   ```
3. **自动化 Instrumentation**  
   - 对 HTTP 服务器使用 `nethttp` 包包装：`router := chi.NewRouter(); router.Use(ddhttp.WrapHandler)`  
   - 对数据库（MySQL、PostgreSQL、Redis 等）使用对应的 `sqltrace`、`redistrace` 包进行包装。  
4. **自定义 Span**（如需细粒度监控）  
   ```go
   span, ctx := tracer.StartSpanFromContext(context.Background(), "my.operation")
   // 业务代码...
   span.Finish()
   ```
5. **验证**：运行 `go test` 或启动服务后，在 Datadog UI 中确认 Trace、Metrics、Security Events 已成功上报。

**生产可用性**  
- **活跃维护**：截至 2026‑07‑10 最近一次提交，拥有 847 ⭐、535 🍴，社区活跃，Datadog 官方持续发布新特性与安全补丁。  
- **成熟度**：已在大量生产环境中使用（如微服务、无服务器函数），支持 Go 1.20+，兼容主流框架（Gin、Echo、Chi、gRPC 等）。  
- **风险**：许可证为 Apache‑2.0，符合企业合规；仍需在正式投产前完成内部安全审计和依赖漏洞扫描。  
- **推荐策略**：先在预生产或单节点服务做 PoC，验证 Trace、Profiling 与 Security 事件是否满足业务需求，再逐步推广到全链路。  

综上，DataDog/dd-trace-go 在可观测性与安全监控方面提供了“一站式”解决方案，集成成本低，且已具备在生产环境中大规模使用的成熟度。

## 🧭 Practical evaluation

**Value:** DataDog/dd-trace-go helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 847 GitHub stars
- 535 forks
- updated 2026-07-10
- primary language: Go
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 68/100 |
| stars | 62/100 |
| topics | 100/100 |
| outlook | 62/100 |
| quality | 69/100 |
| recency | 40/100 |
| adoption | 64/100 |
| production | 58/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-10 · [View on GitHub](https://github.com/DataDog/dd-trace-go) · [← Back to Observability](./README.md)</sub>
