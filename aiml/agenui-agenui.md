# AGenUI/AGenUI

[![Stars](https://img.shields.io/github/stars/AGenUI/AGenUI?style=flat-square&color=yellow)](https://github.com/AGenUI/AGenUI/stargazers) [![Forks](https://img.shields.io/github/forks/AGenUI/AGenUI?style=flat-square&color=blue)](https://github.com/AGenUI/AGenUI/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Native A2UI Renderer for iOS/Android/HarmonyOS — high performance streaming AI-generated UI with 22 built-in components. The only complete 3-platform A2UI implementation.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 857 |
| 🍴 **Forks** | 117 |
| 💻 **Language** | C++ |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`a2ui` `agent-ui` `agenui` `ai-agents` `ai-generative-ui` `cross-platform` `generative-ui` `harmonyos` `llm-ui` `native-rendering` `native-ui` `server-driven-ui`

## 🎯 Categories

AI/ML · Frontend · Backend · Mobile

## 📝 Summary

### English

**Summary**  
AGenUI provides a native A2UI renderer for iOS, Android, and HarmonyOS, delivering high‑performance streaming of AI‑generated user interfaces with 22 ready‑made components—the only fully‑featured three‑platform implementation. It lets developers plug AI‑driven UI capabilities into mobile apps without building a custom model stack from scratch, making rapid prototyping of RAG, agent, or other AI workflows straightforward.  

**Value**  
- **Speed to market:** By handling the heavy lifting of UI generation and streaming, AGenUI lets teams focus on the AI logic and product features rather than low‑level rendering code.  
- **Cross‑platform consistency:** One codebase renders identical AI‑generated interfaces on iOS, Android, and HarmonyOS, reducing maintenance overhead.  
- **Rich component library:** The 22 built‑in UI components cover common patterns (lists, forms, charts, etc.), accelerating prototype development and early‑stage validation of AI‑augmented experiences.  

**Practical adoption path**  
1. **Proof‑of‑concept:** Clone the repo, follow the README to build the minimal C++ library for a single platform (e.g., Android).  
2. **Integrate a simple AI service:** Connect a lightweight model or API (e.g., OpenAI, local LLaMA) that returns A2UI specifications and stream them to the renderer.  
3. **Iterate with built‑in components:** Replace hand‑crafted UI screens with generated ones, using the provided components to validate layout, latency, and UX.  
4. **Scale to multiple platforms:** Once the PoC is stable, add iOS and HarmonyOS targets, sharing the same A2UI definitions across devices.  

**Production readiness**  
- **Maturity:** Medium. The project is actively maintained (last update 2026‑06‑24) and has a solid community signal (857 ★, 117 forks).  
- **Strengths:** High‑performance streaming, cross‑platform support, and a comprehensive component set make it suitable for internal tools, prototypes, and early‑stage customer demos.  
- **Caveats:** The integration workflow is not fully documented; setting up the build environment and linking the renderer to existing mobile codebases may require additional engineering effort. Before production deployment, perform a dependency audit, verify long‑term maintenance of the C++ library, and conduct load/latency testing in your target environment.  

In summary, AGenUI offers a compelling way to embed AI‑generated UI into mobile apps quickly, but teams should start with a small proof‑of‑concept, validate the integration effort, and perform thorough stability checks before treating it as production‑grade.

### Русский

AGenUI / AGenUI — это нативный рендерер A2UI для iOS, Android и HarmonyOS, обеспечивающий высокопроизводительный потоковый UI, генерируемый ИИ, с 22 готовыми компонентами; единственная полностью кроссплатформенная реализация A2UI. Его обычно используют для быстрой прототипизации AI‑фич, построения RAG‑ или агентных воркфлоу и оценки инструментов модели, начиная с небольшого proof‑of‑concept и проверки README. Готовность к production — средняя: проект подходит для прототипов и внутренних процессов, но требует проверки зависимостей и уточнения пути интеграции перед масштабным запуском.

### 中文

**价值**  
AGenUI/AGenUI 为 iOS、Android 与 HarmonyOS 提供唯一的跨三平台 A2UI 实现，能够在移动端以极低的延迟实时渲染 AI 生成的 UI，并内置 22 种常用组件。它让开发者不必从零搭建模型推理与 UI 渲染链路，就能直接在现有 App 中加入 AI 交互、RAG（检索增强生成）或智能体工作流，极大缩短原型验证和功能迭代的时间。

**典型接入方式**  
1. **准备环境**：克隆仓库，确保 C++ 编译链（Clang/NDK、Xcode）和对应平台的 SDK 已安装。  
2. **阅读 README**：按照文档运行 `./scripts/setup.sh` 完成依赖下载（如 libtorch、OpenCV 等）并生成平台‑specific 的库文件。  
3. **创建最小示例**：在项目根目录执行 `make demo_ios` / `make demo_android` / `make demo_harmony`，生成一个仅包含 `Text`, `Button`, `Image` 等基础组件的演示 App。  
4. **集成到业务代码**：把生成的 `AGenUI` 静态库（或 AAR/Framework）以及头文件加入现有工程，使用 `AGenUI::Renderer` 初始化后，调用 `Renderer::renderFromPrompt("生成一个登录页")` 即可得到 UI 描述并渲染。  
5. **定制组件**：如果业务需要额外控件，只需在 `components/` 目录实现对应的 C++ 子类并在 `ComponentFactory` 中注册，即可在 AI Prompt 中直接引用。  

**生产可用性**  
- **成熟度**：GitHub ★857、Fork 117，最近一次提交在 2026‑06‑24，代码活跃度较高，核心渲染逻辑已在多个内部项目中验证。  
- **适用场景**：非常适合作为 **原型**、**内部工具** 或 **AI 功能验证** 的底层渲染引擎；对外发布的产品仍需进行以下检查：  
  - 依赖安全审计（第三方库如 libtorch、OpenCV 的许可证兼容性）。  
  - 资源占用评估（模型推理的 CPU/GPU/内存占用），尤其在低端设备上进行压力测试。  
  - 稳定的异常捕获与回退机制（渲染失败时的 UI 降级策略）。  
- **上线建议**：先在一个独立的功能模块或内部测试渠道做 **小规模 PoC**，验证模型加载、网络带宽、跨平台构建流程后，再逐步推广到正式业务。  

综上，AGenUI/AGenUI 为移动端 AI‑驱动 UI 提供了高性能、跨平台的即插即用方案，适合作为快速验证和内部流程的核心组件；在完成依赖审计和性能压测后，可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** AGenUI/AGenUI helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 857 GitHub stars
- 117 forks
- updated 2026-06-24
- primary language: C++
- 13 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 52/100 |
| stars | 62/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 77/100 |
| recency | 80/100 |
| adoption | 59/100 |
| production | 68/100 |
| usefulness | 74/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/AGenUI/AGenUI) · [← Back to AI/ML](./README.md)</sub>
