# blue-build/cli

[![Stars](https://img.shields.io/github/stars/blue-build/cli?style=flat-square&color=yellow)](https://github.com/blue-build/cli/stargazers) [![Forks](https://img.shields.io/github/forks/blue-build/cli?style=flat-square&color=blue)](https://github.com/blue-build/cli/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> BlueBuild's command line program that builds custom Fedora Atomic images based on your recipe.yml

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 172 |
| 🍴 **Forks** | 30 |
| 💻 **Language** | Rust |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-07-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `cli-tool` `fedora` `fedora-silverblue`

## 🎯 Categories

AI/ML · Frontend · DevTools

## 📝 Summary

### English

**BlueBuild CLI Project Summary**

BlueBuild's command line program is an open-source project that enables users to build custom Fedora Atomic images based on a recipe.yml file. This tool helps developers add AI capabilities without starting from scratch, making it ideal for prototyping AI features, building RAG or agent workflows, and evaluating model tooling. With its straightforward integration and medium production readiness, it's suitable for internal workflows or proof-of-concepts.

**Value Proposition**

The value proposition of BlueBuild CLI lies in its ability to simplify the process of adding AI capabilities to existing projects. By providing a pre-built command line program, developers can focus on the AI aspects without worrying about the underlying infrastructure. This makes it an attractive option for developers who want to quickly prototype AI features or build proof-of-concepts.

**Practical Adoption Path**

The practical adoption path for BlueBuild CLI involves the following steps:

1. **Evaluation**: Developers evaluate the project's integration signals, such as API/SDK/CLI, language metadata, and focused topics.
2. **Setup**: Users set up the project by following the installation instructions and configuring the recipe.yml file.
3. **Testing**: Developers test the project by building custom Fedora Atomic images and verifying the results.
4. **Integration**: Once the project is verified

### Русский

**blue-build/cli** — это CLI‑утилита на Rust, позволяющая быстро собирать кастомные Fedora Atomic‑образы из вашего `recipe.yml`, что упрощает создание и прототипирование AI‑решений (RAG, агентных workflow) без необходимости разворачивать полностью собственный стек. Типичный сценарий — разработчики используют её в локальных и CI‑пайплайнах для генерации образов с предустановленными AI‑инструментами, после чего образ разворачивается в тестовой или внутренней инфраструктуре. Готовность к production — средняя: проект стабилен и активно поддерживается (172★, последние коммиты — 2026‑07‑05), но перед запуском в продакшн рекомендуется проверить лицензирование, безопасность зависимостей и наличие постоянных мейнтейнеров.

### 中文

**项目简介**  
BlueBuild 的 `cli` 是一款用 Rust 编写的命令行工具，能够根据项目根目录下的 `recipe.yml` 自动构建自定义的 Fedora Atomic 镜像。它简化了镜像定制流程，让开发者只需编写配方文件即可完成从源码到可部署镜像的全链路构建。

**价值**  
- **快速原型**：无需手动编写 Dockerfile 或 Kickstart，几行配置即可生成符合需求的 Fedora Atomic 镜像，极大提升 CI/CD 与内部测试的效率。  
- **统一规范**：通过统一的 `recipe.yml` 定义镜像内容，团队可以共享、复用并审计镜像构建过程，降低环境漂移风险。  
- **可扩展**：基于 Rust 实现，性能高、二进制体积小，易于在各种 Linux 环境中部署，且可与现有的 DevOps 工具链（GitHub Actions、GitLab CI、Jenkins 等）无缝集成。

**典型接入方式**  
1. **本地使用**：`cargo install blue-build-cli` 或下载预编译二进制，项目根目录放置 `recipe.yml`，执行 `blue-build build` 即可生成镜像。  
2. **CI/CD 集成**：在流水线脚本中加入 `blue-build` 步骤，例如  
   ```yaml
   - name: Build Fedora Atomic image
     run: |
       curl -L https://github.com/blue-build/cli/releases/download/vX.Y.Z/blue-build-linux-x86_64.tar.gz | tar xz
       ./blue-build build --recipe recipe.yml
   ```  
   生成的镜像可直接推送至容器注册表或用于后续的部署测试。  
3. **API/SDK 方式**：`blue-build` 同时提供了 Rust 库 (`blue-build-core`)，开发者可在自定义工具中调用其内部构建函数，实现更细粒度的自动化。

**生产可用性**  
- **成熟度**：GitHub ★172、Fork 30，最近一次更新在 2026‑07‑05，活跃度尚可。  
- **适用场景**：非常适合内部原型、CI 环境或对镜像一致性要求较高的中小规模生产系统。  
- **风险与准备**：需进一步审查许可证（MIT/Apache）、依赖安全（Rust crates）以及维护者响应速度后方可在高风险生产环境中使用。整体上属于 **中等** 生产就绪度，建议在正式上线前进行安全扫描和回滚演练。

## 🧭 Practical evaluation

**Value:** blue-build/cli helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 172 GitHub stars
- 30 forks
- updated 2026-07-05
- primary language: Rust
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 37/100 |
| stars | 48/100 |
| topics | 50/100 |
| outlook | 76/100 |
| quality | 68/100 |
| recency | 100/100 |
| adoption | 45/100 |
| production | 72/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/blue-build/cli) · [← Back to AI/ML](./README.md)</sub>
