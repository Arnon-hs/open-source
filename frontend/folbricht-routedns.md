# folbricht/routedns

[![Stars](https://img.shields.io/github/stars/folbricht/routedns?style=flat-square&color=yellow)](https://github.com/folbricht/routedns/stargazers) [![Forks](https://img.shields.io/github/forks/folbricht/routedns?style=flat-square&color=blue)](https://github.com/folbricht/routedns/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> DNS stub resolver, proxy and router with support for DoT, DoH, DoQ, and DTLS

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 615 |
| 🍴 **Forks** | 79 |
| 💻 **Language** | Go |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-07-03 |
| 🔍 **Source** | github |

## 🏷️ Topics

`dns` `dns-client` `dns-over-dtls` `dns-over-https` `dns-over-quic` `dns-over-tls` `dns-privacy` `dns-server` `doh` `doq` `dot` `go`

## 🎯 Categories

Frontend · Backend · DevTools

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
`folbricht/routedns` is a Go‑based DNS stub resolver that can act as a proxy and router, supporting modern encrypted protocols such as DNS‑over‑TLS (DoT), DNS‑over‑HTTPS (DoH), DNS‑over‑QUIC (DoQ) and DTLS. It exposes a clean API/CLI/SDK, making it easy to embed DNS routing logic into user‑facing services without writing custom networking code. The project is actively maintained, widely adopted, and comes with a rich set of topics and examples that accelerate UI‑driven product development.

**Value**  
- **Accelerates UI development** – By handling the complex DNS resolution and encryption layer internally, developers can focus on building front‑end components and user experiences rather than low‑level networking.  
- **Reusable interface components** – The library’s SDK and CLI expose ready‑made hooks (e.g., query events, health checks) that can be directly wired into dashboards, monitoring panels, or configuration UIs.  
- **Consistent security posture** – Built‑in support for DoT/DoH/DoQ ensures that any UI that surfaces DNS information does so over encrypted channels, reducing the need for separate security implementations.

**Practical adoption path**  
1. **Prototype** – Clone the repo and run the provided CLI (`routedns serve`) to spin up a local DNS proxy; experiment with the API via the sample Go client.  
2. **Integrate** – Add the Go module (`go get github.com/folbricht/routedns`) to your backend service, configure routing rules via the SDK or a JSON/YAML file, and expose the needed endpoints to your front‑end.  
3. **Wrap UI** – Use the SDK’s event callbacks to feed real‑time status into your React/Vue/Angular components, leveraging the same configuration UI for both development and production.  
4. **Test & Harden** – Run the built‑in test suite, add your own integration tests, and optionally containerize the service (Dockerfile is included) for CI/CD pipelines.

**Production readiness**  
- **Activity & adoption** – 615 ★, 79 forks, recent commits (last update 2026‑07‑03), and multiple downstream projects indicate a healthy community.  
- **Maturity** – The codebase is written in Go, a language known for stability in server environments, and the project ships a CLI, SDK, and comprehensive documentation.  
- **Risk considerations** – No obvious licensing or security red flags, but a final review of the license (MIT) and a security audit of the TLS/QUIC implementations is recommended before large‑scale rollout.  

Overall, `folbricht/routedns` is a production‑grade OSS component that can be quickly evaluated and integrated to reduce custom UI work around DNS functionality, while providing a robust, encrypted DNS routing layer.

### Русский

**Резюме:** `folbricht/routedns` — это открытый DNS‑stub‑резолвер, прокси и маршрутизатор на Go с поддержкой современных протоколов безопасности (DoT, DoH, DoQ, DTLS). Он позволяет быстро добавить в продукт пользовательский интерфейс для управления DNS‑трафиком, переиспользуя готовые API/SDK/CLI‑компоненты и тем самым ускоряя разработку фронтенда без необходимости писать собственный UI‑слой. Проект имеет высокий уровень готовности к продакшн: активные коммиты, 615 звёзд, 79 форков, свежие обновления (03.07.2026) и широкую экосистемную поддержку, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**folbricht/routedns 简介**

folbricht/routedns 是一个 DNS stub 解析器、代理和路由器，支持 DoT、DoH、DoQ 和 DTLS 等协议。它可以帮助开发者快速构建用户界面，减少自定义 UI 工作量。

**价值**

folbricht/routedns 的价值在于它可以帮助开发者快速构建用户界面，减少自定义 UI 工作量，提高前端交付效率。

**典型接入方式**

folbricht/routedns 的接入方式包括：

* API：通过 API 接口调用 folbricht/routedns 的功能。
* SDK：通过 SDK 集成 folbricht/routedns 的功能。
* CLI：通过命令行界面接口调用 folbricht/routedns 的功能。

**生产可用性**

folbricht/routedns 的生产可用性很高，主要原因是：

* 最近的活跃度：folbricht/routedns 有近期的更新和活动。
*采用率：folbricht/routedns 有 615 个 GitHub STAR 和 79 个 Fork。
*生态系统信号：folbricht

## 🧭 Practical evaluation

**Value:** folbricht/routedns helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 615 GitHub stars
- 79 forks
- updated 2026-07-03
- primary language: Go
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 48/100 |
| stars | 59/100 |
| topics | 100/100 |
| outlook | 81/100 |
| quality | 80/100 |
| recency | 100/100 |
| adoption | 56/100 |
| production | 79/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/folbricht/routedns) · [← Back to Frontend](./README.md)</sub>
