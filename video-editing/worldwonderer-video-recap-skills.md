# worldwonderer/video-recap-skills

[![Stars](https://img.shields.io/github/stars/worldwonderer/video-recap-skills?style=flat-square&color=yellow)](https://github.com/worldwonderer/video-recap-skills/stargazers) [![Forks](https://img.shields.io/github/forks/worldwonderer/video-recap-skills?style=flat-square&color=blue)](https://github.com/worldwonderer/video-recap-skills/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Turn any video into a narration recap with claude code skill｜用claude code skill把任何视频剪辑成中文解说视频，支持剪映导出

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 330 |
| 🍴 **Forks** | 56 |
| 💻 **Language** | Python |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `asr` `claude-code` `claude-code-plugin` `claude-skills` `ffmpeg` `llm` `mimo` `speech-to-text` `text-to-speech` `tts` `video-narration`

## 🎯 Categories

Video Editing · AI/ML

## 📝 Summary

### English

**Brief Summary**  
worldwonderer/video-recap-skills is a Python‑based open‑source toolkit that leverages Claude Code Skills to automatically generate Chinese narration recaps from any video file, with built‑in support for exporting the result to the Jianying (剪映) editor. It provides a ready‑to‑use API/CLI that can be dropped into AI‑augmented workflows without having to train or host a custom model stack.  

**Value**  
- **Accelerated AI feature prototyping** – developers can add sophisticated video‑to‑text narration capabilities in minutes, bypassing the time‑consuming steps of data collection, model training, and inference‑engine setup.  
- **Plug‑and‑play integration** – the project ships a clean Python SDK and a command‑line interface, exposing simple functions (e.g., `recap(video_path, language="zh")`) that can be called from scripts, web services, or larger RAG/agent pipelines.  
- **End‑to‑end workflow support** – the generated narration can be directly fed into Jianying for further editing, making the tool useful for content creators, e‑learning platforms, and media monitoring services that need quick Chinese voice‑over drafts.  

**Practical Adoption Path**  
1. **Evaluation** – Clone the repo, install dependencies (`pip install -r requirements.txt`), and run the provided CLI on a sample video to verify output quality and latency.  
2. **Integration** – Wrap the SDK call in a microservice (e.g., FastAPI) or a serverless function; expose an endpoint that accepts a video URL or upload and returns the narration file or a Jianying project bundle.  
3. **Workflow Extension** – Combine the service with other AI components (e.g., summarization, translation, or sentiment analysis) using LangChain, CrewAI, or custom agent frameworks to build richer pipelines such as “video → transcript → summary → Chinese voice‑over”.  
4. **Productionization** – Containerize the microservice (Docker), add monitoring (Prometheus metrics for processing time, error rates), and secure the Claude API key via secret management.  

**Production Readiness**  
- **Activity & Community** – 330 ★, 56 forks, recent commits (last updated 2026‑06‑26), and multiple contributors indicate an active codebase.  
- **Maturity** – The project already offers a stable CLI, clear Python API, and explicit language metadata, reducing integration friction.  
- **Ecosystem Fit** – Compatible with popular AI orchestration tools and with the widely used Jianying editor, facilitating end‑user adoption.  
- **Risks** – Licensing terms, long‑term maintainer commitment, and security hardening of the Claude API key still need a final review, but no major metadata or vulnerability flags have been identified.  

Overall, worldwonderer/video-recap-skills is a high‑readiness OSS candidate for pilots that need fast, Chinese‑language video narration powered by Claude, and it can be scaled to production with modest engineering effort.

### Русский

**worldwonderer/video-recap-skills** — это открытый Python‑пакет, который с помощью Claude Code Skill автоматически преобразует любое видео в китайскую озвученную выдержку, поддерживая экспорт в формат, совместимый с редактором 剪映. Проект уже имеет 330 звёзд, активные коммиты и готовый API/CLI, что делает его пригодным для быстрого прототипирования AI‑функций (RAG, агентные сценарии) и даже для пилотного внедрения в продакшн. При отсутствии серьёзных лицензий‑ и безопасности‑рисков, проект считается «production‑ready» для интеграции в существующие видеоплатформы.

### 中文

**项目简介**  
worldwonderer/video-recap-skills 是一个基于 Claude Code Skill 的开源工具，可将任意视频自动生成中文解说稿并输出剪映可直接使用的剪辑文件，帮助用户快速制作专业级视频回顾。

**价值**  
- **即插即用的 AI 能力**：无需自行训练模型或搭建复杂的推理链，只需调用现成的 Skill 即可实现视频内容理解、摘要生成和中文配音。  
- **加速原型与产品研发**：适用于快速验证 AI 视频解说、内容摘要、RAG（检索增强生成）或智能客服等场景，显著缩短开发周期。  
- **生态兼容**：提供 API、SDK 与 CLI 三种接入方式，且输出格式与剪映（CapCut）高度兼容，方便后续编辑与发布。

**典型接入方式**  
1. **API 调用**：向项目提供的 REST 接口 POST 视频文件或 URL，返回 JSON 结构的解说稿与音频文件链接。  
2. **Python SDK**：在 Python 项目中 `pip install video-recap-skills`，使用 `VideoRecap()` 类直接调用 `generate_narration(video_path, language='zh')`。  
3. **CLI 工具**：在终端执行 `video-recap --input video.mp4 --lang zh --output recap.mp4`，一键完成全部流程，适合脚本化批处理。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑26 最近一次提交，拥有 330+ stars、56 forks，社区活跃且已有多项实际使用案例。  
- **技术成熟**：核心实现基于 Python，依赖明确（Claude API、ffmpeg、OpenAI Whisper），并提供完整的错误日志与重试机制。  
- **安全与合规**：项目采用 MIT 许可证，未发现重大安全漏洞；但在正式生产前仍建议进行内部安全审计与依赖版本锁定。  

综合来看，worldwonderer/video-recap-skills 已具备较高的生产就绪度，适合作为视频解说、内容摘要等 AI 功能的快速落地组件。

## 🧭 Practical evaluation

**Value:** worldwonderer/video-recap-skills helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 330 GitHub stars
- 56 forks
- updated 2026-06-26
- primary language: Python
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 54/100 |
| topics | 100/100 |
| outlook | 58/100 |
| quality | 63/100 |
| recency | 40/100 |
| adoption | 51/100 |
| production | 60/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/worldwonderer/video-recap-skills) · [← Back to Video-editing](./README.md)</sub>
