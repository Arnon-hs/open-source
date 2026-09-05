# DataDog/datadog-lambda-extension

[![Stars](https://img.shields.io/github/stars/DataDog/datadog-lambda-extension?style=flat-square&color=yellow)](https://github.com/DataDog/datadog-lambda-extension/stargazers) [![Forks](https://img.shields.io/github/forks/DataDog/datadog-lambda-extension?style=flat-square&color=blue)](https://github.com/DataDog/datadog-lambda-extension/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> The Datadog Lambda Extension supports submitting: custom metrics; traces; logs; and more observability; asynchronously while your AWS Lambda function executes.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 134 |
| 🍴 **Forks** | 20 |
| 💻 **Language** | Rust |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`aws-lambda` `datadog` `rust` `serverless`

## 🎯 Categories

Cloud & Storage · Observability

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The Datadog Lambda Extension lets AWS Lambda functions emit custom metrics, traces, logs, and other observability data asynchronously, without changing your function code. Packaged as a lightweight Rust binary, it is installed as a Lambda layer and runs alongside your function, forwarding data to Datadog in real time. It is a community‑maintained open‑source project (≈130 ★) that speeds up the rollout of standardized monitoring across serverless workloads.

**Value**  
- **Reuse of existing observability stack** – Teams can leverage Datadog’s full APM, metrics, and log pipelines without building custom exporters or sidecars.  
- **Zero‑code instrumentation** – By simply attaching the extension, every invocation automatically reports latency, error counts, and custom metrics, reducing boilerplate and ensuring consistent telemetry across services.  
- **Cost‑effective scaling** – Because the extension runs in the same execution environment, it adds negligible latency and scales automatically with Lambda invocations.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Add the official Datadog Lambda Extension layer (ARN provided in the README) to a single test Lambda. Verify that metrics, traces, and logs appear in your Datadog workspace.  
2. **Configuration** – Set required environment variables (`DD_API_KEY`, `DD_SITE`, `DD_LOGS_ENABLED`, etc.) and, if needed, enable custom metrics via the `DD_CUSTOM_METRICS` variable.  
3. **CI/CD Integration** – Encode the layer ARN and env‑var settings into your infrastructure‑as‑code (e.g., Terraform, SAM, or Serverless Framework) so new functions automatically inherit the extension.  
4. **Gradual Rollout** – Extend the layer to additional functions or services, monitoring for any cold‑start impact or permission issues.  
5. **Documentation & Governance** – Capture the setup steps in an internal wiki and add a checklist to your service‑creation template to ensure consistent adoption.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last update 2026‑06‑23) and has a modest community footprint (≈130 ★, 20 forks).  
- **Stability**: Suitable for prototypes, internal tools, and low‑risk production workloads after a short validation period.  
- **Risks**: The integration flow is not fully described in the metadata; you’ll need to confirm IAM permissions, layer size limits, and any runtime compatibility (supported runtimes are listed in the README).  
- **Recommendation**: Conduct a small PoC, verify that the extension meets latency and cost expectations, then proceed to production with proper monitoring of Lambda cold‑starts and dependency updates. Once vetted, it can become the default observability layer for all serverless services in your organization.

### Русский

DataDog / datadog‑lambda‑extension — это открытая расширяющая библиотека на Rust, позволяющая в реальном времени отправлять пользовательские метрики, трассировки и логи из AWS Lambda, тем самым централизуя наблюдаемость без необходимости писать собственную инфраструктуру. Типичный сценарий — запуск небольшого proof‑of‑concept, проверка README и базовой конфигурации, а затем интеграция в сервисы API для ускорения их вывода в продакшн и унификации паттернов мониторинга. Готовность к production — средняя: проект стабилен и активно поддерживается (134 звёзд, последние коммиты), но требует проверки зависимостей и процесса установки перед масштабным использованием.

### 中文

**项目简介（2‑3 句话）**  
DataDog 的 Lambda Extension 用 Rust 实现，可在 AWS Lambda 运行期间异步上报自定义指标、分布式追踪、日志等可观测性数据，帮助开发者在不改动业务代码的前提下统一采集监控信息。

**价值**  
- **复用平台设施**：团队无需自行搭建指标、追踪、日志收集管道，直接复用 Datadog 已成熟的后端服务。  
- **加速交付**：统一的可观测性层让 API 服务可以更快上线、快速定位问题，提升整体开发效率。  
- **标准化**：通过统一的 Extension，所有 Lambda 函数遵循相同的监控、追踪规范，降低运维成本。

**典型接入方式**  
1. **在 Lambda 函数的部署包或层中加入 Extension**（可通过 Datadog 官方提供的 Lambda Layer 或自行编译 Rust 二进制）。  
2. **在函数的环境变量中配置 Datadog API key、site、日志端点等**，如 `DD_API_KEY`、`DD_SITE`、`DD_LOGS_ENABLED=true`。  
3. **在函数代码中正常使用 Datadog SDK（如 `datadog-lambda-python`、`datadog-lambda-java`）**，Extension 会在函数执行期间自动收集并异步发送指标/trace/log。  
4. **先做小范围 PoC**：在一个测试函数或 staging 环境启用 Extension，验证数据上报、延迟和费用，再逐步推广到生产函数。

**生产可用性**  
- **成熟度**：GitHub 约 130+ ⭐，活跃维护（最近更新 2026‑06‑23），主语言 Rust，具备基本的社区和文档支撑。  
- **适用场景**：适合内部原型、实验性服务或对可观测性要求较高的业务；在正式生产环境使用前，需要完成以下检查：  
  - 依赖版本兼容性（Lambda 运行时、Datadog API）。  
  - 评估延迟与费用（异步上报会产生额外网络流量）。  
  - 建立监控告警，确保 Extension 本身的健康状态（如启动失败、上报错误）。  
- **总体评估**：**中等**。在完成上述验证后，可作为生产级监控方案使用；若对延迟或成本极为敏感，建议进行更细致的性能基准测试后再全面推广。

## 🧭 Practical evaluation

**Value:** DataDog/datadog-lambda-extension helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 134 GitHub stars
- 20 forks
- updated 2026-06-23
- primary language: Rust
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 33/100 |
| stars | 45/100 |
| topics | 50/100 |
| outlook | 62/100 |
| quality | 61/100 |
| recency | 80/100 |
| adoption | 42/100 |
| production | 63/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/DataDog/datadog-lambda-extension) · [← Back to Cloud--storage](./README.md)</sub>
