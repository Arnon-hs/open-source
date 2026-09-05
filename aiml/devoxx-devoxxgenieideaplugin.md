# devoxx/DevoxxGenieIDEAPlugin

[![Stars](https://img.shields.io/github/stars/devoxx/DevoxxGenieIDEAPlugin?style=flat-square&color=yellow)](https://github.com/devoxx/DevoxxGenieIDEAPlugin/stargazers) [![Forks](https://img.shields.io/github/forks/devoxx/DevoxxGenieIDEAPlugin?style=flat-square&color=blue)](https://github.com/devoxx/DevoxxGenieIDEAPlugin/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> DevoxxGenie is a plugin for IntelliJ IDEA that uses local LLM's (Ollama, LMStudio, GPT4All, Jan and Llama.cpp) and Cloud based LLMs to help review, test, explain your project code. Latest version now also supports Spec Driven Development with CLI Runners.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 662 |
| 🍴 **Forks** | 93 |
| 💻 **Language** | Java |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anthropic` `azure-ai` `chatgpt` `chatgpt-api` `claude-3` `claude-ai` `copilot` `copilot-chat` `gemini` `genai` `gpt4all` `groq`

## 🎯 Categories

AI/ML · Cloud & Storage · Communication · Backend · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
DevoxxGenie is an IntelliJ IDEA plugin that brings AI‑powered code assistance to developers by connecting to local LLMs (Ollama, LMStudio, GPT‑4All, Jan, Llama.cpp) and cloud‑based models. It can review, test, and explain code, and the latest release adds Spec‑Driven Development support via CLI runners. With strong community adoption (≈660 ★, 93 forks) and recent activity, it’s a ready‑to‑evaluate tool for adding AI capabilities without building a model stack from scratch.  

**Value**  
- **Instant AI assistance**: developers get on‑demand code reviews, test generation, and explanations directly inside the IDE, accelerating debugging and learning.  
- **Flexibility**: supports both locally hosted models (useful for privacy‑sensitive projects) and cloud services, letting teams choose the cost‑performance trade‑off that fits their workflow.  
- **Spec‑Driven Development**: the new CLI runners enable automated validation against specifications, bridging the gap between design and implementation.  

**Practical Adoption Path**  
1. **Install the plugin** from the JetBrains Marketplace or directly from the GitHub release assets.  
2. **Configure a model** – point the plugin at a local Ollama/LMStudio server or supply API credentials for a cloud provider.  
3. **Enable desired features** (code review, test generation, spec‑driven CLI) in the plugin settings.  
4. **Iterate**: start with a pilot on a non‑critical module, evaluate output quality, and gradually expand to larger codebases or CI pipelines.  
5. **Optional integration**: use the exposed CLI runners to embed spec checks into build scripts or GitHub Actions for continuous validation.  

**Production Readiness**  
- **Activity & Community**: recent commits (as of 2026‑06‑24), 662 ★, 93 forks, and 20 topical tags indicate an active, engaged community.  
- **Maturity**: core functionality (LLM integration, IDE UI) is stable; the spec‑driven CLI is a newer addition but follows the same well‑tested architecture.  
- **Risk Considerations**: No major metadata or licensing red flags, but a final security audit (dependency scanning, model sandboxing) and verification of maintainer responsiveness are advisable before full‑scale deployment.  

Overall, DevoxxGenieIDEAPlugin is a high‑readiness, low‑friction option for teams that want to prototype or operationalize AI‑enhanced development workflows inside IntelliJ IDEA.

### Русский

DevoxxGenie — плагин для IntelliJ IDEA, который подключает как локальные (Ollama, LMStudio, GPT4All, Jan, Llama.cpp), так и облачные LLM, позволяя автоматически проверять, тестировать и объяснять код, а в последней версии добавлена поддержка Spec‑Driven Development через CLI‑раннеры. Типичный сценарий — быстрое прототипирование AI‑фич, построение RAG‑ или агентных воркфлоу и оценка инструментов модели без необходимости создавать собственный стек. Проект имеет высокий уровень готовности к production: активные коммиты, 662 звезды, 93 форка, широкая экосистема и поддержка Java, что делает его надёжным кандидатом для серьёзного пилотного внедрения.

### 中文

**项目价值**  
DevoxxGenie IDEA 插件让开发者可以在 IntelliJ 中直接调用本地（Ollama、LMStudio、GPT4All、Jan、Llama.cpp）或云端的大语言模型，对代码进行审查、单元测试、解释，甚至支持基于规范的开发（Spec‑Driven Development）和 CLI Runner。它把 AI 能力“即插即用”，免去了自行搭建模型堆栈的前期工作，适合快速原型、RAG/Agent 工作流以及模型评估等场景。

**典型接入方式**  
1. **插件安装**：在 IntelliJ IDEA Marketplace 搜索 *DevoxxGenie* 并一键安装。  
2. **模型配置**：在插件设置页填写本地模型的 API 地址（如 Ollama 的 `http://localhost:11434`）或云服务的凭证。插件会自动发现模型能力并展示语言/代码元数据。  
3. **功能调用**：选中代码块或打开项目视图，右键选择 “AI Review / Explain / Generate Tests”，或在终端使用插件提供的 CLI 命令（`devoxx-genie run …`）进行 Spec‑Driven 流程。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑24，项目仍在维护，最近一次提交在当日，拥有 662 ⭐、93 🍴，社区活跃。  
- **技术成熟度**：基于 Java 开发，兼容 IntelliJ IDEA 最新版本，提供完整的 API/SDK/CLI 接口，易于在 CI/CD 或内部工具链中嵌入。  
- **风险**：许可证（Apache‑2.0）和安全审计尚需进一步确认，但暂无明显元数据或供应链风险。整体来看，已具备 **高** 的生产可用性，适合作为内部 AI 助手或功能原型的首选 OSS 组件。

## 🧭 Practical evaluation

**Value:** devoxx/DevoxxGenieIDEAPlugin helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 662 GitHub stars
- 93 forks
- updated 2026-06-24
- primary language: Java
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 49/100 |
| stars | 60/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 76/100 |
| recency | 80/100 |
| adoption | 57/100 |
| production | 75/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/devoxx/DevoxxGenieIDEAPlugin) · [← Back to AI/ML](./README.md)</sub>
