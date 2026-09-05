# nginx-proxy/nginx-proxy

[![Stars](https://img.shields.io/github/stars/nginx-proxy/nginx-proxy?style=flat-square&color=yellow)](https://github.com/nginx-proxy/nginx-proxy/stargazers) [![Forks](https://img.shields.io/github/forks/nginx-proxy/nginx-proxy?style=flat-square&color=blue)](https://github.com/nginx-proxy/nginx-proxy/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> Automated Nginx Reverse Proxy for Docker

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 19.9k |
| 🍴 **Forks** | 3.1k |
| 💻 **Language** | Python |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`docker` `docker-gen` `nginx` `reverse-proxy`

## 🎯 Categories

Networking · DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
nginx‑proxy/nginx‑proxy is an open‑source tool that automatically creates and updates an Nginx reverse‑proxy configuration for Docker containers, turning ad‑hoc container networking into a repeatable, declarative deployment pattern. With strong community adoption (≈20 k stars, 3 k forks) and recent activity, it is a mature candidate for production pilots that need standardized, reliable proxy management.  

**Value**  
By generating Nginx virtual‑host files on‑the‑fly from Docker container metadata, the project eliminates manual proxy configuration, reduces human error, and ensures that new services are instantly reachable behind a single, centrally‑managed endpoint. This standardization speeds up onboarding of micro‑services, improves platform reliability, and frees DevOps teams to focus on higher‑level automation rather than low‑level networking tweaks.  

**Practical Adoption Path**  
1. **Evaluation** – Pull the Docker image (`jwilder/nginx-proxy`) and run it alongside your existing Docker host; the proxy listens on port 80/443 and watches the Docker socket for container events.  
2. **Integration** – Add the required environment variables (`VIRTUAL_HOST`, `VIRTUAL_PORT`, optional TLS settings) to each service you want exposed.  
3. **Testing** – Verify that Nginx configuration updates correctly when containers start, stop, or change labels; use the built‑in health‑check endpoint to confirm proxy health.  
4. **Production Roll‑out** – Deploy the proxy as a highly‑available service (e.g., behind a load balancer or using Docker Swarm/Kubernetes with a host‑network mode) and gradually migrate existing services to the automated workflow.  

**Production Readiness**  
The project scores high on production readiness: it shows continuous commits (last update 2026‑06‑27), a large and active user base, and clear API/CLI signals for integration. While the license and security posture still require a final audit, the combination of strong community support, frequent releases, and proven use in many public deployments makes nginx‑proxy a solid OSS candidate for serious pilot projects and, ultimately, full‑scale production environments.

### Русский

Резюме проекта nginx-proxy/nginx-proxy:

nginx-proxy/nginx-proxy - автоматизированный обратный прокси Nginx для Docker, который упрощает повторяемость развертывания и эксплуатации. Он идеально подходит для стандартизации развертывания, автоматизации операций и улучшения надежности платформы. Проект готов к использованию в production, обладает высокой степенью готовности (High) и сильным экосистемным потенциалом.

### 中文

**简短介绍**  
nginx‑proxy/nginx‑proxy 是一个自动化的 Nginx 反向代理工具，专为 Docker 环境设计，能够在容器启动或停止时自动生成并更新 Nginx 配置，实现零手动干预的负载均衡与路由。它帮助团队把部署和运维流程标准化、可重复，从而提升平台的可靠性和交付速度。

**价值**  
- **部署统一**：通过 Docker 环境变量或标签即能让新服务自动加入代理，无需手动编辑 Nginx 配置。  
- **运维自动化**：容器生命周期变化会即时触发 Nginx 重载，降低人为错误和运维成本。  
- **平台可靠性**：统一的入口与健康检查机制，使得服务故障时能够快速切流，提升整体可用性。

**典型接入方式**  
1. **Docker‑Compose / Swarm**：在 `docker-compose.yml` 中加入 `jwilder/nginx-proxy`（官方镜像），并在需要暴露的服务容器上设置 `VIRTUAL_HOST`、`VIRTUAL_PORT` 等环境变量。  
2. **Kubernetes**：使用 `nginx-proxy` 的 Helm Chart 或者将其作为 sidecar，配合 `Ingress` 注解实现同样的自动化路由。  
3. **CLI / API**：通过 `docker-gen`（nginx‑proxy 内部使用）或自定义脚本，实时生成 Nginx 配置文件并调用 `nginx -s reload` 完成热更新。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑27，项目拥有近 2 万星、3000+ Fork，最近一次提交在同一天，表明社区和维护者仍在积极维护。  
- **成熟生态**：已被多个大型企业和开源项目在生产环境中采用，具备完整的 Docker‑Compose、Swarm、Kubernetes 示例。  
- **风险点**：需要进一步审查许可证兼容性、容器安全基线以及核心维护者的响应时效，但整体信号表明该项目已具备在正式生产环境中进行试点的条件。

## 🧭 Practical evaluation

**Value:** nginx-proxy/nginx-proxy helps make deployment and operations more repeatable.

**Best use cases**

- standardize deployment
- automate operations
- improve platform reliability

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 19863 GitHub stars
- 3053 forks
- updated 2026-06-27
- primary language: Python
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 87/100 |
| stars | 91/100 |
| topics | 50/100 |
| outlook | 74/100 |
| quality | 83/100 |
| recency | 80/100 |
| adoption | 90/100 |
| production | 75/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/nginx-proxy/nginx-proxy) · [← Back to Networking](./README.md)</sub>
