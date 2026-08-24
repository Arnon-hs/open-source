# Xeeynamo/sotn-decomp

[![Stars](https://img.shields.io/github/stars/Xeeynamo/sotn-decomp?style=flat-square&color=yellow)](https://github.com/Xeeynamo/sotn-decomp/stargazers) [![Forks](https://img.shields.io/github/forks/Xeeynamo/sotn-decomp?style=flat-square&color=blue)](https://github.com/Xeeynamo/sotn-decomp/network) [![Language](https://img.shields.io/badge/lang-C-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-46%2F100-brightgreen?style=flat-square)](#)

> Decompilation of Castlevania: Symphony of the Night (PSX, PSP, Saturn)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 965 |
| 🍴 **Forks** | 82 |
| 💻 **Language** | C |
| 📈 **Score** | 46/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`decompilation` `game`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Xeeynamo’s **sotn‑decomp** is an open‑source effort to decompile the classic PlayStation titles *Castlevania: Symphony of the Night* (PSX, PSP, Saturn) into readable C code. With over 965 stars and recent activity (last commit 2026‑07‑03), the repository provides a foundation for reverse‑engineering, modding, or academic study of the game’s engine.

**Value Proposition**  
- **Deep Insight:** The decompiled source reveals the game’s original logic, data structures, and rendering pipeline, enabling developers to understand, modify, or extend the original title without starting from scratch.  
- **Community Backing:** A sizable star count and active forks indicate a community that can help troubleshoot and contribute improvements.  
- **Reusable Assets:** The C code can be repurposed for fan‑made ports, tool‑chain development, or as a teaching resource for low‑level game programming.

**Practical Adoption Path**  
1. **Clone & Build:** Pull the repo, follow the README to set up the required toolchain (PSX SDK, C compiler, make).  
2. **Validate the Build:** Run the provided test harness or compile a known‑good binary to confirm the environment matches the repository’s expectations.  
3. **Inspect & Refactor:** Manually review the generated C files for missing symbols or platform‑specific stubs; replace or stub out any hardware‑specific calls that are irrelevant to your target platform.  
4. **Integrate:** Link the cleaned source into your own project (e.g., a custom emulator, a modding framework, or a research prototype). Use the repository’s issue tracker and community forks for guidance on common integration hurdles.  
5. **Iterate & Contribute:** As you adapt the code, submit patches upstream to benefit future users and reduce maintenance overhead.

**Production Readiness**  
- **Maturity:** Medium. The codebase is functional enough for prototypes and internal tooling, but it lacks formal documentation, automated tests, and a clearly defined API surface.  
- **Dependencies & Maintenance:** Requires a legacy PSX development environment and occasional manual fixes; these should be evaluated for long‑term support before committing to a production pipeline.  
- **Risk Mitigation:** Conduct a small‑scale proof‑of‑concept to measure integration effort, verify licensing compliance, and confirm that the decompiled code meets performance and stability requirements for your use case. Once these checks pass, the project can move from experimental to a stable component of an internal workflow.

### Русский

Xeeynamo/sotn-decomp — открытый набор инструментов для декомпиляции оригинальных образов *Castlevania: Symphony of the Night* (PSX, PSP, Saturn) на C, который уже привлек более 900 звёзд на GitHub и регулярно обновляется (последний коммит — 2026‑07‑03). Он подходит для прототипов и внутренних пайплайнов, где требуется получить читаемый исходный код игры для анализа, моддинга или портирования, но перед внедрением необходимо вручную проверить совместимость и настроить окружение, так как метаданные дают мало информации о интеграции. Готовность к production — средняя: проект можно использовать в ограниченных сценариях после проверки зависимостей и оценки затрат на настройку.

### 中文

**简短介绍**

Xeeynamo/sotn-decomp 是一个开源项目，用于解压和反编译 Castlevania: Symphony of the Night 的 PlayStation、PlayStation Portable 和 Saturn 版本。该项目可以帮助开发者在需要时使用其 README 和活动匹配的具体工作流程。

**价值**

该项目的价值在于它可以帮助开发者在特定的工作流程中找到有用的信息和工具。它可以作为一个参考或工具，帮助开发者更好地理解和利用 Castlevania: Symphony of the Night 的游戏数据。

**典型接入方式**

由于该项目的接入信号在发现的元数据中较为稀少，因此需要手动检查和验证接入之前的设置成本。具体接入方式可能包括：

1. 读取和分析项目的 README 文件，了解其工作原理和接入方法。
2. 验证项目的活动和更新情况，以确保其仍然是可用的和有效的。
3. 手动检查和测试项目的接入方法，以确保其与自己的项目兼容。

**生产可用性**

该项目的生产可用性为中等（Medium）。

## 🧭 Practical evaluation

**Value:** Xeeynamo/sotn-decomp may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 965 GitHub stars
- 82 forks
- updated 2026-07-03
- primary language: C
- 2 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 48/100 |
| stars | 64/100 |
| topics | 25/100 |
| outlook | 50/100 |
| quality | 55/100 |
| recency | 40/100 |
| adoption | 59/100 |
| production | 51/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/Xeeynamo/sotn-decomp) · [← Back to Misc](./README.md)</sub>
