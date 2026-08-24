# seancorfield/deps-new

[![Stars](https://img.shields.io/github/stars/seancorfield/deps-new?style=flat-square&color=yellow)](https://github.com/seancorfield/deps-new/stargazers) [![Forks](https://img.shields.io/github/forks/seancorfield/deps-new?style=flat-square&color=blue)](https://github.com/seancorfield/deps-new/network) [![Language](https://img.shields.io/badge/lang-Clojure-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> Create new projects for the Clojure CLI / deps.edn

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 446 |
| 🍴 **Forks** | 22 |
| 💻 **Language** | Clojure |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`seancorfield/deps-new` is a lightweight Clojure‑CLI tool that scaffolds new projects based on `deps.edn`, letting developers spin up a ready‑to‑code directory with a single command. With 446 stars and recent activity (last commit 2026‑06‑27), it streamlines the initial setup phase of Clojure projects, reducing boiler‑plate and manual configuration.

**Value**  
- **Time‑saving**: Generates the full project skeleton (src, test, CI configs, README, etc.) in seconds, cutting the repetitive “copy‑paste” steps that dominate early development cycles.  
- **Consistency**: Enforces a standard project layout and dependency set across teams, which improves code review speed and reduces onboarding friction.  
- **Automation‑friendly**: The generated files can be templated for internal conventions, making it easy to embed in CI pipelines for rapid prototyping or sandbox environments.

**Practical Adoption Path**  
1. **Proof‑of‑Concept**: Run `clojure -Sdeps '{:deps {io.github.seancorfield/deps-new {:git/tag "v0.5.0" :git/sha "…"}}}' -M -m deps-new` to create a sample project and verify that the generated structure matches your organization’s expectations.  
2. **README & Template Review**: Compare the default README and `deps.edn` with internal guidelines; adjust the tool’s template files (or fork the repo) if needed.  
3. **Pilot Integration**: Add a small wrapper script (e.g., `bin/new-clj`) to your internal tooling suite and expose it to a single development team. Collect feedback on missing dependencies or preferred conventions.  
4. **Roll‑out**: Once the pilot is stable, publish the wrapper in your internal artifact registry or as a pre‑commit hook, and document the usage in the team’s onboarding guide.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last update 2026‑06‑27) and has a healthy star count, indicating community interest, but it lacks a formal release process and extensive test coverage.  
- **Suitability**: Ideal for prototypes, internal tooling, and as a bootstrap for new services. For production‑critical pipelines, perform a dependency audit (check transitive libs for known CVEs) and consider pinning a specific tag or SHA to avoid accidental upstream changes.  
- **Risks**: No major metadata or licensing concerns identified, but confirm the SPDX license (likely EPL‑1.0) aligns with your organization’s policy, and verify that the maintainers are responsive to security issues before committing to long‑term use.  

Overall, `deps-new` offers a high‑impact productivity boost with modest integration effort; a small, controlled rollout followed by a security/dependency review will bring it to a production‑ready state.

### Русский

Резюме проекта seancorfield/deps-new:

seancorfield/deps-new - это открытый исходный проект, который помогает инженерам экономить время в повседневной разработке и отладке. Этот проект может ускорить рабочие процессы разработчиков, автоматизировать локальные задачи инженеров и улучшить обратную связь в CI. seancorfield/deps-new готов к внедрению в прототипах или внутренних процессах, но требует проверки зависимостей и обслуживания перед использованием в production.

### 中文

**简短介绍**

seancorfield/deps-new 是一个用于创建新的 Clojure CLI / deps.edn 项目的开源工具。它可以帮助开发者节省每天的开发和审查时间，提高工作效率和 CI 反馈。

**价值**

seancorfield/deps-new 的价值在于：

* 加快开发者工作流程
* 自动化本地工程任务
* 提高 CI 反馈

**典型接入方式**

典型接入方式包括：

* 在项目中添加 deps-new 的依赖
* 使用 deps-new 创建新项目
* 自定义 deps-new 的配置和行为

**生产可用性**

seancorfield/deps-new 的生产可用性为中等（Medium）。它适合用于原型或内部工作流程，但在生产环境中需要进行依赖和维护检查。

## 🧭 Practical evaluation

**Value:** seancorfield/deps-new helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 446 GitHub stars
- 22 forks
- updated 2026-06-27
- primary language: Clojure

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 56/100 |
| topics | 0/100 |
| outlook | 48/100 |
| quality | 48/100 |
| recency | 40/100 |
| adoption | 50/100 |
| production | 50/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/seancorfield/deps-new) · [← Back to Misc](./README.md)</sub>
