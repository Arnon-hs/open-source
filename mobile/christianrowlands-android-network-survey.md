# christianrowlands/android-network-survey

[![Stars](https://img.shields.io/github/stars/christianrowlands/android-network-survey?style=flat-square&color=yellow)](https://github.com/christianrowlands/android-network-survey/stargazers) [![Forks](https://img.shields.io/github/forks/christianrowlands/android-network-survey?style=flat-square&color=blue)](https://github.com/christianrowlands/android-network-survey/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> Cellular Survey Android App

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 479 |
| 🍴 **Forks** | 65 |
| 💻 **Language** | Java |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Summary**  
`christianrowlands/android-network-survey` is an open‑source Android app written in Java that lets users collect cellular‑network information (signal strength, cell ID, operator details, etc.) directly from a device. With 479 ★ and recent activity (last commit 2026‑05‑12), it can serve as a quick‑start prototype for field‑testing or internal diagnostics when its README and sample activity align with your workflow.

**Value**  
The project provides a ready‑made UI and sensor‑access code for gathering LTE/5G metrics, saving development time for teams that need to log network performance without building a collector from scratch.

**Practical adoption path**  
1. Clone the repo and run the sample app on a test device to verify that the UI and data output meet your requirements.  
2. Review the README and source code to understand required permissions (e.g., `READ_PHONE_STATE`, `ACCESS_FINE_LOCATION`) and any hard‑coded API calls.  
3. Fork the project and adapt the activity or service to feed the collected data into your backend (e.g., via REST, MQTT, or local storage).  
4. Add dependency checks (Gradle version, Android SDK level) and run the full test suite before integrating it into a larger codebase.

**Production readiness**  
The app is at a **medium** readiness level: it is functional and actively maintained, making it suitable for prototypes, internal tools, or limited‑scale deployments. However, because integration details are sparse, you should perform a manual code audit, confirm compatibility with your target Android versions, and establish a maintenance plan for future SDK updates before using it in a production environment.

### Русский

**Краткое резюме:** `christianrowlands/android-network-survey` — это открытое Android‑приложение для проведения клеточных сетевых опросов, реализованное на Java. Оно удобно использовать в прототипах или внутренних процессах, когда требуется быстро собрать данные о покрытии и качестве сотовой связи (например, в полевых тестах или при оценке новых базовых станций). Готовность к production — средняя: приложение работает, но путь интеграции неочевиден, поэтому перед внедрением следует проверить зависимости, актуальность кода и затраты на настройку.

### 中文

**项目简介**  
`christianrowlands/android-network-survey` 是一款基于 Java 的 Android 应用，用于对移动设备的蜂窝网络信号、基站信息和连接质量进行自动化采集与可视化展示，适合作为网络性能调研或运营商覆盖评估的原型工具。

**价值**  
- 通过统一的 UI 与后台采集逻辑，快速获取大量现场信号指标，帮助研发、运营或学术团队验证网络覆盖假设。  
- 开源代码可自行扩展，支持自定义字段、数据导出（CSV/JSON）以及与内部分析平台的对接。

**典型接入方式**  
1. **克隆仓库 → Android Studio 导入**：使用 Android Studio 打开 `app` 模块，确保 Gradle 与 SDK 版本匹配后编译。  
2. **权限与配置**：在 `AndroidManifest.xml` 中添加必要的权限（`ACCESS_FINE_LOCATION`、`READ_PHONE_STATE`、`ACCESS_NETWORK_STATE`），并在 `res/values/strings.xml` 中配置目标运营商的 MCC/MNC（如有需要）。  
3. **业务集成**：在自己的项目中通过 Gradle 子模块或 AAR 包方式引用 `network-survey`，然后在需要的 Activity/Fragment 中调用 `SurveyManager.startSurvey(context, callback)`，在回调里获取 `SurveyResult` 并自行存储或上报。  
4. **数据后处理**：默认会把采集结果写入本地 SQLite 数据库或导出为 CSV，亦可实现 `SurveyResultListener` 将数据实时推送到内部服务器。

**生产可用性**  
- **成熟度**：已有 479 ★、65 Fork，最近一次提交在 2026‑05‑12，代码基本稳定但缺少完整的 CI/CD 与自动化测试。  
- **适用场景**：适合原型验证、内部调研或实验室测试；若用于大规模生产，需要自行进行代码审计、依赖升级（如 AndroidX、Google Play Services）以及异常恢复机制的补充。  
- **风险**：集成文档较少，需手动检查权限、设备兼容性及后台服务的电量管理策略；建议在正式上线前完成性能评估和安全审计。  

总体而言，该项目在原型阶段价值突出，经过适当的代码审查和包装后可用于内部生产环境，但不建议直接作为面向外部用户的成熟产品投入使用。

## 🧭 Practical evaluation

**Value:** christianrowlands/android-network-survey may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 479 GitHub stars
- 65 forks
- updated 2026-05-12
- primary language: Java

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 57/100 |
| topics | 0/100 |
| outlook | 60/100 |
| quality | 59/100 |
| recency | 80/100 |
| adoption | 54/100 |
| production | 62/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/christianrowlands/android-network-survey) · [← Back to Mobile](./README.md)</sub>
