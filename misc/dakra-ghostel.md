# dakra/ghostel

[![Stars](https://img.shields.io/github/stars/dakra/ghostel?style=flat-square&color=yellow)](https://github.com/dakra/ghostel/stargazers) [![Forks](https://img.shields.io/github/forks/dakra/ghostel?style=flat-square&color=blue)](https://github.com/dakra/ghostel/network) [![Language](https://img.shields.io/badge/lang-Emacs%20Lisp-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> Terminal emulator powered by libghostty

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 589 |
| 🍴 **Forks** | 41 |
| 💻 **Language** | Emacs Lisp |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`dakra/ghostel` is a terminal emulator built on top of the **libghostty** library and written in Emacs Lisp. It offers a lightweight, scriptable terminal experience that can be embedded in Emacs‑centric workflows, and it currently shows modest community interest (≈ 589 ★, 41 forks). The project is actively maintained (last commit 2026‑07‑02) but its integration documentation is sparse, so a quick trial is advisable before committing to it for production use.  

**Value**  
- **Emacs‑first workflow** – because it is implemented in Emacs Lisp, Ghostel can be configured and extended from within Emacs, letting power users keep their terminal and editor tightly coupled.  
- **Libghostty backend** – leverages a modern, high‑performance rendering engine, giving a smoother UI and better Unicode/graphics support than many classic terminal emulators.  
- **Open‑source and extensible** – the codebase is openly available, allowing custom patches or feature additions without waiting on a vendor roadmap.  

**Practical Adoption Path**  
1. **Clone & build** – `git clone https://github.com/dakra/ghostel.git` and follow the minimal build steps in the README (install libghostty, then evaluate the Emacs Lisp files).  
2. **Prototype** – launch Ghostel from an Emacs session (`M-x ghostel`) and test the required workflows (e.g., REPL integration, SSH sessions, custom keybindings).  
3. **Validate dependencies** – ensure libghostty and any OS‑specific libraries are available on target machines; document any extra packages.  
4. **Create a thin wrapper** – if the team uses a different init system (e.g., Doom Emacs, Spacemacs), write a small wrapper module that loads Ghostel on demand.  
5. **Run a pilot** – roll out to a small developer group, collect feedback on performance, UI quirks, and integration effort.  

**Production‑Readiness Assessment**  
- **Maturity**: Medium. The project is actively maintained and has a respectable star count, but the lack of detailed integration guides and limited real‑world case studies mean it is best suited for prototypes or internal tooling.  
- **Risk**: Moderate. Integration pathways are not clearly documented; teams must allocate time to verify that libghostty builds cleanly on all target platforms and that the Emacs Lisp code aligns with their configuration management.  
- **Recommendation**: Use Ghostel for internal or experimental workflows after a short pilot; for mission‑critical production environments, perform a thorough dependency audit and consider fallback to a more mature terminal emulator unless Ghostel’s Emacs‑centric advantages outweigh the integration overhead.

### Русский

**dakra/ghostel** — это терминальный эмулятор, построенный на библиотеке libghostty и написанный на Emacs Lisp. Он подходит для прототипов и внутренних рабочих процессов, где требуется лёгкая интеграция в Emacs‑ориентированную среду, но перед внедрением стоит проверить совместимость зависимостей и оценить затраты на настройку, так как детали интеграции из метаданных скудны. Уровень готовности — средний: проект активно поддерживается (обновления 2026‑07‑02, 589 звёзд), однако для production‑использования рекомендуется провести ручную проверку и обеспечить надёжное обслуживание.

### 中文

**简短介绍**

dakra/ghostel 是一个基于 libghostty 的终端模拟器。它可以在特定的工作流程中发挥作用，但其 README 和活动信息需要与具体的工作流程匹配。

**价值**

dakra/ghostel 的价值在于，它可以在特定的工作流程中提供帮助。但是，需要注意的是，其 README 和活动信息需要与具体的工作流程匹配。

**典型接入方式**

由于对接信号在元数据中较为稀疏，因此需要手动检查和验证接入方式。具体的接入方式需要根据项目的具体需求和工作流程来定制。

**生产可用性**

dakra/ghostel 的生产可用性为中等。它适合用于原型或内部工作流程，但需要进行依赖检查和维护检查后才能用于生产环境。

## 🧭 Practical evaluation

**Value:** dakra/ghostel may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 589 GitHub stars
- 41 forks
- updated 2026-07-02
- primary language: Emacs Lisp

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 41/100 |
| stars | 59/100 |
| topics | 0/100 |
| outlook | 60/100 |
| quality | 59/100 |
| recency | 80/100 |
| adoption | 54/100 |
| production | 62/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/dakra/ghostel) · [← Back to Misc](./README.md)</sub>
