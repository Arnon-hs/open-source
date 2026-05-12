# AsyncHttpClient/async-http-client

[![Stars](https://img.shields.io/github/stars/AsyncHttpClient/async-http-client?style=flat-square&color=yellow)](https://github.com/AsyncHttpClient/async-http-client/stargazers) [![Forks](https://img.shields.io/github/forks/AsyncHttpClient/async-http-client?style=flat-square&color=blue)](https://github.com/AsyncHttpClient/async-http-client/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> Asynchronous Http and WebSocket Client library for Java

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 6.4k |
| 🍴 **Forks** | 1.6k |
| 💻 **Language** | Java |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ahc` `async` `asynchttpclient` `http-client` `java` `netty`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
AsyncHttpClient (async‑http‑client) is a high‑performance, non‑blocking HTTP and WebSocket client library for Java that lets developers issue requests and handle responses without tying up threads. With over 6 000 GitHub stars and active maintenance, it provides a lightweight, API‑first way to integrate asynchronous networking into any Java application. Its simple Maven/Gradle artifacts and clear SDK make it easy to drop into existing projects or CI pipelines for faster, more reliable HTTP interactions.  

**Value**  
- **Developer productivity:** By offloading I/O to Netty’s event loop, engineers can write concise, callback‑ or CompletableFuture‑based code that eliminates boiler‑plate thread management, shortening development and review cycles.  
- **Automation & CI:** The library’s deterministic, non‑blocking behavior yields faster integration tests and more stable CI feedback, especially for services that depend on external APIs or WebSocket streams.  
- **Cost efficiency:** Reduced thread count and lower latency translate into lower resource consumption in staging and production environments.  

**Practical Adoption Path**  
1. **Evaluate the API:** Pull the latest Maven/Gradle dependency (`org.asynchttpclient:async-http-client`) and prototype a simple GET/POST request in a sandbox module.  
2. **Integrate with existing code:** Replace blocking `HttpURLConnection` or legacy Apache HttpClient calls with `AsyncHttpClient`’s fluent API or CompletableFuture wrappers.  
3. **Add to CI:** Use the client in integration tests that hit mock services (e.g., WireMock) to verify asynchronous handling and measure performance gains.  
4. **Roll out incrementally:** Start with low‑risk services (e.g., internal micro‑service calls) before moving to high‑throughput external APIs or WebSocket connections.  

**Production Readiness**  
- **Activity & Community:** 6 394 stars, 1 590 forks, recent commits (as of 2026‑05‑12), and a vibrant issue/PR community indicate strong momentum.  
- **Stability:** The library follows semantic versioning, provides extensive documentation, and is used by several large‑scale Java projects, suggesting proven stability.  
- **Ecosystem Fit:** Built on Netty, it integrates cleanly with common Java stacks (Spring Boot, Vert.x, Micronaut) and supports both HTTP/1.1 and HTTP/2.  
- **Risks:** No immediate licensing or security red flags, but a final review of the Apache‑2.0 license compliance, vulnerability scans, and maintainer responsiveness is recommended before a full production rollout.  

Overall, AsyncHttpClient is a mature, high‑performance choice for teams seeking to modernize their Java networking layer and accelerate development pipelines.

### Русский

AsyncHttpClient (async‑http‑client) — это высокопроизводительная асинхронная библиотека для работы с HTTP и WebSocket в Java, позволяющая ускорить разработку, автоматизировать локальные задачи и получать быстрый фидбэк в CI‑процессах. Проект уже доказал свою готовность к продакшну: активные коммиты, более 6 000 звёзд, 1 590 форков и широкое принятие в экосистеме, что делает его надёжным кандидатом для пилотного внедрения в микросервисные или реактивные системы. Оценка готовности — высокая, однако перед масштабным использованием следует окончательно проверить лицензию, безопасность и наличие активных мейнтейнеров.

### 中文

**项目简介（2‑3 句）**  
AsyncHttpClient（`async-http-client`）是基于 Netty 实现的高性能异步 HTTP 与 WebSocket 客户端库，提供全异步、非阻塞的请求/响应模型，帮助 Java 开发者在微服务、爬虫、实时推送等场景下快速完成网络交互。

**价值**  
- **提升开发效率**：统一的 API 抽象、丰富的配置选项，让编写并发请求和 WebSocket 通信变得简洁，显著缩短调试和代码审查周期。  
- **加速 CI/CD 反馈**：在自动化测试、性能基准和集成流水线中使用，可并行发起大量请求，快速获取接口可用性与响应时延。  
- **降低运维成本**：基于 Netty 的零阻塞 I/O，资源占用低，适配高并发场景，减少对额外代理或负载均衡层的依赖。

**典型接入方式**  
1. **Maven/Gradle 依赖**：在项目的 `pom.xml` 或 `build.gradle` 中加入 `org.asynchttpclient:async-http-client`。  
2. **代码层面**：通过 `AsyncHttpClientConfig` 定制连接池、超时、SSL 等参数，随后使用 `asyncHttpClient.prepareGet/preparePost/...` 构造请求并调用 `execute()` 获得 `ListenableFuture` 或 `CompletableFuture`。  
3. **CLI/SDK**：库本身提供了 `AsyncHttpClient` 实例，可直接在脚本或测试框架中调用，无需额外的运行时服务。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑12，项目仍在持续更新，拥有 6 400+ 星、1 600+ Fork，最近一次提交仅数天前。  
- **生态采纳**：被多个大型微服务平台和爬虫框架引用，社区贡献活跃，Issue 处理及时。  
- **成熟度**：基于成熟的 Netty 核心，提供完整的异常捕获、连接池管理和 TLS 支持，已在高并发生产环境中验证。  
- **风险**：暂无重大许可证或安全漏洞报告，但仍建议在正式投产前完成一次依赖审计和安全扫描，确认维护者响应速度符合贵公司 SLA。  

综上，AsyncHttpClient 是一个高性能、易集成且已具备生产级别成熟度的 Java 异步网络库，适合作为日常开发、自动化测试以及 CI 流水线的网络交互基础组件。

## 🧭 Practical evaluation

**Value:** AsyncHttpClient/async-http-client helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 6394 GitHub stars
- 1590 forks
- updated 2026-05-12
- primary language: Java
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 80/100 |
| stars | 81/100 |
| topics | 75/100 |
| outlook | 84/100 |
| quality | 88/100 |
| recency | 100/100 |
| adoption | 81/100 |
| production | 79/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/AsyncHttpClient/async-http-client) · [← Back to DevTools](./README.md)</sub>
