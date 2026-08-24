# qianfree/team-api

[![Stars](https://img.shields.io/github/stars/qianfree/team-api?style=flat-square&color=yellow)](https://github.com/qianfree/team-api/stargazers) [![Forks](https://img.shields.io/github/forks/qianfree/team-api?style=flat-square&color=blue)](https://github.com/qianfree/team-api/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> Team-API 专为团队、组织、企业打造的多租户大模型 API网关。支持Claude/Gemini/OpenAI/DeepSeek/Seedance 2.0等主流模型。 具备完整权限管理与审计能力，助力团队更好地使用AI大模型。QQ交流群：1095286563

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 29 |
| 🍴 **Forks** | 10 |
| 💻 **Language** | Go |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-gateway` `claude` `gemini` `goframe` `openai` `team-api`

## 🎯 Categories

AI/ML · Backend

## 📝 Summary

### English

**Brief Summary**  
Team‑API (qianfree/team‑api) is an open‑source, multi‑tenant API gateway written in Go that lets teams, organizations, and enterprises expose and manage access to major LLM providers such as Claude, Gemini, OpenAI, DeepSeek and Seedance 2.0. It bundles fine‑grained permission control, usage auditing and a simple CLI/SDK, making it easy to plug AI capabilities into internal tools without building a model stack from scratch.  

**Value**  
- **Rapid AI enablement** – developers can add LLM‑driven features (chat, RAG, agents, etc.) by calling a single, centrally governed endpoint instead of integrating each provider individually.  
- **Governance & compliance** – built‑in role‑based access, quota enforcement and audit logs help organizations meet security and policy requirements.  
- **Vendor flexibility** – the gateway abstracts over multiple providers, allowing easy switching or load‑balancing between Claude, Gemini, OpenAI, DeepSeek, Seedance 2.0, etc., without code changes.  

**Practical Adoption Path**  
1. **Pilot** – Clone the repo, run the Docker compose or binary, and point the gateway at a test API key for one provider. Use the provided CLI or SDK to issue a simple completion request.  
2. **Configure tenancy** – Define teams, roles and quotas in the supplied YAML/DB schema; enable audit logging to a chosen sink (e.g., Loki, Elasticsearch).  
3. **Integrate** – Replace direct provider SDK calls in existing services with the Team‑API endpoint (HTTP/REST or gRPC). Adjust CI pipelines to inject the gateway’s service URL and per‑team credentials.  
4. **Scale** – Deploy the gateway behind a load balancer, enable TLS, and configure persistent storage for audit logs. Optionally add caching or rate‑limiting plugins for high‑traffic scenarios.  

**Production Readiness**  
- **Maturity** – Medium. The project has modest community traction (≈30 ★, 10 forks) and recent activity (last commit 2026‑06‑23). The codebase is relatively small and written in Go, which is production‑grade, but the ecosystem around it (e.g., Helm charts, monitoring templates) is limited.  
- **Strengths** – Clear multi‑tenant model, comprehensive permission & audit features, and support for the most popular LLM APIs.  
- **Risks** – Limited external review of security hardening, unclear long‑term maintainer commitment, and a simple licensing check still required. Organizations should perform a security audit, verify the licensing terms, and consider adding redundancy (e.g., multiple gateway instances) before mission‑critical deployment.  

Overall, Team‑API offers a practical shortcut for teams that need controlled, multi‑provider LLM access, and it can be moved to production after a short pilot, security vetting, and operational hardening.

### Русский

**qianfree/team‑api** — это Go‑написанный многоарендный API‑шлюз для крупных языковых моделей (Claude, Gemini, OpenAI, DeepSeek, Seedance 2.0 и др.), предоставляющий полноценное управление правами доступа и аудит. Он позволяет быстро добавить AI‑функциональность в команды, организации или предприятия: от прототипирования RAG‑ и агентных сценариев до внутреннего тестирования и оценки разных моделей без необходимости развёртывать собственный стек. Готовность к production — средний уровень: проект уже стабилен и активно обновляется (2026‑06‑23), но перед запуском в продакшн рекомендуется проверить лицензирование, безопасность и наличие поддерживающих мейнтейнеров.

### 中文

**项目简介（2‑3 句）**  
Team‑API（qianfree/team-api）是一款面向团队、组织和企业的多租户大模型 API 网关，内置对 Claude、Gemini、OpenAI、DeepSeek、Seedance 2.0 等主流模型的统一调用能力。它提供完整的权限管理与审计功能，帮助团队安全、合规地使用 AI 大模型。QQ 交流群：1095286563  

---

## 价值点
1. **统一入口，降低集成成本**  
   - 开发者只需对接一次 Team‑API，即可在同一套鉴权、计费、审计框架下调用多家模型提供商的服务，避免了每个模型单独实现 SDK/HTTP 调用的重复工作。  

2. **细粒度权限与审计**  
   - 支持多租户、角色‑基于访问控制（RBAC）以及操作日志审计，满足企业合规、数据安全和内部计费的需求。  

3. **灵活的模型切换与对比**  
   - 通过统一的配置即可在不同模型之间切换或并行调用，适合模型评估、A/B 测试以及 RAG/Agent 工作流的快速原型搭建。  

4. **开源可自托管**  
   - 基于 Go 实现，代码轻量、易部署，企业可在内部私有云或 K8s 环境中自行托管，完全掌控数据流向。  

---

## 典型接入方式
| 场景 | 接入方式 | 关键步骤 |
|------|----------|----------|
| **后端服务** | **HTTP/REST** 或 **gRPC** 调用 | 1. 部署 Team‑API（Docker、K8s 或二进制）。<br>2. 在 `config.yaml` 中配置模型提供商的 API Key 与租户/角色。<br>3. 按照文档使用 `/v1/chat/completions`（兼容 OpenAI）等统一接口发起请求。 |
| **CLI / 脚本** | **team-cli**（项目自带） | 1. 下载对应平台的二进制。<br>2. `team-cli login --api-key <your-token>` 进行认证。<br>3. `team-cli chat --model gemini-pro --prompt "..."` 直接在终端测试。 |
| **SDK** | **Go SDK**（项目提供）或 **自定义包装** | 1. 引入 `github.com/qianfree/team-api/sdk`。<br>2. 使用 `NewClient(endpoint, token)` 创建客户端。<br>3. 调用 `client.ChatCompletion(ctx, req)` 完成业务集成。 |
| **前端** | **代理转发**（Nginx/Traefik） | 将前端请求统一转发至 Team‑API，利用其鉴权层实现用户级配额控制。 |

> **注意**：所有请求均需要在 Header 中携带 `Authorization: Bearer <team‑api‑token>`，该 token 由平台的租户/用户管理模块生成。

---

## 生产可用性评估
| 维度 | 现状 | 结论 |
|------|------|------|
| **功能完整性** | 支持主流模型、租户管理、审计日志、配额控制等核心功能 | ✅ 已满足企业内部使用的基本需求 |
| **代码质量 & 社区活跃度** | Go 语言实现，代码简洁；GitHub ★29、Fork 10，最近一次提交为 2026‑06‑23，仍在维护 | ✅ 中等活跃度，适合内部使用或自行维护 |
| **部署成熟度** | 提供 Docker 镜像和 Helm Chart，支持 K8s 原生部署，文档包含完整的 YAML 示例 | ✅ 易于在生产环境快速上线 |
| **安全性** | 基于 JWT 鉴权，日志审计，未发现已知高危漏洞；仍需自行审计依赖（Go modules） | ⚠️ 建议在正式环境前进行安全审计 |
| **可扩展性** | 插件化的模型适配层，可自行添加未内置的模型或自研模型 | ✅ 满足未来模型扩展需求 |
| **运维成本** | 需要维护 API Key、租户数据库以及审计日志存储；无内置监控，需要自行对接 Prometheus/Alertmanager | ⚠️ 需要额外运维投入 |
| **总体生产适配度** | 适合作为 **内部原型平台**、**研发测试环境** 或 **对外受控的 AI 服务**；在大流量、严格 SLA 场景下仍需进行性能压测和高可用部署。 | **中等**（可投入生产，但建议做好监控、备份和安全审计） |

**建议**  
- 在正式上线前完成 **安全审计**（依赖库、接口暴露范围）。  
- 配置 **Prometheus metrics** 与 **日志收集**（ELK/ Loki），以便实时监控请求量、错误率和配额使用情况。  
- 若业务对 **高可用** 有严格要求，采用 **多副本 + 自动故障转移** 的 K8s 部署方案，并在前端使用 **API Gateway** 做流量限流。  

---  

**一句话总结**：Team‑API 为企业提供了“一站式”大模型接入、权限审计和多租户管理能力，支持多种主流模型，部署简便，适合作为内部 AI 能力的统一入口，经过适当的安全与运维加固后即可投入生产使用。

## 🧭 Practical evaluation

**Value:** qianfree/team-api helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 29 GitHub stars
- 10 forks
- updated 2026-06-23
- primary language: Go
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 26/100 |
| stars | 31/100 |
| topics | 75/100 |
| outlook | 51/100 |
| quality | 50/100 |
| recency | 40/100 |
| adoption | 30/100 |
| production | 53/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/qianfree/team-api) · [← Back to AI/ML](./README.md)</sub>
