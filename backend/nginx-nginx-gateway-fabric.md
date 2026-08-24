# nginx/nginx-gateway-fabric

[![Stars](https://img.shields.io/github/stars/nginx/nginx-gateway-fabric?style=flat-square&color=yellow)](https://github.com/nginx/nginx-gateway-fabric/stargazers) [![Forks](https://img.shields.io/github/forks/nginx/nginx-gateway-fabric?style=flat-square&color=blue)](https://github.com/nginx/nginx-gateway-fabric/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> NGINX Gateway Fabric provides an implementation for the Gateway API using NGINX as the data plane.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.1k |
| 🍴 **Forks** | 198 |
| 💻 **Language** | Go |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`gateway-api` `k8s` `kubernetes` `nginx`

## 🎯 Categories

Backend · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
NGINX Gateway Fabric is an open‑source implementation of the Kubernetes Gateway API that uses NGINX as the data‑plane proxy. It lets teams expose, secure, and manage API traffic with a familiar, battle‑tested stack while avoiding the need to build custom ingress or service‑mesh components. With strong community adoption (1 k+ stars, active commits, and a Go codebase), it is ready for pilots in production environments.

**Value**  
- **Reuse of proven infrastructure** – Leverages NGINX’s performance, observability, and security features, so teams don’t have to reinvent load‑balancing, TLS termination, or routing logic.  
- **Accelerated API delivery** – By conforming to the standard Gateway API, developers can define routes, policies, and back‑ends declaratively, reducing time‑to‑market for new services.  
- **Standardized service patterns** – Provides a single, consistent way to expose services across clusters, simplifying governance and reducing operational variance.

**Practical Adoption Path**  
1. **Evaluation** – Clone the repo, run the provided `make dev` or Helm chart in a sandbox cluster, and verify that the exposed API/SDK/CLI matches your existing CI/CD workflow.  
2. **Pilot** – Deploy the controller alongside a few non‑critical services, configure Gateway resources, and validate traffic routing, observability, and security policies.  
3. **Gradual migration** – Replace legacy ingress or custom proxies service‑by‑service, using the same Gateway manifests to keep configuration consistent.  
4. **Full rollout** – Standardize on the Gateway API across all clusters, integrate with existing NGINX monitoring (Prometheus, Grafana) and CI pipelines.

**Production Readiness**  
- **Activity & Adoption** – Recent commits (as of 2026‑06‑24), 1,109 stars, 198 forks, and multiple downstream users indicate a healthy ecosystem.  
- **Maturity** – Implemented in Go, with clear API/CLI surface, and aligns with the CNCF‑approved Gateway API specification.  
- **Risk considerations** – No major metadata issues, but a final review of the Apache‑2.0 license compliance, security audit reports, and maintainer responsiveness is advisable before mission‑critical deployment.  

Overall, NGINX Gateway Fabric offers a production‑grade, standards‑based gateway solution that can be introduced incrementally and scaled to full production use with confidence.

### Русский

NGINX Gateway Fabric — open‑source‑реализация Gateway API, использующая NGINX в качестве дата‑плейна, что позволяет командам быстро переиспользовать готовую сервисную инфраструктуру вместо её собственного построения. Его типичный сценарий — ускоренная доставка API‑сервисов и стандартизация паттернов backend‑операций за счёт единого, проверенного решения, доступного через API/SDK/CLI. Проект уже имеет активную разработку, широкое принятие (1109 звёзд, 198 форков), обновления до 2026‑06‑24 и считается готовым к пилотному запуску в продакшн, хотя требуется окончательная проверка лицензии и безопасности.

### 中文

**项目简介**  
NGINX Gateway Fabric 是基于 NGINX 实现的 Gateway API，提供统一的入口层，帮助团队直接复用成熟的服务基础设施，而无需自行搭建底层网关功能。

**价值**  
- **复用成熟组件**：利用 NGINX 强大的数据平面，省去自行实现 API 网关、负载均衡、流量治理等公共模块的工作。  
- **加速交付**：通过标准化的 Gateway API，团队可以更快地将后端服务上线，统一治理流量与安全策略。  
- **统一模式**：在组织内部形成统一的服务入口规范，提升可观测性、可维护性和安全合规性。

**典型接入方式**  
1. **声明式配置**：在 Kubernetes 集群中使用 Gateway、HTTPRoute、TCPRoute 等 CRD，直接交付业务服务。  
2. **CLI/SDK**：通过提供的 CLI 工具或 Go SDK 在 CI/CD 流程中自动生成或更新网关资源。  
3. **语言/元数据集成**：可在已有的服务框架（如 Go、Java、Node.js）中使用注解或配置文件，快速映射到 Gateway API。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑24，项目拥有 1109 星、198 Fork，最近一次提交在同一天，表明社区活跃。  
- **成熟度**：核心实现使用 Go 编写，已在多个生产环境中采用，具备高可用、水平扩展和成熟的监控/日志体系。  
- **风险**：暂无重大元数据风险，但仍需进一步审查许可证、漏洞报告以及维护者的长期承诺。总体而言，NGINX Gateway Fabric 已具备在生产环境进行试点甚至全量上线的条件。

## 🧭 Practical evaluation

**Value:** nginx/nginx-gateway-fabric helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1109 GitHub stars
- 198 forks
- updated 2026-06-24
- primary language: Go
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 57/100 |
| stars | 65/100 |
| topics | 50/100 |
| outlook | 56/100 |
| quality | 61/100 |
| recency | 40/100 |
| adoption | 63/100 |
| production | 60/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/nginx/nginx-gateway-fabric) · [← Back to Backend](./README.md)</sub>
