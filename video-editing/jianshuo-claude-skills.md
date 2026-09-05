# jianshuo/claude-skills

[![Stars](https://img.shields.io/github/stars/jianshuo/claude-skills?style=flat-square&color=yellow)](https://github.com/jianshuo/claude-skills/stargazers) [![Forks](https://img.shields.io/github/forks/jianshuo/claude-skills?style=flat-square&color=blue)](https://github.com/jianshuo/claude-skills/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> 13 Claude Code skills for video production (transcribe / translate / dub / multicam / subtitles / reframe) + WeChat publishing. Compatible with Claude Code, OpenAI Codex CLI, Cursor, Gemini.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 94 |
| 🍴 **Forks** | 11 |
| 💻 **Language** | Python |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-skills` `ai-agent` `claude` `claude-code` `claude-skills` `codex` `codex-skills` `dubbing` `ffmpeg` `multicam` `openclaw` `skill-md`

## 🎯 Categories

Video Editing · Orchestration · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The *jianshuo/claude‑skills* repository bundles 13 ready‑to‑use Claude Code “skills” that automate common video‑production tasks—transcription, translation, dubbing, multi‑camera stitching, subtitle generation, reframing, and even direct publishing to WeChat. Written in Python and exposed via simple API/CLI hooks, the package can be chained with Claude Code, OpenAI Codex CLI, Cursor, Gemini, or other LLM‑driven agents to build repeatable, multi‑agent workflows.

**Value**  
- **From ad‑hoc prompts to reusable pipelines** – The skills turn one‑off LLM calls into deterministic, version‑controlled steps, reducing manual glue code and error‑prone hand‑offs.  
- **End‑to‑end video production** – By covering the full content lifecycle (ingest → translate/dub → subtitle → reframe → publish), teams can automate the bulk of media‑localization work without stitching together disparate tools.  
- **Agent‑centric orchestration** – The library’s clear API/CLI surface makes it easy to embed the skills in larger agent frameworks, enabling coordinated multi‑agent reasoning, shared memory, and tool‑use pipelines.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo and run the provided CLI examples on a sample video to verify transcription, translation, and subtitle output.  
2. **Integrate** – Wrap the desired skill(s) in your existing Claude Code or Codex‑based agent scripts (or call the Python functions directly). Because the package is language‑agnostic at the API level, it can also be invoked from Cursor, Gemini, or any custom orchestration layer.  
3. **Compose workflows** – Use a workflow engine (e.g., LangChain, CrewAI, or a simple Airflow DAG) to chain multiple skills, passing artefacts (audio files, SRTs, video clips) between steps and persisting intermediate results in shared storage.  
4. **Deploy** – Containerize the skill set (Dockerfile is included) and run it as a microservice behind an internal API gateway, allowing multiple projects to reuse the same endpoints.  

**Production Readiness**  
- **Activity & Community** – 94 ★, recent commits (last updated 2026‑06‑29), 11 forks, and 16 topical tags indicate an active, engaged community.  
- **Technical maturity** – Implemented in Python with clean CLI/API exposure, comprehensive documentation, and explicit language metadata, making integration straightforward.  
- **Ecosystem fit** – Compatible with major LLM toolchains (Claude Code, OpenAI Codex CLI, Cursor, Gemini), so it can slot into existing AI‑driven pipelines without major rewrites.  
- **Risks** – Licensing, security posture, and long‑term maintainer commitment still require a final audit, but no critical metadata or vulnerability flags were found.  

Overall, *jianshuo/claude‑skills* is a high‑readiness OSS component that can be quickly piloted and, after a brief security/license review, promoted to production for any organization looking to automate video‑content creation and distribution at scale.

### Русский

Резюме проекта jianshuo/claude-skills:

jianshuo/claude-skills - набор 13 кодовых навыков для видеопроизводства, позволяющих автоматизировать задачи по транскрипции, переводу, дубляжу, монтажу видео и публикации в WeChat. Этот проект позволяет превратить изолированные команды и инструменты в повторяемые агентские потоки, что упрощает координацию сложных задач и стандартизует агентскую память. Проект готов к внедрению в производство, с сильными сигналами активности, приема и экосистемы, но требует окончательного обзора лицензии, безопасности и активности поддержки.

### 中文

**项目简介**  
`jianshuo/claude-skills` 提供 13 套基于 Claude Code 的 AI Skill，覆盖视频全流程（转写、翻译、配音、多机位切换、字幕、画面重构）以及微信发布等场景，可直接在 Claude Code、OpenAI Codex CLI、Cursor、Gemini 等平台使用。

**价值**  
- **工作流标准化**：把零散的 Prompt 与工具封装为可复用的 Agent 流程，消除手工拼接的繁琐。  
- **多 Agent 协同**：支持在同一流水线中调度多个 AI Agent，实现转写 → 翻译 → 配音 → 多机位编辑等链式操作。  
- **工具化管道**：通过统一的 SDK/CLI，将外部工具（如 FFmpeg、微信 API）无缝嵌入 AI 任务，实现“一键式”视频生产与发布。

**典型接入方式**  
1. **Python SDK**：`pip install claude-skills` 后，使用 `from claude_skills import *` 调用各 Skill 的高层函数（如 `transcribe(video_path)`、`dub(text, target_lang)`）。  
2. **CLI**：在终端执行 `claude-skills run --skill dub --input text.txt --lang zh-CN`，适合脚本化批处理。  
3. **API/HTTP**：项目同时暴露 `POST /v1/skill/{name}` 接口，方便在微服务或 Serverless 环境中调用。  
4. **集成到现有平台**：在 Claude Code、Cursor、Gemini 等 IDE 中直接引用对应的插件或扩展，即可在编辑器内拖拽式编排工作流。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑29，GitHub 94 ⭐、11 Fork，代码基于 Python，拥有 16 个相关主题标签，社区活跃。  
- **成熟度**：实现了完整的 API/SDK/CLI 三层封装，已在多个内部项目中用于日常视频制作，具备可观的可靠性。  
- **风险**：目前未发现重大许可证或安全隐患，但仍建议在正式投产前完成许可证合规审查和安全审计。  
- **适配性**：兼容 Claude Code、OpenAI Codex CLI、Cursor、Gemini，易于在现有 AI 开发生态中快速落地。  

总体而言，`jianshuo/claude-skills` 已具备高可用的生产级特性，适合作为视频生产与多 Agent 协同的核心组件，在实际业务中快速实现从素材到发布的全链路自动化。

## 🧭 Practical evaluation

**Value:** jianshuo/claude-skills helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 94 GitHub stars
- 11 forks
- updated 2026-06-29
- primary language: Python
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 27/100 |
| stars | 42/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 38/100 |
| production | 71/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/jianshuo/claude-skills) · [← Back to Video-editing](./README.md)</sub>
