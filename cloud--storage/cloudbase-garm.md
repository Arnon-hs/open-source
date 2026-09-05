# cloudbase/garm

[![Stars](https://img.shields.io/github/stars/cloudbase/garm?style=flat-square&color=yellow)](https://github.com/cloudbase/garm/stargazers) [![Forks](https://img.shields.io/github/forks/cloudbase/garm?style=flat-square&color=blue)](https://github.com/cloudbase/garm/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Multi-cloud, auto-scaling manager for GitHub Actions & Gitea self-hosted runners with pluggable providers

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 353 |
| 🍴 **Forks** | 49 |
| 💻 **Language** | Go |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`actions-runner` `autoscaler` `autoscaling` `aws` `azure` `cicd` `ec2` `ephemeral-runners` `gcp` `gitea` `github` `github-actions`

## 🎯 Categories

Cloud & Storage

## 📝 Summary

### English

**Brief Summary**  
cloudbase/garm is an open‑source, multi‑cloud manager that automatically provisions and scales self‑hosted GitHub Actions or Gitea runners using pluggable cloud providers. Written in Go and actively maintained (353 ★, recent commits, multiple forks), it offers a turnkey way to run CI/CD workloads on any cloud without manual runner management.

**Value**  
garm eliminates the operational overhead of maintaining a fixed pool of self‑hosted runners by dynamically creating and destroying instances based on job demand, reducing cost and improving elasticity. Its provider‑agnostic architecture lets teams reuse the same tooling across AWS, Azure, GCP, DigitalOcean, etc., and the same codebase can serve both GitHub Actions and Gitea, consolidating CI infrastructure.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, follow the README to spin up a minimal deployment (e.g., a single Docker container with a mock cloud provider).  
2. **Provider integration** – Enable the desired cloud provider plugin, configure credentials and runner image, and test auto‑scaling with a few CI jobs.  
3. **CI pipeline migration** – Point a subset of repositories to the new self‑hosted runner pool, monitor scaling behavior, and iterate on resource limits.  
4. **Full rollout** – Gradually expand to all projects, integrate monitoring/alerting, and lock down IAM roles and network policies.

**Production Readiness**  
The project scores high on production readiness: it has recent activity (last commit 2026‑07‑09), a healthy star/fork count, and a Go codebase that is easy to audit and containerize. While the license and security posture still need a final review, the active maintainer community and existing adopters make garm a solid candidate for a serious pilot in production environments.

### Русский

Резюме проекта cloudbase/garm:

Представляем cloudbase/garm - многообещающий open-source проект, управляющий облачными ресурсами для GitHub Actions и Gitea self-hosted runner. cloudbase/garm подходит для интеграции в конкретные рабочие процессы, поскольку он обеспечивает автомасштабирование и управление ресурсами в облаке с помощью плагинов-поставщиков. cloudbase/garm имеет высокий уровень готовности к production, что делает его подходящей альтернативой для серьезных пилотных проектов.

### 中文

**简短介绍**

cloudbase/garm 是一个开源项目，用于管理 GitHub Actions 和 Gitea 自托管运行器的多云自动扩缩。它支持可插拔的提供商，使其成为一个灵活的解决方案。

**价值**

cloudbase/garm 的价值在于它可以帮助用户在多个云平台上管理自托管运行器，实现自动扩缩和高可用性。它的 pluggable 设计使得用户可以轻松切换不同的云提供商。

**典型接入方式**

用户可以通过以下步骤接入 cloudbase/garm：

1. 检查 cloudbase/garm 的 README 文档和活动，以确定是否适合用户的工作流。
2. 开始一个小的 PoC（Proof of Concept）来评估 cloudbase/garm 的功能和性能。
3. 根据用户的需求配置 cloudbase/garm 的提供商和设置。

**生产可用性**

cloudbase/garm 的生产可用性较高，主要原因是：

* 近期活动：项目最近更新，表明仍然活跃。
* 采用：项目有

## 🧭 Practical evaluation

**Value:** cloudbase/garm may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 353 GitHub stars
- 49 forks
- updated 2026-07-09
- primary language: Go
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 54/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 73/100 |
| recency | 80/100 |
| adoption | 51/100 |
| production | 69/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-09 · [View on GitHub](https://github.com/cloudbase/garm) · [← Back to Cloud--storage](./README.md)</sub>
