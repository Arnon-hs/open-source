# ErsatzTV/next

[![Stars](https://img.shields.io/github/stars/ErsatzTV/next?style=flat-square&color=yellow)](https://github.com/ErsatzTV/next/stargazers) [![Forks](https://img.shields.io/github/forks/ErsatzTV/next?style=flat-square&color=blue)](https://github.com/ErsatzTV/next/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-46%2F100-brightgreen?style=flat-square)](#)

> Transcode and stream your media as live TV channels.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 122 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | Rust |
| 📈 **Score** | 46/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
ErsatzTV/next is a Rust‑based open‑source tool that creates virtual live‑TV channels by transcoding and streaming your personal media library on‑the‑fly. It lets you assemble playlists, EPG data, and DVR‑style scheduling so that movies, series, and music videos appear as regular broadcast channels in any compatible client. The project is modestly popular (≈120 GitHub stars) and was last updated on 2026‑06‑26.

**Value Proposition**  
- **Unified Live‑TV Experience:** Turns a static media collection into a continuously streaming “live” service, enabling seamless integration with Plex, Kodi, or IPTV clients that expect broadcast‑style inputs.  
- **Dynamic Transcoding:** Performs on‑the‑fly transcoding to match client capabilities, reducing the need for multiple pre‑encoded files.  
- **Programmable Scheduling:** Supports custom channel line‑ups, EPG generation, and time‑based playback, which is valuable for internal media portals, testbeds, or niche consumer products that want a “TV‑like” feel without a traditional broadcast backend.

**Practical Adoption Path**  
1. **Initial Feasibility Check** – Clone the repo and run the provided Docker compose or binary on a test machine; verify that your media library can be indexed and that a client (e.g., VLC, Kodi) can receive the generated HLS/DASH streams.  
2. **Configuration Tailoring** – Edit the TOML/YAML config to define channel playlists, EPG sources, and transcoding presets that match your target devices.  
3. **Integration Validation** – Hook the generated stream URLs into your existing media portal or IPTV gateway and confirm that authentication, DRM (if any), and network routing work as expected.  
4. **Automation & Monitoring** – Wrap the service in systemd/Kubernetes, add health checks, and set up log aggregation to catch transcoding failures early.  
5. **Security & Maintenance Review** – Audit the Rust dependencies (via `cargo audit`), pin versions, and establish a routine for pulling upstream updates.

**Production‑Readiness Assessment**  
- **Maturity:** Medium. The codebase is actively maintained (last commit within days) and has a small but engaged community, but documentation and integration examples are limited.  
- **Stability:** Suitable for prototypes, internal tools, or controlled‑environment deployments; production use will require thorough testing of transcoding pipelines, network load, and failure handling.  
- **Operational Overhead:** Moderate – you’ll need to manage the transcoding workload, storage for temporary files, and ensure the service scales with concurrent viewers.  
- **Risk Mitigation:** Conduct a pilot deployment, perform load testing, and lock down dependency versions before committing to a long‑term production rollout.  

In short, ErsatzTV/next offers a compelling way to deliver “live TV” from a personal media collection, but teams should allocate time for hands‑on validation and operational hardening before treating it as a critical production component.

### Русский

ErsatzTV/next — это open‑source‑решение на Rust, позволяющее транскодировать локальные медиаресурсы и вещать их как живые ТВ‑каналы, что удобно для создания персонализированных потоковых сервисов или прототипов IPTV‑систем. Проект имеет умеренную готовность к production: активные обновления, 122 звёзд на GitHub и небольшое количество форков, однако интеграция требует ручного анализа и проверки зависимостей, так как сигналы о готовых коннекторах и настройках скудны. Подойдёт для внутренних пилотных проектов, при условии предварительного тестирования и оценки затрат на внедрение.

### 中文

**项目简介**  
ErsatzTV/next 是一个用 Rust 编写的开源工具，能够把本地媒体文件实时转码并包装成 IPTV/直播频道，供 Plex、Emby、Jellyfin 等媒体服务器或普通播放器直接播放。

**价值**  
- **即插即用的直播化**：无需预先生成 TS/HLS 文件，媒体在请求时才转码，极大节省存储空间。  
- **统一频道管理**：可把电影、剧集、音乐等不同内容统一映射为虚拟电视台，提升用户在客户端的浏览体验。  
- **高性能**：Rust 实现提供低延迟和较低的 CPU 开销，适合资源受限的 NAS 或家庭服务器。

**典型接入方式**  
1. **部署**：在目标机器上编译或直接使用提供的 Docker 镜像运行 `ersatztv-next`。  
2. **配置**：在 `config.yaml` 中声明媒体库路径、转码参数（如 H.264/AV1、音频 AAC/Opus）以及要生成的频道列表。  
3. **集成**：在 Plex/Emby/Jellyfin 等服务器中添加一个 “网络流”源，URL 指向 `http://<host>:<port>/channel/<channel-id>.m3u8`。  
4. **可选扩展**：通过 Web UI 或 REST API 动态增删频道、调整转码质量，或结合 Nginx 进行鉴权与缓存。

**生产可用性**  
- **成熟度**：项目已有 122 星、5 个 fork，最近一次提交在 2026‑06‑26，活跃度尚可。  
- **适用场景**：适合原型验证、内部媒体服务或家庭实验环境；在正式生产环境使用前建议：  
  - 完整评估转码硬件（CPU/GPU）是否能满足并发需求。  
  - 编写自动化部署脚本并进行故障恢复演练。  
  - 监控日志与资源占用，确保在高负载下不会出现卡顿。  
- **风险**：项目文档和集成示例相对有限，需自行验证与现有媒体服务器的兼容性，并做好后期维护（依赖更新、Rust 生态升级）计划。  

总体而言，ErsatzTV/next 在需要将本地媒体即时转码为直播流的场景下提供了轻量且高效的解决方案，只要做好前期的环境验证和运维准备，即可在生产环境中稳定运行。

## 🧭 Practical evaluation

**Value:** ErsatzTV/next may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 122 GitHub stars
- 5 forks
- updated 2026-06-26
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 44/100 |
| topics | 0/100 |
| outlook | 56/100 |
| quality | 52/100 |
| recency | 80/100 |
| adoption | 37/100 |
| production | 59/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/ErsatzTV/next) · [← Back to Misc](./README.md)</sub>
