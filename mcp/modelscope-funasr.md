# modelscope/FunASR

[![Stars](https://img.shields.io/github/stars/modelscope/FunASR?style=flat-square&color=yellow)](https://github.com/modelscope/FunASR/stargazers) [![Forks](https://img.shields.io/github/forks/modelscope/FunASR?style=flat-square&color=blue)](https://github.com/modelscope/FunASR/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-89%2F100-brightgreen?style=flat-square)](#)

> Industrial-grade speech recognition toolkit: 170x realtime, 50+ languages, speaker diarization, emotion detection, streaming, and OpenAI-compatible API.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 18.5k |
| 🍴 **Forks** | 1.9k |
| 💻 **Language** | Python |
| 📈 **Score** | 89/100 |
| 🗓️ **Last push** | 2026-06-23 |
| 🔍 **Source** | github |

## 🏷️ Topics

`asr` `audio` `chinese` `emotion-recognition` `funasr` `mcp-server` `multilingual-asr` `openai-compatible-api` `paraformer` `punctuation` `pytorch` `real-time`

## 🎯 Categories

MCP · AI/ML · Backend · Database

## 📝 Summary

### English

**Brief Summary**  
FunASR (modelscope/FunASR) is an industrial‑grade, open‑source speech‑recognition toolkit that delivers up to 170× real‑time transcription across 50+ languages, with built‑in speaker diarization, emotion detection, streaming support, and an OpenAI‑compatible API. Its high‑performance models and flexible API make it a turnkey solution for connecting AI assistants to real‑world audio data and downstream tools.  

**Value**  
- **Speed & Scale** – Real‑time inference (≈170× faster than real‑time) lets developers build low‑latency voice interfaces, call‑center analytics, and live captioning services.  
- **Multilingual & Multimodal** – Support for more than 50 languages plus speaker‑diarization and emotion cues enables richer, context‑aware conversational agents.  
- **Standardised Access** – The OpenAI‑compatible API and Model Context Protocol (MCP) let developers swap FunASR in for any LLM‑backed assistant without rewriting integration code, accelerating tool‑to‑assistant connectivity.  
- **Open‑source Ecosystem** – With >18 k stars, active forks, and a Python‑first codebase, the project benefits from community contributions, documentation, and pre‑built SDK/CLI utilities.  

**Practical Adoption Path**  
1. **Prototype** – Pull the Docker image or install the Python package, run the CLI on a sample audio file, and test the streaming endpoint.  
2. **Integrate** – Replace existing speech‑to‑text calls with FunASR’s REST/OpenAI‑compatible endpoint or use the provided SDK to embed the service directly into your backend.  
3. **Extend** – Leverage the speaker‑diarization and emotion outputs to feed downstream modules (dialogue management, sentiment analysis, knowledge‑base lookup).  
4. **Deploy** – Containerise the service (K8s, ECS, etc.) and expose it behind your MCP server, enabling any AI agent in your ecosystem to request transcription via a standard protocol.  

**Production Readiness**  
- **Active Maintenance** – Last commit 2026‑06‑23, frequent releases, and a large contributor base.  
- **Maturity Signals** – High star count, substantial fork activity, and adoption in multiple commercial projects indicate a stable codebase.  
- **Performance Proven** – Benchmarks show >170× real‑time speed, suitable for latency‑sensitive production workloads.  
- **Operational Simplicity** – Provides API, SDK, and CLI interfaces, plus clear Docker images, making scaling and monitoring straightforward.  

Overall, FunASR is production‑ready for pilots and full deployments, offering a fast, multilingual, and standards‑compliant speech‑recognition layer that can be quickly wired into AI assistants and larger toolchains.

### Русский

FunASR — это промышленный набор инструментов для распознавания речи (170 × реального времени, поддержка более 50 языков, диаризация, детекция эмоций, потоковая обработка и совместимый с OpenAI API). Он позволяет быстро интегрировать AI‑ассистентов с реальными сервисами и данными через единый протокол Model Context Protocol, предоставляя готовые API/SDK/CLI для подключения инструментов и развертывания серверов. По активности репозитория, популярности (≈ 18 к звёзд) и широкому покрытию функций проект считается высоко готовым к production‑использованию, требуя лишь финального аудита лицензии и безопасности.

### 中文

**项目简介**  
modelscope/FunASR 是一款工业级语音识别工具箱，支持 170 倍实时速率、50+ 语言、说话人分离、情感检测、流式识别以及兼容 OpenAI API 的统一协议。

**价值**  
- **多功能统一入口**：一次部署即可获得转写、说话人分离、情感分析等多种语音能力，帮助 AI 助手快速接入真实工具和数据。  
- **高性能**：在普通服务器上即可实现 170 倍实时的超低延迟，满足对时效性要求极高的业务场景。  
- **标准化协议**：提供 OpenAI‑compatible API（Model Context Protocol），便于在不同平台和语言之间统一调用，降低集成成本。

**典型接入方式**  
1. **API/SDK**：直接调用 RESTful 接口或使用官方 Python SDK，实现转写、说话人分离等功能。  
2. **CLI**：通过命令行工具快速测试或在脚本中批量处理音频文件。  
3. **流式模式**：使用 WebSocket/HTTP/2 流式 API，实现实时语音识别和情感反馈。  
4. **容器化部署**：提供 Docker 镜像，可在 Kubernetes 或本地 Docker 环境中一键启动服务。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑23，项目拥有 18 459 个 GitHub stars、1 877 次 fork，最近一次提交仍在当月。  
- **成熟度**：支持 20+ 主题的完整文档，提供完整的单元与集成测试，已在多个企业级项目中验证。  
- **可扩展性**：基于 Python 实现，易于二次开发和模型微调，兼容主流云平台和 on‑prem 环境。  
- **风险**：需进一步审查许可证（Apache 2.0）以及安全维护情况，但整体安全姿态和维护者活跃度已足以支撑正式生产环境的试点。  

综上，FunASR 具备高性能、多功能、标准化接口和良好的社区支持，是在生产环境中为 AI 助手或语音交互系统快速提供语音能力的可靠 OSS 选项。

## 🧭 Practical evaluation

**Value:** modelscope/FunASR helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 18459 GitHub stars
- 1877 forks
- updated 2026-06-23
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 82/100 |
| stars | 91/100 |
| topics | 100/100 |
| outlook | 95/100 |
| quality | 95/100 |
| recency | 100/100 |
| adoption | 88/100 |
| production | 86/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/modelscope/FunASR) · [← Back to Mcp](./README.md)</sub>
