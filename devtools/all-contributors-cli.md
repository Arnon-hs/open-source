# all-contributors/cli

[![Stars](https://img.shields.io/github/stars/all-contributors/cli?style=flat-square&color=yellow)](https://github.com/all-contributors/cli/stargazers) [![Forks](https://img.shields.io/github/forks/all-contributors/cli?style=flat-square&color=blue)](https://github.com/all-contributors/cli/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> Tool to help automate adding contributor acknowledgements according to the all-contributors specification  ✨

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 426 |
| 🍴 **Forks** | 148 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`acknowledgements` `all-contributors` `command-line-tool` `contributors` `open-source-tooling` `opensource` `opensource-management` `recognition`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The **all‑contributors/cli** is a JavaScript‑based command‑line tool that automates the addition of contributor acknowledgements in a repository, fully complying with the All‑Contributors specification. By handling the boilerplate updates to README, `package.json`, and related files, it lets engineers record contributions with a single command, keeping the contributor list accurate and up‑to‑date. Its active community (426 ★, 148 forks) and recent maintenance make it a reliable addition to any open‑source or internal project.

**Value**  
- **Time savings** – eliminates manual edits to contributor tables, reducing friction in daily development and code‑review cycles.  
- **Consistency** – enforces the All‑Contributors spec across all repos, ensuring a uniform acknowledgment format.  
- **CI integration** – can be run in CI pipelines to automatically update contributor data after merges, providing immediate feedback to contributors.

**Practical Adoption Path**  
1. **Install** the CLI (`npm i -g all-contributors-cli` or add as a devDependency).  
2. **Initialize** a repo with `all-contributors init` to generate the configuration file.  
3. **Add contributors** via `all-contributors add <type> <username>` as part of the pull‑request workflow or a CI step.  
4. **Commit** the generated changes; optionally gate the step with a CI job that fails if the contributor list is out‑of‑sync.  
5. **Scale** across multiple repositories by scripting the CLI in a monorepo or using a shared GitHub Action.

**Production Readiness**  
The project shows high production readiness: it is actively maintained (last update 2026‑07‑01), has strong adoption signals (over 400 stars, many forks), and is written in a widely‑used language (JavaScript). The CLI is stable, well‑documented, and already used in numerous open‑source projects, indicating low risk for integration. Remaining due‑diligence should focus on confirming the license compatibility, reviewing any disclosed security advisories, and verifying that maintainers are responsive, but overall the tool is ready for pilot deployments in production environments.

### Русский

**all-contributors/cli** — это JavaScript‑инструмент, который автоматизирует добавление благодарностей участникам проекта в соответствии со спецификацией All‑Contributors, экономя время разработчиков на ручных правках и ускоряя цикл ревью. Его типичный сценарий — интеграция в локальный workflow (pre‑commit, npm‑scripts) или CI/CD, где CLI автоматически обновляет файлы `README`/`CONTRIBUTORS` после каждого мерджа. Проект считается готовым к production‑использованию: активные коммиты, 426 звёзд, 148 форков, поддержка JavaScript‑экосистемы и отсутствие серьёзных рисков, требующих лишь финальной проверки лицензии и безопасности.

### 中文

**简短介绍**

all-contributors/cli 是一个开源工具，帮助工程师根据 all-contributors 规范自动添加贡献者致谢。它可以节省开发者的时间，使日常开发和审查流程更高效。

**价值**

all-contributors/cli 帮助工程师在日常开发和审查流程中节省时间，提高开发效率。它可以用于加速开发者工作流、自动化本地工程任务和改善 CI 反馈。

**典型接入方式**

all-contributors/cli 可以通过以下方式接入：

* 直接使用 CLI 命令
* 集成到 CI/CD 流程中
* 使用 API 或 SDK 来自动化贡献者致谢

**生产可用性**

all-contributors/cli 的生产可用性很高，因为它有以下优点：

* 有强大的社区支持（426 GitHub 星，148 forks）
* 有活跃的维护者
* 有强大的生态系统信号
* 有高质量的代码（JavaScript）

但是，仍然需要对其许可、安全性和维护者进行最终的审查。

## 🧭 Practical evaluation

**Value:** all-contributors/cli helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 426 GitHub stars
- 148 forks
- updated 2026-07-01
- primary language: JavaScript
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 54/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 63/100 |
| quality | 65/100 |
| recency | 40/100 |
| adoption | 56/100 |
| production | 57/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/all-contributors/cli) · [← Back to DevTools](./README.md)</sub>
