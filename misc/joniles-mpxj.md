# joniles/mpxj

[![Stars](https://img.shields.io/github/stars/joniles/mpxj?style=flat-square&color=yellow)](https://github.com/joniles/mpxj/stargazers) [![Forks](https://img.shields.io/github/forks/joniles/mpxj?style=flat-square&color=blue)](https://github.com/joniles/mpxj/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> Primary repository for MPXJ library

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 326 |
| 🍴 **Forks** | 113 |
| 💻 **Language** | Java |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
MPXJ is an open‑source Java library for reading and writing Microsoft Project files (MPP, MPX, XML, etc.). With over 300 stars and recent activity (last commit 2026‑05‑13), it can be a handy tool for any workflow that needs to exchange data with Microsoft Project, especially in prototype or internal‑tool contexts.

**Value**  
The library abstracts the complex binary and XML formats used by Microsoft Project, letting developers manipulate schedules, resources, and tasks programmatically without requiring a licensed copy of Microsoft Project. This can dramatically simplify reporting pipelines, data migrations, and custom integrations that need to ingest or generate project plans.

**Practical adoption path**  

1. **Evaluate the API** – Clone the repo, run the provided unit tests, and try a small “read‑a‑file / write‑a‑file” example to confirm it supports the specific Project versions you need.  
2. **Check dependencies** – MPXJ pulls in a few third‑party libraries (e.g., Apache POI, Joda‑Time). Verify they are compatible with your existing stack and that the licensing (Apache‑2.0) fits your project.  
3. **Integrate** – Add the Maven/Gradle artifact (`net.sf.mpxj:mpxj`) to your build, wrap the library in a thin service layer that isolates MPXJ calls, and write integration tests that cover the critical import/export scenarios.  
4. **Validate** – Run the service against real project files from your organization to catch edge‑case format quirks or performance bottlenecks before wider rollout.

**Production readiness**  
The project is **medium‑ready**: it is actively maintained and stable enough for prototypes or internal tools, but the integration surface is not well documented, so you’ll need to invest time in manual testing and possibly contributing missing documentation or bug fixes. Before deploying to production, perform a dependency audit, set up automated regression tests for the file formats you use, and establish a maintenance plan (e.g., monitoring upstream releases and handling version upgrades).

### Русский

**MPXJ** — открытая Java‑библиотека для чтения и записи файлов Microsoft Project (MPP, MPX, XML и др.). Она подходит для быстрого прототипирования или внутренних инструментов, где требуется импортировать/экспортировать данные планов проектов, однако перед внедрением следует проверить совместимость с текущим стеком и оценить затраты на настройку, поскольку детали интеграции в метаданных скудны. Готовность к production — средняя: библиотека активно поддерживается (326 ★, 113 forks, обновления до 2026‑05‑13), но требует ручного аудита и контроля зависимостей перед использованием в критичных системах.

### 中文

**项目简介**  
joniles/mpxj 是 MPXJ 库的主代码仓库，提供对 Microsoft Project（MPP、MPPX、XML 等）文件的读写支持，基于 Java 实现，已累计 326 颗星和 113 次 Fork，近期仍在维护（截至 2026‑05‑13）。

**价值**  
- **跨平台项目数据互操作**：能够在 Java 应用中直接解析、生成或修改 Project 文件，方便在项目管理系统、报表工具或数据迁移场景中使用。  
- **成熟的文件格式覆盖**：支持多种 Project 版本（2003‑2023）以及 Project Server、Project Online 的导出格式，降低自行实现解析逻辑的成本。  
- **开源且活跃**：社区提供的示例代码、Issue 追踪和文档，使得在原型或内部工具中快速上手。

**典型接入方式**  
1. **Maven/Gradle 依赖**  
   ```xml
   <!-- Maven -->
   <dependency>
       <groupId>net.sf.mpxj</groupId>
       <artifactId>mpxj</artifactId>
       <version>12.0.0</version>   <!-- 根据最新 Release 选择 -->
   </dependency>
   ```
   ```groovy
   // Gradle
   implementation 'net.sf.mpxj:mpxj:12.0.0'
   ```
2. **读取文件示例**  
   ```java
   ProjectFile project = new UniversalProjectReader().read(new File("example.mpp"));
   for (Task task : project.getAllTasks()) {
       System.out.println(task.getName() + " – " + task.getStart());
   }
   ```
3. **写入/修改**  
   ```java
   Task newTask = project.addTask();
   newTask.setName("新任务");
   newTask.setStart(DateTime.now());
   new UniversalProjectWriter().write(project, new File("output.mpp"));
   ```
4. **与业务系统集成**  
   - 将读取到的任务信息映射到自研的进度管理数据库。  
   - 在 Spring Boot、Micronaut 等框架中封装为 Service，供 REST API 调用。  
   - 结合 Apache POI、Jackson 等库实现多格式（Excel、JSON）导出。

**生产可用性**  
- **成熟度**：库已存在多年，功能相对稳定，社区维护活跃，适合作为内部或面向客户的项目管理功能的底层实现。  
- **风险**：元数据中未提供完整的 CI/CD、兼容性报告，接入前需自行验证：  
  - 与现有 Java 版本（如 JDK 11/17）及构建工具的兼容性。  
  - 对特定 Project 文件（尤其是自定义字段或宏）是否全部解析。  
- **建议**：在正式生产环境部署前，进行以下检查：  
  1. **单元/集成测试**：覆盖常见的读取、写入、字段映射场景。  
  2. **性能基准**：大文件（>10 MB）读取/写入的耗时评估。  
  3. **依赖审计**：确认库的传递依赖（如 Joda‑Time）符合组织的安全合规要求。  
- **适用场景**：原型开发、内部工具、定制化报表或需要与 Microsoft Project 数据交互的系统；在经过上述验证后，可直接用于生产环境。  

综上，joniles/mpxj 提供了可靠的 Java‑级 Project 文件操作能力，接入成本中等，经过适当的测试与审计后，可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** joniles/mpxj may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 326 GitHub stars
- 113 forks
- updated 2026-05-13
- primary language: Java

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 54/100 |
| topics | 0/100 |
| outlook | 67/100 |
| quality | 64/100 |
| recency | 100/100 |
| adoption | 53/100 |
| production | 68/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/joniles/mpxj) · [← Back to Misc](./README.md)</sub>
