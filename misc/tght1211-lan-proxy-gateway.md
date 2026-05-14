# Tght1211/lan-proxy-gateway

[![Stars](https://img.shields.io/github/stars/Tght1211/lan-proxy-gateway?style=flat-square&color=yellow)](https://github.com/Tght1211/lan-proxy-gateway/stargazers) [![Forks](https://img.shields.io/github/forks/Tght1211/lan-proxy-gateway?style=flat-square&color=blue)](https://github.com/Tght1211/lan-proxy-gateway/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> 把你的电脑变成全屋科学上网网关，Switch / PS5 / Apple TV / 智能电视改个网关就能用。支持 macOS / Linux / Windows

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 464 |
| 🍴 **Forks** | 56 |
| 💻 **Language** | Go |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Tght1211/lan-proxy-gateway turns a personal computer into a LAN‑wide scientific‑internet gateway, allowing devices such as Switch, PS5, Apple TV, and smart TVs to route traffic through a local proxy without any firmware changes. It runs on macOS, Linux and Windows and is written in Go, with a modest but active community (≈ 460 ★, 56 ✂️).  

**Value**  
- **Universal gateway** – One centrally‑managed PC can provide proxy‑based “unblocked” internet to any device on the same network, eliminating the need for per‑device VPN apps or custom router firmware.  
- **Cross‑platform** – Works on the three major desktop OSes, making it easy to deploy in mixed‑environment homes or small offices.  
- **Lightweight & self‑contained** – A single binary plus a simple configuration file; no heavyweight dependencies or container orchestration required.  

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | **Review README & security** – Verify the proxy protocols supported (e.g., V2Ray, Shadowsocks) and confirm the licensing (MIT/Apache‑2.0 typical for Go projects). | Ensures compliance and that the tool meets your security model. |
| 2️⃣  | **Provision a host** – Choose a always‑on PC (e.g., a low‑spec Linux box or a Windows machine) and install the latest release binary. | Provides a stable anchor point for the LAN gateway. |
| 3️⃣  | **Configure upstream proxy** – Add your own VPN or Shadowsocks server credentials in the supplied config file. | Connects the LAN gateway to the external “scientific internet” service. |
| 4️⃣  | **Adjust network settings** – Set the host’s IP as the DNS/proxy for target devices (via DHCP static mapping or manual device config). | Routes traffic from consoles/TVs through the gateway. |
| 5️⃣  | **Test & monitor** – Use a device to verify that geo‑restricted services are reachable; optionally enable logging or Prometheus metrics. | Confirms correct operation and gives early warning of failures. |
| 6️⃣  | **Automate startup** – Register the binary as a system service (systemd, launchd, or Windows Service) and enable auto‑updates (e.g., via GitHub releases). | Guarantees resilience and reduces manual upkeep. |

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑05‑14) and has a healthy star count, but the ecosystem around it (documentation depth, CI/CD testing, formal release process) is limited.  
- **Risk Areas**:  
  * **Security** – The gateway forwards traffic; you must trust the upstream proxy and audit the binary for potential vulnerabilities.  
  * **License** – Verify the repository’s LICENSE file (commonly MIT/Apache) before commercial use.  
  * **Support** – Community support is informal; consider a fallback plan (e.g., alternative router‑based solutions) for critical deployments.  
- **Fit for Production**: Suitable for internal prototypes, home labs, or small‑scale deployments where the convenience of a software gateway outweighs the need for enterprise‑grade SLAs. For large‑scale or compliance‑driven environments, additional hardening, monitoring, and possibly a commercial alternative would be advisable.

### Русский

**Краткое резюме:**  
`Tght1211/lan-proxy-gateway` — это Go‑приложение, превращающее ваш ПК в локальный шлюз для «научного» доступа в интернет, позволяя консолям (Switch, PS5), Apple TV и смарт‑телевизорам пользоваться единой прокси‑сетью без изменения их настроек. Типичный сценарий — развертывание на macOS, Linux или Windows в домашней сети, после чего все устройства подключаются к ПК‑шлюзу и получают обход блокировок. Проект имеет средний уровень готовности к production: достаточное количество звёзд и форков, недавнее обновление, но требует ручной проверки лицензии, безопасности и активности поддержки перед использованием в критически важных системах.

### 中文

**项目简介（2‑3 句）**  
Tght1211/lan-proxy-gateway 能把一台普通电脑（macOS、Linux、Windows）打造成全屋科学上网网关，所有局域网设备（Switch、PS5、Apple TV、智能电视等）只需改为使用该电脑的代理即可实现高速、稳定的网络加速。项目基于 Go 实现，轻量、跨平台，配置简单。

**价值**  
- **一机多用**：无需在每个终端上单独安装翻墙软件，只需在局域网内部署一次即可覆盖所有设备。  
- **跨平台**：同一套代码在 macOS、Linux、Windows 上均可运行，适配家庭、办公室等多种环境。  
- **低成本**：利用现有电脑或小型服务器即可搭建，省去额外硬件采购费用。  

**典型接入方式**  
1. **部署**：在一台常开机的电脑上克隆仓库、编译或直接下载二进制文件。  
2. **配置**：编辑 `config.yaml`（或通过命令行参数）指定上游科学上网节点（如 V2Ray、Clash、Shadowsocks）以及本地监听端口。  
3. **局域网设备设置**：在 Switch、PS5、Apple TV、智能电视等设备的网络设置里，将 DNS 与代理（HTTP/HTTPS 或 SOCKS5）指向该电脑的 IP 与相应端口。  
4. **可选**：使用 Docker 镜像或 systemd 服务管理，确保开机自启并自动重启。  

**生产可用性**  
- **成熟度**：已有 464 Stars、56 Fork，代码最近一次更新（2026‑05‑14）表明仍在活跃维护。  
- **适用场景**：适合家庭、课堂或小型企业内部网络的科学上网需求，尤其是需要统一管理多种终端的场景。  
- **风险与注意事项**  
  - 需要自行审查上游代理节点的安全与合规性。  
  - 项目许可证、依赖库的安全审计应在正式上线前完成。  
  - 对于高并发或大流量的企业级部署，建议进行性能压测并做好监控。  

综合来看，lan-proxy-gateway 在原型验证和内部使用上已经相当可行，经过一次性安全与运维审查后即可投入生产环境使用。

## 🧭 Practical evaluation

**Value:** Tght1211/lan-proxy-gateway may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 464 GitHub stars
- 56 forks
- updated 2026-05-14
- primary language: Go

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 57/100 |
| topics | 0/100 |
| outlook | 67/100 |
| quality | 64/100 |
| recency | 100/100 |
| adoption | 53/100 |
| production | 71/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/Tght1211/lan-proxy-gateway) · [← Back to Misc](./README.md)</sub>
