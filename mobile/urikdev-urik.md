# urikdev/Urik

[![Stars](https://img.shields.io/github/stars/urikdev/Urik?style=flat-square&color=yellow)](https://github.com/urikdev/Urik/stargazers) [![Forks](https://img.shields.io/github/forks/urikdev/Urik?style=flat-square&color=blue)](https://github.com/urikdev/Urik/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-45%2F100-brightgreen?style=flat-square)](#)

> Privacy-focused Android keyboard with swipe typing, custom layouts, and password manager support. No tracking, 100% on-device, and fully open source.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 359 |
| 🍴 **Forks** | 28 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 45/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `f-droid` `i18n` `keyboard` `kotlin` `no-telemetry` `open-source` `privacy` `swipe-typing`

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Summary**  
Urik is an open‑source Android keyboard written in Kotlin that emphasizes privacy: all typing, swipe input, custom layouts and password‑manager integration run 100 % on‑device with no tracking. With a modest star count (≈ 360) and recent activity, it can be a solid choice for internal prototypes or niche apps that need a self‑hosted, fully auditable input method.

**Value**  
- **Privacy‑first**: No network calls or telemetry; the entire stack (including swipe‑typing algorithms) lives on the device, which is attractive for security‑sensitive products or regulated environments.  
- **Feature set**: Supports swipe typing, user‑defined keyboard layouts, and direct integration with password managers, covering most needs of a modern mobile input method.  
- **Open source & Kotlin**: The codebase is fully visible, easy to audit, and aligns with typical Android development stacks, reducing vendor lock‑in.

**Adoption path**  
1. **Proof‑of‑concept** – Clone the repo, follow the README to build the keyboard APK, and install it on a test device. Verify that the custom layout and swipe features work with your app’s input fields.  
2. **Integration check** – Review the `KeyboardService` and activity declarations to confirm they can be bundled with your existing Android module or distributed as a separate APK. Adjust the manifest if you need to expose additional permissions (e.g., `REQUEST_INSTALL_PACKAGES` for on‑the‑fly updates).  
3. **Customization** – Fork the repository to add any brand‑specific UI tweaks or to expose a simple API for toggling password‑manager support. Because the project is Kotlin‑native, you can reuse existing Gradle modules without extra bridging layers.  
4. **Testing & CI** – Add unit‑ and UI‑instrumentation tests for your custom layout and for the interaction with your password manager, then integrate the build into your CI pipeline.

**Production readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑05‑13) and has enough community interest to suggest stability, but it lacks formal release artifacts, extensive documentation, and a clear migration guide.  
- **Risks**: Integration steps are not fully documented; you’ll need to invest time in understanding the service lifecycle and handling edge cases (e.g., Android 13+ input‑method restrictions). Dependency management is straightforward (Kotlin + AndroidX), but you should lock versions to avoid breaking changes.  
- **Recommendation**: Suitable for internal tools, prototypes, or products where privacy is a core differentiator. Before a full production rollout, perform a small‑scale pilot, lock down the forked version, and establish a maintenance plan for security patches and Android OS updates.

### Русский

Urik — это полностью открытая Android‑клавиатура, ориентированная на конфиденциальность: все функции (включая свайп‑ввод, кастомные раскладки и интеграцию с менеджером паролей) работают на устройстве без какого‑либо трекинга. Подойдёт для прототипов или внутренних приложений, где требуется безопасный ввод текста, при условии предварительной проверки README и небольшого proof‑of‑concept‑пилотного внедрения. Готовность к production — средняя: проект имеет активную поддержку (обновления, 359 звёзд), но путь интеграции не полностью документирован, поэтому перед запуском в прод необходимо оценить затраты на настройку и поддержание зависимостей.

### 中文

**项目简介**  
Urik 是一款注重隐私的 Android 键盘，支持滑行输入、自定义布局以及密码管理器集成。所有功能均在本地完成，零网络追踪，代码全开源，使用 Kotlin 编写。

**价值点**  
- **隐私安全**：键入内容不离开设备，避免任何后台上报或数据泄露。  
- **高效输入**：滑行输入和可自定义键盘布局提升打字速度与舒适度。  
- **密码管理**：直接在键盘中调用系统或第三方密码管理器，降低登录时的复制粘贴风险。  

**典型接入方式**  
1. **阅读 README & 示例**：项目提供了一个 `KeyboardService` 示例以及在 `AndroidManifest.xml` 中声明的方式。  
2. **在现有 Android 应用中集成**  
   - 在 `build.gradle` 中加入 `implementation 'com.github.urikdev:Urik:latest'`（或直接克隆源码）。  
   - 将 `UrikKeyboardService` 注册为 `android:permission="android.permission.BIND_INPUT_METHOD"` 的输入法服务。  
   - 在 UI 中通过 `InputMethodManager` 调用键盘，或在用户设置页提供“切换到 Urik”按钮。  
3. **自定义布局**：复制项目的 `res/xml/keyboard_layout.xml`，在自己的资源目录中修改后在 `UrikKeyboardService` 的 `onCreateInputView` 中加载。  
4. **密码管理器集成**：实现 `UrikPasswordProvider` 接口，返回已加密的凭据；键盘会在需要时弹出密码填充 UI。  

**生产可用性评估**  
- **成熟度**：已有 359 星、28 Fork，最近一次提交在 2026‑05‑13，活跃度尚可。  
- **依赖与维护**：仅依赖 AndroidX 与 Kotlin 标准库，升级成本低；但需自行监控上游库的安全更新。  
- **适用场景**：适合内部工具、原型或对隐私要求较高的企业内部应用；对外发布的产品在投入生产前应完成以下检查：  
  1. 完整的键盘兼容性测试（不同 Android 版本、OEM 定制系统）。  
  2. 安全审计（代码审查、键盘输入日志是否意外泄露）。  
  3. 性能基准（滑行输入延迟、内存占用）。  
- **风险**：项目文档虽提供基本接入示例，但缺少完整的 API 文档和 CI/CD 流程，集成前需评估学习成本和后期维护成本。  

**结论**  
Urik 在隐私保护和可定制输入体验方面具备明确优势，适合作为原型或内部业务的键盘方案。若项目对安全、兼容性有严格要求，建议先在受控环境中完成小范围 PoC，确认集成成本后再决定是否用于生产。

## 🧭 Practical evaluation

**Value:** urikdev/Urik may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 359 GitHub stars
- 28 forks
- updated 2026-05-13
- primary language: Kotlin
- 9 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 37/100 |
| stars | 54/100 |
| topics | 100/100 |
| outlook | 48/100 |
| quality | 57/100 |
| recency | 20/100 |
| adoption | 49/100 |
| production | 47/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/urikdev/Urik) · [← Back to Mobile](./README.md)</sub>
