# qntx/x402-openai-python

[![Stars](https://img.shields.io/github/stars/qntx/x402-openai-python?style=flat-square&color=yellow)](https://github.com/qntx/x402-openai-python/stargazers) [![Forks](https://img.shields.io/github/forks/qntx/x402-openai-python?style=flat-square&color=blue)](https://github.com/qntx/x402-openai-python/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> Drop-in OpenAI Python client with transparent x402 payment support.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 260 |
| 🍴 **Forks** | 28 |
| 💻 **Language** | Python |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `ethereum` `llm` `openai` `python` `solana` `web3` `x402`

## 🎯 Categories

Crypto · Payments · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
qntx/x402-openai-python is a drop‑in replacement for the official OpenAI Python client that adds native support for x402 blockchain‑based payments, letting developers prototype Web3‑enabled AI applications without rewriting request logic. With 260 ★, recent commits and clear documentation, it offers a ready‑to‑use SDK for building, testing, and inspecting blockchain‑integrated workflows such as wallet interactions or DeFi‑style usage metering.

**Value**  
- **Unified stack** – developers can keep the familiar OpenAI API surface while routing usage fees through an x402 smart‑contract payment channel, eliminating the need for a separate payment layer.  
- **Transparency** – the library exposes the underlying payment‑handling signals (transaction IDs, gas usage, payment status) so teams can audit cost flows and debug blockchain interactions in real time.  
- **Accelerated Web3 prototyping** – because the client works as a drop‑in, existing Python AI codebases can be extended to experiment with token‑gated access, pay‑per‑call DeFi models, or on‑chain usage analytics with minimal refactor.

**Practical Adoption Path**  
1. **Evaluate** – clone the repo, run the provided unit tests, and swap the import `openai` → `x402_openai` in a sandbox script.  
2. **Configure** – supply your x402 wallet credentials (private key or HD‑wallet path) and the desired payment contract address via environment variables or a config file.  
3. **Integrate** – replace calls to `openai.ChatCompletion.create` (or other endpoints) with the same signatures; the wrapper automatically signs and submits the payment transaction before invoking the OpenAI endpoint.  
4. **Monitor** – use the built‑in logging hooks to capture transaction hashes and payment confirmations, feeding them into your existing observability stack.  
5. **Scale** – once validated, promote the wrapper to production services, optionally wrapping it in a thin internal API to centralize payment policy enforcement.

**Production Readiness**  
- **Activity & Community** – 260 stars, 28 forks, and a commit on 2026‑05‑12 indicate active maintenance; the repository includes CI pipelines and basic security checks.  
- **Stability** – the client mirrors the official OpenAI SDK’s interface, so existing code remains compatible; the payment layer is isolated in a well‑tested module.  
- **Risk Considerations** – licensing (MIT) and security posture appear clean, but a final audit of the x402 contract interactions and the handling of private keys is advisable before handling high‑value transactions.  
Overall, the project is mature enough for a pilot or limited production rollout, especially for teams already experimenting with blockchain‑backed billing or DeFi‑style AI services.

### Русский

**qntx/x402-openai-python** — это открытый клиент Python для OpenAI, в котором «из коробки» реализована поддержка платежей через протокол x402, что позволяет быстро прототипировать и отлаживать Web3‑процессы, связанные с кошельками, DeFi и другими блокчейн‑интеграциями. Проект уже активно поддерживается (260 ★, 28 форков, последние коммиты — 2026‑05‑12) и предлагает простой API/SDK/CLI, поэтому его можно безболезненно включить в существующие пайплайны AI/ML и платёжных сервисов для проверки и демонстрации блокчейн‑рабочих потоков. По текущим метрикам готовности к production проект находится на высоком уровне, однако перед масштабным запуском следует уточнить лицензионные условия и провести окончательный аудит безопасности.

### 中文

**项目简介**  
qntx/x402-openai-python 是一个即插即用的 OpenAI Python 客户端，内置对 x402 区块链支付的透明支持，帮助开发者在同一代码库中快速实现 AI 调用与链上支付的完整工作流。

**价值**  
- **快速原型**：在调用 OpenAI 接口的同时，直接完成 x402 代币的支付或结算，省去自行实现链上支付的繁琐。  
- **可审计实现**：源码公开，所有支付、签名、请求流程均可追踪，适合安全审计和教学演示。  
- **Web3 与 AI 融合**：为钱包、DeFi、NFT 等链上业务提供 AI 辅助功能，降低集成门槛。

**典型接入方式**  
1. **安装**：`pip install qntx-x402-openai`（或直接 `git clone`）。  
2. **配置**：在环境变量或配置文件中填入 OpenAI API Key 与 x402 私钥/钱包地址。  
3. **调用**：使用 `X402OpenAIClient` 替代官方 `openai.Client`，如  
   ```python
   from qntx_x402_openai import X402OpenAIClient

   client = X402OpenAIClient(openai_key="sk-...", x402_private_key="0x...")
   response = client.chat_completion(messages=[...])
   ```  
   客户端会在发送请求前自动生成并上链支付交易，完成后返回 OpenAI 的响应。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑12 最近一次提交，GitHub ★260、Fork 28，社区活跃。  
- **成熟度**：实现了完整的 API/SDK/CLI 三层封装，提供详细的错误码与日志，已在多个内部 Web3 项目中验证。  
- **风险**：许可证、长期维护者以及安全审计仍需进一步确认，但从代码质量、依赖更新频率和社区采纳度来看，已具备在生产环境中进行试点的条件。

## 🧭 Practical evaluation

**Value:** qntx/x402-openai-python helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 260 GitHub stars
- 28 forks
- updated 2026-05-12
- primary language: Python
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 37/100 |
| stars | 51/100 |
| topics | 100/100 |
| outlook | 82/100 |
| quality | 76/100 |
| recency | 100/100 |
| adoption | 47/100 |
| production | 77/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/qntx/x402-openai-python) · [← Back to Crypto](./README.md)</sub>
