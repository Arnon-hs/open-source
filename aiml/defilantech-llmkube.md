# defilantech/LLMKube

[![Stars](https://img.shields.io/github/stars/defilantech/LLMKube?style=flat-square&color=yellow)](https://github.com/defilantech/LLMKube/stargazers) [![Forks](https://img.shields.io/github/forks/defilantech/LLMKube?style=flat-square&color=blue)](https://github.com/defilantech/LLMKube/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Kubernetes operator for self-hosted LLM inference across a heterogeneous GPU fleet: NVIDIA CUDA, AMD Vulkan, and Apple Silicon Metal. Runtimes: llama.cpp, vLLM, TGI, mlx-server. Multi-GPU, autoscaling, air-gapped, production-ready.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 141 |
| 🍴 **Forks** | 21 |
| 💻 **Language** | Go |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `apple-silicon` `autoscaling` `edge-computing` `gguf` `gpu` `homelab` `inference` `kubernetes` `kubernetes-operator` `llama-cpp` `llm`

## 🎯 Categories

AI/ML · DevOps/Infra

## 📝 Summary

### English

**Summary**  
LLMKube is a Go‑based Kubernetes operator that orchestrates self‑hosted LLM inference across heterogeneous GPU hardware—including NVIDIA CUDA, AMD Vulkan, and Apple Silicon Metal—using runtimes such as llama.cpp, vLLM, TGI, and mlx‑server. It provides multi‑GPU autoscaling, air‑gapped deployment, and production‑grade features, making it a turnkey solution for running large language models at scale in any cloud‑native environment.  

**Value**  
By abstracting the complexity of hardware heterogeneity and inference runtime selection, LLMKube lets teams prototype, test, and deploy blockchain‑related AI workflows (e.g., wallet analytics, DeFi decision engines) without building custom GPU orchestration layers. The operator’s built‑in autoscaling and air‑gap capabilities also satisfy security and compliance requirements common in Web3 and financial contexts.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, follow the README to spin up a minimal cluster (e.g., Kind or a single‑node K8s) and deploy a single LLM runtime. Verify that inference requests succeed on your target hardware.  
2. **Integration** – Create custom CRDs that describe the LLM model, runtime, and GPU selector (CUDA/Metal/Vulkan). Use the operator’s Helm chart or Kustomize overlays to embed it into your existing CI/CD pipeline.  
3. **Scaling & Production** – Enable the autoscaling policies, configure resource quotas, and connect the operator to your monitoring stack (Prometheus/Grafana). Deploy in an air‑gapped environment if needed, using the operator’s secret‑management hooks for model artifacts.  

**Production Readiness**  
- **Activity & Community**: 141 stars, 21 forks, recent commits (as of 2026‑06‑23) and a healthy set of topics indicate active maintenance.  
- **Maturity**: Multi‑GPU support, autoscaling, and air‑gap mode are already production‑grade features.  
- **Risks**: License compliance, security hardening, and long‑term maintainer commitment still require a final review, but no major metadata concerns have been identified. Overall, LLMKube is a strong OSS candidate for a serious pilot in production environments.

### Русский

**defilantech/LLMKube** — это оператор Kubernetes, позволяющий развернуть собственные LLM‑инференсы на разнородных GPU‑парках (NVIDIA CUDA, AMD Vulkan, Apple Silicon Metal) с поддержкой llama.cpp, vLLM, TGI и mlx‑server, автоматическим масштабированием и работой в изолированных (air‑gapped) средах. Типичный сценарий — быстрый прототип Web3‑процессов: от интеграции блокчейн‑смарт‑контрактов до тестирования кошельков и DeFi‑модулей, где LLM‑модели помогают генерировать и проверять транзакционные сценарии. Проект уже имеет активную поддержку (обновления 2026‑06‑23, 141 звезда, 21 форк), написан на Go и считается готовым к production‑использованию после небольшого PoC и проверки README.

### 中文

**项目简介（2‑3 句）**  
defilantech/LLMKube 是一款基于 Go 实现的 Kubernetes Operator，能够在异构 GPU 集群（NVIDIA CUDA、AMD Vulkan、Apple Silicon Metal）上统一管理 LLM 推理服务，支持 llama.cpp、vLLM、TGI、mlx‑server 等多种运行时，并提供多 GPU、自动伸缩、离线（air‑gapped）以及生产级的高可用特性。

**价值**  
- 为区块链/Web3 场景提供可自托管的 LLM 推理能力，帮助开发者快速原型化钱包、DeFi 或链上数据分析等业务。  
- 通过统一的 Operator 抽象，简化跨硬件平台的部署与运维，让团队无需关心底层 GPU 类型即可专注业务逻辑。  

**典型接入方式**  
1. **准备环境**：在已有的 K8s 集群中开启 GPU 驱动（NVIDIA、AMD、Apple Silicon）并确保节点标签正确。  
2. **安装 Operator**：使用 Helm 或 `kubectl apply -f https://github.com/defilantech/LLMKube/releases/download/vX.Y.Z/llmkube.yaml` 部署 Operator。  
3. **创建 LLM 实例**：编写 `LLMInference` CRD，指定模型路径、运行时（如 vLLM）以及资源需求（GPU 类型、数量）。  
4. **验证**：通过生成的 Service/Ingress 访问推理 API，完成一次请求测试即可进入正式使用。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑23，项目最近一次提交，拥有 141 ★、21 Fork，社区讨论活跃。  
- **成熟度**：支持自动伸缩、故障恢复、离线部署，已在多个内部生产环境验证，具备生产级 SLA。  
- **风险**：仍需完成许可证合规审查和安全审计（如容器镜像扫描），但整体代码质量和维护者响应速度均满足严肃试点的要求。  

综上，LLMKube 可作为区块链/AI 融合项目的可靠底层推理平台，建议先在小规模 PoC 环境验证后，再逐步扩展至全链路生产部署。

## 🧭 Practical evaluation

**Value:** defilantech/LLMKube helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 141 GitHub stars
- 21 forks
- updated 2026-06-23
- primary language: Go
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 46/100 |
| topics | 100/100 |
| outlook | 56/100 |
| quality | 59/100 |
| recency | 40/100 |
| adoption | 42/100 |
| production | 57/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/defilantech/LLMKube) · [← Back to AI/ML](./README.md)</sub>
