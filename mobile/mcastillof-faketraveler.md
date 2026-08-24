# mcastillof/FakeTraveler

[![Stars](https://img.shields.io/github/stars/mcastillof/FakeTraveler?style=flat-square&color=yellow)](https://github.com/mcastillof/FakeTraveler/stargazers) [![Forks](https://img.shields.io/github/forks/mcastillof/FakeTraveler?style=flat-square&color=blue)](https://github.com/mcastillof/FakeTraveler/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-46%2F100-brightgreen?style=flat-square)](#)

> Fake where your phone is located (Mock location for Android).

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.3k |
| 🍴 **Forks** | 165 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 46/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android-application` `fake-locations` `floss` `mock-locations` `opensource`

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
FakeTraveler (mcastillof/FakeTraveler) is an open‑source Android app that lets you spoof the device’s GPS location, enabling developers and testers to simulate any point on the globe. With a solid community backing (1.2 k ★, 165 forks) and recent updates, it can be a handy tool for prototyping location‑based features or internal QA workflows.

**Value**  
- **Rapid testing of location‑dependent functionality** – you can verify maps, geofencing, location‑aware UI, and backend services without leaving the lab or using physical devices in the field.  
- **Cost‑effective prototyping** – eliminates the need for multiple devices or expensive location‑simulation hardware.  
- **Open‑source flexibility** – the code can be extended or integrated into custom test suites, CI pipelines, or internal tooling.

**Practical adoption path**  

| Step | Action | Goal |
|------|--------|------|
| 1️⃣  | **Clone & read the README** – confirm the build instructions (Android Studio/Gradle) and required permissions. | Verify that the project can be built on your current Android SDK version. |
| 2️⃣  | **Run a small proof‑of‑concept** – install the APK on a test device or emulator, enable mock locations, and set a sample coordinate. | Ensure the mock‑location API works and that the UI matches your workflow. |
| 3️⃣  | **Integrate into your test harness** – wrap the command‑line build or use the library (if exposed) in your automated UI tests (e.g., Espresso, UIAutomator). | Automate location changes as part of CI/CD pipelines. |
| 4️⃣  | **Validate maintenance** – check the issue tracker, pull‑request activity, and compatibility with the latest Android versions (target SDK 34+). | Assess long‑term sustainability before moving to production. |
| 5️⃣  | **Security & policy review** – confirm that using mock locations complies with your organization’s security policies and that no sensitive data is exposed. | Clear any compliance hurdles. |

**Production readiness** – **Medium**. The project is mature enough for internal prototypes and QA environments, but it lacks formal documentation for large‑scale integration and its mock‑location implementation may need adaptation for newer Android restrictions (e.g., background location limits). Before committing to production, perform the PoC, verify compatibility with your target Android version, and put a maintenance plan in place (e.g., fork and keep a custom branch).

### Русский

FakeTraveler — это open‑source приложение для Android, позволяющее подменять GPS‑координаты телефона, что удобно для тестирования гео‑зависимых функций, разработки прототипов и внутреннего использования (например, проверка рекламных кампаний или отладка карт). Для внедрения рекомендуется сначала изучить README, собрать небольшой proof‑of‑concept и убедиться, что зависимости (JavaScript‑ядро, Android‑SDK) совместимы с вашим стеком, после чего можно интегрировать модуль в CI‑тесты или внутренние билды. Готовность к production — средняя: проект имеет активную звёздную базу (1284 ★) и недавнее обновление, но путь интеграции не полностью документирован, поэтому требуется дополнительная проверка перед запуском в продакшн.

### 中文

**项目简介（2‑3 句）**  
FakeTraveler 是一款 Android 平台的“假位置”工具，能够在手机上模拟任意 GPS 坐标，实现伪造当前位置的功能。它提供了简洁的 UI 与 API，适合在调试、演示或内部测试时快速切换位置。

**价值**  
- **快速定位调试**：开发者可以在不更改真实 GPS 的情况下，立刻验证基于位置的业务逻辑（如地图、位置推送、地理围栏等）。  
- **隐私保护与演示**：在需要隐藏真实位置或在演示环境中展示特定场景时，提供安全、可控的替代方案。  
- **原型验证**：产品经理和设计师可用它快速验证基于位置的交互原型，缩短迭代周期。

**典型接入方式**  
1. **阅读 README 与示例**：先确认项目的安装步骤（通常是通过 `adb` 安装 APK 或在 Android Studio 中导入源码）。  
2. **集成到现有项目**：在需要模拟位置的模块中，调用其公开的 Intent 或广播接口（如 `com.fake.traveler.SET_LOCATION`），传入经纬度。  
3. **小范围验证**：在本地设备或 CI 环境中写一个最小化的 proof‑of‑concept（PoC），验证能够成功更改系统位置并被目标 App 读取。  
4. **自动化脚本**：如果需要在测试流水线中使用，可编写 shell/Gradle 脚本，利用 `adb shell` 命令触发位置切换，实现持续集成测试。

**生产可用性评估**  
- **成熟度**：项目已有 1284 星、165 次 Fork，且最近一次提交在 2026‑05‑14，表明社区活跃度尚可。  
- **适用场景**：更适合作为 **原型、内部测试或演示** 环境的工具；不建议直接在面向终端用户的生产 App 中使用，主要因为：  
  - 需要系统级权限（Mock location）并可能受到 Android 安全策略限制。  
  - 依赖的 JavaScript 代码与原生模块的兼容性需自行验证。  
- **集成成本**：集成路径并未在元数据中明示，需通过 README 与源码确认具体 API 与权限要求。建议先在沙箱环境完成 PoC，评估以下因素后再决定是否投入生产：  
  1. **权限管理**：是否能在目标设备上安全获取 `android.permission.ACCESS_MOCK_LOCATION`。  
  2. **维护频率**：项目的更新频率与社区响应速度，以确保后续 Android 版本兼容。  
  3. **依赖安全**：审查项目的第三方依赖（尤其是 JavaScript 包）是否存在已知漏洞。  

**结论**  
FakeTraveler 在 **原型验证、内部测试和演示** 场景下价值突出，接入方式相对直接但需先完成小规模验证。若业务对位置伪造有严格的合规或安全要求，建议在生产环境中采用更成熟、官方支持的 Mock Location 方案或自行实现受控的定位模拟。

## 🧭 Practical evaluation

**Value:** mcastillof/FakeTraveler may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1284 GitHub stars
- 165 forks
- updated 2026-05-14
- primary language: JavaScript
- 5 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 56/100 |
| stars | 66/100 |
| topics | 63/100 |
| outlook | 47/100 |
| quality | 58/100 |
| recency | 20/100 |
| adoption | 63/100 |
| production | 47/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/mcastillof/FakeTraveler) · [← Back to Mobile](./README.md)</sub>
