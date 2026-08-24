# kubernetes-sigs/gateway-api

[![Stars](https://img.shields.io/github/stars/kubernetes-sigs/gateway-api?style=flat-square&color=yellow)](https://github.com/kubernetes-sigs/gateway-api/stargazers) [![Forks](https://img.shields.io/github/forks/kubernetes-sigs/gateway-api?style=flat-square&color=blue)](https://github.com/kubernetes-sigs/gateway-api/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Repository for the next iteration of composite service (e.g. Ingress) and load balancing APIs.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.9k |
| 🍴 **Forks** | 754 |
| 💻 **Language** | Go |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`gateway-api` `k8s-sig-network` `kubernetes` `networking` `sig-network`

## 🎯 Categories

Backend · DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
The **kubernetes-sigs/gateway-api** project defines a modern, extensible set of Kubernetes APIs for composite services such as Ingress, load‑balancing, and service mesh integration. It lets teams reuse a common, standards‑based service‑infrastructure layer instead of building custom networking logic for each application, accelerating API‑service delivery and promoting consistent service patterns.

**Value**  
- **Standardization** – Provides a single, CNCF‑backed API surface that unifies ingress, routing, and traffic‑splitting across clouds and service meshes.  
- **Reuse & Efficiency** – Teams can adopt the same gateway resources across multiple services, eliminating duplicated networking code and reducing operational overhead.  
- **Ecosystem Compatibility** – Broad support from major CNCF projects (e.g., Istio, Contour, Kong, Traefik) means existing controllers can be swapped or added without changing application manifests.

**Practical Adoption Path**  
1. **Evaluate Compatibility** – Deploy the `gateway-api` CRDs in a non‑production cluster and verify that your current ingress controller (or a supported one) offers a GatewayClass implementation.  
2. **Pilot with a Small Service** – Create `Gateway`, `HTTPRoute`, and related resources for a low‑risk service, using the same CI/CD pipelines you already have for Kubernetes manifests.  
3. **Gradual Migration** – Incrementally replace legacy Ingress objects with Gateway resources, leveraging the API’s versioning (v1alpha2 → v1beta1 → v1) to stay aligned with upstream releases.  
4. **Automate & Extend** – Use the provided Go client SDK or generated OpenAPI specs to embed Gateway creation into your internal tooling, and add custom policies via `ExtensionRef` if needed.

**Production Readiness**  
- **Activity & Adoption**: 2,917 stars, 754 forks, frequent commits (last update 2026‑07‑01) and multiple CNCF‑backed controllers already support the API, indicating a mature and actively maintained codebase.  
- **Stability**: The API has progressed through several release stages (alpha → beta → v1), and the spec is now stable enough for production use.  
- **Risk Assessment**: No major licensing or security red flags have been identified, though a final review of the project's security policy and maintainers’ activity is recommended before a full rollout.  

Overall, **gateway-api** is a high‑readiness, open‑source component that can be introduced in a controlled pilot and scaled to production to standardize and simplify service networking across Kubernetes environments.

### Русский

**kubernetes-sigs/gateway-api** — это открытый набор API для построения гибких шлюзов, ингрэссов и балансировщиков нагрузки в Kubernetes, позволяющий командам переиспользовать уже существующую сервисную инфраструктуру вместо создания собственных решений. Типичный сценарий — быстрое развёртывание новых API‑сервисов с единым, стандартизированным способом управления маршрутизацией, TLS и политиками, что ускоряет выпуск продукта и упрощает поддержку. Проект имеет высокий уровень готовности к production: активные коммиты, широкое принятие в сообществе (≈ 3 тыс. звёзд, 754 форка), поддержка Go‑клиентов и CLI, а также стабильную экосистему, требующую лишь финального аудита лицензии и безопасности.

### 中文

**项目简介（2‑3 句）**  
kubernetes-sigs/gateway‑api 是 Kubernetes 社区维护的下一代复合服务（如 Ingress）和负载均衡 API，提供统一的、可扩展的 Service‑Mesh 与网关抽象。它通过标准化的 CRD 与控制面向的 SDK/CLI，使团队能够在不同实现之间复用同一套服务基础设施，而无需重复构建底层的路由、流量管理和安全策略。

**价值**  
- **基础设施复用**：一次定义 Gateway、HTTPRoute 等资源，即可在多种实现（Istio、Contour、Envoy 等）上共享，同步演进，降低运维成本。  
- **加速交付**：开发者只需编写业务 Service，交给统一的 Gateway API 即可实现流量路由、TLS、负载均衡等功能，显著缩短 API 服务上线时间。  
- **标准化服务模式**：统一的 API 规范帮助组织在不同团队、不同集群之间保持一致的流量治理实践，提升可观测性与安全合规性。

**典型接入方式**  
1. **安装 CRD**：使用 `kubectl apply -f https://github.com/kubernetes-sigs/gateway-api/releases/download/vX.Y.Z/standard-install.yaml` 将 Gateway API 的 CRD 部署到集群。  
2. **选择实现**：部署对应的控制平面实现（如 `gateway-api-controller`、`contour`、`istio`），这些实现会监听 Gateway、HTTPRoute 等资源并在底层配置实际的代理。  
3. **使用 SDK/CLI**：通过官方 Go SDK（`sigs.k8s.io/gateway-api`）或 `kubectl`、`kustomize` 等工具创建 `Gateway`、`HTTPRoute`、`TLSRoute` 等对象，即可完成流量路由配置。  

**生产可用性**  
- **活跃度**：项目近期（2026‑07‑01）仍在持续更新，拥有 2917 ⭐、754 🍴，社区活跃，主要语言为 Go，拥有 5 个相关话题。  
- **生态采纳**：已被多家大型云厂商和 Service‑Mesh 项目（Istio、Envoy、Traefik）正式支持，具备成熟的实现层。  
- **成熟度**：在 CNCF SIG‑Network 中作为官方项目，遵循严格的审查与安全流程，具备明确的版本发布策略和兼容性保证。  

综合来看，gateway‑api 已具备 **高** 生产就绪度，适合作为企业内部或多租户平台的统一入口层进行试点或直接上线使用。

## 🧭 Practical evaluation

**Value:** kubernetes-sigs/gateway-api helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2917 GitHub stars
- 754 forks
- updated 2026-07-01
- primary language: Go
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 72/100 |
| stars | 74/100 |
| topics | 63/100 |
| outlook | 60/100 |
| quality | 67/100 |
| recency | 40/100 |
| adoption | 73/100 |
| production | 62/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/kubernetes-sigs/gateway-api) · [← Back to Backend](./README.md)</sub>
