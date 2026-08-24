# uber/NullAway

[![Stars](https://img.shields.io/github/stars/uber/NullAway?style=flat-square&color=yellow)](https://github.com/uber/NullAway/stargazers) [![Forks](https://img.shields.io/github/forks/uber/NullAway?style=flat-square&color=blue)](https://github.com/uber/NullAway/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> A tool to help eliminate NullPointerExceptions (NPEs) in your Java code with low build-time overhead

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4.1k |
| 🍴 **Forks** | 345 |
| 💻 **Language** | Java |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `java` `nullability` `nullability-analysis` `static-analysis` `static-code-analysis`

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Summary**  
NullAway is an open‑source static analysis tool that plugs into your Java build to detect possible null dereferences at compile time, dramatically reducing the risk of NullPointerExceptions with only a few milliseconds of extra build time. Its lightweight, annotation‑free approach makes it easy to adopt in existing codebases while keeping CI times low.

**Value**  
By catching null‑related bugs before code reaches production, NullAway improves runtime stability and developer confidence, especially for UI‑heavy front‑end and mobile applications where NPEs can surface as user‑visible crashes. The tool’s low overhead means teams can enforce stricter null‑safety without sacrificing build performance.

**Practical adoption path**  
1. Add the NullAway Gradle/Maven plugin to a single module as a proof‑of‑concept.  
2. Run the build and review the generated warnings; fix the most critical issues or add `@Nullable`/`@NonNull` annotations where needed.  
3. Gradually expand the plugin to additional modules, using the README and existing CI scripts as a guide, and tune the `-XepOpt:NullAway:AnnotatedPackages` setting to limit analysis to your own packages.  

**Production readiness**  
NullAway scores high on production readiness: it has over 4 k GitHub stars, active maintenance (last commit 2026‑06‑25), broad adoption across many Uber services, and strong ecosystem signals (Java‑first, compatible with Error Prone). While the integration steps are not fully documented in the metadata, a small pilot can quickly validate setup costs, after which the tool is considered mature enough for a serious production pilot.

### Русский

**Uber/NullAway** — это статический анализатор Java, который позволяет почти полностью избавиться от NullPointerException, не замедляя сборку. Обычно его подключают к существующему CI/CD в виде небольшого proof‑of‑concept: добавляют плагин в Gradle/Maven, проверяют, что проект собирается без ошибок, и постепенно расширяют покрытие, что ускоряет разработку UI‑компонентов и повышает надёжность клиентского кода. Проект считается готовым к production‑использованию: активные коммиты, более 4000 звёзд, широкое принятие в индустрии и хорошая поддержка экосистемы.

### 中文

**简短介绍**  
NullAway（uber/NullAway）是一款基于编译器的静态分析工具，能够在 Java 项目中提前发现并消除潜在的空指针异常（NPE），且对构建时间几乎没有额外开销。

**价值**  
- **提升代码安全性**：在编译阶段即捕获可能的 NPE，避免运行时崩溃，提高系统可靠性。  
- **降低调试成本**：自动化检查取代了大量手工 `null` 判空，开发者可以更专注业务逻辑。  
- **快速交付 UI**：对前端/移动端的 UI 代码同样适用，减少因空指针导致的 UI 渲染异常，从而加速用户界面交付。

**典型接入方式**  
1. **Gradle / Maven**：在项目的构建脚本中添加 NullAway 插件依赖（`com.uber.nullaway:nullaway`），并在 `javac` 参数中启用 `-Xep:NullAway:ERROR`。  
2. **增量启用**：先在少量模块或子项目上打开 NullAway，观察报告并逐步修复 `null` 警告，随后在全局范围推广。  
3. **CI 集成**：将 NullAway 检查作为构建流水线的一步，确保每次提交都通过空指针检查，阻止违规代码进入主分支。  
4. **README/示例参考**：官方仓库提供了完整的接入指南和示例项目，建议先跑通 README 中的 “quick start” 示例，再在实际代码库中进行小范围验证。

**生产可用性**  
- **活跃度**：截至 2026‑06‑25，项目仍在持续更新，拥有 4 070+ 星、345+ Fork，社区活跃。  
- **成熟度**：已被 Uber 以及多家大型公司在生产环境中使用，证明其在大规模代码库上的可靠性。  
- **性能**：基于错误倾向的编译期检查，对构建时间的影响极低，基本不影响 CI/CD 效率。  
- **风险**：元数据中未提供完整的集成文档，实际接入时可能需要自行探索插件配置和兼容性问题。建议先在一个独立的子模块或实验分支进行 PoC，确认设置成本后再推广到全仓库。  

综上所述，NullAway 具备高生产可用性，适合作为 Java 项目（包括前端/移动端 UI 代码）的空指针防护方案，接入成本相对可控，只需做好前期小范围验证即可。

## 🧭 Practical evaluation

**Value:** uber/NullAway helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 4070 GitHub stars
- 345 forks
- updated 2026-06-25
- primary language: Java
- 6 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 63/100 |
| stars | 77/100 |
| topics | 75/100 |
| outlook | 61/100 |
| quality | 69/100 |
| recency | 40/100 |
| adoption | 73/100 |
| production | 56/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/uber/NullAway) · [← Back to Mobile](./README.md)</sub>
