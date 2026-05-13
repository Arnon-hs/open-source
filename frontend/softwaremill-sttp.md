# softwaremill/sttp

[![Stars](https://img.shields.io/github/stars/softwaremill/sttp?style=flat-square&color=yellow)](https://github.com/softwaremill/sttp/stargazers) [![Forks](https://img.shields.io/github/forks/softwaremill/sttp?style=flat-square&color=blue)](https://github.com/softwaremill/sttp/network) [![Language](https://img.shields.io/badge/lang-Scala-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> The Scala HTTP client you always wanted!

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.5k |
| 🍴 **Forks** | 331 |
| 💻 **Language** | Scala |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`akka-http` `asynchronous` `cats` `client` `distributed-tracing` `http` `http-client` `httpclient` `interpolator` `monix` `okhttp` `reactive-streams`

## 🎯 Categories

Frontend · DevTools · Observability

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
softwaremill/sttp is a Scala‑based HTTP client that lets developers build user‑facing interfaces with minimal boiler‑plate networking code. Its clean, type‑safe API and extensive ecosystem make it easy to integrate into existing Scala front‑end stacks, accelerating UI development and component reuse. With strong community adoption (1.5 k stars, 331 forks) and active maintenance, it is a solid candidate for production use.

**Value**  
- **Developer productivity:** Provides a high‑level, type‑safe abstraction over HTTP, eliminating repetitive request/response handling and reducing UI‑related networking bugs.  
- **Component reuse:** Because the client is declarative and composable, the same request definitions can be shared across different UI modules or micro‑services, speeding up product UI delivery.  
- **Observability & tooling:** Built‑in support for logging, metrics, and tracing integrates smoothly with existing observability stacks, giving teams insight into API performance without extra boilerplate.

**Practical Adoption Path**  
1. **Prototype:** Add the `sttp-client3` dependency to a sandbox Scala project and replace low‑level `java.net` or `Akka‑http` calls with the STTP DSL.  
2. **Integrate:** Wrap the client in a thin service layer that matches your UI’s data‑access contracts; this isolates STTP from the rest of the codebase and eases future swaps.  
3. **Test & Observe:** Leverage STTP’s built‑in test back‑ends (e.g., `SttpBackendStub`) to write unit tests, and enable its logging/metrics adapters to feed data into your existing observability platform.  
4. **Roll‑out:** Deploy the updated service to a staging environment, monitor latency and error rates, then gradually promote to production via feature flags or canary releases.

**Production Readiness**  
- **Activity & Community:** Recent commits (as of 2026‑05‑13), a healthy star/fork count, and 18 related topics indicate an active, well‑maintained project.  
- **Maturity:** The library has been used in multiple production Scala applications, and its API is stable with semantic versioning guarantees.  
- **Risk Assessment:** No major metadata or licensing concerns have been identified, though a final security audit and confirmation of maintainers’ responsiveness are advisable before a full‑scale rollout.  

Overall, sttp offers a mature, well‑documented solution for Scala front‑end teams seeking to streamline HTTP interactions, with a clear, low‑friction path from evaluation to production deployment.

### Русский

**softwaremill/sttp** — это высокоуровневый HTTP‑клиент для Scala, который упрощает построение пользовательских интерфейсов, позволяя быстро интегрировать готовые API‑запросы без написания собственного сетевого кода. Типичный сценарий — разработчики фронтенда используют sttp в микросервисных UI‑приложениях, переиспользуя компоненты запросов и ускоряя доставку продукта. Проект считается готовым к production: активные коммиты, 1500+ звёзд, широкое принятие в сообществе и стабильный стек технологий, хотя окончательная проверка лицензии и безопасности всё же требуется.

### 中文

**项目简介**  
softwaremill/sttp 是一款基于 Scala 的 HTTP 客户端库，旨在让开发者以声明式、类型安全的方式发送请求、解析响应，从而快速构建用户界面层的后端交互。它提供统一的 API、丰富的插件体系（如 async、circe、play‑json 等），帮助团队在前端交付时省去大量自研网络请求代码。

**价值点**  
- **提升开发效率**：统一的请求 DSL 与自动的响应解码，使 UI 开发者可以专注业务逻辑，而不必在每个页面手写繁琐的 HTTP 代码。  
- **可复用的接口组件**：通过抽象的 `SttpBackend`，同一套请求实现可以在服务端、CLI、测试甚至浏览器（Scala.js）中复用，保证前后端接口的一致性。  
- **可靠的交付**：类型安全的请求/响应模型在编译期捕获错误，降低运行时异常，提升前端交付的质量与可维护性。

**典型接入方式**  
1. **在项目中加入依赖**（sbt 示例）  
   ```scala
   libraryDependencies += "com.softwaremill.sttp.client3" %% "core" % "3.9.0"
   ```
2. **创建 Backend**（可选 async、sync、Scala.js 等）  
   ```scala
   import sttp.client3._
   implicit val backend = HttpURLConnectionBackend()
   ```
3. **编写请求并发送**  
   ```scala
   val request = basicRequest
     .get(uri"https://api.example.com/users")
     .response(asJson[List[User]])

   val response = request.send()
   response.body match {
     case Right(users) => // 正常处理
     case Left(error)  => // 错误处理
   }
   ```
4. **在测试或多环境中切换 Backend**：使用 `StubBackend`、`AsyncHttpClientBackend` 等实现即可，无需改动业务代码。

**生产可用性**  
- **活跃度**：近 1500 星、300+ Fork，最近一次提交在 2026‑05‑13，社区活跃。  
- **生态兼容**：支持多种后端实现（JVM、Scala.js、Native），并提供与主流 JSON 库、认证框架的集成插件。  
- **稳定性**：已在多个大型 Scala 项目中上线，具备成熟的错误处理与重试机制。  
- **风险**：目前未发现重大许可证或安全漏洞，但仍建议在正式投产前完成许可证合规审查和安全依赖扫描。

综上，softwaremill/sttp 具备高可用的技术成熟度和丰富的集成选项，是在 Scala 前端/微服务项目中快速构建可靠 HTTP 接口的理想选择。

## 🧭 Practical evaluation

**Value:** softwaremill/sttp helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1504 GitHub stars
- 331 forks
- updated 2026-05-13
- primary language: Scala
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 63/100 |
| stars | 68/100 |
| topics | 100/100 |
| outlook | 83/100 |
| quality | 85/100 |
| recency | 100/100 |
| adoption | 66/100 |
| production | 78/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/softwaremill/sttp) · [← Back to Frontend](./README.md)</sub>
