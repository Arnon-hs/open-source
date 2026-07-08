# zaproxy/zaproxy

[![Stars](https://img.shields.io/github/stars/zaproxy/zaproxy?style=flat-square&color=yellow)](https://github.com/zaproxy/zaproxy/stargazers) [![Forks](https://img.shields.io/github/forks/zaproxy/zaproxy?style=flat-square&color=blue)](https://github.com/zaproxy/zaproxy/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> The ZAP by Checkmarx Core project

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 15.3k |
| 🍴 **Forks** | 2.6k |
| 💻 **Language** | Java |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-06-23 |
| 🔍 **Source** | github |

## 🏷️ Topics

`appsec` `dast` `hacktoberfest` `opensource` `security` `security-scanner` `zap` `zap-development` `zaproxy`

## 🎯 Categories

Security

## 📝 Summary

### English

**Brief Summary**  
ZAP (Zed Attack Proxy) is an open‑source security testing platform that helps teams discover vulnerabilities and privacy flaws early in the development lifecycle. With a large community, active maintenance, and strong Java‑based tooling, it is ready for serious pilot projects and can be integrated incrementally into CI/CD pipelines.

**Value**  
ZAP automates dynamic security testing, providing passive and active scans, authentication handling, and reporting that let developers and security teams catch risks before code reaches production. By surfacing issues early, it reduces remediation costs, improves compliance, and strengthens overall product security posture.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the Docker image or the bundled desktop, and execute a basic scan against a non‑critical test environment.  
2. **CI Integration** – Add the ZAP Docker container or the Maven/Gradle plugin to your build pipeline, configure a small set of baseline scans, and generate SARIF or JUnit reports for automated review.  
3. **Auth & Policy Tuning** – Extend the setup with authentication scripts (e.g., JWT, OAuth) and custom scan policies to match your application’s threat model.  
4. **Full Rollout** – Scale the scans to staging/production environments, integrate results with your ticketing or security dashboards, and codify the process in documentation and README for team onboarding.

**Production Readiness**  
ZAP scores high on production readiness: it has over 15 k stars, thousands of forks, frequent releases (latest update 2026‑06‑23), and a mature Java codebase. The ecosystem includes Docker images, CI plugins, and extensive documentation, making it suitable for a serious pilot. The main risk is the lack of a turnkey integration guide; teams should allocate time to validate configuration, authentication handling, and resource requirements before committing to a full‑scale deployment.

### Русский

ZAP (zaproxy/zaproxy) — мощный open‑source сканер безопасности, позволяющий выявлять уязвимости и проблемы конфиденциальности уже на ранних этапах разработки, что ускоряет аудит рисков и упрощает добавление механизмов аутентификации и контроля доступа. Для внедрения рекомендуется начать с небольшого proof‑of‑concept, проверив README и базовую конфигурацию, а затем масштабировать интеграцию в CI/CD. Проект обладает высокой готовностью к production: активное развитие, более 15 тыс. звёзд, регулярные обновления и широкое принятие в сообществе.

### 中文

**项目简介（2‑3 句）**  
ZAP（Zed Attack Proxy）是 Checkmarx 维护的开源 Web 安全测试平台，能够在开发和 CI/CD 流程中自动发现安全与隐私漏洞。凭借活跃的社区、丰富的插件生态和强大的主动扫描能力，ZAP 已成为业界常用的渗透测试与安全审计工具。

**价值**  
- **提前发现风险**：在代码提交、构建或部署阶段即捕获安全与隐私缺陷，降低后期修复成本。  
- **可扩展的安全检查**：提供主动扫描、被动代理、API 测试、身份认证模拟等多种检测手段，满足不同安全合规需求。  
- **社区与生态支持**：超过 15 k ⭐、2 k+ Fork，拥有丰富的插件、脚本和 CI 集成示例，便于快速落地。

**典型接入方式**  
1. **本地或容器运行**：直接下载 ZAP Desktop 或使用官方 Docker 镜像（`owasp/zap2docker-stable`），通过 UI 或 CLI 启动。  
2. **CI/CD 集成**：在 Jenkins、GitHub Actions、GitLab CI 等流水线中调用 ZAP 的命令行模式或 Docker 镜像，执行自动化安全扫描并将报告输出为 JUnit、JSON 或 SARIF。  
3. **脚本化与插件**：利用 ZAP 的 Python/Jython、JavaScript 或 Groovy 脚本接口，自定义认证流程、漏洞过滤或结果上报；亦可通过 Marketplace 安装现成插件（如 OpenAPI 解析、Active Scan Rules 等）。  

**生产可用性**  
- **成熟度高**：项目活跃，最近一次提交在 2026‑06‑23，且拥有稳定的发布周期（每 3‑4 周一次）。  
- **部署可靠**：官方提供的 Docker 镜像经过安全审计，可在 Kubernetes、OpenShift 等容器平台无缝运行。  
- **风险与准备**：虽然核心功能已相当完善，但元数据中缺少明确的“一键集成”文档，建议先在小范围 PoC 环境验证安装、认证脚本和报告收集的成本，再逐步推广到全链路。  

总体而言，ZAP 具备高生产级别的可靠性，适合作为安全审计的 OSS 候选，在实现自动化安全检测、提升合规性方面能够快速产生价值。

## 🧭 Practical evaluation

**Value:** zaproxy/zaproxy helps catch security and privacy issues earlier in the workflow.

**Best use cases**

- strengthen security checks
- add auth or privacy controls
- audit risk earlier

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 15315 GitHub stars
- 2583 forks
- updated 2026-06-23
- primary language: Java
- 9 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 85/100 |
| stars | 89/100 |
| topics | 100/100 |
| outlook | 85/100 |
| quality | 95/100 |
| recency | 100/100 |
| adoption | 88/100 |
| production | 79/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/zaproxy/zaproxy) · [← Back to Security](./README.md)</sub>
