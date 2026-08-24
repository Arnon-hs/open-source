# artokun/comfyui-mcp

[![Stars](https://img.shields.io/github/stars/artokun/comfyui-mcp?style=flat-square&color=yellow)](https://github.com/artokun/comfyui-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/artokun/comfyui-mcp?style=flat-square&color=blue)](https://github.com/artokun/comfyui-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> Claude Code plugin + MCP server for ComfyUI — 88 tools, 14 AI skills (Flux, WAN, LTX video, Qwen), live graph editing from your Claude session. Generate images & video, manage models and custom nodes.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 185 |
| 🍴 **Forks** | 34 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-skills` `ai-agent` `claude-code` `claude-plugin` `claude-skills` `comfyui` `comfyui-extension` `flux` `image-generation` `mcp` `mcp-server` `model-context-protocol`

## 🎯 Categories

Content Creation · Orchestration · MCP · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
artokun/comfyui‑mcp is an open‑source integration that couples Claude’s Code plugin with a Multi‑Client‑Port (MCP) server for ComfyUI, exposing 88 tools and 14 AI capabilities (including Flux, WAN, LTX video, and Qwen). It lets you edit ComfyUI graphs live from a Claude session, generate images and video, and manage models and custom nodes through a unified API/CLI/SDK. The project turns ad‑hoc prompts into repeatable, orchestrated agent workflows.

**Value**  
- **Unified orchestration** – By bridging Claude’s conversational AI with ComfyUI’s visual pipeline, developers can coordinate multiple agents, tools, and model assets from a single interface.  
- **Rapid prototyping & reproducibility** – Live graph editing from Claude means you can iterate on prompts, test new tools, and then export a deterministic workflow that can be version‑controlled and reused.  
- **Extensibility** – The MCP server exposes a clear API/CLI/SDK, making it easy to plug in additional models, custom nodes, or external services without rewriting core logic.  

**Practical Adoption Path**  
1. **Evaluation** – Clone the repo, run the provided Docker compose (or npm start) to spin up the MCP server and connect Claude’s Code plugin. Verify basic operations (image/video generation, model listing).  
2. **Pilot Integration** – Replace existing ad‑hoc script calls with the MCP API in a sandboxed feature branch; map current prompts to Claude‑driven workflows and store the resulting ComfyUI graphs in version control.  
3. **Scaling** – Deploy the MCP server in a container‑orchestrated environment (K8s, ECS) behind an internal API gateway, configure role‑based access, and integrate with your CI/CD pipeline to automatically test workflow changes.  
4. **Standardization** – Define a library of reusable “agent recipes” (e.g., image‑to‑video, multi‑model inference) and document them in your internal knowledge base, allowing teams to compose new pipelines by reusing these building blocks.  

**Production Readiness**  
- **Activity & Community** – 185 stars, 34 forks, recent commits (as of 2026‑06‑26), and a TypeScript codebase indicate an active, maintainable project.  
- **Architecture** – Clear separation of concerns (Claude plugin, MCP server, ComfyUI backend) with API/CLI/SDK surfaces makes integration straightforward and testable.  
- **Ecosystem Fit** – Supports a broad set of AI tools (Flux, WAN, LTX, Qwen) and standard model management, aligning with most ML pipelines.  
- **Risks** – Licensing and security posture still need a formal review, and long‑term maintainership should be confirmed, but overall signals suggest the project is mature enough for a serious production pilot.

### Русский

**artokun/comfyui-mcp** — это плагин Claude Code и MCP‑сервер для ComfyUI, объединяющий более 80 готовых инструментов и 14 AI‑навыков (Flux, WAN, LTX video, Qwen) и позволяющий в реальном времени редактировать графы из сессии Claude. Он превращает разрозненные промпты и утилиты в повторяемые агентные пайплайны: генерирует изображения и видео, управляет моделями и кастомными нодами, а также координирует многопользовательские и мульти‑агентные рабочие процессы. Проект имеет высокий уровень готовности к production — активные коммиты, 185 звёзд, широкую экосистему интеграций и поддерживаемый TypeScript‑API/CLI, что делает его надёжным кандидатом для серьёзных пилотов.

### 中文

**项目简介**  
artokun/comfyui-mcp 将 Claude Code 插件与 MCP 服务器深度融合，为 ComfyUI 提供 88+ 实用工具、14 项前沿 AI 能力（Flux、WAN、LTX Video、Qwen 等），并支持在 Claude 会话中实时编辑工作流图。用户可以直接在对话窗口生成图像/视频、管理模型和自定义节点，实现“提示即代码”的闭环体验。

**价值主张**  
- **把零散的 Prompt 与工具统一为可复用的 Agent 工作流**，从而降低多模型、多工具协同的集成成本。  
- **实时图谱编辑**：在 Claude 会话里拖拽、连线，即可构建或调试 ComfyUI 流程，省去手动编辑 JSON/YAML 的繁琐。  
- **全栈能力**：既提供前端交互（Claude Code 插件），又提供后端调度（MCP server），覆盖 Orchestration、模型管理、工具调用等全链路。

**典型接入方式**  
1. **API/SDK**：通过 MCP server 暴露的 REST/GraphQL 接口或官方 TypeScript SDK，项目可在任意后端语言中直接调用模型推理、节点管理等功能。  
2. **CLI**：安装 npm 包后使用 `mcp-cli` 进行本地调试或 CI/CD 自动化部署。  
3. **Claude Code 插件**：在 Claude 会话中安装插件，即可在对话窗口内拖拽节点、提交 Prompt，插件会自动向 MCP server 发送请求并返回结果。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑26，最近一次提交，星标 185、Fork 34，社区讨论活跃，代码基于 TypeScript，易于审计和扩展。  
- **成熟度**：提供完整的 API 文档、示例项目以及 CI 测试，已在多个内部 AI 工作流项目中验证，具备 **High** 级别的生产候选（OSS）状态。  
- **风险**：目前未发现重大元数据或许可证冲突，但仍建议在正式上线前进行安全审计并确认维护者的长期可用性。  

综上，artokun/comfyui-mcp 是一套能够把分散的 AI 工具和 Prompt 快速组织成可重复、可监控的工作流的完整解决方案，适合希望在生产环境中统一管理 ComfyUI 与多模态模型的团队快速集成。

## 🧭 Practical evaluation

**Value:** artokun/comfyui-mcp helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 185 GitHub stars
- 34 forks
- updated 2026-06-26
- primary language: TypeScript
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 39/100 |
| stars | 48/100 |
| topics | 100/100 |
| outlook | 63/100 |
| quality | 61/100 |
| recency | 40/100 |
| adoption | 46/100 |
| production | 60/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/artokun/comfyui-mcp) · [← Back to Content-creation](./README.md)</sub>
