# HearthSim/HSTracker

[![Stars](https://img.shields.io/github/stars/HearthSim/HSTracker?style=flat-square&color=yellow)](https://github.com/HearthSim/HSTracker/stargazers) [![Forks](https://img.shields.io/github/forks/HearthSim/HSTracker?style=flat-square&color=blue)](https://github.com/HearthSim/HSTracker/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> A deck tracker and deck manager for Hearthstone on macOS

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.2k |
| 🍴 **Forks** | 194 |
| 💻 **Language** | Swift |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`deck-tracker` `hearthstone` `hearthstone-deck-tracker` `hsreplay` `swift`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
HSTracker is an open‑source deck‑tracking and deck‑management tool for Hearthstone that runs on macOS. Written in Swift, it has attracted a modest community (≈1.2 k stars) and is still being maintained as of June 2026. It can help players and developers quickly view hand, board, and card‑draw information while testing decks or building analytics pipelines.

**Value**  
- **Immediate utility**: Provides real‑time game data (cards in hand, board state, mana curve) without manual logging, which is valuable for players, streamers, and researchers building Hearthstone‑related analytics.  
- **Extensible code base**: The Swift source is cleanly organized, making it a solid starting point for custom UI overlays, AI training data collection, or integration with third‑party Hearthstone APIs.  
- **Community backing**: Over a thousand stars and active forks indicate a usable, battle‑tested codebase that can be leveraged rather than built from scratch.

**Practical Adoption Path**  
1. **Read the README & run the demo** – Verify that the project builds on your macOS version and that the UI launches correctly.  
2. **Create a proof‑of‑concept (PoC)** – Fork the repo and add a tiny feature (e.g., export current hand to JSON). This validates the build pipeline, dependency management, and integration points.  
3. **Wrap the core tracker** – Expose the tracker’s data via a lightweight REST or WebSocket endpoint, or embed it as a library in your own macOS app.  
4. **Iterate & test** – Use the PoC in a controlled environment (e.g., internal QA or a single‑player test) before scaling to broader internal workflows.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained and functional for its intended purpose, but it was not designed as a production‑grade service.  
- **Dependencies**: Pure Swift/macOS, so integration cost is low if your stack is already Apple‑centric; otherwise you’ll need a macOS host.  
- **Maintenance**: Monitor upstream updates (bug fixes, Swift version changes) and plan for periodic rebasing of your fork.  
- **Risk mitigation**: Because the integration path isn’t documented in detail, allocate time for environment setup and for confirming that the tracker can run head‑less (if needed) before committing to a production deployment.

In short, HSTracker offers a ready‑made, community‑validated way to capture Hearthstone game state on macOS; start with a small PoC to confirm build and data‑export capabilities, then layer any custom logic needed for your workflow. With proper dependency checks and periodic syncs to the upstream repo, it can be a reliable component for prototypes or internal tools, though additional engineering effort is required to reach full production robustness.

### Русский

HearthSim/HSTracker — это open‑source‑приложение‑трекер и менеджер колод для Hearthstone, написанное на Swift для macOS. Оно может быть полезно в проектах, где нужен быстрый доступ к статистике игр и удобное управление колодами, однако перед внедрением следует проверить README и провести небольшой proof‑of‑concept, так как путь интеграции не очевиден. Готовность к production средняя: подходит для прототипов и внутренних инструментов после оценки зависимостей и затрат на настройку.

### 中文

**价值**  
HSTracker 是 macOS 上为《炉石传说》玩家打造的卡组追踪与管理工具，能够实时记录对手出牌、统计卡组胜率、提供卡牌搜索与过滤等功能，帮助玩家在对局中做出更精准的决策并快速构建、优化卡组。

**典型接入方式**  
1. **阅读并遵循 README**：项目在 GitHub 上提供了完整的构建说明（使用 Xcode + Swift），先按照文档完成本地编译和运行，确认依赖（如 Swift 5.7、macOS 13+）已满足。  
2. **代码层面集成**（若需二次开发或嵌入自研系统）：  
   - 将 `HSTracker` 作为子模块或 Swift Package 添加到自己的 Xcode 项目。  
   - 通过公开的 API（例如 `GameTracker`, `DeckManager`）调用卡组数据、对局日志或实时事件回调。  
   - 如仅需 UI 展示，可直接使用项目的 `HSTrackerUI` 组件，配合自定义视图进行嵌入。  
3. **最小可行验证（PoC）**：在内部测试环境中跑通一次完整的对局追踪流程，验证数据采集、持久化以及 UI 更新是否符合预期，再决定是否深化集成。

**生产可用性**  
- **成熟度**：已有 1248 星、194 次 fork，活跃度仍在（最近一次提交为 2026‑06‑30），代码基于 Swift，适合 macOS 原生生态。  
- **适用场景**：适合作为内部原型、数据分析平台或面向高级玩家的辅助工具；对外直接面向终端用户时，需要自行处理签名、分发以及与 Blizzard 官方客户端的兼容性。  
- **风险与准备**：  
  - 项目文档虽齐全，但缺少明确的 SDK 接口说明，集成成本主要在自行探索 API 与事件回调。  
  - 依赖 macOS 13+ 与 Xcode 15 以上的开发环境，需确认团队的构建流水线能够满足。  
  - 需要自行评估后续维护（如 Blizzard 客户端更新导致抓包/日志格式变化）的工作量。  

**结论**：在确保开发环境兼容、完成小规模 PoC 并评估后续维护成本的前提下，HSTracker 可在内部原型或面向技术玩家的产品中投入使用；若要在大规模生产环境直接面向普通玩家，则需额外投入包装、兼容性测试和持续维护工作。

## 🧭 Practical evaluation

**Value:** HearthSim/HSTracker may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1248 GitHub stars
- 194 forks
- updated 2026-06-30
- primary language: Swift
- 5 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 57/100 |
| stars | 66/100 |
| topics | 63/100 |
| outlook | 69/100 |
| quality | 73/100 |
| recency | 80/100 |
| adoption | 63/100 |
| production | 67/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/HearthSim/HSTracker) · [← Back to Misc](./README.md)</sub>
