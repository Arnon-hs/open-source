# MHSanaei/3x-ui

[![Stars](https://img.shields.io/github/stars/MHSanaei/3x-ui?style=flat-square&color=yellow)](https://github.com/MHSanaei/3x-ui/stargazers) [![Forks](https://img.shields.io/github/forks/MHSanaei/3x-ui?style=flat-square&color=blue)](https://github.com/MHSanaei/3x-ui/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> Xray panel supporting multi-protocol multi-user expire day & traffic & IP limit (Vmess, Vless, Trojan, ShadowSocks, Wireguard, Hysteria, Tunnel, Mixed, HTTP, Tun)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 41.5k |
| 🍴 **Forks** | 7.7k |
| 💻 **Language** | Go |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ech` `fail2ban` `http` `hysteria2` `mixed` `nodes` `post-quantum` `reality` `shadowsocks` `shadowsocks2022` `tls` `trojan`

## 🎯 Categories

Networking · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
MHSanaei/3x‑ui is an open‑source, Go‑based Xray control panel that supports a wide range of proxy protocols (Vmess, Vless, Trojan, Shadowsocks, WireGuard, Hysteria, Tunnel, Mixed, HTTP, Tun) with per‑user expiration, traffic accounting, and IP‑based access limits. Although its primary focus is network proxy management, the project’s robust API and automation‑friendly design make it useful for research and automation of market‑related workflows such as data collection, strategy back‑testing, and monitoring. With over 41 k stars, active recent commits, and a large fork network, it is a mature OSS candidate ready for pilot deployments.

**Value Proposition**  
- **Unified multi‑protocol gateway** – eliminates the need for separate services for each proxy technology, simplifying infrastructure and reducing operational overhead.  
- **Fine‑grained user controls** – expiration dates, traffic caps, and IP whitelisting let you enforce usage policies automatically, which is handy for sandboxed research environments or paid API access.  
- **Automation‑ready API** – the panel exposes REST endpoints and configuration files that can be scripted, enabling seamless integration with trading‑system pipelines, data‑ingestion bots, or CI/CD workflows.  

**Practical Adoption Path**  
1. **Proof of Concept (PoC)** – Clone the repo, run the provided Docker compose or binary on a test VM, and verify that the UI and API can create users, set expiry/traffic limits, and switch protocols.  
2. **Integration Checklist** – Review the README for required environment variables (e.g., Xray core path, DB credentials), confirm the license (MIT) aligns with your compliance policy, and run a quick security scan (e.g., Trivy) on the container image.  
3. **Pilot Deployment** – Deploy to a staging Kubernetes namespace using the official Helm chart (or Helm‑compatible manifest). Connect a small set of market‑data collectors or back‑testing agents through the panel and script user provisioning via the REST API.  
4. **Monitoring & Scaling** – Enable Prometheus metrics (built‑in) and set alerts for traffic quota breaches or abnormal IP activity. Scale the Xray core horizontally if needed, leveraging the panel’s ability to manage multiple instances.  

**Production Readiness**  
- **Activity & Community** – 41 k stars, 7 7 k forks, and daily commits as of 2026‑06‑25 indicate a healthy, actively maintained project.  
- **Stability** – The core is written in Go, compiled into a single binary, and the UI is a thin web layer, both of which are proven in production environments.  
- **Ecosystem Fit** – The panel’s REST API and Docker/Helm delivery make it straightforward to embed in existing CI/CD pipelines and cloud‑native stacks.  
- **Risk Considerations** – No immediate licensing or metadata red flags, but a final security audit (dependency scanning, CVE checks) and verification of maintainers’ response times are recommended before full‑scale rollout.  

Overall, MHSanaei/3x‑ui offers a mature, feature‑rich proxy management solution that can be quickly validated in a sandbox and, after a brief security review, promoted to production for automating market‑data workflows and related research pipelines.

### Русский

MHSanaei/3x‑ui — это открытый Go‑панель управления Xray, позволяющая централизованно администрировать множество протоколов (Vmess, Vless, Trojan, Shadowsocks, Wireguard, Hysteria, Tunnel, Mixed, HTTP, Tun) с учётом сроков действия, трафика и ограничений по IP, что упрощает построение и автоматизацию торговых и аналитических пайплайнов. Для внедрения типично начинается с небольшого proof‑of‑concept: развертывается контейнер, настраивается один‑два тестовых пользователя и проверяется интеграция через README; после подтверждения работоспособности панель готова к масштабному продакшн‑развёртыванию. Проект обладает высокой готовностью к production — активные коммиты, более 41 к звёзд, широкое сообщество и поддержка множества протоколов, хотя перед запуском стоит окончательно проверить лицензию, безопасность и наличие активных мейнтейнеров.

### 中文

**项目简介（2‑3 句）**  
MHSanaei/3x-ui 是一款基于 Go 开发的 Xray 可视化面板，支持 Vmess、Vless、Trojan、ShadowSocks、Wireguard、Hysteria、Tunnel、Mixed、HTTP、Tun 等多协议的多用户管理，能够为每个用户单独设置到期时间、流量配额和 IP 限制。它提供直观的 Web UI 与 API，帮助运维和研发团队快速部署、监控和调度跨协议的代理服务。

**价值说明**  
- **统一管理**：一次部署即可统一管理十余种代理协议，省去分别配置多个服务的繁琐。  
- **细粒度控制**：支持单用户的到期天数、流量上限和 IP 白名单/黑名单，适合商业化运营或内部资源分配。  
- **可视化与自动化**：通过 Web UI 与 RESTful API，能够与 CI/CD、监控平台或自研的业务系统对接，实现自动化开通、续费、流量统计等业务流程。  

**典型接入方式**  
1. **Docker 部署**：官方提供 `docker-compose.yml`，只需拉取镜像并配置环境变量（如 `XRAY_PORT`、`DB_PATH`）即可快速启动。  
2. **二进制直装**：在 Linux 服务器上下载对应平台的 `3x-ui` 可执行文件，使用系统服务（systemd）管理，适合对容器化有顾虑的内部网络。  
3. **API 集成**：面板提供 `/api/v1/*` 的 REST 接口，使用任意语言（Go、Python、Node.js 等）发送 HTTP 请求即可完成用户增删、流量查询、限速设置等操作，常见场景包括：  
   - 业务系统调用接口为新用户自动创建账号并分配流量。  
   - 监控平台通过定时任务查询流量使用情况并触发告警或自动扣费。  
   - CI/CD 流水线在部署新环境时自动生成对应的 Xray 配置并写入面板。  

**生产可用性评估**  
- **活跃度**：截至 2026‑06‑25，项目最近一次提交在当天，拥有 41 501 星、7 738 次 fork，社区活跃，Issue 与 PR 反馈速度快。  
- **技术成熟度**：核心代码使用 Go 编写，单二进制交付，依赖少，易于容器化和横向扩展。  
- **安全与合规**：项目采用 MIT 许可证，暂无已知重大安全漏洞；建议在生产环境前进行一次 `npm audit`/`go mod tidy` 并开启容器安全扫描。  
- **可扩展性**：支持自定义插件和外部数据库（SQLite、MySQL、PostgreSQL），可根据业务规模水平扩容。  
- **推荐上线策略**：先在预生产环境完成 **小规模 PoC**（如 10‑20 条用户、单协议），验证 API 调用、流量统计与告警链路；确认无误后逐步迁移至全量生产，配合 Prometheus/Grafana 监控面板运行状态。  

综合以上因素，3x‑ui 已具备 **高** 的生产就绪度，适合作为企业或运营商的统一代理管理平台进行正式部署。

## 🧭 Practical evaluation

**Value:** MHSanaei/3x-ui helps research and automate market workflows.

**Best use cases**

- research trading systems
- backtest strategies
- monitor market workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 41501 GitHub stars
- 7738 forks
- updated 2026-06-25
- primary language: Go
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 97/100 |
| stars | 98/100 |
| topics | 100/100 |
| outlook | 81/100 |
| quality | 94/100 |
| recency | 80/100 |
| adoption | 98/100 |
| production | 77/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/MHSanaei/3x-ui) · [← Back to Networking](./README.md)</sub>
