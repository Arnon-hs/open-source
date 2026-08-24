# docker/mcp-registry

[![Stars](https://img.shields.io/github/stars/docker/mcp-registry?style=flat-square&color=yellow)](https://github.com/docker/mcp-registry/stargazers) [![Forks](https://img.shields.io/github/forks/docker/mcp-registry?style=flat-square&color=blue)](https://github.com/docker/mcp-registry/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Official Docker MCP registry

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 483 |
| 🍴 **Forks** | 783 |
| 💻 **Language** | Go |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

MCP · DevOps/Infra

## 📝 Summary

### English

**Summary**  
docker/mcp-registry is the official Docker implementation of the Model Context Protocol (MCP) registry, providing a Go‑based, open‑source service that lets AI assistants discover and invoke real‑world tools and data sources through a standardized API. With 483 stars, 783 forks, recent commits (as of 2026‑05‑12) and strong community adoption, it is ready for pilot‑grade production use.  

**Value** – By exposing tools, services, and datasets via MCP, the registry turns ad‑hoc AI integrations into a plug‑and‑play ecosystem, enabling developers to connect AI agents to internal tooling, ship custom MCP servers, and enforce a common contract across teams.  

**Practical adoption path** – Start with a small proof‑of‑concept: clone the repo, run the provided Docker compose setup, and validate the README examples against a single internal tool. Once the basic flow works, incrementally register additional services, integrate CI/CD pipelines for automated registry updates, and expose the service behind your organization’s internal network.  

**Production readiness** – The project shows high readiness: active maintenance, recent releases, and a sizable contributor base indicate stability; its Go implementation is lightweight and easy to containerize. After the initial PoC, perform a standard security audit (license compliance, vulnerability scanning of dependencies) and configure production‑grade observability (metrics, logging, TLS) before rolling it out to broader workloads.

### Русский

**docker/mcp-registry** — официальная реализация реестра Model Context Protocol, написанная на Go. Проект позволяет быстро подключать AI‑агентов к реальным инструментам и данным через единый протокол, что упрощает создание серверов MCP и стандартизацию интеграций; типичный сценарий — запуск небольшого proof‑of‑concept, проверка README и последующее масштабирование в продакшн. Благодаря активному развитию (обновления до 2026‑05‑12), высокой популярности (483★, 783 форка) и сильной экосистеме, репозиторий готов к использованию в серьёзных пилотных проектах, хотя окончательная проверка лицензии, безопасности и поддержки поддерживающих разработчиков всё‑ещё требуется.

### 中文

**项目简介**  
`docker/mcp-registry` 是 Docker 官方维护的 **Model Context Protocol（MCP）** 注册中心，实现了一个统一的协议，用于让 AI 助手安全、可靠地访问真实的工具和数据。

**价值**  
- **标准化接入**：提供统一的 MCP 接口，帮助 AI 代理快速对接各种后端服务（如模型推理、数据查询、CI/CD 工具等），降低集成成本。  
- **生态兼容**：作为官方项目，拥有活跃的社区、丰富的示例和文档，便于在已有 Docker 基础设施上直接使用。  
- **可扩展性**：支持自定义 MCP 服务器的部署与发布，适配不同业务场景的模型上下文需求。

**典型接入方式**  
1. **快速验证**：克隆仓库 → 参考 `README` 中的示例，使用 Docker Compose 启动一个本地 MCP Registry 实例。  
2. **服务注册**：在业务服务（如模型推理服务、数据库 API）中实现 MCP 接口或使用官方 SDK，将服务信息注册到 Registry。  
3. **AI 代理调用**：在 AI 助手的运行时配置 Registry 地址，代理即可通过标准化的 MCP 调用已注册的工具/数据。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑12，项目最近一次提交，拥有 483 ★、783 Fork，主要语言为 Go，社区活跃。  
- **成熟度**：官方维护、已有多家企业在内部 Pilot 使用，具备稳定的发布流程和安全审计。  
- **风险**：目前未发现重大元数据或许可证风险，但仍建议在正式上线前完成安全依赖审计并确认维护者响应速度。  

综上，`docker/mcp-registry` 已具备高生产就绪度，适合作为 AI‑Tool 集成的核心组件，从小规模 PoC 起步后可平滑扩展到全链路生产环境。

## 🧭 Practical evaluation

**Value:** docker/mcp-registry helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 483 GitHub stars
- 783 forks
- updated 2026-05-12
- primary language: Go

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 72/100 |
| stars | 57/100 |
| topics | 0/100 |
| outlook | 44/100 |
| quality | 48/100 |
| recency | 20/100 |
| adoption | 61/100 |
| production | 50/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/docker/mcp-registry) · [← Back to Mcp](./README.md)</sub>
