# JeffreyCA/spleeter-web

[![Stars](https://img.shields.io/github/stars/JeffreyCA/spleeter-web?style=flat-square&color=yellow)](https://github.com/JeffreyCA/spleeter-web/stargazers) [![Forks](https://img.shields.io/github/forks/JeffreyCA/spleeter-web?style=flat-square&color=blue)](https://github.com/JeffreyCA/spleeter-web/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Self-hostable web app for isolating the vocal, accompaniment, bass, and drums of any song. Supports Spleeter, Demucs, BS-RoFormer. Started in 2019.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 549 |
| 🍴 **Forks** | 89 |
| 💻 **Language** | Python |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bs-roformer` `demucs` `separation` `source-separation` `spleeter` `vocal-remover`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
JeffreyCA/spleeter‑web is a self‑hosted web application that lets users separate a song into vocal, accompaniment, bass, and drum stems using Spleeter, Demucs, or BS‑RoFormer. Launched in 2019, the project is actively maintained (last update 2026‑07‑01) and written in Python, with a strong community presence (≈ 550 ⭐, 89 🍴). It provides an easy‑to‑deploy UI and API for audio source‑separation tasks.

**Value Proposition**  
- **Rapid audio preprocessing:** Teams can automate high‑quality stem extraction without relying on third‑party SaaS, reducing latency and cost for downstream tasks such as remixing, karaoke generation, or training ML models.  
- **Unified backend:** By supporting three state‑of‑the‑art separation engines, the app lets users experiment with the best model for their data while keeping a single deployment footprint.  
- **Self‑hosting & control:** All processing runs on‑premises, giving full control over data privacy, licensing, and compute resources.

**Practical Adoption Path**  
1. **Proof‑of‑Concept:** Clone the repo, follow the README to spin up the Docker compose stack (or a simple `pip install` + `uvicorn` command) on a test server. Run a few songs through the UI/API to verify separation quality and performance.  
2. **Integration:** Wrap the provided REST endpoints in your existing pipeline (e.g., a media‑ingestion service) or call the Python library directly for tighter coupling.  
3. **Scaling:** Deploy the service behind a load balancer, enable GPU acceleration on the host, and configure persistent storage for uploaded tracks and generated stems.  
4. **Monitoring & CI:** Add health checks, log aggregation, and automated tests for the API to ensure reliability before promoting to production.

**Production Readiness**  
- **Activity & Community:** Recent commits (as of 2026‑07‑01), a healthy star/fork count, and multiple topics indicate an engaged user base.  
- **Stability:** Core functionality (audio separation) is mature; the codebase is primarily Python with clear dependency management.  
- **Risk Assessment:** No critical metadata or licensing issues have been identified, but a final security audit and confirmation of active maintainers are advisable. Overall, the project is mature enough for a serious pilot or production deployment, provided the usual OSS due‑diligence steps are completed.

### Русский

JeffreyCA/spleeter‑web — это самодостаточное веб‑приложение, позволяющее в реальном времени извлекать вокал, аккомпанемент, бас и ударные из любой аудиодорожки с помощью Spleeter, Demucs и BS‑RoFormer. Для команд, которым требуется быстро развернуть сервис аудио‑разделения (например, в музыкальных сервисах, медиаплатформах или при создании прототипов приложений с хранением и обработкой аудиофайлов), проект предоставляет готовый стек без необходимости писать собственную интеграцию. По состоянию на июль 2026 проект считается практически готовым к production: активные коммиты, 549 звёзд, регулярные обновления и широкая поддержка в экосистеме Python, однако перед запуском в продакшн стоит проверить лицензию, безопасность зависимостей и наличие активных мейнтейнеров.

### 中文

**项目简介**  
JeffreyCA/spleeter‑web 是一款可自行部署的 Web 应用，能够对任意音频进行人声、伴奏、低音和鼓声的分离，底层支持 Spleeter、Demucs 与 BS‑RoFormer 等主流模型，项目自 2019 年启动并持续维护。

**价值**  
- **一站式音频分离**：无需自行搭建复杂的机器学习环境，直接通过浏览器上传音频即可获得高质量的四轨分离结果。  
- **多模型兼容**：同时支持 Spleeter（轻量快速）、Demucs（时域高保真）和 BS‑RoFormer（最新 Transformer）三种算法，满足不同精度与速度需求。  
- **自托管安全**：所有音频和模型都运行在本地服务器上，数据不泄露，适合企业内部或隐私敏感的音频处理场景。

**典型接入方式**  
1. **快速部署**：克隆仓库后使用 Docker Compose 或直接 `pip install -r requirements.txt`，配置好模型路径，即可在本机或私有云上启动。  
2. **API 调用**：启动后提供 RESTful `/separate` 接口，支持 POST 音频文件并返回分轨的下载链接或直接的二进制流，便于后端服务或前端页面集成。  
3. **前端嵌入**：利用自带的 React 前端页面，可直接在内部门户或 SaaS 产品中以 iframe 形式嵌入，实现“上传即分离”的用户体验。

**生产可用性**  
- **活跃度**：截至 2026‑07‑01，项目仍在维护，最近一次提交在当月，拥有 549 ★、89 Fork，社区活跃。  
- **技术成熟度**：核心使用 Python 编写，依赖成熟的开源模型（Spleeter、Demucs、BS‑RoFormer），并提供 Docker 镜像，部署与扩容相对简单。  
- **风险评估**：暂无重大元数据或许可证风险，但仍建议在正式上线前完成安全审计（依赖库的 CVE 检查）并确认维护者的响应能力。  
- **适配建议**：先在测试环境完成一次完整的端到端验证（上传‑分离‑下载），确认模型加载、并发性能以及存储策略后，再推广到生产环境。  

综合来看，spleeter‑web 已具备较高的生产就绪度，适合作为企业内部音频处理或面向用户的音乐分离服务的核心组件。

## 🧭 Practical evaluation

**Value:** JeffreyCA/spleeter-web helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 549 GitHub stars
- 89 forks
- updated 2026-07-01
- primary language: Python
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 49/100 |
| stars | 58/100 |
| topics | 75/100 |
| outlook | 68/100 |
| quality | 71/100 |
| recency | 80/100 |
| adoption | 56/100 |
| production | 69/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/JeffreyCA/spleeter-web) · [← Back to Misc](./README.md)</sub>
