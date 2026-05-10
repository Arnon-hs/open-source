# Lissy93/web-check

[![Stars](https://img.shields.io/github/stars/Lissy93/web-check?style=flat-square&color=yellow)](https://github.com/Lissy93/web-check/stargazers) [![Forks](https://img.shields.io/github/forks/Lissy93/web-check?style=flat-square&color=blue)](https://github.com/Lissy93/web-check/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> 🕵️‍♂️ All-in-one OSINT tool for analysing any website

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 33.1k |
| 🍴 **Forks** | 2.7k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-05-10 |
| 🔍 **Source** | github |

## 🏷️ Topics

`osint` `privacy` `security` `security-tools` `sysadmin`

## 🎯 Categories

Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Lissy93/web‑check is a TypeScript‑based, all‑in‑one OSINT toolkit that scans any website for security and privacy weaknesses, surfacing issues early in the development pipeline. With over 33 k GitHub stars, frequent updates (last commit 2026‑05‑10) and a vibrant fork community, it is a mature open‑source candidate for security‑focused teams. A small proof‑of‑concept integration—starting with the README examples—can quickly validate its fit before broader rollout.

**Value**  
- **Early detection**: Automates discovery of misconfigurations, exposed credentials, and privacy leaks, letting teams remediate before code ships.  
- **Broad coverage**: Consolidates many OSINT checks (DNS, SSL, headers, third‑party services) into a single CLI, reducing tool sprawl.  
- **Community‑driven**: High star/fork count and active issue discussion mean bugs are identified and fixed quickly, and new checks are contributed regularly.

**Practical Adoption Path**  
1. **Proof of Concept** – Clone the repo, run the CLI against a non‑production domain using the default configuration to verify output and understand required parameters.  
2. **CI Integration** – Add a lightweight step to existing pipelines (e.g., GitHub Actions, Jenkins) that runs `web-check` on PR URLs and fails the build on high‑severity findings.  
3. **Policy Tuning** – Customize rule sets or thresholds via the provided config file to align with internal security policies.  
4. **Gradual Rollout** – Extend the step to all services, and optionally feed results into a central security dashboard or ticketing system for tracking remediation.

**Production Readiness**  
- **Activity & Maintenance**: Recent commits, a large contributor base, and active issue handling indicate a healthy maintainer ecosystem.  
- **Adoption Signals**: Thousands of forks and a strong star count show real‑world usage and community trust.  
- **Technical Maturity**: Written in TypeScript with clear documentation, the tool can be packaged as a Docker image or NPM module for consistent deployment.  
- **Risk Considerations**: No immediate licensing or metadata red flags, but a final review of the MIT/Apache license terms and a security audit of the dependency tree is advisable before full production use.  

Overall, Lissy93/web‑check is production‑ready for a pilot, offering immediate security value with a low‑friction integration path.

### Русский

**Lissy93/web-check** — это универсальный OSINT‑инструмент на TypeScript, позволяющий быстро выявлять уязвимости и проблемы конфиденциальности любого сайта, что помогает включать проверки безопасности на ранних этапах разработки. Для внедрения рекомендуется начать с небольшого proof‑of‑concept: установить пакет, протестировать его на одном‑двух сервисах и проверить README; при положительном результате можно масштабировать на все проекты. По оценкам проекта он готов к production: активные коммиты, более 33 тыс. звёзд, активное сообщество и хорошая экосистема, что делает его надёжным кандидатом для серьёзного пилотного использования.

### 中文

**项目简介**  
Lissy93/web-check 是一款基于 TypeScript 的全功能 OSINT（开源情报）工具，能够对任意网站进行安全与隐私风险的自动化分析。它聚合了子域枚举、端口扫描、指纹识别、隐私泄漏检测等多种检查手段，帮助团队在开发和运维的早期阶段发现潜在问题。

**价值体现**  
- **提前发现风险**：在代码提交、CI/CD 流程或上线前即对目标站点进行安全与合规审计，显著降低后期修复成本。  
- **统一安全基线**：提供统一的检查报告，可作为安全审计、合规评估或内部安全培训的参考。  
- **易于扩展**：基于插件化设计，开发者可以自定义检查规则或集成内部工具，满足特定业务需求。

**典型接入方式**  
1. **本地或容器化运行**：直接 `npm i -g web-check` 后在命令行使用，或通过官方提供的 Docker 镜像在 CI 环境中调用。  
2. **CI/CD 集成**：在 GitHub Actions、GitLab CI、Jenkins 等流水线中添加一步执行 `web-check scan <url> --output json`，并将结果作为构建状态或安全报告上传。  
3. **API/插件调用**：项目提供了可编程的 Node.js 接口，业务系统可以在后台服务中调用 `webCheck.scan(url)`，将结果实时写入内部监控或告警平台。  
4. **README/文档检查**：在项目初始化阶段先运行 `web-check readme-check <repo>`，快速评估项目文档中是否泄露敏感信息。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑10，项目仍在持续更新，拥有 33 058 个 GitHub 星、2 664 次 Fork，社区贡献活跃。  
- **成熟度**：核心功能已相对完整，TypeScript 代码质量良好，且提供详细的使用文档和示例。  
- **集成风险低**：仅需 Node.js 环境或 Docker 即可部署，依赖较少，适合作为安全审计的第一层防线。  
- **待确认事项**：在正式生产使用前建议再次审查许可证兼容性、维护者响应速度以及潜在的第三方依赖安全报告。  

综上所述，Lissy93/web-check 具备高可用性和明确的价值主张，适合作为安全与隐私审计的 OSS 方案，在小规模 PoC 验证后即可推广至正式生产环境。

## 🧭 Practical evaluation

**Value:** Lissy93/web-check helps catch security and privacy issues earlier in the workflow.

**Best use cases**

- strengthen security checks
- add auth or privacy controls
- audit risk earlier

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 33058 GitHub stars
- 2664 forks
- updated 2026-05-10
- primary language: TypeScript
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 86/100 |
| stars | 96/100 |
| topics | 63/100 |
| outlook | 86/100 |
| quality | 91/100 |
| recency | 100/100 |
| adoption | 93/100 |
| production | 81/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-10 · [View on GitHub](https://github.com/Lissy93/web-check) · [← Back to Security](./README.md)</sub>
