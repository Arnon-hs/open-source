# facebook/SoLoader

[![Stars](https://img.shields.io/github/stars/facebook/SoLoader?style=flat-square&color=yellow)](https://github.com/facebook/SoLoader/stargazers) [![Forks](https://img.shields.io/github/forks/facebook/SoLoader?style=flat-square&color=blue)](https://github.com/facebook/SoLoader/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> Native code loader for Android

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.4k |
| 🍴 **Forks** | 191 |
| 💻 **Language** | Java |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Summary**  
SoLoader is Facebook’s lightweight native‑code loader for Android, providing a simple API to load shared libraries ( .so  files) at runtime. With over 1.4 k stars and recent activity, it can streamline the bootstrap of native modules in apps that already use Facebook’s ecosystem, but its integration points are not well documented.

**Value**  
- Eliminates boilerplate and platform‑specific quirks when loading native libraries, offering a unified, battle‑tested solution that works across Android versions.  
- Reduces the risk of runtime crashes caused by incorrect `System.loadLibrary` calls, especially in projects that bundle multiple native modules or need to load them conditionally.

**Practical adoption path**  
1. **Review the README and source** to understand the expected initialization sequence (`SoLoader.init`) and the supported loading patterns.  
2. **Add the library** as a Gradle dependency (`implementation 'com.facebook.soloader:soloader:x.y.z'`).  
3. **Integrate the init call** early in your `Application` class, then replace existing `System.loadLibrary` calls with `SoLoader.loadLibrary`.  
4. **Run the provided unit tests** and a small prototype on target devices to confirm that the loader resolves your .so files correctly.  
5. **Audit transitive dependencies** (e.g., Facebook’s `folly` or `fbjni`) to ensure they do not introduce version conflicts.

**Production readiness**  
The project is at a **medium** readiness level: it is actively maintained and widely used internally at Facebook, making it suitable for prototypes or internal tools. However, because integration guidance is sparse, teams should allocate time for a manual code‑review, verify compatibility with their build system, and set up monitoring for any loader‑related crashes before promoting SoLoader to a production release.

### Русский

**SoLoader** — это лёгкий загрузчик нативных библиотек для Android, позволяющий динамически подгружать `.so`‑файлы из Java‑кода без необходимости писать собственные JNI‑обёртки. Он обычно интегрируется в проекты, где требуется быстрый прототип или внутренний инструмент, который работает с нативным кодом (например, при подключении собственных C/C++‑модулей к React Native или другим фреймворкам). По уровню готовности — проект имеет среднюю готовность к production: достаточное количество звёзд и активные обновления, но путь интеграции неочевиден, поэтому перед внедрением следует вручную проверить совместимость, зависимости и требования к сборке.

### 中文

**项目简介**  
SoLoader（facebook/SoLoader）是 Facebook 开源的 Android 原生库加载器，提供统一、可靠的方式在 Java 层加载 `.so` 动态库，解决了不同 Android 版本、CPU 架构以及系统限制下的兼容性问题。

**价值**  
- **统一加载入口**：封装了 `System.loadLibrary` 的细节，自动处理库的解压、拷贝和路径管理，减少手动编写 JNI 加载代码的工作量。  
- **跨平台兼容**：内置对多种 ABI（armeabi‑v7a、arm64‑v8a、x86、x86_64 等）的适配逻辑，避免在不同设备上出现 “UnsatisfiedLinkError”。  
- **轻量且可扩展**：仅依赖 Java，源码体积小，易于在现有 Android 项目中嵌入或自行定制。

**典型接入方式**  
1. **Gradle 引入**  
   ```gradle
   implementation 'com.facebook.soloader:soloader:0.10.5'   // 版本请参考最新 release
   ```
2. **初始化**（通常在 `Application` 的 `onCreate` 中）  
   ```java
   public class MyApp extends Application {
       @Override
       public void onCreate() {
           super.onCreate();
           SoLoader.init(this, /* native exopackage */ false);
       }
   }
   ```
3. **加载库**  
   ```java
   SoLoader.loadLibrary("my_native_lib");
   ```
   之后即可通过常规的 JNI 接口调用本地方法。

**生产可用性**  
- **成熟度**：GitHub ★1.4k、Fork 191，最近一次提交在 2026‑07‑02，活跃度仍然可观。  
- **适用场景**：适合内部原型、实验性功能以及对本地库加载有明确需求的生产系统。  
- **风险与注意事项**  
  - 项目本身不提供完整的构建或打包流水线，需要自行确保 `.so` 文件随 APK 正确打包（可结合 Android App Bundle 或 exopackage 使用）。  
  - 元数据中缺少详细的集成指南，建议在正式项目中先做一次小规模验证，确认加载路径、ABI 过滤以及混淆规则（ProGuard/R8）不会导致运行时错误。  
  - 维护成本相对低，但仍需关注 Facebook 是否继续维护该仓库以及潜在的安全补丁。

综上，SoLoader 是一个 **中等成熟度、轻量且易于集成** 的原生库加载方案，适合在对本地代码有依赖的 Android 项目中使用，只要在引入前做好兼容性和维护性评估，即可投入生产环境。

## 🧭 Practical evaluation

**Value:** facebook/SoLoader may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1436 GitHub stars
- 191 forks
- updated 2026-07-02
- primary language: Java

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 57/100 |
| stars | 67/100 |
| topics | 0/100 |
| outlook | 62/100 |
| quality | 64/100 |
| recency | 80/100 |
| adoption | 64/100 |
| production | 64/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/facebook/SoLoader) · [← Back to Mobile](./README.md)</sub>
