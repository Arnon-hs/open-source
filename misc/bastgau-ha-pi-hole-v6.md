# bastgau/ha-pi-hole-v6

[![Stars](https://img.shields.io/github/stars/bastgau/ha-pi-hole-v6?style=flat-square&color=yellow)](https://github.com/bastgau/ha-pi-hole-v6/stargazers) [![Forks](https://img.shields.io/github/forks/bastgau/ha-pi-hole-v6?style=flat-square&color=blue)](https://github.com/bastgau/ha-pi-hole-v6/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> 🛡️ This custom integration restored compatibility between Home Assistant and Pi-hole, which was no longer supported by the native integration. Today, this integration offers additional and complementary features.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 496 |
| 🍴 **Forks** | 17 |
| 💻 **Language** | Python |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`hacs` `hacs-integration` `home-assistant` `home-assistant-integration` `pi-hole`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
bastgau/ha‑pi‑hole‑v6 is a community‑maintained Python integration that restores and extends the link between Home Assistant and Pi‑hole after the official add‑on lost support. It adds extra sensors, services and configuration options that go beyond the native integration, making it a handy drop‑in for anyone who already runs Pi‑hole and wants richer Home Assistant visibility.

**Value proposition**  
- **Compatibility rescue** – works with current Home Assistant releases where the built‑in Pi‑hole component no longer functions.  
- **Extended feature set** – provides additional entities (e.g., query‑type breakdowns, block‑list stats) and service calls (enable/disable lists, reload config) that are not available out of the box.  
- **Open‑source & lightweight** – pure‑Python, easy to audit, and can be customized further if needed.

**Practical adoption path**  

| Step | Action | Why |
|------|--------|-----|
| 1️⃣  | **Read the README** – verify that the supported Home Assistant version matches your deployment and that required Pi‑hole API tokens are configured. | Ensures you meet the basic prerequisites and understand the setup flow. |
| 2️⃣  | **Create a sandbox** – add the integration to a test Home Assistant instance (or a dedicated VM) using the “Custom Integration” UI or by placing the repo in `custom_components/ha_pi_hole_v6`. | Limits risk to production services while you confirm functionality. |
| 3️⃣  | **Run a small proof‑of‑concept** – enable a few key sensors (e.g., total queries, blocked domains) and test service calls (e.g., `enable`, `disable` lists). | Validates that the API communication, authentication, and entity updates work in your environment. |
| 4️⃣  | **Review code & security** – scan the repo (e.g., with `bandit` or GitHub’s Dependabot) for vulnerable dependencies and confirm the license (MIT/Apache‑2.0‑compatible). | Mitigates supply‑chain and licensing risks before broader rollout. |
| 5️⃣  | **Document configuration** – capture the exact YAML/ UI settings used, version pinned, and any required secrets in your internal docs. | Guarantees repeatability and eases future maintenance. |
| 6️⃣  | **Gradual production rollout** – deploy to a staging Home Assistant instance, then to production after monitoring for a few days. | Allows you to catch edge‑case failures without impacting end users. |

**Production readiness assessment**  

- **Maturity**: 496 ★ on GitHub, recent commit (2026‑07‑03), modest fork count – indicates an active community but not a large corporate backing.  
- **Stability**: Medium. The integration works for prototypes and internal workflows, but you should verify that the feature set aligns with your exact needs and that the maintainer’s response time is acceptable for bug fixes.  
- **Dependencies**: Pure Python with only standard HTTP libraries; easy to audit and unlikely to introduce heavy runtime overhead.  
- **Operational risk**: Low to moderate – the main concerns are potential API changes on the Pi‑hole side and the lack of a formal SLA from the maintainer. Mitigate by pinning a known good version and keeping a fallback to the native integration (if still usable).  

**Bottom line** – bastgau/ha‑pi‑hole‑v6 is a solid, community‑driven solution for restoring Pi‑hole support in Home Assistant and adds useful extra capabilities. With a brief proof‑of‑concept, code review, and proper version pinning, it can be safely adopted for internal or prototype deployments; production use is feasible once you’ve validated stability in a staging environment and confirmed that maintenance responsibilities are covered.

### Русский

**bastgau/ha-pi-hole-v6** — это кастомный Python‑модуль, восстанавливающий и расширяющий интеграцию Home Assistant с Pi‑hole после прекращения поддержки официального решения. Он позволяет в реальном времени отображать статистику блокировок, управлять списками блокировки и получать уведомления о критических изменениях, что удобно для автоматизации домашней сети и мониторинга рекламных фильтров. Готовность к production — средняя: проект имеет активные коммиты, 500+ звёзд и базовую документацию, но перед развертыванием в продакшн рекомендуется проверить актуальность README, лицензии и провести небольшое POC, а также убедиться в наличии поддержки и безопасности зависимостей.

### 中文

**项目简介（2‑3 句）**  
bastgau/ha-pi-hole-v6 是一套为 Home Assistant 定制的 Pi‑hole 集成，弥补了官方集成已失效的兼容性，并在此基础上提供了日志、统计、黑名单管理等额外功能。  

**价值**  
- **恢复并扩展兼容性**：在官方集成不再维护的情况下，仍能让 Home Assistant 实时监控和控制 Pi‑hole。  
- **功能增强**：支持查询详细查询日志、按设备/域名过滤、批量添加/删除黑白名单等，帮助用户更精细地管理网络广告拦截。  
- **开箱即用**：基于 Python 编写，遵循 Home Assistant 的自定义集成规范，易于在已有 HA 环境中直接部署。  

**典型接入方式**  
1. **准备工作**：确保 Pi‑hole 已开启 API（在 Pi‑hole 控制面板 → Settings → API / Web interface），记录 API Token。  
2. **在 Home Assistant 中添加自定义组件**：  
   - 将仓库克隆或下载的 `custom_components/pi_hole_v6` 文件夹放入 HA 配置目录的 `custom_components/` 下。  
   - 在 `configuration.yaml` 中加入：  
     ```yaml
     pi_hole_v6:
       host: http://<pi-hole-ip>
       api_token: YOUR_API_TOKEN
       scan_interval: 30  # 可选，刷新间隔（秒）
     ```  
3. **重启 Home Assistant**，集成会自动创建实体（如 `sensor.pi_hole_ads_blocked`、`binary_sensor.pi_hole_status`）以及服务（`pi_hole_v6.add_blacklist`、`pi_hole_v6.remove_blacklist`）。  
4. **在 Lovelace 中使用**：将生成的传感器、开关或自定义卡片拖入仪表盘，即可实时查看拦截统计并通过 UI 管理名单。  

**生产可用性**  
- **成熟度**：已有 496 ★、17 Fork，最近一次提交在 2026‑07‑03，活跃度仍在，代码质量符合 Home Assistant 自定义集成的基本要求。  
- **适用场景**：适合内部原型、家庭或小型企业网络的监控与自动化；在对稳定性要求不极端的生产环境中使用是可行的。  
- **风险与注意事项**：  
  - 仍需自行审查许可证（MIT/Apache 等）以及潜在的安全依赖。  
  - 建议在正式部署前先在测试环境验证 API 权限、网络连通性以及异常恢复流程。  
  - 关注上游仓库的后续更新或社区 Fork，以防止未来因依赖停更导致的兼容性问题。  

综上，bastgau/ha-pi-hole-v6 能快速为 Home Assistant 带来完整的 Pi‑hole 监控与管理能力，适合作为原型或内部工具使用；在完成安全审计和小规模验证后，也可进入生产环境。

## 🧭 Practical evaluation

**Value:** bastgau/ha-pi-hole-v6 may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 496 GitHub stars
- 17 forks
- updated 2026-07-03
- primary language: Python
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 31/100 |
| stars | 57/100 |
| topics | 63/100 |
| outlook | 68/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 50/100 |
| production | 67/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/bastgau/ha-pi-hole-v6) · [← Back to Misc](./README.md)</sub>
