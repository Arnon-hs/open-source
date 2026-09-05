# d-kuro/kirocc

[![Stars](https://img.shields.io/github/stars/d-kuro/kirocc?style=flat-square&color=yellow)](https://github.com/d-kuro/kirocc/stargazers) [![Forks](https://img.shields.io/github/forks/d-kuro/kirocc?style=flat-square&color=blue)](https://github.com/d-kuro/kirocc/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> A local proxy server that relays Anthropic Messages API-compatible requests to the Kiro (Amazon Q) backend using Kiro CLI credentials.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 32 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | Go |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anthropic` `claude` `claude-code` `go` `kiro`

## 🎯 Categories

AI/ML · Networking · Backend

## 📝 Summary

### English

**Brief Summary**  
`d-kuro/kirocc` is a Go‑based local proxy that translates Anthropic‑compatible Messages API calls into the Kiro (Amazon Q) backend, using credentials supplied via the Kiro CLI. It lets teams reuse an existing Kiro deployment instead of building a custom Anthropic‑style service layer from scratch.

**Value**  
- **Infrastructure reuse** – By sitting in front of Kiro, the proxy eliminates the need to duplicate authentication, rate‑limiting, and request‑routing logic for each new Anthropic‑compatible service.  
- **Speed to market** – Teams can ship an API that speaks the familiar Anthropic Messages schema in minutes, accelerating prototype and internal‑tool development.  
- **Standardisation** – Because the proxy enforces a single request/response shape, downstream services adopt a consistent pattern, reducing bugs and onboarding friction.

**Practical Adoption Path**  
1. **Provision Kiro** – Ensure an Amazon Q (Kiro) instance is running and that the Kiro CLI is installed and authenticated for the target account.  
2. **Deploy the proxy** – Clone the repo, run `go build` (or use the provided Dockerfile) and start the binary, pointing it at the Kiro endpoint via environment variables (`KIRO_ENDPOINT`, `KIRO_TOKEN`, etc.).  
3. **Redirect clients** – Point existing Anthropic‑compatible SDKs or HTTP clients to the proxy’s host/port. No code changes are needed on the client side.  
4. **Add observability** – Hook up logging, metrics, or a side‑car API‑gateway if you need request tracing or rate limiting beyond what Kiro provides.  
5. **Iterate** – For production, consider adding TLS termination, CI‑driven image rebuilds, and a health‑check endpoint.

**Production Readiness**  
- **Maturity** – Medium. The project is actively maintained (last commit 2026‑07‑01), has 32 ⭐ and 4 🍴, and is written in Go, which is well‑suited for low‑latency proxies.  
- **What’s still needed**  
  * **Security review** – Verify the license, audit the handling of Kiro credentials, and ensure TLS is enforced in deployment.  
  * **Reliability** – Add health checks, graceful shutdown, and circuit‑breaker logic if the Kiro backend becomes unavailable.  
  * **Observability** – Export metrics (e.g., Prometheus) and logs to your monitoring stack.  
  * **Ops tooling** – Containerise the binary, pin a specific version tag, and include it in your CI/CD pipeline.  

With these checks in place, `d-kuro/kirocc` is a solid foundation for internal prototypes and can be hardened for production use where the benefits of reusing Kiro outweigh the modest additional operational overhead.

### Русский

**d-kuro/kirocc** — это локальный прокси‑сервер на Go, который принимает запросы в формате Anthropic Messages API и пересылает их в бекенд Kiro (Amazon Q) с использованием учётных данных Kiro CLI. Проект упрощает быстрый запуск API‑сервисов, позволяя командам повторно использовать существующую инфраструктуру вместо создания собственного бэкенда, и подходит для прототипов или внутренних workflow‑ов, требующих стандартизированных паттернов доступа к Kiro. Готовность к production — средняя: код стабилен (32★, 4 forks, обновлён 01‑07‑2026), но перед выводом в продакшн рекомендуется проверить лицензию, безопасность зависимостей и наличие активных мейнтейнеров.

### 中文

**d-kuro/kirocc 简介**

d-kuro/kirocc 是一个本地代理服务器，通过 Kiro CLI 凭据将 Anthropic Messages API 兼容的请求转发到 Kiro (Amazon Q) 后端。它可以帮助团队重用服务基础设施，而不是重建常见的后端组件。

**价值**

d-kuro/kirocc 帮助团队重用服务基础设施，减少重复工作，提高开发效率。它可以帮助团队快速部署 API 服务，并标准化服务模式。

**典型接入方式**

1. 克隆 d-kuro/kirocc 项目到你的本地机器。
2. 配置 Kiro CLI 凭据。
3. 使用 d-kuro/kirocc 作为代理服务器，将请求转发到 Kiro (Amazon Q) 后端。

**生产可用性**

d-kuro/kirocc 的生产可用性为中等（Medium）。它适合用于原型开发或内部工作流程，但在生产环境中需要进行依赖和维护检查。

## 🧭 Practical evaluation

**Value:** d-kuro/kirocc helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 32 GitHub stars
- 4 forks
- updated 2026-07-01
- primary language: Go
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 32/100 |
| topics | 63/100 |
| outlook | 66/100 |
| quality | 57/100 |
| recency | 80/100 |
| adoption | 28/100 |
| production | 68/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/d-kuro/kirocc) · [← Back to AI/ML](./README.md)</sub>
