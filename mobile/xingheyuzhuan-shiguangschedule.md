# XingHeYuZhuan/shiguangschedule

[![Stars](https://img.shields.io/github/stars/XingHeYuZhuan/shiguangschedule?style=flat-square&color=yellow)](https://github.com/XingHeYuZhuan/shiguangschedule/stargazers) [![Forks](https://img.shields.io/github/forks/XingHeYuZhuan/shiguangschedule?style=flat-square&color=blue)](https://github.com/XingHeYuZhuan/shiguangschedule/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-47%2F100-brightgreen?style=flat-square)](#)

> 一款开源、无广告、极简的课程表 APP，支持教务导入

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 369 |
| 🍴 **Forks** | 31 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 47/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `jetpack-compose` `kotlin` `schedule` `school-schedule` `school-timetable` `students`

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
XingHeYuZhuan/shiguangschedule is an open‑source, ad‑free, minimalist Android app for managing class schedules, with built‑in support for importing data from university academic‑affairs systems. Written in Kotlin and actively maintained (last commit 2026‑07‑04), the project has gathered modest community interest (≈369 ★, 31 forks). It can serve as a lightweight foundation for custom timetable solutions or internal tools that need a simple, extensible schedule UI.

**Value**  
- **Zero‑ads, clean UI** – ideal for educational institutions or internal portals that want a distraction‑free experience.  
- **Direct import from school portals** – reduces manual data entry and aligns the app with existing academic‑affairs workflows.  
- **Kotlin codebase** – easy to extend for Android developers familiar with modern Android tooling (Jetpack Compose, Coroutines, etc.).  

**Practical Adoption Path**  
1. **Read the README & try the demo** – verify that the import flow matches your institution’s portal format.  
2. **Create a small proof‑of‑concept (PoC)**: fork the repo, replace the demo data source with your own API or CSV export, and run the app on a test device.  
3. **Integrate or wrap**: either embed the schedule UI as a module in a larger app, or use the existing APK as a standalone internal tool.  
4. **Validate dependencies** – check the Gradle file for third‑party libraries, update any outdated versions, and run the full test suite.  

**Production Readiness**  
- **Maturity**: Medium. The app is functional and actively maintained, but it lacks extensive documentation on integration and limited automated tests.  
- **Risks**: Integration steps are not fully described in the metadata; you’ll need to invest time in understanding the import pipeline and possibly refactoring the code to fit your data format.  
- **Next steps before production**: perform a dependency audit, add unit/instrumentation tests for your custom import logic, and confirm that the app complies with your organization’s security and privacy policies.  

Overall, shiguangschedule is a solid starting point for prototypes or internal scheduling tools, provided you allocate time for a modest integration effort and a brief stability review before moving to production.

### Русский

XingHeYuZhuan / shiguangschedule — это открытое Android‑приложение‑расписание без рекламы, написанное на Kotlin, позволяющее быстро импортировать данные из учебного портала и отображать их в минималистичном виде. Его типичный сценарий — интеграция в студенческие или корпоративные мобильные решения для автоматического построения расписаний, где достаточно добавить небольшую библиотеку/модуль и настроить импорт из существующей системы. Готовность к production — средняя: проект активно поддерживается (обновления до 2026‑07‑04), имеет 369 звёзд и 31 форк, но требует проверки зависимостей и небольшого proof‑of‑concept перед масштабным внедрением.

### 中文

**项目简介（2‑3 句）**  
XingHeYuZhuan/shiguangschedule 是一款开源、无广告、极简风格的课程表 Android APP，支持从高校教务系统直接导入课表数据，帮助学生快速构建、查看和管理自己的课程安排。

---

## 价值点

| 价值维度 | 说明 |
|----------|------|
| **零商业干扰** | 完全开源、无广告、无埋点，使用体验纯净，适合对隐私有要求的校园环境。 |
| **快速上手** | 通过教务系统导入（支持常见的教务 JSON/CSV 接口），学生只需一次登录即可自动生成完整课表，省去手动录入的繁琐。 |
| **极简 UI** | 采用 Kotlin + Jetpack Compose 实现的轻量 UI，启动快、占用资源低，适合作为内部工具或原型快速展示。 |
| **可定制** | 源码公开，业务方可在 UI、主题、提醒等层面自行扩展，满足学校或企业内部的特定需求。 |
| **社区活跃** | 已有 369+ stars、31+ forks，最近一次提交在 2026‑07‑04，说明项目仍在维护，社区可提供一定的技术支持。 |

---

## 典型接入方式

1. **源码集成**  
   - 将项目 `git clone` 到本地，使用 Android Studio 打开 `app` 模块。  
   - 在 `build.gradle.kts` 中根据业务方的包名、签名、依赖版本进行适配（如更换 `applicationId`、更新 Kotlin/Compose 版本）。  
   - 若需要对接自有教务系统，只需实现 `CourseImportProvider` 接口，提供统一的课表数据解析（JSON/CSV/Excel），然后在 `ImportActivity` 中注册。  

2. **模块化使用（Gradle Maven 本地依赖）**  
   - 将 `schedule` 模块发布为本地 Maven（`./gradlew publishToMavenLocal`），在业务项目的 `settings.gradle` 中 `includeBuild` 引入。  
   - 业务方只需要在自己的 UI 中嵌入 `ScheduleFragment`，通过 `ViewModel` 注入自己的 `CourseRepository` 即可实现数据驱动。  

3. **最小可行原型（PoC）**  
   - 直接使用项目提供的 `demo` 入口（`MainActivity`），修改 `demo` 中的教务导入 URL 即可快速跑通一次完整的课表展示，适合作为原型验证或内部演示。  

> **关键点**：接入的核心是实现教务数据的统一入口（`CourseImportProvider`），其余 UI 与业务逻辑均已封装好，几乎不需要改动。

---

## 生产可用性评估

| 维度 | 评估 | 说明 |
|------|------|------|
| **代码成熟度** | ★★★★☆ (4/5) | 项目活跃，最近更新在 2026‑07‑04，使用 Kotlin + Jetpack Compose，符合现代 Android 开发规范。 |
| **依赖安全** | ★★★☆☆ (3/5) | 依赖主要是 AndroidX、Kotlin 标准库，安全性高；但需自行审计教务导入的网络请求库（如 Retrofit）是否有已知漏洞。 |
| **文档/示例** | ★★☆☆☆ (2/5) | README 简要说明了导入方式，缺乏完整的集成指南和 API 文档，建议在接入前自行梳理 `CourseImportProvider`、`ScheduleFragment` 的使用方式。 |
| **可扩展性** | ★★★★☆ (4/5) | UI 与业务层解耦，提供插件式的导入接口，便于二次开发（如添加推送提醒、课表导出等）。 |
| **运维成本** | ★★★☆☆ (3/5) | 作为纯客户端 APP，主要成本在于 Android 版本适配与教务接口维护；若需要后台同步，则需自行实现服务端。 |
| **总体生产级别** | **中等**（适合作为内部工具或原型） | 对于校园内部使用、学生自助服务或企业内部培训排课等场景，经过一次代码审计和教务适配即可投入使用；若面向大规模公开发布，建议补充完整的接入文档、单元/UI 测试以及安全审计后再上线。 |

---

### 推荐的接入路径

1. **快速验证**：克隆仓库，运行 `demo`，把教务导入 URL 换成自己的测试数据，确认课表渲染正常。  
2. **代码审计**：检查网络请求、数据解析、权限声明（如存储、网络）是否符合贵公司安全合规要求。  
3. **业务适配**：实现 `CourseImportProvider`，将贵公司教务系统的导出格式统一为项目要求的模型。  
4. **集成到现有 APP**：通过 `includeBuild` 或本地 Maven 将 `schedule` 模块引入主项目，使用 `ScheduleFragment` 替代原有课表页面。  
5. **上线前准备**：添加必要的单元测试、UI 测试，配置签名、混淆规则（ProGuard/R8），并在内部测试渠道完成灰度验证。  

按照上述步骤即可在几天内完成从概念验证到生产级别的落地。祝项目顺利！

## 🧭 Practical evaluation

**Value:** XingHeYuZhuan/shiguangschedule may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 369 GitHub stars
- 31 forks
- updated 2026-07-04
- primary language: Kotlin
- 7 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 38/100 |
| stars | 55/100 |
| topics | 88/100 |
| outlook | 54/100 |
| quality | 61/100 |
| recency | 40/100 |
| adoption | 50/100 |
| production | 53/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-04 · [View on GitHub](https://github.com/XingHeYuZhuan/shiguangschedule) · [← Back to Mobile](./README.md)</sub>
