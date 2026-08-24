# Canop/broot

[![Stars](https://img.shields.io/github/stars/Canop/broot?style=flat-square&color=yellow)](https://github.com/Canop/broot/stargazers) [![Forks](https://img.shields.io/github/forks/Canop/broot?style=flat-square&color=blue)](https://github.com/Canop/broot/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> A new way to see and navigate directory trees : https://dystroy.org/broot

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 12.7k |
| 🍴 **Forks** | 292 |
| 💻 **Language** | Rust |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`balanced-bfs-descent` `command-line` `command-line-tool` `fuzzy-search` `hacktoberfest` `linux` `rust` `tree`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
Canop /broot is a Rust‑based terminal tool that lets you explore and manipulate directory trees with a visual, interactive view (see https://dystroy.org/broot). With over 12 000 GitHub stars, recent commits, and a growing user community, it is a mature open‑source candidate for projects that need faster, more ergonomic file‑system navigation.  

**Value**  
broot replaces the classic `ls`/`cd` workflow with a pane that shows the whole tree, supports fuzzy filtering, bulk rename, git‑aware highlights and custom commands, dramatically reducing the time spent typing paths and hunting files. This can boost developer productivity, simplify scripts that need to locate files, and improve onboarding for new team members who must understand a large codebase layout.  

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run `cargo install broot` (or use the pre‑built binaries) and try the basic navigation on a sample project.  
2. **README validation** – Verify that the documented installation steps, key bindings, and configuration options (e.g., `~/.config/broot/conf.toml`) cover your environment (Linux/macOS, CI containers, etc.).  
3. **Integration pilot** – Wrap `broot` in a small wrapper script or alias (e.g., `alias br='broot'`) and replace a few manual `cd`/`ls` usages in a low‑risk component. Capture feedback on speed and usability.  
4. **Scale up** – If the pilot succeeds, roll the alias out to the whole team, add custom commands (e.g., open in IDE, run tests) via broot’s `commands` feature, and optionally embed it in CI pipelines for automated tree inspections.  

**Production readiness**  
The project scores high on production readiness: it has recent activity (last commit 2026‑05‑13), a large star count, active forks, and a well‑maintained Rust codebase. Its ecosystem signals (documentation, issue triage, community contributions) indicate a stable, battle‑tested tool suitable for a serious pilot. The main risk is the integration effort—broot’s configuration files and custom command hooks must be aligned with your existing tooling—so a modest initial proof‑of‑concept is recommended before full adoption.

### Русский

Canop/broot — интерактивный файловый менеджер, позволяющий быстро просматривать и перемещаться по древовидной структуре каталогов через терминал, что повышает эффективность навигации в больших проектах. Для внедрения достаточно выполнить небольшой proof‑of‑concept: установить пакет, протестировать базовые команды и сверить README с вашими рабочими процессами. Проект имеет высокую готовность к production‑использованию: активные обновления, более 12 000 звёзд на GitHub, широкое принятие в сообществе Rust и подтверждённая стабильность.

### 中文

**项目简介**  
Canop/broot（broot）是一款用 Rust 编写的交互式文件树浏览器，提供 “树形视图 + 关键字过滤 + 直接在树中执行命令” 的全新目录浏览体验。它的核心优势在于能够在一次交互中完成目录定位、文件筛选和批量操作，大幅提升终端下的文件管理效率。

---

### 价值点

1. **快速定位 & 过滤**：输入任意子串即可即时过滤树节点，省去层层 `cd`/`ls` 的过程。  
2. **统一操作入口**：在树中直接打开、编辑、删除、复制、移动等，支持自定义快捷键和外部命令，形成“一站式”工作流。  
3. **轻量且可脚本化**：二进制文件小（≈2 MB），可通过 `broot --install` 自动生成 shell 补全和别名，易于在 CI、容器或开发环境中部署。  
4. **活跃社区 & 可靠实现**：截至 2026‑05‑13 拥有 12 664 ⭐、292 fork，最近一次提交就在当日，使用 Rust 提供的安全性和性能保证。

---

### 典型接入方式

| 场景 | 步骤 | 说明 |
|------|------|------|
| **本地开发环境** | 1. `cargo install broot` 或下载预编译二进制 <br>2. 执行 `broot --install` 生成 `br` 别名 & Bash/Zsh/Fish 自动补全 <br>3. 在 `.bashrc`/`.zshrc` 中加入 `export BROOT_LOG=error`（可选） | 完全零配置，即可在终端使用 `br` 替代 `cd`/`ls` |
| **CI / Docker 镜像** | 1. 在 Dockerfile 中加入 `RUN cargo install broot && broot --install` <br>2. 通过 `ENTRYPOINT ["broot", "--"]` 或在脚本中调用 `broot -c <cmd>` | 只增加几 MB 的镜像体积，适合需要目录检查或文件批处理的 CI 步骤 |
| **自定义工作流** | 1. 在 `~/.config/broot/conf.toml` 中定义 `commands`，例如 `open = "code {path}"` <br>2. 在项目根目录执行 `br`，使用 `o` 快捷键直接在 VS Code 中打开文件 | 通过配置文件实现业务专属快捷操作，降低上下文切换成本 |
| **与其他工具链集成** | 通过 `broot --cmd <shell‑cmd>` 将过滤结果直接传给 `xargs`、`git`、`fd` 等，例如 `br -c 'git add {}'` | 使 broot 成为文件选择器，配合现有脚本实现“选‑即‑执行”。 |

> **关键点**：接入成本主要在于把 `broot --install` 加入用户的 shell 初始化脚本，后续即可通过别名 `br` 替代 `cd`/`ls`，不需要额外的服务或守护进程。

---

### 生产可用性评估

| 维度 | 评估 | 说明 |
|------|------|------|
| **代码成熟度** | ★★★★★ | 采用 Rust 编写，内存安全，单元测试覆盖率高；最近一次提交为 2026‑05‑13，活跃维护。 |
| **社区与生态** | ★★★★☆ | 12 k+ ⭐、300+ forks，官方文档完整，GitHub Issues 响应及时；已有多篇博客和视频教程。 |
| **部署成本** | ★★★★☆ | 只需二进制或 `cargo install`，无外部依赖；在容器或 CI 中可自动化安装。 |
| **可扩展性** | ★★★★☆ | 通过 `conf.toml` 支持自定义命令、主题、过滤规则，能够适配不同团队的工作流。 |
| **风险** | ★★★☆☆ | 主要风险在于需要用户习惯新的交互方式；在极端大目录（>10 万文件）下首次加载会稍慢，建议配合 `.gitignore` 或 `--filter` 预过滤。 |

**结论**：broot 已具备 **高生产可用性**，适合作为开发团队的默认目录浏览工具或在 CI 中做文件筛选/批处理的“前置”。建议先在小范围（如个人机器或单个 CI job）进行 PoC，验证自定义快捷键和脚本集成后，再推广至全团队。

## 🧭 Practical evaluation

**Value:** Canop/broot may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 12664 GitHub stars
- 292 forks
- updated 2026-05-13
- primary language: Rust
- 8 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 62/100 |
| stars | 87/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 71/100 |
| recency | 20/100 |
| adoption | 80/100 |
| production | 52/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/Canop/broot) · [← Back to Misc](./README.md)</sub>
