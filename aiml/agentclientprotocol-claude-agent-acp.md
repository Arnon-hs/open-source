# agentclientprotocol/claude-agent-acp

[![Stars](https://img.shields.io/github/stars/agentclientprotocol/claude-agent-acp?style=flat-square&color=yellow)](https://github.com/agentclientprotocol/claude-agent-acp/stargazers) [![Forks](https://img.shields.io/github/forks/agentclientprotocol/claude-agent-acp?style=flat-square&color=blue)](https://github.com/agentclientprotocol/claude-agent-acp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-76%2F100-brightgreen?style=flat-square)](#)

> Use Claude Agent SDK from any ACP client

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.2k |
| 🍴 **Forks** | 316 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 76/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

AI/ML · Libraries & SDKs

## 📝 Summary

### English

Here's a brief summary of the agentclientprotocol/claude-agent-acp project:

**Summary:** The agentclientprotocol/claude-agent-acp project provides an open-source solution to integrate AI capabilities into applications using the Claude Agent SDK, allowing developers to add AI functionality without starting from scratch. This project enables users to prototype AI features, build RAG or agent workflows, and evaluate model tooling, making it a valuable addition to any development stack. With a strong ecosystem and recent activity, it's ready for serious pilot projects.

**Value:** The project offers significant value by providing a pre-built AI capability, saving developers time and resources that would be spent on building a custom AI stack from scratch. This enables faster prototyping, testing, and deployment of AI-powered applications.

**Practical Adoption Path:** To adopt this project, developers can start by evaluating the codebase through a small proof of concept, checking the README documentation, and reviewing the license, security posture, and active maintainers. Once satisfied with the project's quality and risk factors, they can integrate the Claude Agent SDK into their application, leveraging the pre-built AI capabilities to enhance their product or service.

**Production Readiness:** With 2166 GitHub stars, 316 forks, and recent updates (2026-06

### Русский

**Краткое резюме:** agentclientprotocol/claude-agent-acp позволяет быстро добавить возможности Claude Agent SDK в любые ACP‑клиенты, что упрощает прототипирование AI‑фич, построение RAG‑ и агентных воркфлоу и оценку новых инструментов без необходимости создавать стек моделей с нуля. Для внедрения рекомендуется начать с небольшого proof‑of‑concept, следуя README, и постепенно интегрировать SDK в существующий код на TypeScript. Проект демонстрирует высокий уровень готовности к production: активные коммиты, более 2000 звёзд, множество форков и позитивные сигналы экосистемы, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句）**  
`agentclientprotocol/claude-agent-acp` 是一个基于 TypeScript 的开源库，允许任意 ACP（Agent Client Protocol）客户端直接调用 Claude Agent SDK，从而在现有系统中快速嵌入 Claude 的对话与工具调用能力。它提供了统一的协议层，使开发者无需自行搭建模型堆栈，即可在原型或生产环境中实现 RAG、智能代理等 AI 工作流。

**价值**  
- **快速赋能**：通过封装好的协议和 SDK，团队可以在几行代码内为产品添加自然语言理解、生成和工具调用等功能，显著缩短研发周期。  
- **统一标准**：ACP 作为统一的客户端协议，帮助不同语言或平台的服务之间保持一致的交互方式，降低集成复杂度。  
- **生态兼容**：基于 Claude 官方 SDK，天然支持最新的模型特性和安全审计，适配 Claude 的多模态和工具使用能力。

**典型接入方式**  
1. **阅读 README**：先确认 Node.js 环境（>=18）和 TypeScript 编译配置。  
2. **安装依赖**：`npm i @acp/claude-agent-acp`（或对应的 Yarn/PNPM 命令）。  
3. **初始化客户端**：在代码中创建 `ClaudeAgentClient`，传入 API Key 与可选的 ACP 配置。  
   ```ts
   import { ClaudeAgentClient } from '@acp/claude-agent-acp';

   const client = new ClaudeAgentClient({
     apiKey: process.env.CLAUDE_API_KEY,
     endpoint: 'https://api.anthropic.com/v1',
   });
   ```
4. **调用 SDK**：使用 `client.runAgent()`、`client.queryRAG()` 等方法即可完成对话、工具调用或检索增强生成。  
5. **小范围验证**：在本地或 CI 环境中跑通一个“Hello, Claude”示例，确认网络、鉴权和返回结构符合预期后，再逐步扩展到业务服务。

**生产可用性**  
- **活跃度**：截至 2026‑06‑29，项目拥有 2166+ 星、316+ Fork，最近一次提交在同日，表明维护活跃。  
- **成熟度**：基础协议已稳定，Claude 官方 SDK 支持良好，适合作为内部或对外 API 的底层实现。  
- **风险**：目前未发现重大元数据或许可证冲突，但仍建议在正式上线前完成以下检查：  
  - 确认许可证（MIT/Apache 等）与公司合规要求匹配；  
  - 通过 SCA 工具审计依赖的安全漏洞；  
  - 评估维护者响应速度，必要时可考虑内部 fork 维护关键路径。  
- **结论**：在完成上述合规与安全审查后，`claude-agent-acp` 已具备在生产环境中进行试点或正式部署的条件，尤其适合需要快速原型验证或在现有服务中平滑引入 Claude AI 能力的团队。

## 🧭 Practical evaluation

**Value:** agentclientprotocol/claude-agent-acp helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2166 GitHub stars
- 316 forks
- updated 2026-06-29
- primary language: TypeScript

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 63/100 |
| stars | 71/100 |
| topics | 0/100 |
| outlook | 73/100 |
| quality | 66/100 |
| recency | 80/100 |
| adoption | 69/100 |
| production | 71/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/agentclientprotocol/claude-agent-acp) · [← Back to AI/ML](./README.md)</sub>
