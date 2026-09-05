# LambdaHack/LambdaHack

[![Stars](https://img.shields.io/github/stars/LambdaHack/LambdaHack?style=flat-square&color=yellow)](https://github.com/LambdaHack/LambdaHack/stargazers) [![Forks](https://img.shields.io/github/forks/LambdaHack/LambdaHack?style=flat-square&color=blue)](https://github.com/LambdaHack/LambdaHack/network) [![Language](https://img.shields.io/badge/lang-Haskell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> Haskell game engine library for roguelike dungeon crawlers; please offer feedback, e.g., after trying out the sample game with the web frontend at

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 661 |
| 🍴 **Forks** | 57 |
| 💻 **Language** | Haskell |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ascii` `browsergame` `engine` `freesoftware` `game` `gamedev` `haskell` `html5` `indiedev` `library` `pcg` `replayability`

## 🎯 Categories

Games & Graphics

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
LambdaHack is a Haskell library that provides a full‑featured game‑engine framework for building roguelike dungeon crawlers, complete with a web‑frontend demo. It lets developers focus on AI and gameplay mechanics rather than low‑level engine code, and the project invites feedback after trying the sample game. With over 660 stars and recent activity, it’s a mature open‑source option for rapid prototyping of AI‑driven game agents.

**Value**  
- **Accelerated AI prototyping** – The engine supplies world simulation, entity management, and turn‑based mechanics out of the box, so AI researchers can plug in reinforcement‑learning, planning, or retrieval‑augmented generation (RAG) models without building a game loop from scratch.  
- **Reusable components** – Built‑in support for map generation, field‑of‑view, combat, and a web UI lets teams experiment with different AI techniques (e.g., hierarchical agents, curriculum learning) in a consistent environment.  
- **Open‑source community** – A modest but active Haskell community contributes bug fixes and extensions, providing a reference point for best practices in functional‑style game AI.

**Practical Adoption Path**  
1. **Read the README & run the web demo** – Verify the toolchain (Stack or Cabal) and confirm the sample game works locally.  
2. **Create a minimal proof‑of‑concept** – Fork the repo, replace the default “monster” AI with a simple scripted policy, and run a few episodes to ensure the engine’s callbacks (e.g., `onTurn`, `onMove`) are reachable from your model code.  
3. **Integrate your AI stack** – Wrap your Python/ML code with a thin Haskell FFI layer or use a microservice architecture (e.g., expose a REST endpoint that the Haskell engine queries for actions).  
4. **Iterate and benchmark** – Leverage the built‑in logging and turn‑based stepping to collect data, tune hyper‑parameters, and compare baseline agents.  
5. **Scale up** – Once the POC is stable, expand the world (larger dungeons, more entities) and add richer observation spaces (e.g., visual tiles, inventory) to support more sophisticated models.

**Production Readiness**  
- **Maturity**: Medium. The engine is stable enough for internal prototypes and sandbox experiments, but it is not a turnkey commercial product.  
- **Dependencies**: Pure Haskell with a modest set of libraries; however, teams unfamiliar with Haskell will need to allocate time for onboarding and build‑pipeline setup.  
- **Maintenance**: Active commits as of 2026‑06‑30, but long‑term support depends on the open‑source community; consider pinning versions and adding internal tests.  
- **Risk Mitigation**: Validate the integration cost early (e.g., by completing the POC) and isolate the AI component behind a service boundary to reduce coupling to Haskell internals.  

Overall, LambdaHack offers a solid foundation for experimenting with AI in roguelike environments, with a clear, incremental adoption route that can be hardened for production use after an initial proof‑of‑concept and dependency audit.

### Русский

**LambdaHack/LambdaHack** — открытая Haskell‑библиотека‑движок для создания roguelike‑игр, позволяющая быстро добавить AI‑возможности (например, RAG‑агентов или прототипы игровых ботов) без разработки собственного стека моделей. Типичный путь внедрения — запуск небольшого proof‑of‑concept: собрать пример‑игру с веб‑фронтендом, изучить README и интегрировать нужные AI‑модули в существующий пайплайн. Готовность к production — средняя: проект стабилен и имеет активное сообщество (661 ★), но требует проверки зависимостей и поддержки Haskell‑стека перед использованием в продакшене.

### 中文

**简短介绍**

LambdaHack/LambdaHack 是一个基于 Haskell 的游戏引擎库，专门用于创建 roguelike dungeon crawler 类型的游戏。它提供了 AI 能力，帮助开发者快速 prototyping 和评估模型工具。

**价值**

LambdaHack/LambdaHack 的价值在于，它可以帮助开发者快速添加 AI 能力，而无需从头开始构建模型栈。它适合用于 prototype AI 特性、构建 RAG 或 agent 工作流，以及评估模型工具。

**典型接入方式**

通常情况下，开发者会首先评估 LambdaHack/LambdaHack 的 sample game 和 web 前端，了解其基本功能和接口。然后，可以通过阅读 README 和小规模的 proof of concept 来了解其接入方式。最后，需要仔细检查依赖和维护成本，以确保其生产可用性。

**生产可用性**

LambdaHack/LambdaHack 的生产可用性为中等（Medium）。它适合用于 prototyping 或内部工作流，但在生产环境中需要进行更多的依赖和维护检查。

## 🧭 Practical evaluation

**Value:** LambdaHack/LambdaHack helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 661 GitHub stars
- 57 forks
- updated 2026-06-30
- primary language: Haskell
- 17 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 60/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 75/100 |
| recency | 80/100 |
| adoption | 56/100 |
| production | 68/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/LambdaHack/LambdaHack) · [← Back to Games--graphics](./README.md)</sub>
