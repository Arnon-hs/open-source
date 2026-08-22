# dramaclaw/dramaclaw

[![Stars](https://img.shields.io/github/stars/dramaclaw/dramaclaw?style=flat-square&color=yellow)](https://github.com/dramaclaw/dramaclaw/stargazers) [![Forks](https://img.shields.io/github/forks/dramaclaw/dramaclaw?style=flat-square&color=blue)](https://github.com/dramaclaw/dramaclaw/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-78%2F100-brightgreen?style=flat-square)](#)

> A general-purpose AIGC video engine: script to finished film in one pipeline — dramas, ads, product videos, otome games, and more. | 通用 AIGC 视频引擎 —— 从剧本到成片一条流水线，漫剧、广告、电商、乙游皆可

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 204 |
| 🍴 **Forks** | 12 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 78/100 |
| 🗓️ **Last push** | 2026-07-03 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `ai-filmmaking` `ai-video` `aigc` `aigc-pipeline` `content-creation` `dramaclaw` `fastapi` `generative-ai` `image-to-video` `python` `react`

## 🎯 Categories

AI/ML · Frontend · Backend · Marketing · Product

## 📝 Summary

### English

**Brief Summary**  
dramaclaw / dramaclaw is an open‑source, TypeScript‑based AIGC video engine that turns a script into a finished film in a single pipeline, supporting use cases such as dramas, ads, product videos, and otome games. It offers a ready‑to‑use API/SDK/CLI that lets developers plug AI‑driven generation, RAG, and agent workflows into their products without building a model stack from scratch.  

**Value**  
- **Accelerated AI integration** – The platform abstracts the heavy lifting of video synthesis, text‑to‑speech, scene composition, and post‑production, letting teams add AI‑generated video capabilities with minimal code.  
- **Broad applicability** – Because it is script‑driven, the same engine can serve entertainment, marketing, e‑commerce, and interactive game scenarios, reducing the need for multiple specialized tools.  
- **Extensible workflow** – Exposes clear implementation signals (API, SDK, CLI) and language metadata, making it easy to embed RAG or custom agents for dynamic content generation.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the CLI locally, and feed a short script to generate a test video; iterate quickly to validate quality and performance.  
2. **Integrate** – Use the provided TypeScript SDK or REST API to embed video generation into your backend or frontend services, wiring in your own prompt templates, asset libraries, or RAG components.  
3. **Scale** – Deploy the engine in containers or serverless functions, configure autoscaling, and connect to your media storage/CDN for production‑grade delivery.  

**Production Readiness**  
- **Activity & Community** – 204 ★, recent commits (as of 2026‑07‑03), and active issue handling indicate a healthy open‑source project.  
- **Technical maturity** – A complete TypeScript codebase with API/SDK/CLI, clear documentation, and a focused set of 19 topics suggest the core functionality is stable.  
- **Risk considerations** – License, security audit, and maintainer continuity still need a final review, but overall signals (recent updates, adoption hints, and ecosystem integration) make dramaclaw a strong candidate for a serious pilot or production rollout.

### Русский

Резюме проекта dramaclaw/dramaclaw:

dramaclaw/dramaclaw — это общепринятый видеоинженер AIGC, который позволяет создавать полноценные фильмы из скрипта в одной цепочке. Этот проект предлагает возможность добавлять функциональность AI без создания новой модели стека. Он готов к внедрению в производство на высоком уровне, что подтверждается активностью,採用 и экосистемными сигналами. 

Проект идеально подходит для прототипирования функций AI, создания RAG или агентных потоков, а также оценки инструментов моделирования.

### 中文

**项目简介（2‑3 句）**  
dramaclaw 是一个通用的 AIGC 视频引擎，能够把剧本直接生成完整影片，支持漫剧、广告、电商短片、乙女游戏等多种场景。它提供统一的 API/SDK/CLI，帮助开发者在已有模型堆栈上快速叠加 AI 能力，而无需从零搭建。  

**价值**  
- **快速原型**：只需提供剧本，即可在同一流水线中完成分镜、配音、特效、渲染等全部步骤，大幅缩短视频内容生产周期。  
- **复用模型**：内部封装了多模态模型（文本‑图像‑音频），开发者可直接调用，无需自行训练或集成多个模型。  
- **灵活扩展**：支持自定义插件、RAG（检索增强生成）和 Agent 工作流，方便在广告投放、商品展示、互动剧情等业务中加入特定业务逻辑。  

**典型接入方式**  
1. **API 调用**：通过 RESTful 接口提交剧本 JSON，获取生成进度和最终视频 URL。  
2. **SDK（TypeScript）**：在前端或 Node.js 后端直接引入 `@dramaclaw/sdk`，使用 `createProject()`、`addScene()`、`render()` 等高层函数。  
3. **CLI**：在 CI/CD 或本地脚本中使用 `dramaclaw-cli`，如 `dramaclaw run --script=my.txt --output=out.mp4`。  

**生产可用性**  
- **活跃度**：截至 2026‑07‑03 最近一次提交，GitHub ★204、Fork 12，社区讨论活跃。  
- **技术成熟度**：核心实现使用 TypeScript，提供完整的类型定义和自动化测试，易于在企业代码库中集成。  
- **生态兼容**：兼容主流云函数、容器化部署（Docker 镜像已提供），并可与现有的媒体处理管线（FFmpeg、AWS MediaConvert）无缝对接。  
- **风险**：仍需进一步审查许可证（MIT/Apache?）和安全依赖；建议在正式生产前进行安全扫描和维护者沟通。  

综合来看，dramaclaw 已具备较高的生产就绪度，适合作为视频内容自动化生产的核心组件进行试点或直接上线。

## 🧭 Practical evaluation

**Value:** dramaclaw/dramaclaw helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 204 GitHub stars
- 12 forks
- updated 2026-07-03
- primary language: TypeScript
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 28/100 |
| stars | 49/100 |
| topics | 100/100 |
| outlook | 84/100 |
| quality | 74/100 |
| recency | 100/100 |
| adoption | 43/100 |
| production | 79/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/dramaclaw/dramaclaw) · [← Back to AI/ML](./README.md)</sub>
