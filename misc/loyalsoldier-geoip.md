# Loyalsoldier/geoip

[![Stars](https://img.shields.io/github/stars/Loyalsoldier/geoip?style=flat-square&color=yellow)](https://github.com/Loyalsoldier/geoip/stargazers) [![Forks](https://img.shields.io/github/forks/Loyalsoldier/geoip?style=flat-square&color=blue)](https://github.com/Loyalsoldier/geoip/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> 🌚 🌍 🌝 GeoIP 增强版，自由定制多种格式 GeoIP 文件，包括但不限于 V2Ray dat 格式文件 geoip.dat、MaxMind mmdb 格式文件、sing-box SRS 格式文件、mihomo MRS 格式文件、Clash ruleset、Surge ruleset、Nginx allow & deny 规则文件等。Enhanced edition of GeoIP for Nginx, V2Ray, Xray-core, Clash, mihomo, sing-box, Shadowrocket, Quantumult X, Surge, hysteria, Trojan-Go, dae, etc.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 6.3k |
| 🍴 **Forks** | 885 |
| 💻 **Language** | Go |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anti-censorship` `anticensorship` `clash` `geoip` `gfw` `hysteria` `ipv4` `ipv6` `maxmind` `mihomo` `nginx` `proxy`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary**  
Loyalsoldier/geoip is an open‑source, Go‑based toolkit that generates customized GeoIP data in many formats (V2Ray dat, MaxMind mmdb, sing‑box SRS, mihomo MRS, Clash/Surge rulesets, Nginx allow/deny lists, etc.). It lets developers and operators quickly build the exact IP‑blocking or routing tables they need for a wide range of proxy, firewall, and CDN solutions.

**Value proposition**  
- **Unified source** – One repository produces all the GeoIP variants that different networking and security products require, eliminating the need to maintain separate data pipelines.  
- **Flexibility** – Users can filter, merge, or whitelist/blacklist IP ranges on the fly, tailoring the output to specific compliance or performance goals.  
- **Community‑tested** – With >6 k stars, hundreds of forks, and active contributions, the project benefits from a large user base that continuously validates the accuracy of the IP lists.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the provided CLI to generate a small ruleset (e.g., an Nginx `allow`/`deny` file) and point a test instance of your service at it.  
2. **CI integration** – Add a step in your build pipeline that runs the generator on a schedule (daily/weekly) to keep the GeoIP data fresh.  
3. **Production rollout** – Replace static IP lists in your proxy/firewall configuration with the generated files, monitor hit‑rate and latency, and gradually migrate additional services (V2Ray, Clash, Surge, etc.) once confidence is established.  

**Production readiness**  
- **Activity** – The repository is actively maintained (last commit 2026‑07‑06), with frequent releases and a responsive issue tracker.  
- **Adoption** – Widely used across the proxy and CDN ecosystem (V2Ray, Xray, Clash, mihomo, sing‑box, Shadowrocket, Quantumult X, Surge, Hysteria, Trojan‑Go, dae, etc.), indicating real‑world stability.  
- **Quality signals** – 6.2 k stars, 885 forks, and a well‑documented README demonstrate strong community confidence.  
- **Risk considerations** – A final review of the MIT‑style license, security audit of the Go code, and verification of maintainer activity are recommended, but no major red flags have been identified.  

Overall, Loyalsoldier/geoip is production‑ready for pilots and can be scaled to full‑deployment with minimal friction, providing a single source of truth for all your GeoIP‑based routing and filtering needs.

### Русский

**Loyalsoldier/geoip** — это открытый набор инструментов для генерации и конвертации GeoIP‑данных в любые нужные форматы (V2Ray dat, MaxMind mmdb, sing‑box SRS, mihomo MRS, правила Clash/Surge, Nginx allow‑deny и др.), что позволяет быстро адаптировать гео‑блокировки и маршрутизацию под любые прокси‑ и сетевые решения. Типичный сценарий внедрения — небольшое proof‑of‑concept, в котором из репозитория генерируется нужный файл (например, geoip.dat для V2Ray) и подключается к существующей инфраструктуре, после чего процесс автоматизируется в CI/CD. Проект обладает высокой готовностью к production: активные коммиты, более 6000 звёзд, множество форков, поддержка Go‑сообщества и широкая экосистема интеграций, требующие лишь финальной проверки лицензии и безопасности.

### 中文

**简短介绍**

Loyalsoldier/geoip 是一个开源 GeoIP 增强版项目，提供自由定制多种格式的 GeoIP 文件，支持 V2Ray、MaxMind、sing-box、mihomo 等多种应用。该项目有强大的社区支持和活跃维护，适合用于研究和自动化市场工作流。

**价值**

Loyalsoldier/geoip 帮助研究和自动化市场工作流，适用于以下场景：

* 研究交易系统
* 回测策略
* 监控市场工作流

**典型接入方式**

该项目支持多种接入方式，包括：

* V2Ray dat 格式文件
* MaxMind mmdb 格式文件
* sing-box SRS 格式文件
* mihomo MRS 格式文件
* Clash 规则集
* Surge 规则集
* Nginx 允许 & 拒绝规则文件等

**生产可用性**

该项目具有高生产可用性，社区支持强大，活跃维护，适合用于生产环境。

## 🧭 Practical evaluation

**Value:** Loyalsoldier/geoip helps research and automate market workflows.

**Best use cases**

- research trading systems
- backtest strategies
- monitor market workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 6270 GitHub stars
- 885 forks
- updated 2026-07-06
- primary language: Go
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 74/100 |
| stars | 81/100 |
| topics | 100/100 |
| outlook | 62/100 |
| quality | 75/100 |
| recency | 40/100 |
| adoption | 79/100 |
| production | 60/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/Loyalsoldier/geoip) · [← Back to Misc](./README.md)</sub>
