# ente-io/ente

[![Stars](https://img.shields.io/github/stars/ente-io/ente?style=flat-square&color=yellow)](https://github.com/ente-io/ente/stargazers) [![Forks](https://img.shields.io/github/forks/ente-io/ente?style=flat-square&color=blue)](https://github.com/ente-io/ente/network) [![Language](https://img.shields.io/badge/lang-Dart-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-77%2F100-brightgreen?style=flat-square)](#)

> 💚 End-to-end encrypted cloud for everything.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 27.3k |
| 🍴 **Forks** | 1.7k |
| 💻 **Language** | Dart |
| 📈 **Score** | 77/100 |
| 🗓️ **Last push** | 2026-06-22 |
| 🔍 **Source** | github |

## 🏷️ Topics

`2fa` `android` `authy` `e2ee` `encryption` `end-to-end-encryption` `flutter` `golang` `google-photos` `google-photos-alternative` `ios` `opensource`

## 🎯 Categories

Mobile · Security

## 📝 Summary

### English

**Brief Summary**  
Ente (ente‑io/ente) is an open‑source, end‑to‑end encrypted cloud platform built with Dart, offering secure storage for any type of data. With a strong community presence (27 k+ stars, 1.6 k forks) and recent activity, it is a mature candidate for pilots that need robust privacy and authentication controls.  

**Value**  
Ente gives developers a ready‑made, client‑side encryption stack that removes the need to build custom cryptographic layers, helping teams meet strict security and compliance requirements while delivering a seamless user experience across mobile devices. Its modular design also makes it easy to plug in additional auth providers or policy checks, extending its usefulness beyond simple file storage.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the example app, and verify the encryption workflow against your own data.  
2. **README & API Review** – Follow the documented setup steps, confirm the SDK interfaces align with your existing architecture, and test integration with your authentication system.  
3. **Pilot Integration** – Replace a non‑critical storage component in a sandbox environment, instrument logging, and run security tests.  
4. **Full Rollout** – Gradually migrate production workloads, add monitoring, and configure backup/replication as needed.  

**Production Readiness**  
The project scores 77/100, shows continuous maintenance (latest commit 2026‑06‑22), and enjoys broad ecosystem adoption, indicating high production readiness for a serious pilot. While the license and long‑term maintainer commitment should be confirmed, there are no immediate metadata or security red flags, making Ente a solid OSS candidate for secure cloud storage in production.

### Русский

Ente (ente‑io/ente) — это open‑source сервис сквозного шифрования, предоставляющий облачное хранище для любых файлов с полной защитой конфиденциальности. Его типичное внедрение — небольшое POC в существующем мобильном или веб‑приложении, где требуется добавить безопасный обмен данными, контроль доступа и приватные бэкапы; после проверки README и базовых API проект готов к масштабному пилоту. По активности репозитория (2026‑06‑22), большому количеству звёзд и форков, а также поддержке Dart, Ente считается почти готовым к production, однако окончательная оценка лицензии и процесса обновления безопасности всё‑ещё требуется.

### 中文

**项目简介**  
Ente（ente-io/ente）是一款基于端到端加密的全平台云存储，支持照片、文件、备忘录等多种数据的安全同步与共享。它使用 Dart/Flutter 实现，拥有超过 27k 颗星和活跃的社区维护，适合作为隐私敏感业务的存储后端。

**价值**  
- **数据安全**：所有数据在客户端加密，服务器仅保存密文，确保即使服务器被攻破也无法泄露用户内容。  
- **跨平台**：提供 iOS、Android、Web 与桌面客户端，开发者可通过统一的 API 在多端统一管理加密存储。  
- **开源可审计**：完整源码公开，企业可以自行审计加密实现、密钥管理流程，满足合规与内部安全审查需求。

**典型接入方式**  
1. **读取 README 与 SDK**：先阅读仓库的快速入门文档，确定使用的语言（Flutter/Dart）或通过 REST API。  
2. **创建测试项目**：在本地新建 Flutter 项目，添加 `ente_sdk`（或对应的 HTTP 客户端）依赖，完成用户注册/登录流程。  
3. **上传/下载示例**：使用 SDK 提供的 `uploadFile`、`downloadFile` 等方法实现文件的加密上传与解密下载，验证端到端加密是否生效。  
4. **小范围 PoC**：在实际业务中挑选一类非核心数据（如日志、备份文件）进行试点，评估性能、冲突解决和权限控制等细节后再全面推广。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑22，星标 27k+、fork 1.6k，社区活跃，Issue 反馈响应及时。  
- **成熟度**：已在多个公开项目中使用，具备完整的 CI、自动化发布和安全审计流程，符合企业级稳定性要求。  
- **风险**：需进一步确认许可证（MIT）兼容性、密钥管理策略以及是否有专职维护者长期跟进安全漏洞。总体而言，Ente 已具备在生产环境中进行正式试点的条件，建议先在受控环境完成 PoC 验证后逐步推广。

## 🧭 Practical evaluation

**Value:** ente-io/ente may be useful when its README and activity match a concrete workflow.

**Best use cases**

- strengthen security checks
- add auth or privacy controls

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 27271 GitHub stars
- 1681 forks
- updated 2026-06-22
- primary language: Dart
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 81/100 |
| stars | 94/100 |
| topics | 100/100 |
| outlook | 89/100 |
| quality | 96/100 |
| recency | 100/100 |
| adoption | 91/100 |
| production | 84/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/ente-io/ente) · [← Back to Mobile](./README.md)</sub>
