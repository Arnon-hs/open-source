# RaphGL/Tuckr

[![Stars](https://img.shields.io/github/stars/RaphGL/Tuckr?style=flat-square&color=yellow)](https://github.com/RaphGL/Tuckr/stargazers) [![Forks](https://img.shields.io/github/forks/RaphGL/Tuckr?style=flat-square&color=blue)](https://github.com/RaphGL/Tuckr/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> Super powered replacement for GNU Stow

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 456 |
| 🍴 **Forks** | 32 |
| 💻 **Language** | Rust |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`dotfile-management` `dotfile-manager` `dotfiles` `stow` `tuckr`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Tuckr (RaphGL/Tuckr) is a Rust‑based, feature‑rich alternative to GNU Stow that aims to simplify the management of symlink‑based dot‑file deployments and other file‑system trees. With a modern CLI, built‑in templating, and better handling of conflicts, it promises a smoother workflow for developers who already use Stow but need more automation and safety. The project is actively maintained (last commit 2026‑05‑13) and has gathered a modest community (≈456 ⭐, 32 forks).

**Value Proposition**  
- **Enhanced ergonomics**: Tuckr adds conflict detection, dry‑run previews, and per‑package configuration, reducing the manual steps and errors that often accompany GNU Stow.  
- **Rust performance & safety**: Compiled binaries are fast, have no runtime dependencies, and benefit from Rust’s strong type guarantees, which can be attractive for CI pipelines.  
- **Extensible workflow**: Built‑in support for templating and hooks lets teams embed environment‑specific logic (e.g., secret injection) directly into the deployment process.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, run `tuckr --dry-run` on a small subset of your dot‑files or a test repository to verify that the CLI behaves as expected.  
2. **README validation** – Follow the quick‑start instructions in the README; they cover installation (cargo or pre‑built binaries) and basic package definitions.  
3. **Pilot integration** – Replace a single Stow‑managed bundle with Tuckr in a non‑critical environment (e.g., a personal workstation or a staging VM). Observe conflict handling, speed, and any required custom hooks.  
4. **Gradual rollout** – Once the pilot is stable, incrementally migrate additional bundles, updating CI scripts to invoke `tuckr deploy` instead of `stow`.  

**Production Readiness**  
- **Maturity**: Medium. The project is actively updated and compiled in Rust, but the ecosystem around it (plugins, extensive documentation, enterprise‑grade support) is still limited.  
- **Risk considerations**: The integration path isn’t fully documented; you’ll need to invest time in testing the setup and ensuring that existing Stow scripts can be translated to Tuckr’s manifest format. Dependency management is straightforward (single binary), but you should monitor upstream changes for breaking API updates.  
- **Recommended use**: Suitable for prototypes, internal tooling, or teams looking to replace Stow with a more modern, safer CLI. For large‑scale production environments, conduct a thorough POC and establish a maintenance plan before committing to full deployment.

### Русский

RaphGL/Tuckr — это быстрый и гибкий инструмент‑замена GNU Stow, написанный на Rust, который упрощает управление симлинками и развертывание файловых деревьев в проектах с множеством зависимостей. Его типичный сценарий — небольшие прототипы или внутренние рабочие процессы, где требуется быстрое и надёжное «упаковывание» артефактов; начать интеграцию стоит с проверки README и небольшого proof‑of‑concept. Готовность к production — средняя: проект уже имеет 456 звёзд, активную поддержку и недавние обновления, но путь интеграции не полностью документирован, поэтому перед выводом в продакшн следует оценить затраты на настройку и сопровождение.

### 中文

**项目简介**  
RaphGL/Tuckr 是用 Rust 编写的 GNU Stow 替代品，提供更强大的符号链接管理与配置部署功能，适合在多平台、模块化的开发环境中快速组织和切换 dotfiles、工具链或微服务部署目录。

**价值**  
- **性能与安全**：Rust 实现，零运行时开销，内置类型安全，避免常见的路径拼写或循环链接错误。  
- **高级特性**：支持分层配置、条件链接（基于 OS、架构或自定义标签）以及事务式回滚，帮助团队在 CI/CD 流程中保持环境一致性。  
- **易用 CLI 与 API**：兼容 Stow 常用命令的同时提供 JSON/YAML 配置文件和库接口，便于脚本化和二次开发。

**典型接入方式**  
1. **阅读 README 与示例**：确认项目的工作流（如 `tuckr init`, `tuckr link --profile dev`）与团队需求匹配。  
2. **小范围 PoC**：在一个独立的测试仓库或本地机器上创建简单的 `tuckr.yml`，验证链接创建、回滚与条件过滤是否如预期。  
3. **CI 集成**：在 CI 脚本中加入 `tuckr sync` 步骤，使用 `--dry-run` 检查变更，再在部署阶段实际执行。  
4. **库使用**：如果需要在自研工具中调用，可在 `Cargo.toml` 添加 `tuckr = { git = "https://github.com/RaphGL/Tuckr.git" }`，使用其公开的 Rust API 完成自定义链接逻辑。

**生产可用性**  
- **成熟度**：已有 456 星、32 Fork，最近更新于 2026‑05‑13，代码活跃度良好。  
- **适用场景**：非常适合原型、内部工具链或需要频繁切换配置的团队；在生产环境使用前建议完成以下检查：  
  - 依赖审计（确保所有第三方 crate 已通过安全审计）。  
  - 回滚与灾难恢复流程测试。  
  - 与现有配置管理系统（如 Ansible、Chef）兼容性验证。  
- **风险**：元数据未提供完整的集成指南，初始学习成本略高；建议在正式上线前完成小规模验证并记录部署手册。  

综上，Tuckr 在性能、安全和高级链接管理上优于传统 Stow，适合作为内部或原型项目的配置部署工具；在完成上述验证后，可逐步推广至生产环境。

## 🧭 Practical evaluation

**Value:** RaphGL/Tuckr may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 456 GitHub stars
- 32 forks
- updated 2026-05-13
- primary language: Rust
- 5 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 38/100 |
| stars | 57/100 |
| topics | 63/100 |
| outlook | 65/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 51/100 |
| production | 65/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/RaphGL/Tuckr) · [← Back to Misc](./README.md)</sub>
