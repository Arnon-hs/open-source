# prometheus-community/PushProx

[![Stars](https://img.shields.io/github/stars/prometheus-community/PushProx?style=flat-square&color=yellow)](https://github.com/prometheus-community/PushProx/stargazers) [![Forks](https://img.shields.io/github/forks/prometheus-community/PushProx?style=flat-square&color=blue)](https://github.com/prometheus-community/PushProx/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> Proxy to allow Prometheus to scrape through NAT etc.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 809 |
| 🍴 **Forks** | 157 |
| 💻 **Language** | Go |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Networking · Observability

## 📝 Summary

### English

Here's a brief summary of the project:

**Summary:** prometheus-community/PushProx is an open-source proxy that enables Prometheus to scrape metrics through Network Address Translation (NAT) and other network restrictions, making it easier to monitor and debug production behavior.

**Value:** This project provides a valuable solution for organizations to monitor systems, debug production behavior, and track service health, ultimately making it easier to inspect and debug production behavior.

**Practical Adoption Path:**

1. **Manual Inspection**: Before adopting PushProx, manual inspection is necessary to understand its integration signals and metadata.
2. **Dependency and Maintenance Checks**: Conduct thorough dependency and maintenance checks to ensure a smooth production environment.
3. **Prototype or Internal Workflow**: PushProx is suitable for prototypes or internal workflows, where its medium production readiness can be leveraged effectively.

**Production Readiness:** With a score of 58/100, PushProx is considered medium production ready, indicating that while it's useful for certain environments, it may require additional checks and validation before being deployed in production.

### Русский

Резюме проекта prometheus-community/PushProx:

Прокси сервер prometheus-community/PushProx позволяет мониторить и отслеживать производительность систем через NAT и другие ограничения. Он идеально подходит для отслеживания состояния служб и отладки проблем в производстве. Проект готов к использованию в прототипах или внутренних процессах, но требует проверки зависимостей и поддержки перед внедрением в производство.

### 中文

**简短介绍**

Prometheus-Community/PushProx 是一个开源项目，旨在通过代理使 Prometheus 能够从 NAT 等环境中收集指标数据。它使用户能够更方便地监控系统、调试生产行为以及跟踪服务健康状况。

**价值**

Prometheus-Community/PushProx 的价值在于，它帮助用户更容易地检查和调试生产行为，从而提高系统的可观察性和可靠性。

**典型接入方式**

典型的接入方式是：

1. 部署 PushProx 代理，配置其代理到 Prometheus 的目标。
2. 在 Prometheus 中配置 PushProx 代理，指定代理的地址和端口。
3. PushProx 代理会接收来自 Prometheus 的指标请求，并转发到目标系统。

**生产可用性**

PushProx 的生产可用性为中等（Medium）。它适合用于原型开发或内部工作流程，但在生产环境中使用之前，需要进行依赖检查和维护检查。

## 🧭 Practical evaluation

**Value:** prometheus-community/PushProx helps make production behavior easier to inspect and debug.

**Best use cases**

- monitor systems
- debug production behavior
- track service health

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 809 GitHub stars
- 157 forks
- updated 2026-07-19
- primary language: Go

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 55/100 |
| stars | 62/100 |
| topics | 0/100 |
| outlook | 61/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 60/100 |
| production | 65/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-19 · [View on GitHub](https://github.com/prometheus-community/PushProx) · [← Back to Networking](./README.md)</sub>
