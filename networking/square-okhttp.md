# square/okhttp

[![Stars](https://img.shields.io/github/stars/square/okhttp?style=flat-square&color=yellow)](https://github.com/square/okhttp/stargazers) [![Forks](https://img.shields.io/github/forks/square/okhttp?style=flat-square&color=blue)](https://github.com/square/okhttp/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> Square’s meticulous HTTP client for the JVM, Android, and GraalVM.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 47k |
| 🍴 **Forks** | 9.3k |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `graalvm` `java` `kotlin`

## 🎯 Categories

Networking · Mobile

## 📝 Summary

### English

**Summary:** Square's OkHttp is an open-source, meticulous HTTP client for the JVM, Android, and GraalVM, designed to streamline development workflows and accelerate local engineering tasks. Its robust ecosystem, high adoption rate, and recent activity make it a reliable choice for production environments. With its straightforward integration process, developers can easily evaluate and leverage OkHttp to improve their CI feedback and automate tasks.

**Value:** The primary value proposition of OkHttp lies in saving engineers time in daily development and review loops. By automating local engineering tasks and improving CI feedback, developers can focus on higher-level tasks, increasing productivity and reducing the overall development time.

**Practical Adoption Path:**

1. **Evaluation:** OkHttp exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics, making it straightforward to evaluate its suitability for your project.
2. **Integration:** Developers can easily integrate OkHttp into their existing infrastructure, taking advantage of its robust ecosystem and high adoption rate.
3. **Implementation:** With its recent activity, updated codebase, and strong community support, OkHttp provides a solid foundation for production-ready applications.

**Production Readiness:** OkHttp has a high production readiness score, thanks to its recent activity, strong adoption rate, and robust ecosystem. Its primary

### Русский

**square/okhttp** — это проверенный HTTP‑клиент от Square, написанный на Kotlin и поддерживающий JVM, Android и GraalVM. Он ускоряет разработку, позволяя быстро интегрировать надёжные сетевые запросы в мобильные и серверные приложения, а также автоматизировать локальные задачи и улучшать обратную связь в CI. Проект демонстрирует высокий уровень готовности к продакшн: активные коммиты, более 46 тыс. звёзд, широкое принятие в индустрии и стабильную экосистему, что делает его безопасным кандидатом для пилотного внедрения.

### 中文

**项目简介**  
Square 的 OkHttp 是一款为 JVM、Android 以及 GraalVM 量身打造的高性能 HTTP 客户端，代码简洁、功能完善，已被数千个开源项目和企业级系统广泛采用。

**价值**  
- **提升开发效率**：统一、可靠的 API 让网络请求的编写、调试和单元测试变得极其轻松，显著缩短日常开发和代码审查的循环时间。  
- **加速工作流**：配合拦截器、异步调用和连接池等特性，可在本地快速模拟后端服务、自动化集成测试，从而提升 CI 反馈速度。  
- **可靠的生产支撑**：成熟的错误恢复、重试、超时控制和 HTTP/2、WebSocket 支持，使其在高并发、移动端和微服务场景下表现稳健。

**典型接入方式**  
1. **Gradle / Maven 依赖**  
   ```groovy
   implementation "com.squareup.okhttp3:okhttp:4.12.0"
   ```
2. **创建 OkHttpClient 实例**（可全局复用）  
   ```kotlin
   val client = OkHttpClient.Builder()
       .connectTimeout(10, TimeUnit.SECONDS)
       .readTimeout(30, TimeUnit.SECONDS)
       .addInterceptor(LoggingInterceptor())
       .build()
   ```
3. **发起请求**（同步或异步）  
   ```kotlin
   val request = Request.Builder()
       .url("https://api.example.com/data")
       .get()
       .build()

   // 同步
   client.newCall(request).execute().use { response -> … }

   // 异步
   client.newCall(request).enqueue(object : Callback { … })
   ```
4. **高级特性**：使用 `ConnectionPool`、`Cache`、`Authenticator`、`WebSocketListener` 等实现缓存、身份验证和实时通信。

**生产可用性**  
- **活跃度**：截至 2026‑06‑28，项目最近有提交，拥有 46,993 个 Star、9,271 个 Fork，社区活跃度高。  
- **语言与生态**：主要使用 Kotlin 编写，兼容 Java，支持 Android、Spring Boot、Ktor 等常见框架，且在 GraalVM 上可原生编译。  
- **质量与安全**：拥有完整的单元测试、CI/CD 流程以及公开的安全报告；License 为 Apache‑2.0，商业使用无障碍。  
- **风险**：需在正式投产前完成许可证合规审查、依赖漏洞扫描以及维护者响应时效的二次确认。

综合来看，OkHttp 已具备 **高生产就绪度**，适合作为内部或外部服务的默认 HTTP 客户端，并可快速投入到 CI/CD 流程和移动端项目中。

## 🧭 Practical evaluation

**Value:** square/okhttp helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 46993 GitHub stars
- 9271 forks
- updated 2026-06-28
- primary language: Kotlin
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 99/100 |
| stars | 99/100 |
| topics | 50/100 |
| outlook | 79/100 |
| quality | 87/100 |
| recency | 80/100 |
| adoption | 99/100 |
| production | 74/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/square/okhttp) · [← Back to Networking](./README.md)</sub>
