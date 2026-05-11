# thomaspoignant/go-feature-flag

[![Stars](https://img.shields.io/github/stars/thomaspoignant/go-feature-flag?style=flat-square&color=yellow)](https://github.com/thomaspoignant/go-feature-flag/stargazers) [![Forks](https://img.shields.io/github/forks/thomaspoignant/go-feature-flag?style=flat-square&color=blue)](https://github.com/thomaspoignant/go-feature-flag/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> GO Feature Flag is a simple, complete and lightweight self-hosted cloud native feature flag solution 100% Open Source. 🎛️

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2k |
| 🍴 **Forks** | 204 |
| 💻 **Language** | Go |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`beginner-friendly` `continuous-delivery` `continuous-deployment` `continuous-testing` `experimentation` `experiments` `feature-flag` `feature-flags` `feature-toggle` `feature-toggles` `feature-toggling` `go-feature-flag`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief summary**  
GO Feature Flag (thomaspoignant/go‑feature‑flag) is a lightweight, self‑hosted, cloud‑native feature‑flag service written in Go. It provides a simple API and UI for toggling flags at runtime, making it easy for engineering teams to control feature rollouts without relying on external SaaS solutions. With active maintenance, a growing user base, and solid community metrics, it is ready for pilot projects and early production use.

**Value**  
The library lets developers embed feature‑flag logic directly into their codebases, eliminating the need for separate third‑party services and reducing latency. By toggling flags locally or via a central server, teams can accelerate development cycles, run safer canary releases, and get immediate feedback in CI pipelines, ultimately shortening review loops and cutting the cost of feature rollbacks.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the provided Docker compose or binary, and add a few flags to a sandbox service. Verify the API contract and UI meet your needs.  
2. **Integration** – Follow the README to embed the Go SDK into one microservice, configure the flag store (file, Redis, or DB), and wire the middleware into your HTTP handlers.  
3. **Pilot** – Enable the flag for a low‑traffic endpoint or internal user group, monitor performance, and collect feedback.  
4. **Scale** – Roll the flag out across additional services, adopt the centralized admin UI, and integrate with your CI/CD pipelines for automated flag toggling during deployments.

**Production readiness**  
The project scores high on production readiness: recent commits (as of 2026‑05‑11), 2014 GitHub stars, over 200 forks, and active issue resolution indicate a healthy community. Its Go‑native implementation aligns with cloud‑native architectures, and the self‑hosted model gives full control over security and compliance. While a final review of the license and any disclosed vulnerabilities is still required, the overall signals suggest the solution is mature enough for a serious pilot and, with proper monitoring, can be promoted to production.

### Русский

GO Feature Flag — это лёгкое, полностью self‑hosted решение для управления фич‑флагами, написанное на Go и доступное под открытой лицензией. Оно позволяет инженерам ускорять цикл разработки и ревью, автоматизировать локальные задачи и получать более быстрый фидбэк в CI, при этом готово к production‑использованию: проект активно поддерживается, имеет 2014 звёзд, частые коммиты (последнее обновление — 2026‑05‑11) и уже используется в нескольких продуктах. Рекомендуется начать с небольшого proof‑of‑concept, следуя README, а затем масштабировать в продакшн после окончательной проверки лицензии и безопасности.

### 中文

**项目简介**  
`thomaspoignant/go-feature-flag` 是一套基于 Go 实现的轻量级、完全开源的云原生特性开关系统，支持自托管、零依赖，适合在微服务或单体应用中快速开启/关闭功能。  

**价值**  
- **提升开发效率**：通过代码层面的特性开关，开发者可以在不修改业务代码的前提下安全地进行功能实验或灰度发布，显著缩短功能验证和回滚的周期。  
- **加速 CI/CD 反馈**：在 CI 环境中动态切换标志，可让测试用例只针对特定功能运行，减少不必要的构建和测试时间。  
- **统一治理**：所有特性标志集中管理，配合策略（如用户分群、时间窗口）实现精准控制，降低因手动配置导致的错误风险。  

**典型接入方式**  
1. **依赖引入**：在 Go 项目中 `go get github.com/thomaspoignant/go-feature-flag`。  
2. **配置文件**：准备 `ff.yaml`（或 JSON）描述标志、默认值及策略；支持本地文件、Redis、Consul、etcd 等后端存储。  
3. **初始化 SDK**：在程序启动时创建 `ffclient.New(ffclient.Config{FilePath: "ff.yaml"})` 并在需要的地方调用 `ffclient.BoolVariation("newFeature", ctx, false)`。  
4. **热更新**：SDK 会监听配置后端的变化，实现实时生效，无需重启服务。  
5. **小范围验证**：先在单元测试或本地开发环境开启一个最小的 POC，确认标志解析、策略生效以及监控指标后，再推广到预发布/生产环境。  

**生产可用性**  
- **活跃度**：仓库最近一次更新在 2026‑05‑11，拥有 2014+ 星、204+ Fork，社区活跃，已有多家企业在生产环境使用。  
- **成熟度**：提供完整的 SDK、示例、文档以及多种后端存储适配，支持高可用部署（可配合 Kubernetes/Helm）。  
- **风险**：目前仍需对许可证兼容性、长期维护者的响应速度以及潜在安全漏洞进行最终审查；但整体信号表明该项目已具备作为正式生产候选的条件。  

**结论**：`go-feature-flag` 以简洁、可自托管的特性开关能力帮助工程团队加速迭代和提升 CI 反馈质量，推荐先在小范围 PoC 验证后，逐步在生产环境推广使用。

## 🧭 Practical evaluation

**Value:** thomaspoignant/go-feature-flag helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2014 GitHub stars
- 204 forks
- updated 2026-05-11
- primary language: Go
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 58/100 |
| stars | 70/100 |
| topics | 100/100 |
| outlook | 83/100 |
| quality | 85/100 |
| recency | 100/100 |
| adoption | 67/100 |
| production | 78/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/thomaspoignant/go-feature-flag) · [← Back to DevTools](./README.md)</sub>
