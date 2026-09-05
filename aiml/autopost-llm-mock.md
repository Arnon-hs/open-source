# autopost/llm-mock

[![Stars](https://img.shields.io/github/stars/autopost/llm-mock?style=flat-square&color=yellow)](https://github.com/autopost/llm-mock/stargazers) [![Forks](https://img.shields.io/github/forks/autopost/llm-mock?style=flat-square&color=blue)](https://github.com/autopost/llm-mock/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-38%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 38/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
LLM‑mock is an open‑source pytest plugin that records calls to OpenAI and Anthropic APIs and can replay them later, enabling deterministic testing of LLM‑driven code. By capturing request/response payloads, it lets developers prototype, unit‑test, and benchmark AI features without incurring live‑API costs or dealing with flaky external services. The project is actively maintained (last update 2026‑07‑13) and targets AI/ML and DevTools use cases such as RAG pipelines, agent workflows, and model‑tooling evaluation.

**Value**  
- **Fast, cost‑effective prototyping** – developers can iterate on prompts, retrieval‑augmented generation, or agent logic without repeatedly hitting paid APIs.  
- **Deterministic test suites** – recorded fixtures guarantee repeatable CI runs, catching regressions in prompt engineering or response handling.  
- **Seamless pytest integration** – works with existing test frameworks, requiring only a decorator or fixture to swap live calls for mocks.  

**Practical Adoption Path**  
1. **Add the dependency** (`pip install llm-mock`) to your development environment.  
2. **Wrap existing OpenAI/Anthropic client calls** with the provided `@mock_llm` decorator or use the `llm_mock` fixture in your pytest files.  
3. **Run the test suite once against the real APIs** to generate the “cassette” files that store request/response pairs.  
4. **Commit the cassette files** (or store them in a secure artifact store) and switch the test configuration to replay mode for CI/CD pipelines.  
5. **Periodically refresh cassettes** by re‑recording against the live APIs when you upgrade models or change prompts.  

**Production Readiness**  
- **Maturity:** Medium – the tool is stable enough for internal prototypes and CI testing, but it lacks extensive production‑grade features (e.g., automatic secret redaction, multi‑tenant cassette management).  
- **Dependencies & Maintenance:** Requires the official OpenAI/Anthropic SDKs and pytest; the repository shows recent activity, but you should verify the license, open issues, and release cadence before committing to long‑term use.  
- **Risk Mitigation:** Perform a manual code review of the recorded payloads to ensure no sensitive data is persisted, and run a small‑scale pilot to confirm that replayed responses match expected behavior under load.  

In short, LLM‑mock offers a pragmatic way to embed AI capabilities into your codebase while keeping tests fast, cheap, and reliable; it is ready for internal or prototype deployments, provided you conduct the usual due‑diligence checks before scaling to production.

### Русский

**Show HN: LLM‑mock – Record and replay OpenAI/Anthropic calls in pytest (v1.0)** – это open‑source утилита, позволяющая быстро добавить AI‑функциональность в проекты, записывая реальные запросы к моделям OpenAI/Anthropic и воспроизводя их в тестах pytest. Типичный сценарий — прототипирование новых AI‑фич, построение RAG‑ или агентных пайплайнов и оценка инструментов без необходимости обращения к внешним сервисам. Готовность к production — средняя: подходит для прототипов и внутренних процессов, но требует ручной проверки лицензии, поддержки и документации перед запуском в продакшн.

### 中文

**项目简介**  
Show HN: LLM‑mock – Record and replay OpenAI/Anthropic calls in pytest (v1.0) 是一个用于在 pytest 环境中记录并回放 OpenAI 与 Anthropic API 调用的测试工具。它让开发者可以在不实际调用外部大模型的情况下，快速验证和调试 AI 功能。

**价值**  
- **降低成本**：通过录制真实的 API 响应，避免在开发、CI/CD 流程中频繁消耗付费的模型调用额度。  
- **加速原型**：在本地即可复现相同的模型输出，帮助团队快速迭代 RAG、Agent 或其他 AI 工作流的原型。  
- **提升可靠性**：在离线环境下运行单元测试，避免外部网络波动或服务限流导致的 flaky 测试。

**典型接入方式**  
1. **安装**：`pip install llm-mock`（或从源码安装）。  
2. **在 pytest 中启用**：在 `conftest.py` 中加入 `import llm_mock; llm_mock.enable()`。  
3. **录制模式**：首次运行时使用 `--record` 参数，实际调用 OpenAI/Anthropic 并将请求/响应保存为 JSON/YAML 文件。  
4. **回放模式**：后续测试省去 `--record`，LLM‑mock 会拦截对应的调用并返回已保存的响应。  
5. **手动审查**：在将录制文件用于正式项目之前，人工检查响应是否符合业务预期，确保不泄露敏感信息。

**生产可用性**  
- **成熟度**：目前标记为 **Medium**，适合原型开发、内部工具或 CI 环境的自动化测试。  
- **依赖与维护**：项目仍在活跃维护（最近一次更新 2026‑07‑13），但元数据中集成信号稀少，建议在引入前检查许可证、issue 活跃度、文档完整度以及发布周期。  
- **上线建议**：在生产环境使用前，进行以下检查：  
  1. **许可证兼容性**（确认符合公司开源合规）。  
  2. **录制文件安全**（去除可能的 PII、API 密钥等）。  
  3. **回放准确性**（通过对比真实调用结果验证回放的可靠性）。  
  4. **监控与回退**：在关键业务流中保留真实调用的 fallback 机制，以防录制文件失效。  

综上，LLM‑mock 是一个在开发和测试阶段显著提升效率的工具，适合在内部或原型阶段快速集成 AI 能力；在生产环境使用时，需要做好审查、监控和回退策略，以确保安全性和可靠性。

## 🧭 Practical evaluation

**Value:** Show HN: LLM-mock – Record and replay OpenAI/Anthropic calls in pytest (v1.0) helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-07-13
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 47/100 |
| quality | 36/100 |
| recency | 80/100 |
| adoption | 0/100 |
| production | 51/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/autopost/llm-mock) · [← Back to AI/ML](./README.md)</sub>
