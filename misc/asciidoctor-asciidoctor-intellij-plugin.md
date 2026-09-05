# asciidoctor/asciidoctor-intellij-plugin

[![Stars](https://img.shields.io/github/stars/asciidoctor/asciidoctor-intellij-plugin?style=flat-square&color=yellow)](https://github.com/asciidoctor/asciidoctor-intellij-plugin/stargazers) [![Forks](https://img.shields.io/github/forks/asciidoctor/asciidoctor-intellij-plugin?style=flat-square&color=blue)](https://github.com/asciidoctor/asciidoctor-intellij-plugin/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> AsciiDoc plugin for products on the IntelliJ platform (IDEA, RubyMine, etc)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 392 |
| 🍴 **Forks** | 155 |
| 💻 **Language** | Java |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`antora` `asciidoc` `asciidoctor` `hacktoberfest` `intellij-plugin`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
The **asciidoctor‑intellij‑plugin** adds full‑featured AsciiDoc support to any JetBrains IDE (IntelliJ IDEA, RubyMine, PyCharm, etc.), enabling live preview, syntax highlighting, navigation and export to HTML/PDF directly inside the editor. With over 390 stars and recent updates, it is a mature open‑source extension that streamlines documentation authoring for development teams.  

**Value**  
- **Unified workflow** – developers can write, preview, and publish AsciiDoc without leaving their IDE, reducing context‑switching and accelerating documentation cycles.  
- **Consistency** – the plugin enforces AsciiDoc syntax and provides project‑wide rendering, helping teams keep technical docs, READMEs, and release notes in sync with code.  
- **Extensibility** – built on the Asciidoctor Java library, it can be customized or integrated with CI pipelines for automated doc generation.  

**Practical adoption path**  
1. **Evaluate** – Install the plugin from the JetBrains Marketplace in a sandbox or a single developer’s IDE and test the core features (preview, export, navigation).  
2. **Pilot** – Roll it out to a small team working on a shared documentation repository; configure project‑level settings (e.g., custom attributes, include paths).  
3. **Integrate** – Add the plugin to your IDE image or configuration management (e.g., Docker‑based dev containers, JetBrains Toolbox) and optionally script Asciidoctor CLI calls for CI builds.  
4. **Govern** – Review the MIT‑style license, run a security scan of the bundled Asciidoctor Java dependency, and set up a maintenance schedule for version upgrades.  

**Production readiness**  
- **Maturity** – Medium: the plugin is actively maintained (last commit 2026‑06‑27), has a healthy star/fork count, and is used across many JetBrains‑based projects, making it reliable for internal tooling and prototypes.  
- **Considerations** – Verify compatibility with your IDE version, audit the underlying Asciidoctor library for any known CVEs, and assign an owner for periodic updates. Once these checks are done, the plugin can be safely promoted to production environments for documentation pipelines and developer onboarding.

### Русский

**asciidoctor/asciidoctor‑intellij‑plugin** — это плагин для поддержки AsciiDoc в IDE семейства IntelliJ (IDEA, RubyMine, WebStorm и др.). Он упрощает работу с документацией, позволяя писать, просматривать и экспортировать AsciiDoc‑файлы прямо в среде разработки, что ускоряет создание и поддержание технической документации в проектах. Плагин имеет средний уровень готовности к production: активные коммиты, 392 звёзд и 155 форков, но перед внедрением в критически важные системы рекомендуется проверить лицензию, безопасность зависимостей и наличие поддерживающих мейнтейнеров.

### 中文

**项目简介**  
asciidoctor/asciidoctor‑intellij‑plugin 是一款在 IntelliJ 系列 IDE（IDEA、RubyMine、PyCharm 等）上提供 AsciiDoc 编辑、渲染和预览功能的插件，帮助开发者在 IDE 中直接编写和查看文档。

**价值**  
- **提升文档编写效率**：在代码编辑器内实时渲染 AsciiDoc，省去切换工具的时间。  
- **统一团队文档规范**：通过插件统一渲染引擎，确保所有成员看到的文档样式一致。  
- **降低学习成本**：使用熟悉的 IDE 环境，无需额外学习独立的文档编辑器。

**典型接入方式**  
1. **插件市场安装**：在 IDE 的插件仓库搜索 “AsciiDoc” 并直接安装。  
2. **项目级配置**：在项目根目录添加 `asciidoctorconfig.yml`（可选），自定义渲染选项、宏定义等。  
3. **CLI/SDK 结合**：插件内部提供 `asciidoctor` CLI 接口，可在构建脚本（Gradle、Maven）中调用，实现文档的自动生成与 CI 集成。

**生产可用性**  
- **成熟度**：GitHub ★392、Fork ★155，最近一次提交在 2026‑06‑27，活跃度尚可。  
- **适用场景**：非常适合内部文档、技术博客、产品手册等快速迭代的场景；在对文档渲染一致性要求高的团队中也能稳定使用。  
- **风险与注意事项**：需自行检查许可证兼容性（MIT），并在正式环境中评估插件的安全更新频率与维护者响应速度。总体而言，作为原型或内部工作流的工具已相对可靠，生产环境使用前建议做好依赖审计与版本锁定。

## 🧭 Practical evaluation

**Value:** asciidoctor/asciidoctor-intellij-plugin helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 392 GitHub stars
- 155 forks
- updated 2026-06-27
- primary language: Java
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 55/100 |
| stars | 55/100 |
| topics | 63/100 |
| outlook | 66/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 55/100 |
| production | 68/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/asciidoctor/asciidoctor-intellij-plugin) · [← Back to Misc](./README.md)</sub>
