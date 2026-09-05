# open-telemetry/opentelemetry-js-contrib

[![Stars](https://img.shields.io/github/stars/open-telemetry/opentelemetry-js-contrib?style=flat-square&color=yellow)](https://github.com/open-telemetry/opentelemetry-js-contrib/stargazers) [![Forks](https://img.shields.io/github/forks/open-telemetry/opentelemetry-js-contrib?style=flat-square&color=blue)](https://github.com/open-telemetry/opentelemetry-js-contrib/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> OpenTelemetry instrumentation for JavaScript modules

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 904 |
| 🍴 **Forks** | 655 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Observability

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
OpenTelemetry JS Contrib provides a growing collection of community‑maintained instrumentation modules for JavaScript and TypeScript applications, enabling automatic trace, metric, and log collection from popular libraries and frameworks. With over 900 GitHub stars and active recent commits, it offers a lightweight way to add observability to production services, though the available integration metadata is limited and requires manual review before use.  

**Value**  
- **Visibility:** By auto‑instrumenting common Node.js/Browser packages, it surfaces request flows, latency, and error information that would otherwise require custom logging or tracing code.  
- **Speed to Insight:** Teams can start capturing end‑to‑end telemetry with minimal code changes, accelerating debugging of production incidents and health monitoring.  
- **Extensibility:** The contrib package is modular; you can pick only the instrumentations you need, keeping bundle size low while staying compatible with the core OpenTelemetry SDK.

**Practical Adoption Path**  
1. **Evaluate Fit:** Review the list of supported libraries (e.g., Express, Axios, pg, Redis) and confirm they match the dependencies in your codebase.  
2. **Prototype:** Add `@opentelemetry/contrib` to a non‑critical branch, enable a few instrumentations, and run locally or in a staging environment. Observe the generated spans/metrics and verify they align with your monitoring backend (e.g., Jaeger, Prometheus, Grafana).  
3. **Metadata Review:** Because the discovered integration signals are sparse, manually audit the generated telemetry for completeness and ensure no sensitive data is inadvertently captured.  
4. **Lock Versions & Add Tests:** Pin the package version, add integration tests that assert expected spans are emitted, and include the instrumentation in your CI pipeline.  
5. **Roll Out Gradually:** Deploy the instrumented service behind a feature flag or to a small percentage of traffic, monitor overhead, and iterate before full production rollout.

**Production Readiness**  
- **Maturity:** Rated “Medium.” The library is stable enough for prototypes and internal tooling, but production use should be preceded by dependency checks and a maintenance plan.  
- **Maintenance Signals:** 904 stars, 655 forks, and recent commits (as of 2026‑05‑11) indicate an active community, yet you should verify that core maintainers are still responding to issues and security patches.  
- **Risk Considerations:** No major licensing or metadata red flags have been identified, but a final security audit and confirmation of an active maintainer roster are advisable before committing to long‑term production deployment.  

In short, OpenTelemetry JS Contrib offers a pragmatic way to enrich JavaScript services with observability data, provided you perform a brief validation and monitoring phase to ensure it meets your reliability and security standards.

### Русский

open‑telemetry/opentelemetry‑js‑contrib — это набор TypeScript‑инструментов для автоматической трассировки и метрик JavaScript‑модулей, позволяющий быстро получать видимость поведения приложений в продакшене и упрощать отладку. Обычно его подключают в прототипы или внутренние сервисы, где требуется мониторинг систем, диагностика проблем и контроль здоровья сервисов, при этом перед запуском в продакшн рекомендуется проверить покрытие сигналов и убедиться в актуальности зависимостей. Готовность к продакшн — средняя: проект стабилен (904★, 655 форков, активные коммиты), но требует дополнительного аудита лицензий, безопасности и поддержки перед широким использованием.

### 中文

**项目简介**  
OpenTelemetry JS Contrib 为 JavaScript/TypeScript 项目提供丰富的 OpenTelemetry 仪表化插件，帮助开发者在生产环境中更轻松地观察、调试和分析代码行为。

**价值**  
- **可观测性即代码即服务**：通过统一的 trace、metric、log 接口，将业务关键路径、外部依赖和错误信息自动化捕获，显著降低排障成本。  
- **生态兼容**：覆盖常见的 Node.js 框架（Express、Koa、NestJS 等）和库（Redis、MySQL、gRPC 等），让已有系统快速接入统一的监控平台。  
- **社区活跃**：拥有 900+ 星、600+ Fork，持续更新（截至 2026‑05‑11），社区贡献丰富的插件集合。

**典型接入方式**  
1. **安装核心与插件**  
   ```bash
   npm i @opentelemetry/api @opentelemetry/sdk-node \
         @opentelemetry/instrumentation-http \
         @opentelemetry/instrumentation-express \
         ...   # 根据业务选取对应的 @opentelemetry/instrumentation-*
   ```
2. **初始化 SDK**（通常放在项目入口文件）  
   ```ts
   import { NodeTracerProvider } from '@opentelemetry/sdk-trace-node';
   import { registerInstrumentations } from '@opentelemetry/instrumentation';
   import { HttpInstrumentation } from '@opentelemetry/instrumentation-http';
   import { ExpressInstrumentation } from '@opentelemetry/instrumentation-express';
   import { SimpleSpanProcessor } from '@opentelemetry/sdk-trace-base';
   import { OTLPTraceExporter } from '@opentelemetry/exporter-trace-otlp-grpc';

   const provider = new NodeTracerProvider();
   provider.addSpanProcessor(new SimpleSpanProcessor(new OTLPTraceExporter()));
   provider.register();

   registerInstrumentations({
     instrumentations: [
       new HttpInstrumentation(),
       new ExpressInstrumentation(),
       // 其它业务库的 instrumentation
     ],
   });
   ```
3. **在监控平台（如 Jaeger、Tempo、Prometheus）查看**：启动后，所有已注册的库会自动产生 trace/metric，直接在后端 UI 中进行可视化分析。

**生产可用性**  
- **成熟度**：Medium。插件已在多个开源项目和内部原型中验证，功能完整，但部分 instrumentation 的元数据较为稀疏，建议在正式环境前进行一次完整的信号覆盖检查。  
- **依赖与维护**：项目使用 TypeScript 编写，依赖明确；社区活跃度高，近期仍有维护者提交 PR。上线前请确认所选插件的最新版本与项目的 Node.js 版本兼容。  
- **风险**：暂无重大许可证或安全漏洞报告，但仍需自行审计依赖的安全姿态，并确保后端接收端（OTLP、Jaeger 等）具备相应的容量和访问控制。  

综上，**open-telemetry/opentelemetry-js-contrib** 是在 JavaScript 生态中实现统一可观测性的实用工具，适合先在预生产或内部系统中验证信号完整性，随后在经过依赖与安全审查后投入正式生产环境。

## 🧭 Practical evaluation

**Value:** open-telemetry/opentelemetry-js-contrib helps make production behavior easier to inspect and debug.

**Best use cases**

- monitor systems
- debug production behavior
- track service health

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 904 GitHub stars
- 655 forks
- updated 2026-05-11
- primary language: TypeScript

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 70/100 |
| stars | 63/100 |
| topics | 0/100 |
| outlook | 63/100 |
| quality | 64/100 |
| recency | 80/100 |
| adoption | 65/100 |
| production | 66/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/open-telemetry/opentelemetry-js-contrib) · [← Back to Observability](./README.md)</sub>
