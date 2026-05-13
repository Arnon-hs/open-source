# xubiaolin/docker-zerotier-planet

[![Stars](https://img.shields.io/github/stars/xubiaolin/docker-zerotier-planet?style=flat-square&color=yellow)](https://github.com/xubiaolin/docker-zerotier-planet/stargazers) [![Forks](https://img.shields.io/github/forks/xubiaolin/docker-zerotier-planet?style=flat-square&color=blue)](https://github.com/xubiaolin/docker-zerotier-planet/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> 一分钟私有部署zerotier-planet服务

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4k |
| 🍴 **Forks** | 740 |
| 💻 **Language** | Shell |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`dockerfile` `planet` `self-host-zerotier` `self-hosted` `zerotier` `zerotier-network`

## 🎯 Categories

DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
`xubiaolin/docker-zerotier-planet` provides a ready‑to‑run Docker image that spins up a private Zerotier‑Planet controller in under a minute, turning Zerotier’s global network into a self‑hosted, fully controllable overlay. With 4 k+ stars and active maintenance, it offers a repeatable, scriptable way to standardise and automate Zerotier deployments for on‑prem or cloud environments.

**Value**  
- **Repeatable deployment** – The Docker‑based approach eliminates manual configuration steps, ensuring every environment (dev, test, prod) gets an identical Zerotier‑Planet instance.  
- **Operational automation** – The container can be orchestrated with CI/CD pipelines, Terraform, or Kubernetes, allowing automated scaling, upgrades, and health‑checks.  
- **Reliability & control** – Running your own Planet server removes dependence on the public Zerotree service, giving you full control over network policies, routing, and data residency.

**Practical Adoption Path**  
1. **Evaluate** – Pull the image (`docker pull xubiaolin/zerotier-planet`) and run a quick test container to verify connectivity with your existing Zerotier clients.  
2. **Integrate** – Add the container to your infrastructure‑as‑code (Docker Compose, Helm chart, or Terraform `docker_container` resource) and expose the required ports (9993/9994).  
3. **Configure** – Use the provided CLI or REST API to create and manage networks, then point your devices’ Zerotier clients to the private Planet URL.  
4. **Automate** – Embed the start‑up script in your CI pipeline, schedule regular backups of the Planet database, and monitor health via Prometheus exporters or Docker health checks.  

**Production Readiness**  
- **Activity & Adoption** – The repo shows recent commits (as of 2026‑05‑13), 4 k+ stars, 740 forks, and a vibrant issue/PR community, indicating strong user interest and ongoing maintenance.  
- **Maturity** – The implementation is pure Shell with a single Dockerfile, making the attack surface small and the build process transparent.  
- **Risk Considerations** – While no licensing or major security red flags appear, a final audit of the underlying Zerotier binaries, container base image, and the project’s contribution guidelines is recommended before a full‑scale rollout.  

Overall, the project is production‑ready for a serious pilot, offering a low‑friction path to self‑hosted Zerotier networking with the benefits of repeatable, automated deployment.

### Русский

**xubiaolin/docker-zerotier-planet** — это готовый Docker‑образ, позволяющий за минуту развернуть собственный сервис zerotier‑planet в приватной сети, что делает процесс установки и последующего управления полностью повторяемым и автоматизируемым. Он идеально подходит для стандартизации развертывания Zerotier‑контроллеров, ускорения операций и повышения надёжности инфраструктуры, при этом имеет высокий уровень готовности к продакшн: активные коммиты, более 4000 звёзд, 740 форков и свежие обновления (2026‑05‑13).

### 中文

**项目简介（2‑3 句）**  
xubiaolin/docker-zerotier-planet 是一个基于 Docker 的 Zerotier‑Planet 私有化部署方案，利用官方镜像和一键脚本即可在一分钟内完成服务搭建。它将 Zerotier 的全局控制平面封装为容器，便于在企业内网或云环境中快速构建安全的 SD‑WAN 网络。

**价值**  
- **部署可重复**：通过 Docker Compose/单文件镜像实现“一键启动”，避免手工配置差异。  
- **运维自动化**：支持环境变量自定义、日志统一输出，可与 CI/CD 流程无缝集成。  
- **平台可靠性**：容器化隔离提升服务可用性，故障恢复仅需重新启动容器即可。

**典型接入方式**  
1. **Docker Compose**：在 `docker-compose.yml` 中声明 `zerotier-planet` 服务，配置 `ZEROTIER_NETWORK_ID`、`ZEROTIER_TOKEN` 等环境变量。  
2. **Kubernetes**：将镜像包装为 Deployment + Service，使用 ConfigMap 注入配置文件，实现弹性伸缩。  
3. **CLI/脚本**：通过 `docker run` 或项目提供的 `install.sh` 脚本直接启动，适合单机或轻量实验环境。

**生产可用性**  
- **活跃度**：截至 2026‑05‑13，项目最近一次提交，拥有 4010+ 星、740+ Fork，社区活跃。  
- **技术成熟度**：核心实现使用 Shell，依赖官方 Zerotier 镜像，容器化程度高，易于监控和日志收集。  
- **风险评估**：暂无重大许可证或安全漏洞报告，仍需自行审计镜像安全和长期维护者的响应速度。总体而言，已具备在内部生产环境进行试点或正式上线的条件。

## 🧭 Practical evaluation

**Value:** xubiaolin/docker-zerotier-planet helps make deployment and operations more repeatable.

**Best use cases**

- standardize deployment
- automate operations
- improve platform reliability

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 4010 GitHub stars
- 740 forks
- updated 2026-05-13
- primary language: Shell
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 72/100 |
| stars | 77/100 |
| topics | 75/100 |
| outlook | 83/100 |
| quality | 85/100 |
| recency | 100/100 |
| adoption | 75/100 |
| production | 78/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/xubiaolin/docker-zerotier-planet) · [← Back to DevOps & Infra](./README.md)</sub>
