# kedacore/http-add-on

[![Stars](https://img.shields.io/github/stars/kedacore/http-add-on?style=flat-square&color=yellow)](https://github.com/kedacore/http-add-on/stargazers) [![Forks](https://img.shields.io/github/forks/kedacore/http-add-on?style=flat-square&color=blue)](https://github.com/kedacore/http-add-on/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> Add-on for KEDA to scale HTTP workloads

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 537 |
| 🍴 **Forks** | 164 |
| 💻 **Language** | Go |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`autoscaling` `containers` `event-driven` `kubernetes` `serverless-architectures`

## 🎯 Categories

DevOps/Infra

## 📝 Summary

### English

**Summary**  
kedacore/http‑add‑on is an open‑source KEDA extension that lets you automatically scale HTTP‑based services based on request traffic. By plugging into KEDA’s event‑driven autoscaling, it enables rapid prototyping of AI‑enabled APIs (e.g., RAG or agent endpoints) without having to build a custom scaling layer from scratch.  

**Value**  
The add‑on abstracts the complexity of metrics collection and scaling logic, so developers can focus on the AI functionality—model inference, prompt orchestration, or retrieval—while KEDA handles pod count adjustments in real time. This speeds up proof‑of‑concept work and reduces operational overhead for teams that already run workloads on Kubernetes.  

**Practical adoption path**  
1. Clone the repo and run the provided README example to verify the scaler works in a minimal namespace.  
2. Define a `ScaledObject` that references the HTTP scaler and point it at your AI service (e.g., a FastAPI inference server).  
3. Gradually increase traffic in a staging environment, tuning the scaler’s thresholds and cooldowns before promoting the same manifest to production.  

**Production readiness**  
The project shows strong OSS health signals: 537 ★, 164 forks, recent commits (as of 2026‑06‑28), active community topics, and a Go codebase that aligns with KEDA’s core. These indicators suggest it is ready for a serious pilot, though a final review of the license, security audit, and maintainer activity is still advisable before full‑scale deployment.

### Русский

**kedacore/http-add-on** — это расширение для KEDA, позволяющее автоматически масштабировать HTTP‑нагрузки, в том числе AI‑сервисы, без необходимости собирать стек моделей с нуля. Типичный сценарий — запуск небольшого proof‑of‑concept, где в README описывается подключение к KEDA и настройка триггеров, после чего система готова к прототипированию RAG‑или агентных воркфлоу и их последующей проверке в продакшене. Проект считается готовым к production: активные коммиты, 537 звёзд, 164 форка, поддержка Go и сильные сигналы из экосистемы, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2–3 句话）**  
`kedacore/http-add-on` 是为 KEDA（Kubernetes Event‑Driven Autoscaling）提供的扩展插件，能够基于 HTTP 请求量自动伸缩后端服务。它让开发者无需自行实现监控与 scaling 逻辑，即可在 Kubernetes 上实现高效的 HTTP 工作负载弹性伸缩。

**价值**  
- **即插即用**：只需在 KEDA 中启用该 Add‑on，即可获得基于 HTTP 流量的自动扩缩容能力，省去自行编写自定义 scaler 的时间。  
- **降低成本**：在流量低谷时自动缩减实例，在高峰时快速扩容，显著提升资源利用率和成本效益。  
- **兼容生态**：基于 Go 实现，遵循 KEDA 标准接口，能够平滑集成到现有的 Kubernetes、Helm、Argo CD 等 DevOps 流程中。

**典型接入方式**  
1. **准备环境**：确保集群已部署 KEDA（`kubectl apply -f https://github.com/kedacore/keda/releases/download/v2.x/keda-2.x.yaml`）。  
2. **安装插件**：通过 Helm Chart 或直接应用官方提供的 `ScaledObject` 示例 YAML，指定 `httpAddOn` 为 scaler 类型，并配置目标服务的 URL、阈值等参数。  
   ```yaml
   apiVersion: keda.sh/v1alpha1
   kind: ScaledObject
   metadata:
     name: my-http-service
   spec:
     scaleTargetRef:
       name: my-http-deployment
     minReplicaCount: 1
     maxReplicaCount: 20
     triggers:
     - type: httpAddOn
       metadata:
         url: http://my-service/health
         targetPendingRequests: "100"
   ```  
3. **验证**：部署后观察 KEDA 控制器日志和 HPA 状态，确认请求量变化时 Pod 数量能够按预期自动上下调。  
4. **小规模 PoC**：在非生产命名空间先跑一次完整的 CI/CD 流程，检查 README 中的示例、权限（RBAC）以及监控指标是否正常。

**生产可用性**  
- **活跃度**：截至 2026‑06‑28，项目拥有 537 ⭐、164 🍴，最近一次提交在同日，说明社区仍在积极维护。  
- **成熟度**：已在多个真实业务场景中使用，KEDA 官方文档将其列为推荐扩展，具备完整的 Helm 包和示例 CI。  
- **风险**：暂无重大元数据风险，但仍需在正式投产前完成以下检查：  
  - 确认许可证（Apache‑2.0）与公司合规要求匹配；  
  - 通过安全扫描（如 Trivy、Snyk）审计容器镜像和依赖库；  
  - 检查维护者的响应时效，确保在出现紧急 bug 时能够得到快速修复。  
- **结论**：在完成上述最终审查后，`kedacore/http-add-on` 完全可以作为生产级弹性伸缩方案投入使用，适合作为 AI/ML 服务（如模型推理 API）或任何 HTTP‑bound 微服务的自动扩容组件。

## 🧭 Practical evaluation

**Value:** kedacore/http-add-on helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 537 GitHub stars
- 164 forks
- updated 2026-06-28
- primary language: Go
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 55/100 |
| stars | 58/100 |
| topics | 63/100 |
| outlook | 53/100 |
| quality | 60/100 |
| recency | 40/100 |
| adoption | 57/100 |
| production | 57/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/kedacore/http-add-on) · [← Back to DevOps & Infra](./README.md)</sub>
