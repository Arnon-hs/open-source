# walkingddd/TgtoDrive

[![Stars](https://img.shields.io/github/stars/walkingddd/TgtoDrive?style=flat-square&color=yellow)](https://github.com/walkingddd/TgtoDrive/stargazers) [![Forks](https://img.shields.io/github/forks/walkingddd/TgtoDrive?style=flat-square&color=blue)](https://github.com/walkingddd/TgtoDrive/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> 一条龙网盘媒体自动化平台：从找资源、自动转存、智能整理、挂载 STRM、到 Emby 302 直链播放，全流程打通；重点强化 115 / 123 / 光鸭云盘整理与转存、115 / 123 /光鸭云盘 STRM 全量与增量生成、以及 Emby 反向代理 302 播放能力。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.5k |
| 🍴 **Forks** | 124 |
| 💻 **Language** | Python |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

walkingddd/TgtoDrive is an open‑source Python platform that automates the entire media pipeline—from locating resources and auto‑saving them to 115/123/光鸭云盘, generating full and incremental STRM files, to serving those links through an Emby reverse‑proxy for seamless 302 playback. Adoption involves reviewing the README and recent activity to confirm it matches your workflow, then installing the dependencies and configuring the supported cloud‑storage APIs before running the scripts; because integration signals are limited, a manual inspection and testing phase is recommended. The project shows moderate production readiness (useful for prototypes or internal use) but requires a final check of its license, security posture, and maintainer activity before deploying in a production environment.

### Русский

walkingddd/TgtoDrive — это платформа для полной автоматизации медиа‑конвейера: она ищет ресурсы в облаках 115, 123 и 光鸭, автоматически сохраняет их, формирует STRM‑ссылки и обеспечивает их воспроизведение в Emby через 302‑переад

### 中文

**项目价值**  
walkingddd/TgtoDrive 是一个“一条龙”式的网盘媒体自动化平台，能够把从资源搜索、自动转存、智能分类、生成 STRM 播放地址一直到通过 Emby 反向代理实现 302 直链播放的完整流程全部自动化。它特别针对 115、123、光鸭等常用网盘做了深度优化，支持全量/增量 STRM 生成和批量整理，帮助个人或小团队大幅降低手动搬运、分类和播放配置的工作量，从而实现媒体库的高效、持续更新。

**典型接入方式**  

| 步骤 | 操作要点 | 关键配置 |
|------|----------|----------|
| 1. 环境准备 | - Python 3.9+ <br>- Docker（推荐） <br>- 需要的网盘 API Token（115、123、光鸭） | 在 `config.yaml` 中填写网盘账号、密码或 token |
| 2. 安装部署 | - `git clone https://github.com/walkingddd/TgtoDrive.git` <br>- `docker compose up -d`（或 `pip install -r requirements.txt` 本地运行） | 可通过 `docker-compose.yml` 自定义挂载目录、Emby 反向代理端口 |
| 3. 资源抓取 | - 配置 TG 频道或 RSS 源的关键词 <br>- 启动 `crawler` 服务 | 支持正则过滤、去重、自动下载至临时目录 |
| 4. 自动转存 & 整理 | - 设置转存规则（如按类型、年份、标签分目录） <br>- 启动 `transfer` 服务 | 支持 115/123/光鸭之间的跨盘搬迁，自动生成目录结构 |
| 5. STRM 生成 | - 通过 `strm_generator` 自动遍历已转存文件 <br>- 生成对应的 `.strm` 文件并推送到指定网盘根目录 | 支持全量一次性生成，也支持增量监听新文件自动生成 |
| 6. Emby 反向代理 | - 在 Emby 中添加网络共享路径指向生成的 STRM 目录 <br>- 配置 Nginx/Traefik 进行 302 重定向 | 通过 `emby_proxy` 模块实现播放链接的安全转发，兼容外网访问 |

> **快速上手示例**（Docker）  
> ```bash
> git clone https://github.com/walkingddd/TgtoDrive.git
> cd TgtoDrive
> cp config.example.yaml config.yaml   # 按需求填写
> docker compose up -d
> ```  
> 完成后访问 `http://<host>:8000/docs` 可查看 API 文档并手动触发各步骤。

**生产可用性评估**  

| 维度 | 现状 | 备注 |
|------|------|------|
| **功能完整度** | ✅ 全流程自动化（抓取 → 转存 → 整理 → STRM → Emby） | 已在多个个人媒体库中实际使用 |
| **代码成熟度** | ⭐ 1.5k 星 / 124 Fork，最近一次提交 2026‑06‑30 | 社区活跃度一般，但核心功能稳定 |
| **部署难度** | 中等 | 推荐使用 Docker，手动部署需处理网盘 API 鉴权 |
| **依赖管理** | 依赖 Python 第三方库和网盘官方/非官方 API | 需定期检查依赖安全更新 |
| **安全性** | 需要自行管理网盘凭证、Emby 代理的访问控制 | 建议在内部网络或使用 VPN，避免凭证泄露 |
| **运维成本** | 需要监控任务执行（cron / Celery）和磁盘空间 | 可通过内置日志和 Prometheus Exporter 进行监控 |
| **适用场景** | - 个人/小团队的媒体库自动化 <br>- 需要统一管理多网盘资源的内部工具 | 不建议直接用于大规模商业 SaaS，除非进行二次审计和容灾设计 |

**结论**  
walkingddd/TgtoDrive 在媒体资源自动化方面提供了相对完整且易于扩展的解决方案，适合作为 **内部原型** 或 **小规模生产** 环境使用。若要在业务关键系统中正式上线，建议：

1. 完成安全审计（尤其是网盘凭证和 Emby 代理的访问控制）。  
2. 将关键任务（抓取、转存、STRM 生成）封装为可靠的作业调度（如 Airflow / Celery Beat），并加入失败重试与告警。  
3. 对核心依赖（Python 库、网盘 API）进行定期更新和兼容性测试。  

经过上述加固后，项目可以在 **中等规模** 的媒体服务场景中投入生产使用。

## 🧭 Practical evaluation

**Value:** walkingddd/TgtoDrive may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1510 GitHub stars
- 124 forks
- updated 2026-06-30
- primary language: Python

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 52/100 |
| stars | 68/100 |
| topics | 0/100 |
| outlook | 62/100 |
| quality | 64/100 |
| recency | 80/100 |
| adoption | 63/100 |
| production | 66/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/walkingddd/TgtoDrive) · [← Back to Misc](./README.md)</sub>
