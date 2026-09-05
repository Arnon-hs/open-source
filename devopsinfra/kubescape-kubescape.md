# kubescape/kubescape

[![Stars](https://img.shields.io/github/stars/kubescape/kubescape?style=flat-square&color=yellow)](https://github.com/kubescape/kubescape/stargazers) [![Forks](https://img.shields.io/github/forks/kubescape/kubescape?style=flat-square&color=blue)](https://github.com/kubescape/kubescape/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> Kubescape is an open-source Kubernetes security platform for your IDE, CI/CD pipelines, and clusters. It includes risk analysis, security, compliance, and misconfiguration scanning, saving Kubernetes users and administrators precious time, effort, and resources.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 11.4k |
| 🍴 **Forks** | 938 |
| 💻 **Language** | Go |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`best-practice` `devops` `kubernetes` `mitre-attack` `nsa` `security` `vulnerability-detection`

## 🎯 Categories

DevOps/Infra · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Kubescape is an open‑source security platform for Kubernetes that runs in IDEs, CI/CD pipelines, and directly on clusters, providing automated risk analysis, compliance checks, and misconfiguration detection. With over 11 k GitHub stars and active maintenance in Go, it helps teams secure their Kubernetes workloads without building custom tooling. The project is mature enough for a pilot, offering a low‑friction way to embed continuous security into the development lifecycle.

**Value**  
- **Comprehensive security coverage** – Scans for vulnerabilities, CIS‑benchmark compliance, and runtime misconfigurations in a single run.  
- **Developer‑first workflow** – Integrates with IDE extensions and CI/CD systems, enabling “shift‑left” security and reducing remediation effort later.  
- **Cost‑effective** – Free, open‑source solution eliminates the need for expensive commercial scanners while delivering enterprise‑grade detection.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the CLI locally against a test cluster, and verify the output matches your security policies.  
2. **CI/CD Integration** – Add the Kubescape Docker image or CLI step to your pipeline (e.g., GitHub Actions, GitLab CI) to fail builds on high‑severity findings.  
3. **IDE Plug‑in** – Install the Kubescape extension for VS Code or JetBrains IDEs to surface issues as developers write manifests.  
4. **Policy Tuning** – Customize the built‑in frameworks or supply your own OPA policies to align scans with organizational compliance requirements.  
5. **Full‑Scale Rollout** – Deploy the Kubescape operator in production clusters for continuous, scheduled scanning and alerting.

**Production Readiness**  
- **Activity & Community** – Recent commits (as of 2026‑05‑13), >11 k stars, 938 forks, and a vibrant Go‑centric ecosystem indicate strong community support.  
- **Stability** – The project follows semantic versioning, provides pre‑built binaries and Helm charts, and has been adopted by multiple enterprises.  
- **Risk Profile** – No major licensing or metadata concerns identified; a final security audit of the codebase and dependency chain is recommended before mission‑critical use.  

Overall, Kubescape is production‑ready for a serious pilot, offering a fast, low‑cost path to embed Kubernetes security throughout the software delivery lifecycle.

### Русский

Kubescape — это открытая платформа для обеспечения безопасности Kubernetes, позволяющая в IDE, CI/CD‑конвейерах и кластерах быстро проводить анализ рисков, проверку соответствия и сканирование на наличие уязвимостей и неправильных конфигураций, экономя время и ресурсы команд. Типичный сценарий внедрения — запуск Kubescape в виде небольшого proof‑of‑concept в пайплайне CI, проверка результатов по README и постепенное расширение на все кластеры и рабочие нагрузки. По уровню готовности проект считается почти production‑ready: активные коммиты, более 11 тыс. звёзд на GitHub, регулярные обновления и широкое принятие в сообществе позволяют использовать его в серьёзных пилотных проектах.

### 中文

**项目简介**  
Kubescape 是一款开源的 Kubernetes 安全平台，能够在 IDE、CI/CD 流水线以及运行中的集群中进行风险分析、合规检查和误配置扫描，帮助用户快速发现并修复安全隐患。

**价值**  
- **全链路安全**：从代码编写到部署运行全阶段提供统一的安全检测，降低因配置错误导致的攻击面。  
- **节省人力成本**：自动化的扫描与报告让运维和开发团队无需手动审计，大幅提升效率。  
- **合规支撑**：内置多种行业基准（如 PCI‑DSS、CIS），帮助企业快速通过审计。

**典型接入方式**  
1. **IDE 插件**：在本地开发环境中安装 Kubescape 插件，保存代码时即时进行安全检查。  
2. **CI/CD 步骤**：在 GitHub Actions、GitLab CI、Jenkins 等流水线中加入 `kubescape scan` 命令，自动生成报告并阻止不合规的镜像或 YAML 文件。  
3. **集群守护进程**：在 Kubernetes 集群中部署 Kubescape DaemonSet，持续监控运行时配置和镜像安全状态。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑13，项目拥有 11 416 颗星、938 次 Fork，最近一次提交仍在进行中。  
- **成熟度**：已被多家企业在生产环境中使用，社区提供丰富的文档和案例。  
- **风险可控**：暂无重大许可证或安全隐患，但仍建议在正式上线前完成一次小规模的 PoC 并审查最新的安全报告。  

综上所述，Kubescape 具备高可用性和成熟的生态，可作为生产环境中 Kubernetes 安全防护的首选方案。

## 🧭 Practical evaluation

**Value:** kubescape/kubescape helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 11416 GitHub stars
- 938 forks
- updated 2026-05-13
- primary language: Go
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 74/100 |
| stars | 86/100 |
| topics | 88/100 |
| outlook | 76/100 |
| quality | 85/100 |
| recency | 80/100 |
| adoption | 83/100 |
| production | 76/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/kubescape/kubescape) · [← Back to DevOps & Infra](./README.md)</sub>
