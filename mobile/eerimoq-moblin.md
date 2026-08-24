# eerimoq/moblin

[![Stars](https://img.shields.io/github/stars/eerimoq/moblin?style=flat-square&color=yellow)](https://github.com/eerimoq/moblin/stargazers) [![Forks](https://img.shields.io/github/forks/eerimoq/moblin?style=flat-square&color=blue)](https://github.com/eerimoq/moblin/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-45%2F100-brightgreen?style=flat-square)](#)

> Moblin, a free iOS app for IRL streaming.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 681 |
| 🍴 **Forks** | 92 |
| 💻 **Language** | Swift |
| 📈 **Score** | 45/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Summary**  
Moblin is an open‑source iOS application that enables real‑world (IRL) video streaming directly from an iPhone. With a solid Swift codebase (681 ★, 92 forks) and recent activity (last commit 2026‑07‑01), it can serve as a quick prototype or internal tool for teams needing a custom streaming client, provided the integration work is carefully evaluated.

**Value**  
- Provides a ready‑made, free streaming client that can be forked and extended, saving the effort of building an iOS streamer from scratch.  
- The Swift implementation aligns well with existing iOS development pipelines, making it easy for teams already using Apple’s ecosystem to adopt and customize.  

**Practical adoption path**  
1. **Review the README and source** to understand the streaming protocol, authentication flow, and any third‑party services it relies on.  
2. **Clone the repo** and run the example project locally to verify that the basic streaming functionality works with your own media server (e.g., RTMP, SRT, or WebRTC).  
3. **Map required integrations** (e.g., token handling, UI branding, analytics) and add missing hooks; because the metadata is sparse, you’ll likely need to read the code to locate extension points.  
4. **Create a small proof‑of‑concept** that streams to a test endpoint, then iterate on any missing features or bug fixes.  

**Production readiness**  
- **Maturity:** Medium. The project is actively maintained but lacks comprehensive documentation and explicit integration guides, so it’s best suited for prototypes or internal tools rather than a turnkey production service.  
- **Dependencies:** Verify the compatibility of its Swift packages and any native libraries with your target iOS version and CI pipeline.  
- **Maintenance:** Monitor upstream updates (e.g., security patches) and be prepared to fork long‑term if the original maintainers shift focus.  

In short, Moblin can accelerate the development of an iOS IRL streaming client, but teams should perform a manual code audit and a small pilot integration before committing it to a production environment.

### Русский

Moblin — открытое iOS‑приложение для прямых IRL‑трансляций, написанное на Swift (681 ★, 92 форка) и активно поддерживаемое (обновление 2026‑07‑01). Оно подходит для быстрого прототипирования или внутренних потоков видеотрансляций, однако интеграция требует ручного анализа — в метаданных мало информации о подключаемых сервисах, поэтому перед внедрением следует оценить затраты на настройку и поддержание зависимостей. При достаточной проверке готово к использованию в ограниченных продакшн‑сценариях.

### 中文

Moblin 是一个开源 iOS 应用程序，用于实地直播（IRL streaming）。其价值在于，当 README 和活动与具体的工作流程匹配时，可能会很有用。典型的接入方式需要手动检查和确认，因为元数据中的集成信号较少。Moblin 的生产可用性为中等（Medium），适合用于原型或内部工作流程，需要在生产环境中进行依赖和维护检查。

## 🧭 Practical evaluation

**Value:** eerimoq/moblin may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 681 GitHub stars
- 92 forks
- updated 2026-07-01
- primary language: Swift

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 49/100 |
| stars | 60/100 |
| topics | 0/100 |
| outlook | 47/100 |
| quality | 51/100 |
| recency | 40/100 |
| adoption | 57/100 |
| production | 49/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/eerimoq/moblin) · [← Back to Mobile](./README.md)</sub>
