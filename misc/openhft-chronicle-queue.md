# OpenHFT/Chronicle-Queue

[![Stars](https://img.shields.io/github/stars/OpenHFT/Chronicle-Queue?style=flat-square&color=yellow)](https://github.com/OpenHFT/Chronicle-Queue/stargazers) [![Forks](https://img.shields.io/github/forks/OpenHFT/Chronicle-Queue?style=flat-square&color=blue)](https://github.com/OpenHFT/Chronicle-Queue/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> Micro second messaging that stores everything to disk

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.8k |
| 🍴 **Forks** | 567 |
| 💻 **Language** | Java |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`chronicle` `java` `low-latency` `performance` `persistance` `queue`

## 🎯 Categories

Misc

## 📝 Summary

### English

Here's a brief summary of the OpenHFT/Chronicle-Queue project:

OpenHFT/Chronicle-Queue is an open-source project that enables microsecond messaging and data storage, allowing teams to persist, query, and move data with minimal custom development. Its value proposition lies in streamlining data management, speeding up access, and facilitating the prototyping of database-backed applications. With its strong adoption, recent activity, and robust ecosystem, OpenHFT/Chronicle-Queue is production-ready for serious pilots, despite requiring a cautious integration approach.

### Русский

OpenHFT / Chronicle‑Queue — это Java‑библиотека микросекундного обмена сообщениями, полностью записывающая данные на диск, что позволяет быстро сохранять, запросить и перемещать большие потоки информации без собственного кода «трубопроводов». Для типичного внедрения рекомендуется начать с небольшого proof‑of‑concept, следуя README, чтобы оценить процесс интеграции, а затем использовать очередь как слой постоянства в приложениях, требующих высокой скорости доступа к данным (например, прототипы баз с поддержкой persistence). Проект считается готовым к production: активные коммиты, более 3700 звёзд, широкое принятие в сообществе и стабильный Java‑экосистемный стек, хотя детали настройки следует проверить перед масштабным развертыванием.

### 中文

**项目简介**  
OpenHFT/Chronicle‑Queue 是一个基于磁盘的微秒级消息队列，能够以极低的延迟持久化、查询和转发海量数据，适合作为高性能持久化层或轻量级数据库的底层引擎。

**价值**  
- **极致性能**：通过内存映射文件和无锁算法，实现微秒级的写入/读取延迟。  
- **简化架构**：把“写入磁盘 + 消息传递”合二为一，免除自研持久化和队列代码的开发成本。  
- **灵活查询**：支持顺序读取、随机访问以及基于时间戳的回放，便于调试和数据回溯。  

**典型接入方式**  
1. **依赖引入**：在 Maven/Gradle 中添加 `net.openhft:chronicle-queue`。  
2. **创建队列**：使用 `ChronicleQueueBuilder.single("path/to/queue")` 创建或打开磁盘目录。  
3. **写入**：通过 `ExcerptAppender` 追加消息，消息体可直接写入 `Bytes`、`String`、自定义对象（实现 `Marshallable`）。  
4. **读取**：使用 `ExcerptTailer` 按顺序或按时间戳回放，支持阻塞/非阻塞读取。  
5. **集成验证**：先在本地或 CI 环境跑一个最小的“生产者‑消费者”示例，确认 README 中的启动脚本和依赖版本即可。

**生产可用性**  
- **成熟度高**：2026‑07‑03 最近一次提交，活跃的维护者和社区；GitHub ★3764、Fork ★567，已在金融、广告和游戏等高并发场景中被广泛采用。  
- **可靠性**：采用写前日志（WAL）+ 文件轮转，崩溃恢复可保证数据不丢失；提供单机和多进程共享模式。  
- **运维成本**：只需磁盘空间和适当的文件系统（推荐 XFS/EXT4），无需额外的服务进程；监控可通过 JMX 暴露的指标完成。  
- **风险**：元数据和部署文档相对简洁，首次接入时需评估磁盘 I/O、文件权限以及 JVM‑Native 兼容性，建议先在预生产环境做一次完整的 POC 再正式上线。  

综上，Chronicle‑Queue 具备高性能、低运维和成熟社区等优势，是在需要微秒级持久化与高速消息传递的 Java 项目中进行生产级部署的可靠 OSS 选型。

## 🧭 Practical evaluation

**Value:** OpenHFT/Chronicle-Queue helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 3764 GitHub stars
- 567 forks
- updated 2026-07-03
- primary language: Java
- 6 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 69/100 |
| stars | 76/100 |
| topics | 75/100 |
| outlook | 58/100 |
| quality | 70/100 |
| recency | 40/100 |
| adoption | 74/100 |
| production | 56/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/OpenHFT/Chronicle-Queue) · [← Back to Misc](./README.md)</sub>
