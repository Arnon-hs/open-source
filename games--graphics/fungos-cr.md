# fungos/cr

[![Stars](https://img.shields.io/github/stars/fungos/cr?style=flat-square&color=yellow)](https://github.com/fungos/cr/stargazers) [![Forks](https://img.shields.io/github/forks/fungos/cr?style=flat-square&color=blue)](https://github.com/fungos/cr/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> cr.h: A Simple C Hot Reload Header-only Library

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.8k |
| 🍴 **Forks** | 119 |
| 💻 **Language** | C++ |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`c` `gamedev` `gamedev-tool` `header-only` `header-only-lib` `header-only-library` `hot-reload` `linux` `live-coding` `osx` `single-header` `single-header-lib`

## 🎯 Categories

Games & Graphics

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`fungos/cr` is a header‑only C library that provides simple hot‑reloading capabilities, letting developers rebuild and reload code at runtime with minimal boilerplate. With over 1.7 k GitHub stars, recent commits, and a clear README, it is a mature, community‑backed option for projects that need rapid iteration without restarting the whole application.

**Value**  
- **Rapid development cycles:** By hot‑reloading compiled objects, developers can see code changes instantly, cutting down test‑and‑debug time.  
- **Zero‑dependency integration:** Being a single header, it adds virtually no build complexity or external runtime requirements.  
- **Broad applicability:** Works with any C/C++ codebase that can be modularized, making it suitable for games, embedded firmware, or scientific tools that benefit from live updates.

**Practical Adoption Path**  
1. **Proof‑of‑concept:** Add `cr.h` to a small, non‑critical module (e.g., a plugin or a demo app) and verify that changes compile and reload as expected.  
2. **Readme verification:** Follow the usage steps in the repository’s README to ensure the build flags and runtime hooks align with your build system (Make, CMake, etc.).  
3. **Gradual rollout:** Once the PoC succeeds, replace static linking for additional modules, monitoring for any symbol‑collision or state‑preservation issues.  
4. **Automated testing:** Integrate hot‑reload checks into CI to catch regressions early.

**Production Readiness**  
The project scores high on production readiness: it shows recent activity (last commit 2026‑06‑23), strong community adoption (1,777 stars, 119 forks), and a clear C++ primary language. While no major metadata risks appear, a final review of the license (MIT‑style) and a quick security audit of the header are advisable. Assuming those checks pass, `fungos/cr` is ready for a serious pilot in production environments, especially where fast iteration outweighs the modest overhead of hot‑reloading.

### Русский

**fungos/cr** — это небольшая header‑only библиотека на C, реализующая «горячую» перезагрузку кода без перезапуска процесса. Она подходит для проектов, где требуется быстро вносить изменения в бизнес‑логику (например, игровые движки, серверные плагины или микросервисы) и проверять их в реальном времени, интегрируя её через один заголовочный файл и небольшую проверочную пробу. По оценкам, библиотека готова к production‑использованию: активные коммиты, более 1700 звёзд, значительное количество форков и положительные сигналы экосистемы, хотя перед масштабным внедрением стоит уточнить лицензионные и безопасность‑аспекты.

### 中文

**项目简介**  
`fungos/cr` 是一个仅包含单个头文件 `cr.h` 的 C 语言热重载库，旨在让开发者在不重启进程的情况下即时加载更新的代码或资源，极大提升调试和迭代效率。

**价值体现**  
- **极简依赖**：只需把 `cr.h` 加入项目，无需额外编译或链接步骤，几行宏调用即可开启热重载。  
- **即时反馈**：在开发阶段修改函数实现或数据文件后，库会自动检测并重新加载，避免频繁重启进程，缩短开发周期。  
- **跨平台**：实现基于标准 C/C++，在 Linux、macOS 与 Windows 上均可工作，适配大多数 C 项目。

**典型接入方式**  
1. **引入头文件**：`#include "cr.h"` 并在需要热重载的源码文件中加入 `CR_INIT();` 初始化宏。  
2. **标记可热重载代码**：使用 `CR_EXPORT`（或相应宏）导出需要在运行时重新加载的函数。  
3. **编译为共享库**：将标记的实现编译为动态库（`.so/.dll/.dylib`），并在主程序启动时通过 `cr_load("myplugin.so")` 加载。  
4. **自动监控**：库内部会监控文件系统变化，文件被修改后自动调用 `dlclose`/`LoadLibrary` 重新加载，随后继续执行新代码。  

> **小型验证**：在一个独立的 demo 项目中创建一个简单的插件库并使用上述宏进行加载，确认热重载生效后，再把相同的模式迁移到实际业务模块。

**生产可用性评估**  
- **活跃度**：最近一次提交在 2026‑06‑23，拥有 1777 星、119 Fork，社区活跃度较高。  
- **成熟度**：库本身只有单文件实现，代码量小、审计成本低，且已在多个开源项目中被引用，具备一定的实战验证。  
- **风险**：需进一步确认许可证兼容性（MIT/Apache 等）以及对动态库加载的安全审计；若项目对安全要求极高，建议在正式环境前进行渗透测试。  
- **结论**：在经过一次小规模的概念验证（POC）并完成许可证与安全审查后，可视为 **生产级候选**，适合在内部工具、游戏引擎、嵌入式系统等需要快速迭代的 C 项目中推广使用。

## 🧭 Practical evaluation

**Value:** fungos/cr may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1777 GitHub stars
- 119 forks
- updated 2026-06-23
- primary language: C++
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 52/100 |
| stars | 69/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 79/100 |
| recency | 80/100 |
| adoption | 64/100 |
| production | 71/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/fungos/cr) · [← Back to Games--graphics](./README.md)</sub>
