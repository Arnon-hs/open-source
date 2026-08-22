# sazardev/goca

[![Stars](https://img.shields.io/github/stars/sazardev/goca?style=flat-square&color=yellow)](https://github.com/sazardev/goca/stargazers) [![Forks](https://img.shields.io/github/forks/sazardev/goca?style=flat-square&color=blue)](https://github.com/sazardev/goca/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Goca is a powerful CLI code generator for Go that helps you create Clean Architecture projects following best practices.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 267 |
| 🍴 **Forks** | 9 |
| 💻 **Language** | Go |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-07-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`clean-architecture` `cli` `cli-app` `code-generation` `go` `golang`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Goca is an open‑source CLI code generator that scaffolds Go projects using Clean Architecture principles, letting developers spin up well‑structured codebases with a single command. With 267 ★ on GitHub and recent activity, it streamlines daily development and review cycles while enforcing best‑practice patterns. The tool is positioned as a high‑readiness OSS candidate for teams that want to accelerate Go project bootstrapping and improve CI feedback loops.  

---

### Value  
- **Time savings** – Generates boilerplate (layers, interfaces, test skeletons, DI wiring) in seconds, cutting weeks of manual setup.  
- **Consistency** – Enforces Clean Architecture conventions across teams, reducing architectural drift and code‑review friction.  
- **Improved CI** – Projects start with a reproducible structure and ready‑made test scaffolds, leading to faster, more reliable CI pipelines.  

### Practical Adoption Path  
1. **Pilot** – Clone the repo, run `goca init` on a small internal service, and compare the generated layout with the team’s existing conventions.  
2. **Integration** – Add the `goca` binary to the developer toolbox (e.g., as a Homebrew formula or Docker image) and embed it in the project‑creation script used by the team.  
3. **Standardisation** – Document the generated project skeleton in the engineering handbook and incorporate it into the onboarding checklist for new Go services.  
4. **Automation** – Hook the CLI into CI templates or GitHub Actions to automatically scaffold new micro‑services when a repository is created.  

### Production Readiness  
- **Activity & Adoption** – Updated as of 2026‑07‑12, 267 ★, recent commits, and a modest but active fork base indicate healthy maintenance.  
- **Ecosystem Fit** – Pure Go implementation, straightforward CLI, and clear API/SDK boundaries make it easy to integrate with existing toolchains.  
- **Risk Profile** – No glaring licensing or security red flags identified; however, a final review of the license (MIT‑style) and maintainer responsiveness is recommended before a large‑scale rollout.  

Overall, Goca is production‑ready for a controlled pilot and, given its strong community signals, can be scaled to become the default scaffolding tool for Go Clean Architecture projects in a production environment.

### Русский

**Goca** — это CLI‑генератор кода для Go, который автоматически создаёт каркас проектов по Clean Architecture, позволяя инженерам экономить время на рутинных задачах и ускорять цикл разработки и ревью. Его типичный сценарий — генерация нового микросервиса или модуля, интеграция в CI для автоматической проверки структуры проекта и последующее развитие кода без необходимости вручную настраивать слои архитектуры. По оценке готовности проект считается практически готовым к production: активные коммиты, 267 звёзд, регулярные обновления и хорошая экосистема, однако требуется финальная проверка лицензии, безопасности и активности мейнтейнеров.

### 中文

**项目简介**  
Goca（sazardev/goca）是一款面向 Go 语言的强大 CLI 代码生成器，能够一键生成符合 Clean Architecture 规范的项目结构和模板，帮助团队在日常开发与代码审查中快速搭建符合最佳实践的代码库。

**价值**  
- **提升开发效率**：通过自动生成目录、接口、用例、数据层等骨架代码，显著缩短项目初始化和迭代的时间。  
- **规范统一**：内置 Clean Architecture 模板，确保新建模块始终遵循同一层次划分，降低代码审查和维护成本。  
- **加速 CI 反馈**：生成的代码结构天然兼容常见的 CI 检查（如 lint、单元测试），帮助 CI 更快给出可靠反馈。

**典型接入方式**  
1. **本地安装**：`go install github.com/sazardev/goca@latest`，随后在项目根目录运行 `goca init` 生成完整的 Clean Architecture 框架。  
2. **CI/CD 集成**：在 CI 脚本（如 GitHub Actions、GitLab CI）中加入 `goca generate` 步骤，实现代码骨架的自动更新或新功能模块的快速生成。  
3. **IDE/脚本化调用**：通过自定义脚本或 VS Code 插件调用 Goca 的 CLI 参数（如 `goca new service User`），实现“一键”生成业务模块。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑07‑12，星标 267、Fork 9，社区活跃度良好。  
- **成熟度**：项目已实现完整的 Clean Architecture 模板，具备明确的 API/CLI 接口，易于评估和集成。  
- **风险**：目前未发现重大许可证或安全隐患，但仍建议在正式投产前完成许可证合规审查并监控后续安全更新。  

综上所述，Goca 具备高可用性，适合作为内部或外部 Go 项目的代码生成工具，在提升开发效率、统一架构规范方面能够带来显著收益。

## 🧭 Practical evaluation

**Value:** sazardev/goca helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 267 GitHub stars
- 9 forks
- updated 2026-07-12
- primary language: Go
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 25/100 |
| stars | 52/100 |
| topics | 75/100 |
| outlook | 75/100 |
| quality | 71/100 |
| recency | 100/100 |
| adoption | 44/100 |
| production | 75/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/sazardev/goca) · [← Back to DevTools](./README.md)</sub>
