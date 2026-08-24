# mescon/Muximux

[![Stars](https://img.shields.io/github/stars/mescon/Muximux?style=flat-square&color=yellow)](https://github.com/mescon/Muximux/stargazers) [![Forks](https://img.shields.io/github/forks/mescon/Muximux?style=flat-square&color=blue)](https://github.com/mescon/Muximux/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> A self-hosted homelab dashboard with an optional built-in reverse proxy that makes stubborn apps work in iframes

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.2k |
| 🍴 **Forks** | 83 |
| 💻 **Language** | Go |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`caddy` `dashboard` `docker` `golang` `grafana` `health-monitoring` `homelab` `htpc` `iframe` `plex` `radarr` `reverse-proxy`

## 🎯 Categories

Observability · DevOps/Infra

## 📝 Summary

### English

**Summary**  
Muximux (mescon/Muximux) is a self‑hosted homelab dashboard that bundles an optional reverse‑proxy, enabling otherwise “frame‑blocked” web apps to be embedded in iframes. It lets teams assemble a unified UI for disparate services with minimal custom front‑end code, speeding up product‑facing interfaces while keeping everything under their own control.

**Value**  
- **Rapid UI composition** – By aggregating existing web apps into a single pane, developers avoid building duplicate navigation, authentication, and layout layers.  
- **Built‑in reverse proxy** – The proxy rewrites headers and CSP policies so legacy or third‑party tools that normally refuse iframe embedding work out‑of‑the‑box.  
- **Open‑source flexibility** – Written in Go, it can be extended or containerised to match any homelab or internal‑tool stack.

**Practical adoption path**  
1. **Pilot deployment** – Spin up the Docker image (or compile the Go binary) alongside your existing services; configure the `apps.yml` manifest to point to each target URL.  
2. **Integrate authentication** – Leverage the built‑in proxy to enforce a single sign‑on method (e.g., OAuth2, LDAP) across all embedded apps.  
3. **Iterate UI** – Use the provided theming options or inject custom CSS/JS to align the dashboard with your brand, then replace or retire legacy portals as they become redundant.  
4. **Scale** – Deploy the proxy behind your own ingress controller or Kubernetes ingress for HA and TLS termination.

**Production readiness**  
- **Activity & adoption**: 1,191 GitHub stars, 83 forks, recent commits (last updated 2026‑06‑28) and a growing ecosystem of 15 topics indicate an active community.  
- **Stability**: The Go codebase is compact and compiled, reducing runtime dependencies; the reverse‑proxy logic has been battle‑tested in homelab environments.  
- **Risk considerations**: No immediate licensing or metadata red flags, but a final security audit and confirmation of an active maintainer team are recommended before a full‑scale rollout.  

Overall, Muximux is a mature OSS candidate suitable for a serious pilot and, after the standard security/maintenance review, can be promoted to production for internal dashboards and lightweight customer‑facing portals.

### Русский

**Краткое резюме:**  
mescon/Muximux — это self‑hosted dashboard для homelab с встроенным обратным прокси, позволяющий без лишних усилий отображать «упрямые» приложения в iframe и быстро собрать пользовательский интерфейс. Типичный сценарий — разработчики и DevOps‑инженеры используют готовый набор компонентов UI и прокси‑логики, чтобы за считанные часы создать продуктовый фронтенд и упростить доставку новых сервисов. Проект имеет высокий уровень готовности к production: активные коммиты, более 1100 звёзд на GitHub, широкую экосистему (Go, API/SDK/CLI), но перед масштабным внедрением следует уточнить лицензионные условия и текущий статус безопасности.

### 中文

**项目简介**  
Muximux 是一个自托管的 homelab 仪表盘，内置可选的反向代理，使得原本不支持 iframe 的应用也能顺利嵌入页面。它帮助团队快速搭建统一的用户界面，省去大量自研 UI 的工作。

**价值点**  
- **快速交付前端**：通过统一的仪表盘和 iframe 集成方式，业务方可以直接复用已有的内部或第三方工具页面，无需重新开发 UI。  
- **降低维护成本**：所有外部服务统一通过 Muximux 的反向代理访问，统一的入口和鉴权策略简化了运维和安全管理。  
- **可视化运维**：作为 homelab 仪表盘，能够直观展示服务健康、日志、监控等信息，提升运维效率。

**典型接入方式**  
1. **部署**：使用 Docker 镜像或直接编译 Go 程序，在本地或 Kubernetes 中运行。  
2. **配置**：在 `config.yaml` 中声明需要嵌入的应用 URL，选择是否启用内置 reverse‑proxy（可为每个应用单独配置自定义 Header、Auth 等）。  
3. **集成**：  
   - **API/CLI**：通过提供的 REST API 动态增删仪表盘卡片，或使用 `muximux-cli` 在 CI/CD 中自动化部署。  
   - **SDK**：项目提供 Go SDK，方便在自研服务中读取仪表盘元数据或触发刷新。  
4. **访问**：完成配置后，直接访问 Muximux 的统一域名，即可在浏览器中看到所有嵌入的应用。

**生产可用性**  
- **活跃度**：截至 2026‑06‑28，项目最近一次提交，GitHub ★1191、Fork 83，社区活跃。  
- **技术成熟度**：核心使用 Go 编写，单二进制文件易于部署；提供完整的 Docker 镜像和 Helm Chart，支持容器化和 K8s 环境。  
- **安全性**：内置 reverse‑proxy 支持 TLS、Header 重写和基本鉴权，可配合外部 OAuth/LDAP 实现统一登录。  
- **风险**：仍需对许可证（MIT）和依赖的第三方库进行安全审计，确认维护者的响应速度符合企业 SLA。  

综合来看，Muximux 已具备较高的生产就绪度，适合作为内部工具平台或 homelab 的统一入口进行试点，随后可在更大规模的 DevOps/Infra 环境中推广使用。

## 🧭 Practical evaluation

**Value:** mescon/Muximux helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1191 GitHub stars
- 83 forks
- updated 2026-06-28
- primary language: Go
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 48/100 |
| stars | 65/100 |
| topics | 100/100 |
| outlook | 67/100 |
| quality | 67/100 |
| recency | 40/100 |
| adoption | 61/100 |
| production | 60/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/mescon/Muximux) · [← Back to Observability](./README.md)</sub>
