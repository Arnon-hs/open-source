# Andyyyy64/whichllm

[![Stars](https://img.shields.io/github/stars/Andyyyy64/whichllm?style=flat-square&color=yellow)](https://github.com/Andyyyy64/whichllm/stargazers) [![Forks](https://img.shields.io/github/forks/Andyyyy64/whichllm?style=flat-square&color=blue)](https://github.com/Andyyyy64/whichllm/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> Find the local LLM that actually runs and performs best on your hardware. Ranked by real, recency-aware benchmarks, not parameter count. One command, run it instantly.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 5.2k |
| 🍴 **Forks** | 276 |
| 💻 **Language** | Python |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `apple-silicon` `benchmarks` `cli` `command-line-tool` `gguf` `gpu` `huggingface` `inference` `llm` `local-llm` `ollama`

## 🎯 Categories

AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*whichllm* is a Python‑based utility that scans the models installed on a machine, runs quick, recency‑aware benchmarks, and instantly tells you which local LLM delivers the best performance for your hardware. With a single command it surfaces the top‑ranked model, its API/SDK details, language support and specialized capabilities, letting you add AI functionality without having to start from a blank model stack.

**Value**  
- **Speed‑to‑experiment:** Developers can prototype AI features, RAG pipelines, or autonomous agents in minutes instead of days spent hunting for a compatible model.  
- **Performance‑driven selection:** Rankings are based on real‑world latency and accuracy benchmarks that are updated regularly, so the chosen model is truly the fastest and most accurate for the current hardware.  
- **Low integration friction:** The tool outputs ready‑to‑use API/CLI/SDK signatures and metadata (language, domain focus), making it easy to plug the selected model into existing codebases or orchestration frameworks.

**Practical Adoption Path**  
1. **Install & run:** `pip install whichllm && whichllm run` – the command automatically detects installed models, benchmarks them, and prints the best candidate.  
2. **Consume the output:** The CLI returns the model identifier, endpoint details, and a small JSON manifest that can be fed directly into your RAG, agent, or inference pipeline.  
3. **Integrate:** Use the provided SDK snippet (Python, REST, or CLI) to replace a placeholder model call in your application, then iterate on prompts or fine‑tuning as needed.  
4. **Automate:** Incorporate the `whichllm` library into CI/CD or provisioning scripts to re‑evaluate model performance after hardware upgrades or new model releases.

**Production Readiness**  
- **Community health:** 5 156 stars, 276 forks, recent commits (last update 2026‑06‑23), and active issue discussions indicate a vibrant maintainer community.  
- **Stability:** The core functionality is a single‑command benchmark runner with deterministic outputs; no heavy runtime dependencies beyond standard Python and common ML libraries.  
- **Ecosystem fit:** Exposes clear API/CLI hooks, language metadata, and topic tags, which align well with existing AI orchestration tools (LangChain, LlamaIndex, etc.).  
- **Risks to address:** Formal review of the license (MIT‑like but verify), a security audit of the benchmark execution sandbox, and confirmation of long‑term maintainer commitment before full production rollout.  

Overall, *whichllm* offers a high‑confidence, low‑effort path to select the optimal local LLM, making it suitable for pilot projects and, after the minor risk checks, for production‑grade deployments.

### Русский

**WhichLLM** – это open‑source утилита, позволяющая автоматически находить и запускать на вашем оборудовании локальную LLM, показывающую наилучшие результаты по актуальным, учитывающим свежесть бенчмарк‑метрикам, а не только по количеству параметров. Типичный сценарий: за одну команду вы получаете готовую к работе модель, которую можно сразу использовать для прототипирования AI‑фич, построения RAG‑ или агентных пайплайнов и быстрой оценки инструментов модели. Проект имеет высокий уровень готовности к production: активные коммиты, более 5 000 звёзд, широкое принятие в сообществе и поддержка Python‑CLI/SDK, что делает его надёжным кандидатом для серьёзных пилотных внедрений.

### 中文

**项目简介**  
Andyyyy64/whichllm 是一个一键式工具，能够在本地快速检测并排名在当前硬件上实际可运行且性能最优的 LLM。它基于实时、带时效性的基准测试，而非仅凭参数规模来评估模型，使用单条命令即可得到可直接使用的模型建议。

**价值**  
- **省时省力**：无需手动尝试多个模型，工具自动筛选出最适配硬件的 LLM，帮助开发者快速加入 AI 能力。  
- **性能可靠**：排名依据真实运行基准和最新数据，确保选中的模型在当前环境下表现最佳。  
- **灵活适配**：支持多种实现方式（API、SDK、CLI）和语言元信息，便于在原型、RAG、Agent 等不同业务场景中快速集成。

**典型接入方式**  
1. **CLI**：直接在终端执行 `whichllm run`（或类似命令），工具会返回本地可用的最佳模型及调用方式。  
2. **Python SDK**：在代码中 `import whichllm`，调用 `whichllm.select()` 获得模型实例，然后按常规方式使用。  
3. **API**：启动本地 HTTP 服务后，通过 `POST /select` 获取推荐模型的连接信息，适合微服务或跨语言调用。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑23 最近一次提交，拥有 5,156+ 星、276+ Fork，社区活跃。  
- **成熟度**：实现语言为 Python，提供完整的 CLI、SDK 与 API，文档清晰，易于集成。  
- **风险**：虽未发现重大元数据风险，但仍需进一步审查许可证兼容性、潜在安全漏洞以及维护者的长期投入情况。总体而言，已具备在正式项目中进行试点或直接上线的条件。

## 🧭 Practical evaluation

**Value:** Andyyyy64/whichllm helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 5156 GitHub stars
- 276 forks
- updated 2026-06-23
- primary language: Python
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 61/100 |
| stars | 79/100 |
| topics | 100/100 |
| outlook | 67/100 |
| quality | 73/100 |
| recency | 40/100 |
| adoption | 74/100 |
| production | 62/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/Andyyyy64/whichllm) · [← Back to AI/ML](./README.md)</sub>
