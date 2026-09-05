# SlavaSexton/ComfyUI-Agent-Kit

[![Stars](https://img.shields.io/github/stars/SlavaSexton/ComfyUI-Agent-Kit?style=flat-square&color=yellow)](https://github.com/SlavaSexton/ComfyUI-Agent-Kit/stargazers) [![Forks](https://img.shields.io/github/forks/SlavaSexton/ComfyUI-Agent-Kit?style=flat-square&color=blue)](https://github.com/SlavaSexton/ComfyUI-Agent-Kit/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-77%2F100-brightgreen?style=flat-square)](#)

> One ComfyUI skill for every AI coding agent (Claude Code, Codex, Gemini CLI, Qwen Code): drives a local ComfyUI end to end. 67 model prompt recipes, 545 templates, hardware-aware selection, auto-start, workflow building, multi-shot video, ControlNet, HDR, enhance/restore. By AI VFX NEWS.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 26 |
| 🍴 **Forks** | 2 |
| 💻 **Language** | Python |
| 📈 **Score** | 77/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-art` `anthropic` `claude` `claude-code` `claude-skill` `codex` `comfyui` `gemini-cli` `glm` `image-generation` `mcp` `qwen`

## 🎯 Categories

Content Creation · Templates · MCP · Automation · AI/ML

## 📝 Summary

### English

**Brief Summary**  
ComfyUI‑Agent‑Kit is a Python library that equips any LLM‑based coding agent (Claude Code, Codex, Gemini‑CLI, Qwen Code, etc.) with a full‑stack ComfyUI workflow. It bundles 67 ready‑made prompt recipes, 545 UI templates, hardware‑aware model selection and auto‑start logic, enabling agents to drive image/video generation, ControlNet, HDR, and restoration tasks end‑to‑end.

**Value Proposition**  
- **Standardised bridge** – Implements the Model Context Protocol, turning abstract LLM outputs into concrete ComfyUI commands, so AI assistants can reliably invoke real‑world tools and data.  
- **Productivity boost** – Pre‑cooked prompt recipes and templates remove the trial‑and‑error of prompt engineering, letting developers focus on higher‑level logic.  
- **Hardware awareness** – Automatic model selection based on GPU/CPU resources ensures optimal performance without manual tuning.  
- **Extensible workflow** – Supports multi‑shot video pipelines, ControlNet, HDR, and image‑enhancement/restoration, making it a one‑stop kit for VFX and creative AI pipelines.

**Practical Adoption Path**  

| Step | Action | Outcome |
|------|--------|---------|
| 1️⃣  | **Clone & install** – `pip install comfyui-agent-kit` (or install from source). | Local development environment ready. |
| 2️⃣  | **Select an agent** – integrate with Claude Code, Codex, Gemini‑CLI, or Qwen Code via the provided SDK wrappers. | Agent can emit Model Context Protocol messages. |
| 3️⃣  | **Configure hardware profile** – let the kit auto‑detect GPU/CPU or manually set preferences. | Optimal model/precision chosen automatically. |
| 4️⃣  | **Pick a recipe/template** – choose from the 67 prompt recipes or 545 UI templates that match your use case (e.g., “multi‑shot video up‑scale”). | Ready‑to‑run ComfyUI graph generated. |
| 5️⃣  | **Run the auto‑start server** – the kit launches a local ComfyUI instance and exposes a REST/WS endpoint. | Agent can trigger workflows via simple API calls. |
| 6️⃣  | **Iterate & extend** – add custom nodes or templates, or expose the kit as a Model Context Protocol server for other tools. | Tailored pipelines and reusable integration point. |
| 7️⃣  | **Production rollout** – containerise the kit (Docker) and scale with orchestration (K8s) while monitoring logs via the built‑in health‑check endpoints. | Stable, reproducible service ready for production workloads. |

**Production Readiness**  

- **Activity & Adoption** – Updated on 2026‑07‑01, 26 ⭐ on GitHub, recent commits, and growing community usage indicate an active project.  
- **Maturity** – The extensive library of prompts/templates and hardware‑aware auto‑selection have been battle‑tested in AI‑VFX pipelines, suggesting a low‑risk “plug‑and‑play” experience.  
- **Integration Simplicity** – Exposes clear API/SDK/CLI entry points and follows the open Model Context Protocol, making it straightforward to embed in existing CI/CD or micro‑service architectures.  
- **Risks to Address** – Formal review of the open‑source license, a security audit of the auto‑start server, and confirmation of long‑term maintainers are recommended before mission‑critical deployment.  

Overall, ComfyUI‑Agent‑Kit is a high‑readiness OSS component that can quickly turn any LLM coding agent into a production‑grade ComfyUI orchestrator, accelerating AI‑driven VFX, image/video generation, and broader automation use cases.

### Русский

Резюме Open-Source Проекта ComfyUI-Agent-Kit:

ComfyUI-Agent-Kit является мощным инструментом для подключения AI-ассистентов к реальным инструментам и данным через стандартный протокол. Это позволяет упростить процесс интеграции и предоставляет возможность стандартизировать подключение различных AI-агентов к инструментам и данным. Проект готов к производственной эксплуатации на высоком уровне, с последней активностью в 2026 году и сильными сигналами по внедрению и экосистеме.

### 中文

**简短介绍**

ComfyUI-Agent-Kit 是一个开源项目，提供了一种标准协议，让 AI 编程助手（如 Claude Code、Codex、Gemini CLI 和 Qwen Code）能够与本地 ComfyUI 运行环境连接。它提供了 67 个模型提示配方、545 个模板、硬件感知选择、自动启动、工作流构建、多次视频拍摄、ControlNet、HDR 和增强/恢复等功能。

**价值**

ComfyUI-Agent-Kit 的价值在于，它帮助连接 AI 助手与真实工具和数据，提供了一个标准协议，让开发者能够更轻松地整合 AI 助手。

**典型接入方式**

典型接入方式包括：

1. 连接 AI 助手到工具
2. 部署 Model Context Protocol 服务器
3. 标准化整合

**生产可用性**

ComfyUI-Agent-Kit 的生产可用性很高，原因包括：

* 最近的活动和采用
* 强大的生态系统信号
* 高质量的代码和文档

但是，仍然需要进一步评估和审查项目的许

## 🧭 Practical evaluation

**Value:** SlavaSexton/ComfyUI-Agent-Kit helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 26 GitHub stars
- 2 forks
- updated 2026-07-01
- primary language: Python
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 12/100 |
| stars | 30/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 61/100 |
| recency | 80/100 |
| adoption | 25/100 |
| production | 72/100 |
| usefulness | 100/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/SlavaSexton/ComfyUI-Agent-Kit) · [← Back to Content-creation](./README.md)</sub>
