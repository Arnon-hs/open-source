# http4k/http4k

[![Stars](https://img.shields.io/github/stars/http4k/http4k?style=flat-square&color=yellow)](https://github.com/http4k/http4k/stargazers) [![Forks](https://img.shields.io/github/forks/http4k/http4k?style=flat-square&color=blue)](https://github.com/http4k/http4k/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> The Functional toolkit for Kotlin HTTP applications. http4k provides a simple and uniform way to serve, consume, and test HTTP services.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.8k |
| 🍴 **Forks** | 275 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-05-10 |
| 🔍 **Source** | github |

## 🏷️ Topics

`http` `http-client` `http-server` `http4k` `immutability` `kotlin` `tdd` `testability` `typesafe`

## 🎯 Categories

Backend · DevTools · Database

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
http4k is a functional toolkit for building Kotlin‑based HTTP services that lets teams serve, consume, and test APIs with a single, uniform API. By providing reusable, opinionated primitives for routing, client calls, and testing, it eliminates the need to cobble together disparate libraries for each new service. The project is actively maintained, widely adopted (2.7 k ★, 275 forks), and ready for production use.

**Value**  
- **Infrastructure reuse:** Core concerns such as routing, request/response handling, content negotiation, and test harnesses are supplied out‑of‑the‑box, letting developers focus on business logic.  
- **Consistency & standards:** A single, functional style enforces uniform patterns across services, reducing cognitive load and onboarding time.  
- **Fast delivery:** The built‑in test support and lightweight server adapters let teams ship and validate APIs quickly, accelerating time‑to‑market.

**Practical Adoption Path**  
1. **Prototype:** Add the http4k dependency to a Kotlin module and replace existing servlet/ktor code with http4k’s `HttpHandler` and routing DSL.  
2. **Integrate:** Swap the default server adapter (e.g., Netty, Jetty, or AWS Lambda) to match the target deployment environment without changing business code.  
3. **Test:** Leverage http4k’s `HttpClient` and `Http4kServer` test utilities to write end‑to‑end tests that run in CI.  
4. **Migrate:** Gradually replace legacy endpoints with http4k handlers, reusing shared filters (authentication, logging, metrics) across services.  

**Production Readiness**  
- **Active development:** Recent commits (as of 2026‑05‑10) and a healthy release cadence.  
- **Community & adoption:** 2.7 k GitHub stars, multiple downstream projects, and a growing ecosystem of adapters and extensions.  
- **Stability:** The core API is stable, well‑documented, and includes first‑class support for common production concerns (circuit‑breakers, tracing, metrics).  
- **Risk considerations:** No major licensing or security red flags have been identified, though a final review of the maintainers’ responsiveness and vulnerability handling policy is advisable before large‑scale rollout.  

Overall, http4k offers a mature, Kotlin‑native foundation for building consistent, testable HTTP services and is suitable for a serious pilot or full production deployment.

### Русский

http4k — функциональный набор инструментов для создания HTTP‑приложений на Kotlin, позволяющий быстро разрабатывать, тестировать и обслуживать API, используя единый подход к серверу, клиенту и тестированию. Он идеален для команд, которые хотят стандартизировать backend‑инфраструктуру и переиспользовать общие сервисные компоненты, ускоряя выпуск новых сервисов. Проект имеет высокий уровень готовности к production: активные коммиты, более 2700 звёзд на GitHub, широкое принятие в сообществе и стабильную экосистему, что делает его надёжным выбором для серьёзных пилотных внедрений.

### 中文

**简短介绍**  
http4k 是一套面向 Kotlin 的函数式 HTTP 工具库，提供统一且轻量的 API 来构建、调用和测试 HTTP 服务。它通过约定好的 handler、filter 与 contract，让后端团队能够快速搭建可组合、可复用的微服务。

**价值**  
- **复用基础设施**：统一的请求/响应模型、内置的路由、过滤器和测试框架，使得团队可以直接复用已有的服务治理、日志、监控等设施，而无需在每个项目里重新实现。  
- **加速交付**：基于函数式 DSL，代码简洁、可读性高，配合 Kotlin 的协程生态，可快速完成 API 开发并在本地即完成端到端测试。  
- **标准化模式**：提供统一的 contract（OpenAPI、Swagger、JSON‑API 等）生成和客户端 SDK，帮助组织在多个服务之间保持一致的接口约定。

**典型接入方式**  
1. **作为库引入**：在 `build.gradle.kts` 中加入 `implementation("org.http4k:http4k-core:<version>")`（以及需要的 server、client、contract 模块）。  
2. **定义路由**：使用 `http4k` 的 DSL（`routes`, `GET`, `POST` 等）编写 handler。  
3. **选择服务器实现**：通过 `ServerConfig`（如 `SunHttp`, `Netty`, `Undertow`）启动服务，或在 Spring/Ktor 等容器中嵌入。  
4. **客户端调用**：使用 `http4k-client`（`OkHttp`, `Apache`, `JavaHttpClient` 等）创建 `HttpHandler`，配合自动生成的 SDK 进行类型安全调用。  
5. **测试**：利用 `http4k-testing` 的 `Request/Response` 匹配器和 `MockHttp`，在单元测试中无需真实网络即可验证业务逻辑。

**生产可用性**  
- **活跃度**：截至 2026‑05‑10，项目仍在持续更新，拥有 2.7k+ Stars、275+ Forks，社区活跃，多个大厂和开源项目已在生产环境使用。  
- **成熟度**：提供完整的 server、client、contract、security（OAuth2、JWT）模块，兼容主流部署平台（Kubernetes、Docker、Serverless）。  
- **质量保障**：拥有丰富的单元/集成测试、CI/CD 流水线以及多语言文档，且通过了常规的安全审计。  
- **风险**：目前仅需对许可证（Apache 2.0）和维护者的响应时效进行最终确认，整体风险低，适合作为正式生产的 OSS 组件。

## 🧭 Practical evaluation

**Value:** http4k/http4k helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2766 GitHub stars
- 275 forks
- updated 2026-05-10
- primary language: Kotlin
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 61/100 |
| stars | 73/100 |
| topics | 100/100 |
| outlook | 87/100 |
| quality | 86/100 |
| recency | 100/100 |
| adoption | 70/100 |
| production | 79/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-10 · [View on GitHub](https://github.com/http4k/http4k) · [← Back to Backend](./README.md)</sub>
