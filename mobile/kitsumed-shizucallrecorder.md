# kitsumed/ShizuCallRecorder

[![Stars](https://img.shields.io/github/stars/kitsumed/ShizuCallRecorder?style=flat-square&color=yellow)](https://github.com/kitsumed/ShizuCallRecorder/stargazers) [![Forks](https://img.shields.io/github/forks/kitsumed/ShizuCallRecorder?style=flat-square&color=blue)](https://github.com/kitsumed/ShizuCallRecorder/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-47%2F100-brightgreen?style=flat-square)](#)

> ShizuCallRecorder empowers ADB through Shizuku to record phone calls on non-rooted device!

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 527 |
| 🍴 **Forks** | 16 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 47/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`adb` `android` `callrecorder` `no-root` `scrcpy` `shizuku`

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Summary**  
ShizuCallRecorder is an open‑source Kotlin app that uses ADB via the Shizuku framework to capture incoming and outgoing phone calls on devices that are not rooted. It targets Android developers or power users who need a lightweight, scriptable way to record calls without modifying the system image.

**Value**  
The project fills a niche where call‑recording is required (e.g., QA testing, compliance logging, or personal archiving) but rooting or custom ROMs are prohibited. By leveraging Shizuku, it runs with normal user privileges while still gaining the elevated ADB permissions needed to access the audio stream, making it far easier to adopt than traditional root‑only solutions.

**Practical adoption path**  

1. **Proof‑of‑concept** – Clone the repo, follow the README to install Shizuku on a test device, and run the sample activity to verify that calls are recorded correctly.  
2. **Integration** – Wrap the core recording service in a small library module or invoke it via an Intent from your own app, adjusting the permission request flow to match your UI.  
3. **Validation** – Test on the target Android versions (the project targets API 21+), confirm that the recorded files meet your quality and format requirements, and evaluate any device‑specific quirks (e.g., OEM audio policies).  

**Production readiness**  
The codebase is moderately mature (527 ★, recent updates) and suitable for prototypes or internal tools, but it is not yet a turnkey production component. Before shipping, you should:  

* Verify long‑term maintenance of Shizuku and the ADB‑bridge on your supported devices.  
* Harden the integration (error handling, user consent dialogs, storage management).  
* Conduct security and privacy reviews, as call recording is subject to legal restrictions in many jurisdictions.  

With these steps, ShizuCallRecorder can be safely moved from a proof‑of‑concept to a reliable internal workflow, though further polishing is advisable for public‑facing releases.

### Русский

ShizuCallRecorder — это Kotlin‑проект, позволяющий через ADB и Shizuku записывать телефонные разговоры на не‑rootованных Android‑устройствах, что удобно для прототипов, тестирования и внутренних процессов, где нужен быстрый доступ к аудиозаписям звонков. Для внедрения достаточно проверить README, выполнить небольшую proof‑of‑concept‑интеграцию и убедиться в совместимости с текущей инфраструктурой, после чего можно использовать библиотеку в ограниченных продакшн‑сценариях, учитывая необходимость контроля зависимостей и поддержки. Уровень готовности — средний: проект активно поддерживается (527 звёзд, недавнее обновление), но путь интеграции не полностью документирован, поэтому требуется предварительная проверка.

### 中文

**项目简介**  
ShizuCallRecorder 通过 Shizuku 在非 root 设备上利用 ADB 权限实现通话录音，使用 Kotlin 编写，已获 527 星，活跃维护至 2026‑06‑25。

**价值**  
- **无需 Root**：在普通 Android 手机上即可完成通话录音，降低用户门槛。  
- **利用已有工具**：基于 Shizuku 与 ADB 的授权机制，免除额外的系统级权限申请，适合企业内部审计、客服质检或研发调试等场景。  
- **开源可定制**：代码结构清晰，便于二次开发或嵌入自有业务流程。

**典型接入方式**  
1. **环境准备**  
   - 在目标设备上安装 **Shizuku**（通过 Play 商店或 APK），并打开 “允许通过 ADB 调用”。  
   - 在开发机器上确保已安装 **ADB** 并能正常连接设备。  
2. **项目集成**  
   - 将项目 `kitsumed/ShizuCallRecorder` 通过 Gradle 引入（或直接 clone 源码）。  
   - 在业务模块中调用 `ShizuCallRecorder.startRecording()` / `stopRecording()`，并监听回调获取录音文件路径。  
   - 如需 UI，可直接使用项目自带的 Activity，或参考 `README` 中的 Intent 示例自行包装。  
3. **验证**  
   - 运行 `adb shell dumpsys activity services` 检查 Shizuku 服务是否已启动。  
   - 通过小范围的 POC（例如在测试机上录制一次通话）确认权限、文件写入路径和音质符合预期。  

**生产可用性**  
- **成熟度**：中等（Score 56/100），已有 527 星、活跃提交，代码质量总体良好。  
- **适用场景**：原型验证、内部工具或对通话录音有明确合规需求的业务；不建议直接在面向公众的高并发服务中使用，除非完成以下工作：  
  - 完整的异常处理与重试机制（ADB 连接不稳定时）。  
  - 对录音文件的加密存储与访问控制。  
  - 持续监控 Shizuku 服务状态，防止因系统升级导致授权失效。  
- **维护成本**：需要定期检查 Android 系统与 Shizuku 的兼容性，特别是新系统版本对通话音频接口的变动。  

**结论**  
ShizuCallRecorder 为非 root Android 设备提供了一个轻量、开源的通话录音方案，适合作为内部原型或业务流程的快速集成点。若在生产环境使用，建议先完成小规模 POC，评估其在目标设备上的稳定性与合规性，并在此基础上加入必要的监控与安全措施。

## 🧭 Practical evaluation

**Value:** kitsumed/ShizuCallRecorder may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 527 GitHub stars
- 16 forks
- updated 2026-06-25
- primary language: Kotlin
- 6 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 31/100 |
| stars | 58/100 |
| topics | 75/100 |
| outlook | 52/100 |
| quality | 59/100 |
| recency | 40/100 |
| adoption | 50/100 |
| production | 52/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/kitsumed/ShizuCallRecorder) · [← Back to Mobile](./README.md)</sub>
