# deezertidal/shadowrocket-rules

[![Stars](https://img.shields.io/github/stars/deezertidal/shadowrocket-rules?style=flat-square&color=yellow)](https://github.com/deezertidal/shadowrocket-rules/stargazers) [![Forks](https://img.shields.io/github/forks/deezertidal/shadowrocket-rules?style=flat-square&color=blue)](https://github.com/deezertidal/shadowrocket-rules/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> 小火箭 shadowrocket 配置文件 模块 脚本 module sgmodule 图文教程 规则 分流 破解 解锁

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 6.5k |
| 🍴 **Forks** | 343 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The *shadowrocket‑rules* repository provides a collection of configuration files, modules, and scripts for the iOS proxy client Shadowrocket, along with a visual tutorial (sgmodule) that explains how to set up rule‑based traffic splitting, unlocking, and bypassing. It is a community‑maintained rule set written in JavaScript that can be imported directly into Shadowrocket to apply custom routing, ad‑blocking, and geo‑unblocking policies.

**Value**  
- **Ready‑made rule set**: Saves developers and power users time by delivering a curated, frequently updated list of routing and filtering rules that would otherwise need to be assembled manually.  
- **Documentation & examples**: The included “图文教程” (image‑text tutorial) walks users through module installation and configuration, lowering the learning curve for non‑technical users.  
- **Community traction**: With over 6.5 k stars and 300+ forks, the project enjoys a sizable user base, indicating that the rules are battle‑tested and widely applicable.

**Practical Adoption Path**  
1. **Review the README** – Verify that the rule syntax and module structure match your Shadowrocket version.  
2. **Clone or download** the `rules/` folder and any required `sgmodule` scripts.  
3. **Import** the configuration into Shadowrocket (Settings → Import Config).  
4. **Test** the rules in a staging environment or on a secondary device, adjusting domain lists or policy groups as needed.  
5. **Integrate** into CI/CD (e.g., a simple script that pulls the latest rules from the repo and redeploys them to your fleet of devices) if you need automated updates.

**Production Readiness**  
- **Maturity**: Medium. The repository is actively maintained (last update 2026‑06‑25) and has strong community signals, but the integration workflow is not formally documented beyond the tutorial.  
- **Suitability**: Ideal for prototypes, internal tooling, or as a baseline rule set that you can extend for production.  
- **Risks**: Lack of explicit versioning or release notes means you should pin a specific commit for stable deployments and monitor upstream changes for breaking updates. Conduct a manual security review of the scripts before committing them to production.  

Overall, *shadowrocket‑rules* is a valuable, community‑driven resource for quickly enabling advanced routing and unlocking capabilities in Shadowrocket, provided you perform the necessary validation and version‑pinning before using it in a production environment.

### Русский

**deezertidal/shadowrocket-rules** — набор готовых конфигураций, модулей и скриптов для клиента Shadowrocket (iOS), позволяющий быстро добавить правила маршрутизации, обхода блокировок и разблокировки контента. Проект удобно интегрировать в процесс настройки собственного прокси‑клиента: достаточно скопировать нужный `.conf`‑файл или модуль, подключить его в Shadowrocket и при необходимости адаптировать под свои серверы. Готовность к production — средняя: репозиторий активно поддерживается (последнее обновление — 2026‑06‑25, ≈ 6,5 k звёзд), но интеграция требует ручного просмотра и проверки совместимости с текущей инфраструктурой.

### 中文

**项目简介**  
deezertidal/shadowrocket‑rules 是一套针对 iOS/ macOS 客户端 **Shadowrocket** 的规则、模块与脚本集合，提供图文教程、分流、破解、解锁等实用配置，帮助用户快速搭建科学上网与流量分流方案。

**价值**  
- **一站式规则库**：汇聚国内外常用的域名、IP、URL‑Pattern 等规则，免去手动搜集和维护的繁琐。  
- **模块化脚本**（sgmodule）：可直接在 Shadowrocket 中引用，支持自定义分流、广告拦截、地域解锁等功能。  
- **图文教程**：配套的使用指南降低上手门槛，适合新手和进阶用户快速部署。

**典型接入方式**  
1. **克隆或下载仓库**：`git clone https://github.com/deezertidal/shadowrocket-rules.git`。  
2. **导入规则文件**：在 Shadowrocket → “配置文件” → “导入” 中选择 `rules/*.conf` 或 `modules/*.sgmodule`。  
3. **根据需求启用模块**：在 “模块管理” 页面勾选相应的 sgmodule，或在配置文件中添加 `module = xxx.sgmodule`。  
4. **可选自定义**：复制需要的规则到本地，按实际网络环境修改后重新导入，以实现更精准的分流或解锁。

**生产可用性**  
- **成熟度**：项目已有 6 523 星、343 Fork，且最近一次更新在 2026‑06‑25，社区活跃度较高。  
- **适用场景**：适合原型验证、内部研发或小规模业务的科学上网、流量分流需求。  
- **上线前检查**：由于集成路径主要依赖手动导入，建议在正式环境前完成以下步骤：  
  1. 验证规则与业务域名的匹配度，剔除不必要或冲突的条目。  
  2. 进行安全审计，确保脚本不包含潜在的恶意代码。  
  3. 在测试环境进行完整的分流与解锁效果验证。  
- **维护成本**：规则库需定期同步上游更新；若业务对规则的时效性要求高，建议设立自动化拉取和验证流程。

综上，deezertidal/shadowrocket‑rules 可在原型或内部系统中快速提供可靠的 Shadowrocket 配置，经过适度的审查与测试后即可投入生产使用。

## 🧭 Practical evaluation

**Value:** deezertidal/shadowrocket-rules may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 6523 GitHub stars
- 343 forks
- updated 2026-06-25
- primary language: JavaScript

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 63/100 |
| stars | 81/100 |
| topics | 0/100 |
| outlook | 65/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 76/100 |
| production | 66/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/deezertidal/shadowrocket-rules) · [← Back to Misc](./README.md)</sub>
