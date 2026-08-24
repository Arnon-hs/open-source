# reidmorrison/semantic_logger

[![Stars](https://img.shields.io/github/stars/reidmorrison/semantic_logger?style=flat-square&color=yellow)](https://github.com/reidmorrison/semantic_logger/stargazers) [![Forks](https://img.shields.io/github/forks/reidmorrison/semantic_logger?style=flat-square&color=blue)](https://github.com/reidmorrison/semantic_logger/network) [![Language](https://img.shields.io/badge/lang-Ruby-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> Semantic Logger is a feature rich logging framework, and replacement for existing Ruby & Rails loggers.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 951 |
| 🍴 **Forks** | 138 |
| 💻 **Language** | Ruby |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bugsnag` `elasticsearch` `logging` `rails-semantic-logger` `splunk` `syslog`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
Semantic Logger (reidmorrison/semantic_logger) is a feature‑rich, drop‑in replacement for Ruby and Rails logging that adds structured, semantic output and advanced filtering capabilities. With over 950 stars and active maintenance, it can serve as a foundation for rapid AI‑related prototyping—such as RAG pipelines or agent workflows—by providing clean, machine‑readable logs that downstream models can consume.

**Value**  
- **Structured logs for AI** – By emitting JSON or key‑value pairs, the logger makes it trivial to feed application events into LLMs, vector stores, or monitoring pipelines without writing custom parsers.  
- **Feature set** – Supports log levels, thread‑local contexts, log rotation, and multiple output destinations (file, STDOUT, Syslog, Kafka, etc.), reducing the need for separate logging utilities.  
- **Community & maturity** – 951 stars, frequent updates, and a solid Ruby ecosystem mean you get a battle‑tested component rather than building a logger from scratch.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, run `bundle install`, and replace `Rails.logger` (or `Logger.new`) with `SemanticLogger::Logger.new('app')` in a sandbox Rails or Sinatra app. Verify that logs appear in JSON format.  
2. **Integrate with AI stack** – Point the logger to a file or a streaming sink (e.g., Kafka) that your RAG or agent service reads from, then use the structured fields as prompts or metadata.  
3. **Iterate** – Add context (e.g., `SemanticLogger.tagged`) around AI calls to capture request IDs, model versions, and latency.  
4. **Scale** – Once the pattern is validated, migrate the logger configuration to the main codebase, lock the gem version, and add CI tests to ensure log format stability.

**Production Readiness**  
- **Maturity:** Medium. The library is stable and widely used, but it is a logging component, not an AI model itself, so the “AI‑ready” claim depends on how you consume the logs.  
- **Dependencies:** Pure Ruby with optional back‑ends; ensure any chosen sink (Kafka, Elasticsearch, etc.) is already part of your stack.  
- **Operational concerns:** Verify log rotation, storage costs, and compliance (PII handling) for structured logs.  
- **Risk mitigation:** Conduct a small pilot, lock the gem version, and add monitoring for log‑ingestion failures before promoting to production.  

Overall, Semantic Logger offers a low‑friction way to generate AI‑friendly logs in Ruby applications, making it a practical choice for prototypes and internal workflows, with a clear path to production once integration and compliance checks are completed.

### Русский

Semantic Logger — это мощный open‑source фреймворк для логирования в Ruby и Rails, который упрощает добавление AI‑функционала (RAG, агентные сценарии) без необходимости писать собственный стек. Для внедрения рекомендуется начать с небольшого proof‑of‑concept, следуя инструкциям в README, и проверить совместимость с текущей инфраструктурой. Проект имеет средний уровень готовности к production: достаточная популярность (951 звёзд) и активные обновления, но требует проверки зависимостей и возможных сложностей интеграции.

### 中文

**项目简介**  
Semantic Logger（reidmorrison/semantic_logger）是一个功能丰富的 Ruby/ Rails 日志框架，可直接替代默认的 logger，提供结构化、可搜索、可自定义的日志输出，帮助开发者在代码中快速加入 AI 相关的可观测性与调试信息。

**价值**  
- **提升可观测性**：通过结构化 JSON、日志级别过滤、颜色高亮等特性，让 AI 模型的调用链、输入输出、错误信息一目了然。  
- **降低集成成本**：只需在 Gemfile 中加入 `semantic_logger` 并在初始化文件中配置一次，即可在整个 Rails 应用或纯 Ruby 项目中统一使用，无需改动业务代码。  
- **支持 AI 工作流**：配合 RAG、Agent 或模型监控工具，可把模型请求、响应、延迟、token 消耗等关键指标写入日志，便于后续分析与优化。

**典型接入方式**  
1. **添加依赖**  
   ```ruby
   # Gemfile
   gem 'semantic_logger'
   ```
2. **初始化配置（Rails 示例）**  
   ```ruby
   # config/initializers/semantic_logger.rb
   SemanticLogger.add_appender(file_name: 'log/application.log', formatter: :json)
   Rails.logger = SemanticLogger['Rails']
   ```
3. **在代码中使用**  
   ```ruby
   logger = SemanticLogger['MyAIService']
   logger.info "model_call", model: 'gpt-4', prompt: prompt, response: response
   ```
4. **与 AI 监控平台对接**（可选）  
   - 将日志输出到 Elasticsearch / Loki / CloudWatch，或使用 `semantic_logger` 的 HTTP appender 直接推送到自建的日志聚合服务。

**生产可用性**  
- **成熟度**：已有 951+ ⭐、138+ 🍴，活跃维护（截至 2026‑06‑22），社区成熟度中等。  
- **适用场景**：非常适合原型、内部工具或需要快速可观测性的 AI 项目；在生产环境使用前建议完成以下检查：  
  1. **依赖审计**：确认兼容的 Ruby 版本、Rails 版本以及其他 gem 的冲突。  
  2. **性能评估**：在高并发下对 JSON 序列化和文件写入进行基准测试，必要时开启异步 appender。  
  3. **日志治理**：配置日志轮转、压缩以及敏感信息脱敏，防止日志泄露。  
- **风险**：集成路径在官方文档中较为简洁，缺少针对 AI 框架的示例；建议先在小型 PoC 中验证配置和性能，再推广到全链路。  

综上，Semantic Logger 能够以极低的成本为 Ruby/ Rails 项目提供结构化、可搜索的日志能力，是构建 AI 可观测性与调试体系的实用工具，只要做好依赖、性能和安全检查，即可在生产环境安全使用。

## 🧭 Practical evaluation

**Value:** reidmorrison/semantic_logger helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 951 GitHub stars
- 138 forks
- updated 2026-06-22
- primary language: Ruby
- 6 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 54/100 |
| stars | 63/100 |
| topics | 75/100 |
| outlook | 58/100 |
| quality | 64/100 |
| recency | 40/100 |
| adoption | 61/100 |
| production | 54/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/reidmorrison/semantic_logger) · [← Back to Misc](./README.md)</sub>
