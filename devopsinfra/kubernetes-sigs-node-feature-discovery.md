# kubernetes-sigs/node-feature-discovery

[![Stars](https://img.shields.io/github/stars/kubernetes-sigs/node-feature-discovery?style=flat-square&color=yellow)](https://github.com/kubernetes-sigs/node-feature-discovery/stargazers) [![Forks](https://img.shields.io/github/forks/kubernetes-sigs/node-feature-discovery?style=flat-square&color=blue)](https://github.com/kubernetes-sigs/node-feature-discovery/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Node feature discovery for Kubernetes

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.1k |
| 🍴 **Forks** | 310 |
| 💻 **Language** | Go |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cpuid` `feature-detection` `hacktoberfest` `hardware` `k8s-sig-node` `kubernetes` `node-labels` `rdt`

## 🎯 Categories

DevOps/Infra

## 📝 Summary

### English

Here's a brief summary:

**Node Feature Discovery for Kubernetes**: This open-source project, kubernetes-sigs/node-feature-discovery, enables developers to build product UI faster and reuse interface components, ultimately improving frontend delivery. By leveraging this project, users can reduce custom UI work and focus on delivering high-quality user-facing interfaces. With its strong ecosystem signals, recent activity, and high adoption rate, it's a suitable candidate for a serious pilot.

**Value:**
The value proposition of this project lies in its ability to reduce the time and effort required to build product UI, allowing developers to focus on delivering high-quality user-facing interfaces. By reusing interface components, users can improve frontend delivery and reduce custom UI work.

**Practical Adoption Path:**
To adopt this project, users should start with a small proof of concept and thoroughly review the README documentation. This will help evaluate the feasibility of integration and ensure a smooth onboarding process. With a solid understanding of the project's capabilities and limitations, users can proceed with a more extensive implementation.

**Production Readiness:**
The project demonstrates high production readiness, with strong ecosystem signals, recent activity, and high adoption rates. Although some final review of license, security posture, and active maintainers is necessary, the overall quality signals and metadata suggest that

### Русский

**kubernetes-sigs/node-feature-discovery** — это open‑source‑инструмент, который автоматически собирает характеристики узлов (CPU, GPU, сетевые возможности, драйверы и т.п.) и публикует их в виде меток Kubernetes, позволяя быстро адаптировать пользовательские UI‑компоненты и другие сервисы под реальное железо без написания собственного сбора данных. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept DaemonSet, проверка README и интеграция меток в CI/CD‑pipeline для динамического включения UI‑фич; после подтверждения работоспособности можно масштабировать на весь кластер. Проект имеет высокий уровень готовности к production: активные коммиты, более 1000 звёзд, широкое принятие в сообществе и стабильную экосистему, однако перед запуском в прод необходимо окончательно проверить лицензию, безопасность и наличие активных мейнтейнеров.

### 中文

**简短介绍**

kubernetes-sigs/node-feature-discovery 是一个开源项目，旨在为 Kubernetes 提供节点特征发现功能。它可以帮助开发者快速构建用户界面，减少自定义 UI 工作量。

**价值**

kubernetes-sigs/node-feature-discovery 的价值在于，它可以帮助开发者:

* 快速构建产品 UI
* 重用界面组件
* 提高前端交付效率

**典型接入方式**

接入该项目的步骤包括:

1. 阅读 README 文档
2. 运行一个小型 PoC（Proof of Concept）
3. 检查项目的文档和示例

**生产可用性**

该项目已被广泛采用，具有强大的生态系统信号，且最近有活跃的维护者。因此，它对生产环境的可用性评分为高（High）。但是，仍需要对其许可证、安全情绪和活跃维护者进行最终审查。

## 🧭 Practical evaluation

**Value:** kubernetes-sigs/node-feature-discovery helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1053 GitHub stars
- 310 forks
- updated 2026-07-06
- primary language: Go
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 62/100 |
| stars | 64/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 79/100 |
| recency | 80/100 |
| adoption | 64/100 |
| production | 73/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/kubernetes-sigs/node-feature-discovery) · [← Back to DevOps & Infra](./README.md)</sub>
