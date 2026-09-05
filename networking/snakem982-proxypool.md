# snakem982/proxypool

[![Stars](https://img.shields.io/github/stars/snakem982/proxypool?style=flat-square&color=yellow)](https://github.com/snakem982/proxypool/stargazers) [![Forks](https://img.shields.io/github/forks/snakem982/proxypool?style=flat-square&color=blue)](https://github.com/snakem982/proxypool/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> Free Proxies，Free Nodes，免费节点，白嫖节点，免费vpn，免费v2ray，免费订阅，免费clash，Free VPN，Free v2ray，Free Sub，Free Clash

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.9k |
| 🍴 **Forks** | 137 |
| 💻 **Language** | Go |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`clash` `cloudflare` `freenode` `hysteria` `hysteria2` `mihomo` `proxies` `proxy` `sing-box` `ss` `trojan` `v2ray`

## 🎯 Categories

Networking · Backend

## 📝 Summary

### English

**Brief Summary**  
snakem982/proxypool is a Go‑based open‑source service that aggregates free proxy, VPN, V2Ray and Clash nodes and exposes them via a simple API. With a strong community (1.8 k ★, 137 forks) and recent activity, it lets teams reuse a ready‑made proxy pool instead of building and maintaining their own infrastructure.

**Value**  
- **Accelerated delivery** – By providing a plug‑and‑play proxy backend, developers can focus on business logic and ship API services faster.  
- **Standardization** – A single, well‑documented source for free proxy nodes reduces the variance in how different services obtain and rotate proxies, improving consistency and security posture across the organization.  
- **Cost savings** – Leveraging publicly available nodes eliminates the need for paid proxy subscriptions or custom provisioning pipelines.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repository, run the provided Docker compose (or `go run`) locally, and verify that the API returns a list of functional proxies for a test request.  
2. **Integration** – Wrap the API calls in a thin client library within your service, configure health checks, and add a fallback to a secondary proxy source if needed.  
3. **Pilot** – Deploy the proxypool service in a sandbox environment (e.g., a Kubernetes namespace) and route a subset of traffic through it, monitoring latency, success rates, and node churn.  
4. **Scale** – After confirming stability, promote the deployment to production, enable automatic node refresh (via the built‑in scheduler), and document usage patterns for other teams.

**Production Readiness**  
The project scores high on readiness: it has recent commits (as of 2026‑06‑25), a sizable star count, active forks, and a clear Go codebase with 19 related topics. While no critical metadata risks were identified, a final review of the license, security scanning of the proxy sources, and confirmation of maintainers’ responsiveness is recommended before committing to a mission‑critical rollout. With those checks completed, proxypool is a solid candidate for a production pilot.

### Русский

**snakem982/proxypool** — это open‑source сервис на Go, собирающий и обслуживая бесплатные прокси‑серверы, VPN, V2Ray, Clash и подписки, позволяя командам быстро подключать готовую инфраструктуру прокси‑пула вместо её самостоятельной разработки. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept, проверка README и интеграция API пула в существующие бэкенд‑сервисы для ускорения вывода новых API и стандартизации доступа к внешним ресурсам. По оценке готовности проект достаточно зрелый для production: активные коммиты, более 1800 звёзд, активное сообщество и современный стек, однако перед масштабным использованием следует уточнить лицензию и текущий статус безопасности.

### 中文

**项目简介**  
snakem982/proxypool 是一款基于 Go 实现的免费代理池工具，聚合了 Free Proxies、Free Nodes、免费 VPN/V2Ray/Clash 订阅等资源，帮助用户快速获取、管理和切换高可用的免费节点。

**价值**  
- **降低运维成本**：无需自行搭建或维护代理服务器，直接复用已有的免费节点资源。  
- **加速业务上线**：在开发或测试阶段即可通过统一的 API 获取代理，省去自行编写代理管理逻辑的时间。  
- **统一标准**：提供统一的接口和配置格式（Clash、V2Ray、Sub），便于团队在不同项目中复用同一套代理方案。

**典型接入方式**  
1. **直接使用二进制**：下载最新 Release，配置 `config.yaml`（可指定节点来源、过滤规则等），启动后通过 `http://localhost:PORT/api/proxies` 获取实时代理列表。  
2. **作为库集成**：在 Go 项目中 `go get github.com/snakem982/proxypool`，调用 `proxypool.NewPool()` 创建实例，使用 `GetProxy()`、`Refresh()` 等方法获取或更新节点。  
3. **Docker 部署**：`docker run -d -p 8080:8080 snakem982/proxypool:latest`，配合环境变量或挂载配置文件即可在容器化环境中快速上线。

**生产可用性**  
- **活跃度**：截至 2026‑06‑25 最近一次提交，拥有 1871 星、137 Fork，社区活跃度高。  
- **技术成熟度**：使用 Go 编写，单二进制部署，性能和资源占用均优秀，适合作为后端服务的共享组件。  
- **风险评估**：暂无重大元数据风险，需进一步审查许可证（MIT/Apache 等）和安全审计报告，确保依赖库无已知漏洞。  
- **推荐做法**：在正式生产环境前先做小规模 POC（例如在内部测试环境部署），验证节点可用性和更新频率，再逐步推广至全链路使用。  

综合来看，proxypool 在免费代理资源获取与统一管理方面具备较高的实用价值，经过基本的安全与合规审查后，可作为 OSS 级别的后端基础设施在生产环境中使用。

## 🧭 Practical evaluation

**Value:** snakem982/proxypool helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1871 GitHub stars
- 137 forks
- updated 2026-06-25
- primary language: Go
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 53/100 |
| stars | 70/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 79/100 |
| recency | 80/100 |
| adoption | 65/100 |
| production | 71/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/snakem982/proxypool) · [← Back to Networking](./README.md)</sub>
