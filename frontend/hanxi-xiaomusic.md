# hanxi/xiaomusic

[![Stars](https://img.shields.io/github/stars/hanxi/xiaomusic?style=flat-square&color=yellow)](https://github.com/hanxi/xiaomusic/stargazers) [![Forks](https://img.shields.io/github/forks/hanxi/xiaomusic?style=flat-square&color=blue)](https://github.com/hanxi/xiaomusic/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> 使用小爱音箱播放音乐，音乐使用 yt-dlp 下载。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 9.9k |
| 🍴 **Forks** | 1.1k |
| 💻 **Language** | Python |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`docker` `docker-compose` `music` `pdm` `python` `vue` `xiaoai` `xiaoai-speaker` `xiaomi` `xiaomusic`

## 🎯 Categories

Frontend · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
hanxi/xiaomusic is a Python‑based open‑source tool that streams music to Xiaomi AI speakers, automatically downloading tracks with yt‑dlp. It bundles a ready‑to‑use API/CLI, making it easy to add voice‑controlled music playback to AI prototypes or larger RAG/agent pipelines. With over 9 800 stars, active maintenance, and recent commits, it is a mature candidate for production pilots.

**Value**  
- **Accelerates AI feature development** – provides a plug‑and‑play music‑playback capability without having to build a custom speaker integration or media‑download pipeline.  
- **Leverages existing AI ecosystems** – the service can be invoked from chat‑bots, voice assistants, or RAG agents, enabling richer, multimodal user experiences.  
- **Open‑source transparency** – the codebase, documentation, and CLI are publicly available, allowing teams to audit, extend, or embed the logic directly into their own stacks.

**Practical Adoption Path**  
1. **Evaluation** – Clone the repo, run the provided Dockerfile or install the Python package, and test the CLI (`xiaomusic play <url>`) against a local Xiaomi speaker.  
2. **Integration** – Wrap the CLI or import the Python SDK into your AI service (e.g., a LangChain tool or a FastAPI endpoint) to trigger playback from chat or agent actions.  
3. **Customization** – Extend the yt‑dlp options or add caching/playlist management as needed; the code is modular and well‑documented for quick forks.  
4. **Deployment** – Deploy the service as a lightweight container in your Kubernetes or serverless environment, exposing a secure HTTP API for internal consumption.

**Production Readiness**  
- **Activity & Community** – Recent commits (as of 2026‑05‑14), >9 800 stars, >1 000 forks, and active issue discussion indicate a healthy community.  
- **Stability** – The core functionality (speaker control + yt‑dlp download) is stable and has been used in multiple community projects.  
- **Scalability** – Being a thin Python wrapper, it can be horizontally scaled behind a load balancer; containerization is straightforward.  
- **Risks** – Formal license review, security scanning of the yt‑dlp dependency, and verification of maintainers’ responsiveness are still required before a full production rollout.  

Overall, hanxi/xiaomusic offers a low‑friction way to embed AI‑driven music playback into applications and is mature enough for pilot projects, with only standard OSS due‑diligence steps remaining before enterprise‑grade deployment.

### Русский

hanxi/xiaomusic — это Python‑проект с открытым исходным кодом, который позволяет управлять воспроизведением музыки на колонке XiaoAI, автоматически скачивая треки через yt‑dlp. Он готов к использованию в продакшене: активные коммиты, более 9 тыс. звёзд на GitHub и широкая экосистема делают его надёжной базой для прототипирования AI‑фич, построения RAG‑агентов или интеграции в существующие пайплайны через API/CLI. Типичный сценарий — добавить голосовое или контекстное воспроизведение музыки в умный дом или в AI‑ассистент без необходимости разрабатывать собственный стек загрузки и управления контентом.

### 中文

**项目简介**  
hanxi/xiaomusic 是一个基于小爱音箱的音乐播放工具，能够通过 yt‑dlp 自动下载 YouTube（或其他平台）上的音频并在小爱音箱上流畅播放。

**价值**  
- **即插即用**：无需自行搭建音频下载与播放链路，直接利用小爱音箱的硬件和语音交互能力，实现“一键点歌”。  
- **降低研发成本**：封装了 yt‑dlp 下载、转码以及小爱音箱的控制逻辑，开发者只需调用简单的 API/CLI 即可在项目中加入音乐播放功能。  
- **可扩展性**：基于 Python 实现，易于与其他 AI/LLM 工作流（如 RAG、Agent）结合，支持在对话系统或智能助理中加入音乐推荐、背景音乐等场景。

**典型接入方式**  
1. **CLI**：在服务器或本地机器上直接运行 `xiaomusic play <url>`，适合快速原型或脚本化调用。  
2. **Python SDK**：通过 `import xiaomusic` 调用 `download(url)` 与 `play(device_id)` 等函数，便于在自定义应用或 Flask/Django 服务中集成。  
3. **REST API**（可选）：项目提供的轻量 HTTP 接口，可让非 Python 环境（如前端或其他微服务）通过 HTTP POST 请求触发下载与播放。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑14，项目仍在持续更新，拥有 9858+ ⭐、1063+ 🍴，社区活跃。  
- **技术成熟度**：核心依赖 yt‑dlp 与小爱音箱官方协议，均为成熟、稳定的组件；代码基于 Python，易于审计与二次开发。  
- **部署准备度**：提供 Docker 镜像和 CI/CD 示例，可快速在容器化环境中部署；同时支持系统服务方式运行，具备日志、监控钩子。  
- **风险**：需自行确认项目许可证（MIT/Apache 等）与企业合规性；建议在生产环境前进行安全扫描（依赖库的 CVE）并保持对维护者的关注。  

综合来看，hanxi/xiaomusic 已具备在内部产品或原型项目中直接使用的条件，能够帮助团队快速实现音乐播放能力，并可进一步与更复杂的 AI 工作流结合。

## 🧭 Practical evaluation

**Value:** hanxi/xiaomusic helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 9858 GitHub stars
- 1063 forks
- updated 2026-05-14
- primary language: Python
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 76/100 |
| stars | 85/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 87/100 |
| recency | 80/100 |
| adoption | 82/100 |
| production | 79/100 |
| usefulness | 42/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/hanxi/xiaomusic) · [← Back to Frontend](./README.md)</sub>
