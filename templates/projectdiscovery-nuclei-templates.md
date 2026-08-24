# projectdiscovery/nuclei-templates

[![Stars](https://img.shields.io/github/stars/projectdiscovery/nuclei-templates?style=flat-square&color=yellow)](https://github.com/projectdiscovery/nuclei-templates/stargazers) [![Forks](https://img.shields.io/github/forks/projectdiscovery/nuclei-templates?style=flat-square&color=blue)](https://github.com/projectdiscovery/nuclei-templates/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Community curated list of templates for the nuclei engine to find security vulnerabilities.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 12.5k |
| 🍴 **Forks** | 3.5k |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bugbounty` `exploit-development` `exploits` `fingerprint` `hacktoberfest` `nuclei` `nuclei-checks` `nuclei-templates` `security` `vulnerability-detection`

## 🎯 Categories

Templates · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The *projectdiscovery/nuclei-templates* repository is a community‑maintained collection of detection templates for the Nuclei scanning engine, enabling fast identification of security and privacy vulnerabilities. With over 12 k stars, active contributions, and recent updates, it offers a ready‑to‑use, high‑quality rule set that can be plugged into existing CI/CD pipelines to catch issues early.  

**Value**  
- **Early risk detection** – By providing continuously updated, community‑vetted vulnerability signatures, the templates let teams surface misconfigurations, exposed secrets, and known CVEs before code reaches production.  
- **Broad coverage** – Templates span web applications, cloud services, containers, and compliance checks, helping organizations harden their attack surface across multiple layers.  
- **Cost‑effective security** – Leveraging an open‑source asset eliminates the need for expensive commercial rule libraries while still delivering comparable detection depth.  

**Practical Adoption Path**  
1. **Install Nuclei** (CLI) in your build environment or security tooling stack.  
2. **Pull the latest templates** (`nuclei -update-templates` or clone the repo) to keep the rule set current.  
3. **Integrate** the scan step into CI pipelines (GitHub Actions, GitLab CI, Jenkins, etc.) with a simple command such as `nuclei -t ./nuclei-templates/ -target <url>`.  
4. **Customize** by adding organization‑specific templates or disabling irrelevant ones via tags or the `-exclude-tags` flag.  
5. **Monitor** results through existing ticketing or SIEM systems using Nuclei’s JSON/CSV output options.  

**Production Readiness**  
- **Activity & Adoption** – The repo shows recent commits (as of 2026‑06‑23), a high star/fork count, and active community contributions, indicating strong maintenance.  
- **Integration Simplicity** – Exposes a straightforward CLI and can be invoked programmatically via its Go SDK or wrapped in scripts, fitting seamlessly into automated workflows.  
- **Ecosystem Fit** – Compatible with major CI/CD platforms, container orchestration, and cloud native tooling; the primary language (JavaScript) is only for documentation/examples, while the engine itself is Go‑based and lightweight.  
- **Risk Profile** – No critical licensing or security red flags have been identified, though a final review of the repository’s license (Apache‑2.0) and maintainer responsiveness is advisable before enterprise rollout.  

Overall, *projectdiscovery/nuclei-templates* is a mature, high‑impact OSS component that can be quickly adopted to enhance an organization’s security posture with minimal friction.

### Русский

**Краткое резюме:** projectdiscovery/nuclei-templates — это открытый набор шаблонов для движка Nuclei, позволяющий автоматизированно обнаруживать уязвимости и проблемы конфиденциальности ещё на ранних этапах разработки. Типовой сценарий — интеграция шаблонов в CI/CD pipeline (CLI/SDK) для регулярных security‑сканирований, что усиливает контроль над рисками и ускоряет реакцию на найденные проблемы. Проект считается готовым к production: активные коммиты, более 12 тыс. звёзд, широкое принятие в сообществе и надёжная экосистема, требующая лишь финального подтверждения лицензии и поддержки.

### 中文

**项目简介**  
projectdiscovery/nuclei-templates 是由社区维护的 Nuclei 扫描引擎模板库，收录了数千条可直接用于检测安全漏洞和隐私风险的规则。  

**价值**  
- **提前发现风险**：在 CI/CD、代码审计或渗透测试阶段即能自动化捕获常见漏洞和配置错误，帮助团队在生产环境之前修复问题。  
- **降低安全成本**：通过复用社区共享的高质量模板，避免重复编写规则，提升安全团队的效率。  

**典型接入方式**  
1. **CLI 直接使用**：在本地或 CI 环境中安装 Nuclei（`go install -v github.com/projectdiscovery/nuclei/v2/cmd/nuclei@latest`），然后通过 `-t` 参数指向模板仓库路径或 GitHub URL，例如 `nuclei -t https://github.com/projectdiscovery/nuclei-templates`。  
2. **API/SDK 集成**：项目提供了 Go SDK，可在自定义安全平台中调用 Nuclei 引擎并加载指定模板，实现自动化扫描与结果回调。  
3. **容器化部署**：官方提供了 Docker 镜像 `projectdiscovery/nuclei`，配合 `-t /templates` 挂载模板目录，适合在 Kubernetes 中作为安全 side‑car 使用。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑23，仓库拥有 12 535 星、3 532 Fork，最近一次提交仅数天前，表明社区和维护者仍在持续更新。  
- **生态兼容**：模板以 YAML/JSON 形式存放，语言无关，可直接被 Nuclei（Go 实现）解析，兼容多数 CI/CD 工具链（GitHub Actions、GitLab CI、Jenkins 等）。  
- **成熟度**：项目已被多家安全公司和开源项目在生产环境中采用，具备完整的发布流程、版本标签和安全审计记录，属于“高”生产就绪度的 OSS 候选。  

综上，projectdiscovery/nuclei-templates 通过即插即用的模板体系，为安全检测提供了可靠、可扩展且已在生产环境验证的解决方案。

## 🧭 Practical evaluation

**Value:** projectdiscovery/nuclei-templates helps catch security and privacy issues earlier in the workflow.

**Best use cases**

- strengthen security checks
- add auth or privacy controls
- audit risk earlier

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 12535 GitHub stars
- 3532 forks
- updated 2026-06-23
- primary language: JavaScript
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 89/100 |
| stars | 87/100 |
| topics | 100/100 |
| outlook | 68/100 |
| quality | 79/100 |
| recency | 40/100 |
| adoption | 88/100 |
| production | 62/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/projectdiscovery/nuclei-templates) · [← Back to Templates](./README.md)</sub>
