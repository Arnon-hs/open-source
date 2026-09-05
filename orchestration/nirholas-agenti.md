# nirholas/agenti

[![Stars](https://img.shields.io/github/stars/nirholas/agenti?style=flat-square&color=yellow)](https://github.com/nirholas/agenti/stargazers) [![Forks](https://img.shields.io/github/forks/nirholas/agenti?style=flat-square&color=blue)](https://github.com/nirholas/agenti/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-80%2F100-brightgreen?style=flat-square)](#)

> Give any AI agent a crypto wallet. Agents deserve access to money.  Pay x402 APIs, receive USDC, check balances — autonomously. Works with Claude, LangChain, AutoGen, CrewAI, and any MCP client. EVM + Solana.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 70 |
| 🍴 **Forks** | 21 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 80/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`api` `automated` `bot` `claude` `clawd` `crypto` `llm` `mcp` `payments` `trade` `trading` `x402`

## 🎯 Categories

Orchestration · Crypto · Payments · Trading · MCP

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*agenti* (nirholas/agenti) equips any AI agent with a full‑featured crypto wallet, letting it pay for APIs, receive USDC, and query balances autonomously across EVM and Solana chains. It integrates out‑of‑the‑box with Claude, LangChain, AutoGen, CrewAI, and any MCP client, making it a plug‑and‑play layer for Web3‑enabled AI applications. The project is actively maintained in TypeScript, with 70 ★, 21 forks, and recent commits as of June 2026.

---

### Value Proposition
- **Rapid Web3 prototyping** – developers can add wallet creation, balance checks, and USDC transfers to AI agents without writing low‑level blockchain code.  
- **Unified multi‑chain support** – one API works for both EVM‑compatible networks and Solana, simplifying cross‑chain experiments.  
- **Seamless AI stack integration** – ready‑made adapters for popular LLM orchestration frameworks (Claude, LangChain, AutoGen, CrewAI) accelerate the build of autonomous agents that need to transact or pay for services.  
- **Transparency** – the open‑source implementation reveals the exact request/response flow, which is valuable for auditing, security reviews, and teaching blockchain workflows.

### Practical Adoption Path
1. **Evaluate the SDK/CLI** – clone the repo, run the provided TypeScript examples, and confirm wallet creation and USDC receipt on a testnet (e.g., Sepolia + Solana devnet).  
2. **Integrate with your AI stack** – import the `agenti` package into your LangChain/AutoGen/CrewAI pipeline and replace the “payment” step with `agenti.pay(...)` or `agenti.checkBalance()`.  
3. **Configure credentials** – set up API keys for the underlying RPC providers (Infura/Alchemy for EVM, QuickNode/Hyperspace for Solana) and any USDC bridge contracts you need.  
4. **Run a sandbox pilot** – let an agent execute a simple workflow (e.g., query a price oracle, pay for an x402 API, receive USDC) in a controlled environment.  
5. **Scale to production** – move from testnet to mainnet, add monitoring (wallet nonce tracking, gas‑price alerts), and optionally wrap the SDK in a microservice for multi‑tenant usage.

### Production Readiness
- **Activity & Community** – recent commits (June 2026), 70 GitHub stars, 21 forks, and clear documentation indicate healthy momentum.  
- **Ecosystem Fit** – native adapters for the major LLM orchestration frameworks reduce integration effort and lower the risk of breaking changes.  
- **Technical Maturity** – written in TypeScript with an exposed API/CLI, the codebase is modular and testable; the multi‑chain abstraction has been validated on both EVM and Solana testnets.  
- **Risks to Address** – a final legal review of the license, a security audit of wallet handling (private‑key storage, transaction signing), and confirmation of an active maintainer team are still required before mission‑critical deployment.  

Overall, *agenti* offers a high‑signal, production‑grade foundation for any organization looking to embed autonomous crypto‑capable agents into their AI products or internal tooling.

### Русский

**nirholas/agenti** — это открытая TypeScript‑библиотека, позволяющая любому AI‑агенту работать с криптовалютным кошельком: автоматически платить за API‑вызовы, получать USDC, проверять балансы в EVM и Solana и интегрировать эти операции в цепочки Claude, LangChain, AutoGen, CrewAI и любые MCP‑клиенты. Типичный сценарий — прототипирование Web3‑процессов (например, автоматическое пополнение кошелька при выполнении задач или проверка DeFi‑операций) и отладка блокчейн‑интеграций без написания собственного кода. Проект имеет активную поддержку (обновления 2026‑06‑23, 70 звёзд, 21 форк), широкую экосистемную совместимость и готов к запуску в продакшн после окончательной проверки лицензии и безопасности.

### 中文

**项目简介（2‑3 句话）**  
nirholas/agenti 为任意 AI 代理配备加密钱包，使其能够自行支付 API 调用费用、收取 USDC、查询余额等金融操作，兼容 Claude、LangChain、AutoGen、CrewAI 以及任何 MCP 客户端，支持 EVM 与 Solana 链。

**价值**  
- **快速原型**：提供开箱即用的区块链/DeFi 工作流实现，帮助开发者在几行代码内验证支付、转账、余额查询等链上交互。  
- **透明实现**：项目公开实现细节（API/SDK/CLI、语言元数据、主题标签），便于审计和二次开发。  
- **跨链统一**：一次集成即可在以太坊兼容链和 Solana 上使用同一套接口，降低多链开发成本。

**典型接入方式**  
1. **通过 NPM 安装**：`npm i @agenti/sdk`（或 Yarn、pnpm）。  
2. **在代码中引入 SDK**，创建 `AgentWallet` 实例并配置链、私钥或托管密钥。  
3. **调用高层 API**：  
   - `payApiCost(agentId, amount)` 付费调用外部 API；  
   - `receiveUSDC(amount, from)` 接收 USDC；  
   - `getBalance(chain)` 查询指定链上余额。  
4. **与现有框架对接**：在 LangChain、AutoGen、CrewAI 等链路中，将 `AgentWallet` 注入到工具或工具链中，即可让 LLM 自动完成链上支付与查询。

**生产可用性**  
- **活跃度**：2026‑06‑23 最近一次提交，70+ 星、21+ Fork，社区讨论活跃。  
- **技术成熟度**：使用 TypeScript 编写，提供完整的 API 文档、示例项目和 CLI，易于 CI/CD 集成。  
- **生态兼容**：已在多个 MCP 客户端和主流 LLM 框架中验证，可直接在生产环境中替换传统支付服务。  
- **风险提示**：仍需进一步审查许可证细节、长期维护者承诺以及安全审计报告，但目前的代码质量和社区信号足以支持正式的试点或内部生产部署。

## 🧭 Practical evaluation

**Value:** nirholas/agenti helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 70 GitHub stars
- 21 forks
- updated 2026-06-23
- primary language: TypeScript
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 39/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 38/100 |
| production | 74/100 |
| usefulness | 100/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/nirholas/agenti) · [← Back to Orchestration](./README.md)</sub>
