# Openwrt-Passwall/openwrt-passwall2

[![Stars](https://img.shields.io/github/stars/Openwrt-Passwall/openwrt-passwall2?style=flat-square&color=yellow)](https://github.com/Openwrt-Passwall/openwrt-passwall2/stargazers) [![Forks](https://img.shields.io/github/forks/Openwrt-Passwall/openwrt-passwall2?style=flat-square&color=blue)](https://github.com/Openwrt-Passwall/openwrt-passwall2/network) [![Language](https://img.shields.io/badge/lang-Lua-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> _No description provided._

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.3k |
| 🍴 **Forks** | 712 |
| 💻 **Language** | Lua |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Openwrt‑Passwall2 is an open‑source Lua‑based suite that adds advanced firewall, proxy, and traffic‑shaping capabilities to OpenWrt routers. With a sizable community (over 3 300 stars) and recent activity, it can serve as a plug‑and‑play enhancement for home‑lab or edge‑router environments that need granular network control.  

**Value**  
- Provides a ready‑made, feature‑rich “passwall” (proxy + rule engine) that would otherwise require custom scripting or multiple separate packages.  
- Consolidates ad‑blocking, VPN routing, DNS‑forwarding, and QoS into a single, centrally managed configuration, reducing operational overhead for network admins.  

**Practical Adoption Path**  
1. **Review the README and issue tracker** to confirm that the supported OpenWrt version matches your device firmware.  
2. **Clone the repository** and follow the installation script (usually `make menuconfig` → select `passwall2` → compile).  
3. **Test on a non‑critical router**: import a sample configuration, verify that traffic is correctly intercepted and routed, and adjust firewall rules as needed.  
4. **Integrate with existing services** (e.g., WireGuard, DNSMasq) by editing the generated `/etc/config/passwall` files; the project’s Wiki provides example snippets.  

**Production Readiness**  
- **Maturity:** Medium – the project is actively maintained (last commit 2026‑07‑12) and widely used, but documentation is sparse and integration steps are not fully automated.  
- **Risk Management:** Before production rollout, perform a controlled pilot, confirm compatibility with your router’s hardware resources, and lock down dependency versions (Lua, luci libraries).  
- **Suitability:** Ideal for prototypes, internal networks, or edge devices where the added functionality outweighs the modest integration effort; for mission‑critical deployments, conduct a thorough validation and consider a fallback firewall solution.

### Русский

Openwrt‑Passwall 2 — это открытый набор скриптов и правил на Lua, позволяющий быстро добавить в роутер OpenWrt полноценный прокси‑брандмауэр (Shadowsocks/V2Ray/Trojan, DNS‑перехват, фильтрацию трафика). Он подходит для прототипов и внутренних сетей, где требуется гибкая маршрутизация и обход ограничений, но перед запуском в продакшн необходимо вручную проверить совместимость с текущей конфигурацией роутера и оценить нагрузку и обновления зависимостей. При достаточной проверке проект считается готовым к использованию в производстве со средним уровнем надёжности.

### 中文

**项目简介**  
Openwrt‑Passwall（亦称 passwall2）是基于 OpenWrt 的网络代理/分流插件，使用 Lua 编写，提供透明代理、分应用/分设备流量走向、自动节点切换等功能，适合在路由器上快速搭建科学上网或企业内部流量管控方案。

**价值**  
- **一键式代理管理**：通过 Web UI 或命令行即可添加、切换 V2Ray、SSR、Trojan 等多种协议的节点，免去手动配置 iptables、dnsmasq 的繁琐。  
- **细粒度分流**：支持基于域名、IP、端口或 MAC 地址的策略路由，帮助实现国内外流量分离、宽带限速或安全审计。  
- **社区活跃**：超过 3 k 星、700+ Fork，维护者持续更新（截至 2026‑07‑12），拥有丰富的插件生态和文档示例，降低学习成本。

**典型接入方式**  
1. **准备 OpenWrt 环境**：在支持的路由器上刷入官方或 LEDE 版 OpenWrt。  
2. **安装 Passwall**：  
   ```bash
   opkg update
   opkg install luci-app-passwall
   ```  
   或使用官方提供的自定义仓库 URL 添加后再安装。  
3. **配置节点和策略**：登录 LuCI（http://<router‑ip>/cgi-bin/luci），在 “Passwall” 页面添加代理节点，设置分流规则（如 “国外流量走代理”， “局域网设备直连”）。  
4. **启用并验证**：启动 Passwall 服务，使用 `curl ipinfo.io` 或浏览器访问被墙网站确认流量已走代理。  

在更复杂的企业场景下，可通过 SSH/Ansible 自动化脚本批量部署 Passwall，并结合 `iptables`、`dnsmasq` 的自定义规则实现统一的流量审计与日志上报。

**生产可用性**  
- **成熟度**：项目已在大量家庭和小型企业路由器上长期运行，社区贡献活跃，更新频率高。  
- **适用范围**：适合原型验证、内部工具或对网络代理有明确需求的生产环境；但因依赖 OpenWrt 硬件平台，需确保路由器性能足以承担加密转发。  
- **风险与注意事项**：  
  - **集成成本**：元数据中缺少标准化的 CI/CD 或 Helm 包，需要手动验证依赖（Lua、iptables、dnsmasq 版本兼容性）。  
  - **维护负担**：升级 OpenWrt 时需确认 Passwall 与新内核、libustream‑websocket 等库的兼容性。  
  - **安全审计**：代理节点信息保存在路由器文件系统，建议加固 SSH、使用只读根文件系统或容器化（如 OpenWrt‑Docker）以降低风险。  

总体而言，Passwall2 在 **原型开发** 与 **内部网络代理** 场景下具备 **中等到高** 的生产可用性，只要在部署前完成硬件兼容性、依赖版本以及安全加固的检查，即可在正式环境中稳定运行。

## 🧭 Practical evaluation

**Value:** Openwrt-Passwall/openwrt-passwall2 may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 3331 GitHub stars
- 712 forks
- updated 2026-07-12
- primary language: Lua

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 71/100 |
| stars | 75/100 |
| topics | 0/100 |
| outlook | 65/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 74/100 |
| production | 63/100 |
| usefulness | 42/100 |
| integration | 18/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/Openwrt-Passwall/openwrt-passwall2) · [← Back to Misc](./README.md)</sub>
