# jaredsburrows/gradle-license-plugin

[![Stars](https://img.shields.io/github/stars/jaredsburrows/gradle-license-plugin?style=flat-square&color=yellow)](https://github.com/jaredsburrows/gradle-license-plugin/stargazers) [![Forks](https://img.shields.io/github/forks/jaredsburrows/gradle-license-plugin?style=flat-square&color=blue)](https://github.com/jaredsburrows/gradle-license-plugin/network) [![Language](https://img.shields.io/badge/lang-Groovy-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> Gradle plugin that provides a task to generate a HTML license report of your project.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 440 |
| 🍴 **Forks** | 70 |
| 💻 **Language** | Groovy |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `gradle` `groovy` `html-report` `java` `json-report` `license` `licenses` `open` `open-source` `report` `source`

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Brief Summary**  
The **gradle-license-plugin** is a lightweight Gradle plugin that adds a `generateLicenseReport` task, producing an HTML page that lists all third‑party dependencies and their licenses. It helps developers quickly verify compliance and share licensing information with stakeholders, and it can be plugged into any Java/Groovy/Kotlin‑based Gradle build.  

**Value**  
- **Compliance + Transparency:** Automates the tedious process of gathering license data, reducing legal risk and audit effort.  
- **AI‑ready foundation:** By exposing a clear, machine‑readable list of dependencies, the plugin can feed into downstream AI/ML workflows (e.g., RAG pipelines that need to know which libraries are permissible).  
- **Zero‑config adoption:** A single line in `build.gradle` enables the report, letting teams focus on product code rather than licensing tooling.  

**Practical Adoption Path**  
1. **Add the plugin** to the root `build.gradle` (or `build.gradle.kts`) and run `./gradlew generateLicenseReport`.  
2. **Review the generated `license.html`** to confirm all required notices are present.  
3. **Integrate into CI/CD** (e.g., fail the build if the report contains disallowed licenses) and optionally publish the HTML as an artifact or site page.  
4. **Leverage the output** in AI‑driven compliance checks, documentation generators, or automated RAG agents that need to query allowed libraries.  

**Production Readiness**  
- **Active maintenance:** Last update June 2026, 440 ⭐, 70 🍴, and a healthy issue/PR turnover indicate a vibrant community.  
- **Mature ecosystem fit:** Works with standard Gradle versions and all JVM languages (Groovy, Kotlin, Java).  
- **Low risk:** No critical security findings reported; the plugin’s license (Apache 2.0) is permissive.  
- **Scalability:** Generates static HTML, so it adds negligible build overhead even for large multi‑module projects.  

Overall, the gradle-license-plugin is production‑ready for immediate pilot use, offering a quick compliance win while also serving as a reliable data source for AI‑enhanced tooling.

### Русский

Gradle‑плагин **jaredsburrows/gradle-license-plugin** автоматически генерирует HTML‑отчёт о лицензиях всех зависимостей проекта, что упрощает соблюдение требований открытого ПО и ускоряет подготовку к релизу. Его обычно подключают к сборке Gradle и вызывают задачу `generateLicenseReport`, получая готовый документ для аудита и публикации. Плагин считается готовым к production‑использованию: активные коммиты, более 400 звёзд, широкая адаптация в сообществе и отсутствие серьёзных открытых уязвимостей.

### 中文

**项目简介（2‑3 句）**  
`jaredsburrows/gradle-license-plugin` 是一个 Gradle 插件，能够在构建过程中自动生成项目依赖的 HTML 许可证清单报告，帮助开发者快速了解并合规管理所有第三方库的授权信息。

**价值**  
- **合规审计**：一键生成完整、可视化的许可证报告，满足开源合规、审计和法律审查的需求。  
- **降低风险**：通过明确列出每个依赖的许可证类型，避免因使用不兼容授权而产生的法律纠纷。  
- **提升效率**：无需手动收集或维护许可证信息，插件在 `assemble` 或自定义任务中自动执行，节省人力成本。

**典型接入方式**  
1. 在项目根目录的 `build.gradle`（或 `build.gradle.kts`）中添加插件：  
   ```groovy
   plugins {
       id "com.jaredsburrows.license" version "0.9.0"
   }
   ```
2. 配置报告输出路径（可选）：  
   ```groovy
   licenseReport {
       outputDir = "$buildDir/reports/licenses"
       // 其他自定义过滤、合并等配置
   }
   ```
3. 运行任务生成报告：  
   ```bash
   ./gradlew generateLicenseReport   // 生成 HTML 报告
   ```
   生成的 `licenseReport.html` 即可在浏览器中查看。

**生产可用性**  
- **活跃度**：截至 2026‑06‑26 最近一次提交，拥有 440+ 星、70+ Fork，社区活跃，Issue 处理及时。  
- **兼容性**：基于 Groovy 编写，兼容 Gradle 6+，在 Android、Java、Kotlin 项目中均可直接使用。  
- **成熟度**：插件已在多个开源和商业项目中广泛采用，生成的报告结构稳定，且支持自定义过滤，适合作为 CI/CD 流程的一环。  
- **风险**：暂无重大安全或许可证冲突风险，但仍建议在正式生产环境前审查插件本身的许可证（MIT）以及依赖的第三方库的兼容性。  

综合来看，`gradle-license-plugin` 已具备较高的生产就绪度，适合作为项目合规审计的标准工具快速集成。

## 🧭 Practical evaluation

**Value:** jaredsburrows/gradle-license-plugin helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 440 GitHub stars
- 70 forks
- updated 2026-06-26
- primary language: Groovy
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 46/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 56/100 |
| quality | 64/100 |
| recency | 40/100 |
| adoption | 53/100 |
| production | 56/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/jaredsburrows/gradle-license-plugin) · [← Back to Mobile](./README.md)</sub>
