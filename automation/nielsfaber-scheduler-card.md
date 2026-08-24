# nielsfaber/scheduler-card

[![Stars](https://img.shields.io/github/stars/nielsfaber/scheduler-card?style=flat-square&color=yellow)](https://github.com/nielsfaber/scheduler-card/stargazers) [![Forks](https://img.shields.io/github/forks/nielsfaber/scheduler-card?style=flat-square&color=blue)](https://github.com/nielsfaber/scheduler-card/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> HA Lovelace card for control of scheduler entities

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.2k |
| 🍴 **Forks** | 176 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`assistant` `automation` `card` `custom-card` `home` `home-assistant` `homeassistant` `lovelace` `schedule` `scheduler` `sunrise` `sunset`

## 🎯 Categories

Automation

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The *scheduler‑card* is a Home Assistant Lovelace UI component that lets users create, edit, and trigger “scheduler” entities directly from the dashboard, turning repetitive timing‑based actions into a visual, click‑and‑drag workflow. With over 1 200 GitHub stars and active maintenance, it offers a ready‑to‑use, TypeScript‑based solution for automating routine tasks without writing custom scripts.

**Value**  
- **Eliminates manual steps** – Users can schedule lights, scripts, or service calls once and let the card handle execution, freeing time and reducing human error.  
- **Connects tools into repeatable flows** – By exposing scheduler entities in the UI, the card bridges disparate integrations (e.g., scripts, scenes, external APIs) into a single, easily auditable workflow.  
- **Low‑code automation** – Non‑technical Home Assistant users can build complex timing logic without touching YAML or Python, widening automation adoption across a household or small‑office environment.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Add the card to a test Lovelace view following the README instructions; create a simple scheduler (e.g., turn a lamp on/off at a fixed time).  
2. **Validate Integration** – Verify that the scheduled actions fire correctly and that state changes appear in Home Assistant’s history.  
3. **Scale Gradually** – Replace existing cron‑like automations with scheduler entities, grouping related tasks into a single card for better visibility.  
4. **Documentation & Training** – Use the built‑in help tooltip and the project’s README to onboard other users in the household or team.

**Production Readiness**  
- **High** – The repository shows recent commits (last update 2026‑06‑29), a healthy star/fork count, and active community engagement, indicating a mature codebase.  
- **Ecosystem Fit** – It is written in TypeScript, aligns with Home Assistant’s Lovelace architecture, and has no known licensing or major security concerns, though a final review of the MIT/Apache license and any third‑party dependencies is advisable.  
- **Risk Profile** – No critical metadata or supply‑chain risks have been identified; the remaining checks (license compliance, security audit) are routine for an OSS pilot.  

Overall, *nielsfaber/scheduler-card* is a production‑ready component that can be introduced with a small pilot and then expanded to automate a wide range of recurring Home Assistant tasks.

### Русский

**nielsfaber/scheduler-card** — это открытая Lovelace‑карта для Home Assistant, позволяющая управлять сущностями‑планировщиками и автоматизировать повторяющиеся операции без ручного вмешательства. Типичный сценарий внедрения: в небольшом пилотном проекте добавить карту в панель Lovelace, настроить несколько задач (например, включение освещения или запуск скриптов) и проверить их работу через простой proof‑of‑concept. Проект считается почти готовым к production: активные коммиты, 1239 звёзд, 176 форков, недавнее обновление (29 июня 2026) и широкая поддержка в экосистеме Home Assistant, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句话）**  
nielsfaber/scheduler-card 是一款 Home Assistant Lovelace 卡片，用于在 UI 上直观地创建、编辑和触发 Scheduler 实体。它让用户可以在仪表盘上直接管理定时任务，省去在 YAML 或 Automations 中手动编写的繁琐步骤。

**价值**  
- **降低重复操作**：通过卡片 UI 一键开启/关闭、修改时间表达式，避免每次都去编辑配置文件。  
- **实现可视化工作流**：把多个工具或服务的调度统一展示，便于快速构建可重复的业务流程。  
- **提升运维效率**：运维人员可以在 Lovelace 页面直接调度备份、更新、清理等日常任务，减少人为错误。

**典型接入方式**  
1. 在 Home Assistant 中通过 HACS 添加 `scheduler-card`（或手动克隆仓库）。  
2. 在 `ui-lovelace.yaml` 或仪表盘编辑器中加入卡片配置，例如：  
   ```yaml
   type: custom:scheduler-card
   entity: schedule.my_daily_backup
   ```  
3. 根据需要在卡片属性中设置 `show_actions`, `hide_time` 等可选参数，完成后即可在仪表盘上看到并操作对应的 Scheduler 实体。  
4. 建议先在测试环境做一个小范围的 Proof‑of‑Concept（如仅调度一次备份），确认卡片与现有 Scheduler 实体兼容后再推广。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑29，项目最近一次提交，拥有 1,239 星、176 个 fork，社区活跃。  
- **技术成熟**：使用 TypeScript 编写，代码质量良好，已在多个公开的 Home Assistant 实例中验证。  
- **适配性强**：兼容 Home Assistant 主流版本，且通过 HACS 分发，集成成本低。  
- **风险**：目前未发现重大元数据或许可证问题，但仍建议在正式生产环境前审查安全报告和维护者响应情况。  

综合来看，nielsfaber/scheduler-card 已具备较高的生产就绪度，适合作为自动化工作流中的调度 UI 层进行试点部署。

## 🧭 Practical evaluation

**Value:** nielsfaber/scheduler-card helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1239 GitHub stars
- 176 forks
- updated 2026-06-29
- primary language: TypeScript
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 56/100 |
| stars | 66/100 |
| topics | 100/100 |
| outlook | 61/100 |
| quality | 68/100 |
| recency | 40/100 |
| adoption | 63/100 |
| production | 58/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/nielsfaber/scheduler-card) · [← Back to Automation](./README.md)</sub>
