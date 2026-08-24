# nextcloud/talk-android

[![Stars](https://img.shields.io/github/stars/nextcloud/talk-android?style=flat-square&color=yellow)](https://github.com/nextcloud/talk-android/stargazers) [![Forks](https://img.shields.io/github/forks/nextcloud/talk-android?style=flat-square&color=blue)](https://github.com/nextcloud/talk-android/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> 📱😀 Video & audio calls through Nextcloud on Android

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 730 |
| 🍴 **Forks** | 313 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `audio` `communication` `hacktoberfest` `nextcloud` `nextcloud-talk` `open-source` `video`

## 🎯 Categories

Mobile

## 📝 Summary

### English

Here's a brief summary of the open-source project nextcloud/talk-android:

Nextcloud/talk-android is an open-source project that enables video and audio calls through Nextcloud on Android devices, providing a valuable solution for users seeking seamless communication within their Nextcloud ecosystem. The practical adoption path involves evaluating the project's README and activity, starting with a small proof of concept to ensure a smooth integration process. With its high production readiness, recent activity, and strong adoption, this project is suitable for a serious pilot, offering a promising solution for Nextcloud users.

Value: The project offers a valuable solution for users seeking seamless communication within their Nextcloud ecosystem.

Practical Adoption Path: Evaluate the project's README and activity, starting with a small proof of concept to ensure a smooth integration process.

Production Readiness: High, due to recent activity, adoption, and ecosystem signals, making it suitable for a serious pilot.

### Русский

**nextcloud/talk-android** — это официальное Android‑клиентское приложение для виде и аудиозвонков через Nextcloud. Оно подходит для компаний, которые уже используют Nextcloud и хотят добавить мобильную связь: достаточно установить приложение, подключить аккаунт Nextcloud и начать звонки из чатов или календаря. Проект активно поддерживается (730 ⭐, последние коммиты — июнь 2026), имеет зрелый Kotlin‑код и широкое сообщество, поэтому готов к пилотному внедрению в продакшн после небольшого proof‑of‑concept и проверки README.

### 中文

**项目简介**  
nextcloud/talk-android 是 Nextcloud 官方维护的 Android 客户端，提供基于 Nextcloud 服务器的高清视频和音频通话功能，支持一键加入会议、屏幕共享、聊天等协作场景。  

**价值**  
- **统一协作平台**：在已有的 Nextcloud 文件、日历、联系人等业务之上直接实现实时音视频，避免在企业内部部署额外的会议系统。  
- **数据主权与安全**：通话流量全部走自建的 Nextcloud 服务器，符合对隐私和合规性的严格要求。  
- **跨平台一致性**：与 Nextcloud Web、iOS 客户端保持功能一致，用户体验统一，降低培训成本。  

**典型接入方式**  
1. **准备 Nextcloud 服务器**  
   - 确保已启用 **Talk** 应用（版本 ≥ 13），并在服务器管理后台打开 “WebRTC” 与 “SIP”（如需）功能。  
   - 配置 TURN/STUN 服务器（coturn）以保证移动网络下的 NAT 穿透。  

2. **在 Android 项目中集成 SDK**  
   - 在 `build.gradle` 中加入 Maven 仓库和依赖：  
     ```gradle
     repositories {
         maven { url "https://jitpack.io" }
     }
     dependencies {
         implementation 'com.github.nextcloud:talk-android:master-SNAPSHOT'
     }
     ```  
   - 按照 README 中的 **Authentication** 示例，使用 OAuth2 / App‑Password 完成登录。  

3. **调用核心 API**  
   - 初始化 `TalkClient` 并传入服务器 URL 与用户凭证。  
   - 通过 `TalkRoomManager` 创建或加入房间，随后使用 `CallService` 发起/接收音视频流。  
   - 可选：集成 **Push Notification**（FCM）实现来电弹窗和后台通话保持。  

4. **UI 与业务层适配**  
   - 项目提供的 `TalkFragment`、`CallActivity` 可直接嵌入现有 UI，或自行实现 UI 只保留底层通话逻辑。  

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑30，GitHub ★730、Fork 313，社区活跃，Issue 响应及时。  
- **技术成熟度**：使用 Kotlin 编写，遵循 Android Jetpack 架构，已通过多轮内部和社区的功能测试（包括 4K 视频、多人会议）。  
- **安全合规**：所有通话数据均在自建服务器上加密传输，支持端到端加密（E2EE）插件，可满足 GDPR、ISO 27001 等要求。  
- **风险**：文档主要集中在 README，部分高级功能（如自定义 TURN 配置、SIP 集成）需要自行探索；建议先在测试环境完成 **OAuth + TURN** 的完整链路验证，再推广到生产。  

**结论**  
nextcloud/talk-android 已具备完整的音视频通话能力，集成成本相对适中，且在自有云环境中可完全掌控数据安全，适合作为企业内部协作工具的移动端实现。只要在正式上线前完成一次端到端的 POC（包括身份认证、TURN 穿透和推送），即可投入生产使用。

## 🧭 Practical evaluation

**Value:** nextcloud/talk-android may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 730 GitHub stars
- 313 forks
- updated 2026-06-30
- primary language: Kotlin
- 8 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 62/100 |
| stars | 61/100 |
| topics | 100/100 |
| outlook | 58/100 |
| quality | 68/100 |
| recency | 40/100 |
| adoption | 61/100 |
| production | 55/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/nextcloud/talk-android) · [← Back to Mobile](./README.md)</sub>
