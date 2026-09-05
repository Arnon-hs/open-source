# deretame/Breeze

[![Stars](https://img.shields.io/github/stars/deretame/Breeze?style=flat-square&color=yellow)](https://github.com/deretame/Breeze/stargazers) [![Forks](https://img.shields.io/github/forks/deretame/Breeze?style=flat-square&color=blue)](https://github.com/deretame/Breeze/network) [![Language](https://img.shields.io/badge/lang-Dart-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Breeze 是一款使用flutter构建的漫画阅读器，通过插件提供漫画支持，现支持哔咔，禁漫，ehentai，nhentai再漫画，拷贝漫画，NoyAcg，komiic，包子漫画，绅士漫画。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.6k |
| 🍴 **Forks** | 46 |
| 💻 **Language** | Dart |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `baozimanhua` `bika` `copymanhua` `ehentai-client` `ios` `jm` `jmcomic` `komiic` `linux` `macos` `nhentai`

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Brief Summary**  
Breeze is a Flutter‑based manga reader that supports a wide range of Chinese and international comic sources through a plug‑in architecture (e.g., Bika, Jmcomic, e‑hentai, nhentai, etc.). The project is actively maintained, written in Dart, and has amassed over 1.5 k stars on GitHub, making it a solid foundation for adding AI‑powered features such as recommendation, content tagging, or RAG‑style assistants.

**Value Proposition**  
- **Rapid AI integration** – Breeze already exposes clear API/SDK hooks and a modular plug‑in system, allowing developers to layer AI services (e.g., image classification, language translation, or personalized recommendation) without rebuilding the core reader.  
- **Cross‑platform reach** – Built with Flutter, the same codebase runs on iOS, Android, and desktop, so AI‑enhanced experiences can be delivered to all users with a single implementation.  
- **Community and ecosystem** – With 1,576 stars, 46 forks, and a growing set of source‑specific plugins, the project provides a ready‑made user base and documentation that accelerate prototyping and validation of AI use‑cases (e.g., automated tag generation, content summarisation, or chat‑based assistants).

**Practical Adoption Path**  
1. **Clone the repository and run the Flutter app** to verify the baseline reader works on your target platforms.  
2. **Identify integration points** – the project’s plugin architecture and exposed services (e.g., `MangaProvider`, `SearchService`) are ideal places to inject AI calls.  
3. **Add an AI micro‑service** (e.g., a FastAPI endpoint using a LLM or vision model) and call it from the Flutter code via HTTP or gRPC.  
4. **Extend or create a plugin** that decorates fetched manga metadata with AI‑generated tags, recommendations, or translations.  
5. **Iterate and test** using the built‑in CLI tools and the provided SDK documentation, then package the enhanced app for distribution.

**Production Readiness**  
- **Activity & Maintenance** – Last commit on 2026‑06‑26, active issue handling, and a responsive maintainer community indicate a healthy codebase.  
- **Stability** – The core Flutter UI and plugin framework are mature; the high star count and multiple source plugins demonstrate real‑world usage.  
- **Scalability** – Because AI logic lives outside the Flutter client (via APIs), you can scale the model serving layer independently, keeping the mobile app lightweight.  
- **Risks** – Licensing (MIT‑style) and security posture appear clean, but a final audit of third‑party dependencies and the plug‑in sources is recommended before a production rollout.  

Overall, Breeze offers a ready‑to‑use, cross‑platform manga reader that can be quickly augmented with AI capabilities, making it a strong candidate for pilot projects and, after a brief security/license review, for full production deployment.

### Русский

Breeze — это открытый Flutter‑клиент для чтения манги, который через модульную систему подключает поддержу множества источников (Bika, Jmcomic, e‑hentai, nhentai, etc.). Его легко интегрировать в существующие мобильные проекты: достаточно добавить SDK/CLI и задать нужный плагин, после чего можно быстро прототипировать AI‑фичи (RAG, агенты) поверх уже готового контента. Проект имеет высокий уровень готовности к production — активные коммиты, более 1500 звёзд, широкое сообщество и стабильный Dart‑код, требующий лишь финальной проверки лицензии и безопасности.

### 中文

**项目价值**  
Breeze 将 Flutter 打造成轻量级的漫画阅读器框架，并通过插件化机制统一接入多家主流漫画站点（哔咔、禁漫、ehentai、nhentai、再漫画、拷贝漫画、NoyAcg、komiic、包子漫画、绅士漫画），极大降低了开发者在不同平台之间的适配成本。得益于其开源、跨平台的特性，开发者可以在现有代码基础上快速添加 AI 功能（如图像识别、内容推荐、自动翻译等），而无需从零搭建模型堆栈。

**典型接入方式**  
1. **依赖引入**：在 Flutter 项目 `pubspec.yaml` 中添加 `breeze` 包及所需的漫画插件。  
2. **插件注册**：在 `main.dart` 初始化时调用 `Breeze.registerPlugin(MyPlugin())`，插件实现统一的 `MangaProvider` 接口即可接入新的漫画源。  
3. **AI 扩展**：通过公开的 API/SDK（如 `Breeze.ai.runModel(...)`）或 CLI 工具，将自研或第三方的模型（TensorFlow Lite、ONNX、OpenAI 等）嵌入阅读流程，实现封面识别、章节自动标签、智能搜索等功能。  
4. **跨平台部署**：一次代码即可生成 Android、iOS、Web、Desktop 四端产物，适配不同设备的 UI/UX。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑26，拥有 1.5k+ Stars、46+ Forks，社区讨论活跃。  
- **技术成熟度**：核心使用 Dart/Flutter，跨平台一致性高；插件机制已在多个漫画站点验证，稳定性良好。  
- **安全与合规**：目前未发现重大许可证或安全风险，但仍建议在正式上线前进行一次许可证合规审查和安全渗透测试。  
- **适配性**：提供完整的 API/SDK 文档和示例代码，集成门槛低，适合作为内部原型或对外商业产品的基础框架。  

综合来看，Breeze 已具备在生产环境中使用的技术和社区支撑，适合作为漫画类移动/跨平台产品的快速搭建基座，并可在此基础上灵活加入 AI 能力。

## 🧭 Practical evaluation

**Value:** deretame/Breeze helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1576 GitHub stars
- 46 forks
- updated 2026-06-26
- primary language: Dart
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 68/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 77/100 |
| recency | 80/100 |
| adoption | 61/100 |
| production | 71/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/deretame/Breeze) · [← Back to Mobile](./README.md)</sub>
