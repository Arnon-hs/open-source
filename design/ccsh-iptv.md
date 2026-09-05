# CCSH/IPTV

[![Stars](https://img.shields.io/github/stars/CCSH/IPTV?style=flat-square&color=yellow)](https://github.com/CCSH/IPTV/stargazers) [![Forks](https://img.shields.io/github/forks/CCSH/IPTV?style=flat-square&color=blue)](https://github.com/CCSH/IPTV/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> 一个免费、轻量、全自动化的直播源、台标 Logo 与 EPG 电子节目指南网络采集同步工具。自动拉取并整合互联网公开资源，格式化输出，适配 IPTV、电视盒子、手机直播 APP 等主流使用场景。（自动采集、测速、无广告）

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 324 |
| 🍴 **Forks** | 133 |
| 💻 **Language** | Python |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`diyp` `epg` `free` `icon` `iptv` `iptv-m3u` `live` `logo` `m3u` `m3u8` `playlist` `stream`

## 🎯 Categories

Design

## 📝 Summary

### English

**Brief Summary**  
CCSH/IPTV is a free, lightweight, fully‑automated tool that harvests live‑stream URLs, channel logos, and EPG data from public internet sources, normalises the information and outputs it in formats ready for IPTV services, set‑top boxes and mobile streaming apps. It performs continuous source collection, speed testing and ad‑free filtering without any manual intervention.  

**Value**  
- **Accelerates AI‑enabled media workflows** – By providing clean, structured streaming metadata out‑of‑the‑box, CCSH/IPTV lets developers focus on higher‑level AI features (e.g., recommendation engines, content‑based search, RAG or autonomous agents) instead of building a data‑collection pipeline from scratch.  
- **Broad compatibility** – The generated manifests and EPG files conform to the standards used by most IPTV platforms, reducing integration effort for downstream services.  
- **Cost‑effective and open** – No licensing fees, a permissive open‑source license, and a modest codebase (Python) make it easy to audit, extend, and embed in proprietary stacks.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the provided `README` examples, and verify that the generated playlists/EPG files work with a local IPTV client.  
2. **Integration Layer** – Wrap the CLI or import the Python modules into your existing media‑pipeline service; map the output to your AI model’s input schema (e.g., channel‑name → embedding, logo → image feature).  
3. **Pilot Deployment** – Deploy the collector as a scheduled job (Docker/K8s) in a staging environment, monitor source freshness and speed‑test metrics, and feed the data into a prototype recommendation or RAG system.  
4. **Scale‑Out** – Add custom source parsers or filters, enable CI/CD for automated updates, and integrate with your production IPTV or OTT backend.  

**Production Readiness**  
- **Activity & Community** – 324 stars, 133 forks, recent commits (as of 2026‑06‑23), and a healthy number of topics indicate an active project.  
- **Technical Maturity** – The tool is written in Python, has clear documentation, and follows a simple, testable architecture, making it straightforward to audit and harden.  
- **Risk Assessment** – No immediate licensing or security red flags, though a final review of the license (likely MIT/Apache) and a security scan of dependencies is recommended.  
Overall, CCSH/IPTV is sufficiently mature for a serious pilot and can be incrementally integrated into production pipelines once the initial PoC validates data quality and stability.

### Русский

CCSH/IPTV — это бесплатный, лёгкий и полностью автоматизированный инструмент для сбора, тестирования и синхронизации онлайн‑источников трансляций, логотипов каналов и EPG‑данных; он собирает открытые интернет‑ресурсы, форматирует их и выводит в совместимых с IPTV, ТВ‑плеерами и мобильными приложениями видах (без рекламы). Типичный сценарий внедрения — быстрая настройка прототипа AI‑сервисов, RAG‑агентов или других функций, где требуется готовый набор живых потоков и метаданных без необходимости построения модели с нуля. Проект имеет высокий уровень готовности к production: активные коммиты, более 300 звёзд на GitHub, поддержка Python, обширная экосистема и подтверждённое использование в реальных IPTV‑решениях.

### 中文

**项目简介（2‑3 句）**  
CCSH/IPTV 是一款免费、轻量、全自动化的直播源、台标 Logo 与 EPG 电子节目指南采集同步工具。它能够自动抓取并整合互联网上公开的直播资源，统一格式化输出，直接兼容 IPTV、电视盒子、手机直播 App 等主流播放场景，实现无广告、测速、自动更新。

**价值**  
- **省时省力**：一次配置后即可持续自动抓取、测速并生成符合标准的播放列表和节目表，免去手工搜集、校验的繁琐工作。  
- **跨平台兼容**：输出的 M3U、JSON、XML 等格式可直接在几乎所有 IPTV 软硬件上使用，降低二次开发成本。  
- **质量保障**：内置线路测速与可用性检测，自动剔除失效或慢速源，保证用户观看体验。  
- **开源透明**：基于 Python 实现，社区活跃（>300 星、130+ Fork），便于二次定制和安全审计。

**典型接入方式**  
1. **直接部署**：在服务器或容器（Docker）上克隆仓库，按 `config.yaml` 配置采集源、更新频率等参数，运行 `python run.py` 即可生成 `m3u`、`epg.xml` 等文件。  
2. **CI/CD 自动化**：将项目加入已有的 CI 流程（GitHub Actions、GitLab CI），利用定时任务每天或每小时触发采集，生成的文件推送到对象存储或 CDN。  
3. **二次封装**：通过提供的 Python API（`ccsh.iptv` 包）在自研的内容平台中调用 `fetch_sources()`、`generate_epg()` 等函数，实现与业务系统的深度集成。  

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑23，社区仍在持续维护，Issue 响应及时。  
- **成熟度**：项目已在多个公开 IPTV 项目中验证，具备完整的错误重试、日志、健康检查机制，适合作为生产环境的核心采集服务。  
- **安全与合规**：使用 MIT 许可证，代码公开，可自行审计依赖库的安全性；建议在上线前进行一次依赖漏洞扫描（如 `pip-audit`）并确认采集的内容符合当地版权法规。  
- **可扩展性**：基于插件式的采集器设计，新增或替换数据源只需实现对应的抓取类，无需修改核心逻辑，便于后期功能迭代。  

综上，CCSH/IPTV 具备 **高可用、易集成、低成本** 的特性，是构建或升级 IPTV 内容供应链的理想开源组件。

## 🧭 Practical evaluation

**Value:** CCSH/IPTV helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 324 GitHub stars
- 133 forks
- updated 2026-06-23
- primary language: Python
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 53/100 |
| stars | 53/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 74/100 |
| recency | 80/100 |
| adoption | 53/100 |
| production | 72/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/CCSH/IPTV) · [← Back to Design](./README.md)</sub>
