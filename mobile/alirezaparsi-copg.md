# AlirezaParsi/COPG

[![Stars](https://img.shields.io/github/stars/AlirezaParsi/COPG?style=flat-square&color=yellow)](https://github.com/AlirezaParsi/COPG/stargazers) [![Forks](https://img.shields.io/github/forks/AlirezaParsi/COPG?style=flat-square&color=blue)](https://github.com/AlirezaParsi/COPG/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-48%2F100-brightgreen?style=flat-square)](#)

> An advanced and powerful Zygisk module for comprehensive device and CPU spoofing with granular per-app control via JSON configuration.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 313 |
| 🍴 **Forks** | 30 |
| 💻 **Language** | C++ |
| 📈 **Score** | 48/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`advance` `android` `copg` `device-spoofing` `free` `gaming` `kernelsu-module` `magisk` `opensource` `rezygisk` `root` `spoofing`

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
AlirezaParsi/COPG is a Zygisk module that lets Android users spoof device identifiers and CPU characteristics on a per‑app basis, driven by a flexible JSON configuration. It offers fine‑grained control for developers who need to test or hide hardware details, making it a powerful tool for privacy‑focused or compatibility‑testing scenarios.

**Value Proposition**  
- **Granular spoofing** – Change model, manufacturer, CPU flags, etc., for individual apps without affecting the whole system.  
- **JSON‑driven rules** – Simple, declarative configuration lets teams script complex spoofing policies quickly.  
- **Open‑source, C++ core** – Low overhead and easy to audit, with a growing community (300+ ⭐, 30 forks).  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, follow the README to build the Zygisk module, and load it on a test device (rooted or using Magisk).  
2. **Configure a JSON rule set** – Define a few apps (e.g., a banking app, a game) and verify that the spoofed properties appear as expected via `adb shell getprop`.  
3. **Iterate & integrate** – Wrap the JSON generation in your CI pipeline or internal tooling if you need dynamic rules (e.g., per‑user or per‑environment).  
4. **Security review** – Because the module runs with high privileges, audit the C++ code and any third‑party libraries before wider rollout.  

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last commit 2026‑06‑25) and has a solid star/fork base, but documentation is modest and the integration steps are not fully automated.  
- **Risks:** Requires a rooted/Magisk‑enabled device; the exact build and deployment steps can be non‑trivial for large fleets. Dependency and maintenance overhead should be evaluated, especially for devices with custom ROMs.  
- **Recommendation:** Suitable for internal prototypes, QA labs, or privacy‑enhancing features on controlled device groups. Before production use, perform a small‑scale pilot, verify stability across Android versions, and establish a maintenance plan for future OS updates.

### Русский

AlirezaParsi/COPG — это мощный Zygisk‑модуль, позволяющий подменять идентификацию устройства и процессора с детальной настройкой поведения для каждого приложения через JSON‑конфигурацию, что упрощает прототипирование AI‑фич и построение RAG‑агентов. Для внедрения рекомендуется начать с небольшого proof‑of‑concept, проверив README и базовую сборку, а затем постепенно интегрировать модуль в существующий мобильный стек. Готовность к production — средняя: проект подходит для прототипов и внутренних процессов, но требует проверки зависимостей, поддержки и потенциальных рисков интеграции перед запуском в продакшн.

### 中文

**项目简介**  
AlirezaParsi/COPG 是一款基于 Zygisk 的高级模块，能够对 Android 设备及 CPU 参数进行全面伪装，并通过 JSON 文件实现细粒度的按应用控制。

**价值**  
- **快速实现 AI 场景**：在不自行搭建底层模型的情况下，即可为移动端 AI 功能提供可信的硬件信息，帮助模型获得更真实的运行环境或规避硬件检测。  
- **灵活的按应用配置**：通过 JSON 可为不同应用分别指定伪装策略，适用于安全测试、隐私保护和开发调试等多种场景。  
- **开源且活跃**：拥有 300+ 星、30+ 分支，代码基于 C++，社区持续维护，便于二次开发。

**典型接入方式**  
1. **环境准备**：在已刷入 Magisk 的设备上安装 Zygisk 并启用 “Zygisk module loading”。  
2. **模块部署**：将 COPG 的 zip 包放入 `/data/adb/modules/`，重启设备或使用 `magisk reload` 生效。  
3. **配置 JSON**：在模块根目录下创建 `config.json`，按照文档定义全局或 per‑app 的 CPU/设备属性。  
4. **验证**：使用 `adb shell getprop` 或对应 APP 的硬件查询接口确认伪装生效。  
5. **集成到 AI 流程**：在模型加载或推理前读取设备信息，确保 AI 框架（如 TensorFlow Lite、ONNX Runtime）获取到伪装后的参数，从而实现一致的性能/兼容性测试。

**生产可用性**  
- **成熟度**：当前评分 57/100，适合作为原型或内部工具使用。代码更新活跃（截至 2026‑06‑25），但缺少完整的 CI/CD 与官方文档，需自行验证兼容性。  
- **风险**：模块依赖 Magisk/Zygisk，若设备不支持或系统升级导致兼容性问题，集成成本会增加；此外，JSON 配置的错误可能导致系统不稳定，需要在受控环境中充分测试。  
- **建议**：先在少量测试机上完成 PoC，确认伪装效果与 AI 推理表现后，再逐步推广至生产设备；同时做好回滚方案（保留原始 Magisk 模块）。  

总体而言，COPG 在需要对硬件信息进行细粒度控制的 AI 原型开发中价值突出，但在正式生产环境部署前应完成充分的兼容性和稳定性验证。

## 🧭 Practical evaluation

**Value:** AlirezaParsi/COPG helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 313 GitHub stars
- 30 forks
- updated 2026-06-25
- primary language: C++
- 17 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 37/100 |
| stars | 53/100 |
| topics | 100/100 |
| outlook | 55/100 |
| quality | 62/100 |
| recency | 40/100 |
| adoption | 49/100 |
| production | 53/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/AlirezaParsi/COPG) · [← Back to Mobile](./README.md)</sub>
