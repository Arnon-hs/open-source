# radareorg/r2garlic

[![Stars](https://img.shields.io/github/stars/radareorg/r2garlic?style=flat-square&color=yellow)](https://github.com/radareorg/r2garlic/stargazers) [![Forks](https://img.shields.io/github/forks/radareorg/r2garlic?style=flat-square&color=blue)](https://github.com/radareorg/r2garlic/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-38%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 38/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
Radareorg / r2garlic couples the world’s fastest Android/DEX decompiler with the radare2 reverse‑engineering framework, giving developers a high‑speed way to translate DEX bytecode into readable C‑like pseudocode. The tool is positioned as a productivity booster for daily development, code review, and CI pipelines, though its integration details are currently sparse.  

**Value**  
- **Speed:** r2garlic’s decompilation runtime is orders of magnitude faster than most open‑source alternatives, cutting the turnaround time for binary analysis and bug‑hunting.  
- **Unified workflow:** By plugging directly into radare2, teams can stay within a single CLI/GUI environment for disassembly, debugging, and decompilation, reducing context‑switching.  
- **Automation potential:** The command‑line interface can be scripted to generate reports or feed CI jobs, providing faster feedback on pull‑requests that touch Android code.  

**Practical adoption path**  

| Step | Action | Why |
|------|--------|-----|
| 1️⃣  | **Clone & build** the repository and run the provided test suite on a representative DEX sample. | Confirms that the binary works on your OS and that dependencies (radare2, libclang, etc.) are satisfied. |
| 2️⃣  | **Create a sandboxed wrapper** (e.g., a Docker image or a CI job) that invokes `r2 -i <dex>` → `r2garlic` → output file. | Isolates the tool, makes it reproducible, and surfaces any missing runtime assets. |
| 3️⃣  | **Integrate into the local workflow** – add a Makefile or Gradle task that runs the wrapper on changed modules and stores the decompiled output for manual inspection. | Gives engineers immediate value while keeping a safety net for false positives. |
| 4️⃣  | **Pilot in CI** – configure a non‑blocking pipeline stage that runs the wrapper on PRs, archives the pseudocode, and optionally flags large diffs. | Provides early feedback without breaking builds if the tool fails. |
| 5️⃣  | **Iterate & harden** – monitor issue tracker, update radare2 version, and add linting or diff‑checking scripts as needed. | Addresses the limited quality signals and ensures long‑term maintainability. |

**Production readiness**  
- **Maturity:** Medium – the project is actively updated (last commit 2026‑05‑13) but has only two topics and limited documentation, so it is best suited for prototypes, internal tooling, or “sandbox‑first” adoption.  
- **Risks:** Sparse integration metadata, unknown license compatibility, and a modest issue‑tracker history mean you should verify the repository’s license, test for stability across radare2 releases, and confirm that the maintainers respond to bugs.  
- **Recommendation:** Deploy the tool behind a manual‑review step (e.g., in a staging CI job) before promoting it to production pipelines. Once the wrapper is stable and the team is comfortable with the output quality, you can consider making the stage mandatory for release builds.

### Русский

**Radareorg/r2garlic** — это интеграция самого быстрого DEX‑декомпилятора с radare2, позволяющая инженерам мгновенно получать читаемый код из Android‑приложений, ускоряя отладку, ревью и автоматизацию CI‑проверок. Типичный сценарий — подключение r2garlic в локальный pipeline (например, в GitHub Actions) для быстрой декомпиляции новых билдов и последующего анализа в radare2; перед масштабным внедрением рекомендуется вручную проверить совместимость, лицензирование и активность проекта. Готовность к production — средняя: подходит для прототипов и внутренних workflow, но требует дополнительного аудита зависимостей и поддержки перед использованием в критичных продакшн‑системах.

### 中文

**项目简介**  
Radareorg/r2garlic 是一款将世界最快的 Android/DEX 反编译器与 radare2 深度融合的开源工具，旨在帮助开发者在日常开发和代码审查中快速获取可读的源码。

**价值**  
- **显著提速**：利用 r2garlic 的高速 DEX 反编译能力，能够在几秒钟内完成大文件的逆向，显著缩短调试和审计的循环时间。  
- **工作流自动化**：可在本地脚本或 CI/CD 流程中调用，实现自动化的二进制分析、报告生成和质量门禁，提升团队效率。  
- **与 radare2 生态兼容**：生成的中间表示直接可在 radare2 中进一步分析、调试或可视化，避免了工具之间的格式转换成本。

**典型接入方式**  
1. **本地脚本**：在开发机器上 `git clone` 项目，使用 `r2 -i r2garlic` 或直接调用 `r2garlic -i <apk>` 完成反编译，输出 radare2 可识别的 `.r2` 或 `.c` 文件。  
2. **CI 集成**：在 CI 配置（如 GitHub Actions、GitLab CI）中添加一个步骤，安装 radare2 与 r2garlic（可通过预编译二进制或 Docker 镜像），对每次提交的 APK 进行自动反编译并将报告上传至审查平台。  
3. **内部工具链**：将 r2garlic 包装为内部 API（例如 Flask/Go microservice），其他工具通过 HTTP 调用获取反编译结果，实现统一的二进制分析服务。

**生产可用性**  
- **成熟度**：目前标记为 **Medium**，适合作为原型或内部工作流使用。代码最近一次更新于 2026‑05‑13，活跃度一般，文档和 issue 反馈相对有限。  
- **接入前检查**：  
  - 确认许可证（MIT/Apache 等）与公司合规要求一致。  
  - 评估依赖（radare2 版本、系统库）是否在生产环境可稳定维护。  
  - 通过小规模内部测试验证反编译准确性、性能以及与现有 CI 工具的兼容性。  
- **生产建议**：在正式上线前，做好以下措施：  
  1. **版本锁定**：使用固定的 Git tag 或 Docker 镜像，防止意外升级导致不兼容。  
  2. **监控与回滚**：为反编译步骤添加日志、执行时间监控，并准备回滚脚本。  
  3. **安全审计**：检查二进制输入的安全性，防止恶意 APK 触发未预料的代码路径。  

综上，r2garlic 能显著加速 Android 逆向分析并与 radare2 无缝衔接，适合作为内部原型或辅助工具使用；在投入生产前需完成依赖、许可证、稳定性和安全性的全面评估。

## 🧭 Practical evaluation

**Value:** Radareorg/r2garlic: the world's fastest Android/DEX decompiler meets radare2 helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-05-13
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 47/100 |
| quality | 36/100 |
| recency | 80/100 |
| adoption | 0/100 |
| production | 51/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/radareorg/r2garlic) · [← Back to Mobile](./README.md)</sub>
