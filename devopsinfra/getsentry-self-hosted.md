# getsentry/self-hosted

[![Stars](https://img.shields.io/github/stars/getsentry/self-hosted?style=flat-square&color=yellow)](https://github.com/getsentry/self-hosted/stargazers) [![Forks](https://img.shields.io/github/forks/getsentry/self-hosted?style=flat-square&color=blue)](https://github.com/getsentry/self-hosted/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Sentry, feature-complete and packaged up for low-volume deployments and proofs-of-concept

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 9.3k |
| 🍴 **Forks** | 1.9k |
| 💻 **Language** | Shell |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`docker` `docker-compose` `fair-source` `hacktoberfest` `on-premise` `self-hosted` `sentry` `tag-production`

## 🎯 Categories

DevOps/Infra

## 📝 Summary

### English

**Summary**  
getsentry/self‑hosted packages the full‑featured Sentry error‑tracking platform for low‑volume or proof‑of‑concept deployments, letting teams add observability and AI‑related telemetry without building a monitoring stack from scratch. With over 9 k stars, active commits (last updated 2026‑05‑12) and a rich set of integration signals (API, SDK, CLI, language metadata), it’s ready for rapid prototyping of AI features such as RAG pipelines or autonomous agents.  

**Value**  
The project gives developers an out‑of‑the‑box, production‑grade observability backend that can be extended with AI‑centric data (e.g., model latency, inference errors, prompt logs). By reusing Sentry’s existing UI, alerting, and issue‑grouping, teams avoid reinventing core monitoring while focusing on AI‑specific logic.  

**Practical adoption path**  
1. **Spin‑up**: Clone the repo and run the provided Docker‑Compose or Helm chart to launch Sentry locally or in a small cloud sandbox.  
2. **Integrate**: Add the Sentry SDK/CLI to your AI service (Python, Node, etc.) to emit events, performance spans, and custom tags for model calls.  
3. **Prototype**: Use the UI to explore error trends, set alerts, and experiment with RAG or agent workflow telemetry.  
4. **Scale**: When the prototype proves valuable, transition to a dedicated VM or Kubernetes deployment, configure persistent storage, and enable SSO/role‑based access.  

**Production readiness**  
- **Activity & community**: 9 331 stars, 1 941 forks, frequent commits, and recent releases indicate a healthy open‑source project.  
- **Stability**: The core Sentry platform is battle‑tested in large‑scale SaaS environments; the self‑hosted variant inherits the same code base with only deployment‑specific adjustments.  
- **Risk considerations**: No major metadata or licensing red flags, but a final security audit and verification of maintainers’ responsiveness are advisable before a mission‑critical rollout.  

Overall, getsentry/self‑hosted is a high‑readiness OSS candidate for teams that want robust observability and a quick path to AI‑enabled monitoring without building a stack from the ground up.

### Русский

getsentry/self-hosted — это полностью укомплектованная сборка Sentry, адаптированная для небольших развертываний и прототипов, позволяющая быстро добавить AI‑функциональность (RAG, агентные сценарии, оценку моделей) без необходимости строить стек с нуля. Проект легко интегрируется через API/SDK/CLI, предоставляет метаданные о языках и тематиках, а его активная разработка (9331 звёзд, 1941 форк, обновления до 2026‑05‑12) свидетельствует о высокой готовности к пилотному и даже production‑использованию. Единственное, что стоит дополнительно проверить — лицензия, безопасность и наличие активных мейнтейнеров.

### 中文

**项目简介**  
getsentry/self‑hosted 将功能完整的 Sentry 打包，专为低流量部署和概念验证（PoC）场景提供即插即用的监控与错误追踪能力。

**价值**  
- **快速赋能 AI 项目**：在已有的监控体系上直接获取异常、性能和调用链信息，帮助团队在不从零搭建模型栈的情况下，快速原型化 AI 功能（如 RAG、Agent 工作流）。  
- **统一可观测性**：通过统一的 API/SDK/CLI，收集语言元数据、错误日志、事务指标，为模型调试与性能评估提供完整的实现信号。  

**典型接入方式**  
1. **Docker/Compose 部署**：拉取官方镜像或使用提供的 `docker-compose.yml`，在几分钟内完成本地或私有云的 Sentry 实例。  
2. **SDK 集成**：在代码中引入对应语言的 Sentry SDK（Python、JavaScript、Go 等），通过简单的 `init` 配置即可捕获异常、事务和自定义事件。  
3. **CLI 与 API**：使用自带的 `sentry-cli` 或 REST API 管理项目、发布源码映射（source maps）以及查询事件数据，便于 CI/CD 流程自动化。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑12，项目拥有 9,331 星、1,941 Fork，最近一次提交在当日，表明维护活跃。  
- **成熟度**：Sentry 本身是业界广泛采用的错误监控平台，self‑hosted 版本在功能完整性和安全补丁方面保持同步，适合作为正式环境的监控后端。  
- **风险点**：仍需进一步审查许可证（BSD‑3‑Clause）与安全审计报告，确认长期维护者的响应能力后方可在关键业务中全量使用。  

综上，getsentry/self‑hosted 是一套即装即用、易于集成且已具备生产级可靠性的自托管监控解决方案，能够帮助 AI/ML 项目在原型阶段快速获取可观测数据，并平滑过渡到正式生产环境。

## 🧭 Practical evaluation

**Value:** getsentry/self-hosted helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 9331 GitHub stars
- 1941 forks
- updated 2026-05-12
- primary language: Shell
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 82/100 |
| stars | 84/100 |
| topics | 100/100 |
| outlook | 60/100 |
| quality | 73/100 |
| recency | 20/100 |
| adoption | 84/100 |
| production | 57/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/getsentry/self-hosted) · [← Back to DevOps & Infra](./README.md)</sub>
