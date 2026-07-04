# tradesdontlie/tradingview-mcp

[![Stars](https://img.shields.io/github/stars/tradesdontlie/tradingview-mcp?style=flat-square&color=yellow)](https://github.com/tradesdontlie/tradingview-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/tradesdontlie/tradingview-mcp?style=flat-square&color=blue)](https://github.com/tradesdontlie/tradingview-mcp/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-75%2F100-brightgreen?style=flat-square)](#)

> AI-assisted TradingView chart analysis — connect Claude Code to your TradingView Desktop for personal workflow automation

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4.2k |
| 🍴 **Forks** | 2k |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 75/100 |
| 🗓️ **Last push** | 2026-07-04 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Trading · MCP · Automation · AI/ML

## 📝 Summary

### English

Here's a brief summary of the project:

**Project Summary:** tradesdontlie/tradingview-mcp is an open-source project that enables AI-assisted TradingView chart analysis by connecting Claude Code to the TradingView Desktop, allowing for personal workflow automation. This project helps researchers and traders automate market workflows, making it ideal for backtesting strategies, monitoring market trends, and optimizing trading systems. With a moderate level of production readiness, this project is suitable for prototyping or internal workflows but requires further evaluation and maintenance checks before production.

**Value:** The project offers significant value to traders and researchers by automating market workflows, allowing for more efficient and accurate analysis of trading systems and strategies.

**Practical Adoption Path:** To adopt this project, users can start by evaluating its feasibility through a small proof of concept and reviewing the README documentation. Once familiar with the project's capabilities and limitations, users can integrate it into their existing workflows, starting with small-scale applications and gradually scaling up to more complex use cases.

**Production Readiness:** The project has a moderate level of production readiness, scoring 75/100. While it is useful for prototypes or internal workflows, it requires further evaluation and maintenance checks before it can be deployed in production environments. This includes reviewing the license, security posture, and ensuring that

### Русский

Резюме проекта tradesdontlie/tradingview-mcp:

Этот проект предлагает интеграцию TradingView с AI-ассистентом Claude Code для автоматизации рабочих процессов трейдинга. Он помогает исследователям и трейдерам оптимизировать свои workflows, анализируя рынки и тестировая стратегии. Проект имеет средний уровень готовности к production, что делает его подходящим для прототипирования или внутренних рабочих процессов.

### 中文

**项目简介（2‑3 句）**  
tradesdontlie/tradingview-mcp 是一款 AI 辅助的 TradingView 桌面插件，能够将 Claude Code 与本地 TradingView 客户端相连，实现图表分析自动化和个人化工作流。它帮助用户在研究交易系统、回测策略和实时监控市场时，借助大模型快速生成、验证和执行分析脚本。

---

## 价值点

| 维度 | 说明 |
|------|------|
| **核心价值** | 将 Claude（Anthropic）的大语言模型能力直接嵌入 TradingView，自动化图表标注、指标生成、策略回测等繁琐步骤，显著提升研究效率。 |
| **业务场景** | - **交易系统研发**：快速生成技术指标代码、验证逻辑。<br>- **策略回测**：一键把模型输出的策略转化为 Pine Script 并在 TradingView 回测。<br>- **市场监控**：自动化监测特定形态或信号，实时推送提醒。 |
| **竞争优势** | 与传统手动编写 Pine Script 相比，省去大量重复劳动；比纯粹的 AI 文本生成更贴合 TradingView 环境，降低实现门槛。 |

---

## 典型接入方式

1. **环境准备**  
   - 确保本地已安装最新的 TradingView Desktop 客户端。  
   - 在项目根目录执行 `npm install` 安装依赖（主要是 JavaScript/Node 环境）。  

2. **Claude API 配置**  
   - 在 `.env` 中填入 `ANTHROPIC_API_KEY`（或对应的 Claude 访问凭证）。  
   - 可选：配置 `TRADINGVIEW_MCP_PORT` 以自定义本地服务端口。  

3. **启动服务**  
   ```bash
   npm run start   # 启动本地 MCP 服务器
   ```
   服务器会监听 TradingView Desktop 的插件接口，接收图表请求并返回 Claude 生成的代码或分析结果。

4. **在 TradingView Desktop 中加载插件**  
   - 打开 TradingView → “插件” → “本地插件” → 选择 `tradingview-mcp` 的入口文件（通常是 `manifest.json`）。  
   - 完成后即可在图表右键菜单或自定义按钮中看到 “AI 分析” 等选项。

5. **验证与迭代（PoC）**  
   - 先在测试账号或非生产图表上运行几次 AI 生成的 Pine Script，检查语法和逻辑是否符合预期。  
   - 根据实际需求微调 `.env` 中的提示模板或模型参数（如 `max_tokens`、`temperature`）。

---

## 生产可用性评估

| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | **中等** | 项目已有 4165 星、1997 Fork，活跃度高（最近更新于 2026‑07‑04），但仍主要定位原型/内部工具。 |
| **依赖风险** | 中等 | 依赖 Claude API（外部付费服务）以及 TradingView Desktop 的本地插件接口，需监控 API 费用和版本兼容性。 |
| **安全合规** | 需要进一步审查 | 当前未发现显著的元数据风险，仍需检查许可证（MIT / Apache 等）以及第三方库的安全报告。 |
| **运维成本** | 低‑中 | 只需维持 Node 环境和 API 秘钥，部署在内部服务器或容器即可。 |
| **推荐使用场景** | - 原型验证<br>- 内部研究团队的自动化工作流<br>- 高频交易前的策略快速迭代 | 对外部客户或高并发生产环境建议先进行 **小规模 PoC**，并在通过安全、费用和 SLA 评估后再正式上线。 |

**结论**：tradesdontlie/tradingview-mcp 适合作为 **原型/内部自动化** 的加速器，能够快速把 AI 生成的交易逻辑落地到 TradingView。若业务对可靠性、成本和合规要求较高，建议在小范围 PoC 验证后，再进行依赖审计和容错设计后方可投入生产。

## 🧭 Practical evaluation

**Value:** tradesdontlie/tradingview-mcp helps research and automate market workflows.

**Best use cases**

- research trading systems
- backtest strategies
- monitor market workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 4165 GitHub stars
- 1997 forks
- updated 2026-07-04
- primary language: JavaScript

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 83/100 |
| stars | 77/100 |
| topics | 0/100 |
| outlook | 83/100 |
| quality | 75/100 |
| recency | 100/100 |
| adoption | 79/100 |
| production | 75/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-04 · [View on GitHub](https://github.com/tradesdontlie/tradingview-mcp) · [← Back to Trading](./README.md)</sub>
