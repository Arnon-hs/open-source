# andrius/asterisk

[![Stars](https://img.shields.io/github/stars/andrius/asterisk?style=flat-square&color=yellow)](https://github.com/andrius/asterisk/stargazers) [![Forks](https://img.shields.io/github/forks/andrius/asterisk?style=flat-square&color=blue)](https://github.com/andrius/asterisk/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> ✨📞 Asterisk PBX in 🐳 Docker — Smallest Asterisk ever! 🚀

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 392 |
| 🍴 **Forks** | 125 |
| 💻 **Language** | Shell |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-07-04 |
| 🔍 **Source** | github |

## 🏷️ Topics

`asterisk-pbx` `docker` `docker-image` `voip`

## 🎯 Categories

DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`andrius/asterisk` packages the Asterisk PBX into a minimal Docker container, offering the smallest‑footprint Asterisk image for quick spin‑up of telephony services. It streamlines repeatable deployments and automates routine operations, making it a handy tool for prototyping, internal testing, or low‑volume production use cases.  

**Value**  
- **Consistent, repeatable environments:** By containerising Asterisk, the project eliminates host‑specific quirks and ensures the same binary, configuration, and dependencies run everywhere.  
- **Speed and resource efficiency:** The image is deliberately tiny, reducing start‑up time and infrastructure costs—ideal for CI pipelines, automated tests, or edge‑deployed VoIP gateways.  
- **Operational automation:** The Docker‑based setup can be orchestrated with standard DevOps tooling (Docker Compose, Kubernetes, CI/CD), enabling automated scaling, health‑checks, and rolling updates without manual SIP‑server fiddling.  

**Practical Adoption Path**  
1. **Evaluation:** Pull the image (`docker pull andrius/asterisk`) and run a quick container with a sample `extensions.conf` to verify basic call routing.  
2. **Integration:** Add the container to your existing Docker Compose or Helm chart, exposing the required SIP (UDP/TCP) and management ports, and mount a persistent volume for configuration and call logs.  
3. **Automation:** Incorporate the container into your CI/CD pipeline to spin up a fresh PBX for each test run, or use an orchestration platform to manage scaling and fail‑over for internal services.  
4. **Hardening:** Review the Dockerfile for any unnecessary privileges, apply your organization’s security baseline (e.g., non‑root user, network policies), and add monitoring/logging agents as needed.  

**Production Readiness**  
- **Maturity:** Medium. The repo is actively maintained (last update 2026‑07‑04) with a solid community signal (≈ 400 ★, 125 forks).  
- **Suitability:** Well‑suited for prototypes, internal workflows, or low‑to‑moderate traffic PBX deployments. For high‑availability, large‑scale telephony, additional layers (load balancers, persistent storage, hardened OS images) and thorough security audits are recommended.  
- **Risks:** License compliance, security posture of the underlying base image, and the long‑term commitment of the maintainer need verification before mission‑critical production use.  

Overall, `andrius/asterisk` offers a quick, reproducible way to run Asterisk in containers, making it a practical building block for DevOps‑driven telephony projects, provided the necessary hardening and scalability considerations are addressed.

### Русский

**andrius/asterisk** — это минимальный образ Asterisk PBX в Docker, который позволяет быстро и последовательно разворачивать телефонные сервисы без необходимости ручной установки и настройки зависимостей. Типичный сценарий — стандартизированное развертывание Asterisk в тестовых стендах, прототипах или внутренних workflow, где важна автоматизация и повышенная надёжность инфраструктуры. Готовность к production — средняя: образ подходит для прототипов и ограниченных внутренних задач, но перед выводом в продакшн требуется проверка лицензии, безопасности и наличие активных мейнтейнеров.

### 中文

**简短介绍**

andrius/asterisk 是一个开源项目，提供了使用 Docker 部署 Asterisk PBX 的解决方案。它旨在使部署和运维更加可重复。

**价值**

和rius/asterisk 帮助开发者实现以下价值：

* 标准化部署
* 自动化运维
* 提高平台可靠性

**典型接入方式**

和rius/asterisk 提供了以下接入方式：

* API/SDK：通过 API 或 SDK 接入和rius/asterisk
* CLI：使用命令行界面（CLI）进行交互
* 语言元数据：支持多种语言的元数据

**生产可用性**

和rius/asterisk 的生产可用性为中等（Medium），适合用于原型或内部工作流程。建议在生产环境中进行依赖和维护检查后再使用。

## 🧭 Practical evaluation

**Value:** andrius/asterisk helps make deployment and operations more repeatable.

**Best use cases**

- standardize deployment
- automate operations
- improve platform reliability

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 392 GitHub stars
- 125 forks
- updated 2026-07-04
- primary language: Shell
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 53/100 |
| stars | 55/100 |
| topics | 50/100 |
| outlook | 72/100 |
| quality | 72/100 |
| recency | 100/100 |
| adoption | 54/100 |
| production | 74/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-04 · [View on GitHub](https://github.com/andrius/asterisk) · [← Back to DevOps & Infra](./README.md)</sub>
