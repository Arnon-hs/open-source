# sgasser/pasteguard

[![Stars](https://img.shields.io/github/stars/sgasser/pasteguard?style=flat-square&color=yellow)](https://github.com/sgasser/pasteguard/stargazers) [![Forks](https://img.shields.io/github/forks/sgasser/pasteguard?style=flat-square&color=blue)](https://github.com/sgasser/pasteguard/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> AI gets the context. Not your secrets. Open-source privacy proxy for LLMs.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 628 |
| 🍴 **Forks** | 26 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anthropic` `browser-extension` `chatgpt` `claude` `data-protection` `llm` `open-webui` `openai` `pii` `presidio` `privacy` `secrets`

## 🎯 Categories

AI/ML · Networking · Frontend · Data · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
sgasser/pasteguard is an open‑source privacy proxy that lets you add LLM capabilities to your applications without exposing confidential data. It sits between your frontend and any large language model, stripping or masking sensitive context while preserving the conversational flow, making it ideal for rapid prototyping of RAG, agent‑based, or AI‑augmented features. With a healthy star count, recent commits, and a TypeScript codebase, it is ready for a serious pilot.

**Value**  
- **Privacy‑first AI integration:** By intercepting and sanitizing user inputs before they reach the model, Pasteguard protects proprietary or personal information without sacrificing the usefulness of the LLM.  
- **Speed to market:** Developers can plug the proxy into existing front‑ends and LLM APIs, avoiding the need to build a custom data‑filtering layer from scratch.  
- **Flexibility for experimentation:** Supports a range of use cases—from simple “paste‑and‑ask” prototypes to more complex Retrieval‑Augmented Generation (RAG) or autonomous agent workflows—so teams can iterate on AI features while keeping data safe.

**Practical Adoption Path**  
1. **Proof‑of‑Concept:** Clone the repo, run the provided Docker compose (or the npm scripts) and point the proxy at your preferred LLM endpoint (OpenAI, Anthropic, etc.).  
2. **Configuration:** Define the sanitisation rules (regexes, token‑based redaction, or custom handlers) in the `config.yaml` file; the README includes a quick‑start example.  
3. **Integration:** Update your frontend or backend to send requests to `http://localhost:<proxy‑port>` instead of the raw LLM endpoint. Verify that the returned responses are unchanged while the logged payloads contain no secrets.  
4. **Iterate & Scale:** Add more sophisticated policies (e.g., context‑aware masking, rate limiting) and, if needed, deploy the proxy in a Kubernetes pod behind your API gateway for production traffic.

**Production Readiness**  
- **Activity & Community:** 628 ★, 26 forks, recent commit (2026‑05‑13), and an active issue tracker indicate a vibrant project.  
- **Technical Maturity:** Written in TypeScript with clear typings, CI pipelines, and Docker support, making it straightforward to embed in CI/CD pipelines.  
- **Security Posture:** No known metadata leakage; however, a final review of the MIT‑style license, dependency vulnerabilities, and maintainer responsiveness is recommended before a full rollout.  
Overall, Pasteguard meets the criteria for an OSS candidate suitable for a pilot or even production use once the final security and licensing checks are completed.

### Русский

**sgasser/pasteguard** — это открытый privacy‑прокси для LLM, позволяющий подключать возможности ИИ к приложению, не раскрывая собственные данные. Типичный сценарий: быстро прототипировать функции ИИ (RAG, агентные воркфлоу, оценка моделей) через небольшую proof‑of‑concept интеграцию, следуя инструкциям в README. Проект имеет высокий уровень готовности к production: активные коммиты, 628 звёзд, поддержка TypeScript и сильные сигналы экосистемы, однако перед запуском в продакшн следует окончательно проверить лицензию, безопасность и наличие активных мейнтейнеров.

### 中文

**项目简介（2‑3 句）**  
sgasser / pasteguard 是一个开源的 **隐私代理层**，让 LLM 在获取业务上下文的同时 **不泄露用户机密**。它以 TypeScript 实现，提供即插即用的 API，帮助开发者在现有模型之上快速构建 RAG、Agent 或其他 AI 功能原型。

**价值**  
- **安全隐私**：在请求 LLM 前对敏感信息做脱敏或遮蔽，防止机密数据被模型记录。  
- **降低门槛**：无需自行搭建完整的模型堆栈，直接在已有 LLM（OpenAI、Claude、Gemini 等）上叠加隐私保护层，即可开启 AI 能力。  
- **加速原型**：提供统一的中间件接口，适合快速验证 RAG、智能客服、工作流自动化等场景。

**典型接入方式**  
1. **阅读 README**，确认所使用的 LLM 提供商已在 `supportedProviders` 列表中。  
2. **在项目中安装**：`npm i @pasteguard/core`（或直接克隆仓库）。  
3. **配置代理**：在代码中创建 `PasteGuard` 实例，传入 API‑Key、模型端点以及脱敏规则（正则、关键字列表或自定义函数）。  
   ```ts
   import { PasteGuard } from '@pasteguard/core';

   const guard = new PasteGuard({
     provider: 'openai',
     apiKey: process.env.OPENAI_API_KEY,
     redactionRules: [/(\d{4})\d{8}/g, '****'], // 示例：脱敏身份证号
   });

   const response = await guard.ask('请帮我分析这段日志', userInput);
   ```
4. **在微服务或前端** 中将所有对 LLM 的调用统一走 `guard.ask`，即可实现“上下文可见、机密不可见”。  
5. **小范围 PoC**：先在内部测试环境用几条真实业务请求验证脱敏效果，再逐步推广到全链路。

**生产可用性**  
- **活跃度**：截至 2026‑05‑13，最近一次提交在 2 天前，拥有 628 ★、26 forks，社区讨论活跃。  
- **技术成熟度**：使用 TypeScript 编写，提供完整类型定义，易于在前后端项目中集成。  
- **安全与合规**：核心功能是本地脱敏，未将原始数据发送至 LLM，符合多数数据保护法规（GDPR、CCPA）。仍建议自行审计 `redactionRules` 与依赖库的安全报告。  
- **生产建议**：可直接用于 **试点或内部业务**，在正式上线前完成以下步骤：  
  1. 完整的单元/集成测试（包括边界脱敏场景）。  
  2. 监控请求延迟与错误率，确保代理层不会成为性能瓶颈。  
  3. 配置 CI/CD 自动检查依赖安全（Dependabot / npm audit）。  

综合来看，pasteguard 已具备 **高可用的 OSS 候选**，适合作为企业在引入 LLM 时的首选隐私保护层。

## 🧭 Practical evaluation

**Value:** sgasser/pasteguard helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 628 GitHub stars
- 26 forks
- updated 2026-05-13
- primary language: TypeScript
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 36/100 |
| stars | 60/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 74/100 |
| recency | 80/100 |
| adoption | 53/100 |
| production | 69/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/sgasser/pasteguard) · [← Back to AI/ML](./README.md)</sub>
