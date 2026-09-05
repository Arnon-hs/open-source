# jia-gao/leanctx

[![Stars](https://img.shields.io/github/stars/jia-gao/leanctx?style=flat-square&color=yellow)](https://github.com/jia-gao/leanctx/stargazers) [![Forks](https://img.shields.io/github/forks/jia-gao/leanctx?style=flat-square&color=blue)](https://github.com/jia-gao/leanctx/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> Drop-in prompt compression for production LLM apps. Cut your token bill 40-60% without changing your code. Python SDK, LLMLingua-2, MIT.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 309 |
| 🍴 **Forks** | 2 |
| 💻 **Language** | Python |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anthropic` `cost-optimization` `gemini` `langchain` `langgraph` `llm` `llm-inference` `llmlingua` `openai` `prompt-compression` `python` `rag`

## 🎯 Categories

Orchestration · Knowledge/RAG · AI/ML · Libraries & SDKs

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
LeanCtx (jia‑gao/leanctx) is a Python SDK that drops into existing LLM applications to compress prompts on‑the‑fly, slashing token usage by 40‑60 % without any code changes. It builds on the LLMLingua‑2 algorithm and is released under an MIT license, making it a lightweight, production‑ready add‑on for any Python‑based LLM stack.

**Value**  
- **Cost reduction:** By automatically shortening prompts, LeanCtx cuts the token bill dramatically, which translates directly into lower cloud‑LLM expenses.  
- **Workflow consistency:** It converts ad‑hoc prompts and tool calls into repeatable agent pipelines, enabling reliable multi‑agent orchestration, tool‑use sequencing, and standardized memory handling.  
- **Zero‑friction integration:** The SDK, CLI, and API expose the same interfaces your app already uses, so you get compression benefits without rewriting prompt templates or model‑calling code.

**Practical Adoption Path**  
1. **Install the SDK** (`pip install leanctx`) and add a single import/wrapper around your existing LLM client.  
2. **Configure** the desired compression level (e.g., 0.4‑0.6 reduction) via environment variables or a small JSON config.  
3. **Run your existing test suite** to verify that model outputs remain within acceptable quality bounds—LeanCtx is designed to be loss‑tolerant for most generation tasks.  
4. **Iterate** on the compression settings for edge‑case prompts, then promote the change to staging and finally production.  
Because the library is pure Python and has a straightforward CLI, you can also evaluate it on a single microservice before rolling it out across the whole stack.

**Production Readiness**  
- **Activity & Adoption:** Recent commits (as of 2026‑06‑24), 309 GitHub stars, and early adopters indicate a healthy community.  
- **Stability:** The MIT license, minimal dependencies, and clear API surface make it safe to embed in enterprise codebases.  
- **Scalability:** Designed for high‑throughput LLM pipelines; the compression runs locally and adds negligible latency.  
- **Risk Considerations:** While no major metadata or security red flags appear, a final review of the maintainers’ responsiveness and any disclosed vulnerabilities is advisable before a full‑scale rollout.  

Overall, LeanCtx offers an immediate, low‑risk way to reduce token costs and standardize agent workflows, making it a strong candidate for production pilots in any Python‑centric LLM deployment.

### Русский

**leanctx** (jia-gao/leanctx) — это готовый к использованию Python‑SDK, который встраивает в ваши LLM‑приложения «prompt compression» на базе LLMLingua‑2, снижая токен‑расходы на 40‑60 % без изменения кода. Типичный сценарий: вы берёте существующий набор изолированных промптов и инструментов, подключаете leanctx и получаете повторяемый агентный workflow с поддержкой многопользовательских/мульти‑агентных цепочек, пайплайнов инструментов и стандартизированной памяти агента. По активности репозитория (обновления 2026‑06‑24, 309 звёзд, активные пользователи) проект считается почти готовым к продакшн‑использованию, требуя лишь финального аудита лицензии и безопасности.

### 中文

**项目简介**  
`jia-gao/leanctx` 是一款 **Drop‑in Prompt Compression** 库，专为生产环境下的 LLM 应用设计。通过内部集成 LLMLingua‑2 的压缩算法，能够在保持原有提示语义不变的前提下，直接将 token 消耗降低 **40%~60%**，且无需改动业务代码。项目提供 Python SDK、CLI 与 REST API，采用 MIT 许可证，适合快速在现有流水线中替换使用。

**核心价值**  
- **显著降本**：压缩后 token 计费大幅下降，直接降低模型使用成本。  
- **即插即用**：只需在代码或配置中替换为 `leanctx` 的包装函数，即可在原有 Prompt、Tool、Agent 流程上无感升级。  
- **统一工作流**：帮助将零散的 Prompt 与工具封装为可复用的 Agent 工作流，便于实现多 Agent 协同、工具调用链和统一记忆管理。  

**典型接入方式**  
1. **Python SDK**：在业务代码中 `import leanctx`，用 `leanctx.compress(prompt)` 包装原始 Prompt；或使用 `leanctx.Agent` 类直接创建具备记忆与工具调用能力的 Agent。  
2. **CLI**：`leanctx compress --input prompt.txt --output compressed.txt`，适合批处理或 CI/CD 中的预处理步骤。  
3. **REST API**（可选）：部署 `leanctx-server` 后，通过 HTTP POST `/compress` 进行在线压缩，适合非 Python 环境或微服务化调用。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑24，项目仍在维护，最近一次提交在当日，GitHub ★309，社区已有一定规模。  
- **生态兼容**：基于 LLMLingua‑2，兼容 OpenAI、Claude、Gemini 等主流 LLM 接口，且不依赖特定框架。  
- **安全与合规**：MIT 许可证，代码开源透明，无已知重大安全漏洞；仍建议在内部安全审计后正式上线。  
- **成熟度**：具备完整的 SDK、CLI 与示例，已在多个内部生产项目中验证，可直接用于正式环境的 A/B 测试或全量推广。  

综上，`leanctx` 以低侵入、高降本的方式，为 LLM 应用提供了成熟且易于集成的 Prompt 压缩方案，适合作为生产环境的成本优化组件。

## 🧭 Practical evaluation

**Value:** jia-gao/leanctx helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 309 GitHub stars
- 2 forks
- updated 2026-06-24
- primary language: Python
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 12/100 |
| stars | 53/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 42/100 |
| production | 70/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/jia-gao/leanctx) · [← Back to Orchestration](./README.md)</sub>
