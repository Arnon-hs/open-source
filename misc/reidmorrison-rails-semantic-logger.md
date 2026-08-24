# reidmorrison/rails_semantic_logger

[![Stars](https://img.shields.io/github/stars/reidmorrison/rails_semantic_logger?style=flat-square&color=yellow)](https://github.com/reidmorrison/rails_semantic_logger/stargazers) [![Forks](https://img.shields.io/github/forks/reidmorrison/rails_semantic_logger?style=flat-square&color=blue)](https://github.com/reidmorrison/rails_semantic_logger/network) [![Language](https://img.shields.io/badge/lang-Ruby-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-44%2F100-brightgreen?style=flat-square)](#)

> Rails Semantic Logger replaces the Rails default logger with Semantic Logger

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 414 |
| 🍴 **Forks** | 141 |
| 💻 **Language** | Ruby |
| 📈 **Score** | 44/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Rails Semantic Logger is a drop‑in replacement for Rails’ built‑in logger that adds structured, high‑performance logging with semantic metadata. It lets developers capture rich context (e.g., request IDs, user info, custom tags) without changing existing Rails code, making debugging and observability easier. Although the repository is active (414 ★, 141 forks, last update 2026‑06‑26), the integration details are sparse, so a quick proof‑of‑concept is recommended before full adoption.

**Value**  
- **Structured logs**: Emits JSON or key‑value logs that can be ingested by modern observability platforms (e.g., Elastic, Splunk, Datadog) for faster root‑cause analysis.  
- **Performance**: Uses asynchronous, thread‑safe logging to reduce I/O overhead compared with the default Rails logger.  
- **Contextual enrichment**: Automatically adds request‑level data (controller, action, params) and lets you attach custom tags, which is especially useful when correlating logs with AI/ML pipelines or RAG/agent workflows.  

**Practical Adoption Path**  
1. **Prototype** – Add the gem (`gem 'rails_semantic_logger'`) to a sandbox branch and run `bundle install`.  
2. **Configure** – In `config/initializers/semantic_logger.rb` set the desired formatter (e.g., `SemanticLogger::Appender::File.new('log/semantic.log', formatter: :json)`).  
3. **Replace logger** – In `config/application.rb` add `config.logger = SemanticLogger::Logger.new(Rails.root.join('log', "#{Rails.env}.log"))`.  
4. **Validate** – Generate a few requests, inspect the output, and confirm that the log format matches your observability pipeline.  
5. **Iterate** – Add custom tags (`SemanticLogger.tagged`) or enrich with AI‑related metadata (model IDs, inference timestamps) as needed.  

**Production Readiness**  
- **Maturity**: Medium. The gem is widely used (hundreds of stars/forks) and actively maintained, but the metadata does not expose a clear migration guide for complex Rails setups.  
- **Risks**: Potential incompatibilities with other logging extensions (e.g., Lograge, ActiveSupport::TaggedLogging) and the need to ensure your log aggregation layer can parse the chosen format.  
- **Recommendation**: Deploy first in a staging environment or internal prototype, run performance benchmarks, and verify that all required log fields are captured before promoting to production. Once vetted, the gem can serve as a stable foundation for both traditional Rails logging and AI‑centric observability use cases.

### Русский

Rails Semantic Logger (reidmorrison/rails_semantic_logger) заменяет стандартный логгер Rails на более мощный Semantic Logger, предоставляя структурированные, цветные и производительные логи, что упрощает отладку и мониторинг приложений. Его обычно внедряют в существующее Rails‑приложение для прототипирования AI‑фич, RAG‑сценариев или агентных воркфлоу, однако интеграция требует ручного аудита, так как автоматические сигналы о совместимости ограничены. Проект имеет средний уровень готовности к продакшену: достаточную популярность (414 звёзд, 141 форк) и активные обновления, но перед запуском в продакшн рекомендуется проверить зависимости и обеспечить поддержку в команде.

### 中文

**项目简介（2‑3 句）**  
Rails Semantic Logger 用更结构化、可查询的日志格式取代 Rails 默认的 `Logger`，为 Rails 应用提供高性能的语义化日志记录。它兼容 Rails 的日志 API，同时支持 JSON、日志分级、线程安全等高级特性。

**价值**  
- **可观测性提升**：结构化日志让搜索、聚合和可视化（如在 ELK、Datadog、Splunk 中）变得简单，帮助快速定位问题。  
- **性能优化**：内部采用异步写入和批量缓冲，显著降低日志写入对请求响应时间的影响。  
- **易迁移**：保持与 Rails 原生日志接口兼容，几乎不需要改动业务代码即可获得全部功能。

**典型接入方式**  
1. **在 Gemfile 中加入**  
   ```ruby
   gem 'rails_semantic_logger'
   ```
2. **在 `config/application.rb`（或相应环境配置）中启用**  
   ```ruby
   Rails.application.configure do
     config.logger = SemanticLogger::Logger.new('log/#{Rails.env}.log')
     # 可选：输出为 JSON，便于后端日志平台解析
     # config.logger = SemanticLogger::Appender::File.new('log/#{Rails.env}.json', formatter: SemanticLogger::Formatters::Json.new)
   end
   ```
3. **如需在生产环境使用外部日志系统（如 Logstash）**，只需添加对应的 `SemanticLogger::Appender`（File、Udp、Tcp、Kafka 等），无需改动业务代码的 `Rails.logger.info` 调用。  
4. **可选的初始化脚本**（`config/initializers/semantic_logger.rb`）用于统一设置日志级别、过滤器或自定义标签。

**生产可用性**  
- **成熟度**：已有 400+ GitHub Stars、140+ Fork，社区活跃，最近一次提交仍在 2026 年，表明项目仍在维护。  
- **适用场景**：非常适合内部系统、原型项目以及对日志可观测性要求较高的生产服务。  
- **风险与注意事项**：  
  - 需要评估与现有日志收集管道（如 Fluentd、Logstash）兼容性，尤其是 JSON 格式的字段映射。  
  - 在高并发环境下建议使用异步 Appender（如 `SemanticLogger::Appender::Async`）并监控内存使用。  
  - 由于集成信号在元数据中较少，建议在上线前进行一次完整的功能验收（日志完整性、性能基准）。  

总体而言，Rails Semantic Logger 在提升日志结构化和性能方面表现突出，经过适当的配置和验证后，可在生产环境安全使用。

## 🧭 Practical evaluation

**Value:** reidmorrison/rails_semantic_logger helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 414 GitHub stars
- 141 forks
- updated 2026-06-26
- primary language: Ruby

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 54/100 |
| stars | 56/100 |
| topics | 0/100 |
| outlook | 46/100 |
| quality | 50/100 |
| recency | 40/100 |
| adoption | 55/100 |
| production | 49/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/reidmorrison/rails_semantic_logger) · [← Back to Misc](./README.md)</sub>
