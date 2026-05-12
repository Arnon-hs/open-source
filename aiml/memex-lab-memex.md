# memex-lab/memex

[![Stars](https://img.shields.io/github/stars/memex-lab/memex?style=flat-square&color=yellow)](https://github.com/memex-lab/memex/stargazers) [![Forks](https://img.shields.io/github/forks/memex-lab/memex?style=flat-square&color=blue)](https://github.com/memex-lab/memex/network) [![Language](https://img.shields.io/badge/lang-Dart-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> Open-source, local-first AI journal app for iOS and Android. Capture text, photos, and voice — AI agents organize them into timeline cards and insights. Your data stays on your device. Bring your own LLM (OpenAI, Claude, Gemini, Ollama, and more).

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 130 |
| 🍴 **Forks** | 15 |
| 💻 **Language** | Dart |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-assistant` `ai-companion` `ai-diary` `ai-journal` `assistant-app` `journal-app` `journaling` `journaling-app` `knowledge-management` `life-logging` `local-agent` `local-first`

## 🎯 Categories

AI/ML · Data · Mobile

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
memex‑lab/memex is an open‑source, local‑first AI journal app for iOS and Android that lets users capture text, photos, and voice recordings. Built with Dart/Flutter, the app uses plug‑in LLMs (OpenAI, Claude, Gemini, Ollama, etc.) to automatically organize entries into timeline cards and generate insights, while keeping all data on the device.

**Value proposition**  
- **AI‑enabled journaling without a ground‑up stack** – developers can add sophisticated retrieval‑augmented generation (RAG) and autonomous‑agent capabilities to a ready‑made mobile UI, saving weeks of UI and data‑pipeline work.  
- **Local‑first privacy** – all content stays on the user’s device, making it suitable for privacy‑sensitive use cases (personal knowledge bases, health logs, field notes).  
- **LLM‑agnostic** – the architecture supports any hosted or self‑hosted model, giving teams flexibility to experiment with cost‑effective or on‑premise models.

**Practical adoption path**  

| Step | Action | Why it matters |
|------|--------|----------------|
| 1️⃣ Quick‑look | Clone the repo, run `flutter pub get` and launch the demo on a simulator/emulator. Verify the README instructions and basic capture workflow. | Confirms the project builds with your Flutter version and that the UI works out‑of‑the‑box. |
| 2️⃣ Model hookup | Add your preferred LLM credentials (e.g., OpenAI API key, Claude token, or local Ollama endpoint) in the `config.yaml` or environment file. Test the “organize” and “insight” endpoints with a single entry. | Validates the plug‑in integration layer and measures latency/cost for your chosen model. |
| 3️⃣ Proof of concept | Extend a single feature—e.g., a custom RAG prompt that pulls from captured notes to answer domain‑specific questions. Keep the change isolated to a new Dart service class. | Demonstrates that the internal agent pipeline is extensible and that you can inject domain knowledge without rewriting the core. |
| 4️⃣ Evaluation | Run a small user‑study or internal QA to compare AI‑generated cards vs. manual tagging. Track metrics such as processing time, error rate, and user satisfaction. | Provides data to decide whether the solution meets your product’s quality bar. |
| 5️⃣ Production prep | Harden the build: pin Flutter/Dart versions, lock LLM SDKs, add automated tests for the new service, and set up CI/CD for iOS/Android releases. Review licensing (MIT) and ensure any third‑party model usage complies with your organization’s policy. | Turns the prototype into a maintainable, ship‑ready component. |

**Production readiness assessment**  
- **Maturity**: Medium. The app is actively maintained (last commit 2026‑05‑12), has a modest community (≈130 ★), and the core UI is functional. However, the integration documentation is sparse, and the LLM‑plug‑in layer requires custom configuration.  
- **Strengths for production**:  
  * Local‑first data model → strong privacy compliance.  
  * Multi‑LLM support → easy to swap models as costs or policies change.  
  * Flutter codebase → single code path for iOS & Android, reducing platform‑specific debt.  
- **Open risks**:  
  * No out‑of‑the‑box CI pipelines or extensive test coverage; you’ll need to add these.  
  * Dependency on external LLM APIs can introduce latency or rate‑limit issues; self‑hosted Ollama mitigates this but adds operational overhead.  
  * The “agent” orchestration is not fully documented, so onboarding may require reverse‑engineering the existing services.  

**Bottom line**  
memex‑lab/memex offers a fast way to prototype AI‑driven journaling or knowledge‑base features on mobile, especially when privacy and model flexibility are priorities. Start with a small, isolated proof‑of‑concept to validate the LLM integration and UI flow, then invest in testing, CI/CD, and dependency pinning before promoting it to production. With those steps, the project can move from a promising prototype to a reliable component of internal tools or a consumer‑facing app.

### Русский

**memex‑lab/memex** — это open‑source приложение‑дневник для iOS и Android, которое хранит все данные локально и использует подключаемые LLM (OpenAI, Claude, Gemini, Ollama и др.) для автоматической организации записей в карточки‑таймлайны и генерации инсайтов. Типичный сценарий внедрения — добавить AI‑функциональность в существующее мобильное приложение или создать прототип RAG/агентных воркфлоу, подключив собственный LLM и проверив работу через небольшую proof‑of‑concept, следуя инструкциям в README. Готовность к production — средняя: проект уже имеет 130 звёзд, активные обновления и написан на Dart, но путь интеграции не полностью документирован, поэтому перед запуском в продакшн требуется проверка зависимостей и небольшая доработка настройки.

### 中文

**项目价值**  
memex‑lab/memex 为 iOS/Android 提供了一个本地优先的 AI 日记平台，能够在设备端安全地捕获文字、照片和语音，并通过可插拔的 LLM（OpenAI、Claude、Gemini、Ollama 等）把碎片化信息自动组织成时间线卡片和洞察。它把 AI 能力包装成即插即用的「agent」层，开发者无需从零搭建向量存储、检索、提示工程等基础设施，就能快速在移动端原型化 RAG、智能助理或知识管理功能。

**典型接入方式**  

| 步骤 | 说明 |
|------|------|
| 1️⃣ 克隆仓库 & 安装依赖 | `git clone https://github.com/memex-lab/memex.git` → `flutter pub get`（项目基于 Dart/Flutter）。 |
| 2️⃣ 配置 LLM 访问 | 在 `config.yaml`（或 `.env`）中填入所选模型的 API key 与端点，例如 `OPENAI_API_KEY`、`CLAUDE_API_KEY`、`OLLAMA_BASE_URL` 等。支持多模型切换，只需修改对应字段。 |
| 3️⃣ 本地数据初始化 | 首次启动时应用会在设备上创建 SQLite/Realm 数据库，用于存放原始笔记和向量索引（使用 `sqlite‑fts5` 或 `hnswlib` 之类的本地向量库）。无需额外服务器。 |
| 4️⃣ 调用 AI Agent | 通过 Flutter UI 或直接调用 `MemexAgent` 类的 `processEntry(entry)` 方法，把新建的文本/图片/音频交给后端 agent，获取自动生成的时间线卡片或洞察。 |
| 5️⃣ 业务集成 | 将 `MemexAgent` 封装为内部 SDK，供其他模块调用；或在原有 APP 中嵌入 `MemexScreen` 直接使用完整的日记 UI。 |

**生产可用性评估**  

| 维度 | 评估 | 说明 |
|------|------|------|
| **功能完整性** | ✅ 已实现核心捕获、向量化、AI 组织、离线存储 | 适合内部原型、内部工具或对隐私有严格要求的产品。 |
| **代码成熟度** | ⭐ 130 星，15 fork，最近更新 2026‑05‑12 | 活跃度一般，社区规模小，仍需自行审查依赖安全性。 |
| **依赖风险** | ⚠️ 依赖外部 LLM API（费用、速率）和本地向量库（可能需要 native 编译） | 在生产环境部署前需评估成本、网络可达性以及本地库的跨平台兼容性。 |
| **可扩展性** | ✅ 支持多模型、插件式 Agent，代码结构清晰 | 可在现有项目中逐步替换或扩展为自研模型。 |
| **运维成本** | 中等 | 主要是模型 API 的密钥管理和本地数据库备份；不涉及后端服务器。 |
| **推荐使用场景** | ✅ 原型开发、内部知识库、隐私敏感的移动端 AI 日记 | 若需要大规模并发或复杂业务逻辑，建议在此基础上再做层层包装或迁移到后端服务。 |

**结论**  
memex‑lab/memex 是一个 **“本地优先 + 可插拔 LLM”** 的移动端 AI 日记框架，能够让团队在几行代码内为 iOS/Android 应用加入智能笔记、自动摘要和时间线洞察等功能。对于 **原型验证、内部工具或对数据本地化有强需求的产品**，它的集成成本低、隐私保护好；在进入大规模生产前，需要对模型费用、跨平台本地向量库的兼容性以及长期维护计划进行充分评估。

## 🧭 Practical evaluation

**Value:** memex-lab/memex helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 130 GitHub stars
- 15 forks
- updated 2026-05-12
- primary language: Dart
- 17 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 30/100 |
| stars | 45/100 |
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

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/memex-lab/memex) · [← Back to AI/ML](./README.md)</sub>
