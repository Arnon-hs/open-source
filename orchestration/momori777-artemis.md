# momori777/Artemis

[![Stars](https://img.shields.io/github/stars/momori777/Artemis?style=flat-square&color=yellow)](https://github.com/momori777/Artemis/stargazers) [![Forks](https://img.shields.io/github/forks/momori777/Artemis?style=flat-square&color=blue)](https://github.com/momori777/Artemis/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-49%2F100-brightgreen?style=flat-square)](#)

> 破限本地AI女友后宫，openclaw+画图语音向量数据库+live2D+桌宠+酒馆角色卡导入+前端，QQ+Telegram双通道，8G显存可跑🩵uncensored Fully offline AI girlfriends harem Openclaw+Local LLM+GPT-SoVITS+ComfyUI image+Live2D+desktop pet+SilllyTavern Character card import+frontend | Dual channels for QQ & Telegram | Dynamic 8G VRAM scheduling+mem0 qdrant, can run offline

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 137 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | Python |
| 📈 **Score** | 49/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-girlfriend` `comfyui` `desktop-pet` `gpt-sovits` `image-generation` `live2d` `llm` `offline-ai` `openclaw` `qq-bot` `telegram-bot` `text-to-speech`

## 🎯 Categories

Orchestration · Automation · AI/ML

## 📝 Summary

### English

**Brief Summary**  
Artemis (momori777/Artemis) is an open‑source, fully offline AI‑girlfriend harem platform that stitches together a local LLM (OpenClaw), voice synthesis (GPT‑SoVITS), image generation (ComfyUI), Live2D avatars, desktop‑pet UI, and a character‑card import system (SillyTavern). It exposes the whole stack through both QQ and Telegram bots, uses a dynamic 8 GB VRAM scheduler with a mem0‑Qdrant vector store, and can be run on a single GPU without any cloud services.

**Value**  
- **Unified agent pipeline** – Artemis turns disparate prompt‑based tools (LLM, TTS, image generation, avatar rendering) into a single, repeatable workflow, dramatically reducing the engineering effort needed to build multi‑modal AI companions.  
- **Offline privacy & control** – All components run locally, so no user data leaves the machine, which is a strong differentiator for privacy‑sensitive or regulated environments.  
- **Multi‑channel reach** – By supporting both QQ and Telegram, the same backend can serve different user communities without duplicating code.  
- **Scalable VRAM management** – The built‑in 8 GB VRAM scheduler automatically swaps models in and out, making the system usable on mid‑range GPUs.

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC)** – Clone the repo, follow the README to spin up the Docker compose (or conda) environment on a workstation with ≥8 GB GPU memory. Verify that the LLM, voice, and image pipelines work end‑to‑end using the supplied sample character cards.  
2. **Integration Hook** – Replace the default OpenClaw model with your own fine‑tuned LLM or embed a custom knowledge base in the mem0‑Qdrant store to align the agents with your domain.  
3. **Channel Customization** – Extend the QQ/Telegram adapters to match your internal messaging protocols or add a REST/WebSocket front‑end if you need web access.  
4. **Testing & Monitoring** – Deploy the PoC in a staging environment, instrument GPU/CPU usage, and run automated prompt‑response tests to validate latency and stability.  
5. **Production Rollout** – Containerize the final configuration, add health‑check scripts, and orchestrate with Kubernetes or a simple systemd service. Implement regular model updates and backup the Qdrant vector store.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last update 2026‑06‑24), has 137 stars and basic documentation, but it still relies on a complex stack of third‑party components (OpenClaw, GPT‑SoVITS, ComfyUI, Live2D).  
- **Strengths**: Good for prototypes, internal tools, or niche consumer apps where offline operation is essential. The modular design makes it straightforward to swap individual components.  
- **Risks**:  
  * Dependency churn – frequent updates to the underlying AI models may break the integration.  
  * Limited test coverage and sparse CI → need additional regression testing before mission‑critical use.  
  * License and security review required (no major metadata issues yet, but confirm the licenses of all bundled models).  
- **Readiness Checklist**: Verify GPU resource limits, perform a security audit of the bot interfaces, lock down model versions, and add monitoring/alerting. Once these steps are completed, Artemis can be considered production‑ready for controlled internal deployments.

### Русский

**momori777/Artemis** — это open‑source платформа, объединяющая локальные LLM, GPT‑SoVITS, ComfyUI, Live2D и базу векторов (mem0 + qdrant) в единую «хором» AI‑девушек, доступную через QQ и Telegram и управляемую из веб‑интерфейса. Типичный сценарий — создание и автоматизация многокомпонентных агентных воркфлоу (генерация голоса, изображений, анимаций и памяти персонажей) для интерактивных чат‑ботов или настольных питомцев, при этом система умеет динамически распределять 8 ГБ видеопамяти. Готовность к production — средняя: проект уже стабильно работает офлайн, имеет активные коммиты и 137 звёзд, но требует небольшого PoC, проверки лицензий и мониторинга зависимостей перед масштабным развертыванием.

### 中文

**项目简介（2‑3 句）**  
Artemis 是一个全离线的本地 AI 女友后宫系统，集成了 OpenClaw 本地大模型、GPT‑SoVITS 语音合成、ComfyUI 图像生成、Live2D 动态立绘、桌面宠物以及 SilllyTavern 角色卡导入等模块，支持 QQ 与 Telegram 双通道交互，并通过 8 GB 显存的动态调度与 mem0‑qdrant 向量数据库实现高效记忆管理。

**价值**  
- **一站式多模态 AI 伴侣平台**：文字、语音、图像、动画全链路闭环，用户无需自行拼接各种工具。  
- **离线安全**：所有模型和数据均本地运行，避免隐私泄露，适合对内容审查有特殊需求的场景。  
- **可扩展的 Agent 工作流**：提供统一的记忆库（mem0 + qdrant）和工具调用框架，便于在同一后宫中组织多个角色的独立或协同对话。  
- **跨平台交互**：QQ 与 Telegram 双通道，使得用户可以在常用社交软件中直接召唤 AI 角色。

**典型接入方式**  
1. **环境准备**：在具备 8 GB 以上显存的 Linux/Windows 机器上安装 Python≥3.10、CUDA、ffmpeg 等依赖；克隆仓库后运行 `pip install -r requirements.txt`。  
2. **模型部署**：按照 README 配置本地 LLM（OpenClaw）、GPT‑SoVITS、ComfyUI checkpoint 与 Live2D 资源；使用提供的脚本生成或导入角色卡。  
3. **启动服务**：  
   ```bash
   python run_qq_bot.py   # 启动 QQ 端口
   python run_telegram_bot.py   # 启动 Telegram 端口
   ```  
   两个进程共享同一记忆库（mem0 + qdrant），即可实现多角色并发对话。  
4. **二次开发**：如果只需要其中的某一模块（如仅使用语音合成或图像生成），可以在 `agents/` 目录下引用对应的 `Tool` 类，按需求组装成自定义工作流。

**生产可用性评估**  
- **成熟度**：当前 58/100，代码已在 2026‑06‑24 更新，拥有 137 星、8 次 Fork，核心功能基本可用。  
- **适用场景**：适合原型验证、内部娱乐系统或对隐私要求极高的闭环部署；不建议直接用于大规模商业客服或高并发公开服务。  
- **风险点**  
  - 依赖较多（OpenClaw、GPT‑SoVITS、ComfyUI、Live2D），需要自行管理模型版权与许可证。  
  - 维护者活跃度一般，生产环境需自行制定升级、容灾和安全审计流程。  
  - 显存调度虽支持 8 GB 动态分配，但在多角色并发时仍可能出现 OOM，需要根据实际负载调整 `scheduler.yaml`。  
- **准备度**：**中等**。可在内部或小规模用户群体中投入使用，前提是完成以下工作：  
  1. 完整的 CI/CD 测试套件（目前项目缺乏）。  
  2. 对依赖库进行安全扫描并确认许可证兼容。  
  3. 实施监控（显存、CPU、网络）和日志收集，以便快速定位异常。  

综上，Artemis 为本地多模态 AI 角色交互提供了相对完整的解决方案，具备快速原型化的价值；在生产环境使用时，应先进行小范围验证并补齐运维、合规等配套措施。

## 🧭 Practical evaluation

**Value:** momori777/Artemis helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 137 GitHub stars
- 8 forks
- updated 2026-06-24
- primary language: Python
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 46/100 |
| topics | 100/100 |
| outlook | 52/100 |
| quality | 58/100 |
| recency | 40/100 |
| adoption | 39/100 |
| production | 54/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/momori777/Artemis) · [← Back to Orchestration](./README.md)</sub>
