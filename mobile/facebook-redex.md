# facebook/redex

[![Stars](https://img.shields.io/github/stars/facebook/redex?style=flat-square&color=yellow)](https://github.com/facebook/redex/stargazers) [![Forks](https://img.shields.io/github/forks/facebook/redex?style=flat-square&color=blue)](https://github.com/facebook/redex/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> A bytecode optimizer for Android apps

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 6.3k |
| 🍴 **Forks** | 678 |
| 💻 **Language** | C++ |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-07-08 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Mobile

## 📝 Summary

### English

Here's a brief summary of the open-source project facebook/redex:

Facebook Redex is an open-source bytecode optimizer for Android apps that can improve performance and reduce app size. Its value lies in its potential to streamline development workflows, particularly for prototypes or internal projects, where its optimization capabilities can make a tangible difference. However, due to its sparse integration signals and medium production readiness, careful validation and setup are required before committing to production use.

In terms of practical adoption path, the project's README and activity should be thoroughly reviewed to ensure alignment with the intended workflow. Manual inspection is necessary to confirm the integration process and address potential risks. Once validated, the project can be adopted for its intended use cases, such as optimizing Android app performance and reducing app size.

In terms of production readiness, Facebook Redex is rated as medium, indicating that it can be useful for prototypes or internal workflows, but may require additional checks and validation before being used in production environments. This is due to the need for manual inspection and potential setup costs, which can impact the project's overall adoption and maintenance.

### Русский

Резюме проекта facebook/redex:

Facebook Redex - это оптимизатор байткода для Android-приложений, который может быть полезен в конкретных рабочих процессах, если README и активность проекта соответствуют им. typовой сценарий внедрения предполагает ручной осмотр перед принятием решения о внедрении, поскольку сигналы интеграции в метаданных разбросаны. Проект готов к production на среднем уровне, что означает его пригодность для прототипов или внутренних рабочих процессов, но требует проверки зависимостей и поддержки перед выпуском в производство.

### 中文

**价值**  
Redex 是 Facebook 开源的 Android 字节码优化工具，能够在编译后对 *.dex* 文件进行多种优化（如方法内联、类合并、未使用代码剔除等），显著减小 APK 体积并提升运行时性能。对需要在发布前压缩体积或提升启动速度的 Android 项目尤为有用。

**典型接入方式**  
1. **安装**：通过源码编译或直接使用 Facebook 提供的二进制发行版。  
2. **配置**：在项目根目录创建 `redex-config.json`，声明要启用的优化 Pass（如 `MethodInlinePass`、`MergeClassesPass` 等），并可根据业务需求排除特定类或方法。  
3. **集成**：在 CI/CD 流程或本地构建脚本中加入一步调用，例如  
   ```bash
   ./redex -i app.apk -o app-optimized.apk -c redex-config.json
   ```  
   该步骤通常放在 `apktool`/`bundletool` 打包完成后、签名之前。  
4. **验证**：运行优化前后的 APK，使用 `apktool`、`dexdump` 或自动化 UI 测试比对功能、体积和启动时间，确保没有功能回归。

**生产可用性**  
- **成熟度**：GitHub 近 6300 星、678 Fork，活跃维护至 2026‑07‑08，代码基于 C++ 实现，性能可靠。  
- **准备度**：**中等**。适合作为原型或内部流水线的优化环节，但因官方文档和元数据中缺少完整的集成指南，建议在正式上线前进行一次完整的手动审查和回归测试。  
- **风险**：集成路径不够透明，可能需要根据项目的 ProGuard/R8 配置自行调优；此外，升级 Redex 版本时需检查依赖的 LLVM/Clang 兼容性。  

综上，Redex 在需要显著压缩 APK 大小或提升启动性能的 Android 项目中具备较高价值，推荐在内部 CI 中先做验证，确认无功能回归后再推广到生产环境。

## 🧭 Practical evaluation

**Value:** facebook/redex may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 6291 GitHub stars
- 678 forks
- updated 2026-07-08
- primary language: C++

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 71/100 |
| stars | 81/100 |
| topics | 0/100 |
| outlook | 73/100 |
| quality | 75/100 |
| recency | 100/100 |
| adoption | 78/100 |
| production | 72/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-08 · [View on GitHub](https://github.com/facebook/redex) · [← Back to Mobile](./README.md)</sub>
