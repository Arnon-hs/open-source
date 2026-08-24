# zamojski/TowerCollector

[![Stars](https://img.shields.io/github/stars/zamojski/TowerCollector?style=flat-square&color=yellow)](https://github.com/zamojski/TowerCollector/stargazers) [![Forks](https://img.shields.io/github/forks/zamojski/TowerCollector?style=flat-square&color=blue)](https://github.com/zamojski/TowerCollector/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-40%2F100-brightgreen?style=flat-square)](#)

> The OpenCellID and BeaconDB contributor's app.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 329 |
| 🍴 **Forks** | 42 |
| 💻 **Language** | Java |
| 📈 **Score** | 40/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
TowerCollector (zamojski/TowerCollector) is a Java‑based desktop client that lets users collect, edit, and upload cellular tower and Bluetooth beacon data to the OpenCellID and BeaconDB databases. It provides a simple UI for scanning, geotagging, and batch‑exporting observations, making it a handy tool for contributors who need to enrich location‑based datasets.

**Value**  
- **Data contribution** – Automates the capture of GSM/LTE/5G cell IDs and BLE beacons, reducing the manual effort required to grow OpenCellID and BeaconDB.  
- **Cross‑platform** – Runs on any system with a Java runtime, so contributors can use existing laptops or Raspberry Pi setups.  
- **Export flexibility** – Supports CSV, JSON and direct API upload, enabling downstream pipelines (e.g., map‑matching, coverage analysis) to consume the data without custom parsers.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, build with Maven/Gradle, and run the UI on a test machine equipped with a supported radio (e.g., a USB LTE dongle or a BLE scanner).  
2. **Workflow validation** – Verify that the scan results match your field‑testing expectations, and experiment with the export formats or the built‑in API upload to a sandbox OpenCellID/BeaconDB instance.  
3. **Integration** – Wrap the command‑line export step in a script that feeds the generated files into your existing data‑ingestion pipeline; if needed, extend the Java code to emit custom JSON fields.  
4. **Governance** – Pin the specific commit/tag used, audit the third‑party libraries, and add health‑checks (e.g., “tower count > 0”) to detect mis‑configurations before committing data to production databases.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑05‑11) and has a respectable community signal (329 ★, 42 forks), but the integration surface is thin—metadata about configuration, CI pipelines, and deployment scripts is sparse.  
- **Suitability**: Good for prototypes, internal data‑collection workflows, or as a “data‑ingestion front‑end” for teams that already run OpenCellID/BeaconDB.  
- **Risks**: Lack of explicit integration documentation means you’ll need to allocate time for manual testing and possibly code tweaks; also verify that the Java runtime and radio drivers are compatible with your production environment.  

Overall, TowerCollector can accelerate crowd‑sourced tower/beacon collection when you’re willing to perform a modest validation effort before rolling it into a production‑grade pipeline.

### Русский

**TowerCollector** — это Java‑приложение для сбора и публикации данных о сотовых вышках и Bluetooth‑маячках, используемое участниками проектов OpenCellID и BeaconDB. Его обычно внедряют в прототипные или внутренние пайплайны геоданных: приложение сканирует сеть, формирует CSV/JSON‑отчёты и отправляет их в центральные базы, после чего результаты проверяются вручную. Готовность к production — средняя: проект активно поддерживается (обновления 2026‑05‑11, 329 звёзд), но интеграция требует предварительной проверки зависимостей и настройки, поскольку автоматических инструкций мало.

### 中文

**项目简介**  
zamojski/TowerCollector 是一款面向 OpenCellID 与 BeaconDB 贡献者的 Java 应用，用于采集、整理和上传移动基站及蓝牙信标信息。它帮助社区快速构建本地测量数据，并同步到公开数据库。

**价值**  
- **数据收集利器**：提供统一的采集流程，降低手动记录基站/信标信息的工作量。  
- **社区协同**：直接对接 OpenCellID 与 BeaconDB，提交的数据可立即惠及全球定位与定位服务生态。  
- **原型与内部工具**：适合研发团队在信号覆盖分析、网络规划或位置服务原型阶段快速获取真实基站数据。

**典型接入方式**  
1. **环境准备**：在 Android 设备或支持 Java 的嵌入式平台上安装项目依赖（Gradle/Maven）。  
2. **配置 API**：在 `config.properties` 中填写 OpenCellID / BeaconDB 的 API key 与上传端点。  
3. **启动采集**：调用 `TowerCollector.start()`，根据需求选择 GPS、CellInfo、BLE 扫描模式。  
4. **数据上传**：采集完成后，使用内置的 `Uploader` 将 JSON/CSV 数据推送到对应数据库。  
5. **可选扩展**：通过实现 `ITowerProcessor` 接口，自定义数据过滤、聚合或与内部系统的同步逻辑。

**生产可用性**  
- **成熟度**：项目已有 329 ⭐、42 🍴，最近一次提交在 2026‑05‑11，代码活跃度中等。  
- **适用场景**：适合原型、内部测试或数据采集任务；在生产环境使用前建议完成以下检查：  
  - 评估依赖库的安全性与长期维护（Gradle 依赖、Android SDK 版本）。  
  - 验证网络上传接口的稳定性与速率限制。  
  - 加入异常监控与日志收集，以防采集过程中出现的硬件或权限问题。  
- **风险**：元数据中缺乏明确的集成文档，接入成本主要在于手动配置 API、权限申请以及对采集结果的后处理。完成这些步骤后，系统可在内部部署的定位或网络规划工作流中稳定运行。

## 🧭 Practical evaluation

**Value:** zamojski/TowerCollector may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 329 GitHub stars
- 42 forks
- updated 2026-05-11
- primary language: Java

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 41/100 |
| stars | 54/100 |
| topics | 0/100 |
| outlook | 38/100 |
| quality | 43/100 |
| recency | 20/100 |
| adoption | 50/100 |
| production | 42/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/zamojski/TowerCollector) · [← Back to Misc](./README.md)</sub>
