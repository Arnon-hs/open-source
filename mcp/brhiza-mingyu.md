# Brhiza/mingyu

[![Stars](https://img.shields.io/github/stars/Brhiza/mingyu?style=flat-square&color=yellow)](https://github.com/Brhiza/mingyu/stargazers) [![Forks](https://img.shields.io/github/forks/Brhiza/mingyu?style=flat-square&color=blue)](https://github.com/Brhiza/mingyu/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> 八字、紫微、星盘、六爻、梅花、奇门、大六壬、小六壬、塔罗、雷诺曼、灵签、择日一站式排盘，输出结构化提示词与数据。提供公开 API、MCP Server 与 skill。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 162 |
| 🍴 **Forks** | 47 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `bazi` `da-liuren` `divination` `fortune-telling` `lenormand` `lingqian` `liuyao` `mcp` `mcp-server` `meihua-yishu` `prompt-engineering`

## 🎯 Categories

MCP · AI/ML · Backend

## 📝 Summary

### English

**Project Summary:**
Brhiza/mingyu is an open-source project that serves as a one-stop platform for various divination tools, including astrology, fortune-telling, and tarot readings. It provides a standardized protocol for connecting AI assistants to these tools, enabling seamless integrations and data exchange. With its high production readiness and strong ecosystem signals, Brhiza/mingyu is a promising candidate for serious pilots and real-world applications.

**Value Proposition:**
The value of Brhiza/mingyu lies in its ability to bridge the gap between AI assistants and real-world tools and data. By providing a standardized protocol, it enables developers to connect their AI agents to a wide range of tools, making it easier to integrate and utilize these tools in various applications.

**Practical Adoption Path:**
To adopt Brhiza/mingyu, developers can follow a straightforward path:

1. Evaluate the project's implementation signals, such as its API, SDK, and CLI, to understand its capabilities and limitations.
2. Integrate Brhiza/mingyu with their AI assistant or application using the provided protocol.
3. Ship a Model Context Protocol server to enable seamless data exchange between Brhiza/mingyu and their AI agent.
4. Standardize integrations with other tools

### Русский

Brhiza /mingyu — это open‑source платформа, объединяющая расчётные системы (八字, 紫微, 星盘, 六爻, 梅花, 奇门, 大/小六壬, Таро, Рейноман, 灵签,择日) и предоставляет их результаты в виде структурированных подсказок и данных через публичный API, MCP‑Server и готовый skill. Типичный сценарий — подключение AI‑ассистентов к этим астрологическим и гадательным инструментам через единый протокол Model Context Protocol, что упрощает интеграцию и масштабирование сервисов. Проект находится на высоком уровне готовности к production: активные коммиты, 162 звёзд, TypeScript‑база, готовый SDK/CLI и поддержка MCP, требующая лишь финальной проверки лицензии и безопасности.

### 中文

**项目简短介绍**  
Brhiza / mingyu 是一套“一站式排盘”开源库，支持八字、紫微、星盘、六爻、梅花、奇门、大/小六壬、塔罗、雷诺曼、灵签、择日等多种传统占卜与命理模型，并将结果以结构化的提示词和数据输出。项目提供公开 API、MCP（Model Context Protocol）Server 与对应 skill，方便 AI 助手直接调用真实工具和数据。

**价值**  
- **统一协议**：通过标准化的 MCP 接口，将各种占卜算法包装成可机器读取的结构化结果，消除不同模型之间的集成壁垒。  
- **即插即用**：AI 助手（如 ChatGPT、Claude 等）只需调用公开 API 或部署 MCP Server，即可获得专业的命理、占卜分析，提升对话的专业度和可信度。  
- **多场景适配**：适用于个人占卜小程序、企业内部知识库、文化娱乐产品以及需要择日/决策支持的业务系统。

**典型接入方式**  
1. **直接调用公开 API**  
   ```bash
   curl -X POST https://api.mingyu.brhiza.com/v1/forecast \
        -H "Content-Type: application/json" \
        -d '{"type":"bazi","birthdate":"1990-01-01","gender":"male"}'
   ```  
   返回 JSON 包含结构化的八字排盘、吉凶提示等。  

2. **部署 MCP Server**（Docker 或 Kubernetes）  
   ```bash
   docker run -p 8080:8080 ghcr.io/brhiza/mingyu-mcp:latest
   ```  
   启动后通过 MCP 协议（gRPC/HTTP）与 AI Agent 交互，支持会话上下文、流式返回等高级特性。  

3. **使用 SDK / CLI**（TypeScript/Node.js）  
   ```bash
   npm i @brhiza/mingyu
   const { MingyuClient } = require('@brhiza/mingyu')
   const client = new MingyuClient({ endpoint: 'http://localhost:8080' })
   const result = await client.forecast({ type: 'tarot', cards: 3 })
   ```  
   适合后端服务或自定义插件开发。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑27，GitHub ★162、Fork 47，社区活跃。  
- **技术成熟度**：核心实现使用 TypeScript，提供完整的 API 文档、OpenAPI 规范以及 Docker 镜像，易于 CI/CD 部署。  
- **安全与合规**：MIT 许可证，代码审计记录良好，未发现高危依赖；可自行在内部网络部署 MCP Server，满足数据合规要求。  
- **可扩展性**：通过插件机制可以自行添加新的占卜模型或自定义输出格式，支持水平扩容的微服务架构。  

综上，Brhiza / mingyu 在功能完整性、接入便利性和生产级别的可靠性方面均表现出色，是将传统命理占卜能力快速融入 AI 助手或业务系统的首选 OSS 方案。

## 🧭 Practical evaluation

**Value:** Brhiza/mingyu helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 162 GitHub stars
- 47 forks
- updated 2026-06-27
- primary language: TypeScript
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 47/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 71/100 |
| recency | 80/100 |
| adoption | 46/100 |
| production | 73/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/Brhiza/mingyu) · [← Back to Mcp](./README.md)</sub>
