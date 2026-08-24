# C2SP/wycheproof

[![Stars](https://img.shields.io/github/stars/C2SP/wycheproof?style=flat-square&color=yellow)](https://github.com/C2SP/wycheproof/stargazers) [![Forks](https://img.shields.io/github/forks/C2SP/wycheproof?style=flat-square&color=blue)](https://github.com/C2SP/wycheproof/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-28%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 28/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Crypto

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Project Wycheproof is an open‑source test suite that checks cryptographic libraries for known vulnerabilities and implementation flaws. By running a comprehensive set of attack vectors against a library’s API, it helps developers verify that their crypto primitives (e.g., signatures, hash functions, key‑exchange) behave securely before they are used in blockchain or Web3 applications. The project is actively maintained (last update 2026‑05‑14) and is positioned as a dev‑tool for prototyping and internal security reviews rather than a turnkey production component.  

**Value**  
- **Security confidence:** Provides concrete, reproducible evidence that a crypto library resists real‑world attacks, reducing the risk of subtle bugs that could compromise wallets, DeFi contracts, or cross‑chain bridges.  
- **Fast feedback loop:** Integrates into CI pipelines, giving developers immediate pass/fail results for each supported algorithm, which speeds up security‑by‑design iterations.  
- **Open implementation details:** Test cases are fully visible, making it easy to understand why a failure occurs and to patch or replace the offending component.  

**Practical Adoption Path**  
1. **Select the target crypto library** (e.g., BouncyCastle, OpenSSL, libsodium) and add Wycheproof as a test dependency.  
2. **Run the provided test harness** (`mvn test`, `go test`, etc.) against the library’s API; review the generated report for any “FAIL” or “WARN” entries.  
3. **Address failures** by upgrading the library, configuring it securely, or swapping out vulnerable primitives.  
4. **Integrate into CI/CD** (GitHub Actions, Jenkins, etc.) so that every pull request re‑executes the Wycheproof suite, preventing regressions.  
5. **Document the results** and, if needed, add custom Wycheproof‑style tests for project‑specific edge cases (e.g., custom curve parameters).  

**Production Readiness**  
- **Maturity:** Medium. The suite is stable and actively updated, but it is a testing tool, not a production library.  
- **Dependencies & Maintenance:** Verify that the version of Wycheproof you adopt matches the language runtime and that the underlying crypto library receives regular security patches.  
- **License & Governance:** Confirm the open‑source license (Apache 2.0) aligns with your product’s licensing model and check the project’s issue tracker for unresolved critical bugs.  
- **Operational Considerations:** Because Wycheproof only reports test outcomes, you must still perform manual code reviews and threat modeling before shipping a blockchain‑related product.  

In short, Wycheproof is a valuable “security gate” for crypto components in Web3 projects; adopt it early in the development cycle, embed it in automated testing, and complement its findings with broader security audits before moving to production.

### Русский

Project Wycheproof — это набор тестов, проверяющих криптографические библиотеки на уязвимости, известные из реальных атак, что позволяет быстро оценить безопасность Web3‑приложений, кошельков и DeFi‑фич. Его типичное применение — прототипирование и аудит блокчейн‑интеграций, однако перед внедрением в продакшн требуется ручная проверка лицензии, поддержки и документации из‑за скудных метаданных. Готовность к production средняя: подходит для внутренних и экспериментальных решений при условии дополнительного контроля качества и обновлений.

### 中文

**项目简介**  
Project Wycheproof 是 Google 开源的安全测试套件，专门对常见加密库进行已知攻击向量的验证。它帮助开发者在原型或内部环境中快速检查区块链、钱包、DeFi 等 Web3 组件的加密实现是否存在已知漏洞。

**价值**  
- **安全把关**：提供覆盖广泛的攻击案例（如弱随机数、错误的填充、侧信道等），让团队在代码提交前发现潜在的密码学缺陷。  
- **加速研发**：在原型阶段即可对加密库进行自动化回归，降低后期安全审计成本。  
- **透明可审计**：所有测试用例和攻击描述均开源，便于审计和合规检查。

**典型接入方式**  
1. **依赖引入**：在项目的构建脚本（如 Maven、Gradle、npm、Cargo）中加入 Wycheproof 对应语言的测试库。  
2. **编写测试**：使用库提供的 `TestVector` 或 `TestCase` 接口，将目标加密库的实现包装为测试对象。  
3. **CI 集成**：在 CI/CD 流水线中执行 `wycheproof` 测试任务，确保每次提交都通过已知攻击向量的校验。  
4. **手动审查**：由于元数据中集成信号稀疏，建议在通过自动化后由安全团队进行一次手动审计，确认测试覆盖范围与业务需求匹配。

**生产可用性**  
- **成熟度**：Medium。适合作为原型、内部工具或预生产环境的安全检查手段。  
- **依赖与维护**：项目最近更新于 2026‑05‑14，活跃度一般；在正式生产前需评估其与所用加密库的兼容性、许可证（Apache 2.0）以及社区维护情况。  
- **上线建议**：在正式部署前完成以下步骤：  
  1. **依赖审计**：确认所有 transitive dependencies 的安全状态。  
  2. **文档对齐**：阅读官方使用指南，确保测试向量覆盖业务使用的算法和参数。  
  3. **发布节奏**：监控项目的发布频率和 issue 处理速度，确保能够及时获取安全补丁。  

总体而言，Wycheproof 是一个高价值的密码学安全检测工具，适合在研发阶段快速验证加密实现的安全性；在生产环境使用时，需要配合手动审查和持续的依赖管理，以确保长期可靠性。

## 🧭 Practical evaluation

**Value:** Project Wycheproof tests crypto libraries against known attacks helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-05-14
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 26/100 |
| quality | 21/100 |
| recency | 20/100 |
| adoption | 0/100 |
| production | 32/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/C2SP/wycheproof) · [← Back to Crypto](./README.md)</sub>
