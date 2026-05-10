# aws-samples/sample-strands-agent-with-agentcore

[![Stars](https://img.shields.io/github/stars/aws-samples/sample-strands-agent-with-agentcore?style=flat-square&color=yellow)](https://github.com/aws-samples/sample-strands-agent-with-agentcore/stargazers) [![Forks](https://img.shields.io/github/forks/aws-samples/sample-strands-agent-with-agentcore?style=flat-square&color=blue)](https://github.com/aws-samples/sample-strands-agent-with-agentcore/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-76%2F100-brightgreen?style=flat-square)](#)

> Reference architecture for agentic AI chatbots with Strands Agents and Amazon Bedrock AgentCore

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 155 |
| 🍴 **Forks** | 50 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 76/100 |
| 🗓️ **Last push** | 2026-05-10 |
| 🔍 **Source** | github |

## 🏷️ Topics

`a2a-protocol` `agent-to-agent` `agentcore` `ai-agents` `amazon-bedrock` `browser-automation` `mcp` `multi-agent` `skills` `strands-agents` `voice-assistant`

## 🎯 Categories

Orchestration · MCP · Automation · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The *aws-samples/sample‑strands‑agent‑with‑agentcore* repository provides a reference architecture that shows how to build agentic AI chatbots using Strands Agents together with Amazon Bedrock AgentCore. It demonstrates how to turn isolated prompts and tool calls into repeatable, orchestrated agent workflows, complete with memory handling and multi‑agent coordination. The sample is written in TypeScript, actively maintained, and includes ready‑to‑use API/SDK/CLI snippets for quick evaluation.

**Value**  
- **From ad‑hoc prompts to reusable agents** – By wiring prompts, tools, and memory into a single orchestrated flow, developers can create production‑grade chatbots that are maintainable and extensible.  
- **Multi‑agent and tool‑use patterns** – The reference shows how to coordinate several specialized agents and integrate external tools (e.g., search, database, or custom APIs) in a standardized pipeline.  
- **Accelerated onboarding** – The project ships ready‑made TypeScript examples, API contracts, and deployment scripts, reducing the time needed to prototype and iterate on agentic solutions.

**Practical Adoption Path**  
1. **Clone & explore** – Fork the repo, run the provided `npm install` and `npm run dev` scripts to spin up the local demo.  
2. **Customize prompts & tools** – Replace the sample prompts and tool definitions with your own business logic, leveraging the same AgentCore SDK calls.  
3. **Integrate with your environment** – Hook the TypeScript service into your CI/CD pipeline, connect it to your existing AWS resources (Bedrock models, IAM roles, VPCs), and expose the chatbot via API Gateway or Lambda.  
4. **Add persistence & monitoring** – Extend the sample’s memory layer with DynamoDB or Aurora, and enable CloudWatch logs/metrics for production observability.  
5. **Pilot & scale** – Deploy the customized agent to a staging environment, run load tests, then promote to production using standard AWS deployment practices (e.g., CDK or SAM).

**Production Readiness**  
- **Activity & community** – 155 ★, 50 forks, recent commit (2026‑05‑10), and a growing set of topics indicate strong community interest.  
- **Technical maturity** – Built on TypeScript with explicit API/SDK/CLI interfaces, the codebase follows AWS best practices and is ready for container or serverless packaging.  
- **Ecosystem fit** – Direct integration with Amazon Bedrock AgentCore and Strands Agents means you can leverage existing AWS security, IAM, and monitoring tooling out‑of‑the‑box.  
- **Risks** – License compliance, a formal security audit, and confirmation of active maintainers should be completed before a production rollout, but no major metadata or architectural concerns have been identified.  

Overall, the project is a solid, high‑readiness OSS candidate for teams looking to move from proof‑of‑concept prompt engineering to robust, orchestrated AI agents in production.

### Русский

**aws-samples/sample‑strands‑agent‑with‑agentcore** — открытый репозиторий, демонстрирующий референсную архитектуру чат‑ботов‑агентов на базе Strands Agents и Amazon Bedrock AgentCore. Он позволяет превратить разрозненные промпты и инструменты в повторяемые, управляемые рабочие процессы с поддержкой многопользовательского координации, пайплайнов инструментов и стандартизованной памяти агентов. Проект уже активно поддерживается (обновления – 2026‑05‑10, 155 звёзд, 50 форков, TypeScript), имеет ясный API/SDK/CLI и готов к пилотному внедрению в продакшн после финального аудита лицензии и безопасности.

### 中文

**项目简介**  
`aws-samples/sample-strands-agent-with-agentcore` 是一个参考架构，演示如何使用 **Strands Agents** 与 **Amazon Bedrock AgentCore** 搭建具备记忆、工具调用和多代理协作能力的 AI 聊天机器人。  

**价值**  
- 将零散的 Prompt 与工具封装为可复用、可编排的 **Agent 工作流**，实现统一的记忆管理和工具链调用。  
- 支持 **多代理协同**，可在同一会话中调度不同专长的 Agent 完成复杂任务。  
- 为企业提供标准化的 Agent 开发模板，降低从原型到生产的落地门槛。  

**典型接入方式**  
1. **API/SDK**：项目提供基于 **TypeScript** 的 SDK 示例，直接调用 Bedrock AgentCore 的 REST/SDK 接口。  
2. **CLI**：通过预置的 `sam`（Serverless Application Model）或 `cdk` 脚本，一键部署 Lambda‑based Agent 服务。  
3. **语言/元数据**：仓库中包含 OpenAPI 规范、TypeScript 类型定义以及常用的 **topic**（如 `agent‑memory`、`tool‑integration`），便于在现有代码库中快速集成。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑10 最近一次提交，仓库拥有 155 Stars、50 Forks，社区活跃。  
- **技术成熟度**：基于 Bedrock AgentCore 的托管服务，具备自动扩缩容、日志审计和安全控制，适合作为正式生产环境的核心组件。  
- **风险**：目前未发现重大元数据或许可证问题，但仍建议在正式投产前完成安全审计并确认维护者响应时效。  

总体而言，该项目已经具备 **高可用**、**易集成** 的特性，可作为企业在 AI 编排与自动化领域的首选 OSS 参考实现。

## 🧭 Practical evaluation

**Value:** aws-samples/sample-strands-agent-with-agentcore helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 155 GitHub stars
- 50 forks
- updated 2026-05-10
- primary language: TypeScript
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 43/100 |
| stars | 47/100 |
| topics | 100/100 |
| outlook | 84/100 |
| quality | 76/100 |
| recency | 100/100 |
| adoption | 46/100 |
| production | 77/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-10 · [View on GitHub](https://github.com/aws-samples/sample-strands-agent-with-agentcore) · [← Back to Orchestration](./README.md)</sub>
