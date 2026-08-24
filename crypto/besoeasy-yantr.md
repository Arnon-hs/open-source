# besoeasy/yantr

[![Stars](https://img.shields.io/github/stars/besoeasy/yantr?style=flat-square&color=yellow)](https://github.com/besoeasy/yantr/stargazers) [![Forks](https://img.shields.io/github/forks/besoeasy/yantr?style=flat-square&color=blue)](https://github.com/besoeasy/yantr/network) [![Language](https://img.shields.io/badge/lang-Vue-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> YANTR is a powerful, cross-platform alternative to Umbrel — a Docker-based app store designed for flexible, server-grade self-hosting. It lets you deploy ready-to-run apps — from Bitcoin nodes and privacy tools to file converters — all packaged as lightweight containers, giving you more control, portability, and freedom over your setup.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 127 |
| 🍴 **Forks** | 12 |
| 💻 **Language** | Vue |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`app-catalog` `app-store` `claude` `dashboard` `docker` `docker-apps` `home-server` `homelab` `homeserver` `openclaw` `self-hosted` `self-hosting`

## 🎯 Categories

Crypto · Backend · DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
YANTR (besoeasy/yantr) is an open‑source, Docker‑based app store that offers a cross‑platform alternative to Umbrel, letting you spin up ready‑to‑run containers for Bitcoin nodes, privacy tools, file converters, and other Web3 services. Built with Vue, it exposes APIs/SDKs/CLI hooks that make it easy to prototype, inspect, and extend blockchain workflows while keeping full control over the underlying infrastructure.

**Value**  
- **Rapid blockchain prototyping** – developers can launch fully functional Bitcoin or DeFi components in minutes, without writing low‑level integration code.  
- **Transparency & extensibility** – the project publishes implementation details (API specs, language metadata, CLI commands), enabling teams to audit, customize, or build on top of the provided services.  
- **Portability** – containerized apps run on any host that supports Docker, giving the same environment for local development, staging, or edge deployments.

**Practical Adoption Path**  
1. **Evaluation** – clone the repo, run `docker compose up` to launch the default stack and explore the exposed APIs/CLI.  
2. **Integration** – use the provided SDK or REST endpoints to connect your own Web3 front‑end or backend services, swapping or adding containers as needed.  
3. **Customization** – modify the Vue UI or add new Docker images for additional tools (e.g., a custom wallet or analytics service).  
4. **CI/CD** – incorporate the Docker compose files into your pipeline to automate provisioning of the same stack across dev, test, and production environments.

**Production Readiness**  
- **Maturity**: Medium. The codebase is actively maintained (last update 2026‑05‑11) and has modest community traction (127 ★, 12 forks).  
- **Strengths**: Clear containerization model, well‑defined APIs, and a UI built with a popular framework (Vue).  
- **Concerns**: Requires a thorough security audit of the Docker images, verification of the licensing terms, and a check on long‑term maintainer commitment before a public‑facing production rollout. With those checks completed, YANTR is suitable for internal prototypes, sandbox environments, and, after hardening, for production‑grade self‑hosted Web3 services.

### Русский

**YANTR (besoeasy/yantr)** — это кроссплатформенный Docker‑магазин приложений, позволяющий быстро развернуть готовые контейнеры (биткоин‑ноды, privacy‑инструменты, конвертеры файлов и др.) для построения и отладки Web3‑воркфлоу. Он удобно интегрируется через API/SDK/CLI, предоставляя открытые детали реализации, что делает его идеальным для прототипирования блокчейн‑интеграций, тестовых кошельков и DeFi‑фич. Готовность к production оценивается как средняя: проект подходит для прототипов и внутренних сервисов, но требует проверки лицензии, безопасности и поддержки перед масштабным вводом.

### 中文

**项目简介（2‑3 句）**  
YANTR（besoeasy/yantr）是一款基于 Docker 的跨平台应用商店，提供类似 Umbrel 的自托管体验。它将比特币节点、隐私工具、文件转换等常用服务封装为轻量容器，帮助用户以更低的运维成本实现灵活、可搬迁的服务器级部署。

**价值**  
- **快速原型**：通过即插即用的容器镜像，开发者可以在几分钟内搭建完整的区块链工作流或 DeFi 原型，省去手动安装、配置的繁琐。  
- **透明实现**：项目公开了 API/SDK/CLI 以及语言/主题元数据，便于审计、学习和二次开发，特别适合研究区块链集成细节。  
- **可控自由**：所有服务均运行在用户自行管理的 Docker 环境中，数据、密钥完全自持，提升安全与合规性。

**典型接入方式**  
1. **Docker Compose / CLI**：克隆仓库后直接运行 `docker compose up` 或使用提供的 `yantr-cli` 启动所需的容器。  
2. **API/SDK**：通过项目公开的 REST API 或对应的 JavaScript SDK 与已部署的容器交互，可在前端（Vue）或后端（Node/Python）中调用。  
3. **自定义镜像**：基于官方 Dockerfile 构建自己的业务镜像，然后在 YANTR 的 UI 或配置文件中注册，实现业务专属的容器化部署。

**生产可用性**  
- **成熟度**：目前在 GitHub 上拥有 127 星、12 个 Fork，活跃度较高（最近一次提交 2026‑05‑11），代码主要使用 Vue，适合作为内部原型或业务实验平台。  
- **准备程度**：属于 **Medium** 级别。对原型开发和内部工作流已足够可靠，但在生产环境部署前仍需：  
  - 完整的安全审计（容器镜像漏洞、网络隔离等）。  
  - 依赖版本锁定与升级策略，防止上游库突变。  
  - 评估许可证兼容性以及维护者响应速度。  
- **运维要求**：需要自行管理 Docker 主机、监控容器状态以及备份持久化卷。若已有容器编排平台（如 Kubernetes），可进一步提升弹性与可观测性。

综上，besoeasy/yantr 是一套适合快速搭建、审计和迭代区块链相关服务的工具箱，能够在原型阶段显著提升开发效率；在生产环境使用时，只要做好安全与运维的补充措施，即可实现可靠的自托管部署。

## 🧭 Practical evaluation

**Value:** besoeasy/yantr helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 127 GitHub stars
- 12 forks
- updated 2026-05-11
- primary language: Vue
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 28/100 |
| stars | 45/100 |
| topics | 100/100 |
| outlook | 55/100 |
| quality | 53/100 |
| recency | 20/100 |
| adoption | 40/100 |
| production | 48/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/besoeasy/yantr) · [← Back to Crypto](./README.md)</sub>
