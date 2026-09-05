# streamnative/pulsarctl

[![Stars](https://img.shields.io/github/stars/streamnative/pulsarctl?style=flat-square&color=yellow)](https://github.com/streamnative/pulsarctl/stargazers) [![Forks](https://img.shields.io/github/forks/streamnative/pulsarctl?style=flat-square&color=blue)](https://github.com/streamnative/pulsarctl/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> a CLI for Apache Pulsar written in Go

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 169 |
| 🍴 **Forks** | 71 |
| 💻 **Language** | Go |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`apache-pulsar` `cli` `golang` `pulsar` `pulsarctl` `restful-api`

## 🎯 Categories

Backend · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
streamnative/pulsarctl is an open‑source command‑line interface for Apache Pulsar, written in Go, that lets developers manage Pulsar clusters, topics, and subscriptions without writing custom code. With 169 GitHub stars, recent commits (as of 2026‑05‑14), and active community adoption, it offers a ready‑to‑use tool for standardizing backend service patterns and accelerating API delivery.

**Value**  
- **Infrastructure reuse:** By exposing Pulsar’s management functions through a stable CLI, teams can avoid re‑implementing common admin and monitoring logic in each service.  
- **Speed to market:** Developers can script provisioning, schema updates, and consumer management directly from CI/CD pipelines, shortening the time needed to ship new API services.  
- **Standardization:** A single, language‑agnostic interface encourages consistent operational practices across microservices, reducing drift and onboarding friction.

**Practical Adoption Path**  
1. **Evaluation:** Clone the repo, run `pulsarctl` against a dev Pulsar cluster, and verify that the commands cover the required use‑cases (topic creation, subscription handling, ACLs, etc.).  
2. **Integration:** Wrap the CLI in internal scripts or CI jobs, or invoke it via its Go SDK for tighter programmatic control.  
3. **Policy & Security Review:** Confirm the Apache‑2.0 license, run a vulnerability scan (e.g., `govulncheck`), and ensure maintainers have a visible contribution pipeline.  
4. **Roll‑out:** Deploy the binary to a shared tooling repository (e.g., internal Docker image or artifact store) and document standard command sets for all teams.

**Production Readiness**  
- **Activity & Adoption:** Frequent commits, recent updates (May 2026), 169 stars, and 71 forks indicate an active community and ongoing maintenance.  
- **Ecosystem Fit:** The project provides clear API/SDK signals, Go language metadata, and a focused topic set, making it easy to integrate with existing Go services or any language via the CLI.  
- **Risk Assessment:** No immediate licensing or security red flags, though a final review of the maintainers’ responsiveness and any disclosed CVEs is recommended. Overall, pulsarctl is mature enough for a pilot in production environments, with a clear path to full adoption.

### Русский

**streamnative/pulsarctl** — это CLI‑утилита на Go для управления Apache Pulsar, позволяющая командам быстро использовать готовую инфраструктуру брокеров, темы и подписчиков без необходимости писать собственный бекенд. Ее обычно внедряют, когда нужно ускорить запуск API‑сервисов, стандартизировать паттерны работы с Pulsar и повторно использовать общие сервисные компоненты. Проект демонстрирует высокий уровень готовности к production: активные коммиты, растущее сообщество (169 звёзд, 71 форк), поддержка основных API/SDK и наличие лицензии, хотя окончательная проверка безопасности и поддержки должна быть проведена.

### 中文

**项目简介**  
`streamnative/pulsarctl` 是一款用 Go 编写的 Apache Pulsar 命令行工具，提供统一的 API/SDK/CLI 接口，帮助开发者快速管理 Pulsar 集群和资源。  

**价值**  
- **复用基础设施**：团队无需自行实现 Pulsar 的运维脚本或自定义客户端，直接使用成熟的 CLI 即可完成主题、订阅、租户等日常操作。  
- **加速交付**：通过标准化的命令和一致的输出格式，开发和运维可以更快地上线 API 服务，降低重复劳动。  
- **统一服务模式**：在多项目或多团队环境下，使用同一套工具可以保证操作规范和审计一致性。  

**典型接入方式**  
1. **本地或 CI 环境直接安装**：`go install github.com/streamnative/pulsarctl@latest` 或下载预编译二进制。  
2. **在容器/脚本中调用**：将二进制挂载到 CI/CD 步骤或 Kubernetes Init 容器中，使用 `pulsarctl` 完成主题创建、权限配置等。  
3. **与现有 SDK 组合**：在 Go 项目中通过 `os/exec` 调用 CLI，或在其他语言的自动化脚本中使用其 JSON 输出做进一步处理。  

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑05‑14，拥有 169 ★、71 Fork，社区活跃，Issue 反馈及时。  
- **生态兼容**：直接面向 Pulsar 官方 API，支持最新的 Pulsar 版本，且提供丰富的命令子集（topic、namespace、tenant、functions 等）。  
- **风险**：目前未发现重大许可证或安全隐患，但仍建议在正式上线前审查其依赖的第三方库和维护者的响应速度。  

综合来看，`streamnative/pulsarctl` 已具备高生产就绪度，适合作为内部或跨团队的 Pulsar 运维与自动化入口。

## 🧭 Practical evaluation

**Value:** streamnative/pulsarctl helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 169 GitHub stars
- 71 forks
- updated 2026-05-14
- primary language: Go
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 46/100 |
| stars | 47/100 |
| topics | 75/100 |
| outlook | 72/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 47/100 |
| production | 72/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/streamnative/pulsarctl) · [← Back to Backend](./README.md)</sub>
