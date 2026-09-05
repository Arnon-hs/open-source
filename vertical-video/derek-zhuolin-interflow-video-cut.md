# derek-zhuolin/interflow-video-cut

[![Stars](https://img.shields.io/github/stars/derek-zhuolin/interflow-video-cut?style=flat-square&color=yellow)](https://github.com/derek-zhuolin/interflow-video-cut/stargazers) [![Forks](https://img.shields.io/github/forks/derek-zhuolin/interflow-video-cut?style=flat-square&color=blue)](https://github.com/derek-zhuolin/interflow-video-cut/network) [![Language](https://img.shields.io/badge/lang-HTML-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> 把本地口播视频自动剪成卡片式成片的 Agent Skill：抽音轨 → ElevenLabs 转录 → AI 逐张写 HTML 卡片 → 渲染 MP4。10 种视觉风格 × 4 布局，转录只走 ElevenLabs 永不下本地模型。Turn a talking-head video into an AI-composed card-based video.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 29 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | HTML |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-skill` `ai-video` `claude-code` `content-creation` `elevenlabs` `ffmpeg` `gsap` `hyperframes` `short-video` `talking-head` `transcription` `video-editing`

## 🎯 Categories

Vertical Video · Video Editing · Content Creation · AI/ML

## 📝 Summary

### English

**derek-zhuolin/interflow-video-cut** automates the repurposing of talking-head videos into vertical, card-style shorts by leveraging ElevenLabs for transcription and AI-generated HTML layouts, eliminating the need for local model inference. The practical adoption path suggests starting with a small proof-of-concept to validate the ElevenLabs dependency and rendering pipeline against specific content workflows. With medium production readiness, it is currently best suited for prototypes or internal automation, requiring a thorough review of licensing, security, and long-term maintenance before deploying in a production environment.

### Русский

derek‑zhuolin/interflow-video‑cut автоматизирует создание коротких вертикальных роликов из «говорящей головы»: извлекает аудио, транскрибирует его через ElevenLabs, генерирует HTML‑карточки и рендерит MP4 в одном из 10 визуальных стилей и 4 layouts. Типовой сценарий — быстрая переработка длинных вебинаров или интервью в Shorts/Reels‑формат для соцсетей без необходимости ручного монтажа и без загрузки локальных моделей ИИ. Проект имеет средний уровень готовности к production: подходит для прототипов и внутренних workflow‑ов, но перед коммерческим использованием рекомендуется проверить зависимости, лицензию и активность поддержки.

### 中文

**价值**：derek-zhuolin/interflow-video-cut 通过“抽音轨 → ElevenLabs 转录 → AI 逐张写 HTML 卡片 → 渲染 MP4”全链路自动化，将本地口播视频一键生成多风格卡片式短视频，大幅降低垂直短视频（如 Shorts/Reels）制作成本与工时。

**典型接入方式**：开发者可依据项目 README，先搭建本地或云端的 Python 运行环境，配置 ElevenLabs API 密钥，随后传入一段口播视频即可得到 10 种视觉风格 × 4 种布局的 9:16 MP4 产出；若需批量处理，可封装为脚本或微服务接入自有视频流水线。

**生产可用性**：中等水平。该项目适合作为原型或内部工具使用，但在正式投入生产前，需要完成依赖锁链、模型服务安全、代码许可证及维护活跃度等风险评估；建议先进行小规模 POC 验证，再逐步扩展到实际业务

## 🧭 Practical evaluation

**Value:** derek-zhuolin/interflow-video-cut helps automate short-form video production and repurposing for vertical channels.

**Best use cases**

- produce Shorts/Reels-style clips
- repurpose long videos into 9:16 assets
- automate captions and clipping

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 29 GitHub stars
- 5 forks
- updated 2026-08-07
- primary language: HTML
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 31/100 |
| topics | 100/100 |
| outlook | 60/100 |
| quality | 58/100 |
| recency | 60/100 |
| adoption | 28/100 |
| production | 59/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-08-23 · [View on GitHub](https://github.com/derek-zhuolin/interflow-video-cut) · [← Back to Vertical-video](./README.md)</sub>
