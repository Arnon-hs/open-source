# facebook/sapling

[![Stars](https://img.shields.io/github/stars/facebook/sapling?style=flat-square&color=yellow)](https://github.com/facebook/sapling/stargazers) [![Forks](https://img.shields.io/github/forks/facebook/sapling?style=flat-square&color=blue)](https://github.com/facebook/sapling/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> A Scalable, User-Friendly Source Control System.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 6.9k |
| 🍴 **Forks** | 370 |
| 💻 **Language** | Rust |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-06-23 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
facebook/sapling is a fast, scalable source‑control system written in Rust that aims to replace traditional Git workflows with a more user‑friendly, high‑performance experience. With over 6 800 stars and active maintenance as of June 2026, it offers a modern alternative for teams that need to handle very large repositories or complex branching patterns. Its open‑source nature makes it attractive for internal prototypes, but the integration details are currently sparse and require careful evaluation.

**Value**  
- **Performance & scalability**: Designed for massive codebases, Sapling can dramatically reduce checkout, diff, and merge times compared to Git.  
- **User‑friendly commands**: It adds higher‑level operations (e.g., “shelf”, “unshelve”, richer history queries) that simplify everyday development tasks.  
- **Rust implementation**: Provides safety, low‑level efficiency, and a growing ecosystem of libraries for extension.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the built‑in test suite, and try basic commands on a non‑critical repository to gauge performance gains.  
2. **Integration assessment** – Map existing CI/CD pipelines, hooks, and tooling (e.g., code review, IDE plugins) to Sapling equivalents; because metadata on integrations is limited, you’ll need to manually test each touch‑point.  
3. **Pilot rollout** – Deploy Sapling to a small, isolated team or a sandbox environment, documenting any required wrappers or scripts for the missing integration points.  
4. **Full migration** – Once performance, workflow fit, and tooling gaps are resolved, plan a staged migration (e.g., export/import via `git fast-export`/`fast-import`) and update documentation for developers.

**Production Readiness**  
- **Medium**: The project is actively maintained and has a sizable community, making it suitable for internal prototypes or controlled production use.  
- **Considerations**: Verify dependency compatibility (Rust version, OS support), evaluate the cost of building missing integrations (hooks, CI plugins), and perform a risk assessment for long‑term maintenance before committing to mission‑critical deployments.

### Русский

**facebook/sapling** — это масштабируемая система контроля версий, написанная на Rust и активно поддерживаемая (6886 звёзд, последние обновления 2026‑06‑23). Она подходит для прототипов и внутренних рабочих процессов, где требуется гибкая и быстрая работа с большими репозиториями, однако перед внедрением в продакшн следует вручную оценить путь интеграции и зависимости, так как готовые инструкции ограничены. При успешной проверке проекта Sapling может стать удобным и надёжным заменителем Git в специализированных пайплайнах.

### 中文

**项目价值**  
facebook/sapling 是一套由 Facebook 开发的可扩展、易用的源码管理系统，采用 Rust 编写，天然具备高性能和安全特性。相较于传统 Git，它在大规模仓库、增量检查和分支管理等场景下拥有更低的磁盘占用和更快的操作响应，特别适合需要处理数十万文件或频繁提交的内部代码库。

**典型接入方式**  

| 步骤 | 说明 |
|------|------|
| 1️⃣ 环境准备 | - 确保服务器上已安装 Rust（`rustup`）<br>- 需要 `glibc` ≥ 2.17 的 Linux 环境（CentOS 7、Ubuntu 20.04 及以上） |
| 2️⃣ 拉取源码 | `git clone https://github.com/facebook/sapling.git && cd sapling` |
| 3️⃣ 编译安装 | `cargo build --release` → 可执行文件位于 `target/release/sapling`，复制到 `$PATH` 中的目录（如 `/usr/local/bin`） |
| 4️⃣ 初始化仓库 | `sapling init <repo_path>`（类似 `git init`）<br>或在已有 Git 仓库上运行 `sapling convert` 将其迁移为 Sapling 仓库 |
| 5️⃣ 与 CI/CD 集成 | - 在 CI 脚本中使用 `sapling checkout`、`sapling commit`、`sapling push` 替代对应的 Git 命令<br>- 通过 `sapling config` 设置远程（如 `origin`）与 Git 兼容的 HTTP/SSH 端点 |
| 6️⃣ 权限与审计 | 与现有的 LDAP/SSO 集成可通过 `sapling auth` 插件实现；审计日志可通过 `sapling log --json` 导出供安全审计使用 |

> **小技巧**：在迁移阶段，保持 Git 与 Sapling 双写（即同一仓库同时保留 `.git` 与 `.hg`/`.sl` 结构），可以逐步验证兼容性，降低迁移风险。

**生产可用性评估**  

- **成熟度**：GitHub ★ 6.9k、Fork 370，最近一次提交在 2026‑06‑23，社区活跃度尚可。项目仍在快速迭代，文档和案例相对有限。  
- **适用场景**：内部原型、实验性平台、大规模单体仓库、需要高效增量检查的 CI 环境。对外部合作伙伴或对 Git 生态高度依赖的项目，采用成本较高。  
- **风险点**  
  1. **集成路径不明确**：官方文档对常见 CI/CD、代码审查工具（如 Gerrit、GitHub Actions）的适配示例少，需要自行编写适配层。  
  2. **运维成本**：依赖 Rust 编译链和自研二进制，升级、回滚以及二进制兼容性需要自行管理。  
  3. **生态兼容**：虽然提供了 Git‑compatible 的 transport，但部分高级 Git 功能（子模块、rebase‑interactive 等）仍未完全实现。  

- **推荐使用方式**  
  - **原型/内部工具**：直接在内部 CI 服务器上部署，配合脚本层包装即可快速获益。  
  - **生产环境**：在决定正式上线前，进行 **完整的功能验证**（分支、合并、冲突解决、权限控制）以及 **性能基准测试**（大仓库的 clone、checkout、push 时延），并准备好回退到 Git 的应急方案。  

**结论**：Sapling 在处理大规模代码库时具备显著性能优势，适合作为内部原型或特定业务线的代码管理工具。但因集成文档稀缺、生态兼容度有限，建议在充分评估迁移成本和运维负担后，再决定是否在生产环境中全面采用。

## 🧭 Practical evaluation

**Value:** facebook/sapling may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 6886 GitHub stars
- 370 forks
- updated 2026-06-23
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 64/100 |
| stars | 82/100 |
| topics | 0/100 |
| outlook | 73/100 |
| quality | 75/100 |
| recency | 100/100 |
| adoption | 77/100 |
| production | 72/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/facebook/sapling) · [← Back to Misc](./README.md)</sub>
