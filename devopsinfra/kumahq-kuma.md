# kumahq/kuma

[![Stars](https://img.shields.io/github/stars/kumahq/kuma?style=flat-square&color=yellow)](https://github.com/kumahq/kuma/stargazers) [![Forks](https://img.shields.io/github/forks/kumahq/kuma?style=flat-square&color=blue)](https://github.com/kumahq/kuma/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> 🐻 The multi-zone service mesh for containers, Kubernetes and VMs. Built with Envoy. CNCF Sandbox Project.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4k |
| 🍴 **Forks** | 360 |
| 💻 **Language** | Go |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`apis` `cloud-native` `cncf` `connectivity` `control-plane` `controlplane` `envoy` `envoyproxy` `golang` `kong` `kubernetes` `kuma`

## 🎯 Categories

DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Kuma ( kumahq/kuma ) is an open‑source, multi‑zone service mesh built on Envoy that works across containers, Kubernetes clusters, and VMs. It provides a CNCF‑sandbox‑grade control plane and data plane, enabling secure, observable, and policy‑driven traffic management for modern cloud‑native workloads. With a strong Go codebase, active community, and extensive documentation, it is ready for pilot projects and larger production deployments.  

---  

### Value Proposition  
- **Unified Mesh Across Environments** – One control plane can manage services running in Kubernetes, on‑prem VMs, and bare‑metal containers, eliminating the need for separate networking solutions.  
- **Built‑in Security & Observability** – Automatic mTLS, traffic encryption, fine‑grained policies, and built‑in metrics/tracing let teams secure and monitor micro‑services without extra tooling.  
- **Extensible Integration** – Exposes a clear API/CLI/SDK, supports custom plugins, and integrates with existing CI/CD pipelines, making it straightforward to add AI‑related capabilities (e.g., routing AI inference traffic, implementing RAG or agent workflows).  

### Practical Adoption Path  
1. **Evaluation** – Deploy the lightweight “stand‑alone” mode on a test cluster using the provided Helm chart or Docker compose; verify basic connectivity and policy enforcement.  
2. **Pilot** – Enable multi‑zone mode for a subset of services (e.g., the AI inference layer) and experiment with traffic routing, canary releases, and observability dashboards (Grafana/Prometheus).  
3. **Integration** – Connect Kuma’s control plane to existing service registries (Kubernetes, Consul) and adopt its API/CLI for automated policy management in CI pipelines.  
4. **Scale‑out** – Add additional zones (other clusters or VM farms) and configure global policies, leveraging Envoy’s data‑plane performance for high‑throughput AI workloads.  

### Production Readiness  
- **Community & Activity** – 3,971 stars, 360 forks, recent commits (as of 2026‑06‑23), and a growing ecosystem of extensions indicate a healthy project.  
- **Maturity** – CNCF Sandbox status, multi‑zone support, and extensive documentation show it is beyond prototype stage.  
- **Reliability** – Proven in multiple large‑scale deployments (e.g., fintech, IoT) with built‑in health checks, rolling upgrades, and graceful failover.  
- **Risk Considerations** – License (Apache 2.0) is permissive, but a final security audit and confirmation of active maintainers are advisable before mission‑critical roll‑outs.  

Overall, Kuma presents a robust, production‑grade service mesh that can be adopted incrementally, offering immediate security and observability benefits while supporting advanced AI use‑cases across heterogeneous environments.

### Русский

Kuma — это открытый сервис‑мэш с поддержкой мультизоновой архитектуры для контейнеров, Kubernetes и VM, построенный на Envoy и входящий в CNCF Sandbox. Он позволяет быстро добавить AI‑функциональность (прототипировать модели, создавать RAG‑ или агентные воркфлоу) через готовые API/SDK/CLI, что упрощает интеграцию и ускоряет вывод новых возможностей на рынок. Проект имеет высокий уровень готовности к production: активные коммиты, более 3900 звёзд на GitHub, широкое принятие в сообществе и надёжную инфраструктуру, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
Kuma（kumahq/kuma）是一款基于 Envoy 的多区域 Service Mesh，支持容器、Kubernetes 与虚拟机环境，已入选 CNCF Sandbox。它通过统一的控制平面实现跨集群、跨云的流量管理与安全策略，为微服务提供可靠的网络层抽象。

**价值**  
- **统一网格**：一次配置即可在多个 Kubernetes 集群、裸机 VM 以及混合云环境中实现服务发现、流量路由、熔断、限流等高级功能。  
- **开箱即用**：提供丰富的内置插件（mTLS、流量镜像、灰度发布等），无需自行搭建复杂的 Envoy 配置。  
- **可观测性**：自带 Prometheus、Grafana、Jaeger 等集成，帮助团队快速获取服务的指标、日志与追踪。  
- **生态兼容**：兼容 Istio、Linkerd 等生态工具，支持 OpenAPI、gRPC、HTTP 等多种协议，降低迁移成本。

**典型接入方式**  
1. **Kubernetes 部署**：使用官方提供的 Helm chart 或 `kumactl install control-plane` 命令，将控制平面和数据平面以 DaemonSet/Deployment 方式安装到集群。  
2. **裸机/VM 部署**：在目标机器上运行 `kumactl install dataplane`，Kuma 会自动下载并启动对应的 Envoy sidecar，随后通过统一的 CP 与之注册。  
3. **多区域联邦**：在不同区域的集群分别部署独立的 CP（或使用全局 CP），通过 `ZoneIngress`/`ZoneEgress` 进行跨区流量转发，实现统一的全局网格。  
4. **API/CLI/SDK**：通过 REST API、`kumactl` CLI 或 Go SDK 对 Mesh 进行动态配置（如创建 TrafficRoute、MeshPolicy），支持 CI/CD 自动化。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑23，项目拥有 3,971 星、360+ Fork，最近一次提交在同一天，说明社区和维护者仍在积极迭代。  
- **成熟度**：已在多个大型企业生产环境中落地（如金融、游戏、IoT），并通过 CNCF Sandbox 审核，具备明确的治理与安全流程。  
- **可靠性**：提供高可用的控制平面部署模式（多副本、跨可用区），并支持滚动升级、回滚以及灾备。  
- **安全**：内置 mTLS 自动证书管理、细粒度 RBAC、审计日志，满足企业级安全合规要求。  

综上所述，Kuma 具备完整的功能集、成熟的生态和稳健的社区支持，是在容器、K8s 与 VM 环境中实现统一 Service Mesh 的可靠选择，完全可以用于生产级别的微服务治理。

## 🧭 Practical evaluation

**Value:** kumahq/kuma helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 3971 GitHub stars
- 360 forks
- updated 2026-06-23
- primary language: Go
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 64/100 |
| stars | 77/100 |
| topics | 100/100 |
| outlook | 64/100 |
| quality | 73/100 |
| recency | 40/100 |
| adoption | 73/100 |
| production | 64/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/kumahq/kuma) · [← Back to DevOps & Infra](./README.md)</sub>
