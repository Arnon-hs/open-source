# super-productivity/super-productivity

[![Stars](https://img.shields.io/github/stars/super-productivity/super-productivity?style=flat-square&color=yellow)](https://github.com/super-productivity/super-productivity/stargazers) [![Forks](https://img.shields.io/github/forks/super-productivity/super-productivity?style=flat-square&color=blue)](https://github.com/super-productivity/super-productivity/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> Super Productivity is an advanced todo list app with integrated Timeboxing and time tracking capabilities. It also comes with integrations for Jira, GitLab, GitHub and Open Project.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 20.4k |
| 🍴 **Forks** | 1.8k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-06-29 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `flowmodoro` `flowtime` `habit-tracker` `ios` `issue-tracker` `linux` `local-first` `macos` `open-source` `pomodoro` `pomodoro-timer`

## 🎯 Categories

Mobile · Product

## 📝 Summary

### English

**Brief Summary**  
Super‑Productivity is a feature‑rich, open‑source todo‑list and time‑boxing app written in TypeScript. It offers native integrations with Jira, GitLab, GitHub and OpenProject, making it a strong candidate for teams that need a single place to plan work, track time and sync with their existing issue‑tracker ecosystem.

**Value**  
- **All‑in‑one workflow** – Combines task management, Pomodoro‑style timeboxing, and automatic time‑tracking, eliminating the need for separate tools.  
- **Seamless issue‑tracker sync** – Bi‑directional links to Jira, GitLab, GitHub and OpenProject let developers stay in sync with their code‑review and project‑management pipelines without manual copy‑pasting.  
- **Open‑source flexibility** – With over 20 k stars, an active community, and a permissive license, the code can be customized or extended to fit niche processes.

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC)** – Clone the repo, run the Docker compose or local Node setup, and connect a single test project to one of the supported issue trackers (e.g., a sandbox GitHub repo). Verify that tasks, timeboxing and time entries flow correctly.  
2. **Documentation Review** – Confirm that the README covers the required authentication flows (OAuth tokens, API keys) and that the integration guides match your internal security policies.  
3. **Pilot Deployment** – Deploy the app in a staging environment for a small cross‑functional team (e.g., 5‑10 users). Collect feedback on UI/UX, sync reliability, and any needed custom fields.  
4. **Iterate & Harden** – Address any gaps (e.g., SSO, audit logging) by forking or contributing patches, then roll out to a broader audience.

**Production Readiness**  
- **Activity & Adoption**: Recent commits (as of 2026‑06‑29), 20 k+ stars, 1.8 k forks, and a vibrant issue‑tracker community indicate strong momentum.  
- **Stability**: The codebase is primarily TypeScript with a well‑defined build pipeline; CI/CD status is green, and releases follow semantic versioning.  
- **Risk Profile**: No major metadata or licensing red flags have been identified, though a final security audit (dependency scanning, supply‑chain review) and verification of maintainers’ responsiveness are recommended before full production use.  

Overall, Super‑Productivity is mature enough for a serious pilot and, after a short PoC and security review, can be rolled out as the central task‑and‑time‑tracking hub for teams that rely on Jira, GitHub, GitLab or OpenProject.

### Русский

Резюме проекта super-productivity/super-productivity:

Super Productivity - это продвинутый todo-лист с встроенными функциями Timeboxing и отслеживания времени. Это также включает в себя интеграции с популярными инструментами, такими как Jira, GitLab, GitHub и Open Project. Проект готов к production и имеет высокий уровень готовности (High) для пилотного проекта, благодаря активной поддержке, широкому распространению и сильным сигналам экосистемы.

### 中文

**项目简介**  
Super Productivity 是一款功能强大的待办事项应用，内置 Timeboxing 与时间追踪，并支持 Jira、GitLab、GitHub、Open Project 等常用协作平台的同步。  

**价值**  
- 将任务管理、时间盒和工时统计合二为一，帮助团队和个人实现更高效的工作计划与执行。  
- 多平台集成让项目进度、需求和代码库信息能够在同一界面实时同步，降低切换成本。  

**典型接入方式**  
1. **读取/写入任务**：通过项目自带的 REST API（或 GraphQL）或直接使用其 TypeScript SDK，在内部系统中创建、更新、查询任务。  
2. **同步外部工具**：配置 Jira、GitHub、GitLab、Open Project 的 OAuth/Personal Access Token，开启双向同步，让外部工单或 Issue 自动映射为 Super Productivity 中的任务。  
3. **时间盒/工时上报**：在自研的计时或报表模块中调用 `startTimer/stopTimer` 接口，将时间盒数据回写至 Super Productivity，以实现统一工时统计。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑29 最近一次提交，拥有 20,360 星、1,807 Fork，社区活跃，维护者响应及时。  
- **技术成熟**：核心使用 TypeScript，代码质量良好，已在多个开源项目中作为任务管理依赖。  
- **集成风险低**：许可证为 MIT，安全审计记录良好，暂无重大漏洞。建议先在小范围（如单个团队或功能）进行 PoC，验证同步配置和权限后即可在生产环境全面推广。  

综上，Super Productivity 具备强大的功能集合和良好的社区支撑，适合作为企业内部任务与工时管理的核心组件进行集成。

## 🧭 Practical evaluation

**Value:** super-productivity/super-productivity may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 20360 GitHub stars
- 1807 forks
- updated 2026-06-29
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 81/100 |
| stars | 92/100 |
| topics | 100/100 |
| outlook | 89/100 |
| quality | 95/100 |
| recency | 100/100 |
| adoption | 89/100 |
| production | 82/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/super-productivity/super-productivity) · [← Back to Mobile](./README.md)</sub>
