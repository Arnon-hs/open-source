# tomaae/homeassistant-mikrotik_router

[![Stars](https://img.shields.io/github/stars/tomaae/homeassistant-mikrotik_router?style=flat-square&color=yellow)](https://github.com/tomaae/homeassistant-mikrotik_router/stargazers) [![Forks](https://img.shields.io/github/forks/tomaae/homeassistant-mikrotik_router?style=flat-square&color=blue)](https://github.com/tomaae/homeassistant-mikrotik_router/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> Mikrotik router integration for Home Assistant

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 458 |
| 🍴 **Forks** | 118 |
| 💻 **Language** | Python |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`hacs` `homeassistant` `homeassistant-components` `homeassistant-integration` `mikrotik`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
`tomaae/homeassistant-mikrotik_router` is a Python‑based integration that lets Home Assistant communicate with MikroTik routers, exposing router metrics, status, and control functions as Home Assistant entities. With over 450 ★ on GitHub and recent activity (last commit 2026‑06‑29), it offers a ready‑to‑use bridge for network‑aware automations.

**Value**  
- **Unified automation** – Home Assistant can now react to router events (e.g., client connect/disconnect, bandwidth usage, VPN status) without custom scripts.  
- **Community‑driven** – The project’s popularity and forking activity indicate a healthy user base that can contribute fixes and feature requests.  
- **Extensible** – Written in Python and packaged as a Home Assistant custom component, it can be extended to cover additional MikroTik APIs as needed.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, follow the README to install the custom component in a test Home Assistant instance, and configure it with a test MikroTik device.  
2. **Validate the README** – Ensure the documentation covers your router model, required API credentials, and the entities it creates; adjust or contribute missing details.  
3. **Pilot deployment** – Deploy the component to a staging Home Assistant environment, monitor logs, and create a few simple automations (e.g., turn off lights when a specific client disconnects).  
4. **Production rollout** – After confirming stability, add the component to your production Home Assistant, lock the version in your configuration management, and set up alerts for component updates.

**Production Readiness**  
- **Maturity**: Medium. The integration is feature‑complete enough for prototyping and internal use, but it has not been formally audited for security or long‑term support.  
- **Maintenance**: Recent commits suggest active maintenance, yet you should verify the maintainer’s responsiveness and check the license for compatibility with your organization.  
- **Risk mitigation**: Perform a security review of the MikroTik API usage, pin the component version, and monitor upstream changes before promoting to mission‑critical environments.  

Overall, the project is a solid candidate for internal or prototype deployments, provided you run a small proof‑of‑concept, verify the documentation, and put basic maintenance and security checks in place before using it in production.

### Русский

**tomaae/homeassistant‑mikrotik_router** — это open‑source‑модуль, позволяющий Home Assistant управлять роутерами MikroTik (получать статус, менять настройки, отслеживать устройства). Типичный сценарий: в домашней автоматизации подключаете интеграцию, задаёте простые автоматизации (например, отключать Wi‑Fi для гостей или переключать QoS при включении IPTV). Проект имеет средний уровень готовности: активные коммиты, более 450 звёзд и 100 форков, но перед запуском в продакшн рекомендуется проверить лицензию, актуальность зависимостей и наличие ответственного мейнтейнера.

### 中文

**项目价值**  
`tomaae/homeassistant-mikrotik_router` 为 Home Assistant 提供了对 MikroTik 路由器的原生集成，使得用户可以在 HA 仪表盘中直接监控和控制路由器的接口、流量、DHCP 租约、防火墙规则等关键状态。对需要统一管理网络设备与智能家居的场景（如家庭自动化、办公小型网络）非常实用，省去手动登录 RouterOS 的繁琐操作。

**典型接入方式**  
1. **在 Home Assistant 中添加集成**：进入 HA 的「集成」页面，搜索 “MikroTik Router”。  
2. **填写连接信息**：提供路由器的 IP、API 端口（默认 8728/8729）、用户名、密码或 API Token。  
3. **选择需要的实体**：可勾选接口、流量监控、DHCP 租约、热点、防火墙等模块，系统会自动创建对应的 sensor、binary_sensor、switch 等实体。  
4. **自动发现 & 自动更新**：集成会定期调用 MikroTik API 拉取最新状态，并在 HA 中实时刷新，支持自定义扫描间隔。  

> **提示**：如果路由器开启了 TLS（API over HTTPS），需要在 HA 中配置 `verify_ssl: false`（或提供可信证书）以避免握手错误。

**生产可用性评估**  
- **成熟度**：项目已有 458 ⭐、118 🍴，最近一次提交在 2026‑06‑29，活跃度尚可。代码基于 Python，遵循 Home Assistant 的集成框架，易于审计。  
- **适用场景**：适合原型验证、内部网络监控以及中小规模家庭/办公室部署。  
- **风险点**：  
  - 需要自行确认许可证兼容性（MIT/Apache 等）。  
  - 依赖 MikroTik API，若路由器固件升级导致 API 兼容性变化，可能需要维护者跟进。  
  - 安全上应使用最小权限的 API 用户，避免在 HA 中泄露全局管理员凭证。  
- **生产建议**：在正式上线前进行一次 **PoC**（如在测试 HA 实例中接入一台非关键路由器），验证以下几点：  
  1. 连接稳定性与延迟。  
  2. 实体更新频率对 HA 性能的影响。  
  3. 权限最小化配置是否满足业务需求。  
  4. 备份与恢复流程（如路由器 API 失效时的告警）。  

综上，`tomaae/homeassistant-mikrotik_router` 在功能完整性和社区认可度上已具备中等生产可用性，经过小规模验证并做好安全/权限控制后，可安全用于正式环境的网络监控与自动化。

## 🧭 Practical evaluation

**Value:** tomaae/homeassistant-mikrotik_router may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 458 GitHub stars
- 118 forks
- updated 2026-06-29
- primary language: Python
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 52/100 |
| stars | 57/100 |
| topics | 63/100 |
| outlook | 70/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 55/100 |
| production | 68/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/tomaae/homeassistant-mikrotik_router) · [← Back to Misc](./README.md)</sub>
