# gnzsnz/ib-gateway-docker

[![Stars](https://img.shields.io/github/stars/gnzsnz/ib-gateway-docker?style=flat-square&color=yellow)](https://github.com/gnzsnz/ib-gateway-docker/stargazers) [![Forks](https://img.shields.io/github/forks/gnzsnz/ib-gateway-docker?style=flat-square&color=blue)](https://github.com/gnzsnz/ib-gateway-docker/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Docker image with IB Gateway/TWS and IBC

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.1k |
| 🍴 **Forks** | 217 |
| 💻 **Language** | Shell |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`algorithmic-trading` `docker` `ibgateway` `ibkr` `quant` `quantitative-finance` `trading` `trading-bot` `tws` `tws-api`

## 🎯 Categories

Trading · Automation · Backend · DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
gnzsnz/ib‑gateway‑docker packages Interactive Brokers’ Gateway/TWS and the IBC (IB Controller) into a ready‑to‑run Docker image, letting developers spin up a fully functional IB environment with a single `docker run` command. The container exposes the standard IB API/SDK endpoints, making it easy to integrate with back‑testing frameworks, algorithmic trading bots, or market‑monitoring pipelines.  

**Value**  
By containerising the IB Gateway and IBC, the project eliminates the tedious, error‑prone manual installation of Java, TWS, and configuration files, providing a reproducible, isolated environment that can be started, stopped, and version‑controlled like any other service. This accelerates research and automation of market workflows, enables rapid prototyping of trading strategies, and simplifies CI/CD pipelines for quantitative finance teams.  

**Practical Adoption Path**  
1. **Pull the image** – `docker pull ghcr.io/gnzsnz/ib-gateway-docker:latest`.  
2. **Configure credentials** – mount a small `config.ini` or set environment variables (`IBKR_USER`, `IBKR_PASSWORD`, `IBKR_TWS_PORT`).  
3. **Start the container** – `docker run -d -p 7497:7497 -v $HOME/.ib:/root/.ib ghcr.io/gnzsnz/ib-gateway-docker`.  
4. **Connect your code** – point your Python/Java/C# IB API client to `localhost:7497` (or the mapped port).  
5. **Integrate into pipelines** – use Docker Compose or Kubernetes to spin up the service alongside back‑testing or data‑ingestion containers, and shut it down after tests.  

**Production Readiness**  
- **Activity & Adoption**: 1,064 GitHub stars, 217 forks, recent commits (last update 2026‑06‑22), and active issue discussions indicate a healthy community.  
- **Stability**: The image bundles a specific, tested version of IB Gateway and IBC, and the Dockerfile is deterministic, reducing “works on my machine” problems.  
- **Observability**: Logs are streamed to the container’s stdout, and health‑check endpoints can be added via Docker Compose for automated restarts.  
- **Risks**: The project’s license, security scanning of the base image, and long‑term maintainer commitment still need a final audit, but no major red flags have been identified.  

Overall, gnzsnz/ib-gateway-docker is a mature, production‑ready OSS component that streamlines the deployment of Interactive Brokers’ gateway services, making it a solid foundation for research, back‑testing, and automated trading pipelines.

### Русский

**gnzsnz/ib-gateway-docker** — готовый Docker‑образ, включающий Interactive Brokers Gateway/TWS и IBC, позволяющий быстро развернуть полностью функциональную среду для исследования и автоматизации торговых стратегий. Типичный сценарий — запуск контейнера в CI/CD‑конвейере или в облачной инфраструктуре, подключение к API/SDK IB и использование его для бэктестов, мониторинга рыночных потоков и интеграции с собственными торговыми системами. Проект обладает высокой готовностью к production: активные коммиты, более 1000 звёзд, сотни форков, свежие обновления и широкая поддержка в сообществе, что делает его надёжным кандидатом для пилотных и масштабных внедрений.

### 中文

**项目简介**  
`gnzsnz/ib-gateway-docker` 是一个基于 Docker 的镜像，预装了 Interactive Brokers 的 IB Gateway/TWS 与 IBC（IB Controller），旨在为量化研究与交易自动化提供即插即用的运行环境。

**价值**  
- **快速搭建**：无需手动安装 IB Gateway/TWS，直接拉取镜像即可在本地或云端启动，极大缩短环境准备时间。  
- **统一化部署**：Docker 化后可在 CI/CD 流水线、K8s 集群或普通服务器上统一管理，保证开发、回测、实盘环境的一致性。  
- **可靠性**：镜像内已集成 IBC 自动登录、会话保持和日志轮转，降低因网络或会话失效导致的中断风险。

**典型接入方式**  
1. **Docker Run**（最简方式）  
   ```bash
   docker run -d --name ib-gateway \
       -p 7496:7496 -p 4002:4002 \
       -e IBC_USERNAME=your_user \
       -e IBC_PASSWORD=your_pass \
       gnzsnz/ib-gateway-docker
   ```  
   - `7496` 为 TWS/IB Gateway API 端口，`4002` 为 IBC 控制端口。  
2. **Docker‑Compose**（多服务协同）  
   ```yaml
   version: "3.8"
   services:
     ib-gateway:
       image: gnzsnz/ib-gateway-docker
       ports:
         - "7496:7496"
         - "4002:4002"
       environment:
         IBC_USERNAME: ${IB_USER}
         IBC_PASSWORD: ${IB_PASS}
       restart: unless-stopped
   ```  
   可与策略回测容器、数据库或消息队列一起编排，实现完整的交易工作流。  
3. **Kubernetes**（大规模或高可用）  
   - 将镜像部署为 `Deployment`，配合 `Service` 暴露 API 端口；使用 `livenessProbe` 检查 IBC 状态，配合 `HorizontalPodAutoscaler` 实现弹性伸缩。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑22，项目最近一次提交在当天，拥有 1 064 星、217 fork，社区活跃。  
- **成熟度**：镜像已内置 IBC 自动登录、日志轮转、健康检查等生产级特性，适合作为正式交易系统的网关层。  
- **风险**：目前未发现重大许可证或安全漏洞，但仍建议在投产前完成以下步骤：  
  1. **审计镜像**（使用 Trivy、Syft 等工具检查依赖漏洞）。  
  2. **确认许可证**（项目采用的开源许可证是否符合贵公司合规要求）。  
  3. **监控与告警**（对 `ib-gateway` 容器的 CPU、内存、网络以及 IBC 心跳进行监控）。  

综上，`gnzsnz/ib-gateway-docker` 提供了即开即用、易于集成且在社区和更新频率上都具备生产级别的可靠性，是构建 IB 交易自动化系统的理想底层组件。

## 🧭 Practical evaluation

**Value:** gnzsnz/ib-gateway-docker helps research and automate market workflows.

**Best use cases**

- research trading systems
- backtest strategies
- monitor market workflows

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1064 GitHub stars
- 217 forks
- updated 2026-06-22
- primary language: Shell
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 58/100 |
| stars | 64/100 |
| topics | 100/100 |
| outlook | 61/100 |
| quality | 68/100 |
| recency | 40/100 |
| adoption | 63/100 |
| production | 62/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/gnzsnz/ib-gateway-docker) · [← Back to Trading](./README.md)</sub>
