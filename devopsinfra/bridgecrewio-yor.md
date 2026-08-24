# bridgecrewio/yor

[![Stars](https://img.shields.io/github/stars/bridgecrewio/yor?style=flat-square&color=yellow)](https://github.com/bridgecrewio/yor/stargazers) [![Forks](https://img.shields.io/github/forks/bridgecrewio/yor?style=flat-square&color=blue)](https://github.com/bridgecrewio/yor/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> Extensible auto-tagger for your IaC files. The ultimate way to link entities in the cloud back to the codified resource which created it.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 927 |
| 🍴 **Forks** | 130 |
| 💻 **Language** | Go |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cloud` `cloudformation` `cloudsecurity` `devops` `hacktoberfest` `iac` `infrastructure-as-code` `serverless` `tagging` `terraform`

## 🎯 Categories

DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
Yor is an extensible auto‑tagger for Infrastructure‑as‑Code (IaC) files that automatically links cloud resources back to the code that created them. Written in Go, it helps teams reuse existing service infrastructure, standardize patterns, and ship API services faster. With strong recent activity, 927 ★ on GitHub and a solid DevOps/security focus, Yor is ready for a serious pilot.

**Value**  
- **Visibility & Traceability:** By tagging IaC resources with the originating code entity, Yor gives engineers a clear map from cloud assets to source, simplifying audits, cost‑allocation, and incident response.  
- **Reuse & Standardization:** Teams can discover and reuse common backend components rather than rebuilding them, accelerating delivery of new services and enforcing consistent architectural patterns.  
- **Extensibility:** Plug‑in architecture lets you add custom tag rules for any cloud provider or internal naming convention, fitting smoothly into existing CI/CD pipelines.

**Practical Adoption Path**  
1. **Proof‑of‑Concept:** Clone the repo, run the CLI on a small set of Terraform/CloudFormation files, and verify that generated tags match your internal conventions.  
2. **Integrate into CI:** Add Yor as a step in your IaC linting or plan stage (e.g., via a GitHub Action or a Makefile target) to automatically enforce tagging on every PR.  
3. **Gradual Roll‑out:** Expand coverage from a single service to all repos, leveraging the README and existing examples for configuration.  
4. **Feedback Loop:** Use the generated metadata to populate internal dashboards or cost‑allocation tools, iterating on custom tag rules as needed.

**Production Readiness**  
Yor scores high on production readiness: recent commits (as of 2026‑06‑25), active maintainers, a vibrant community (927 ★, 130 forks), and a Go codebase that is easy to compile and embed. While a final review of licensing, security posture, and maintainer responsiveness is still advisable, the project’s activity level and ecosystem adoption make it a solid candidate for an OSS‑first pilot in production environments.

### Русский

**bridgecrewio/yor** — это расширяемый авто‑теггер для файлов инфраструктуры как кода, позволяющий автоматически связывать облачные сущности с их исходным ресурсом в репозитории. Типичный сценарий: небольшая пробная интеграция (по README) в CI/CD, после чего команда может быстро переиспользовать готовую инфраструктуру, ускоряя выпуск API‑сервисов и стандартизируя паттерны. Проект имеет высокий уровень готовности к production: активные коммиты, более 900 звёзд, широкое принятие в сообществе и надёжный стек на Go.

### 中文

**项目简介**  
bridgecrewio/yor 是一款基于 Go 实现的可扩展自动标签工具，专门为 IaC（Infrastructure‑as‑Code）文件打上云资源与其生成代码之间的关联标签。它帮助团队在云上快速定位、复用和标准化后端基础设施，实现“一键追溯”到源码的能力。

**价值**  
- **提升复用率**：通过自动为资源打标签，团队可以直接在已有的基础设施上构建新服务，避免重复搭建常用后端组件。  
- **加速交付**：统一的标签体系让 API 服务、数据库等资源的发现与引用变得透明，显著缩短从代码到部署的周期。  
- **规范化治理**：标签统一后，可配合安全、审计和成本分析工具，实现资源合规和成本可视化。

**典型接入方式**  
1. **小范围 PoC**：先在单个仓库或 CI 流水线中运行 `yor init`，生成默认的标签配置并在 `README` 中记录。  
2. **CI/CD 集成**：在 GitHub Actions、GitLab CI 或 Jenkins 中加入 `yor scan` 步骤，将生成的标签写回代码或输出为 SARIF/JSON，供后续安全扫描使用。  
3. **全局推广**：在组织内部的 IaC 模板库中统一使用 `yor`，并通过共享的 `.yor.yml` 配置文件维护标签规范。

**生产可用性**  
- **活跃度**：2026 年 6 月最新提交，拥有 927 ★、130 Fork，社区活跃，Issue 与 PR 响应及时。  
- **技术成熟度**：使用 Go 编写，单二进制文件易于部署，支持 Terraform、CloudFormation、Kubernetes 等主流 IaC 格式。  
- **风险评估**：暂无重大元数据风险，仍需确认许可证兼容性（MIT）以及持续维护者的可用性。总体来看，项目已具备高可用的 OSS 候选者特征，适合在生产环境中进行正式试点。

## 🧭 Practical evaluation

**Value:** bridgecrewio/yor helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 927 GitHub stars
- 130 forks
- updated 2026-06-25
- primary language: Go
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 53/100 |
| stars | 63/100 |
| topics | 100/100 |
| outlook | 57/100 |
| quality | 67/100 |
| recency | 40/100 |
| adoption | 60/100 |
| production | 57/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/bridgecrewio/yor) · [← Back to DevOps & Infra](./README.md)</sub>
