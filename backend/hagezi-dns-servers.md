# hagezi/dns-servers

[![Stars](https://img.shields.io/github/stars/hagezi/dns-servers?style=flat-square&color=yellow)](https://github.com/hagezi/dns-servers/stargazers) [![Forks](https://img.shields.io/github/forks/hagezi/dns-servers?style=flat-square&color=blue)](https://github.com/hagezi/dns-servers/network) [![Language](https://img.shields.io/badge/lang-PowerShell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-48%2F100-brightgreen?style=flat-square)](#)

> HaGeZi DNS: Free, Non-Commercial EU Public DNS Servers

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 424 |
| 🍴 **Forks** | 12 |
| 💻 **Language** | PowerShell |
| 📈 **Score** | 48/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ads` `block` `dns` `dns-over-http3` `dns-over-https` `dns-over-quic` `dns-over-tls` `dns-server` `dnssec` `fake` `free` `malware`

## 🎯 Categories

Backend · Security · Marketing

## 📝 Summary

### English

**Summary**  
HaGeZi DNS provides a set of free, non‑commercial public DNS resolvers hosted in the EU, packaged as a PowerShell‑driven project. With 424 ★ on GitHub, the repo offers ready‑to‑use configuration scripts and documentation that let teams spin up the resolvers quickly and embed them in user‑facing applications without building a custom DNS UI from scratch.  

**Value**  
The project abstracts the low‑level DNS server setup into reusable PowerShell modules and sample UI components, so developers can focus on the product’s core features while still delivering a reliable, privacy‑friendly DNS service to end users. This reduces UI development effort, accelerates time‑to‑market, and leverages an EU‑based infrastructure that helps meet data‑locality and GDPR requirements.  

**Practical adoption path**  

1. **Proof‑of‑concept** – Clone the repo, run the provided PowerShell bootstrap on a test VM or container, and verify that the DNS endpoints resolve correctly.  
2. **Integration** – Wrap the supplied UI fragments (HTML/JS) into your existing frontend, or call the PowerShell modules from your backend deployment pipeline.  
3. **Validation** – Review the README, confirm the licensing (non‑commercial) aligns with your use case, and perform a small security audit of the scripts.  
4. **Scale‑up** – Deploy the scripts to production‑grade infrastructure (e.g., Azure VM scale set) and configure monitoring/alerting.  

**Production readiness**  
The project is **medium‑ready**: it is actively maintained (last update 2026‑07‑06) and has a modest community, but it lacks formal CI/CD pipelines, extensive testing, and clear production‑grade documentation. Before moving to production, teams should:  

* Conduct a dependency audit (PowerShell version, required modules).  
* Harden the deployment (firewall rules, TLS, logging).  
* Set up automated health checks and fallback DNS strategies.  

With those steps, HaGeZi DNS can be safely used for internal tools, prototypes, or as a supplemental EU‑based DNS service in larger architectures.

### Русский

Резюме проекта hagezi/dns-servers:

Проект HaGeZi DNS предлагает бесплатные и некоммерческие общественные серверы DNS для Европы, позволяя разработчикам быстрее разрабатывать пользовательские интерфейсы с минимальным количеством настроек. Этот проект может помочь разработчикам быстрее разрабатывать UI продуктов, реализовывать компоненты пользовательского интерфейса и улучшать доставку frontend-приложений. Проект готов для использования в прототипах или внутренних процессах, но требует проверки зависимостей и поддержки перед использованием в продуктивной среде.

### 中文

**项目简介**  
HaGeZi DNS（hagezi/dns-servers）提供一套免费、非商业化的欧盟公共 DNS 服务器列表，帮助用户快速获取可靠的解析服务，适合在前端、后端或安全相关的产品中直接使用。

**价值**  
- **省时省力**：无需自行搭建或维护 DNS 基础设施，直接调用已有的公共 DNS，降低运维成本。  
- **提升可靠性**：欧盟境内的服务器遵循 GDPR 与本地网络规范，适合对数据合规有要求的业务。  
- **易于复用**：项目以 PowerShell 脚本形式提供，可快速集成到 CI/CD 流程或自动化部署脚本中。

**典型接入方式**  
1. **读取配置**：克隆仓库后，使用 `Get-Content ./dns-servers.ps1` 或直接在 PowerShell 中 `.\dns-servers.ps1` 获得服务器 IP 列表。  
2. **在系统或容器中设置**：  
   - **Linux**：将列表写入 `/etc/resolv.conf` 或在 Docker‑Compose 中的 `dns:` 字段引用。  
   - **Windows**：使用 `Set-DnsClientServerAddress -InterfaceAlias "Ethernet" -ServerAddresses <IP>` 将 IP 写入网络适配器。  
3. **在代码中调用**：在后端服务（如 Nginx、Node.js、Go）或前端构建工具（如 Vite、Webpack）中配置 `resolver` 指向这些 DNS，以加速域名解析。  

**生产可用性**  
- **成熟度**：GitHub ★424，最近一次更新为 2026‑07‑06，活跃度尚可，适合作为原型或内部工具的 DNS 方案。  
- **风险**：项目主要以 PowerShell 脚本分发，缺少统一的 API 文档或容器镜像，接入前需评估脚本在不同平台的兼容性，并做好依赖和维护审查。  
- **建议**：先在测试环境做小范围 PoC（例如在 CI 流水线中替换 DNS），确认解析速度、合规性和故障恢复策略后，再逐步推广至生产。  

总体而言，HaGeZi DNS 适合作为快速搭建的公共 DNS 方案，尤其在需要欧盟本地解析且对成本敏感的项目中能显著提升交付效率，但在正式生产环境使用前应完成兼容性与可靠性验证。

## 🧭 Practical evaluation

**Value:** hagezi/dns-servers helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 424 GitHub stars
- 12 forks
- updated 2026-07-06
- primary language: PowerShell
- 17 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 28/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 54/100 |
| quality | 62/100 |
| recency | 40/100 |
| adoption | 48/100 |
| production | 53/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/hagezi/dns-servers) · [← Back to Backend](./README.md)</sub>
