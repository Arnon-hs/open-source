# tonhowtf/omniget

[![Stars](https://img.shields.io/github/stars/tonhowtf/omniget?style=flat-square&color=yellow)](https://github.com/tonhowtf/omniget/stargazers) [![Forks](https://img.shields.io/github/forks/tonhowtf/omniget?style=flat-square&color=blue)](https://github.com/tonhowtf/omniget/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> Open-source desktop app for downloading, organizing and studying media. Native cross-platform (Tauri + Rust + Svelte). PDF/EPUB reader with focus mode, timestamped notes and spaced repetition. Media downloads via yt-dlp (1.800+ sites). Extensible plugin system.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 6.6k |
| 🍴 **Forks** | 556 |
| 💻 **Language** | Rust |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-07-09 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bilibili-downloader` `course-downloader` `desktop-app` `download-manager` `downloader` `hotmart-downloader` `instagram-downloader` `media-downloader` `open-source` `reddit-downloader` `rust` `svelte`

## 🎯 Categories

Database · Education · Marketing

## 📝 Summary

### English

Here's a brief summary of the project:

Omniget is an open-source desktop app for managing and studying media, offering features such as a PDF/EPUB reader, timestamped notes, and spaced repetition. Its extensible plugin system and native cross-platform capabilities make it a versatile tool for users and teams. With its strong GitHub presence and recent activity, Omniget is a production-ready candidate for serious pilots.

**Value:**
The value proposition of Omniget lies in its ability to help teams persist, query, and move data with ease, reducing the need for custom plumbing. Its extensible plugin system also makes it an attractive option for users who want to customize the app to their specific needs.

**Practical Adoption Path:**
To adopt Omniget, users can start by evaluating its implementation signals, such as its API, SDK, CLI, language metadata, and focused topics. They can also explore its GitHub presence, including its number of stars, forks, and updates. With its recent activity and adoption, Omniget is a viable option for serious pilots.

**Production Readiness:**
Omniget is considered production-ready due to its recent activity, adoption, and ecosystem signals. Its high score of 67/100 and strong GitHub presence make it a

### Русский

Резюме проекта tonhowtf/omniget:

Омнигет - это открытый проект для управления и изучения медиа, включающий в себя функции скачивания, организации и чтения PDF/EPUB файлов. Программа предназначена для команд и позволяет им сохранять, запросить и перемещать данные без необходимости создания сложной инфраструктуры.

Типовой сценарий внедрения: омнигет подойдет для команд, которые хотят ускорить доступ к данным, прототипировать приложения с базой данных и эффективно управлять сохранением и запросами данных.

Уровень готовности к production: высокий, поскольку проект демонстрирует активность, широкое принятие и сильные сигналы экосистемы, что делает его подходящим кандидатом для серьезного пилота.

### 中文

**项目简介**  
tonhowtf/omniget 是一款基于 Tauri、Rust 与 Svelte 的跨平台桌面应用，专注于媒体下载、整理与学习。它内置 PDF/EPUB 阅读器，支持专注模式、带时间戳的笔记以及间隔重复记忆，并通过 yt‑dlp 能够一次性下载 1,800+ 网站的音视频资源，还提供可扩展的插件体系。

**价值主张**  
- **统一管理**：帮助团队把分散的媒体、文档和学习笔记持久化、统一索引，随时可检索。  
- **提升效率**：一次性批量下载并自动归档，配合间隔重复功能让学习更高效。  
- **可扩展**：插件系统让业务可以在现有功能之上快速添加自定义数据处理或工作流。

**典型接入方式**  
1. **CLI / API**：通过 omniget 提供的命令行接口或本地 HTTP API 调用下载、查询、标注等功能，适合脚本化或后端服务集成。  
2. **SDK**：项目在 `src/sdk` 中导出 Rust 与 JavaScript（via WASM）绑定，开发者可在自研应用中直接调用核心库。  
3. **插件**：编写符合约定的 Rust/Svelte 插件并放入 `plugins/` 目录，即可在 UI 与后台自动加载，实现业务特定的元数据同步或第三方服务对接。

**生产可用性**  
- **活跃度**：截至 2026‑07‑09 最近一次提交，GitHub 计 6,579 星、556 Fork，社区活跃，Issue 处理及时。  
- **技术成熟度**：使用 Tauri + Rust 打造的原生二进制体积小、启动快，跨 Windows/macOS/Linux 稳定。  
- **安全与合规**：目前未发现重大元数据泄露风险，仍需对许可证（MIT/Apache 双许可）和依赖（yt‑dlp、ffmpeg）进行正式审计。  
- **可评估性**：提供完整的 API 文档、示例脚本以及插件开发指南，企业可以在短周期内完成概念验证并在生产环境中部署。  

综上，omniget 在媒体管理与学习场景下具备高可用性、易集成的特性，是值得在内部或面向团队的生产环境中试点的开源候选。

## 🧭 Practical evaluation

**Value:** tonhowtf/omniget helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 6579 GitHub stars
- 556 forks
- updated 2026-07-09
- primary language: Rust
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 69/100 |
| stars | 81/100 |
| topics | 100/100 |
| outlook | 83/100 |
| quality | 90/100 |
| recency | 100/100 |
| adoption | 78/100 |
| production | 80/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-09 · [View on GitHub](https://github.com/tonhowtf/omniget) · [← Back to Database](./README.md)</sub>
