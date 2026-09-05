# galaxyproject/planemo

[![Stars](https://img.shields.io/github/stars/galaxyproject/planemo?style=flat-square&color=yellow)](https://github.com/galaxyproject/planemo/stargazers) [![Forks](https://img.shields.io/github/forks/galaxyproject/planemo?style=flat-square&color=blue)](https://github.com/galaxyproject/planemo/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-77%2F100-brightgreen?style=flat-square)](#)

> Command-line utilities to assist in developing Galaxy and Common Workflow Language artifacts - including tools, workflows, and training materials.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 108 |
| 🍴 **Forks** | 101 |
| 💻 **Language** | Python |
| 📈 **Score** | 77/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `click` `commonwl` `hacktoberfest` `sdk` `usegalaxy`

## 🎯 Categories

Automation · DevTools · Libraries & SDKs

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Planemo (galaxyproject/planemo) is a Python‑based CLI toolkit that streamlines the creation, testing, and publishing of Galaxy tools, Common Workflow Language (CWL) artifacts, and associated training material. By automating repetitive steps—such as tool linting, container building, and workflow validation—it lets developers focus on scientific logic rather than boilerplate plumbing. The project is actively maintained (last commit 2026‑05‑14), widely adopted in the Galaxy ecosystem, and backed by a solid community of contributors (108 ★, 101 forks).

**Value**  
- **Productivity boost:** Eliminates manual, error‑prone tasks (e.g., XML generation, test harness setup), accelerating tool‑to‑Galaxy integration.  
- **Consistency & quality:** Built‑in linting and testing enforce best‑practice standards, reducing downstream failures.  
- **Reusability:** Generates reproducible CWL and Galaxy workflows that can be version‑controlled and shared across teams.

**Practical Adoption Path**  
1. **Install** the CLI (`pip install planemo`) in a developer or CI environment.  
2. **Integrate** Planemo commands into existing build pipelines (e.g., `planemo test`, `planemo lint`, `planemo ci_*`) to automate validation on each pull request.  
3. **Adopt** the generated Docker/Singularity containers for runtime consistency, and use `planemo run` to prototype workflows locally before deployment to a Galaxy instance.  
4. **Scale** by adding Planemo to CI/CD (GitHub Actions, GitLab CI) to enforce continuous compliance and automatically publish vetted tools to the Galaxy Tool Shed.

**Production Readiness**  
- **High:** Recent commits, active issue resolution, and strong adoption in the Galaxy community indicate a mature codebase.  
- **Signals:** 108 GitHub stars, 101 forks, six topical tags, and a clear Python API/CLI surface.  
- **Considerations:** Final due‑diligence should verify the project’s license compatibility, review any disclosed security advisories, and confirm that maintainers have a documented hand‑off process. Once these checks are cleared, Planemo is ready for pilot deployments and can be trusted as a core component of a Galaxy‑centric workflow automation stack.

### Русский

**Краткое резюме:**  
Planemo (galaxyproject/planemo) — это набор CLI‑утилит на Python, который автоматизирует рутинные операции при создании и тестировании артефактов Galaxy и Common Workflow Language (инструменты, рабочие процессы, учебные материалы). Типичный сценарий внедрения — интеграция Planemo в CI/CD‑конвейер для автоматической сборки, валидации и публикации workflow, что устраняет ручные шаги и гарантирует воспроизводимость. Проект считается готовым к production: активная поддержка, частые обновления, широкое принятие в сообществе Galaxy и достаточная инфраструктурная зрелость для серьёзных пилотных запусков.

### 中文

**项目简介**  
galaxyproject/planemo 是一套面向 Galaxy 与 Common Workflow Language（CWL）的命令行工具，帮助开发者快速创建、测试、发布工具、工作流以及培训材料，省去大量手动重复操作。

**价值**  
- **自动化重复任务**：一键生成工具包装、运行本地测试、同步至 Galaxy 实例，显著降低人工出错率。  
- **加速工作流构建**：提供快捷的工作流组装、验证和部署命令，使科研流程更易复用和共享。  
- **提升协作效率**：统一的 CLI/SDK 接口让团队成员能够在本地或 CI 环境中一致地操作，配合 GitHub Actions 等 CI/CD 工具实现持续集成。

**典型接入方式**  
1. **CLI 直接使用**：在本地或 CI 环境中安装 `planemo`（`pip install planemo`），通过 `planemo test`, `planemo serve`, `planemo shed` 等子命令完成工具/工作流的全链路操作。  
2. **SDK 调用**：在 Python 脚本或自定义插件中导入 `planemo` 包，利用其内部 API 实现更细粒度的自动化（如批量验证、元数据生成）。  
3. **CI 集成**：在 GitHub Actions、GitLab CI 或 Jenkins 中加入 `planemo` 步骤，实现 PR 自动测试、Docker 镜像构建、Galaxy ToolShed 发布等完整流水线。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑14 最近一次提交，星标 108、Fork 101，社区活跃且有稳定的维护者。  
- **语言与生态**：Python 实现，易于在现有 Python 环境中部署，兼容 Galaxy、CWL 与多种容器技术。  
- **成熟度**：已在多个科研项目和教学平台中实际使用，具备完整的文档、示例和社区支持，适合作为正式生产环境的工作流自动化工具。  

总体而言，planemo 是一款成熟、易集成且社区活跃的 DevTools，能够显著提升 Galaxy/CWL 生态下的开发效率和工作流可靠性，完全可以在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** galaxyproject/planemo helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 108 GitHub stars
- 101 forks
- updated 2026-05-14
- primary language: Python
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 50/100 |
| stars | 43/100 |
| topics | 75/100 |
| outlook | 77/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 45/100 |
| production | 71/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/galaxyproject/planemo) · [← Back to Automation](./README.md)</sub>
