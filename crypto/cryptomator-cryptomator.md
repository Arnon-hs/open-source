# cryptomator/cryptomator

[![Stars](https://img.shields.io/github/stars/cryptomator/cryptomator?style=flat-square&color=yellow)](https://github.com/cryptomator/cryptomator/stargazers) [![Forks](https://img.shields.io/github/forks/cryptomator/cryptomator?style=flat-square&color=blue)](https://github.com/cryptomator/cryptomator/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> Cryptomator for Windows, macOS, and Linux: Secure client-side encryption for your cloud storage, ensuring privacy and control over your data.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 15.5k |
| 🍴 **Forks** | 1.3k |
| 💻 **Language** | Java |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cloud-storage` `crypto` `cryptography` `cryptomator` `encryption` `java` `privacy` `security`

## 🎯 Categories

Crypto · Cloud & Storage · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Cryptomator is an open‑source client‑side encryption tool for Windows, macOS and Linux that lets users protect files stored in any cloud service. By encrypting data locally before it reaches the cloud, it gives users full control over privacy while remaining transparent to the underlying storage provider. The project is actively maintained, widely adopted (15 k+ stars) and written in Java, making it a solid foundation for prototyping and inspecting Web3‑related workflows.

**Value**  
- **Privacy‑first encryption**: Guarantees that only the user holds the decryption keys, a requirement for many blockchain and DeFi applications that need end‑to‑end confidentiality.  
- **Open implementation**: The source code, CLI, and API expose the cryptographic primitives and file‑vault management logic, letting developers study or reuse the exact encryption flow that would be needed in a wallet or smart‑contract‑backed storage solution.  
- **Cross‑platform consistency**: A single Java codebase runs on all major desktop OSes, simplifying testing of Web3 integrations across developer environments.

**Practical Adoption Path**  
1. **Evaluation** – Clone the repo, run the provided CLI (`cryptomator-cli`) or start the desktop UI to create a test vault and verify encryption/decryption against your cloud bucket (e.g., S3, Google Drive).  
2. **Integration** – Use the Java SDK (or invoke the CLI from scripts) to programmatically create vaults, add/remove files, and retrieve encrypted blobs. Wrap these calls in your Web3 service layer to store off‑chain data (IPFS hashes, metadata, etc.) securely.  
3. **Extension** – If you need a custom key‑management scheme (e.g., hardware wallet‑derived keys or threshold signatures), fork the relevant `Vault` classes and replace the key‑derivation module while preserving the existing file‑format compatibility.  
4. **Testing & CI** – Leverage the project's existing unit‑test suite as a baseline for your own integration tests, ensuring that any blockchain‑related transformations preserve the vault’s integrity.

**Production Readiness**  
- **Activity & Community**: Recent commits (as of 2026‑06‑24), a large contributor base, and over 1 300 forks indicate a healthy, actively maintained project.  
- **Stability**: The core encryption logic and file‑format have been stable for several major releases, with backward‑compatible migrations documented.  
- **Security Posture**: Open‑source cryptography audited by the community; however, a final security review (e.g., third‑party pen‑test, dependency scanning) is recommended before a production rollout.  
- **License**: Distributed under the GPL‑3.0‑or‑later license; ensure compatibility with your product’s licensing model.  

Overall, Cryptomator offers a mature, well‑documented encryption layer that can be quickly evaluated and integrated into Web3 prototypes, and—with a brief security and licensing audit—can be promoted to production use in privacy‑sensitive blockchain applications.

### Русский

Cryptomator — это кроссплатформенный клиент‑сайд шифратор (Windows, macOS, Linux), который позволяет безопасно хранить файлы в облаке, полностью контролируя их конфиденциальность. Благодаря открытой Java‑реализации, доступному CLI/SDK и подробной документации, проект удобно использовать для прототипирования Web3‑workflow‑ов, проверки интеграций блокчейна и создания функций кошельков или DeFi. Высокий уровень готовности к продакшну подтверждается активным развитием (обновление 2026‑06‑24), большим сообществом (15 502 ★, 1 319 форков) и надёжной лицензией, хотя окончательная проверка безопасности и юридических аспектов всё‑ещё требуется.

### 中文

**项目简介**  
Cryptomator（cryptomator/cryptomator）是一款跨平台（Windows、macOS、Linux）的开源客户端加密工具，能够在本地对云存储文件进行端到端加密，确保用户数据的隐私与完全控制。

**价值**  
- **数据隐私**：所有加密在本地完成，密钥永不离开用户设备，云服务提供商无法读取内容。  
- **开发便利**：公开的 API/SDK/CLI 以及完整的实现细节，使其成为原型化 Web3、区块链钱包、DeFi 流程的理想实验平台。  
- **生态兼容**：支持常见云盘（Dropbox、Google Drive、OneDrive 等），可直接嵌入现有云存储工作流。

**典型接入方式**  
1. **CLI**：通过 `cryptomator-cli` 在脚本或 CI/CD 流程中创建、挂载、解锁保险箱。  
2. **Java SDK**：项目本身基于 Java，提供 `cryptomator-lib`，可在自定义 Java 应用中调用加密/解密 API。  
3. **REST/IPC**：启动本地服务后，使用 HTTP/IPC 与 Cryptomator 交互，实现跨语言（如 Node.js、Python）集成。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑24，拥有 15,502 星、1,319 Fork，最近一次提交在同日，社区活跃。  
- **成熟度**：跨平台桌面客户端已在多种生产环境中验证，错误率低，文档完整。  
- **风险**：需进一步审查许可证兼容性及安全审计报告，确认维护者的长期投入。总体而言，作为 OSS 组件，已具备在正式项目中试点或全量上线的条件。

## 🧭 Practical evaluation

**Value:** cryptomator/cryptomator helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 15502 GitHub stars
- 1319 forks
- updated 2026-06-24
- primary language: Java
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 78/100 |
| stars | 89/100 |
| topics | 100/100 |
| outlook | 84/100 |
| quality | 89/100 |
| recency | 80/100 |
| adoption | 86/100 |
| production | 75/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/cryptomator/cryptomator) · [← Back to Crypto](./README.md)</sub>
