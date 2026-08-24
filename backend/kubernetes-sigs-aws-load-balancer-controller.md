# kubernetes-sigs/aws-load-balancer-controller

[![Stars](https://img.shields.io/github/stars/kubernetes-sigs/aws-load-balancer-controller?style=flat-square&color=yellow)](https://github.com/kubernetes-sigs/aws-load-balancer-controller/stargazers) [![Forks](https://img.shields.io/github/forks/kubernetes-sigs/aws-load-balancer-controller?style=flat-square&color=blue)](https://github.com/kubernetes-sigs/aws-load-balancer-controller/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> A Kubernetes controller for Elastic Load Balancers

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4.3k |
| 🍴 **Forks** | 1.6k |
| 💻 **Language** | Go |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`aws` `gateway-api` `ingress` `ingress-resource` `k8s-sig-aws` `kubernetes` `kubernetes-ingress-controller`

## 🎯 Categories

Backend · DevOps/Infra

## 📝 Summary

### English

**Summary**  
The aws-load-balancer-controller is a Kubernetes controller that automatically provisions and manages AWS Elastic Load Balancers (ALBs/NLBs) for Kubernetes Service and Ingress resources. With 4.3 k stars, active maintenance (last update 2026‑05‑14) and strong community adoption, it offers a production‑ready way to reuse AWS load‑balancing infrastructure instead of building custom solutions.

**Value**  
By abstracting ELB creation into a native Kubernetes controller, teams can standardize service exposure patterns, accelerate API‑service delivery, and avoid duplicating common networking code across projects. The controller integrates directly with the Kubernetes API, so developers work with familiar manifests while the controller handles the underlying AWS resources.

**Practical adoption path**  
1. **Install** the controller via Helm or the provided manifests in a cluster that has IAM permissions to manage ELBs.  
2. **Annotate** Services/Ingresses with the controller‑specific annotations (e.g., `service.beta.kubernetes.io/aws-load-balancer-type`) to define the desired load‑balancer type and settings.  
3. **Validate** that the controller creates the correct ALB/NLB and that traffic flows as expected; then roll the configuration out to additional namespaces or clusters. Because the controller exposes its own CRDs and uses standard Kubernetes tooling, integration into CI/CD pipelines is straightforward.

**Production readiness**  
The project scores 77/100, shows recent activity, a large contributor base (1.6 k forks), and is written in Go with clear API/CLI interfaces. These signals, together with widespread adoption in the AWS‑Kubernetes ecosystem, indicate a high level of maturity suitable for a serious pilot or production deployment, pending the usual final checks on licensing, security scanning, and maintainer responsiveness.

### Русский

**kubernetes-sigs/aws-load-balancer-controller** — это контроллер Kubernetes, который автоматически управляет ресурсами Elastic Load Balancer (ALB/NLB) в AWS, позволяя командам использовать готовую инфраструктуру вместо самостоятельной разработки балансировщиков. Его типичный сценарий — быстрый запуск API‑сервисов: разработчики описывают Service/Ingress в манифестах, а контроллер создает, настраивает и поддерживает соответствующие ELB, обеспечивая стандартизованные паттерны доступа и масштабирования. Проект имеет высокий уровень готовности к продакшн: активные коммиты, более 4 000 звёзд на GitHub, широкое принятие в сообществе и зрелый набор функций, что делает его надёжным выбором для серьёзных пилотных и production‑развёртываний.

### 中文

**项目简介**  
kubernetes-sigs/aws-load-balancer-controller 是一个用 Go 编写的 Kubernetes 控制器，负责在 AWS 上自动创建、配置和管理 Elastic Load Balancers（ELB/NLB），从而让 Kubernetes Service 与云原生负载均衡无缝对接。

**价值**  
- **复用已有的云基础设施**：无需自行编写 ELB 逻辑，直接使用 AWS 官方的负载均衡功能。  
- **加速 API 服务交付**：通过声明式的 Service/Ingress 资源即可完成外部流量入口，显著缩短上线时间。  
- **统一服务模式**：在多个团队或项目之间统一使用同一套 ELB 配置规范，提升运维可观测性和安全合规性。

**典型接入方式**  
1. **部署控制器**：使用 Helm Chart 或 `kubectl apply -f` 将 controller 的 Deployment、ServiceAccount、ClusterRole 等资源安装到集群。  
2. **配置 IAM 权限**：为 controller 所使用的 ServiceAccount 关联具备 `elasticloadbalancing:*`、`ec2:Describe*` 等权限的 IAM Role（IRSA）。  
3. **声明 Service/Ingress**：在应用的 Service 或 Ingress 中添加注解（如 `service.beta.kubernetes.io/aws-load-balancer-type: nlb`），控制器会自动创建对应的 ELB 并同步状态。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑14，GitHub ★4291、Fork 1624，最近一次提交在当日，社区和 AWS 官方均在积极维护。  
- **成熟度**：已在大规模生产环境中广泛使用，支持多种 ELB 类型（ALB、NLB、CLB）以及高级功能（跨区负载、TLS 终端、WAF 集成）。  
- **风险**：暂无重大许可证或安全隐患，但仍建议在正式投产前完成一次安全审计并确认维护者响应速度。  

综上，aws-load-balancer-controller 具备高可用、易集成、社区活跃等特性，是在 Kubernetes 上使用 AWS 负载均衡的首选方案。

## 🧭 Practical evaluation

**Value:** kubernetes-sigs/aws-load-balancer-controller helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 4291 GitHub stars
- 1624 forks
- updated 2026-05-14
- primary language: Go
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 80/100 |
| stars | 77/100 |
| topics | 88/100 |
| outlook | 57/100 |
| quality | 68/100 |
| recency | 20/100 |
| adoption | 78/100 |
| production | 58/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/kubernetes-sigs/aws-load-balancer-controller) · [← Back to Backend](./README.md)</sub>
