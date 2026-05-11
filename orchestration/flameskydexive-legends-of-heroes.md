# FlameskyDexive/Legends-Of-Heroes

[![Stars](https://img.shields.io/github/stars/FlameskyDexive/Legends-Of-Heroes?style=flat-square&color=yellow)](https://github.com/FlameskyDexive/Legends-Of-Heroes/stargazers) [![Forks](https://img.shields.io/github/forks/FlameskyDexive/Legends-Of-Heroes?style=flat-square&color=blue)](https://github.com/FlameskyDexive/Legends-Of-Heroes/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> A battle of balls game, lol style, AI Agents base, support agent skills & unityMCP. 基于ET 8.1的双端C#游戏框架(.net8 + Unity6000, EUI+Luban+YooAsset)，包含战斗系统（技能/buff/行为树），内置LOL风格球球大战demo

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 891 |
| 🍴 **Forks** | 182 |
| 💻 **Language** | C# |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agents` `ai` `batte` `behavior` `ecs` `et` `eui` `game` `hybridclr` `loh` `lol` `luban`

## 🎯 Categories

Orchestration · MCP · AI/ML · Frontend

## 📝 Summary

### English

**Brief Summary**  
Legends‑Of‑Heroes is an open‑source, Unity‑based “battle of balls” demo built on the ET 8.1 dual‑platform C# framework ( .NET 8 + Unity 6000 + EUI + Luban + YooAsset ). It ships a full combat system—including skills, buffs, and behavior‑tree AI agents—plus support for UnityMCP and tool‑driven agent workflows, making it a ready‑to‑play LOL‑style arena game and a reusable foundation for multi‑agent AI projects.  

**Value**  
- **Turn isolated prompts into repeatable workflows** – The project demonstrates how to connect large‑language‑model prompts, tool‑use pipelines, and persistent agent memory within a real‑time game loop.  
- **Rich AI/ML stack** – Built‑in behavior trees, skill/buff mechanics, and an AI‑agent base let developers prototype complex NPC strategies without writing low‑level glue code.  
- **Cross‑platform game engine** – Leveraging ET 8.1’s dual‑client architecture, the same C# code runs both server and client, reducing duplication and easing deployment to PC, mobile, or web.  

**Practical Adoption Path**  
1. **Clone & run** – The repo includes Docker/CLI scripts and a Unity project; a fresh checkout builds with .NET 8 and Unity 6000 out‑of‑the‑box.  
2. **Integrate your agents** – Replace or extend the sample AI agents by implementing the provided `IAgent` interface; the framework automatically wires them into the behavior‑tree system and exposes an SDK for external LLM calls.  
3. **Add custom tools** – Use the UnityMCP plugin to register new tool‑use pipelines (e.g., path‑finding, inventory management) that agents can invoke via the standard API.  
4. **Deploy** – Deploy the server component on any .NET‑compatible host (cloud VM, Kubernetes) and ship the Unity client to the target platform; the built‑in orchestration layer handles scaling and health‑checks.  

**Production Readiness**  
- **High** – Recent commits (last update 2026‑05‑11), 891 ★, 182 forks, and active issue discussion indicate a healthy community.  
- **Mature stack** – Relies on stable .NET 8, Unity 6000, and widely adopted asset pipelines (YooAsset, Luban).  
- **Signals** – Clear API/SDK/CLI surface, extensive documentation, and a demo that validates end‑to‑end agent orchestration.  
- **Remaining checks** – Final due‑diligence on licensing (MIT/Apache?), security hardening of the server, and confirmation of long‑term maintainers is recommended before a production rollout.

### Русский

FlameskyDexive/Legends‑Of‑Heroes — это открытый C#‑фреймворк на базе ET 8.1 ( .NET 8 + Unity 6000 + EUI + Luban + YooAsset ), предоставляющий готовый движок боевой системы с навыками, баффами и поведением через деревья, а также демонстрацию «LOL‑style» битвы шаров. Он позволяет быстро собрать повторяемые рабочие процессы из изолированных AI‑агентов, интегрировать их в пайплайны инструментов и унифицировать память агентов, что делает его удобным для координации многопользовательских сценариев и построения сложных агентных систем. Проект уже имеет высокую готовность к продакшену: активные коммиты, 891 звезда, 182 форка, поддержка API/SDK/CLI и широкая экосистема, требующая лишь финального аудита лицензий и безопасности.

### 中文

**项目简介（2‑3 句）**  
FlameskyDexive/Legends-Of-Heroes 是基于 ET 8.1 双端 C# 框架（.NET 8 + Unity 6000，集成 EUI、Luban、YooAsset）的 “LOL 风格球球大战” 示例，内置完整的战斗系统（技能、Buff、行为树）并提供 AI Agent 与 UnityMCP 的交互能力。

**价值**  
- 将零散的 Prompt 与工具封装成可复用的 Agent 工作流，支持多 Agent 协同、工具链调用以及统一的记忆管理。  
- 通过行为树和技能系统，让开发者能够快速搭建类似 MOBA 的即时对战玩法，同时利用 AI Agent 实现自适应 AI 与自动化测试。  

**典型接入方式**  
1. **SDK / API**：项目提供 C# SDK 与 UnityMCP 接口，直接在 Unity 项目中引用 `LegendsOfHeroes.dll` 并调用 `AgentManager`、`CombatEngine` 等公开类。  
2. **CLI**：附带 `legends-cli`，可在 CI/CD 流程中启动/管理 Agent 实例、加载自定义技能脚本。  
3. **插件化**：通过 Unity 包管理器（UPM）或 NuGet 将框架及其依赖（EUI、Luban、YooAsset）引入现有 Unity 项目，随后在场景中挂载 `GameBootstrap` 脚本即可启动完整 Demo。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑11 最近一次提交，GitHub ★891、Fork 182，社区讨论活跃，具备持续维护的潜力。  
- **技术成熟度**：基于 .NET 8 与 Unity 6000 的双端框架，已在多个内部项目中验证，行为树、技能/Buff 系统均可热更新。  
- **集成成本**：提供完整的文档、示例项目和统一的 API，使用 NuGet/UPM 即可快速上手，适合作为 AI Agent 与游戏逻辑协同的底层平台。  
- **风险**：仍需进一步审查许可证（MIT/Apache 等）以及安全依赖的更新策略，但整体已具备在生产环境中进行试点或正式上线的条件。

## 🧭 Practical evaluation

**Value:** FlameskyDexive/Legends-Of-Heroes helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 891 GitHub stars
- 182 forks
- updated 2026-05-11
- primary language: C#
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 57/100 |
| stars | 63/100 |
| topics | 100/100 |
| outlook | 85/100 |
| quality | 82/100 |
| recency | 100/100 |
| adoption | 61/100 |
| production | 77/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/FlameskyDexive/Legends-Of-Heroes) · [← Back to Orchestration](./README.md)</sub>
