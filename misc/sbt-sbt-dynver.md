# sbt/sbt-dynver

[![Stars](https://img.shields.io/github/stars/sbt/sbt-dynver?style=flat-square&color=yellow)](https://github.com/sbt/sbt-dynver/stargazers) [![Forks](https://img.shields.io/github/forks/sbt/sbt-dynver?style=flat-square&color=blue)](https://github.com/sbt/sbt-dynver/network) [![Language](https://img.shields.io/badge/lang-Scala-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-49%2F100-brightgreen?style=flat-square)](#)

> An sbt plugin to dynamically set your version from git

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 316 |
| 🍴 **Forks** | 51 |
| 💻 **Language** | Scala |
| 📈 **Score** | 49/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`dynamic-version` `sbt` `sbt-plugin` `versioning`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Project Summary:**

sbt/sbt-dynver is an open-source plugin for sbt that dynamically sets the project version based on the Git repository. This plugin is particularly useful for projects that need to automatically update their version based on their Git history. With its straightforward integration process, it can be a valuable asset for projects looking to streamline their version management.

**Value Proposition:**

The value proposition of sbt/sbt-dynver lies in its ability to simplify version management for projects that use Git. By automatically updating the project version based on the Git repository, developers can save time and reduce errors associated with manual version updates.

**Practical Adoption Path:**

To adopt sbt/sbt-dynver, developers can follow these steps:

1. Evaluate the plugin's implementation signals, such as API/SDK/CLI, language metadata, and focused topics, to ensure it aligns with their project's needs.
2. Integrate the plugin into their sbt project by adding it as a dependency and configuring it according to the plugin's documentation.
3. Test the plugin to ensure it works as expected and updates the project version correctly.

**Production Readiness:**

While sbt/sbt-dynver has a medium production readiness score, it is still a useful tool for prototypes

### Русский

Резюме проекта sbt/sbt-dynver:

Этот плагин sbt позволяет динамически установить версию проекта на основе информации из Git, что может быть полезно при автоматизации процесса версионирования в сложных проектах. Внедрение плагина может быть осуществлено при разработке прототипов или внутренних рабочих процессов, где требуется высокая гибкость и скорость адаптации. Однако перед внедрением в production необходимо провести тщательный осмотр зависимости и поддержки плагина.

### 中文

**项目简介**  
`sbt/sbt-dynver` 是一个 **sbt 插件**，能够在构建时自动从 Git 仓库读取标签/提交信息，生成符合语义化版本号的 `version` 字段，省去手动维护版本号的繁琐。

---

### 价值点
1. **自动化版本管理**：基于 Git 的最新 tag 或 commit，实时生成 `x.y.z‑SNAPSHOT`、`x.y.z‑rcN` 等版本，保证每一次构建都有唯一且可追溯的版本号。  
2. **与 CI/CD 完美契合**：在持续集成流水线中无需额外脚本，只需在 `build.sbt` 中启用插件，即可让每次 CI 运行自动带上对应的 Git 版本。  
3. **降低人为错误**：避免手动修改 `version` 带来的遗漏或冲突，提升团队协作的可靠性。  
4. **轻量且无侵入**：插件本身只有几百行 Scala 代码，依赖少，对现有 sbt 项目几乎没有改动成本。

---

### 典型接入方式
1. **在项目根目录的 `project/plugins.sbt` 中添加**  

   ```scala
   addSbtPlugin("com.github.sbt" % "sbt-dynver" % "5.0.1")   // 版本号请参考最新 release
   ```

2. **在 `build.sbt` 中启用插件**（默认即启用）  

   ```scala
   enablePlugins(DynVerPlugin)   // 可选，若未显式启用，插件会自动生效
   ```

3. **可选配置**（根据需求自定义）  

   ```scala
   dynverSonatypeSnapshots := true          // 生成 SNAPSHOT 版本时加上 -SNAPSHOT
   dynverGitDescribeOutput := DynVerGitDescribeOutput("v", "", "-RC", "", true)
   ```

4. **在 CI 中使用**  
   - 直接读取 `version.value`（如 `sbt "print version"`）作为 Docker 镜像标签、发布 artifact 的版本号等。  
   - 与 GitHub Actions、GitLab CI、Jenkins 等常见 CI 工具配合，无需额外脚本。

---

### 生产可用性评估
| 维度 | 评估 | 说明 |
|------|------|------|
| **社区活跃度** | ★★★★☆ (4/5) | 316 ★、51 Fork，最近一次提交在 **2026‑07‑08**，说明仍在维护。 |
| **成熟度** | ★★★☆☆ (3/5) | 已在多个开源项目中使用，适合作为内部或原型阶段的版本管理方案。 |
| **依赖风险** | ★★☆☆☆ (2/5) | 仅依赖 sbt 与 Scala 标准库，风险低；但使用前需确认与项目 sbt 版本兼容（插件支持 sbt 1.5+）。 |
| **安全/许可证** | ★★★★☆ (4/5) | 基于 Apache‑2.0 许可证，无已知安全漏洞。 |
| **生产建议** | **可用** | 适合 **原型、内部服务、CI/CD 自动化**；在正式生产环境使用前，建议：<br>1. 在预发布环境做一次完整的构建‑发布‑回滚验证。<br>2. 将插件版本锁定在 `project/plugins.sbt`，防止因上游突发改动导致构建不稳定。 |

**结论**：`sbt-dynver` 是一个轻量、自动化的版本号生成方案，能够显著简化 Scala/sbt 项目的发布流程。对大多数内部或中小型生产系统来说，经过一次预发布验证后即可安全投入使用。只要保持插件版本的明确锁定并定期检查其兼容性，即可在生产环境中获得可靠的版本管理支持。

## 🧭 Practical evaluation

**Value:** sbt/sbt-dynver may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 316 GitHub stars
- 51 forks
- updated 2026-07-08
- primary language: Scala
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 43/100 |
| stars | 53/100 |
| topics | 50/100 |
| outlook | 50/100 |
| quality | 55/100 |
| recency | 40/100 |
| adoption | 50/100 |
| production | 53/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-08 · [View on GitHub](https://github.com/sbt/sbt-dynver) · [← Back to Misc](./README.md)</sub>
