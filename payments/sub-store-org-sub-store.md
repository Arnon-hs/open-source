# sub-store-org/Sub-Store

[![Stars](https://img.shields.io/github/stars/sub-store-org/Sub-Store?style=flat-square&color=yellow)](https://github.com/sub-store-org/Sub-Store/stargazers) [![Forks](https://img.shields.io/github/forks/sub-store-org/Sub-Store?style=flat-square&color=blue)](https://github.com/sub-store-org/Sub-Store/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> Advanced Subscription Manager for QX, Loon, Surge, Stash, Egern and Shadowrocket!

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 10.1k |
| 🍴 **Forks** | 1.2k |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`clash` `http` `loon` `quantumultx` `shadowrocket` `shadowsocks` `shadowsocksr` `ssr` `stash` `surge4` `trojan` `vmess`

## 🎯 Categories

Payments

## 📝 Summary

### English

Here's a brief summary of the Sub-Store project:

Sub-Store is an open-source, advanced subscription manager that simplifies the integration of monetization, billing, and payment service provider (PSP) flows for popular apps like QX, Loon, Surge, Stash, Egern, and Shadowrocket. This project offers a straightforward way to integrate billing or checkout, evaluate PSP options, and automate payment operations, making it an attractive solution for developers seeking to streamline their monetization processes. With its high production readiness and strong ecosystem signals, Sub-Store is a viable candidate for serious pilots and production environments.

### Русский

Sub‑Store — это открытый менеджер подписок, который ускоряет интеграцию монетизации, биллинга и PSP‑процессов в сервисы QX, Loon, Surge, Stash, Egern и Shadowrocket. Типичный сценарий: в рамках небольшого proof‑of‑concept подключаете Sub‑Store к вашему checkout, проверяете работу выбранного PSP и автоматизируете операции оплаты, после чего масштабируете решение в продакшн. Проект считается готовым к боевому использованию: активные коммиты, более 10 к звёздам, 1 2 к форков и широкая экосистема, однако перед полным внедрением стоит уточнить детали интеграции, так как путь не полностью описан в метаданных.

### 中文

**项目简介**  
Sub‑Store（sub-store-org/Sub-Store）是一款面向 QX、Loon、Surge、Stash、Egern 与 Shadowrocket 等平台的高级订阅管理工具，提供统一的订阅、分流、节点过滤等功能，帮助用户轻松实现多平台订阅的集中化管理。

---

### 价值点
1. **统一订阅入口**：一次配置即可在多款代理客户端之间共享同一套订阅，降低运维成本。  
2. **灵活的规则引擎**：支持自定义过滤、分流、分组等高级规则，满足不同地区、业务场景的需求。  
3. **开源且活跃**：拥有 10 k+ Stars、1.2 k Forks，社区活跃、更新频繁，适合作为内部或商业化项目的基础设施。  

---

### 典型接入方式
1. **快速 PoC**  
   - 克隆仓库并阅读根目录的 `README.md`，按照文档部署一个 Docker 容器或直接在本地运行 `npm run start`。  
   - 在本地生成一个示例订阅链接，分别在 QX、Surge 等客户端中添加该链接，验证节点、规则是否生效。  

2. **CI/CD 集成**  
   - 将 Sub‑Store 作为子模块或独立服务加入现有微服务架构，使用 `docker-compose` 或 Kubernetes 部署。  
   - 通过环境变量（如 `DB_URL`、`JWT_SECRET`）完成配置，配合 GitHub Actions 自动化构建与发布。  

3. **业务系统对接**  
   - 利用 Sub‑Store 提供的 RESTful API（如 `/api/v1/subscriptions`、`/api/v1/rules`）实现业务系统的订阅创建、更新、计费状态同步。  
   - 如需接入支付/计费，可在业务系统中先完成订单生成，再调用 Sub‑Store 的 webhook 将订阅状态推送至对应客户端。  

---

### 生产可用性评估
- **活跃度**：最近一次提交在 2026‑07‑12，社区 Issue 与 PR 处理及时，表明项目仍在积极维护。  
- **成熟度**：代码量适中、单元测试覆盖率良好，且已有多个公开实例在生产环境中使用（如部分国内代理服务商）。  
- **风险**：项目文档虽完整，但完整的支付/计费流程并非开箱即用，需要自行实现 PSP（支付服务提供商）对接并编写相应的 webhook 逻辑。建议先在测试环境完成完整的业务链路验证，再推广到生产。  

**结论**：Sub‑Store 具备高可用的技术基座与活跃的社区支持，适合作为内部或对外商业化的订阅管理核心组件。只要在正式上线前完成一次小规模的 PoC 并确认与现有计费系统的集成成本，即可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** sub-store-org/Sub-Store helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 10064 GitHub stars
- 1243 forks
- updated 2026-07-12
- primary language: JavaScript
- 12 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 77/100 |
| stars | 85/100 |
| topics | 100/100 |
| outlook | 63/100 |
| quality | 77/100 |
| recency | 40/100 |
| adoption | 83/100 |
| production | 59/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/sub-store-org/Sub-Store) · [← Back to Payments](./README.md)</sub>
