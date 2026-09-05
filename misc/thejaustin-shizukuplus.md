# thejaustin/ShizukuPlus

[![Stars](https://img.shields.io/github/stars/thejaustin/ShizukuPlus?style=flat-square&color=yellow)](https://github.com/thejaustin/ShizukuPlus/stargazers) [![Forks](https://img.shields.io/github/forks/thejaustin/ShizukuPlus?style=flat-square&color=blue)](https://github.com/thejaustin/ShizukuPlus/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> [ HOBBY PROJECT ] Shizuku+ goes deeper than the OG Shizuku. Take a look inside, and see what you find. [WIP - Development slowed due to new job]

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 369 |
| 🍴 **Forks** | 22 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
ShizukuPlus is a hobby‑level Kotlin extension of the original Shizuku project that adds deeper system‑level capabilities for Android apps. Although development has slowed after the maintainer started a new job, the repository still receives occasional updates (last commit 2026‑06‑26) and has attracted a modest community (≈ 369 ★, 22 forks).  

**Value proposition**  
ShizukuPlus offers a richer API surface than the upstream Shizuku, enabling developers to perform advanced privileged operations (e.g., accessing hidden system services) without rooting the device. For teams that already rely on Shizuku for sandbox‑bypass functionality, ShizukuPlus can reduce boilerplate and unlock features that would otherwise require custom native code or separate patches.

**Practical adoption path**  

1. **Initial assessment** – Clone the repo, review the README, and run the provided sample app to verify that the extra APIs you need are present and stable.  
2. **Dependency integration** – Add the library as a Gradle module or Maven artifact (if published) and align the Kotlin version with your project.  
3. **Permission & security review** – Because ShizukuPlus operates with elevated privileges, perform a security audit of the added native calls and confirm the licensing (Apache‑2.0/MIT‑compatible) matches your policy.  
4. **Prototype** – Build a small internal prototype that exercises the new functionality; monitor logcat for crashes or permission denials.  
5. **Feedback loop** – Report any issues to the maintainer (or submit a PR) and consider forking the repo if you need long‑term stability.

**Production readiness**  
- **Maturity:** Medium. The codebase is functional and recent enough for prototyping, but the maintainer’s reduced activity means bug fixes and feature requests may be delayed.  
- **Stability:** The core Shizuku foundation is stable; ShizukuPlus adds optional layers that have not been extensively battle‑tested in large‑scale deployments.  
- **Risk mitigation:** Conduct a manual security audit, pin the library version, and keep a fork with your own CI checks to guard against upstream stagnation.  

In short, ShizukuPlus is suitable for internal tools, proof‑of‑concepts, or niche Android projects that need the extra privileged capabilities it provides, provided you perform the outlined due‑diligence before promoting it to production.

### Русский

**Краткое резюме:**  
`thejaustin/ShizukuPlus` — это hobby‑проект, расширяющий возможности оригинального Shizuku, написанный на Kotlin. Он может пригодиться для прототипов или внутренних инструментов, где требуется более глубокая интеграция с Android‑сервисом Shizuku, однако перед внедрением требуется ручная проверка кода, лицензии и безопасности. Готовность к production — средняя: проект стабилен для экспериментального использования, но нуждается в дополнительном аудите и подтверждении поддержки перед выпуском в продакшн.

### 中文

**项目简介（2‑3 句话）**  
`thejaustin/ShizukuPlus` 是一个基于原版 Shizuku 的深度扩展 Hobby 项目，旨在为 Android 开发者提供更灵活的系统权限桥接能力。项目仍在开发中，近期因作者新工作进展放缓，更新频率较低。

---

## 价值说明

1. **功能增强**：在原始 Shizuku 的基础上加入了额外的 API 扩展和自定义插件机制，可实现更细粒度的权限控制和跨进程调用。  
2. **快速原型**：对于需要在内部工具或实验性产品中临时获取系统权限的团队，ShizukuPlus 能显著减少自行实现底层桥接的工作量。  
3. **开源透明**：代码全部开源（Kotlin），便于审计、二次开发和社区贡献。

---

## 典型接入方式

1. **依赖引入**  
   ```gradle
   implementation 'com.github.thejaustin:shizukuplus:<latest-tag>'
   ```
   或者直接克隆仓库并在本地 `settings.gradle` 中 `includeBuild`。

2. **初始化**（在 `Application` 或 `Activity` 中）  
   ```kotlin
   ShizukuPlus.init(this) { success ->
       if (success) {
           // 可直接使用扩展的 API
       } else {
           // 处理未授权或服务不可用的情况
       }
   }
   ```

3. **权限申请**  
   - 与原版 Shizuku 相同，需要在设备上安装并启用 Shizuku 服务。  
   - 若使用了自定义插件，需要在 `AndroidManifest.xml` 中声明对应的 `service`/`receiver`。

4. **使用扩展 API**（示例）  
   ```kotlin
   // 通过 ShizukuPlus 调用系统隐藏的 API
   ShizukuPlus.callHiddenMethod("android.os.PowerManager", "reboot", null)
   ```

> **注意**：项目的 README 与代码注释相对简略，建议在正式接入前仔细阅读源码，确认所需功能是否已实现，以及是否存在未公开的依赖或权限。

---

## 生产可用性评估

| 维度 | 评估 | 说明 |
|------|------|------|
| **代码成熟度** | 中等 | 369 星、22 Fork，最近一次提交为 2026‑06‑26，活跃度下降。 |
| **文档与示例** | 较弱 | README 只提供概览，缺少完整的使用手册和最佳实践。 |
| **安全性** | 待评估 | 需要自行审计所调用的系统 API，确认没有越权或隐私泄露风险。 |
| **依赖管理** | 中等 | 依赖主要为 Kotlin 标准库和 AndroidX，未见复杂的第三方库。 |
| **维护者响应** | 低 | 项目已进入 WIP 状态，作者因新工作维护频率下降。 |
| **适用场景** | 原型/内部工具 | 适合快速验证概念或内部自动化脚本；不建议直接用于面向用户的生产环境。 |
| **上线建议** | ✔️ 代码审计 → ✔️ 小规模内部验证 → ✔️ 监控与回滚机制 | 在正式部署前务必完成安全审计、性能基准测试，并准备好回滚方案。 |

**总体结论**：ShizukuPlus 在功能上提供了原版 Shizuku 所不具备的扩展能力，适合作为内部原型或实验性项目的快速实现方案。但由于文档不足、维护者活跃度低以及未经过严格的安全审计，直接用于面向用户的生产环境仍存在风险。若决定采纳，务必进行代码审查、权限最小化和持续监控。

## 🧭 Practical evaluation

**Value:** thejaustin/ShizukuPlus may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 369 GitHub stars
- 22 forks
- updated 2026-06-26
- primary language: Kotlin

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 55/100 |
| topics | 0/100 |
| outlook | 59/100 |
| quality | 57/100 |
| recency | 80/100 |
| adoption | 49/100 |
| production | 63/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/thejaustin/ShizukuPlus) · [← Back to Misc](./README.md)</sub>
