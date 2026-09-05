# RustCrypto/AEADs

[![Stars](https://img.shields.io/github/stars/RustCrypto/AEADs?style=flat-square&color=yellow)](https://github.com/RustCrypto/AEADs/stargazers) [![Forks](https://img.shields.io/github/forks/RustCrypto/AEADs?style=flat-square&color=blue)](https://github.com/RustCrypto/AEADs/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> Authenticated Encryption with Associated Data Algorithms: high-level encryption ciphers

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 940 |
| 🍴 **Forks** | 196 |
| 💻 **Language** | Rust |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Security

## 📝 Summary

### English

**Brief Summary**  
RustCrypto/AEADs is a Rust library that implements a suite of Authenticated Encryption with Associated Data (AEAD) algorithms, offering high‑level, reusable ciphers for secure data handling. With ~940 ★ on GitHub and active recent commits, it’s a solid choice for prototyping or inspecting blockchain‑related workflows such as Web3 integrations, wallet features, or DeFi services.  

**Value**  
- **Open, auditable implementation** – the source code is fully visible, making it easy to verify cryptographic correctness and to adapt the primitives to custom blockchain protocols.  
- **Rust‑first ergonomics** – leverages Rust’s safety guarantees, zero‑cost abstractions, and seamless async support, which aligns well with modern blockchain node and client development.  
- **Broad algorithm coverage** – includes AES‑GCM, ChaCha20‑Poly1305, XChaCha20‑Poly1305, and others, covering the most common AEAD schemes used in Web3 and decentralized finance.  

**Practical Adoption Path**  
1. **Prototype** – Add the crate to a Cargo.toml, run the built‑in tests, and experiment with the high‑level `encrypt`/`decrypt` APIs in a sandboxed wallet or smart‑contract simulation.  
2. **Security Review** – Perform a manual code audit (focus on nonce handling, key‑material lifecycle, and any `unsafe` blocks) and run fuzzing tools (e.g., cargo‑afl) to confirm resistance to misuse.  
3. **Integration** – Wrap the library in a thin domain‑specific façade (e.g., `Web3Aead`) that enforces your project’s nonce‑generation policy and key‑storage strategy.  
4. **Dependency & Maintenance Check** – Verify that the crate’s transitive dependencies are actively maintained, pin versions, and set up Dependabot/renovate alerts.  

**Production Readiness**  
- **Readiness Level: Medium** – The library is mature enough for internal tools and prototypes, but it lacks extensive production‑grade documentation and formal security certifications.  
- **What to verify before production**:  
  * License compatibility (MIT/Apache‑2.0) with your product.  
  * Ongoing maintainer activity (monitor issue response times and release cadence).  
  * Integration signals – the current metadata is sparse, so you’ll need to write integration tests that mimic real blockchain payloads.  
- **When it’s production‑ready**: after completing the above audit, adding comprehensive integration tests, and establishing a process for timely updates to address any upstream security patches.  

In short, RustCrypto/AEADs provides a high‑quality, Rust‑native cryptographic foundation for Web3 and DeFi projects, suitable for rapid prototyping and, with a modest security‑review effort, for internal production use.

### Русский

**RustCrypto/AEADs** — это набор открытых реализаций алгоритмов Authenticated Encryption with Associated Data, написанных на Rust, который позволяет быстро прототипировать и исследовать блокчейн‑процессы (Web3‑воркфлоу, интеграцию кошельков, DeFi‑фичи) без необходимости писать собственный криптографический код. Проект уже имеет 940 звёзд на GitHub и активные обновления, однако из‑за ограниченной документации о интеграции его рекомендуется использовать в прототипах или внутренних системах после тщательной проверки зависимости, лицензии и безопасности. В продакшн‑среде он может быть применён при условии дополнительного аудита и контроля поддержки.

### 中文

**项目简介（2‑3 句话）**  
RustCrypto/AEADs 是 Rust 生态下的 Authenticated Encryption with Associated Data（AEAD）实现集合，提供高层次、易用的加解密 API。它以安全、可审计的实现细节帮助开发者快速原型化区块链、Web3 与 DeFi 场景中的加密工作流。

**价值**  
- **透明实现**：源码全部开源，便于审计和定制，满足对加密算法可追溯性的合规要求。  
- **快速原型**：提供即插即用的 AEAD 算法（如 AES‑GCM、ChaCha20‑Poly1305），让团队在几行代码内完成钱包、跨链桥、链上数据加密等功能的验证。  
- **生态兼容**：基于 Rust 编写，天然兼容 Rust‑based 区块链框架（Substrate、Solana）以及通过 FFI 调用的其他语言项目。

**典型接入方式**  
1. **依赖声明**  
   ```toml
   [dependencies]
   aead = { git = "https://github.com/RustCrypto/AEADs", tag = "v0.5.0" }
   aes-gcm = "0.10"
   chacha20poly1305 = "0.10"
   ```  
2. **初始化 Cipher**（以 AES‑GCM 为例）  
   ```rust
   use aead::{Aead, NewAead};
   use aes_gcm::Aes256Gcm; // 或者 Aes128Gcm
   use aes_gcm::Key;
   use aes_gcm::Nonce; // 12‑byte nonce

   let key = Key::from_slice(&hex_literal::hex!("000102030405060708090a0b0c0d0e0f"));
   let cipher = Aes256Gcm::new(key);
   let nonce = Nonce::from_slice(&hex_literal::hex!("1a2b3c4d5e6f708090a0b0c0"));
   let ciphertext = cipher.encrypt(nonce, b"payload".as_ref())?;
   let plaintext  = cipher.decrypt(nonce, ciphertext.as_ref())?;
   ```
3. **在业务层封装**：将加密/解密逻辑抽象为统一的 `CryptoService`，供钱包、链下存储或跨链桥调用。

**生产可用性**  
- **成熟度**：项目已有 940+ GitHub Stars、196+ Fork，最近一次提交在 2026‑06‑26，活跃度良好，属于 **Medium** 级别的生产可用性。  
- **适用场景**：非常适合内部原型、测试网或对安全审计要求高的内部工具；在正式生产环境使用前建议：  
  1. **安全审计**：检查所选 AEAD 算法的实现是否符合最新的密码学最佳实践。  
  2. **依赖管理**：锁定具体 tag/commit，防止上游非兼容更新。  
  3. **维护计划**：关注项目的维护者活跃度与安全通报（如 CVE），并准备自行维护或 fork。  
- **风险**：许可证（MIT/Apache‑2.0）需确认符合公司合规；当前元数据中缺少详细的安全审计报告，建议自行进行代码审计后再投入生产。

综上，RustCrypto/AEADs 为 Rust 开发者提供了高质量、易审计的 AEAD 实现，是构建 Web3/区块链加密功能的理想起点，只要在正式上线前完成审计与依赖锁定，即可安全投入生产使用。

## 🧭 Practical evaluation

**Value:** RustCrypto/AEADs helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 940 GitHub stars
- 196 forks
- updated 2026-06-26
- primary language: Rust

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 57/100 |
| stars | 63/100 |
| topics | 0/100 |
| outlook | 62/100 |
| quality | 63/100 |
| recency | 80/100 |
| adoption | 62/100 |
| production | 65/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/RustCrypto/AEADs) · [← Back to Security](./README.md)</sub>
