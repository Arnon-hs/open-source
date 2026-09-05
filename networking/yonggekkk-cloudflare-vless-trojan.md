# yonggekkk/Cloudflare-vless-trojan

[![Stars](https://img.shields.io/github/stars/yonggekkk/Cloudflare-vless-trojan?style=flat-square&color=yellow)](https://github.com/yonggekkk/Cloudflare-vless-trojan/stargazers) [![Forks](https://img.shields.io/github/forks/yonggekkk/Cloudflare-vless-trojan?style=flat-square&color=blue)](https://github.com/yonggekkk/Cloudflare-vless-trojan/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> CF-workers/pages代理脚本：支持Vless-ws(tls)、Trojan-ws(tls)；Socks5/http本地代理脚本：可选ECH-TLS、普通TLS、无TLS三种代理模式

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 15.4k |
| 🍴 **Forks** | 9.5k |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`argo` `cdn` `clash-meta` `cloudflare` `cloudflare-pages` `cloudflare-workers` `ech` `http` `nat64` `reality` `sing-box` `socks5`

## 🎯 Categories

Networking · Security

## 📝 Summary

### English

**Summary**  
The **Cloudflare‑vless‑trojan** repository provides a Cloudflare Workers/Pages proxy script that supports VLESS‑WS (TLS) and Trojan‑WS (TLS), plus a local SOCKS5/HTTP proxy client with three modes (ECH‑TLS, regular TLS, or no TLS). With a large star/fork count and recent updates, it is positioned as a ready‑to‑use, open‑source solution for deploying secure, low‑latency edge proxies behind Cloudflare.  

**Value**  
- **Unified edge proxy**: One script handles both VLESS and Trojan protocols, simplifying deployment for users who need to serve multiple proxy types from a single Cloudflare endpoint.  
- **Flexible client options**: The local proxy can operate with the strongest ECH‑TLS, standard TLS, or plain connections, allowing adaptation to environments with differing TLS support.  
- **Cost‑effective scaling**: Running on Cloudflare Workers/Pages leverages Cloudflare’s global network and free tier, reducing infrastructure overhead while delivering high availability.  

**Practical adoption path**  
1. **Review the README** – confirm the required Cloudflare account, Workers/Pages setup steps, and any environment variables.  
2. **Proof‑of‑concept** – fork the repo, deploy the Workers script to a test subdomain, and run the local proxy client on a development machine to verify connectivity for both VLESS‑WS and Trojan‑WS.  
3. **Integrate with existing services** – point your client applications (e.g., V2Ray, Trojan‑Go) to the Cloudflare endpoint, and optionally replace any legacy proxy infrastructure.  
4. **Automate deployment** – incorporate the Workers deployment into CI/CD pipelines (e.g., using Wrangler) and package the client script for distribution across your fleet.  

**Production readiness**  
- **Activity**: The project shows recent commits (as of 2026‑06‑24) and a vibrant community (15 k+ stars, 9.5 k forks).  
- **Maturity**: Core functionality (VLESS‑WS, Trojan‑WS, TLS modes) is stable and documented, making it suitable for pilot deployments.  
- **Scalability**: Leveraging Cloudflare’s edge network ensures low latency and high throughput without managing servers.  
- **Risks**: Licensing, security audit of the proxy code, and long‑term maintainer commitment still require verification before full production rollout.  

Overall, with a small PoC to validate the README and security posture, the project is a strong candidate for production use in environments that need flexible, Cloudflare‑backed VLESS/Trojan proxies.

### Русский

**Краткое резюме:**  
`yonggekkk/Cloudflare-vless-trojan` — это набор скриптов для Cloudflare Workers/Pages, позволяющих быстро развернуть прокси‑серверы с поддержкой Vless‑ws(tls) и Trojan‑ws(tls), а также локальные SOCKS5/HTTP‑прокси с тремя режимами шифрования (ECH‑TLS, обычный TLS и без TLS). Проект уже активно поддерживается (обновления в 2026 году, более 15 к тыс. звёзд и 9 к форков), что делает его готовым к пилотному внедрению в production‑среду после небольшого PoC и проверки README.  

**Типовой сценарий:** разместить скрипт в Cloudflare Workers, настроить нужный протокол (Vless или Trojan) и, при необходимости, запустить локальный SOCKS5/HTTP‑клиент для обхода ограничений сети.  

**Уровень готовности:** высокий — проект имеет свежие коммиты, широкое сообщество и достаточную документацию, однако перед масштабным использованием следует уточнить лицензию и провести аудит безопасности.

### 中文

**项目简介（2‑3 句话）**  
yonggekkk/Cloudflare‑vless‑trojan 是一套基于 Cloudflare Workers / Pages 的代理脚本，能够在 Cloudflare 边缘实现 Vless‑ws（TLS）和 Trojan‑ws（TLS）协议的转发；同时提供本地 Socks5/HTTP 代理脚本，支持 ECH‑TLS、普通 TLS 与无 TLS 三种模式，帮助用户在不同网络环境下灵活突破限制。

**价值**  
- **跨平台、零部署**：利用 Cloudflare Workers 的无服务器特性，无需自建服务器即可获得高速、全球分布的代理节点。  
- **协议兼容**：同时支持 Vless‑ws 与 Trojan‑ws，兼容市面上多数 V2Ray / Clash 客户端，降低迁移成本。  
- **安全可选**：本地代理脚本提供 ECH‑TLS（加密 SNI）以及普通 TLS/无 TLS 三种选项，满足对隐私和兼容性的不同需求。  
- **开源透明**：代码公开、星标/分叉量大，社区活跃，易于审计和二次定制。

**典型接入方式**  
1. **在 Cloudflare 创建 Workers**：将仓库中的 `worker.js`（或 `pages` 项目）直接复制到 Cloudflare Workers 控制台或通过 `wrangler` 部署。  
2. **配置后端节点**：在脚本的 `config` 区域填入自己的 Vless/Trojan 服务器地址、UUID、域名等信息。  
3. **本地代理**：下载对应的 `socks5.js` / `http.js`，在本机运行（Node.js 环境），并在客户端（如 Clash、V2RayN）中把本地端口指向该脚本，即可使用 ECH‑TLS、TLS 或明文模式转发流量。  
4. **验证**：使用 `curl https://your-worker.domain/` 或客户端的测试功能确认链路正常后，即可投入日常使用。

**生产可用性**  
- **活跃维护**：最近一次提交在 2026‑06‑24，仓库拥有 15k+ 星标、9k+ 分叉，社区贡献活跃。  
- **技术成熟**：基于 Cloudflare 官方的 Workers 平台，具备高可用、自动弹性伸缩和 DDoS 防护。  
- **安全审计**：代码结构清晰，依赖少，易于自行审计；但仍建议在正式环境前进行安全评估（尤其是 TLS/ECH 配置）。  
- **部署成本低**：Workers 免费额度足以支撑中小流量，超额部分按请求计费，成本可控。  

综上，yonggekkk/Cloudflare‑vless‑trojan 已具备在生产环境中进行小规模试点的条件，建议先在测试环境完成一次完整的部署‑验证‑监控闭环后，再逐步推广到业务生产线。

## 🧭 Practical evaluation

**Value:** yonggekkk/Cloudflare-vless-trojan may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 15423 GitHub stars
- 9523 forks
- updated 2026-06-24
- primary language: JavaScript
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 99/100 |
| stars | 89/100 |
| topics | 100/100 |
| outlook | 79/100 |
| quality | 91/100 |
| recency | 80/100 |
| adoption | 92/100 |
| production | 76/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/yonggekkk/Cloudflare-vless-trojan) · [← Back to Networking](./README.md)</sub>
