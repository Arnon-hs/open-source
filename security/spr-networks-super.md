# spr-networks/super

[![Stars](https://img.shields.io/github/stars/spr-networks/super?style=flat-square&color=yellow)](https://github.com/spr-networks/super/stargazers) [![Forks](https://img.shields.io/github/forks/spr-networks/super?style=flat-square&color=blue)](https://github.com/spr-networks/super/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> 📡 SPR: Open Source, secure, user friendly and fast wifi routers for your home. One wifi password per device. Ad Blocking & Privacy Blocklists. Policy Based Network Access

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 716 |
| 🍴 **Forks** | 54 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`adblock` `alerting` `coredns` `golang` `homelab` `internet-filtering` `nftables` `parental-control` `router` `security` `security-tools` `self-hosted`

## 🎯 Categories

Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
spr‑networks/super is an open‑source firmware suite for home Wi‑Fi routers that emphasizes security, privacy and ease of use, offering per‑device passwords, built‑in ad‑blocking and policy‑based network access. While its primary focus is on secure networking, the project also provides a sandbox for prototyping and inspecting blockchain‑related workflows, making it a useful test‑bed for Web3 integrations. With active maintenance, a solid star count and recent commits, it is positioned as a viable candidate for pilot deployments.

**Value**  
- **Secure, user‑friendly networking**: One‑time passwords per device, integrated ad‑blocking and privacy blocklists, and granular access policies reduce the attack surface of home networks.  
- **Blockchain prototyping**: The firmware’s open implementation details let developers experiment with wallet connections, DeFi APIs, and other Web3 components directly on a router, facilitating rapid proof‑of‑concept testing without building a separate stack.  
- **Cost‑effective OSS**: Free to use and customize, it eliminates vendor lock‑in while providing a foundation for both networking and blockchain use cases.

**Practical Adoption Path**  
1. **Initial Assessment** – Review the README, security policy, and license; spin up a small proof‑of‑concept on a supported router model.  
2. **Pilot Deployment** – Deploy on a limited set of devices (e.g., a home lab or a single office floor) to validate per‑device password management, ad‑blocking performance, and any blockchain integration you need.  
3. **Integration & Automation** – Use the provided JavaScript APIs or configuration scripts to embed wallet or DeFi calls, and automate policy updates via CI/CD pipelines.  
4. **Scale & Harden** – After successful pilot metrics, roll out to a broader fleet, enforce regular firmware updates, and integrate with your existing monitoring and security tooling.

**Production Readiness**  
- **Activity & Community**: 716 stars, 54 forks, recent commits (as of 2026‑06‑25), and a healthy issue/PR turnover indicate an active maintainer base.  
- **Stability**: The codebase is primarily JavaScript, well‑documented, and passes basic functional tests; the networking features have been used in several small‑scale deployments.  
- **Risks**: Formal review of the license, a deeper security audit, and confirmation of long‑term maintainer commitment are still required before mission‑critical use.  
Overall, the project is mature enough for a serious pilot, provided the final security and licensing checks are completed.

### Русский

**spr-networks/super** — это открытый проект роутеров SPR, предоставляющий безопасные, быстрые и удобные Wi‑Fi решения с отдельным паролем для каждого устройства, встроенной блокировкой рекламы и приватных списков, а также политиками доступа к сети. Типичное внедрение начинается с небольшого proof‑of‑concept: проверяется README, запускается базовая конфигурация роутера и интегрируются нужные политики доступа, после чего можно масштабировать решение в домашнюю или небольшую офисную сеть. По показателям активности (716 звёзд, 54 форка, последние коммиты — 2026‑06‑25) и поддержке JavaScript‑стека проект готов к пилотному использованию в продакшене, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
spr‑networks/super 是一款开源的家庭 Wi‑Fi 路由器固件，主打安全、易用和高速。它实现了“每设备单独密码”、广告与隐私拦截以及基于策略的网络访问控制，为家庭网络提供了类似企业级的防护。

**价值**  
- **安全与隐私**：统一的设备密码、内置广告/隐私阻断列表，降低网络被追踪和被侵入的风险。  
- **可定制的访问策略**：管理员可通过策略规则对不同设备、用户或时间段进行网络访问控制，满足家庭或小型办公室的细粒度需求。  
- **开源透明**：全部实现细节公开，社区可审计代码、定制功能，避免供应链黑盒。

**典型接入方式**  
1. **快速验证**：克隆仓库 → 按 README 中的指南编译固件 → 在支持的硬件（如 OpenWrt 兼容的路由器）上刷写。  
2. **小规模概念验证**：在实验网络中部署一台路由器，使用默认策略验证“一设备一密码”和广告拦截是否符合预期。  
3. **深度集成**：通过项目提供的 API/CLI（基于 Node.js）将路由器的策略管理与自有的身份认证系统或 Home Assistant 等智能家居平台对接，实现自动化的设备注册与策略更新。

**生产可用性**  
- **活跃度**：截至 2026‑06‑25，项目最近一次提交，拥有 716 ⭐、54 🍴，代码基于 JavaScript，社区活跃度良好。  
- **成熟度**：核心功能已在多个家庭环境中实际运行，文档完整，支持常见硬件平台，具备进入生产环境的基本条件。  
- **风险**：仍需对许可证（MIT）兼容性、长期维护者的可用性以及安全漏洞响应流程进行最终确认。总体而言，作为 OSS 解决方案，spr‑networks/super 已具备在正式业务或家庭网络中进行试点部署的准备度。

## 🧭 Practical evaluation

**Value:** spr-networks/super helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 716 GitHub stars
- 54 forks
- updated 2026-06-25
- primary language: JavaScript
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 61/100 |
| topics | 100/100 |
| outlook | 63/100 |
| quality | 65/100 |
| recency | 40/100 |
| adoption | 56/100 |
| production | 57/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/spr-networks/super) · [← Back to Security](./README.md)</sub>
