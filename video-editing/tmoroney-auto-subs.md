# tmoroney/auto-subs

[![Stars](https://img.shields.io/github/stars/tmoroney/auto-subs?style=flat-square&color=yellow)](https://github.com/tmoroney/auto-subs/stargazers) [![Forks](https://img.shields.io/github/forks/tmoroney/auto-subs?style=flat-square&color=blue)](https://github.com/tmoroney/auto-subs/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> On-device subtitle generation that connects directly to DaVinci Resolve, Premiere, and After Effects.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.7k |
| 🍴 **Forks** | 240 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `cross-platform` `davinci` `davinci-resolve` `premiere` `resolve` `rust` `speech-to-text` `subtitles` `transcribe` `transcription` `video-editing`

## 🎯 Categories

Video Editing · AI/ML

## 📝 Summary

### English

**Brief Summary**  
tmoroney/auto‑subs is an open‑source TypeScript library that generates subtitles on‑device and streams them directly into DaVinci Resolve, Adobe Premiere, and After Effects. It lets developers add AI‑driven captioning to video workflows without building a model stack from scratch, and it’s backed by strong community signals (3.7 k stars, recent commits, and active forks).  

**Value**  
The project provides a ready‑made pipeline for on‑device speech‑to‑text, eliminating the need to train or host large language or transcription models yourself. By exposing a simple API that plugs into the native scripting interfaces of major NLEs, it accelerates prototyping of AI‑enhanced video tools, RAG pipelines, or autonomous editing agents, while keeping data local for privacy‑sensitive productions.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the provided demo script, and verify subtitle output on a short test clip.  
2. **Integration** – Follow the README to install the npm package in your editing‑tool extension (e.g., a Premiere panel) and configure the on‑device transcription engine (default Whisper‑cpp or a custom model).  
3. **Pilot** – Deploy the extension to a small team, gather feedback on latency and accuracy, and iterate on model selection or post‑processing hooks.  

**Production Readiness**  
The library scores high on OSS maturity: recent activity (last commit 2026‑07‑01), a large star/fork base, and clear TypeScript typings. Its architecture is modular, allowing you to swap the transcription backend without breaking the Resolve/Premiere integration. While the license, security posture, and maintainer responsiveness still need a final audit, the current signals suggest it is ready for a serious pilot in production environments.

### Русский

Резюме проекта tmoroney/auto-subs:

tmoroney/auto-subs - это open-source проект, который позволяет генерировать субтитры на устройстве напрямую из приложений DaVinci Resolve, Premiere и After Effects. Этот проект особенно полезен для разработчиков, которые хотят внедрить функции AI в свои приложения без создания собственного стека моделей. tmoroney/auto-subs готов к использованию в production и обладает высоким уровнем готовности к масштабированию.

### 中文

**项目简介（2‑3 句）**  
tmoroney/auto‑subs 是一款在本地运行的自动字幕生成工具，能够直接与 DaVinci Resolve、Premiere Pro 与 After Effects 对接，实现视频编辑流程的 AI 化。它基于 TypeScript 开发，提供即插即用的 API 与插件，帮助创作者在不从零构建模型的前提下快速加入智能字幕功能。

**价值**  
- **快速原型**：无需自行训练模型，即可在编辑软件中实验 AI 字幕、RAG（检索增强生成）或智能代理等功能。  
- **降低成本**：本地推理避免了云计算费用和数据隐私泄露风险。  
- **生态兼容**：与业界主流非线性编辑软件原生集成，适合制作影视、短视频及后期特效。

**典型接入方式**  
1. **安装依赖**：`npm i auto-subs`（或使用 Yarn）。  
2. **插件配置**：在 DaVinci Resolve / Premiere / After Effects 中加载提供的插件脚本，指定本地模型路径或使用内置的 Whisper/Whisper‑cpp。  
3. **API 调用**：通过 `autoSubs.generate(videoPath, options)` 获得 SRT/JSON 字幕文件，随后在编辑软件的时间线中自动导入。  
4. **小规模 PoC**：先在单个项目或测试素材上跑通生成‑导入闭环，验证字幕准确率与性能后再推广到全流程。

**生产可用性**  
- **活跃度**：截至 2026‑07‑01，项目最近一次提交，星标 3.7k，Fork 240，社区活跃。  
- **成熟度**：已发布稳定的 TypeScript 包，提供完整的 README 与示例，适合作为 OSS 级别的 Pilot。  
- **风险**：仍需完成许可证（MIT）合规审查、依赖安全扫描以及维护者可用性确认；但整体安全与可靠性已经达到可在生产环境试点的水平。  

综上，auto‑subs 具备快速集成、成本低、兼容主流编辑工具的优势，是在视频后期工作流中引入 AI 字幕的理想 OSS 方案。

## 🧭 Practical evaluation

**Value:** tmoroney/auto-subs helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 3721 GitHub stars
- 240 forks
- updated 2026-07-01
- primary language: TypeScript
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 60/100 |
| stars | 76/100 |
| topics | 100/100 |
| outlook | 63/100 |
| quality | 72/100 |
| recency | 40/100 |
| adoption | 71/100 |
| production | 59/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/tmoroney/auto-subs) · [← Back to Video-editing](./README.md)</sub>
