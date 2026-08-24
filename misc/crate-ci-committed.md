# crate-ci/committed

[![Stars](https://img.shields.io/github/stars/crate-ci/committed?style=flat-square&color=yellow)](https://github.com/crate-ci/committed/stargazers) [![Forks](https://img.shields.io/github/forks/crate-ci/committed?style=flat-square&color=blue)](https://github.com/crate-ci/committed/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-42%2F100-brightgreen?style=flat-square)](#)

> Nitpicking commit history since beabf39

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 171 |
| 🍴 **Forks** | 9 |
| 💻 **Language** | Rust |
| 📈 **Score** | 42/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`git`

## 🎯 Categories

Misc

## 📝 Summary

### English

crate‑ci/committed helps teams enforce and inspect commit‑history conventions by providing a lightweight Rust tool that can be integrated into CI pipelines to flag non‑conforming commits. Adoption is straightforward—clone the repo, run the binary (or add it as a Cargo dependency) in your CI step, and review its output—though you’ll need to manually verify that its rules match your workflow before relying on it. The project is production‑ready for prototypes or internal use, but because integration signals are sparse and setup requires manual inspection, you should perform dependency and maintenance checks before deploying it in a critical production environment.

### Русский

crate-ci/committed — это небольшая утилита на Rust, которая помогает «причесывать» историю коммитов, выявляя и исправляя мелкие неточности в логах репозитория. Она особенно полезна в рабочих процессах, где важна чистота и читаемость истории (например, перед релизом или при подготовке pull‑request‑ов), и её можно интегрировать в локальные скрипты или CI‑pipeline после ручной проверки настройки. Уровень готовности к production средний: подходит для прототипов и внутренних workflow‑ов, но перед использованием в продакшене рекомендуется проверить зависимости и выполнить тесты интеграции.

### 中文

**项目简介（2‑3 句）**  
`crate-ci/committed` 是一个用 Rust 编写的工具，用于细致审查 Git 提交历史（自 `beabf39` 之后），帮助开发者发现潜在的提交规范问题或不一致。它适合作为 CI 步骤的一部分，对代码库的提交质量进行自动化检查。

**价值**  
- **提升提交质量**：通过自动化的历史审查，快速捕捉遗漏的签名、错误的消息格式或不符合团队规范的提交。  
- **降低代码审查成本**：在 Pull Request 合并前提前发现问题，减轻人工审查的负担。  
- **可定制**：基于 Rust 实现，易于扩展规则或集成自定义检查逻辑。

**典型接入方式**  
1. **作为 CI 步骤**：在 GitHub Actions、GitLab CI 或自建 CI 中添加一个 job，执行 `committed` 并根据返回码决定是否通过。  
   ```yaml
   # GitHub Actions 示例
   name: Check Commit History
   on: [pull_request]

   jobs:
     committed:
       runs-on: ubuntu-latest
       steps:
         - uses: actions/checkout@v3
         - name: Install committed
           run: cargo install committed
         - name: Run committed
           run: committed --since beabf39
   ```
2. **本地 pre‑commit Hook**：在项目根目录的 `.git/hooks/pre-commit` 中调用 `committed`，阻止不符合规范的提交进入仓库。  
3. **脚本化检查**：在发布脚本或内部工具链中加入 `committed`，例如在 `cargo release` 前执行。

**生产可用性**  
- **成熟度**：已有 171 个 GitHub Stars，活跃度截至 2026‑07‑01，代码基于 Rust，具备较好的性能和安全性。  
- **适用场景**：适合原型、内部工作流以及对提交规范有明确要求的团队。  
- **风险与准备**：元数据中未提供完整的集成指引，建议在正式使用前进行一次手动验证，确认规则与团队流程匹配，并评估对 CI 时长的影响。  
- **总体评估**：在完成上述验证后，可视为 **中等成熟度**（Medium）可投入生产使用；在大规模生产环境中仍需关注依赖更新和维护成本。

## 🧭 Practical evaluation

**Value:** crate-ci/committed may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 171 GitHub stars
- 9 forks
- updated 2026-07-01
- primary language: Rust
- 1 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 25/100 |
| stars | 48/100 |
| topics | 13/100 |
| outlook | 44/100 |
| quality | 45/100 |
| recency | 40/100 |
| adoption | 41/100 |
| production | 47/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/crate-ci/committed) · [← Back to Misc](./README.md)</sub>
