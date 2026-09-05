# trickv/hass-claude-usage

[![Stars](https://img.shields.io/github/stars/trickv/hass-claude-usage?style=flat-square&color=yellow)](https://github.com/trickv/hass-claude-usage/stargazers) [![Forks](https://img.shields.io/github/forks/trickv/hass-claude-usage?style=flat-square&color=blue)](https://github.com/trickv/hass-claude-usage/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Home Assistant integration for monitoring Claude (Anthropic) subscription usage in Home Assistant. Search for "Claude Usage" in HACS.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 32 |
| 🍴 **Forks** | 13 |
| 💻 **Language** | Python |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anthropic` `claude` `custom-component` `hacs` `homeassistant`

## 🎯 Categories

Payments · AI/ML · Observability

## 📝 Summary

### English

**Summary**  
`trickv/hass-claude-usage` is a Home Assistant custom component that pulls Anthropic Claude subscription metrics into Home Assistant, letting you monitor usage and costs directly from your dashboard. It is distributed through HACS under the “Claude Usage” entry and is written in Python (32 ★, 13 forks, last updated 2026‑06‑26).  

**Value**  
The integration gives you real‑time visibility of Claude API consumption, which is essential for controlling spend on AI services, budgeting, and automating alerts when usage thresholds are approached. By surfacing these metrics inside Home Assistant, you can combine them with existing automations—e.g., pause expensive workflows, trigger notifications, or log usage for accounting—without building a separate monitoring pipeline.

**Practical adoption path**  
1. **Proof‑of‑concept** – Add the component via HACS, enable the integration, and configure your Anthropic API key and optional thresholds. Verify that usage data appears in the Home Assistant UI.  
2. **Read‑me validation** – Review the README for required secrets, rate‑limit handling, and any optional sensors you want to expose.  
3. **Pilot automation** – Create a simple automation (e.g., send a notification when daily usage > X) to confirm the data can be used in automations.  
4. **Scale** – If the pilot meets expectations, extend the automation set (budget alerts, auto‑adjusting service calls, logging to external DB, etc.) and incorporate the component into your production Home Assistant configuration.

**Production readiness**  
The project is at a **medium** readiness level. It is actively maintained (last commit today), has modest community interest (32 stars), and the codebase is small and Python‑native, making it easy to audit. Before production deployment you should:

- Verify the license is compatible with your environment.  
- Perform a quick security review of the dependency chain (requests, aiohttp, etc.).  
- Pin the component version in HACS to avoid unexpected breaking changes.  

With these checks, the integration is suitable for prototypes, internal dashboards, or low‑risk production use where you need visibility into Claude billing without building a custom solution.

### Русский

**trickv/hass-claude-usage** — это открытая интеграция для Home Assistant, позволяющая в реальном времени отслеживать расход подписки Claude (Anthropic) и включать данные о потреблении в автоматизации дома. Типовой сценарий: добавить карту «Claude Usage» через HACS, настроить датчики и использовать их в скриптах для контроля расходов, уведомлений или ограничения использования сервисов ИИ. Готовность к production — средняя: проект подходит для прототипов и внутренних процессов, но перед развертыванием в продакшн рекомендуется провести небольшое POC, проверить актуальность README, лицензии и безопасность зависимостей.

### 中文

**项目简介**  
trickv/hass‑claude‑usage 是一款 Home Assistant 集成插件，可在 Home Assistant 仪表盘中实时监控 Anthropic Claude 的订阅使用量。只需在 HACS 中搜索 “Claude Usage” 即可安装。

**价值**  
- **费用可视化**：把 Claude 的 token 消耗、费用等关键指标直接展示在 Home Assistant 中，帮助用户及时掌握成本。  
- **自动化账单**：结合 HA 的自动化脚本，可在使用量达到阈值时触发提醒、暂停服务或自动生成账单，从而简化付费流程。  
- **快速验证 PSP 流程**：在原型或内部工作流中快速接入计费、结算或支付服务（PSP），无需自行编写监控代码。

**典型接入方式**  
1. 在 Home Assistant 的 HACS 中搜索并安装 “Claude Usage”。  
2. 在 **配置 → 集成** 中添加 Claude 账户的 API Key（或使用已有的 Anthropic 集成），并设置监控的订阅 ID。  
3. 配置仪表盘卡片或自动化规则，例如：  
   ```yaml
   automation:
     - alias: "Claude 使用量超限提醒"
       trigger:
         - platform: numeric_state
           entity_id: sensor.claude_usage
           above: 90  # 百分比阈值
       action:
         - service: notify.mobile_app
           data:
             message: "Claude 使用量已超过 90%，请检查或充值。"
   ```  
4. 如需对接支付平台，可在自动化中调用自建的 checkout / billing API，实现 “使用量 → 计费 → 支付” 的闭环。

**生产可用性**  
- **成熟度**：GitHub 32⭐、13 forks，最近一次提交于 2026‑06‑26，代码以 Python 为主，适合作为原型或内部工具使用。  
- **准备度**：中等（Medium）。在生产环境部署前建议：  
  - 完整审阅 README 与配置示例，确保 API Key 管理符合安全规范。  
  - 检查依赖库的安全性与许可证兼容性。  
  - 进行一次小规模的 PoC，验证监控数据的准确性与自动化触发的可靠性。  
- **运维要求**：定期关注上游更新，确保兼容最新的 Home Assistant 与 Anthropic API 版本；如有安全漏洞或依赖更新，及时升级。  

总体而言，trickv/hass‑claude‑usage 适合作为费用监控和计费自动化的快速落地方案，经过少量验证后即可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** trickv/hass-claude-usage helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 32 GitHub stars
- 13 forks
- updated 2026-06-26
- primary language: Python
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 32/100 |
| topics | 63/100 |
| outlook | 67/100 |
| quality | 58/100 |
| recency | 80/100 |
| adoption | 31/100 |
| production | 64/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/trickv/hass-claude-usage) · [← Back to Payments](./README.md)</sub>
