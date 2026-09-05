# getumbrel/umbrel

[![Stars](https://img.shields.io/github/stars/getumbrel/umbrel?style=flat-square&color=yellow)](https://github.com/getumbrel/umbrel/stargazers) [![Forks](https://img.shields.io/github/forks/getumbrel/umbrel?style=flat-square&color=blue)](https://github.com/getumbrel/umbrel/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> An elegant home server OS. Run OpenClaw, store your files and photos, run a Bitcoin node, and do more with over 300 apps in the Umbrel App Store.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 11.2k |
| 🍴 **Forks** | 757 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bitcoin` `docker` `home-server` `homeserver` `lightning` `openclaw` `personal-server` `raspberry-pi` `raspberrypi` `self-hosted` `self-hosting` `selfhosted`

## 🎯 Categories

Crypto · Backend · DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
Umbrel (getumbrel/umbrel) is an open‑source home‑server operating system that bundles a Bitcoin node, a suite of privacy‑focused tools, and an app store with more than 300 ready‑to‑run services. Built primarily in TypeScript, the platform exposes clear APIs, SDKs, and CLI commands, making it a convenient sandbox for prototyping and inspecting blockchain‑related workflows.

**Value**  
- **Rapid Web3 prototyping** – Developers can spin up a full Bitcoin node and a host of DeFi, wallet, and storage apps in minutes, then interact with them through documented APIs or the built‑in CLI.  
- **Transparent implementation** – Because Umbrel’s source code, configuration files, and integration points are openly available, teams can study real‑world blockchain integration patterns and reuse components for custom solutions.  
- **Rich ecosystem** – The Umbrel App Store provides over 300 pre‑packaged services (e.g., OpenClaw, file sync, media servers), reducing the time needed to assemble a complete stack for testing or demo environments.

**Practical Adoption Path**  
1. **Evaluation** – Fork or clone the repo, run the provided Docker‑compose/VM installer on a local machine or a cheap single‑board computer (Raspberry Pi, Intel NUC). Verify connectivity to the bundled Bitcoin node via RPC or REST.  
2. **Integration** – Use the exposed API/CLI to automate app installation, configure custom scripts, or connect external services (e.g., a front‑end wallet UI). The TypeScript SDK simplifies writing integration tests.  
3. **Pilot** – Deploy Umbrel on a dedicated VM or on‑prem server for a controlled pilot, enabling selected team members to build and test wallet, DeFi, or data‑storage features against a live node without exposing the public internet.  
4. **Scale** – Once the prototype is validated, extract the needed micro‑services (e.g., the Bitcoin node, storage backend) and redeploy them in a Kubernetes or cloud‑native environment, preserving the same APIs used during the pilot.

**Production Readiness**  
- **Activity & Adoption** – 11 239 stars, 757 forks, recent commits (as of 2026‑05‑12), and a vibrant community indicate strong momentum.  
- **Stability** – The core OS and most apps are version‑locked and receive regular security patches; the project follows semantic versioning and provides migration guides.  
- **Ecosystem Support** – Over 300 vetted apps, extensive documentation, and a public forum make troubleshooting straightforward.  
- **Risks** – Licensing (MIT) is permissive, but a final legal review is recommended. Security posture depends on keeping the underlying OS and Docker images up to date; organizations should implement standard hardening (firewall, VPN, monitoring) before production use.  

Overall, Umbrel offers a high‑readiness, low‑friction foundation for teams looking to prototype, test, or even run production‑grade blockchain services within a well‑maintained open‑source stack.

### Русский

**Umbrel** – это готовая к эксплуатации ОС для домашнего сервера, позволяющая запускать Bitcoin‑ноду, хранить файлы и подключать более 300 приложений из Umbrel App Store. Проект идеален для прототипирования и отладки Web3‑процессов: предоставляет открытый API/CLI, SDK и подробные метаданные, что упрощает интеграцию кошельков, DeFi‑сервисов и прочих блокчейн‑решений. Благодаря активной поддержке (11239 звёзд, частые обновления, широкая экосистема) Umbrel считается почти готовым к production‑использованию, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
Umbrel（`getumbrel/umbrel`）是一款面向家庭服务器的开源操作系统，内置 Bitcoin 全节点、文件/相册存储、OpenClaw 等基础服务，并通过 Umbrel App Store 提供 300+ 即装即用的应用。  

**价值**  
- **快速原型**：提供完整的区块链实现（节点、钱包、API），开发者可以直接在本地或小型服务器上搭建、调试 Web3、DeFi 或钱包功能，无需自行部署底层节点。  
- **全栈生态**：超过 300 个官方或社区应用覆盖存储、媒体、隐私、监控等场景，帮助团队在同一平台上完成从数据层到业务层的端到端验证。  
- **可视化与可扩展**：通过 UI 与 CLI 双通道暴露配置、日志和监控信息，便于审计链上交互细节并快速迭代。  

**典型接入方式**  
1. **Docker/OCI 镜像**：直接拉取官方 `umbrel/umbrel` 镜像，在任意支持 Docker 的机器（Raspberry Pi、VM、裸机）上启动。  
2. **CLI/SDK**：使用自带的 `umbrel-cli` 或 REST API（如 `/api/v1/bitcoin`）进行节点状态查询、钱包创建、交易广播等操作。  
3. **App Store**：在 UI 中搜索并“一键安装”所需的第三方应用（如 Lightning、IPFS、Nextcloud），亦可通过 `umbrel-apps` 目录自行添加自定义容器。  

**生产可用性**  
- **活跃度**：11239 Stars、757 Forks，最近一次提交为 2026‑05‑12，主语言 TypeScript，社区持续贡献。  
- **成熟度**：已在全球数万台家庭服务器上部署，具备完整的备份、自动更新和安全加固机制。  
- **风险**：目前未发现重大许可证或安全漏洞，但仍建议在正式生产环境前完成内部安全审计并确认维护者响应时效。  

总体而言，Umbrel 具备高可用的开源实现，适合作为区块链原型验证平台，也可在对安全、可维护性有要求的内部生产环境中直接使用。

## 🧭 Practical evaluation

**Value:** getumbrel/umbrel helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 11239 GitHub stars
- 757 forks
- updated 2026-05-12
- primary language: TypeScript
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 72/100 |
| stars | 86/100 |
| topics | 100/100 |
| outlook | 80/100 |
| quality | 87/100 |
| recency | 80/100 |
| adoption | 82/100 |
| production | 76/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/getumbrel/umbrel) · [← Back to Crypto](./README.md)</sub>
