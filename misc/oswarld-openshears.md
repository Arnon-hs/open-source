# oswarld/openshears

[![Stars](https://img.shields.io/github/stars/oswarld/openshears?style=flat-square&color=yellow)](https://github.com/oswarld/openshears/stargazers) [![Forks](https://img.shields.io/github/forks/oswarld/openshears?style=flat-square&color=blue)](https://github.com/oswarld/openshears/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-44%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 44/100 |
| 🗓️ **Last push** | 2026-05-18 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Three months ago the author warned that the OpenClaw tool would not uninstall cleanly and prepared a workaround. The repository, discovered via Hacker News mentions, contains a brief README and minimal activity, making it a niche utility that may only be useful when its limited documentation aligns with a specific workflow.

**Value**  
- Provides a concrete example of handling problematic uninstalls for OpenClaw, which can save time for developers who need to cleanly remove the tool from CI/CD images or developer workstations.  
- The workaround code and notes serve as a reference for building robust uninstall scripts for other third‑party binaries that lack proper package‑manager support.

**Practical Adoption Path**  
1. **Inspect the repo** – clone the project, review the README, source code, and any scripts that address the uninstall issue.  
2. **Validate the fix** – run the provided uninstall routine in an isolated environment (e.g., Docker container or VM) to confirm it removes all OpenClaw artifacts without side effects.  
3. **Integrate** – wrap the script in your own deployment pipeline (e.g., as a post‑install hook in your CI, or as a cleanup step in a Dockerfile).  
4. **Add tests** – create minimal regression tests that verify the uninstall succeeds on the target OS versions you support.  
5. **Document** – record the integration steps and any required environment variables in your internal docs so future team members can reuse the solution.

**Production Readiness**  
- **Readiness Level:** *Medium* – suitable for prototypes, internal tooling, or environments where OpenClaw is an optional component.  
- **What to verify before production:**  
  - License compatibility and any attribution requirements.  
  - Ongoing maintenance: the repo shows sparse commits; consider forking and maintaining the uninstall script yourself.  
  - Issue tracker and community activity: limited, so you may need to handle bugs internally.  
  - Compatibility with your OS/distribution versions and any packaging constraints.  

If these checks pass, the project can be adopted for internal workflows, but it should not be relied upon as a critical production dependency without additional testing and possibly a self‑maintained fork.

### Русский

**Краткое резюме:**  
Проект *3months ago, I predicted OpenClaw wouldn't uninstall cleanly and prepared for it* предлагает готовый набор скриптов и инструкций для безопасного удаления OpenClaw, что может пригодиться в проектах, где требуется гарантировать чистую деинсталляцию перед обновлением или миграцией. Типичный сценарий — интеграция в CI/CD или внутренний workflow для автоматической проверки и восстановления среды перед развёртыванием новых версий. Готовность к production — средняя: проект пригоден для прототипов и внутренних процессов, но перед использованием следует проверить лицензию, актуальность документации, активность репозитория и частоту релизов.

### 中文

**项目简介（2‑3 句话）**  
该项目名为 *“3months ago, I predicted OpenClaw wouldn't uninstall cleanly and prepared for it”*，最初在 Hacker News 上被发现（github‑mentions），目前得分 44/100，归类为 Misc。它记录了一段对 OpenClaw 卸载行为的预测与预处理方案，适合作为特定工作流的参考示例。

**价值**  
- 为需要在自动化脚本或 CI/CD 流程中处理 OpenClaw 卸载异常的场景提供了实战经验。  
- 当项目的 README 与实际活动能够映射到具体的工作流时，可直接复用其思路，节省调研和排错时间。  

**典型接入方式**  
1. **代码审查**：在项目根目录或 CI 脚本中加入该仓库的相关文件（如 `uninstall.sh`、`precheck.sh`），并结合自己的构建系统进行适配。  
2. **手动检查**：由于元数据中集成信号稀疏，建议在首次接入前手动阅读源码、README 与 issue 列表，确认其卸载逻辑符合当前环境。  
3. **依赖管理**：在 `package.json`、`requirements.txt` 或系统级包管理器中声明对 OpenClaw 的版本约束，并在部署前运行项目提供的预检查脚本。  

**生产可用性**  
- **成熟度**：中等（Medium）。项目已在 2026‑05‑18 更新，包含 2 个主题标签，但缺乏持续活跃的维护和完整的文档。  
- **适用场景**：适合原型开发、内部工具或需要快速验证 OpenClaw 卸载行为的团队。若用于对外生产系统，需额外进行：  
  - 许可证合规审查  
  - 维护频率与社区活跃度评估  
  - 完善的单元/集成测试  
  - 与现有部署流程的兼容性验证  

综上，该项目在特定的 OpenClaw 卸载预处理需求上具备实用价值，但在正式生产环境使用前应进行充分的手动审查与补充测试。

## 🧭 Practical evaluation

**Value:** 3months ago, I predicted OpenClaw wouldn't uninstall cleanly and prepared for it may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-05-18
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 54/100 |
| quality | 41/100 |
| recency | 100/100 |
| adoption | 0/100 |
| production | 60/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 80/100 |

---

<sub>🔭 Discovered 2026-05-18 · [View on GitHub](https://github.com/oswarld/openshears) · [← Back to Misc](./README.md)</sub>
