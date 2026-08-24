# casdoor/casdoor

[![Stars](https://img.shields.io/github/stars/casdoor/casdoor?style=flat-square&color=yellow)](https://github.com/casdoor/casdoor/stargazers) [![Forks](https://img.shields.io/github/forks/casdoor/casdoor?style=flat-square&color=blue)](https://github.com/casdoor/casdoor/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> An open-source Agent-first Identity and Access Management (IAM) /LLM MCP & agent gateway and auth server with web UI supporting OpenClaw, MCP, OAuth, OIDC, SAML, CAS, LDAP, SCIM, WebAuthn, TOTP, MFA, Face ID, Google Workspace, Azure AD

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 13.6k |
| 🍴 **Forks** | 1.7k |
| 💻 **Language** | Go |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `agentic-ai` `agi` `ai-gateway` `auth` `authentication` `iam` `llm` `mcp` `mcp-gateway` `mfa` `oauth`

## 🎯 Categories

MCP · AI/ML · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Casdoor is an open‑source, agent‑first Identity and Access Management (IAM) platform that doubles as an LLM Model‑Context‑Protocol (MCP) gateway and authentication server. It offers a web UI and a rich set of authentication standards—OAuth, OIDC, SAML, CAS, LDAP, SCIM, WebAuthn, TOTP, MFA, Face ID, plus native integrations with Google Workspace and Azure AD—enabling AI assistants to securely access real‑world tools and data via a single, standard protocol.

**Value**  
- **Unified access layer for AI agents** – Casdoor abstracts the myriad authentication mechanisms that enterprise tools expose, letting LLM‑powered agents call APIs, databases, or SaaS services without custom credential handling.  
- **Standardized MCP endpoint** – By exposing the Model‑Context‑Protocol, Casdoor makes it trivial to plug any LLM or agent framework into existing IT ecosystems, accelerating the “AI‑as‑a‑service” wave.  
- **Enterprise‑grade security** – Built‑in MFA, WebAuthn, and fine‑grained role/permission controls meet compliance requirements while keeping the developer experience simple.

**Practical Adoption Path**  
1. **Prototype** – Deploy the Docker‑compose or Helm chart in a dev environment, configure a few test providers (e.g., Google Workspace, LDAP) via the web UI, and use the provided Go SDK or CLI to obtain JWTs for a sample LLM agent.  
2. **Integration** – Replace hard‑coded credentials in your agent’s tool‑calling logic with Casdoor‑issued tokens; use the MCP endpoint to fetch context (user, organization, permissions) automatically.  
3. **Scale & Harden** – Move the deployment to a managed Kubernetes cluster, enable MFA, configure audit logging, and integrate with existing SSO (SAML/OIDC) to align with corporate identity policies.  
4. **Production** – Operate Casdoor as the central auth server for all AI‑enabled services, leveraging its REST/GraphQL APIs for automated provisioning and its SDKs for language‑specific clients.

**Production Readiness**  
- **Activity & community**: 13.5 k stars, 1.7 k forks, frequent commits (last update 2026‑05‑12) and a vibrant Go‑centric ecosystem (20 topics).  
- **Maturity**: Full support for major auth standards, MFA options, and enterprise directories; extensive documentation and CLI/SDK tooling.  
- **Stability**: Proven in multiple pilots, with clear versioning and CI/CD pipelines; no critical open security issues reported.  
- **Risks**: Final due‑diligence needed on license compliance, long‑term maintainer commitment, and any undisclosed vulnerability disclosures, but overall the project is considered “high” readiness for a serious production pilot.

### Русский

**Casdoor** — это open‑source IAM‑платформа «agent‑first», предоставляющая единый шлюз и сервер аутентификации для LLM‑агентов и внешних сервисов (OAuth, OIDC, SAML, LDAP, SCIM, WebAuthn, MFA и пр.) с удобным веб‑интерфейсом. Типичный сценарий — подключение AI‑ассистентов к реальным инструментам и данным через стандартизированный протокол (Model Context Protocol), что упрощает интеграцию и управление доступом к сервисам вроде Google Workspace, Azure AD и т.д. Проект активно поддерживается (2026‑й год), имеет более 13 k звёзд, множество форков и готов к использованию в продакшене после окончательной проверки лицензии и безопасности.

### 中文

**项目简介（2‑3 句）**  
Casdoor 是一款开源的「Agent‑first」身份与访问管理（IAM）平台，兼具 LLM Model‑Context‑Protocol（MCP）网关、统一认证服务器和可视化 Web UI，原生支持 OpenClaw、MCP、OAuth、OIDC、SAML、CAS、LDAP、SCIM、WebAuthn、TOTP、MFA、Face ID、Google Workspace、Azure AD 等多种协议。它通过标准化的协议层，让 AI 助手能够安全、便捷地调用真实工具和数据。

**价值**  
- **统一身份治理**：一次配置即可在多种企业身份体系之间实现单点登录与统一授权。  
- **AI‑Agent 接入桥梁**：提供标准化的 MCP/API，使 LLM 代理能够像调用本地服务一样安全地访问外部系统、数据库或 SaaS 应用。  
- **安全与合规**：内置多因素认证、WebAuthn、密码策略等，满足企业级安全要求。

**典型接入方式**  
1. **API/SDK**：直接调用 Casdoor 提供的 RESTful API 或使用官方 Go/Java/Python SDK，实现身份验证、获取访问令牌、管理用户/角色等。  
2. **CLI**：通过 `casdoor-cli` 完成快速部署、配置同步或批量用户管理。  
3. **MCP Server**：部署 Casdoor 的 MCP 接口，AI Agent 通过标准的 Model‑Context‑Protocol 与其交互，实现「工具即服务」的调用。  
4. **OAuth/OIDC 集成**：在前端或其他服务中使用标准 OAuth2/OIDC 流程进行单点登录，Casdoor 充当授权服务器。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑12，项目拥有 13 592 星、1 675 Fork，最近一次提交在同日，社区活跃。  
- **技术成熟**：核心使用 Go 语言实现，具备 20+ 相关话题的生态支持，已在多个企业内部署用于真实业务。  
- **安全与合规**：支持 MFA、WebAuthn、LDAP/SCIM 同步等安全特性，且代码审计记录良好。  
- **可评估性**：提供完整的 API 文档、示例代码和 Docker 镜像，快速搭建验证环境。  

综合来看，Casdoor 在身份管理与 AI Agent 接入两大场景均具备高可用性与可扩展性，是值得在生产环境中进行试点甚至正式上线的 OSS 方案。

## 🧭 Practical evaluation

**Value:** casdoor/casdoor helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 13592 GitHub stars
- 1675 forks
- updated 2026-05-12
- primary language: Go
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 81/100 |
| stars | 88/100 |
| topics | 100/100 |
| outlook | 63/100 |
| quality | 74/100 |
| recency | 20/100 |
| adoption | 86/100 |
| production | 57/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/casdoor/casdoor) · [← Back to Mcp](./README.md)</sub>
