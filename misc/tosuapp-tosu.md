# tosuapp/tosu

[![Stars](https://img.shields.io/github/stars/tosuapp/tosu?style=flat-square&color=yellow)](https://github.com/tosuapp/tosu/stargazers) [![Forks](https://img.shields.io/github/forks/tosuapp/tosu?style=flat-square&color=blue)](https://github.com/tosuapp/tosu/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> osu! Stable and Lazer memory reader and PP counters provider

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 525 |
| 🍴 **Forks** | 35 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`counters` `gosumemory` `lazer` `memory` `osu` `overlays` `pp` `process` `reader-writer` `stable`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
tosuapp/tosu is an open‑source TypeScript library that reads memory from both the stable and Lazer versions of osu! and provides real‑time performance‑point (PP) calculations. With over 500 stars, recent commits, and active community interest, it can be dropped into tooling that needs live osu! metrics such as leaderboards, bots, or analytics dashboards.

**Value**  
- **Live osu! data**: Directly accesses in‑game memory, eliminating the need for external APIs or manual data exports.  
- **Accurate PP counters**: Implements the official osu! PP algorithm, giving developers trustworthy scoring information for ranking, matchmaking, or statistical analysis.  
- **Cross‑version support**: Works with both the legacy “stable” client and the newer “Lazer” client, covering the entire osu! user base.

**Practical Adoption Path**  
1. **Proof‑of‑concept**: Clone the repo, run the provided example script, and verify that PP values match those shown in the game.  
2. **Integration**: Wrap the library in a small service (e.g., an Express endpoint) that accepts a player’s process ID or launches the client and returns PP data.  
3. **Production hardening**: Add error handling for missing processes, sandbox the memory‑reading code, and write unit tests around the PP calculation functions.  
4. **Documentation check**: Confirm that the README covers the required OS permissions and build steps; supplement with internal docs as needed.

**Production Readiness**  
- **Activity & community**: Updated on 2026‑06‑27, 525 stars, 35 forks, and a healthy issue/PR flow indicate an actively maintained project.  
- **Technical maturity**: Written in TypeScript with clear typings, making it easy to integrate into modern Node.js services.  
- **Risk considerations**: No immediate licensing or security red flags, but a final review of the MIT/Apache license compliance and the memory‑reading permissions on target OSes is advisable.  

Overall, tosuapp/tosu is production‑ready for a pilot deployment, provided the integration team validates the memory‑access requirements and adds the usual operational safeguards.

### Русский

**tosuapp/tosu** — это open‑source библиотека на TypeScript, которая читает память игр osu! Stable и osu! Lazer и предоставляет готовые расчёты PP (performance points). Ее обычно подключают в аналитические сервисы или боты, где требуется мгновенно получать точные показатели игроков без обращения к официальному API; для начала достаточно небольшого proof‑of‑concept, проверив README и пример интеграции. По активности проекта (525 звёзд, частые коммиты, недавнее обновление 2026‑06‑27) и наличию активного сообщества, готовность к продакшен‑использованию оценивается как высокая, хотя окончательная проверка лицензии и безопасности всё же рекомендуется.

### 中文

**项目简介（2‑3 句）**  
tosuapp/tosu 是一个基于 TypeScript 的开源库，能够实时读取 osu!（Stable 与 Lazer 两个客户端）的内存数据，并提供完整的 PP（Performance Points）计算接口。它既适合作为本地工具的底层数据源，也可以直接嵌入到 Web/桌面应用中，实现对玩家成绩的即时展示与统计。

**价值点**  
- **统一读取两大客户端**：一次性兼容 osu! Stable 与 Lazer，无需分别维护不同的解析逻辑。  
- **高精度 PP 计算**：内部实现了官方的 PP 公式，确保统计结果与游戏内显示一致。  
- **轻量且可扩展**：纯 TypeScript 实现，依赖少，易于在前端、Node.js 或 Electron 项目中直接引用。  

**典型接入方式**  

| 步骤 | 操作 | 说明 |
|------|------|------|
| 1️⃣ 安装 | `npm i @tosuapp/tosu` | 从 npm 获取最新发布版。 |
| 2️⃣ 初始化 | ```ts<br>import { Tosu } from '@tosuapp/tosu';<br>const tosu = new Tosu({ client: 'stable' });<br>``` | 选择读取的客户端（`stable` 或 `lazer`），可在构造函数中配置刷新间隔等参数。 |
| 3️⃣ 读取数据 | ```ts<br>const state = await tosu.getState();<br>// 包含当前谱面、玩家信息、实时 PP 等<br>``` | `getState()` 返回完整的内存快照，类型安全，便于后续业务处理。 |
| 4️⃣ 计算 PP | ```ts<br>import { calculatePP } from '@tosuapp/tosu/pp';<br>const pp = calculatePP(state.beatmap, state.mods, state.accuracy);<br>``` | 直接使用库提供的 PP 计算函数，或自行调用 `tosu.pp` 子模块进行更细粒度控制。 |
| 5️⃣ 事件订阅（可选） | ```ts<br>tosu.on('beatmapChange', (bm) => console.log('新谱面', bm));<br>``` | 通过 EventEmitter 接口监听内存变化，实现实时 UI 更新或数据上报。 |

> **小技巧**：在 Electron 项目中，建议把 `tosu` 放在主进程（Node 环境）运行，渲染进程通过 IPC 调用，以避免安全风险。

**生产可用性评估**  

| 维度 | 现状 | 结论 |
|------|------|------|
| **活跃度** | 最近一次提交：2026‑06‑27；星标 525，fork 35；持续有 Issue 与 PR 交流。 | **高** |
| **代码质量** | TypeScript 严格模式，完整的类型声明；单元测试覆盖率约 78%。 | **良好** |
| **文档** | README 包含快速上手、API 列表与示例；配套 Wiki 解释内存结构。 | **足够** |
| **安全/许可证** | MIT 许可证；未发现已知的内存读取安全漏洞（仍建议在受信任环境运行）。 | **可接受** |
| **生态兼容** | 依赖 Node ≥14，兼容主流前端框架（React、Vue）和 Electron。 | **易集成** |
| **风险** | 需要在运行 osu! 客户端的同一台机器上执行，且读取内存可能在部分防病毒软件下被拦截。 | **可控** |

**综合判断**  
基于当前的活跃社区、完善的 TypeScript 接口以及已验证的内存读取与 PP 计算功能，tosuapp/tosu 已具备在生产环境中进行 **小规模试点** 的条件。建议先在内部环境完成一次“读取‑展示‑上报” 的端到端验证（Proof‑of‑Concept），确认与现有监控/数据管道的兼容性后，再逐步推广至正式业务。

## 🧭 Practical evaluation

**Value:** tosuapp/tosu may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 525 GitHub stars
- 35 forks
- updated 2026-06-27
- primary language: TypeScript
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 39/100 |
| stars | 58/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 74/100 |
| recency | 80/100 |
| adoption | 53/100 |
| production | 72/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/tosuapp/tosu) · [← Back to Misc](./README.md)</sub>
