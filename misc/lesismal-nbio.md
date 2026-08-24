# lesismal/nbio

[![Stars](https://img.shields.io/github/stars/lesismal/nbio?style=flat-square&color=yellow)](https://github.com/lesismal/nbio/stargazers) [![Forks](https://img.shields.io/github/forks/lesismal/nbio?style=flat-square&color=blue)](https://github.com/lesismal/nbio/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> Pure Go 1000k+ connections solution, support tls/http1.x/websocket and basically compatible with net/http, with high-performance and low memory cost, non-blocking, event-driven, easy-to-use.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.7k |
| 🍴 **Forks** | 180 |
| 💻 **Language** | Go |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The **lesismal/nbio** library is a pure‑Go, event‑driven networking framework that can handle more than a million concurrent connections while supporting TLS, HTTP/1.x, and WebSocket. It offers a non‑blocking API that is largely compatible with the standard `net/http` package, delivering high throughput with low memory overhead.  

**Value Proposition**  
- **Performance & Scalability** – By using a non‑blocking, epoll/kqueue‑based event loop, nbio can serve hundreds of thousands to millions of simultaneous connections on modest hardware, making it ideal for real‑time services, chat servers, streaming APIs, or any workload that must maintain many long‑lived sockets.  
- **Ease of Integration** – The API mirrors `net/http` (e.g., `http.Handler`, `http.Server`), so existing Go code can be migrated with minimal rewrites while gaining the performance benefits of an event‑driven model.  
- **Feature Set** – Built‑in TLS termination, HTTP/1.x parsing, and WebSocket handling eliminate the need for separate libraries, reducing the overall dependency footprint.  

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | **Prototype** – Spin up a small PoC using nbio’s `Server` wrapper around an existing `http.Handler`. Measure latency and connection‑count limits against the current net/http implementation. | Validates performance claims on your workload without committing to a full migration. |
| 2️⃣  | **Code Review & Security Scan** – Run static analysis (e.g., `go vet`, `staticcheck`) and dependency‑vulnerability tools (e.g., `govulncheck`). Review the license (MIT‑style) and confirm it aligns with your policy. | Ensures no hidden security or licensing issues before deeper integration. |
| 3️⃣  | **Integration Layer** – Replace the production `http.Server` with nbio’s server in a staging environment. Keep the same handler signatures; only the server bootstrap changes. | Demonstrates drop‑in compatibility while exposing any edge‑case differences (e.g., request timeouts, connection hijacking). |
| 4️⃣  | **Load Testing** – Use tools like `hey`, `wrk`, or custom Go benchmarks to simulate the target connection count (e.g., 100k‑1M). Capture CPU, memory, and GC metrics. | Confirms that the claimed low‑memory, high‑throughput characteristics hold under realistic traffic. |
| 5️⃣  | **Observability Hook‑up** – Instrument nbio’s event loop with Prometheus metrics or OpenTelemetry (the library exposes connection counters). | Provides visibility for ongoing ops and helps detect regressions after deployment. |
| 6️⃣  | **Gradual Rollout** – Deploy the nbio‑backed service to a canary or subset of traffic, monitor error rates and latency, then expand. | Reduces risk; allows quick rollback to the standard net/http server if needed. |

**Production Readiness Assessment**  

| Dimension | Rating | Comments |
|-----------|--------|----------|
| **Stability** | ★★☆☆☆ (Medium) | The project is actively maintained (last commit 2026‑07‑03) and has a solid star count (≈2.7k), but the documentation and integration examples are sparse, requiring careful code review. |
| **Performance** | ★★★★☆ | Benchmarks and community reports indicate excellent scalability for high‑connection workloads. |
| **Security** | ★★☆☆☆ | No known CVEs, but the repository lacks a formal security policy and automated vulnerability scanning; you’ll need to run your own checks. |
| **Maintainability** | ★★☆☆☆ | Small contributor base (≈180 forks) and limited issue triage; ensure you have an internal fallback plan if the maintainer steps away. |
| **Ecosystem Fit** | ★★★☆☆ | Works well for services that need raw socket handling or WebSockets; less relevant for pure data‑persistence use‑cases. |
| **Overall** | **Medium** – Suitable for prototypes, internal tools, or services where connection density is a primary concern, **provided** you perform the due‑diligence steps above and have a plan for long‑term maintenance. |

**Bottom Line**  
If your team needs to serve a massive number of concurrent HTTP/WebSocket connections with low latency and memory usage, nbio offers a compelling, Go‑native alternative to traditional blocking servers. Adopt it first in a controlled prototype, validate performance and security, and only promote to production after thorough testing and observability integration. With those safeguards in place, nbio can be a reliable component of a high‑scale Go microservice stack.

### Русский

**lesismal/nbio** — это высокопроизводительная, неблокирующая библиотека на чистом Go, позволяющая обслуживать более 1000 тыс. одновременных соединений (TLS, HTTP/1.x, WebSocket) с низким потреблением памяти и совместимостью почти со стеком `net/http`. Она подходит для прототипов и внутренних сервисов, где требуется быстрый и лёгкий ввод‑вывода без лишних зависимостей, однако перед запуском в продакшн стоит проверить лицензию, безопасность и активность поддержки. При надлежащей проверке проект может стать надёжным решением для масштабируемой сетевой и веб‑инфраструктуры.

### 中文

**项目简介（2‑3 句）**  
lesismal/nbio 是一款纯 Go 实现的高性能网络库，能够轻松支撑 1000k+ 并发连接，兼容 net/http，内置 TLS、HTTP/1.x 与 WebSocket，采用非阻塞、事件驱动模型，内存占用极低、使用门槛低。

**价值**  
- **极致并发**：在单机上即可处理上百万连接，适合高并发服务、实时推送、游戏服务器等场景。  
- **低资源消耗**：非阻塞、零拷贝设计，使 CPU 与内存开销远低于传统 net/http 实现。  
- **易集成**：API 与 net/http 接口基本兼容，迁移或混用成本几乎为零。  

**典型接入方式**  
```go
import "github.com/lesismal/nbio/nbhttp"

func main() {
    // 与 net/http Handler 完全兼容
    http.HandleFunc("/", func(w http.ResponseWriter, r *http.Request) {
        fmt.Fprintln(w, "Hello, nbio!")
    })

    // 启动 nbio 服务器（支持 TLS、WebSocket 等）
    nbhttp.ListenAndServeTLS(":443", "cert.pem", "key.pem", nil)
}
```
- 将现有的 `http.Handler` 直接传给 `nbhttp.ListenAndServe*` 即可；  
- 如需 WebSocket，可使用 `github.com/lesismal/nbio/nbhttp/websocket` 包，方式与 Gorilla/WebSocket 类似。  

**生产可用性**  
- **成熟度**：GitHub ★2749，近期仍在更新（截至 2026‑07‑03），社区活跃度中等。  
- **适用场景**：适合内部系统、原型、对并发有极致要求的服务；在正式生产环境使用前建议：  
  1. **安全审计**：检查 TLS 配置、依赖的第三方库安全性。  
  2. **性能基准**：在目标硬件上跑压测，确认内存/CPU 与业务需求匹配。  
  3. **维护计划**：确认项目维护者活跃度或自行 Fork 维护。  
- **风险**：元数据较少，集成文档不够完整；需自行验证与现有监控、日志体系的兼容性。  

总体而言，nbio 在需要极高并发且对资源占用敏感的 Go 项目中具备显著优势，只要做好安全与运维审查，即可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** lesismal/nbio helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 2749 GitHub stars
- 180 forks
- updated 2026-07-03
- primary language: Go

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 56/100 |
| stars | 73/100 |
| topics | 0/100 |
| outlook | 50/100 |
| quality | 56/100 |
| recency | 40/100 |
| adoption | 69/100 |
| production | 53/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/lesismal/nbio) · [← Back to Misc](./README.md)</sub>
