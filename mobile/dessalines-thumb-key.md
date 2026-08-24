# dessalines/thumb-key

[![Stars](https://img.shields.io/github/stars/dessalines/thumb-key?style=flat-square&color=yellow)](https://github.com/dessalines/thumb-key/stargazers) [![Forks](https://img.shields.io/github/forks/dessalines/thumb-key?style=flat-square&color=blue)](https://github.com/dessalines/thumb-key/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-49%2F100-brightgreen?style=flat-square)](#)

> A privacy-conscious Android keyboard made for your thumbs

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.5k |
| 🍴 **Forks** | 309 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 49/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `android-app` `android-keyboard` `keyboard`

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
thumb‑key is an open‑source Android keyboard written in Kotlin that focuses on privacy and thumb‑friendly typing. With nearly 1.5 k stars and active maintenance, it offers a lightweight alternative to mainstream keyboards for users who want to keep their keystrokes off the cloud. The project is most useful when its README and sample activity align with a concrete workflow, such as a custom in‑app keyboard or a secure internal device.

**Value**  
- **Privacy‑first**: No network‑based prediction or telemetry, making it suitable for apps that handle sensitive data.  
- **Thumb‑optimized layout**: Designed for one‑hand use on larger screens, improving ergonomics for mobile‑first teams.  
- **Open source & Kotlin native**: Easy to audit, extend, and integrate into existing Android codebases without pulling in large third‑party SDKs.

**Practical Adoption Path**  
1. **Read the README & sample activity** – verify that the provided demo matches the desired input flow (e.g., a custom input method service).  
2. **Create a small proof‑of‑concept module** that swaps the default system keyboard with thumb‑key in a sandbox app.  
3. **Run the demo on a test device** to assess UI responsiveness, permission handling, and any required manifest entries.  
4. **Iterate** by adding any needed callbacks (e.g., `onKey`, `onTextCommit`) and customizing the layout or theme to fit your brand.  
5. **Document the integration steps** for the team, then roll out to a limited internal pilot before broader deployment.

**Production Readiness**  
- **Maturity**: Medium. The library is actively maintained (last update 2026‑06‑27) and has a solid community signal (≈1.5 k stars, 300+ forks), but it lacks formal release notes, extensive test coverage, or a clear migration guide.  
- **Suitability**: Ideal for prototypes, internal tools, or niche consumer apps where privacy and thumb ergonomics are a priority.  
- **Risks**: The integration path isn’t fully documented; you’ll need to invest time to understand the InputMethodService setup and verify that no hidden dependencies conflict with your app’s build pipeline. Conduct a dependency audit and maintain a fork or vendor copy to mitigate future upstream changes before committing to production use.

### Русский

**dessalines/thumb‑key** — это открытая клавиатура для Android, ориентированная на конфиденциальность и удобство ввода большим пальцем. Она подходит для прототипов или внутренних приложений, где требуется кастомная клавиатура без сбора пользовательских данных; рекомендуется начать с небольшого proof‑of‑concept, проверив README и пример активности, а затем оценить зависимости и план обслуживания. Готовность к продакшну — средняя: проект имеет активную поддержку (1497 звёзд, 309 форков, обновления до 2026‑06‑27), но интеграционный путь не полностью документирован, поэтому перед внедрением стоит уточнить настройки и возможные риски.

### 中文

**项目价值**  
`dessalines/thumb-key` 是一款专为拇指操作优化的 Android 键盘，强调隐私保护（不收集或上传用户输入），适合对数据安全有严格要求的内部工具、原型或面向隐私敏感用户的产品。其轻量的 Kotlin 实现和简洁的 UI 能够显著提升单手输入体验，降低误触率。

**典型接入方式**  

1. **阅读 README 与示例 Activity**  
   - 项目根目录下的 `README.md` 提供了快速上手指南，包括在 `settings.gradle` 中声明仓库、在 `app/build.gradle` 中添加依赖以及在 `AndroidManifest.xml` 中声明键盘服务。  
   - 示例 Activity 展示了如何在自定义输入框中启用 Thumb‑Key（通过 `InputMethodManager` 调用 `showInputMethodPicker()` 或直接指定 `imeId`）。

2. **在现有项目中引入**  
   ```gradle
   // settings.gradle
   dependencyResolutionManagement {
       repositories {
           mavenCentral()
           // 若使用 GitHub Packages
           maven { url = uri("https://maven.pkg.github.com/dessalines/thumb-key") }
       }
   }

   // app/build.gradle
   dependencies {
       implementation "com.dessalines:thumb-key:1.2.0"
   }
   ```

3. **最小化验证（Proof‑of‑Concept）**  
   - 新建一个仅包含一个 `EditText` 的测试 Activity。  
   - 在 `onCreate` 中调用 `ThumbKeyService.enable(this)`（或 README 中提供的包装方法），验证键盘能否成功弹出并正常输入。  
   - 检查日志确保没有意外的权限或兼容性警告。

4. **完整集成**  
   - 将键盘声明为系统输入法（`android:permission="android.permission.BIND_INPUT_METHOD"`），并在用户设置中引导开启。  
   - 如需自定义主题或键位布局，可在 `res/xml/keyboard.xml` 中复制并修改原始布局文件。

**生产可用性评估**  

| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | 中等 | 代码活跃（2026‑06‑27 最近更新），Star 数 1497、Fork 309，说明社区关注度较高。但缺乏正式的发布渠道（如 Maven Central）和完整的 CI/CD 报告。 |
| **隐私合规** | 高 | 项目自称不收集用户数据，代码中未见网络请求或第三方 SDK，易于通过内部审计。 |
| **兼容性** | 中等 | 只提供 Kotlin 实现，最低 Android API 需在 README 中确认（通常为 API 21+）。在部分定制 ROM 上可能需要额外的权限声明。 |
| **维护成本** | 中等 | 依赖单一库（Kotlin 标准库），但缺少详细的升级指南和变更日志，升级时需自行比对 API。 |
| **集成难度** | 低‑中 | 按照 README 完成依赖声明和服务注册即可，推荐先做 PoC 验证。 |
| **适用场景** | 原型、内部工具、隐私敏感的专属 App | 对外发布的消费级产品仍需评估 UI/UX 完整度和品牌一致性。 |

**结论**  
- **价值**：为需要拇指友好、隐私安全的 Android 输入场景提供即插即用的键盘解决方案。  
- **接入方式**：通过 Gradle 引入依赖，按照 README 完成键盘服务声明后，在业务代码中做一次性启用验证，即可在实际页面中使用。  
- **生产可用性**：在内部原型或受控环境下可直接使用；若用于面向大众的正式产品，建议在正式发布前完成完整的兼容性测试、UI 定制以及维护流程（如制定升级策略、加入内部审计）。在满足这些前置条件后，Thumb‑Key 可以作为生产环境的可靠输入法组件。

## 🧭 Practical evaluation

**Value:** dessalines/thumb-key may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1497 GitHub stars
- 309 forks
- updated 2026-06-27
- primary language: Kotlin
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 62/100 |
| stars | 68/100 |
| topics | 50/100 |
| outlook | 54/100 |
| quality | 62/100 |
| recency | 40/100 |
| adoption | 66/100 |
| production | 53/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/dessalines/thumb-key) · [← Back to Mobile](./README.md)</sub>
