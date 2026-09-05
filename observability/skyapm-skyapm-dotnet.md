# SkyAPM/SkyAPM-dotnet

[![Stars](https://img.shields.io/github/stars/SkyAPM/SkyAPM-dotnet?style=flat-square&color=yellow)](https://github.com/SkyAPM/SkyAPM-dotnet/stargazers) [![Forks](https://img.shields.io/github/forks/SkyAPM/SkyAPM-dotnet?style=flat-square&color=blue)](https://github.com/SkyAPM/SkyAPM-dotnet/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> The .NET/.NET Core instrument agent for Apache SkyWalking

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.7k |
| 🍴 **Forks** | 332 |
| 💻 **Language** | C# |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`apm` `csharp` `distributed-tracing` `dotnet` `metric` `observability` `skywalking`

## 🎯 Categories

Observability

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
SkyAPM‑dotnet is the official .NET/.NET Core instrumentation agent for Apache SkyWalking, enabling automatic collection of distributed tracing, metrics, and logging from C# applications. With over 1.6 k stars and active maintenance, it offers a ready‑to‑use observability layer that can be extended with AI‑driven analysis without building a monitoring stack from scratch.  

**Value**  
By plugging into the SkyWalking ecosystem, SkyAPM‑dotnet gives developers immediate visibility into service latency, error rates, and request flows, while also exposing the collected telemetry to AI/ML pipelines for anomaly detection, root‑cause analysis, or RAG (retrieval‑augmented generation) use cases. This eliminates the need to assemble a custom data‑pipeline and model‑training infrastructure, accelerating the prototyping of AI‑enhanced observability features.  

**Practical Adoption Path**  

1. **Proof‑of‑Concept** – Clone the repo, follow the README to add the NuGet package to a small test service, and enable the default SkyWalking agent configuration.  
2. **Validate Integration** – Verify that traces appear in a local or cloud‑hosted SkyWalking UI; experiment with exporting metrics to your AI tooling (e.g., Prometheus → Grafana ML, or direct API calls).  
3. **Scale Gradually** – Extend the agent to additional services, customize plugins for business‑specific libraries, and start feeding the telemetry into your AI models or RAG pipelines.  

**Production Readiness**  
The project scores a solid 65/100 and shows strong production signals: recent commits (as of 2026‑06‑28), a vibrant community (1 656 stars, 332 forks), and adoption in multiple enterprise environments. While the integration steps are not fully documented in the metadata, the agent is mature enough for a serious pilot, provided you allocate time for initial setup verification and any needed custom plugin development.

### Русский

SkyAPM‑dotnet — это открытый агент для трассировки и наблюдаемости приложений на .NET/.NET Core, совместимый с платформой Apache SkyWalking. Он позволяет быстро добавить возможности мониторинга и AI‑поддержки (например, прототипировать RAG‑сервисы или агентные воркфлоу) без необходимости строить стек с нуля, что делает его идеальным для небольших proof‑of‑concept и последующего масштабирования. Проект имеет активную поддержку (1656 звёзд, регулярные обновления, широкое сообщество) и считается готовым к пилотному использованию в продакшн, хотя детали интеграции стоит уточнить в README и протестировать на небольшом примере.

### 中文

**项目简介**  
SkyAPM‑dotnet 是 Apache SkyWalking 官方提供的 .NET/.NET Core 探针代理，用于在 C# 应用中自动埋点、收集链路追踪、指标与日志，实现完整的可观测性。  

**价值**  
- **即插即用**：无需手写埋点代码，直接在现有 .NET 项目中引入即可获得分布式追踪、性能指标和错误告警。  
- **统一观测平台**：与 SkyWalking 后端无缝对接，统一管理微服务、容器、Serverless 等多种运行环境的监控数据。  
- **提升研发效率**：帮助开发团队快速定位性能瓶颈和异常，缩短故障定位时间，提升系统可靠性。  

**典型接入方式**  
1. **添加 NuGet 包**：在项目的 `*.csproj` 中加入 `SkyApm.Agent.AspNetCore`（或对应的 `SkyApm.Agent`）并执行 `dotnet restore`。  
2. **配置环境变量或 appsettings**：通过 `SKYWALKING__SERVICE_NAME`、`SKYWALKING__COLLECTOR__ADDRESS` 等变量指定服务名、Collector 地址、采样率等。  
3. **启动即生效**：在 `Program.cs` 中调用 `builder.UseSkyApm()`（ASP.NET Core）或在普通控制台程序中调用 `SkyApm.Agent.AgentBootstrap.Start()`，无需修改业务代码。  
4. **验证**：访问 SkyWalking UI，确认对应服务的链路、指标已出现。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑28，项目拥有 1.6k+ ⭐、332 fork，最近一次提交在 2026‑06‑28，社区维护频繁。  
- **成熟生态**：已被多家企业在生产环境中采用，支持 .NET Framework、.NET Core、ASP.NET Core、gRPC、EntityFramework 等常见技术栈。  
- **稳定性**：提供完整的单元测试、详细的文档与示例，兼容多种部署方式（K8s、Docker、裸机），可直接用于正式业务。  

**建议**  
在正式上线前，可先在测试环境完成一个小型 POC（例如在一个微服务中仅开启链路追踪），确认 Collector、后端 UI 与现有日志体系的兼容性后，再逐步推广到全链路。整体来看，SkyAPM‑dotnet 已具备进入生产的技术成熟度。

## 🧭 Practical evaluation

**Value:** SkyAPM/SkyAPM-dotnet helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1656 GitHub stars
- 332 forks
- updated 2026-06-28
- primary language: C#
- 7 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 63/100 |
| stars | 69/100 |
| topics | 88/100 |
| outlook | 75/100 |
| quality | 78/100 |
| recency | 80/100 |
| adoption | 67/100 |
| production | 69/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/SkyAPM/SkyAPM-dotnet) · [← Back to Observability](./README.md)</sub>
