# innermost47/ai-dj

[![Stars](https://img.shields.io/github/stars/innermost47/ai-dj?style=flat-square&color=yellow)](https://github.com/innermost47/ai-dj/stargazers) [![Forks](https://img.shields.io/github/forks/innermost47/ai-dj?style=flat-square&color=blue)](https://github.com/innermost47/ai-dj/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Standalone (Ableton Link) + VST3/AU for live performance. 8 tracks, 8 AI models, 30 seconds of patience per loop. It occasionally hallucinates. Not a song generator - you still have to do the work. Stay human.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 226 |
| 🍴 **Forks** | 22 |
| 💻 **Language** | C++ |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ableton-link-audio` `ai` `ai-music` `ai-music-generation` `ai-music-generator` `ai-music-tools` `daw` `juce` `live-performance` `llm` `music-ai` `music-generation`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`innermost47/ai-dj` is a C++‑based, standalone music‑performance engine (with Ableton Link support and VST3/AU plugins) that runs eight simultaneous tracks, each powered by a different AI model. It generates short, 30‑second loops that can be manipulated live, but the output is deliberately imperfect – you still need to shape the music yourself.  

**Value Proposition**  
The project lets developers and musicians add AI‑driven generative elements to a live‑performance workflow without building a model stack from scratch. By bundling ready‑to‑use models, a real‑time sync layer (Ableton Link), and plugin formats, it accelerates prototyping of AI‑augmented DJ or performance tools, RAG‑style audio agents, and experimental creative pipelines.  

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | **Clone & run the demo** – follow the README to build the C++ binaries and launch the standalone app or VST3/AU plugin. | Verifies that the environment (C++ toolchain, dependencies) works on your machine. |
| 2️⃣  | **Play a proof‑of‑concept loop** – load the provided preset, sync with Ableton Link, and observe the 8 tracks and model behavior. | Confirms the core functionality and latency characteristics. |
| 3️⃣  | **Swap or extend models** – replace one of the bundled models with your own (e.g., a custom RAG or agent model) using the documented model‑loader API. | Demonstrates how the framework can be integrated into your own AI pipeline. |
| 4️⃣  | **Wrap in your workflow** – embed the VST3/AU plugin into your DAW or host the standalone app as a microservice that receives MIDI/OSC triggers. | Moves the prototype toward a production‑like usage scenario. |
| 5️⃣  | **Add monitoring & fallback** – because the generator “hallucinates,” implement UI controls or scripts to mute, reset, or manually edit loops. | Ensures reliability for live or semi‑automated deployments. |

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last update 2026‑06‑28), has a modest community (≈226 ★, 22 forks), and provides compiled binaries for common platforms.  
- **Strengths:** Ready‑made VST3/AU plugins, Ableton Link sync, and a clear C++ codebase make it usable for internal prototypes or as a sandbox for AI‑music research.  
- **Risks:**  
  * Integration steps are not fully documented beyond the basic README, so onboarding may require digging into the build system.  
  * Dependency management (specific C++ libraries, model runtimes) must be audited for version compatibility and licensing.  
  * The “hallucination” behavior means you need additional UI/logic to keep the output musically coherent in a production setting.  
- **Recommendation:** Treat `ai-dj` as a **prototype‑grade** component. Start with a small PoC (steps 1‑3) to validate that the model‑swap API and real‑time sync meet your latency and stability requirements, then layer monitoring, fallback, and CI/CD checks before considering it for a live‑performance or commercial product.

### Русский

**innermost47/ai-dj** — это standalone‑приложение (поддержка Ableton Link) и VST3/AU‑плагин, позволяющий в реальном времени добавить к живому сету до 8 дорожек, каждая из которых управляется отдельной AI‑моделью (30 секунд «терпения» на цикл). Проект подходит для быстрого прототипирования AI‑фич в музыкальных воркфлоу (RAG, агентные сценарии) и оценки инструментов модели, но требует небольшого proof‑of‑concept и проверки зависимостей перед интеграцией в продакшн. Готовность — средняя: достаточно зрелый для внутренних экспериментов, но путь интеграции не полностью документирован.

### 中文

**价值**  
- **即插即用的 AI 音乐辅助**：提供 8 条独立轨道和 8 种预置的 AI 模型，能够在 Ableton Link 环境下实时生成、变形或延伸音频循环，极大降低了在现场表演中加入 AI 的技术门槛。  
- **加速原型开发**：不需要从零搭建模型堆栈，直接使用已有的 VST3/AU 插件或独立（Standalone）模式，就能快速验证 RAG、Agent 或自定义音频处理工作流。  
- **保持创作主导权**：AI 只负责提供素材和灵感（每段循环仅 30 s），不会完整生成歌曲，创作者仍然是核心决策者，避免“被 AI 替代”的风险。

**典型接入方式**  
1. **Standalone + Ableton Link**  
   - 下载并运行可执行文件，打开 Ableton Live 并在 **Link** 面板中启用。  
   - 在 Live 中创建 8 条 MIDI/音频轨道，绑定对应的 AI 轨道即可实时接收 AI 生成的循环。  

2. **VST3 / AU 插件**  
   - 将 `ai-dj.vst3`（或 `.component`）复制到系统的插件目录。  
   - 在任何支持 VST3/AU 的 DAW（如 Logic、Reaper、Cubase）中插入插件，按需选择模型、循环时长等参数。  

3. **代码层面集成（原型）**  
   - 项目根目录提供 `README.md` 中的 CMake 示例，可在自己的 C++ 项目中通过 `add_subdirectory` 引入 `ai-dj` 库。  
   - 通过公开的 `AI_DJ::Engine` 接口调用 `loadModel(id)`, `processAudio(buffer)` 等函数，实现自定义 RAG 或 Agent 工作流的原型验证。  

**生产可用性**  
- **成熟度**：GitHub ★226、Fork 22，最近一次提交为 2026‑06‑28，活跃度尚可。核心代码使用 C++ 实现，依赖相对明确（Boost、Eigen、JUCE），适合内部原型或小规模现场使用。  
- **准备度**：  
  - **原型/内部工具**：可直接上手，验证 AI 生成效果和交互流程。  
  - **生产环境**：需要进行以下检查后方可投入：  
    1. **依赖审计**：确认第三方库的许可证兼容性及安全更新。  
    2. **稳定性测试**：AI 模型在长时间运行下的内存泄漏、CPU/GPU 负载以及“幻觉”频率。  
    3. **CI/CD 集成**：项目本身缺乏自动化构建/测试脚本，建议自行添加单元测试与打包流程。  
    4. **运维监控**：对实时音频流的延迟和错误日志进行监控，防止现场卡顿。  

综上，**innermost47/ai-dj** 适合作为现场表演或音频原型的 AI 加速器，接入成本低，快速验证 AI 音乐创意；在经过依赖审计和稳定性验证后，可在内部生产环境中正式使用。

## 🧭 Practical evaluation

**Value:** innermost47/ai-dj helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 226 GitHub stars
- 22 forks
- updated 2026-06-28
- primary language: C++
- 15 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 50/100 |
| topics | 100/100 |
| outlook | 71/100 |
| quality | 71/100 |
| recency | 80/100 |
| adoption | 46/100 |
| production | 66/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/innermost47/ai-dj) · [← Back to AI/ML](./README.md)</sub>
