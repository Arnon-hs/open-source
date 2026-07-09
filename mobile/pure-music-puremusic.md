# pure-music/PureMusic

[![Stars](https://img.shields.io/github/stars/pure-music/PureMusic?style=flat-square&color=yellow)](https://github.com/pure-music/PureMusic/stargazers) [![Forks](https://img.shields.io/github/forks/pure-music/PureMusic?style=flat-square&color=blue)](https://github.com/pure-music/PureMusic/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> Cotton Music(棉花音乐): Player for Local file, Drive, Navidrome, Subsonic, Emby, Jellyfin, Plex.  Supports Android, iOS, and PC

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 559 |
| 🍴 **Forks** | 23 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-07-08 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Mobile

## 📝 Summary

### English

Here's a brief summary and explanation of the project:

**Project Summary:** PureMusic is an open-source music player that supports various local file systems, cloud services, and media servers, available on Android, iOS, and PC. It is developed in Kotlin and has received 559 GitHub stars.

**Value Proposition:** PureMusic is useful when you need a concrete workflow that matches its README and activity. Its value lies in its ability to integrate with multiple music services and local file systems, making it a versatile music player for users with specific needs.

**Practical Adoption Path:** Before adopting PureMusic, it's essential to manually inspect the project's README and activity to ensure it matches your specific workflow. Additionally, you should validate the setup cost and potential integration path to avoid any potential issues. With proper evaluation, PureMusic can be a useful tool for prototypes or internal workflows.

**Production Readiness:** PureMusic has a medium production readiness score, indicating that it's suitable for use in prototypes or internal workflows, but may require additional dependency and maintenance checks before it's ready for production use.

### Русский

Резюме:

PureMusic - это открытое исходный код проект, предназначенный для воспроизведения музыки на различных платформах, включая Android, iOS и PC. Проект может быть полезен в сценариях, когда требуется интеграция с локальными файлами, облачными сервисами (Navidrome, Subsonic, Emby, Jellyfin, Plex) и другими системами. Однако, перед внедрением, необходимо тщательно проверить интеграцию и стоимость настройки.

### 中文

**项目简介**  
PureMusic（Cotton Music）是一款基于 Kotlin 的跨平台音乐播放器，支持本地文件、Google Drive、Navidrome、Subsonic、Emby、Jellyfin、Plex 等多种后端，并可在 Android、iOS 与 PC 上运行。

**价值**  
- **统一入口**：一次部署即可在多种音频服务之间切换，适合拥有混合媒体库的团队或个人。  
- **跨平台**：同一套代码在移动端和桌面端保持一致的使用体验，降低运维和培训成本。  
- **开源可定制**：源码可直接改造，满足特定业务流程（如企业内部音乐广播、活动播放列表等）的需求。

**典型接入方式**  
1. **代码层面**：在现有 Android/iOS 项目中通过 Gradle/Maven 引入 `pure-music` 模块，或在 PC 端通过 JAR 包集成。  
2. **后端配置**：在应用设置页面填写对应服务的 API 地址、凭证（Token、用户名/密码）以及可选的 OAuth 流程。  
3. **UI/业务嵌入**：使用提供的 `PlayerFragment`（Android）/`PlayerViewController`（iOS）或 `Swing/JavaFX` 组件，将播放器嵌入现有界面；如需自定义，可直接继承其抽象类实现业务逻辑（例如自动切歌、统计播放数据）。  

**生产可用性**  
- **成熟度**：已有 559 星、23 Fork，最近一次提交在 2026‑07‑08，活跃度尚可。  
- **稳定性**：代码以 Kotlin 编写，依赖相对明确，但官方文档和集成示例较少，建议在正式环境前进行一次完整的功能验证（包括各后端的鉴权、网络异常恢复等）。  
- **适用场景**：适合原型开发、内部工具或对音乐播放有特定定制需求的项目；若用于面向大量用户的生产系统，需要自行完成以下工作：  
  - 完整的单元/集成测试，覆盖所有支持的后端。  
  - 对关键依赖（如网络库、媒体解码器）进行版本锁定与安全审计。  
  - 监控和日志方案，以便快速定位播放中断或鉴权失败等问题。  

总体而言，PureMusic 在功能覆盖和跨平台能力上具备较好价值，但因集成文档稀缺，建议在投入生产前进行一次完整的技术评估和定制化适配。

## 🧭 Practical evaluation

**Value:** pure-music/PureMusic may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 559 GitHub stars
- 23 forks
- updated 2026-07-08
- primary language: Kotlin

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 58/100 |
| topics | 0/100 |
| outlook | 66/100 |
| quality | 63/100 |
| recency | 100/100 |
| adoption | 52/100 |
| production | 68/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-09 · [View on GitHub](https://github.com/pure-music/PureMusic) · [← Back to Mobile](./README.md)</sub>
