# Byron/dua-cli

[![Stars](https://img.shields.io/github/stars/Byron/dua-cli?style=flat-square&color=yellow)](https://github.com/Byron/dua-cli/stargazers) [![Forks](https://img.shields.io/github/forks/Byron/dua-cli?style=flat-square&color=blue)](https://github.com/Byron/dua-cli/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> View disk space usage and delete unwanted data, fast.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 6k |
| 🍴 **Forks** | 155 |
| 💻 **Language** | Rust |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cleaner` `disk` `efficient` `fast` `space-use` `terminal-based`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
Byron/dua‑cli is a fast, Rust‑based command‑line tool that visualises disk‑space usage and lets developers delete unwanted files in an interactive, colour‑coded UI. With over 5,900 ⭐️ and recent commits, it’s a mature OSS candidate that can be dropped into any workstation or CI environment to keep storage clean and feedback loops short.

**Value**  
- **Time savings** – instantly spot large or duplicate files and purge them without leaving the terminal, cutting the manual “du / | sort -h” cycle.  
- **Workflow acceleration** – can be scripted in pre‑commit hooks, CI jobs, or local dev scripts to enforce size limits or clean caches automatically.  
- **Developer experience** – the interactive UI and rich output (JSON, CSV, tree view) make it easy for engineers of any skill level to understand storage consumption.

**Practical Adoption Path**  
1. **Evaluation** – install via Cargo (`cargo install dua-cli`) or download a pre‑built binary; run `dua i` on a sample project to gauge speed and UI fit.  
2. **Pilot** – add a simple wrapper script (e.g., `dua i ./target && dua purge ./target`) to local dev environments or CI pipelines; monitor the reduction in build‑artifact size.  
3. **Automation** – integrate the CLI into existing tooling (pre‑commit, GitHub Actions, Jenkins) using its JSON output for custom alerts or gating builds that exceed a threshold.  
4. **Scale** – roll out the wrapper to all engineering workstations via a package manager (Homebrew, apt, Chocolatey) or an internal artifact repository.

**Production Readiness**  
- **Activity & Adoption** – 5,961 stars, 155 forks, and a recent update (2026‑06‑23) indicate a healthy community and active maintenance.  
- **Stability** – written in Rust, the binary is self‑contained, cross‑platform, and has no heavy runtime dependencies.  
- **Ecosystem Fit** – exposes a clean CLI and machine‑readable output formats, making integration straightforward with existing DevOps tooling.  
- **Risks** – licensing and security posture still need a final review, but no major metadata concerns have been identified. Overall, the project is ready for a serious pilot in production environments.

### Русский

Byron / dua‑cli — это быстрый CLI‑инструмент на Rust для мониторинга использования диска и безопасного удаления ненужных файлов, который помогает инженерам экономить время в ежедневных циклах разработки и ревью. Его типичное применение — ускорение локальных рабочих процессов (автоматизация очистки, подготовка артефактов) и улучшение обратной связи в CI, где быстрый расчёт свободного места критичен. Проект имеет высокую готовность к production: активные коммиты, более 5 тыс. звёзд на GitHub, широкое принятие в сообществе и стабильный набор API/CLI, однако окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
Byron/dua‑cli 是一款基于 Rust 的命令行工具，能够快速查看磁盘空间占用并安全删除无用文件。它以极高的执行效率帮助开发者在本地和 CI 环境中及时清理垃圾数据，从而提升日常开发、代码审查和持续集成的整体速度。

**价值主张**  
- **节省时间**：一键展示磁盘使用情况并提供交互式删除，避免手动查找和误删。  
- **提升工作流**：可在本地脚本、GitHub Actions、GitLab CI 等自动化流水线中调用，实现磁盘清理的自动化，防止因磁盘满导致的构建失败。  
- **增强 CI 反馈**：在 CI 运行前后自动报告磁盘使用变化，帮助团队快速定位资源泄漏问题。

**典型接入方式**  
1. **CLI 直接使用**：在终端执行 `dua <path>` 查看占用，使用 `dua purge` 交互式删除。  
2. **脚本集成**：在 Bash、PowerShell 或 Makefile 中调用 `dua`，配合 `--json` 输出解析，实现自定义报告或条件清理。  
3. **CI/CD 集成**：在 CI 配置文件（如 `.github/workflows/*.yml`）中添加步骤：  
   ```yaml
   - name: Install dua
     run: cargo install dua-cli
   - name: Clean disk space
     run: dua purge --yes --exclude /important/path
   ```  
4. **SDK/库**：虽然主要是 CLI 工具，但其源码公开，可直接在 Rust 项目中作为库依赖，复用磁盘分析逻辑。

**生产可用性**  
- **活跃度**：截至 2026‑06‑23 最近一次提交，拥有 5 961 个 GitHub Stars、155 个 Fork，社区活跃。  
- **技术成熟度**：使用 Rust 编写，具备良好的性能和安全特性；项目已发布多个稳定版本。  
- **生态兼容**：提供标准的 CLI 接口、JSON 输出以及可通过 Cargo 安装的二进制，易于在各种平台和 CI 环境中部署。  
- **风险**：暂无重大元数据风险；仍需在正式使用前确认许可证（MIT/Apache 双授权）符合企业合规要求，并进行常规的安全审计。

综合上述，Byron/dua‑cli 已具备高生产就绪度，适合作为本地和 CI 环境的磁盘清理利器，帮助团队显著提升开发效率和构建可靠性。

## 🧭 Practical evaluation

**Value:** Byron/dua-cli helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 5961 GitHub stars
- 155 forks
- updated 2026-06-23
- primary language: Rust
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 55/100 |
| stars | 80/100 |
| topics | 75/100 |
| outlook | 61/100 |
| quality | 69/100 |
| recency | 40/100 |
| adoption | 73/100 |
| production | 58/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/Byron/dua-cli) · [← Back to Misc](./README.md)</sub>
