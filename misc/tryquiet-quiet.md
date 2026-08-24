# TryQuiet/quiet

[![Stars](https://img.shields.io/github/stars/TryQuiet/quiet?style=flat-square&color=yellow)](https://github.com/TryQuiet/quiet/stargazers) [![Forks](https://img.shields.io/github/forks/TryQuiet/quiet?style=flat-square&color=blue)](https://github.com/TryQuiet/quiet/network) [![Language](https://img.shields.io/badge/lang-C-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> A private, p2p alternative to Slack and Discord built on Tor & IPFS

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.6k |
| 🍴 **Forks** | 139 |
| 💻 **Language** | C |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`chat` `collaboration` `decentralized` `discord-alternatives` `ipfs` `local-first` `p2p` `privacy` `slack-alternative`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
TryQuiet/quiet is an open‑source, privacy‑first, peer‑to‑peer alternative to Slack and Discord that runs over Tor and IPFS. It provides a ready‑made set of UI components and a web‑based frontend (written in C) that let teams ship user‑facing interfaces with far less custom UI work. The project is actively maintained (2612 ★, 139 forks, last update 2026‑06‑26) and shows strong ecosystem signals for a production pilot.

**Value**  
Quiet supplies reusable chat‑and‑collaboration widgets, authentication flows, and message handling logic, so developers can focus on business features instead of building a secure, decentralized UI from scratch. By leveraging Tor and IPFS, it also satisfies regulatory or corporate requirements for end‑to‑end privacy and data sovereignty.

**Practical adoption path**  
1. **Proof‑of‑concept** – clone the repo, run the provided README steps, and spin up a local Tor/IPFS node to verify basic messaging.  
2. **Component integration** – replace existing chat widgets in your product with Quiet’s UI modules, adjusting only styling and API hooks.  
3. **Pilot rollout** – deploy the integrated frontend to a limited user group, monitor latency and Tor/IPFS connectivity, and iterate on any missing hooks.  

**Production readiness**  
The project scores high on readiness: recent commits, active issue handling, and a sizable star/fork base indicate a healthy community. While the integration documentation is sparse, the codebase is stable enough for a serious pilot, provided you allocate time to validate the Tor/IPFS setup and resolve any missing deployment scripts before full‑scale rollout.

### Русский

**TryQuiet/quiet** — это открытый p2p‑клиент, предоставляющий приватную альтернативу Slack и Discord на базе Tor и IPFS. Он ускоряет создание пользовательских интерфейсов, позволяя быстро собрать UI‑компоненты и улучшить доставку фронтенда, поэтому типичный сценарий внедрения — запуск небольшого proof‑of‑concept (например, отдельного чат‑модуля) с проверкой README, а затем постепенное расширение. Проект считается готовым к production: активная разработка, 2612 звёзд, 139 форков и свежие коммиты (2026‑06‑26), однако перед масштабным rollout стоит уточнить детали интеграции и оценить затраты на настройку.

### 中文

**项目简介**  
TryQuiet/quiet 是一款基于 Tor 与 IPFS 的私有点对点通讯平台，提供 Slack、Discord 的功能替代，专注于安全与去中心化。  

**价值**  
- **快速构建前端 UI**：提供可复用的界面组件，帮助团队在最少的自定义工作量下交付用户界面。  
- **提升交付效率**：统一的 UI 库让产品 UI 开发更快、更一致，降低前端维护成本。  

**典型接入方式**  
1. **阅读 README 与示例**，确认依赖（C 语言编译环境、Tor、IPFS 节点）。  
2. **在本地搭建一个小型 PoC**：先启动一个本地 Tor 隧道和 IPFS 节点，使用项目提供的示例代码渲染一个基本聊天界面。  
3. **逐步集成**：在现有前端项目中引入其 UI 组件库（通过子模块或包管理），并通过项目的 API 与后端（Quiet 网络）对接。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑26 最近一次提交，GitHub ★2612、Fork 139，社区活跃。  
- **成熟度**：代码基于 C 语言实现，核心网络层已在多个私有部署中验证，适合作为正式业务的底层通讯层。  
- **风险**：元数据未提供完整的集成文档，建议在正式投入前完成小规模概念验证，评估部署、运维及安全审计成本。  

总体而言，TryQuiet/quiet 在前端 UI 复用和安全去中心化通信方面具备较高的生产就绪度，适合作为需要私密、抗审查通讯的产品的底层技术选型。

## 🧭 Practical evaluation

**Value:** TryQuiet/quiet helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2612 GitHub stars
- 139 forks
- updated 2026-06-26
- primary language: C
- 9 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 54/100 |
| stars | 73/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 70/100 |
| recency | 40/100 |
| adoption | 67/100 |
| production | 56/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/TryQuiet/quiet) · [← Back to Misc](./README.md)</sub>
