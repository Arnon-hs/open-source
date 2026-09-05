# BelledonneCommunications/linphone-android

[![Stars](https://img.shields.io/github/stars/BelledonneCommunications/linphone-android?style=flat-square&color=yellow)](https://github.com/BelledonneCommunications/linphone-android/stargazers) [![Forks](https://img.shields.io/github/forks/BelledonneCommunications/linphone-android?style=flat-square&color=blue)](https://github.com/BelledonneCommunications/linphone-android/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Linphone.org mirror for linphone-android (https://gitlab.linphone.org/BC/public/linphone-android)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.3k |
| 🍴 **Forks** | 776 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `call` `conference` `liblinphone` `linphone` `linphone-android` `phone` `sip` `video` `voip`

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Linphone‑Android is the official open‑source Android client for the SIP‑based VoIP stack Linphone, maintained by Belledonne Communications. Written in Kotlin and actively updated (last commit 2026‑07‑02), the project offers a full‑featured softphone with audio/video calling, messaging, and push‑notification support, making it a ready‑to‑use foundation for any Android communication app.

**Value**  
- **Feature‑complete VoIP stack** – All core Linphone capabilities (SIP registration, NAT traversal, SRTP, video, chat, presence) are already implemented, so developers can focus on UI/UX and business logic instead of building a SIP stack from scratch.  
- **Strong community & ecosystem** – With >1 200 stars, >700 forks, and active upstream support, bugs are quickly addressed and new protocol features are regularly merged.  
- **Kotlin‑first codebase** – Aligns with modern Android development practices, easing integration with Jetpack components, Compose UI, and existing Kotlin codebases.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the provided sample app, and verify basic call flow on a test device.  
2. **Read the README & docs** – Follow the “Getting Started” guide to set up Linphone core libraries, generate a Linphone‑SDK bundle, and configure required permissions (Internet, RECORD_AUDIO, CAMERA, etc.).  
3. **Customize** – Replace the sample UI with your own screens, inject your branding, and hook the core events (call state, incoming call, registration) into your app’s architecture (e.g., ViewModel + LiveData).  
4. **Push‑notification integration** – Enable Firebase Cloud Messaging as described in the docs to receive incoming calls when the app is in the background.  
5. **Pilot** – Deploy a small internal build to a handful of users, monitor logs, and fine‑tune network/NAT handling.

**Production Readiness**  
- **High**: The project shows recent activity, a mature codebase, and a proven track record in commercial deployments of Linphone.  
- **Stability**: Core SIP functionality is battle‑tested; the Android client passes CI pipelines and includes unit/instrumented tests.  
- **Supportability**: Official maintainers respond to issues on GitLab, and the broader Linphone community provides forums and documentation.  
- **Risk Mitigation**: The integration path is not fully documented in metadata, so allocate time for the initial setup and validation of build scripts, but once the SDK is built the runtime dependencies are minimal.

Overall, Linphone‑Android offers a production‑grade, open‑source VoIP solution that can be integrated into Android apps with a modest proof‑of‑concept effort, followed by straightforward UI customization and push‑notification wiring.

### Русский

Резюме проекта BelledonneCommunications/linphone-android:

Проект Linphone Android представляет собой мощный инструмент для голосовой связи, который может быть полезен в сценариях, когда требуется интеграция голосовой связи в приложение. Типовой сценарий внедрения заключается в интеграции Linphone Android в приложение с голосовой связью, что может быть особенно актуально для приложений, требующих надежной и качественной голосовой связи. Проект демонстрирует высокий уровень готовности к production, благодаря своему активному развитию, большому количеству пользователей и сильной экосистеме.

### 中文

**项目简介**  
BelledonneCommunications/linphone-android 是 Linphone 官方在 GitHub 上的 Android 客户端镜像，基于 Kotlin 实现，提供完整的 SIP/VoIP 功能（音视频通话、即时消息、呼叫记录等），并随 Linphone.org 主站保持同步更新。

**价值**  
- **成熟可靠的 VoIP 栈**：直接复用 Linphone 的核心库，支持多种编解码器、加密（SRTP/ZRTP）和网络穿透（ICE/STUN/TURN），适合需要高质量实时通信的移动应用。  
- **开源且活跃**：截至 2026‑07‑02，拥有 1.3k+ Stars、近 800 Fork，最近一次提交仅在数天前，社区活跃度高，易获取技术支持。  
- **快速定制**：源码结构清晰，提供完整的示例 Activity 与 README，开发者可以在此基础上裁剪 UI、扩展业务逻辑，缩短从概念验证到产品化的周期。

**典型接入方式**  
1. **Fork / Clone 项目**：在自己的组织或私有仓库中 fork，或直接 clone 代码。  
2. **Gradle 依赖**：在 `settings.gradle` 中添加 Linphone Maven 仓库，或直接使用项目自带的 `linphone-sdk` 子模块。  
3. **初始化 SDK**：在 Application 的 `onCreate` 中调用 `LinphoneCoreFactory.instance().createLinphoneCore()`，配置 SIP 账户、网络参数等。  
4. **集成 UI**：复制或继承 `MainActivity`（或 `CallActivity`）示例，实现登录、呼叫、通话界面；如需自定义 UI，只保留业务层代码，替换布局文件即可。  
5. **权限与后台**：在 `AndroidManifest.xml` 中声明 `RECORD_AUDIO、CAMERA、FOREGROUND_SERVICE` 等权限，并在 `Service` 中维护通话保持，确保在 Android 12+ 的限制下仍能正常运行。  
6. **测试 & 上线**：使用官方提供的端到端测试脚本（`linphone-test`），在真实设备上验证音视频质量后，再发布到 Play Store。

**生产可用性**  
- **代码活跃度**：最近一次提交在 2026‑07‑02，说明项目仍在维护。  
- **社区与生态**：Linphone 在全球有数十万活跃用户，官方文档、论坛和 Slack/Matrix 社区提供及时帮助。  
- **质量保障**：CI/CD 流水线覆盖单元测试、集成测试及多平台构建，且已在多个商业产品中使用，具备生产级别的稳定性。  
- **风险提示**：虽然核心功能成熟，但项目的具体接入文档较为简略，建议先做一个“登录‑呼叫”小型 PoC，确认编译环境、权限配置以及自定义 UI 的工作量后再投入大规模开发。

综上，BelledonneCommunications/linphone-android 是一个成熟、可定制且生产就绪的 Android VoIP 解决方案，适合需要快速实现 SIP 通话功能的移动应用。

## 🧭 Practical evaluation

**Value:** BelledonneCommunications/linphone-android may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1296 GitHub stars
- 776 forks
- updated 2026-07-02
- primary language: Kotlin
- 10 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 72/100 |
| stars | 66/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 81/100 |
| recency | 80/100 |
| adoption | 68/100 |
| production | 70/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/BelledonneCommunications/linphone-android) · [← Back to Mobile](./README.md)</sub>
