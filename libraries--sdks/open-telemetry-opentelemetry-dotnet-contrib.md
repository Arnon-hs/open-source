# open-telemetry/opentelemetry-dotnet-contrib

[![Stars](https://img.shields.io/github/stars/open-telemetry/opentelemetry-dotnet-contrib?style=flat-square&color=yellow)](https://github.com/open-telemetry/opentelemetry-dotnet-contrib/stargazers) [![Forks](https://img.shields.io/github/forks/open-telemetry/opentelemetry-dotnet-contrib?style=flat-square&color=blue)](https://github.com/open-telemetry/opentelemetry-dotnet-contrib/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> This repository contains set of components extending functionality of the OpenTelemetry .NET SDK. Instrumentation libraries, exporters, and other components can find their home here.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 641 |
| 🍴 **Forks** | 393 |
| 💻 **Language** | C# |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`dotnet` `dotnet-core` `opentelemetry`

## 🎯 Categories

Libraries & SDKs · Observability

## 📝 Summary

### English

**Brief Summary**  
The **open‑telemetry/opentelemetry‑dotnet‑contrib** repository houses community‑maintained extensions for the OpenTelemetry .NET SDK, including additional instrumentation libraries, exporters, and helper components. These contributions let .NET developers enrich their observability stack (traces, metrics, logs) without building custom integrations from scratch.

**Value Proposition**  
- **Accelerated AI‑enabled observability** – By plugging into the existing OpenTelemetry ecosystem, teams can quickly add telemetry that feeds AI/ML pipelines (e.g., for anomaly detection, RAG, or autonomous agents) without re‑implementing low‑level instrumentation.  
- **Broad coverage** – The contrib packages expose ready‑made instrumentations for popular .NET frameworks (ASP.NET Core, Entity Framework, HttpClient, etc.) and exporters to cloud‑native back‑ends, reducing time‑to‑value for prototype and internal projects.  
- **Open‑source community support** – With ~640 stars and an active fork base, the project benefits from community contributions and peer review, which helps surface best‑practice patterns for telemetry‑driven AI use cases.

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC)** – Start with the README and sample code to add a single contrib package (e.g., `OpenTelemetry.Contrib.Instrumentation.AspNetCore`) to an existing .NET service. Verify that traces/metrics appear in your chosen backend (Jaeger, Prometheus, Azure Monitor, etc.).  
2. **Iterate & Extend** – Incrementally add more instrumentations or exporters as needed (e.g., HTTP client, SQL client). Use the provided configuration helpers to align telemetry attributes with the data schema expected by your AI models.  
3. **Integrate with AI Pipelines** – Export telemetry to a storage or streaming layer (Kafka, Azure Event Hubs, etc.) that feeds downstream ML/RAG pipelines. Leverage the enriched context (span attributes, logs) to train or query models.  
4. **Production Hardening** – Conduct a checklist before moving beyond the PoC:  
   - Review the project’s LICENSE (Apache‑2.0) for compatibility.  
   - Perform a security scan of the NuGet packages and ensure no known CVEs.  
   - Pin versions and set up automated dependency updates.  
   - Validate performance impact (sampling, batch export settings).  

**Production Readiness Assessment**  
- **Maturity**: Medium. The library is stable enough for internal or prototype workloads, but it is community‑driven rather than officially maintained by the OpenTelemetry core team.  
- **Signals**: Recent commits (as of 2026‑06‑24), a healthy star/fork count, and clear documentation indicate active use, yet the contributor base is smaller than the core SDK.  
- **Risks**:  
  - **Maintenance** – Ensure at least one team member monitors upstream changes and releases.  
  - **Security** – Perform regular dependency audits; the project does not ship its own security policy file.  
  - **Support** – No formal SLA; rely on community issue tracking and internal fallback to the core SDK if a contrib package becomes unmaintained.  

**Bottom Line**  
OpenTelemetry’s .NET contrib repository offers a pragmatic shortcut to embed rich observability data into AI/ML workflows, making it a solid choice for prototyping and internal services. With a disciplined PoC‑to‑production transition—focused on version pinning, security vetting, and performance tuning—organizations can safely elevate the library to production for observability‑driven AI use cases.

### Русский

open-telemetry/opentelemetry-dotnet-contrib — набор расширений для OpenTelemetry .NET SDK (инструментация, экспортеры и прочие компоненты), позволяющих быстро добавить наблюдаемость и AI‑ориентированные метрики в .NET‑приложения без построения стеков с нуля. Типичный сценарий — небольшое POC‑внедрение: подключить нужные библиотеки из репозитория к существующему сервису, собрать телеметрию и использовать её в прототипах RAG/агентных воркфлоу. Готовность к production — средняя: проект активно поддерживается (обновления, 641 ★), но перед релизом в прод требуется проверка лицензии, безопасности и стабильности зависимостей.

### 中文

**项目简介（2‑3 句话）**  
OpenTelemetry .NET Contrib 为 OpenTelemetry .NET SDK 提供了丰富的扩展组件，包括多种仪器化库、导出器以及实用工具，帮助开发者快速为 .NET 应用添加可观测性。该仓库聚合了社区贡献的插件，便于在现有监控体系中统一采集、传输和分析遥测数据。

**价值**  
- **即插即用**：无需自行实现底层采集逻辑，直接使用成熟的仪器化库即可捕获日志、指标、追踪等数据。  
- **加速 AI/ML 监控**：在原型阶段即可为模型推理、RAG 或 Agent 工作流注入可观测性，帮助快速定位性能瓶颈和错误。  
- **生态兼容**：兼容 OpenTelemetry 标准，可无缝对接 Prometheus、Jaeger、OTLP 等后端，降低跨语言/跨系统的集成成本。

**典型接入方式**  
1. **阅读 README**：确认所需的仪器化库（如 `OpenTelemetry.Instrumentation.Http`、`OpenTelemetry.Exporter.Console`）已在项目中列出。  
2. **添加 NuGet 包**：在 .NET 项目中通过 `dotnet add package` 安装对应的 Contrib 包。  
3. **在代码或配置中启用**：使用 `TracerProviderBuilder` / `MeterProviderBuilder` 注册仪器化和导出器，例如：

   ```csharp
   using OpenTelemetry;
   using OpenTelemetry.Trace;

   var tracerProvider = Sdk.CreateTracerProviderBuilder()
       .AddHttpClientInstrumentation()
       .AddOtlpExporter(opts => { opts.Endpoint = new Uri("http://otel-collector:4317"); })
       .Build();
   ```

4. **验证**：运行本地或 CI 环境，检查遥测数据是否成功发送到目标后端。  

**生产可用性**  
- **成熟度**：项目已有 600+ 星、近 400 次 fork，活跃度截至 2026‑06‑24，代码质量和社区支持较好，适合作为原型和内部服务的观测层。  
- **准备度**：属于 **中等**（Medium）级别。对生产环境使用前建议：  
  - 评估所选导出器的可靠性和安全性（TLS、身份验证）。  
  - 确认依赖的 Contrib 包的维护频率，避免长期未更新的组件。  
  - 在预生产环境进行压力测试，确保采集开销在可接受范围。  
- **风险**：许可证（Apache‑2.0）和安全审计需要再次确认；若项目缺少专职维护者，建议自行 fork 并锁定依赖版本。  

综上，`open-telemetry/opentelemetry-dotnet-contrib` 是在 .NET 生态中快速加入可观测性的实用工具，适合从原型到内部生产系统的逐步推进，只要做好依赖审查和性能验证，即可安全投入使用。

## 🧭 Practical evaluation

**Value:** open-telemetry/opentelemetry-dotnet-contrib helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 641 GitHub stars
- 393 forks
- updated 2026-06-24
- primary language: C#
- 3 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 65/100 |
| stars | 60/100 |
| topics | 38/100 |
| outlook | 69/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 61/100 |
| production | 67/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/open-telemetry/opentelemetry-dotnet-contrib) · [← Back to Libraries--sdks](./README.md)</sub>
