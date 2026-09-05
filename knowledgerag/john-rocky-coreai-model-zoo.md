# john-rocky/coreai-model-zoo

[![Stars](https://img.shields.io/github/stars/john-rocky/coreai-model-zoo?style=flat-square&color=yellow)](https://github.com/john-rocky/coreai-model-zoo/stargazers) [![Forks](https://img.shields.io/github/forks/john-rocky/coreai-model-zoo?style=flat-square&color=blue)](https://github.com/john-rocky/coreai-model-zoo/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> Community model zoo + knowledge base for Apple Core AI (iOS/macOS 27): Qwen3.5 & Gemma 4 converted end-to-end, verified on-device (iPhone 17 Pro GPU/ANE), conversion gotchas, custom Metal kernels, Swift runner

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 189 |
| 🍴 **Forks** | 12 |
| 💻 **Language** | Swift |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `apple-silicon` `coreai` `coreml` `gemma4` `granite` `ios` `iphone` `lfm` `llm` `local-llm` `macos`

## 🎯 Categories

Knowledge/RAG · AI/ML · Mobile

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`john-rocky/coreai-model-zoo` is an open‑source collection of Apple Core AI models (e.g., Qwen 3.5 and Gemma 4) that have been fully converted, verified on‑device (iPhone 17 Pro GPU/ANE), and packaged with conversion tips, custom Metal kernels, and a Swift runner. The repo also doubles as a knowledge base that documents the conversion process, performance gotchas, and usage patterns, making it easy for developers to index and retrieve model‑related information in assistant‑style workflows.

**Value**  
- **Accelerates on‑device AI**: Provides ready‑to‑run Core AI models, sparing teams the time‑consuming effort of conversion, validation, and low‑level Metal integration.  
- **Searchable knowledge base**: The embedded documentation and “gotchas” list can be indexed by RAG systems, enabling assistants to answer questions about model deployment, performance tuning, and hardware constraints.  
- **Swift‑first workflow**: Seamlessly fits into existing iOS/macOS codebases, allowing developers to prototype and ship AI features without switching languages or frameworks.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the provided Swift runner on a development iPhone 17 Pro (or simulator with ANE support) to verify that the models load and infer as expected.  
2. **Knowledge Indexing** – Feed the markdown docs and conversion notes into your internal RAG pipeline (e.g., Elasticsearch or LangChain) to make the “how‑to” content searchable for assistants.  
3. **Integration** – Wrap the Swift runner in a lightweight library or Swift Package Manager (SPM) module, then call it from your app or backend service that orchestrates on‑device inference.  
4. **Validation & Scaling** – Benchmark latency/power on target devices, adjust custom Metal kernels if needed, and add CI checks for model integrity.

**Production Readiness**  
- **Maturity**: Medium. The models have been verified on real hardware and the repo is actively maintained (last update 2026‑06‑23, 189 ★).  
- **Strengths**: Clear documentation, end‑to‑end conversion scripts, and a Swift‑native runner make it suitable for prototypes and internal tools.  
- **Caveats**: Before full production deployment, perform a security/license audit, confirm long‑term maintainer support, and add robust error handling/monitoring around the Metal kernels and ANE usage. With those checks in place, the library can be considered production‑ready for on‑device AI features on iOS/macOS.

### Русский

**Краткое резюме:**  
`john-rocky/coreai-model-zoo` — это открытый набор моделей и база знаний для Apple Core AI (iOS/macOS 27), включающий полностью сконвертированные Qwen 3.5 и Gemma 4, проверенные на реальном устройстве (iPhone 17 Pro GPU/ANE), а также руководство по типичным проблемам конвертации, кастомным Metal‑ядрам и Swift‑раннеру. Проект позволяет быстро индексировать внутренние документы и делать их доступными ассистентам через RAG‑поиск, что ускоряет прототипирование функций «поиска по знанию» и контекстных ответов. Готовность к production — средняя: подходит для пилотных внедрений и внутренних workflow, но требует предварительной проверки зависимостей, лицензии и поддержки перед масштабным использованием.

### 中文

**项目简介**  
`john-rocky/coreai-model-zoo` 是一个面向 Apple Core AI（iOS/macOS 27）的社区模型仓库和知识库，提供 Qwen 3.5、Gemma 4 等大模型的端到端转换、在 iPhone 17 Pro（GPU + ANE）上的实机验证、转换坑点、定制 Metal Kernel 与 Swift 运行时示例。

**价值**  
- 将大模型与本地 iOS/macOS 设备深度融合，摆脱云端依赖，实现低时延、高隐私的 AI 推理。  
- 汇总转换经验、Metal 加速实现和 Swift 示例，帮助开发者快速上手并在自己的应用中复用模型。  
- 为内部知识库、文档搜索、对话助理等场景提供可离线部署的检索增强（RAG）能力。

**典型接入方式**  
1. **阅读 README**：按照项目提供的 Swift 包管理（SwiftPM）指引将 `coreai-model-zoo` 添加到 Xcode 项目。  
2. **模型下载 & 转换**：使用仓库中的脚本将 Qwen 3.5 / Gemma 4 转换为 Core ML `.mlmodelc`，并参考 “conversion gotchas” 文档处理常见坑点。  
3. **自定义 Metal Kernel（可选）**：若对性能有更高要求，可直接引用仓库提供的 Metal kernel 代码并在 Swift 中注册。  
4. **集成 RAG 流程**：将模型输出与本地知识库（如 SQLite、Embedding 索引）结合，实现文档检索与答案生成。  
5. **小范围验证**：在 iPhone 17 Pro 或配备 ANE 的 Mac 上运行示例，确认推理时延与资源占用符合预期后，再推广到全量业务。

**生产可用性**  
- **成熟度**：项目已在真实设备上完成端到端验证，适合作为原型或内部工具的核心组件。  
- **依赖风险**：依赖 Swift 5、Xcode 15+、Metal 与 Core ML，需确保 CI/CD 环境同步更新。  
- **维护状态**：截至 2026‑06‑23 最近一次提交，星标 189、Fork 12，活跃度一般；在生产环境使用前建议与维护者确认长期维护计划。  
- **安全合规**：暂无显著元数据风险，但仍需审查许可证（MIT/Apache 等）以及模型本身的使用许可。  

总体而言，`coreai-model-zoo` 是面向 Apple 生态的本地大模型解决方案，适合作为内部知识检索、文档搜索或对话助理的原型平台；在完成小规模 PoC、确认依赖兼容性并进行必要的安全审计后，可逐步推广至生产环境。

## 🧭 Practical evaluation

**Value:** john-rocky/coreai-model-zoo helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 189 GitHub stars
- 12 forks
- updated 2026-06-23
- primary language: Swift
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 28/100 |
| stars | 48/100 |
| topics | 100/100 |
| outlook | 67/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 43/100 |
| production | 68/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/john-rocky/coreai-model-zoo) · [← Back to Knowledgerag](./README.md)</sub>
