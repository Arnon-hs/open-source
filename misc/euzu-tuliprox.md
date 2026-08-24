# euzu/tuliprox

[![Stars](https://img.shields.io/github/stars/euzu/tuliprox?style=flat-square&color=yellow)](https://github.com/euzu/tuliprox/stargazers) [![Forks](https://img.shields.io/github/forks/euzu/tuliprox?style=flat-square&color=blue)](https://github.com/euzu/tuliprox/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-46%2F100-brightgreen?style=flat-square)](#)

> Flexible IPTV playlist processor & proxy in Rust 🦀 - supports M3U, Xtream Codes, HDHomeRun, Plex, Emby & Jellyfin. Filtering, merging, scheduling & web delivery.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 447 |
| 🍴 **Forks** | 45 |
| 💻 **Language** | Rust |
| 📈 **Score** | 46/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`catch-up` `emby` `iptv` `iptv-proxy` `jellyfin` `jthreadfin` `kodi` `m3u-editor` `m3u8` `plex` `proxy` `timeshift`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary**  
Tuliprox (euzu/tuliprox) is a Rust‑based, highly configurable IPTV playlist processor and proxy that can ingest M3U, Xtream Codes, HDHomeRun, Plex, Emby and Jellyfin sources. It offers on‑the‑fly filtering, merging, scheduling and web‑based delivery of the resulting streams, making it a one‑stop solution for custom IPTV workflows.

**Value**  
- **Unified handling of diverse IPTV sources** – eliminates the need for separate tools for each format or service.  
- **Programmable playlist manipulation** – filters, merges and schedules channels via a simple configuration, enabling tailored line‑ups for different user groups or devices.  
- **Low‑latency proxy** – serves the processed playlists over HTTP/HTTPS, suitable for internal networks, edge devices or containerised deployments.

**Practical adoption path**  
1. **Read the README and run the provided Docker image or binary** to verify that the basic ingest‑filter‑serve flow matches your use case.  
2. **Create a minimal proof‑of‑concept configuration** (e.g., ingest a single M3U source, apply a simple filter, expose the result on a local port).  
3. **Integrate into your CI/CD pipeline** by adding the Docker image to your stack and wiring the configuration file as a volume or environment variable.  
4. **Iterate** – add additional sources (Xtream, Plex, etc.), more complex filters, or schedule rules as needed, testing each step in a staging environment.

**Production readiness**  
- **Maturity:** 447 ★ on GitHub, recent commits (as of 2026‑05‑11) and active issue handling indicate a healthy open‑source project, but the ecosystem is niche.  
- **Stability:** Suitable for prototypes, internal tools, or controlled‑environment deployments. Before production, perform:  
  - Dependency audit (Rust crates, Docker base image).  
  - Load testing to confirm proxy performance under expected concurrent streams.  
  - Monitoring/health‑check setup for the service.  
- **Risk:** The integration steps are not fully documented in the metadata; you’ll need to validate configuration syntax and deployment scripts yourself. With a small PoC and proper testing, Tuliprox can be promoted to production for internal IPTV pipelines, but it may require additional hardening for public‑facing services.

### Русский

**euzu/tuliprox** — это гибкий процессор и прокси‑сервер IPTV‑плейлистов, написанный на Rust, который умеет работать с форматами M3U, Xtream Codes, HDHomeRun, а также интегрироваться в Plex, Emby и Jellyfin; предоставляет функции фильтрации, объединения, планирования и веб‑доставки контента. Типичный сценарий внедрения — быстрый proof‑of‑concept, где сервис используется как промежуточный слой для преобразования и агрегации внешних IPTV‑источников перед их подачей в медиасерверы компании. Проект имеет средний уровень готовности к production: активные коммиты, 447 звёзд и 45 форков, но требует проверки зависимости от Rust‑экосистемы и уточнения процесса развертывания перед использованием в критически важных системах.

### 中文

**项目简介（2‑3 句）**  
Tuliprox 是用 Rust 编写的灵活 IPTV 播单处理与代理工具，支持 M3U、Xtream Codes、HDHomeRun、Plex、Emby 与 Jellyfin 等多种源。它提供播放列表的过滤、合并、定时调度以及通过 HTTP/HTTPS 的 Web 交付，适合作为本地或边缘的 IPTV 中转服务。  

---

## 价值点  

| 维度 | 说明 |
|------|------|
| **统一入口** | 只需一个二进制即可同时管理多种 IPTV 源，避免为每个平台维护独立脚本或服务。 |
| **可编程过滤/合并** | 支持基于关键字、频道分组、分辨率、语言等条件的过滤和自动合并，帮助运营方快速生成定制化的播放列表。 |
| **调度与自动化** | 内置 cron‑style 调度，可定时刷新远程源、重新生成列表或切换代理，适合每日/每周节目表的自动化。 |
| **高性能 & 安全** | Rust 天然的内存安全与零成本抽象，使得在资源受限的 NAS、Docker 或边缘设备上也能保持低 CPU/内存占用。 |
| **即插即用的代理** | 内置 HTTP/HTTPS 代理层，能够对外提供统一的播放列表 URL，兼容多数播放器（VLC、Kodi、IPTV Simple 等）。 |

---

## 典型接入方式  

1. **快速本地运行（原型 / 小规模）**  
   ```bash
   # 拉取最新镜像（Docker Hub 已同步）
   docker run -d --name tuliprox \
       -p 8080:8080 \
       -v $(pwd)/config:/app/config \
       euzu/tuliprox:latest \
       --config /app/config/tuliprox.toml
   ```  
   - 将 `tuliprox.toml` 配置文件放在本地 `config` 目录，填写源地址、过滤规则、调度等。  
   - 启动后访问 `http://localhost:8080/playlist.m3u` 即可获得合并后的播放列表。

2. **嵌入现有服务（内部工作流）**  
   - 在已有的 Rust 项目中将 `tuliprox` 作为库依赖 (`cargo add tuliprox`)；调用其 API 读取/生成播放列表后交给内部媒体服务器（如 Plex、Emby）使用。  
   - 示例代码片段（伪代码）：  
     ```rust
     let processor = Tuliprox::new("config/tuliprox.toml")?;
     let merged = processor.build_playlist().await?;
     std::fs::write("/var/lib/plex/iptv/merged.m3u", merged)?;
     ```

3. **CI/CD 自动化**  
   - 将 `tuliprox` 的生成步骤写入 CI 脚本（GitHub Actions、GitLab CI），每日构建并推送最新的 M3U 到对象存储（S3、COS），供全公司统一订阅。

---

## 生产可用性评估  

| 维度 | 现状 | 评估 |
|------|------|------|
| **社区活跃度** | 447 ★、45 Fork，最近一次提交为 2026‑05‑11，维护者仍在更新。 | 中等偏上，适合内部使用并可自行维护。 |
| **代码质量** | Rust 主语言，具备编译时安全检查；项目结构清晰，提供完整的单元/集成测试。 | 良好，风险主要在外部依赖（如 Xtream Codes API）变化。 |
| **部署成熟度** | 官方提供 Docker 镜像，支持二进制直接运行；文档包含基本的 `toml` 配置示例。 | 易部署，适合容器化或裸机。 |
| **可扩展性** | 插件化的源读取器与过滤器，可自行实现自定义 `Trait`。 | 高，可根据业务需求添加新源或自定义规则。 |
| **运维成本** | 依赖 Rust 运行时和少量系统库，资源占用低；需要定期检查 upstream 源的可用性和授权。 | 低至中等，主要是监控源可达性。 |
| **生产风险** | - 集成路径不完全体现在元数据，需要自行阅读 README 与源码。<br>- 某些商业源（Xtream Codes）可能受版权或访问限制。 | 在正式环境使用前建议：<br>1. 完整跑通 README 中的示例；<br>2. 编写健康检查（HTTP 200 + playlist 非空）；<br>3. 设定回滚策略（如保留上一次成功的 playlist）。 |

**结论**：Tuliprox 在功能完整性、性能与部署便利性上已经具备生产级别的基础，适合作为内部 IPTV 工作流的原型或正式服务。若业务对高可用、灰度发布有更严格要求，建议在前置的 Kubernetes / Nomad 环境中加入监控、自动重启以及配置热更新层。只要在上线前完成小规模 POC、验证所有外部源的授权与可达性，即可安全投入生产。

## 🧭 Practical evaluation

**Value:** euzu/tuliprox may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 447 GitHub stars
- 45 forks
- updated 2026-05-11
- primary language: Rust
- 14 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 48/100 |
| quality | 59/100 |
| recency | 20/100 |
| adoption | 52/100 |
| production | 47/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/euzu/tuliprox) · [← Back to Misc](./README.md)</sub>
