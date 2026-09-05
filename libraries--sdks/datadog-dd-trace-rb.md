# DataDog/dd-trace-rb

[![Stars](https://img.shields.io/github/stars/DataDog/dd-trace-rb?style=flat-square&color=yellow)](https://github.com/DataDog/dd-trace-rb/stargazers) [![Forks](https://img.shields.io/github/forks/DataDog/dd-trace-rb?style=flat-square&color=blue)](https://github.com/DataDog/dd-trace-rb/network) [![Language](https://img.shields.io/badge/lang-Ruby-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Datadog's client library for Ruby

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 394 |
| 🍴 **Forks** | 401 |
| 💻 **Language** | Ruby |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`apm` `datadog` `debugging` `distributed-tracing` `hacktoberfest` `profiling` `ruby` `tracing`

## 🎯 Categories

Libraries & SDKs · Observability

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Datadog’s **dd‑trace‑rb** is the official Ruby client library for Datadog’s APM, providing a lightweight, idiomatic way to emit traces, spans, and metrics from Ruby applications. With over 390 stars, frequent releases and strong community adoption, it’s a mature, production‑ready OSS component that can be dropped into existing codebases to accelerate debugging and observability.  

**Value**  
- **Faster developer loops:** Automatic instrumentation and easy‑to‑use APIs let engineers add tracing with a single line, reducing the time spent writing custom logging or debugging code.  
- **Improved CI feedback:** Test suites can emit traces that surface performance regressions early, giving teams actionable insight before code reaches production.  
- **Consistent observability:** By exposing standardized Datadog signals (API/SDK/CLI metadata, language tags, etc.), the library ensures that data from Ruby services lines up with the broader Datadog ecosystem.  

**Practical Adoption Path**  
1. **Add the gem** (`gem 'ddtrace'`) to the project’s `Gemfile` and run `bundle install`.  
2. **Enable auto‑instrumentation** (e.g., `Datadog.configure do |c| c.tracing.enabled = true end`) or manually instrument critical code paths with `Datadog.tracer.trace`.  
3. **Configure the Datadog agent** (host/port, service name, environment) via environment variables or the `datadog.yaml` file.  
4. **Validate locally** by running the app and confirming traces appear in the Datadog UI; then extend the same setup to CI pipelines for automated feedback.  

**Production Readiness**  
- **Activity & Adoption:** Recent commits (as of 2026‑05‑11), a healthy fork/star count, and widespread use in the Ruby community signal strong momentum.  
- **Stability:** The library follows SemVer, provides comprehensive documentation, and integrates cleanly with the official Datadog agent.  
- **Risk Assessment:** No immediate licensing or security red flags, though a final review of the maintainers’ responsiveness and any disclosed vulnerabilities is advisable. Overall, dd‑trace‑rb is ready for a serious pilot or full‑scale production deployment.

### Русский

DataDog/dd-trace-rb — открытая клиентская библиотека Datadog для Ruby, позволяющая быстро интегрировать трассировку и метрики в приложения, тем самым ускоряя цикл разработки, ревью кода и повышая качество CI‑feedback. Типичный сценарий — подключение библиотеки в сервисы и тестовые окружения для автоматического сбора телеметрии и упрощения отладки без изменения бизнес‑логики. Проект считается готовым к production: активные коммиты, широкое принятие (394 ★, 401 fork), поддержка Ruby и богатый набор тем, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
DataDog/dd-trace-rb 是 Datadog 为 Ruby 生态提供的官方 APM 客户端库，帮助开发者在代码中轻松植入分布式追踪、性能指标和错误监控。

**价值**  
- **提升开发效率**：通过自动化埋点和统一的监控视图，缩短调试和代码审查的循环时间。  
- **加速 CI 反馈**：在持续集成阶段即可捕获性能回归和异常，提前发现问题。  
- **统一可观测性**：将服务调用链、数据库查询、外部 API 等关键信号统一上报到 Datadog，便于全链路分析和报警。

**典型接入方式**  
1. 在 `Gemfile` 中加入 `gem 'ddtrace'` 并执行 `bundle install`。  
2. 在应用启动入口（如 `config/initializers/datadog.rb`）初始化 tracer：  
   ```ruby
   Datadog.configure do |c|
     c.tracer hostname: 'agent-host', port: 8126
     c.service = 'my-ruby-app'
     c.env     = ENV['RACK_ENV']
   end
   ```  
3. 按需启用框架集成（Rails、Sinatra、Sidekiq 等），或使用 `Datadog::Tracing.trace('custom.operation')` 手动埋点。  
4. 在 CI 环境中通过环境变量 `DD_TRACE_AGENT_URL` 配置本地或远程 Datadog Agent，即可在构建日志中获取实时追踪信息。

**生产可用性**  
- **活跃度高**：最近一次提交在 2026‑05‑11，拥有 394+ 星、401+ Fork，社区和 Datadog 官方均在持续维护。  
- **成熟度**：已在多个大型 Ruby 项目中上线，支持 Rails、Rack、Sidekiq、grpc 等常见框架，具备完整的错误捕获与指标导出能力。  
- **风险**：暂无重大元数据风险，但仍需在正式投产前完成许可证合规、漏洞扫描以及维护者响应时效的最终确认。

总体而言，dd-trace-rb 已具备在生产环境中安全、可靠地使用的条件，是 Ruby 应用实现可观测性的首选 OSS 方案。

## 🧭 Practical evaluation

**Value:** DataDog/dd-trace-rb helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 394 GitHub stars
- 401 forks
- updated 2026-05-11
- primary language: Ruby
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 65/100 |
| stars | 55/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 76/100 |
| recency | 80/100 |
| adoption | 58/100 |
| production | 70/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/DataDog/dd-trace-rb) · [← Back to Libraries--sdks](./README.md)</sub>
