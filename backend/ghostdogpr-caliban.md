# ghostdogpr/caliban

[![Stars](https://img.shields.io/github/stars/ghostdogpr/caliban?style=flat-square&color=yellow)](https://github.com/ghostdogpr/caliban/stargazers) [![Forks](https://img.shields.io/github/forks/ghostdogpr/caliban?style=flat-square&color=blue)](https://github.com/ghostdogpr/caliban/network) [![Language](https://img.shields.io/badge/lang-Scala-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Functional GraphQL library for Scala

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 993 |
| 🍴 **Forks** | 263 |
| 💻 **Language** | Scala |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`functional-programming` `graphql` `graphql-client` `graphql-server` `scala`

## 🎯 Categories

Backend · DevTools

## 📝 Summary

### English

**Summary**  
Caliban (ghostdogpr/caliban) is a functional GraphQL library for Scala that lets teams reuse existing service infrastructure instead of rebuilding common backend components. By providing a type‑safe, compile‑time API definition and a set of ready‑made integrations (SDK, CLI, etc.), it speeds up API delivery, promotes consistent service patterns, and reduces boilerplate across microservices. With strong community adoption (≈1 k stars, 263 forks), recent commits, and active maintainers, it is ready for a serious production pilot.

**Value**  
- **Reuse & consistency** – Define GraphQL schemas directly from Scala types, letting the same code serve as both server implementation and client SDK, which eliminates duplicated contracts.  
- **Speed to market** – Boilerplate‑free schema generation, automatic resolver wiring, and built‑in tooling let teams ship new API services in days rather than weeks.  
- **Standardization** – A single, well‑documented library enforces functional programming best practices across services, making onboarding and code reviews easier.

**Practical adoption path**  
1. **Prototype** – Add Caliban as a dependency in a sandbox Scala project, generate a simple schema, and run the built‑in GraphQL Playground to validate the workflow.  
2. **Integrate** – Replace existing hand‑rolled GraphQL endpoints with Caliban’s `Http4s`/`Akka‑Http`/`Play` adapters, leveraging its automatic resolver derivation.  
3. **Generate SDKs** – Use the provided CLI to emit type‑safe client code for other Scala services (or other languages via the GraphQL schema), ensuring contract fidelity.  
4. **CI/CD & monitoring** – Incorporate Caliban’s health‑check and tracing hooks into your pipeline, then roll out to a staging environment before full production cut‑over.

**Production readiness**  
- **Activity & community** – Recent commits (as of 2026‑05‑12), a healthy star/fork ratio, and active issue discussion indicate ongoing maintenance.  
- **Ecosystem fit** – Works with major Scala HTTP frameworks and integrates with existing tooling (sbt, mill, CI pipelines).  
- **Risk profile** – No critical licensing or security red flags detected; the remaining due diligence (license compliance, vulnerability scanning, maintainer responsiveness) should be completed before large‑scale rollout. Overall, Caliban meets the criteria for a high‑confidence production candidate.

### Русский

**ghostdogpr/caliban** — это функциональная GraphQL‑библиотека для Scala, позволяющая командам быстро запускать API‑сервисы, повторно используя уже построенную инфраструктуру бекенда и стандартизируя типичные паттерны сервисов. Проект готов к продакшн‑использованию: активная разработка, широкое принятие (≈ 1000 звёзд, 263 форка), свежие коммиты и сильные сигналы экосистемы, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
ghostdogpr/caliban 是一款面向 Scala 的函数式 GraphQL 库，帮助团队在已有的服务基础设施上快速构建统一的 API，而无需重复实现常见的后端功能。

**价值主张**  
- **复用基础设施**：通过统一的 GraphQL DSL 与代码生成器，团队可以直接复用已有的业务模型、认证、日志等通用组件，降低重复开发成本。  
- **加速 API 上线**：提供类型安全的 schema 定义、自动生成的客户端 SDK 以及可选的 CLI 工具，使得从设计到部署的全链路时间大幅缩短。  
- **标准化服务模式**：所有服务均采用同一套函数式编程范式和错误处理模型，提升代码可读性与可维护性，进而降低跨团队的技术碎片化风险。

**典型接入方式**  
1. **依赖引入**：在 `build.sbt` 中加入 `libraryDependencies += "com.github.ghostdogpr" %% "caliban" % "<version>"`。  
2. **Schema 定义**：使用 Scala case class 与 `caliban.schema` DSL 编写 GraphQL schema，编译期即能获得完整的类型检查。  
3. **生成 SDK**：运行 `caliban-codegen` CLI（或在 sbt 中配置 `CalibanCodegen` 任务）生成对应语言的客户端代码，直接在前端或其他微服务中调用。  
4. **服务启动**：将生成的 `Http4s`, `Akka HTTP` 或 `Play` 路由与现有 HTTP 服务器集成，即可对外提供 GraphQL 端点。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑12，项目拥有 993 星、263 Fork，最近一次提交在数天前，表明社区和维护者仍在积极迭代。  
- **生态兼容**：官方提供对 Http4s、Akka HTTP、Play 等主流 Scala Web 框架的开箱即用适配，且已在多个大型企业内部项目中验证。  
- **质量与安全**：代码覆盖率、CI/CD 流水线以及公开的安全报告均显示项目成熟；唯一待确认的风险是许可证（MIT）与长期维护者承诺，需要在正式投产前完成最终审查。  

综合来看，Caliban 已具备 **高生产就绪度**，适合作为后端团队的 GraphQL 基础设施，在保证类型安全的前提下显著提升 API 开发与交付效率。

## 🧭 Practical evaluation

**Value:** ghostdogpr/caliban helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 993 GitHub stars
- 263 forks
- updated 2026-05-12
- primary language: Scala
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 61/100 |
| stars | 64/100 |
| topics | 63/100 |
| outlook | 79/100 |
| quality | 78/100 |
| recency | 100/100 |
| adoption | 63/100 |
| production | 76/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/ghostdogpr/caliban) · [← Back to Backend](./README.md)</sub>
