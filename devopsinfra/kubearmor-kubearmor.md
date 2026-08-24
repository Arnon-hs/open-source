# kubearmor/KubeArmor

[![Stars](https://img.shields.io/github/stars/kubearmor/KubeArmor?style=flat-square&color=yellow)](https://github.com/kubearmor/KubeArmor/stargazers) [![Forks](https://img.shields.io/github/forks/kubearmor/KubeArmor?style=flat-square&color=blue)](https://github.com/kubearmor/KubeArmor/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> Runtime Security Enforcement System. Workload hardening/sandboxing and implementing least-permissive policies made easy leveraging LSMs (LSM-BPF, AppArmor).

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.4k |
| 🍴 **Forks** | 501 |
| 💻 **Language** | Go |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bpf` `containers` `ebpf` `hacktoberfest` `kernel` `kubernetes` `lsm` `policy` `sandbox` `security` `system` `tool`

## 🎯 Categories

DevOps/Infra · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
KubeArmor is an open‑source runtime security enforcement system that hardens workloads and sandboxes containers by leveraging Linux Security Modules (LSM‑BPF, AppArmor) to apply least‑privilege policies automatically. It simplifies the creation and management of fine‑grained security policies for Kubernetes clusters, making it easy to protect workloads without deep kernel expertise. With strong community backing (2.4 k stars, 500+ forks) and active development, it is a mature candidate for production use.

**Value**  
- **Unified security enforcement:** Consolidates host‑level LSM capabilities into a single, Kubernetes‑native controller, reducing the need for multiple security tools.  
- **Policy‑as‑code:** Enables declarative, least‑permissive policies that can be version‑controlled and audited, improving compliance and incident response.  
- **Developer productivity:** Provides ready‑to‑use profiles and a simple CLI/CRD interface, lowering the learning curve for security teams and developers alike.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC):** Deploy the official Helm chart or Kustomize manifests in a non‑critical namespace; validate policy generation against a few test pods.  
2. **Read‑me & Documentation Review:** Follow the quick‑start guide to enable LSM‑BPF/AppArmor on the nodes, then experiment with the sample policies.  
3. **Policy Gradual Roll‑out:** Start with “monitor” mode to observe violations, refine policies, then switch to “enforce” mode cluster‑wide.  
4. **CI/CD Integration:** Add KubeArmor policy linting and automated testing to your pipeline to ensure new workloads remain compliant.  

**Production Readiness**  
- **Activity & Ecosystem:** Recent commits (as of 2026‑06‑25), a vibrant contributor base, and integration with major CNCF projects indicate strong momentum.  
- **Stability:** The project follows semantic versioning, provides Helm charts, and has been adopted in several large‑scale Kubernetes deployments.  
- **Risk Profile:** No critical licensing or metadata concerns identified; a final security audit of the binary and review of maintainer responsiveness are recommended before full‑scale rollout.  

Overall, KubeArmor offers a high‑impact, production‑ready solution for runtime security that can be introduced incrementally, starting with a small PoC and scaling to enforce cluster‑wide policies.

### Русский

KubeArmor — это система обеспечения runtime‑безопасности, позволяющая быстро «зажёстить» рабочие нагрузки в Kubernetes и применять политики минимальных привилегий, используя LSM‑механизмы (LSM‑BPF, AppArmor). Типичный сценарий внедрения — небольшое PoC: установить оператор KubeArmor, подключить его к кластерам и задать политики через YAML, после чего расширять покрытие на все поды. Проект имеет высокий уровень готовности к production (активные коммиты, 2434 звёзд, широкое принятие в сообществе) и подходит для пилотных внедрений в DevOps/Infra и Security‑потоках.

### 中文

**项目简介（2‑3 句话）**  
KubeArmor 是一套基于 Linux 安全模块（LSM‑BPF、AppArmor）的运行时安全强化系统，能够对容器、Pod、VM 等工作负载实现细粒度的沙箱化和最小权限策略，帮助用户在 Kubernetes 环境中快速落地安全防护。

**价值**  
- **统一安全治理**：在同一平台上对所有工作负载统一声明式策略，无需编写复杂的防火墙或审计规则。  
- **降低运维成本**：策略以 YAML 形式管理，结合 K8s 原生控制面，可通过 GitOps 自动化部署，极大简化安全团队的日常工作。  
- **提升风险可视化**：实时监控与审计日志帮助安全团队快速定位违规行为，支持事件溯源和合规审计。  

**典型接入方式**  
1. **快速试用**：在集群中直接使用 Helm Chart 或 Kustomize 部署 KubeArmor DaemonSet 与 Controller。  
2. **策略编写**：基于已有的示例 YAML（如文件访问、网络、系统调用限制），在 Git 仓库中编写自定义策略并通过 CI/CD 推送。  
3. **集成 CI/CD**：在代码审查阶段使用 `kubearmor-cli` 对新镜像进行安全基线检查，确保只有符合策略的镜像进入生产。  
4. **监控与告警**：将 KubeArmor 产生的审计事件通过 Prometheus Exporter 导出，结合 Alertmanager 实现告警，或将日志发送至 ELK/ Loki 进行统一分析。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑25，项目拥有 2.4k+ Stars、500+ Fork，最近一次提交在当日，说明社区和维护者仍在积极迭代。  
- **成熟生态**：已被多家企业在生产环境中采用，提供了 Helm、Operator、以及与 OPA、Falco 等安全生态的集成示例。  
- **可靠性**：核心代码使用 Go 编写，经过 CI 完整测试，提供了高可用的 DaemonSet 与控制平面组件。  
- **风险**：需进一步审查许可证（Apache‑2.0）兼容性、镜像安全签名以及维护者响应时效，但总体已具备在正式业务环境中进行试点甚至全量上线的条件。  

> **建议**：先在非关键业务集群做一个小规模 PoC（部署、策略下发、监控），验证与现有 CI/CD、监控体系的兼容性后，再逐步推广到生产环境。

## 🧭 Practical evaluation

**Value:** kubearmor/KubeArmor helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2434 GitHub stars
- 501 forks
- updated 2026-06-25
- primary language: Go
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 68/100 |
| stars | 72/100 |
| topics | 100/100 |
| outlook | 66/100 |
| quality | 72/100 |
| recency | 40/100 |
| adoption | 71/100 |
| production | 61/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/kubearmor/KubeArmor) · [← Back to DevOps & Infra](./README.md)</sub>
