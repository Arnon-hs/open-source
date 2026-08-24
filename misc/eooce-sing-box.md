# eooce/Sing-box

[![Stars](https://img.shields.io/github/stars/eooce/Sing-box?style=flat-square&color=yellow)](https://github.com/eooce/Sing-box/stargazers) [![Forks](https://img.shields.io/github/forks/eooce/Sing-box?style=flat-square&color=blue)](https://github.com/eooce/Sing-box/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> 既然来了，就留下你的Star吧！Serv00 | CT8 | Hostuno | VPS | 游戏机 | sing-box(reality + hy2 + vmess-argo +tuic5)四合一无交互一键安装脚本(已适配Alpine)，支持纯V6 vps，丰富的分流服务

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4.6k |
| 🍴 **Forks** | 1.6k |
| 💻 **Language** | Shell |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`argo` `hysteria2` `oneclick` `reality` `serv00` `sing-box` `tuic` `tunnel` `vmess-ws-tls`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
Sing‑box is an all‑in‑one, non‑interactive installation script (compatible with Alpine) that bundles the Reality, hy2, vmess‑argo and tuic5 protocols into a single package, supporting pure IPv6 VPS and a rich set of traffic‑splitting services. The project is actively maintained, has over 4,500 stars and 1,600 forks, and is positioned as a developer‑friendly tool for quickly delivering user‑facing network‑proxy interfaces with minimal custom UI work.

**Value**  
- **Speed to market:** By providing a ready‑made, one‑click deployment of multiple proxy protocols, teams can focus on building the product UI rather than wiring low‑level networking components.  
- **Reusability:** The script exposes a clear CLI/API surface that can be invoked from CI pipelines or integrated into custom front‑ends, enabling consistent UI components across projects.  
- **Flexibility:** Supports IPv6‑only environments and Alpine Linux, making it suitable for modern cloud/VPS stacks and edge deployments.

**Practical adoption path**  
1. **Evaluation:** Clone the repo and run the one‑click installer on a test VPS (Docker or a lightweight Alpine VM). Verify that the desired protocols (Reality, hy2, vmess‑argo, tuic5) are up and reachable.  
2. **Integration:** Use the provided CLI/REST endpoints to start, stop, and query tunnel status from your frontend code or automation scripts.  
3. **Customization:** Extend the default configuration files to match your product’s routing rules or UI branding, then package the script into your CI/CD pipeline for automated provisioning.  
4. **Production rollout:** Deploy the configured instance behind a managed load balancer or orchestration platform (e.g., Kubernetes with a side‑car container) and integrate with your existing authentication/monitoring stack.

**Production readiness**  
- **Activity & community:** Recent commits (as of 2026‑05‑13), a large star/fork count, and multiple contributors indicate a healthy ecosystem.  
- **Stability:** The script is designed for non‑interactive, repeatable installs, reducing human error in production environments.  
- **Risk considerations:** License and security posture need a final check, but no major metadata issues are evident. Overall, Sing‑box is a strong OSS candidate for pilot projects and can be promoted to production after standard security and compliance vetting.

### Русский

**eooce/Sing-box** — это открытый скрипт‑установщик (Shell) для сборки мультипротокольного прокси‑сервера sing‑box (reality + hy2 + vmess‑argo + tuic5) в один клик, с поддержкой Alpine и чисто IPv6‑VPS, а также готовыми правилами распределения трафика. Он позволяет быстро развернуть полностью готовую к работе инфраструктуру без написания собственного UI, что ускоряет создание пользовательских интерфейсов и сервисов, требующих проксирования трафика. Проект обладает высокой готовностью к production: активные коммиты, более 4500 звёзд, 1600 форков и недавнее обновление (13 мая 2026), что свидетельствует о надёжной поддержке и широком принятии в сообществе.

### 中文

**项目简介**  
eooce/Sing-box 是一个基于 **sing‑box** 的一键部署脚本，集成了 reality、hy2、vmess‑argo、tuic5 四大协议（已适配 Alpine），可在纯 IPv6 VPS、VPS、游戏机等环境下快速搭建多协议分流服务，安装全程无交互，适合需要快速上线的用户。

**价值**  
- **一键全协议**：无需手动编译或逐个配置，脚本一次执行即可完成 reality、hy2、vmess‑argo、tuic5 四种协议的部署。  
- **跨平台**：支持 Alpine、Debian、Ubuntu 等主流 Linux 发行版，兼容纯 IPv6 VPS，降低网络环境限制。  
- **分流能力**：内置丰富的路由/分流规则，帮助用户根据业务需求灵活划分流量，提高网络利用率和安全性。  
- **社区活跃**：近 5k 星、1.6k Fork，近期仍有更新，社区贡献和问题响应速度快。

**典型接入方式**  
1. **脚本方式**：在目标机器上执行 `curl -fsSL https://raw.githubusercontent.com/eooce/Sing-box/main/install.sh | sh`（或下载后 `bash install.sh`），脚本会自动检测系统、下载对应的 sing‑box 二进制并生成默认配置。  
2. **自定义配置**：安装完成后，编辑生成的 `/etc/sing-box/config.json`，根据业务需求开启/关闭对应协议或修改分流规则。  
3. **服务管理**：脚本已将 sing‑box 注册为 systemd 服务（或 OpenRC），使用 `systemctl start|stop|restart sing-box` 即可控制。  
4. **API/CLI**：可通过 sing‑box 自带的 `sing-box ctl` 命令行工具或 RESTful API 动态查询/修改运行时配置，实现自动化运维。

**生产可用性**  
- **代码活跃度**：截至 2026‑05‑13，最近一次提交在 1 天前，说明项目仍在维护。  
- **成熟度**：脚本已在多种 VPS（包括纯 IPv6）上验证，错误处理和日志输出较为完善，适合作为生产环境的基础网络层。  
- **安全性**：项目使用 MIT 许可证，源码公开，可自行审计；建议在生产环境部署前通过容器或沙箱进行安全评估，并开启防火墙/SELinux 等硬化措施。  
- **运维成本**：一键部署 + systemd 管理，运维工作量极低；如需二次定制，只需修改 JSON 配置或自行编写脚本即可。

综上，eooce/Sing-box 以“一键四合一” 的轻量化方式，为需要多协议分流的网络服务提供了快速、可靠的解决方案，适合在生产环境中快速交付并后期灵活扩展。

## 🧭 Practical evaluation

**Value:** eooce/Sing-box helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 4587 GitHub stars
- 1646 forks
- updated 2026-05-13
- primary language: Shell
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 80/100 |
| stars | 78/100 |
| topics | 100/100 |
| outlook | 58/100 |
| quality | 70/100 |
| recency | 20/100 |
| adoption | 79/100 |
| production | 56/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/eooce/Sing-box) · [← Back to Misc](./README.md)</sub>
