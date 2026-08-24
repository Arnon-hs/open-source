# giuseppe99barchetta/SuggestArr

[![Stars](https://img.shields.io/github/stars/giuseppe99barchetta/SuggestArr?style=flat-square&color=yellow)](https://github.com/giuseppe99barchetta/SuggestArr/stargazers) [![Forks](https://img.shields.io/github/forks/giuseppe99barchetta/SuggestArr?style=flat-square&color=blue)](https://github.com/giuseppe99barchetta/SuggestArr/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Effortlessly request recommended movies, TV shows and anime to Jellyseer/Overseer based on your recently watched content on Jellyfin, Plex or Emby—let SuggestArr handle it all automatically, keeping your library fresh with new and exciting content!

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.1k |
| 🍴 **Forks** | 22 |
| 💻 **Language** | Python |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`automation` `docker` `emby` `jellyfin` `jellyseerr` `llm` `media-automation` `ombi` `open-source` `openai` `overseerr` `plex`

## 🎯 Categories

Automation · AI/ML · DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
SuggestArr automatically generates movie, TV‑show, and anime recommendations for Jellyseer/Overseer by analysing the titles you’ve recently watched on Jellyfin, Plex or Emby. The tool runs on a simple Python‑based service, exposing an API/CLI that can be slotted into existing media‑library automation pipelines, keeping your collection fresh without any manual curation.

**Value**  
- **Eliminates repetitive recommendation work** – instead of manually searching for new titles, SuggestArr continuously scans your watch history and pushes curated suggestions to Jellyseer/Overseer.  
- **Integrates with existing media stacks** – it works with the three major self‑hosted media servers (Jellyfin, Plex, Emby), so you can reuse your current infrastructure.  
- **Scalable, repeatable flows** – the API/CLI can be called from cron jobs, CI/CD pipelines, or orchestration tools (e.g., GitHub Actions, Airflow), enabling fully automated, scheduled recommendation updates.  

**Practical Adoption Path**  
1. **Deploy the Python service** – clone the repo, install dependencies (`pip install -r requirements.txt`), and run the containerised version (Dockerfile provided) or a virtual‑env instance.  
2. **Configure credentials** – add API tokens for your Jellyfin/Plex/Emby server and for Jellyseer/Overseer in the supplied `config.yaml`.  
3. **Connect to your workflow** – invoke the CLI (`suggestarr recommend`) or call the REST endpoint from a cron job, a Home Assistant automation, or a CI pipeline to run at your preferred cadence (e.g., nightly).  
4. **Monitor & tune** – use the built‑in logging and optional Prometheus metrics to verify that recommendations are being generated and delivered correctly; adjust filters (genre, rating, watch‑time window) via the config file.  

**Production Readiness**  
- **Active development** – last commit on 2026‑05‑11, 1,133 GitHub stars, and a healthy fork count indicate strong community interest.  
- **Mature ecosystem fit** – Python is a first‑class language for DevOps automation, and the project already ships a Docker image, API, CLI, and comprehensive documentation.  
- **Low risk** – no known licensing or security red flags, though a final review of the dependency tree and maintainer activity is advisable.  
Overall, SuggestArr is production‑ready for a pilot deployment in any self‑hosted media environment, offering a straightforward, automated way to keep your library populated with fresh content.

### Русский

**SuggestArr** — это Python‑скрипт, который автоматически анализирует вашу историю просмотров в Jellyfin, Plex или Emby и формирует запросы рекомендаций фильмов, сериалов и аниме к сервисам Jellyseer/Overseer, избавляя от ручного подбора контента и поддерживая библиотеку актуальной. Типовой сценарий: установить SuggestArr в контейнере или как cron‑задачу, подключить API‑ключи к Jellyfin/Plex/Emby и к Jellyseer, и система будет регулярно (например, раз в сутки) отправлять запросы рекомендаций и обновлять список предложений. Проект считается почти готовым к production: активные коммиты, более 1000 звёзд, множество форков, поддержка CLI/SDK и хорошая экосистема, требующие лишь финальной проверки лицензии и безопасности.

### 中文

**项目简介**  
Giuseppe99barchetta 的 **SuggestArr** 能自动根据 Jellyfin、Plex 或 Emby 中最近观看的影片，为 Jellyseer/Overseer 推荐电影、电视剧和动漫。只需一次配置，系统即可持续为你的媒体库注入新鲜、符合口味的内容，彻底摆脱手动挑选的繁琐。

**核心价值**  
- **省时省力**：把“我最近看了什么”转化为精准推荐的全过程自动化，消除重复的手工搜索与添加操作。  
- **提升库活跃度**：持续推送符合用户口味的内容，让媒体库保持新鲜感，提升观看率。  
- **可组合性**：通过标准化的 API/SDK/CLI，轻松嵌入已有的媒体管理工作流或 CI/CD 管道，实现端到端的自动化。

**典型接入方式**  
1. **API 调用**：使用项目提供的 RESTful 接口，向 SuggestArr 发送最近观看记录（JSON），获取推荐列表。  
2. **CLI 工具**：在服务器上通过 `suggestarr` 命令行工具直接执行“获取推荐 → 自动添加至 Jellyseer/Overseer”的全链路操作，适合 cron / systemd 定时任务。  
3. **Python SDK**：在自定义脚本或现有自动化平台（如 Home Assistant、Ansible）中引入 `suggestarr` 包，调用 `get_recommendations()` 等函数，实现深度集成。  

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑05‑11，项目仍在维护；GitHub ★1133、Fork 22，社区关注度高。  
- **技术成熟度**：核心实现使用 Python，配套完整的 API 文档与示例代码，易于审计和二次开发。  
- **生态兼容**：已支持 Jellyfin、Plex、Emby 三大主流媒体服务器，且可直接对接 Jellyseer/Overseer。  
- **风险评估**：暂无重大元数据或安全漏洞，仍需对许可证（MIT/Apache 等）和长期维护者进行最终确认。  

综合来看，SuggestArr 已具备 **高生产就绪度**，适合作为媒体库自动推荐的首选 OSS 组件，快速在实际环境中进行试点并推广。

## 🧭 Practical evaluation

**Value:** giuseppe99barchetta/SuggestArr helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1133 GitHub stars
- 22 forks
- updated 2026-05-11
- primary language: Python
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 65/100 |
| topics | 100/100 |
| outlook | 56/100 |
| quality | 60/100 |
| recency | 20/100 |
| adoption | 56/100 |
| production | 52/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/giuseppe99barchetta/SuggestArr) · [← Back to Automation](./README.md)</sub>
