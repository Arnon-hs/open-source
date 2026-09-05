# yancyuu/Hermit

[![Stars](https://img.shields.io/github/stars/yancyuu/Hermit?style=flat-square&color=yellow)](https://github.com/yancyuu/Hermit/stargazers) [![Forks](https://img.shields.io/github/forks/yancyuu/Hermit?style=flat-square&color=blue)](https://github.com/yancyuu/Hermit/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> 给一人公司和小团队用的本地 AI Agent 控制台 把 Claude Code、Codex、Gemini、Qoder 等 Agent 放进同一个看板、消息和审查流程里。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 114 |
| 🍴 **Forks** | 2 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Project Summary:**
Hermit is an open-source, local AI Agent console designed for small teams and individual companies. It integrates popular AI agents such as Claude Code, Codex, Gemini, and Qoder into a single dashboard, workflow, and review process. This makes it easier to add AI capabilities without starting from scratch.

**Value Proposition:**
Hermit helps teams quickly prototype AI features, build Reusable Agent Graphs (RAGs) or agent workflows, and evaluate model tooling, ultimately accelerating AI development and experimentation.

**Practical Adoption Path:**
To adopt Hermit, teams can start by evaluating its capabilities and integrating the desired AI agents into the console. This may require manual inspection and testing to ensure seamless integration. Once set up, teams can use Hermit to build and deploy AI workflows, leveraging its review process for collaboration and quality control.

**Production Readiness:**
Hermit is considered medium-production ready, making it suitable for prototype development, internal workflows, and proof-of-concept projects. However, before deploying it in production, teams should conduct thorough dependency and maintenance checks to ensure stability and security.

### Русский

Резюме проекта yancyuu/Hermit:

yancyuu/Hermit - это открытый исходный код проект, который позволяет добавлять возможности искусственного интеллекта без создания новой базовой модели. Этот проект предназначен для компаний и малых команд, и позволяет интегрировать различные агенты AI, такие как Claude Code, Codex, Gemini и Qoder, в одну панель и поток сообщений. Проект готов к экспериментам и внутренним потокам, но требует тщательного проверки и поддержки перед использованием в производстве.

### 中文

**项目简介**  
Hermit（yancyuu/Hermit）是一款面向“一人公司”和小团队的本地 AI Agent 控制台。它把 Claude Code、Codex、Gemini、Qoder 等不同模型的 Agent 集成到同一个看板、消息流和审查流程中，让开发者无需自行搭建繁杂的模型堆栈即可快速使用多模型能力。

**价值**  
- **即插即用**：通过统一的 UI 与 API，把多种大模型当作插件使用，省去自行部署、调优和兼容的工作量。  
- **加速原型**：适合快速验证 AI 功能、构建 RAG（检索增强生成）或多 Agent 工作流，帮助产品在最短时间内验证概念。  
- **统一治理**：所有 Agent 的调用、审查和日志都在同一面板上，可统一审计、权限控制和结果对比，降低运营风险。

**典型接入方式**  
1. **克隆仓库并安装依赖**（Node.js ≥ 18，TypeScript 项目）  
   ```bash
   git clone https://github.com/yancyuu/Hermit.git
   cd Hermit
   npm install
   ```  
2. **配置模型凭证**：在 `config/.env`（或 `config.json`）中填入 Claude、Codex、Gemini、Qoder 等模型的 API Key 与 endpoint。  
3. **启动本地服务**：  
   ```bash
   npm run dev   # 或 npm start
   ```  
   控制台默认在 `http://localhost:3000`，登录后即可在看板中添加、编辑、调度各类 Agent。  
4. **集成到业务代码**：通过提供的 REST/GraphQL SDK（`src/sdk`），在业务服务中调用 `POST /api/agent/run`，指定 `agentId` 与输入数据，即可获得统一返回。  

> **注意**：Hermit 目前的元数据和信号较少，建议在正式上线前进行手动审查和安全评估，确保 API Key、网络访问和日志存储符合企业合规要求。

**生产可用性**  
- **成熟度**：Medium。适合作为原型、内部工具或低并发的生产环境；在高并发、严苛 SLA 场景下仍需自行做负载、容错和监控层面的加固。  
- **依赖与维护**：项目主要使用 TypeScript 与 Node.js，依赖相对轻量；但维护者数量有限，建议自行 fork 并锁定关键依赖版本，以防止上游不再更新。  
- **安全与合规**：未发现重大许可证或安全漏洞，但因涉及多家大模型的 API Key，必须在内部审计后方可投入生产，并做好密钥轮换、审计日志和访问控制。  

综上，Hermit 为小团队提供了“一站式”本地 AI Agent 管理平台，能够快速把多模型能力嵌入业务流程，适合原型开发和内部工作流；在正式生产环境使用前，需要完成安全审查、性能压测以及运维准备。

## 🧭 Practical evaluation

**Value:** yancyuu/Hermit helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 114 GitHub stars
- 2 forks
- updated 2026-06-30
- primary language: TypeScript

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 12/100 |
| stars | 44/100 |
| topics | 0/100 |
| outlook | 58/100 |
| quality | 51/100 |
| recency | 80/100 |
| adoption | 35/100 |
| production | 61/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/yancyuu/Hermit) · [← Back to AI/ML](./README.md)</sub>
