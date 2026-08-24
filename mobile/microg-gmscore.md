# microg/GmsCore

[![Stars](https://img.shields.io/github/stars/microg/GmsCore?style=flat-square&color=yellow)](https://github.com/microg/GmsCore/stargazers) [![Forks](https://img.shields.io/github/forks/microg/GmsCore?style=flat-square&color=blue)](https://github.com/microg/GmsCore/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Free implementation of Play Services

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 13.8k |
| 🍴 **Forks** | 2.9k |
| 💻 **Language** | Java |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `auth` `cloud-messaging` `firebase` `geolocation` `google` `google-cloud-messaging` `java` `kotlin` `kotlin-android` `maps` `microg`

## 🎯 Categories

Mobile · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
microg / GmsCore is an open‑source, Java‑based reimplementation of Google Play Services that lets Android apps run without the proprietary Google stack. With over 13 k stars and recent commits, it can be leveraged to add or replace authentication, location, and privacy‑focused services while giving developers tighter control over security checks.  

**Value**  
- **Security & privacy:** By replacing Google’s closed‑source components, you can enforce custom security policies, audit data flows, and eliminate unwanted telemetry.  
- **Cost & flexibility:** Removes the need for Google Play licensing and allows the same APIs to be used on devices that lack Google Play Services (e.g., custom ROMs, IoT, or enterprise‑managed phones).  
- **Community & ecosystem:** A large contributor base, many forks, and active issue resolution make it a reliable source of updates and bug fixes.  

**Practical Adoption Path**  
1. **Read the README & documentation** – verify that the required Play‑Services APIs (e.g., Location, SafetyNet, Auth) are covered by the current GmsCore version.  
2. **Proof‑of‑concept (PoC):** Create a minimal Android app that switches its `com.google.android.gms` implementation to microG via the “microG Services Core” app or by bundling the library directly. Test the specific APIs you need (e.g., sign‑in, push, location).  
3. **Security review:** Run static analysis on the microG codebase and perform a dependency‑check scan to confirm no known vulnerabilities.  
4. **Integration:** Replace the Play‑Services dependency in your Gradle files with the microG artifact, adjust the manifest (add the required permissions and the `microg` service declarations), and configure the device to use microG as the default provider.  
5. **Pilot rollout:** Deploy the updated app to a controlled group of devices (internal test lab or staged production) and monitor logs for API failures or performance regressions.  

**Production Readiness**  
- **Activity:** The repository shows recent commits (as of 2026‑06‑29) and a healthy fork/star ratio, indicating ongoing maintenance.  
- **Maturity:** microG has been used in numerous custom ROMs (e.g., LineageOS, GrapheneOS) and large‑scale community projects, demonstrating real‑world stability.  
- **Risk considerations:** No immediate licensing conflicts (Apache‑2.0) or critical CVEs are reported, but a final security audit and verification of maintainers’ responsiveness are advisable before full‑scale deployment.  

Overall, microg / GmsCore is production‑ready for pilots, especially where control over authentication, privacy, or device independence from Google Play Services is a priority. A small PoC followed by a staged rollout will validate compatibility and allow you to assess any edge‑case issues before committing to a full release.

### Русский

Резюме:

microg/GmsCore - бесплатная реализация Play Services, предназначенная для укрепления безопасности и добавления функций аутентификации и конфиденциальности в мобильных приложениях. Этот проект может быть полезен в сценарии, когда README и активность проекта соответствуют конкретному рабочему процессу. microg/GmsCore готов к использованию в production, поскольку за ним следят активные разработчики, и он пользуется популярностью в сообществе, но требует тщательного обзора лицензии, безопасности и состояний поддержки.

### 中文

**项目简介**  
microg/GmsCore 是一个开源的、兼容 Google Play Services 的实现，提供了位置、身份验证、推送等核心 API，帮助在没有官方 Play Services 的环境中运行 Android 应用。  

**价值**  
- **安全与隐私**：可自行控制授权流程和数据上报，避免向 Google 服务器泄露敏感信息。  
- **灵活性**：在定制 ROM、AOSP 设备或受限网络环境下仍能使用 Play‑Services‑依赖的功能。  
- **成本**：无需购买 Google Play 认证或订阅服务，降低企业运营费用。  

**典型接入方式**  
1. **阅读 README 与示例**：确认项目的 API 与目标功能（如位置、GCM、SafetyNet）匹配。  
2. **小范围 PoC**：在测试设备上通过 Gradle 引入 `org.microg.gms:play-services-base`（或对应模块），并在 `AndroidManifest.xml` 中声明 `org.microg.gms` 服务。  
3. **验证兼容性**：运行应用的关键功能，检查日志是否有 `microG` 的初始化信息，确保没有未实现的 API 报错。  
4. **逐步扩展**：在 PoC 通过后，将 microG 作为系统组件（如在自建 ROM 中预装）或通过 `microg` 的 UI 启动器进行管理。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑29 最近一次提交，拥有 13 753 星、2 909 次 fork，社区活跃。  
- **成熟度**：核心模块已在多个自定义 ROM（LineageOS、Pixel Experience 等）以及企业内部项目中实战部署，具备生产级别的稳定性。  
- **风险**：需进一步审查许可证（GPL‑v3）对商业闭源代码的影响，并进行安全审计以确认未引入供应链漏洞。  
- **总体评估**：在完成许可证和安全审查后，可视为 **高可用** 的 OSS 组件，用于需要替代或补强 Google Play Services 的生产环境。

## 🧭 Practical evaluation

**Value:** microg/GmsCore may be useful when its README and activity match a concrete workflow.

**Best use cases**

- strengthen security checks
- add auth or privacy controls

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 13753 GitHub stars
- 2909 forks
- updated 2026-06-29
- primary language: Java
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 87/100 |
| stars | 88/100 |
| topics | 100/100 |
| outlook | 64/100 |
| quality | 79/100 |
| recency | 40/100 |
| adoption | 88/100 |
| production | 62/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/microg/GmsCore) · [← Back to Mobile](./README.md)</sub>
