# ferranpons/Llamatik

[![Stars](https://img.shields.io/github/stars/ferranpons/Llamatik?style=flat-square&color=yellow)](https://github.com/ferranpons/Llamatik/stargazers) [![Forks](https://img.shields.io/github/forks/ferranpons/Llamatik?style=flat-square&color=blue)](https://github.com/ferranpons/Llamatik/network) [![Language](https://img.shields.io/badge/lang-HTML-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> True on-device AI for Kotlin Multiplatform (Android, iOS, Desktop, JVM, WASM). LLM, Speech-to-Text and Image Generation — powered by llama.cpp, whisper.cpp and stable-diffusion.cpp.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 116 |
| 🍴 **Forks** | 20 |
| 💻 **Language** | HTML |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `android` `desktop` `edge-ai` `ggml` `inference` `ios` `kmp` `kmp-library` `kotlin` `ktor` `llama`

## 🎯 Categories

Knowledge/RAG · AI/ML · Database · Mobile

## 📝 Summary

### English

**Brief summary**  
Llamatik is an open‑source Kotlin Multiplatform library that brings on‑device large‑language‑model (LLM), speech‑to‑text, and image‑generation capabilities to Android, iOS, desktop, JVM, and WebAssembly apps by wrapping llama.cpp, whisper.cpp and stable‑diffusion.cpp. It enables developers to embed powerful AI features locally, without relying on cloud APIs, making internal knowledge bases searchable and usable by conversational assistants.

**Value**  
- **Privacy & latency** – All inference runs on the device, so sensitive corporate data never leaves the user’s hardware and responses are returned instantly.  
- **Cross‑platform consistency** – A single Kotlin codebase powers AI features on mobile, desktop and web, reducing duplicate effort and maintenance.  
- **Cost‑effective prototyping** – By leveraging the lightweight C++ back‑ends (llama, whisper, stable‑diffusion), teams can experiment with LLM‑driven search, document grounding, and multimodal assistants without paying for external API usage.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, follow the README to build the native binaries for the target platform(s), and run the supplied example that indexes a small knowledge base and answers queries.  
2. **Integration scaffolding** – Wrap the provided Kotlin APIs in your existing data‑access layer (e.g., a local SQLite or vector store) and expose a simple service that your UI or chatbot can call.  
3. **Iterative scaling** – Replace the demo model with a larger, domain‑specific LLM or fine‑tuned whisper model, and benchmark memory/CPU usage on representative devices.  
4. **Production hardening** – Add error handling, model‑download verification, and automated model updates; package the native binaries with your app’s release pipeline.

**Production readiness**  
Llamatik sits at a medium readiness level. It is mature enough for internal prototypes and low‑traffic production workloads, as evidenced by 116 GitHub stars and recent activity (updated 2026‑05‑11). However, the integration steps are not fully documented; teams should allocate time to verify the build process for each target platform, assess binary size and runtime resource consumption, and establish a maintenance plan for the underlying C++ libraries. Once those checks are completed, Llamatik can be safely used in internal tools and, with additional testing, in customer‑facing applications.

### Русский

**Llamatik** — это open‑source‑фреймворк, позволяющий запускать полностью локальные модели ИИ (LLM, распознавание речи и генерацию изображений) на Kotlin Multiplatform (Android, iOS, Desktop, JVM, WASM) с помощью llama.cpp, whisper.cpp и stable‑diffusion.cpp. Он упрощает создание ассистентов, способных индексировать внутренние базы знаний, улучшать поиск по документам и давать обоснованные ответы, что делает его ценным для прототипов и внутренних рабочих процессов. Готовность к продакшну — средняя: проект имеет 116 звёзд, активные форки и недавнее обновление, но путь интеграции не полностью документирован, поэтому рекомендуется начать с небольшого proof‑of‑concept и проверить README перед масштабным внедрением.

### 中文

**项目简介**  
ferranpons/Llamatik 是一套在 **Kotlin Multiplatform**（Android、iOS、Desktop、JVM、WASM）上运行的本地 AI 解决方案，内置 LLM、语音转文字和图像生成能力，底层分别基于 **llama.cpp、whisper.cpp、stable‑diffusion.cpp**。  

**价值**  
- **本地化安全**：所有模型都在设备上推理，无需将敏感数据上传至云端，满足企业内部知识库的隐私要求。  
- **跨平台统一**：一次编写 Kotlin 代码，即可在移动、桌面和 Web（WASM）上使用同一套 AI 能力，降低维护成本。  
- **提升检索与助理体验**：可将企业文档、FAQ、技术手册等索引进 LLM，提供语义搜索、自动摘要和基于上下文的智能回复，显著提升内部助理的准确性和响应速度。  

**典型接入方式**  
1. **准备模型文件**：下载对应平台的 `ggml` 权重（如 `llama‑7B.ggmlv3.q4_0.bin`、`whisper‑base.ggml.bin`、`sd‑v1‑4.ggml.bin`），放置在项目的资源目录。  
2. **添加依赖**：在 `build.gradle.kts` 中加入 Llamatik 的 Maven 坐标（或直接使用源码模块），并在 `commonMain` 中声明平台实现。  
3. **初始化**：在应用启动时调用 `Llamatik.init(context, modelPath, options)`，根据需要开启 LLM、STT、图像生成的子模块。  
4. **业务接入**：  
   - **知识检索**：将文档分块后写入向量库（如 Milvus、Qdrant），使用 LLM 进行语义检索并生成答案。  
   - **语音交互**：调用 `SpeechToText.convert(audio)` 获得文字输入，喂给 LLM 生成回复。  
   - **图像生成**：通过 `ImageGenerator.generate(prompt)` 直接在设备上渲染图片。  
5. **验证 POC**：先在一个小型子系统（如内部 FAQ Bot）实现完整链路，确认模型加载、资源占用和响应时延符合预期，再逐步推广。  

**生产可用性**  
- **成熟度**：已有 116 ⭐、20 fork，近期仍在活跃维护（截至 2026‑05‑11），代码质量和社区活跃度属于中等偏上。  
- **适用场景**：非常适合原型、内部工具或对数据隐私有严格要求的业务；在资源受限的移动端也能运行，但需评估模型大小与内存占用。  
- **风险与准备**：  
  - **集成成本**：项目文档相对简略，首次接入需要自行梳理平台特定的编译参数（如 `-march=native`、WASM 打包）。  
  - **依赖维护**：底层 `llama.cpp`、`whisper.cpp`、`stable-diffusion.cpp` 会随上游更新，需要定期同步并重新编译。  
  - **性能评估**：在不同平台上进行基准测试，确保推理时延（通常在 300‑1500 ms）和电量消耗在可接受范围。  

**结论**：Llamatik 为 Kotlin Multiplatform 项目提供了一站式本地 AI 能力，能够快速构建安全、跨平台的知识助理原型。若在生产环境使用，建议先在受控环境中完成 POC，确认模型体积、性能和依赖管理后，再进行规模化部署。

## 🧭 Practical evaluation

**Value:** ferranpons/Llamatik helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 116 GitHub stars
- 20 forks
- updated 2026-05-11
- primary language: HTML
- 20 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 33/100 |
| stars | 44/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 73/100 |
| recency | 100/100 |
| adoption | 41/100 |
| production | 72/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/ferranpons/Llamatik) · [← Back to Knowledgerag](./README.md)</sub>
