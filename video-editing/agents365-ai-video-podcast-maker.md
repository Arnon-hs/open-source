# Agents365-ai/video-podcast-maker

[![Stars](https://img.shields.io/github/stars/Agents365-ai/video-podcast-maker?style=flat-square&color=yellow)](https://github.com/Agents365-ai/video-podcast-maker/stargazers) [![Forks](https://img.shields.io/github/forks/Agents365-ai/video-podcast-maker?style=flat-square&color=blue)](https://github.com/Agents365-ai/video-podcast-maker/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Topic → 4K narrated video for coding agents. v3.0 Asset Engine: manifest-based asset layer (user files / stock / AI images / AI B-roll / Hyperframes overlays), 11 TTS backends, Remotion composition, cost-gated AI generation

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.4k |
| 🍴 **Forks** | 147 |
| 💻 **Language** | Python |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-skill` `ai-video` `bilibili` `claude-code` `hyperframes` `idea-to-video` `remotion` `text-to-speech` `video-generation`

## 🎯 Categories

Video Editing · Content Creation · AI/ML

## 📝 Summary

### English

**Brief Summary**  
Agents365‑ai/video‑podcast‑maker is an open‑source pipeline for generating 4K narrated videos that combine user‑provided assets, stock media, AI‑generated images, B‑roll, and Hyperframe overlays. It ships a manifest‑driven asset engine, 11 text‑to‑speech back‑ends, Remotion‑based video composition, and cost‑gated AI generation, letting developers add sophisticated video‑AI capabilities without building a stack from scratch.  

**Value**  
- **Accelerated prototyping** – developers can prototype AI‑driven video features (e.g., coding‑agent tutorials, walkthroughs, or RAG‑enhanced explainers) by simply defining a manifest of assets rather than writing low‑level media handling code.  
- **Modular TTS & media mix** – the 11 TTS providers and plug‑in‑style asset layers let teams experiment with voice quality, language support, and visual styles while keeping costs under control via the built‑in gating.  
- **Reusable workflow** – the same pipeline can be reused across projects (agent demos, product marketing, educational content), reducing duplicated effort and ensuring consistent branding.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the provided README example, and replace the sample manifest with a minimal set of your own assets (e.g., a short script and a couple of stock clips).  
2. **Integration** – Wrap the CLI or Python API into your CI/CD pipeline; connect your own TTS subscription or the free back‑ends you need.  
3. **Scale** – Extend the manifest to include AI‑generated images or Hyperframe overlays, and enable the cost‑gated generation to keep cloud spend predictable.  
4. **Productionize** – Containerize the service, add monitoring for asset download failures and TTS latency, and integrate with your existing RAG or agent orchestration layer.  

**Production Readiness**  
The project scores high on readiness: recent commits (as of 2026‑07‑12), 1.4 k GitHub stars, active forks, and a Python codebase with clear modularity. The ecosystem signals (Remotion for video composition, multiple TTS providers) are mature, and the manifest‑driven design simplifies maintenance. While a final license and security audit are still required, the overall health and community activity make it a solid candidate for a serious pilot or even full production deployment after the standard hardening steps.

### Русский

**Agents365‑ai/video-podcast-maker** — это open‑source‑платформа на Python, позволяющая быстро добавить в проект возможности генерации 4K видеоподкастов с озвучкой: слой активов (пользовательские файлы, стоковые материалы, AI‑изображения, B‑roll, Hyperframe‑оверлеи), 11 TTS‑бэкендов, компоновка через Remotion и платёжный контроль за AI‑генерацией. Типичный сценарий — прототипирование новых AI‑фич, построение RAG‑ или агентных воркфлоу и оценка инструментов модели, начиная с небольшого proof‑of‑concept и проверки README. Проект считается почти готовым к production: активные коммиты (последний — 12 июля 2026), 1,4 к звёзд, 147 форков, сильные сигналы экосистемы, хотя лицензия, безопасность и поддержка требуют окончательной валидации.

### 中文

**项目简介**  
Agents365‑ai/video-podcast-maker 是一款面向代码代理的 4K 口播视频生成工具，v3.0 引入了基于 manifest 的资产层（支持用户文件、素材库、AI 生成图片、AI B‑roll、Hyperframes 覆盖层），集成了 11 种 TTS 后端、Remotion 视频合成以及成本门控的 AI 生成模块。

**价值**  
- **快速赋能 AI 能力**：无需从零搭建模型栈，直接复用成熟的 TTS、图像/视频生成和 Remotion 合成组件。  
- **原型与研发加速**：适用于快速原型化 AI 功能、构建 RAG/Agent 工作流以及评估模型工具链的效果。  
- **高质量输出**：支持 4K 分辨率、可自定义资产层和多种配音后端，满足专业级视频播客的制作需求。

**典型接入方式**  
1. **阅读 README**：确认环境依赖（Python、Node、Remotion）并完成初始配置。  
2. **准备 Manifest**：在 `manifest.yaml` 中声明所需的用户文件、库存素材、AI 生成图片或 B‑roll。  
3. **选择 TTS 后端**：通过配置文件或环境变量指定 11 种 TTS 之一（如 Azure、Google、ElevenLabs 等）。  
4. **运行生成**：执行 `python generate.py --manifest manifest.yaml`，系统会自动调度资产、调用 AI 生成、完成 Remotion 合成并输出 4K 视频。  
5. **成本门控**：如需限制 AI 调用费用，可在 `config.yaml` 中设置预算阈值，超出后自动切换为本地或低成本模型。

**生产可用性**  
- **活跃度**：截至 2026‑07‑12，项目仍在持续更新，拥有 1.4k+ GitHub stars、147 个 fork，社区活跃。  
- **技术成熟度**：核心功能已在多个内部项目中验证，Remotion 与多家 TTS 服务的集成经过实战测试。  
- **风险评估**：暂无重大元数据风险，需进一步审查许可证（MIT）和安全依赖（尤其是 Node 包）。  
- **上线建议**：先在沙箱环境完成小规模 PoC，确认资产层、成本门控与 CI/CD 流程的兼容性后，再推广至生产环境。整体来看，该项目具备较高的 OSS 候选人成熟度，适合作为 AI 视频生成的底层平台进行正式部署。

## 🧭 Practical evaluation

**Value:** Agents365-ai/video-podcast-maker helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1430 GitHub stars
- 147 forks
- updated 2026-07-12
- primary language: Python
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 54/100 |
| stars | 67/100 |
| topics | 100/100 |
| outlook | 61/100 |
| quality | 69/100 |
| recency | 40/100 |
| adoption | 64/100 |
| production | 60/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/Agents365-ai/video-podcast-maker) · [← Back to Video-editing](./README.md)</sub>
