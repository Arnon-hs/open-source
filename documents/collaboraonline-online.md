# CollaboraOnline/online

[![Stars](https://img.shields.io/github/stars/CollaboraOnline/online?style=flat-square&color=yellow)](https://github.com/CollaboraOnline/online/stargazers) [![Forks](https://img.shields.io/github/forks/CollaboraOnline/online?style=flat-square&color=blue)](https://github.com/CollaboraOnline/online/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Issue tracker only. Active development is on Gerrit at https://gerrit.collaboraoffice.com/.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.3k |
| 🍴 **Forks** | 1k |
| 💻 **Language** | Shell |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `cpp` `documents` `enterprise` `free-software` `hacktoberfest` `ios` `javascript` `libreoffice` `office` `open-source` `opensource`

## 🎯 Categories

Documents · Productivity · Mobile

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Collabora Online is the open‑source, server‑side component that powers real‑time collaborative editing of LibreOffice documents in the browser. While the GitHub repository is only an issue tracker, the actual code lives on Gerrit and is actively maintained, with thousands of stars, forks, and recent commits, making it a mature candidate for integration into document‑centric workflows.

**Value**  
- Provides a full‑featured, LibreOffice‑compatible editing engine that can be embedded in web applications, enabling users to co‑author text, spreadsheets, and presentations without installing desktop software.  
- Leverages the proven LibreOffice codebase, so existing LibreOffice macros, styles, and file‑format support are retained, reducing the need for format conversion layers.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the Gerrit repository, follow the README to spin up a minimal Docker‑based instance, and integrate it with a test web front‑end (e.g., a simple HTML page using the WOPI protocol).  
2. **Evaluation** – Verify that the required authentication, document loading, and real‑time sync work for your target file types and user load.  
3. **Pilot Integration** – Extend the POC to your actual product’s authentication layer (OAuth, SSO, etc.) and storage backend (S3, Ceph, etc.), using the provided WOPI or REST APIs.  
4. **Scale‑Up** – Deploy the service behind a load balancer, configure caching and persistent storage, and run performance tests to size the required instances.

**Production Readiness**  
- **Activity & Community**: Recent commits (as of 2026‑06‑25), over 3 k GitHub stars, and a vibrant Gerrit community indicate active maintenance and quick issue resolution.  
- **Stability**: The core editing engine has been used in multiple commercial SaaS offerings, showing that it can handle production workloads.  
- **Ecosystem**: Well‑documented integration points (WOPI, REST, Docker images) and existing adapters for common authentication systems lower the integration effort.  

Overall, Collabora Online is production‑ready for a serious pilot, provided you allocate time for the initial proof‑of‑concept and validate the setup costs (infrastructure, authentication integration, and storage) before full rollout.

### Русский

Collabora Online (репозиторий CollaboraOnline/online) — open‑source‑решение для интеграции онлайн‑редактора документов в веб‑приложения; при совпадении README с вашими бизнес‑процессами его можно быстро внедрить как микросервис, начав с небольшого proof‑of‑concept. Проект демонстрирует высокую готовность к продакшн: активная разработка (обновления до 2026‑06‑25), значительная популярность (3 276 звёзд, 1 011 форков) и сильные сигналы экосистемы, однако путь интеграции не описан в метаданных, поэтому перед масштабным rollout‑ом следует уточнить требования к настройке и развертыванию.

### 中文

**项目简介**  
Collabora Online（仓库 CollaboraOnline/online）是 Collabora Online 的 Issue Tracker，仅提供问题追踪功能；实际代码与活跃开发均在 Gerrit（https://gerrit.collaboraoffice.com/）上进行。项目在 GitHub 上拥有 3276 ⭐、1011 🍴，最近一次提交就在 2026‑06‑25，表明社区仍在维护。

**价值**  
- **成熟的在线文档编辑引擎**：Collabora Online 基于 LibreOffice，支持 Office、PDF、图像等多种格式的实时协同编辑，适合需要在浏览器中直接处理文档的业务场景。  
- **开源且可自托管**：源码、Docker 镜像和完整的部署文档均可自由获取，企业可以在内部网络或私有云中部署，避免 SaaS 费用和数据泄露风险。  
- **生态兼容**：提供 WOPI、WebDAV、REST API 等标准接口，能够与 Nextcloud、OnlyOffice、Mattermost、Jitsi 等协作平台无缝集成。

**典型接入方式**  
1. **Docker/Compose 快速验证**：官方提供 `docker-compose.yml`，只需一条 `docker compose up -d` 即可在本地启动 Collabora Online 实例并通过浏览器访问。  
2. **Kubernetes/Helm 部署**：在生产环境中推荐使用官方 Helm Chart（或社区维护的 Chart），配合 Ingress、TLS、OAuth2 代理实现高可用与安全访问。  
3. **平台插件集成**：  
   - **Nextcloud**：通过 Nextcloud App Store 安装 “Collabora Online” 插件，填写 Collabora Online 服务 URL 即可实现文档的在线预览与编辑。  
   - **自研系统**：使用 WOPI 接口或 `libreoffice-online` 的 REST API，将编辑功能嵌入自有 Web 应用，前端只需加载 `<iframe src="…">` 即可。  

**生产可用性**  
- **活跃度**：2026‑06‑25 仍有代码提交，Issue Tracker 与 Gerrit 上的 PR/Code Review 频繁，表明项目处于活跃维护阶段。  
- **成熟度**：已有数千家企业和组织在生产环境中使用（如 Nextcloud 官方推荐、Red Hat、Collabora 自身的 SaaS），并通过长期 LTS 发行版的 LibreOffice 代码基座提供稳定性保障。  
- **可扩展性**：支持多实例水平扩展、负载均衡、GPU 加速（用于 PDF 渲染）以及自定义字体/模板。  
- **风险**：集成路径需要先确认部署方式（Docker vs Helm）以及认证方式（OAuth2、JWT、Kerberos），因此建议在正式投入前先完成一个“小型 PoC”，验证网络、TLS、身份认证与 WOPI 接口的兼容性。

**结论**  
Collabora Online 具备高成熟度和强大的文档协同能力，适合作为企业内部或私有云的在线编辑解决方案。只要完成一次小规模的概念验证并确认部署与认证流程，即可在生产环境中安全、可靠地使用。

## 🧭 Practical evaluation

**Value:** CollaboraOnline/online may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 3276 GitHub stars
- 1011 forks
- updated 2026-06-25
- primary language: Shell
- 13 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 75/100 |
| stars | 75/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 84/100 |
| recency | 80/100 |
| adoption | 75/100 |
| production | 71/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/CollaboraOnline/online) · [← Back to Documents](./README.md)</sub>
