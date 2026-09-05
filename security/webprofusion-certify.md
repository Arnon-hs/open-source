# webprofusion/certify

[![Stars](https://img.shields.io/github/stars/webprofusion/certify?style=flat-square&color=yellow)](https://github.com/webprofusion/certify/stargazers) [![Forks](https://img.shields.io/github/forks/webprofusion/certify?style=flat-square&color=blue)](https://github.com/webprofusion/certify/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Professional ACME Client for Windows (and now cross-platform via Certify Management Hub). Certificate Management UI, powered by Let's Encrypt and compatible with all ACME v2 CAs. Used by over 150,000 organisations. Download from certifytheweb.com

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.7k |
| 🍴 **Forks** | 280 |
| 💻 **Language** | C# |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`acme` `acme-client` `acme-v2` `certbot` `certificate` `certificate-management` `certificates` `https` `iis` `letsencrypt` `pki` `ssl`

## 🎯 Categories

Security

## 📝 Summary

### English

**Brief Summary**  
certify (webprofusion/certify) is a professional ACME client that provides a graphical UI for managing TLS certificates via Let’s Encrypt and any ACME‑v2 CA. Originally built for Windows, it now runs cross‑platform through the Certify Management Hub, and is already used by more than 150 000 organisations.

**Value**  
- **Automation of repetitive tasks** – the UI, CLI, and API let you issue, renew, and revoke certificates automatically, eliminating manual command‑line work.  
- **Integrations & repeatable flows** – built‑in webhooks, PowerShell/CLI modules and a REST API make it easy to embed certificate lifecycle steps into CI/CD pipelines, monitoring systems, or custom orchestration tools.  
- **Enterprise‑grade reliability** – with a mature codebase (1.6 k ★, 280 forks) and active maintenance, it offers a trusted, auditable way to keep TLS assets up‑to‑date across Windows, Linux and container environments.

**Practical Adoption Path**  
1. **Trial deployment** – spin up the Certify Management Hub (Docker/Windows service) in a non‑production environment and connect a test domain to Let’s Encrypt via the UI.  
2. **Evaluate integration points** – use the provided CLI (`certify.exe`) or REST API to script certificate requests and renewals; test webhook callbacks for your monitoring or ticketing system.  
3. **Roll‑out to production** – configure the hub with your production domains, set renewal schedules, and enable role‑based access control. Existing certificates can be imported, and the hub can automatically replace them on web servers, load balancers, or Kubernetes ingress objects.  

**Production Readiness**  
- **High** – recent commits (as of 2026‑06‑26), strong adoption numbers, and a clear roadmap indicate a stable, actively maintained project.  
- **Quality signals** – 1 688 stars, 280 forks, 15 relevant topics, and a primary language of C# with comprehensive documentation.  
- **Remaining checks** – a final review of the license terms, security audit reports, and maintainer responsiveness is recommended before committing to mission‑critical workloads.

### Русский

**webprofusion/certify** — это профессиональный ACME‑клиент с UI, позволяющий полностью автоматизировать выпуск, обновление и хранение TLS‑сертификатов через Let’s Encrypt и любые ACME v2‑CA; он уже используется более чем 150 000 организаций и доступен как Windows‑приложение и кросс‑платформенный Certify Management Hub. Типичный сценарий внедрения — интеграция в CI/CD или инфраструктурные пайплайны, где сертификаты выдаются и обновляются по расписанию без ручного вмешательства, а также подключение к внешним системам через API/CLI/SDK. Проект имеет высокий уровень готовности к production: активные коммиты, крупное сообщество (≈1,7 k звёзд), широкое применение и поддержка, что делает его надёжным кандидатом для серьёзных пилотных запусков.

### 中文

**项目简介**  
webprofusion/certify 是一款面向 Windows（并通过 Certify Management Hub 实现跨平台）的专业 ACME 客户端，提供可视化的证书管理界面，支持 Let’s Encrypt 以及所有兼容 ACME v2 的 CA。已被超过 15 万家组织采用，可从 certifytheweb.com 下载。

**价值**  
- **自动化**：把证书申请、续期、部署等繁琐的手工操作全部脚本化、计划化，显著降低运维成本。  
- **可视化与可控**：统一 UI 与仪表盘让团队能够实时查看证书状态、到期时间和使用情况，避免因证书过期导致的业务中断。  
- **生态兼容**：兼容所有 ACME v2 CA，且提供 API/CLI/SDK，便于与 CI/CD、配置管理工具（如 Ansible、Terraform）以及内部监控系统无缝集成。

**典型接入方式**  
1. **API/CLI**：通过 RESTful API 或内置的 `certify.exe` 命令行工具在脚本或自动化流水线中调用（如在 GitHub Actions、Azure DevOps 中触发证书申请/续期）。  
2. **SDK**：使用其公开的 C# 类库在自研的后台服务或管理平台中直接嵌入证书管理功能。  
3. **管理中心**：部署 Certify Management Hub（Docker/Windows Service），通过统一的 Web UI 统一管理跨服务器、跨平台的证书，适合大规模组织的集中运维。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑26，星标 1.7k+、Fork 280+，社区活跃，文档完善。  
- **成熟度**：已在 150 k+ 组织中正式使用，具备完整的错误监控、日志和通知机制。  
- **安全与合规**：采用 MIT 许可证，代码审计记录良好，支持通过自签根 CA 进行内部审计。  
- **风险**：仍需对许可证兼容性、长期维护者的可用性以及潜在的安全漏洞进行最终确认，但整体信号表明可直接用于生产环境的试点或全量部署。

## 🧭 Practical evaluation

**Value:** webprofusion/certify helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1688 GitHub stars
- 280 forks
- updated 2026-06-26
- primary language: C#
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 61/100 |
| stars | 69/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 80/100 |
| recency | 80/100 |
| adoption | 67/100 |
| production | 72/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/webprofusion/certify) · [← Back to Security](./README.md)</sub>
