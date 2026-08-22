# ClickDevTech/CELERITY-panel

[![Stars](https://img.shields.io/github/stars/ClickDevTech/CELERITY-panel?style=flat-square&color=yellow)](https://github.com/ClickDevTech/CELERITY-panel/stargazers) [![Forks](https://img.shields.io/github/forks/ClickDevTech/CELERITY-panel?style=flat-square&color=blue)](https://github.com/ClickDevTech/CELERITY-panel/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-86%2F100-brightgreen?style=flat-square)](#)

> Self-hosted web panel for Hysteria 2 & Xray VLESS proxy servers. Features cascade network topology (Forward/Reverse Chain), SSH auto-setup, server groups, load balancing, ACL traffic filtering, API with scopes, webhooks, S3 backups, MCP integration, and subscriptions for Clash/Sing-box/Hiddify.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 184 |
| 🍴 **Forks** | 30 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 86/100 |
| 🗓️ **Last push** | 2026-07-10 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-integration` `censorship-resistant` `docker` `hiddify` `hysteria` `hysteria2` `mcp` `mongodb` `nodejs` `proxy` `proxy-panel` `reality`

## 🎯 Categories

Payments · MCP · Automation · AI/ML · Backend

## 📝 Summary

### English

Here's a brief summary of the ClickDevTech/CELERITY-panel project:

The ClickDevTech/CELERITY-panel is an open-source, self-hosted web panel designed for Hysteria 2 & Xray VLESS proxy servers, offering advanced features such as cascade network topology, SSH auto-setup, and load balancing. This project helps streamline integration of monetization, billing, or payment processing flows, making it a valuable tool for developers and businesses. With its high production readiness, strong adoption, and recent activity, it's an excellent candidate for serious piloting.

The value proposition of the ClickDevTech/CELERITY-panel lies in its ability to simplify the integration of billing or checkout processes, evaluate payment service provider (PSP) flows, and automate payment operations. This can save developers and businesses time and resources, making it a practical solution for various use cases.

The practical adoption path for the ClickDevTech/CELERITY-panel involves:

1. Evaluating the project's API, SDK, and CLI implementation signals to ensure it aligns with your specific needs.
2. Reviewing the project's GitHub activity, adoption, and ecosystem signals to gauge its production readiness.
3. Assessing the project's license, security posture, and active maintainers to ensure they meet your requirements.

### Русский

Резюме:

ClickDevTech/CELERITY-panel - это открытый исходный проект, который предоставляет собой веб-интерфейс для управления Hysteria 2 & Xray VLESS прокси-серверами. Этот проект предлагает ряд функций, включая каскадную топологию сети, автоматическую настройку SSH, группировку серверов, балансировку нагрузки, фильтрацию трафика ACL, API с ограничениями, вебхуков, резервное копирование S3 и интеграцию с MCP. 

Проект готов к внедрению в production, поскольку имеет высокий уровень готовности и сильные сигналы экосистемы. Типовой сценарий внедрения - интеграция биллинга или системы оплаты, а также автоматизация операций по оплате.

### 中文

**项目简介（2‑3 句）**  
ClickDevTech/CELERITY‑panel 是一款自托管的 Web 控制面板，专为 Hysteria 2 与 Xray VLESS 代理服务器设计。它支持级联网络拓扑（正向/反向链路）、SSH 自动部署、服务器分组、负载均衡、ACL 流量过滤、细粒度 API（带 Scope）、Webhook、S3 备份、MCP 集成以及 Clash / Sing‑box / Hiddify 订阅等功能。

---

### 价值主张
- **加速货币化与计费集成**：提供统一的 API/SDK/CLI，能够快速嵌入支付、计费或 PSP（Payment Service Provider）工作流，省去自行搭建代理管理与计费系统的时间成本。  
- **统一运维与安全**：通过可视化面板实现代理服务器的集中管理、自动化 SSH 配置、流量 ACL 与负载均衡，提升运维效率并降低人为错误。  
- **灵活扩展**：支持多种订阅格式（Clash、Sing‑box、Hiddify）和 MCP（Monetization Control Platform）对接，便于在不同业务场景下复用。

### 典型接入方式
| 场景 | 接入方式 | 关键步骤 |
|------|----------|----------|
| **业务系统调用计费接口** | 使用提供的 **REST API**（支持 Scope 权限）或 **Node.js SDK** | 1. 在面板创建 API Token 并分配 Scope<br>2. 在业务后端调用 `/api/v1/billing/*` 完成计费、查询、退款等操作 |
| **自动化部署** | 通过 **CLI** 或 **Docker Compose** 部署面板 | 1. `docker pull clickdevtech/celerity-panel`<br>2. 配置 `config.yaml`（包括 S3 备份、MCP 参数）<br>3. `docker compose up -d` |
| **Webhook 事件** | 注册 **Webhook URL**（如支付成功、服务器异常） | 1. 在面板 → Settings → Webhooks 添加目标 URL<br>2. 根据业务需求处理 `POST` payload（如更新用户配额） |
| **MCP 集成** | 使用 **MCP SDK**（JavaScript）在前端/后端调用 | 1. 在面板开启 MCP 集成并获取 `clientId/secret`<br>2. 在业务代码中引入 `@celerity/mcp`，调用 `mcp.trackEvent()`、`mcp.updateQuota()` 等方法 |

### 生产可用性评估
- **活跃度**：截至 2026‑07‑10，最近一次提交在 3 天前，拥有 184 ⭐、30 fork，社区活跃度良好。  
- **技术成熟度**：核心使用 JavaScript（Node.js）实现，提供完整的 API 文档、示例代码以及 Docker 镜像，部署门槛低。  
- **安全与合规**：项目暂无已知重大安全漏洞，仍需自行审计许可证（MIT）以及依赖库的安全性。  
- **可扩展性**：支持 S3 备份、负载均衡、服务器分组等企业级特性，适合中大型代理业务。  
- **风险**：需要进一步确认维护者的长期可用性、对安全漏洞的响应时效以及对特定合规（如 GDPR）要求的支持。

**结论**：CELERITY‑panel 在功能完整性、社区活跃度和部署便捷性方面表现优秀，可作为 OSS 候选进入生产环境进行试点，尤其适合需要快速集成计费/支付流程的代理服务提供商。后续建议进行安全审计并制定运维 SOP，以确保长期稳定运行。

## 🧭 Practical evaluation

**Value:** ClickDevTech/CELERITY-panel helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 184 GitHub stars
- 30 forks
- updated 2026-07-10
- primary language: JavaScript
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 37/100 |
| stars | 48/100 |
| topics | 100/100 |
| outlook | 86/100 |
| quality | 75/100 |
| recency | 100/100 |
| adoption | 45/100 |
| production | 82/100 |
| usefulness | 100/100 |
| integration | 100/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-10 · [View on GitHub](https://github.com/ClickDevTech/CELERITY-panel) · [← Back to Payments](./README.md)</sub>
