# ente/ente

[![Stars](https://img.shields.io/github/stars/ente/ente?style=flat-square&color=yellow)](https://github.com/ente/ente/stargazers) [![Forks](https://img.shields.io/github/forks/ente/ente?style=flat-square&color=blue)](https://github.com/ente/ente/network) [![Language](https://img.shields.io/badge/lang-Dart-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> 💚 End-to-end encrypted cloud for everything.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 27.3k |
| 🍴 **Forks** | 1.7k |
| 💻 **Language** | Dart |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`2fa` `android` `authy` `e2ee` `encryption` `end-to-end-encryption` `flutter` `golang` `google-photos` `google-photos-alternative` `ios` `opensource`

## 🎯 Categories

Mobile · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Ente is an open‑source, end‑to‑end encrypted cloud platform built with Dart that lets users store photos, videos, files and other data securely across devices. With a thriving community (27 k+ stars, 1.6 k forks) and recent activity, it offers a ready‑made, privacy‑first alternative to commercial cloud services. The project is well‑documented and can be trialled quickly as a proof‑of‑concept for any workflow that needs strong encryption and user‑controlled access.

**Value**  
- **Security & privacy** – All data is encrypted on the client before it ever leaves the device, eliminating reliance on third‑party storage providers.  
- **Cross‑platform mobile focus** – Native iOS/Android clients and a web UI make it easy to integrate into existing mobile‑first products.  
- **Open‑source transparency** – The codebase is publicly auditable, allowing teams to add custom auth, policy checks, or integrate with existing identity providers.

**Practical Adoption Path**  
1. **Read the README & explore the demo** – Verify that the core workflow (upload, share, sync) matches your use case.  
2. **Run a small proof‑of‑concept** – Deploy the Docker‑compose stack in a sandbox environment, connect a test mobile client, and exercise the encryption‑key lifecycle.  
3. **Extend or wrap** – If needed, add your own authentication layer (OAuth, SSO) or policy hooks via the provided APIs.  
4. **Pilot in production** – Gradually migrate a limited set of users or data, monitor performance and audit logs, then expand.

**Production Readiness**  
- **High**: The project shows strong recent activity (last commit 2026‑06‑24), a large star/fork count, and a vibrant ecosystem (17 topics).  
- **Maturity**: Core features (upload, sharing, end‑to‑end encryption) are stable, and the Docker deployment scripts simplify ops.  
- **Risks**: Final due‑diligence is required on licensing, long‑term maintainer commitment, and any disclosed security vulnerabilities, but no major red flags have been identified.  

Overall, ente/ente is a solid OSS candidate for teams that need a secure, self‑hosted cloud storage layer and can start with a low‑effort proof‑of‑concept before scaling to full production.

### Русский

**Краткое резюме:**  
`ente/ente` — это open‑source решение на Dart, предоставляющее сквозное шифрование для облачного хранилища, что делает его отличным выбором для проектов, где требуется усиленный контроль доступа, защита персональных данных и интеграция функций аутентификации/приватности. Типовой сценарий внедрения — небольшое POC, в котором через мобильное приложение или API подключается к существующей инфраструктуре хранения, проверяется совместимость README и базовый workflow, а затем расширяется до полноценного защищённого хранилища. По готовности к production проект находится на высоком уровне: активные коммиты, более 27 k звёзд, широкое принятие в сообществе и стабильный экосистемный контекст, однако перед запуском в прод необходимо окончательно проверить лицензию, текущий security‑posture и наличие активных мейнтейнеров.

### 中文

**项目简介**  
Ente（GitHub `ente/ente`）是一款使用端到端加密的全平台云存储服务，支持照片、文件、备忘录等任意数据的安全同步与共享。项目基于 Dart/Flutter 开发，拥有超过 27 k ★、1.6 k Fork，最近一次提交仍在 2026‑06‑24，活跃度和社区认可度都很高。

**价值**  
- **数据隐私**：所有数据在本地加密后再上传，服务器仅保存密文，确保用户隐私不被泄露。  
- **跨平台统一**：提供 iOS、Android、Web 与桌面客户端，开发者可在同一套代码库中实现多端一致的存储体验。  
- **开源可审计**：完整源码公开，企业可以自行审计加密实现或定制安全策略，满足合规要求。

**典型接入方式**  
1. **阅读 README 与 API 文档**：确认 SDK 支持的功能（文件上传/下载、相册管理、共享链接等）。  
2. **创建小型 PoC**：在现有移动或 Web 项目中引入 `ente` 的 Dart 包，完成用户登录、加密上传、解密下载的基本流程，以验证端到端加密链路。  
3. **扩展业务逻辑**：在 PoC 成功后，可进一步集成权限控制、二次验证或自定义加密策略，满足特定业务需求。  

**生产可用性**  
- **活跃维护**：截至 2026‑06‑24 项目仍在持续更新，社区贡献活跃。  
- **成熟生态**：已有多家企业和个人用户在生产环境中使用，社区提供丰富的 issue 与 PR 支持。  
- **风险评估**：暂无重大元数据或许可证风险，但在正式投产前仍建议完成一次完整的安全审计（包括依赖库的漏洞扫描）并确认维护者的响应时效。  

综上，Ente 具备高安全性、跨平台易集成以及稳健的社区支撑，是进行隐私敏感数据存储的可靠 OSS 选型。

## 🧭 Practical evaluation

**Value:** ente/ente may be useful when its README and activity match a concrete workflow.

**Best use cases**

- strengthen security checks
- add auth or privacy controls

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 27292 GitHub stars
- 1681 forks
- updated 2026-06-24
- primary language: Dart
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 81/100 |
| stars | 94/100 |
| topics | 100/100 |
| outlook | 82/100 |
| quality | 91/100 |
| recency | 80/100 |
| adoption | 91/100 |
| production | 78/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/ente/ente) · [← Back to Mobile](./README.md)</sub>
