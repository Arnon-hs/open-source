# iqlusioninc/yubikey.rs

[![Stars](https://img.shields.io/github/stars/iqlusioninc/yubikey.rs?style=flat-square&color=yellow)](https://github.com/iqlusioninc/yubikey.rs/stargazers) [![Forks](https://img.shields.io/github/forks/iqlusioninc/yubikey.rs?style=flat-square&color=blue)](https://github.com/iqlusioninc/yubikey.rs/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> Pure Rust YubiKey host-side driver for PIV-based RSA/ECC key storage + signing/encryption support

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 261 |
| 🍴 **Forks** | 54 |
| 💻 **Language** | Rust |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Knowledge/RAG · AI/ML · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`iqlusioninc/yubikey.rs` is a pure‑Rust library that implements a host‑side driver for YubiKey devices, exposing the PIV (Personal Identity Verification) interface for secure RSA/ECC key storage, signing, and encryption. It lets Rust applications interact with YubiKeys without native bindings or external tools, making hardware‑backed cryptography easy to integrate.

**Value Proposition**  
- **Secure, hardware‑backed crypto**: By leveraging YubiKey’s tamper‑resistant key storage, developers can off‑load private‑key operations to a physical token, reducing the attack surface of their services.  
- **Pure‑Rust implementation**: No C/FFI dependencies, which simplifies cross‑platform builds, improves safety, and aligns with Rust’s ecosystem and tooling.  
- **Open‑source and actively maintained**: 260+ stars and recent commits indicate community interest and ongoing development, making it a reliable source of up‑to‑date PIV support.

**Practical Adoption Path**  
1. **Evaluate Compatibility** – Verify that the target YubiKey models support the PIV applet (most modern YubiKeys do).  
2. **Add the crate** – Include `yubikey` in `Cargo.toml` and run `cargo build` to ensure the dependency resolves cleanly with your existing stack.  
3. **Prototype** – Use the library’s high‑level API to generate a test key, perform a sign/verify cycle, and confirm that the YubiKey is correctly enumerated on your development platform (Linux/macOS/Windows).  
4. **Integrate with Existing Workflows** – Replace software‑only key handling with calls to `yubikey::piv::sign`, `decrypt`, or `generate_key`. Wrap these calls behind an internal trait if you need to support fallback software keys.  
5. **Security Review & Testing** – Perform functional tests (including PIN/PUK handling, retry limits, and error paths) and run a threat model review to ensure the YubiKey usage meets your compliance requirements.  

**Production Readiness**  
- **Maturity**: Medium. The crate is functional and used in several open‑source projects, but the integration documentation is lightweight, so a small amount of engineering effort is needed to handle device discovery, PIN management, and error handling robustly.  
- **Dependencies & Maintenance**: Pure Rust with no external native libraries, which simplifies deployment. However, keep an eye on upstream updates (e.g., changes to the YubiKey firmware or PIV spec) and pin the crate version to avoid accidental breaking changes.  
- **Risk Mitigation**: Conduct a pilot deployment in a staging environment, validate the operational cost of provisioning YubiKeys (inventory, user PIN enrollment, lifecycle management), and implement monitoring for device availability and authentication failures.  

Overall, `yubikey.rs` is a solid building block for adding hardware‑rooted cryptography to Rust services, suitable for prototypes and internal tools, and with modest engineering effort can be hardened for production use.

### Русский

**iqlusioninc/yubikey.rs** — это полностью написанный на Rust драйвер для YubiKey, позволяющий использовать PIV‑модуль устройства как хранилище RSA/ECC ключей и выполнять операции подписи и шифрования. Он подходит для прототипов и внутренних сервисов, где требуется безопасное управление криптографическими материалами без зависимости от сторонних бинарных библиотек; однако перед выводом в продакшн следует проверить совместимость со своей инфраструктурой и оценить затраты на настройку, так как путь интеграции из метаданных не очевиден. При надлежащей проверке проект считается готовым к использованию в средах со средним уровнем требований к надёжности.

### 中文

**项目简介（2‑3 句）**  
iqlusioninc/yubikey.rs 是用纯 Rust 编写的 YubiKey 主机端驱动，专注于基于 PIV（Personal Identity Verification）协议的 RSA 与 ECC 密钥存储，并提供签名、加密等常用密码操作。它无需依赖外部 C 库，天然兼容 Rust 生态，可直接在安全敏感的服务或工具中使用硬件密钥。

**价值**  
- **安全性提升**：所有私钥永远留在 YubiKey 中，防止泄露或被恶意软件窃取。  
- **Rust 原生体验**：完全基于 Rust 实现，拥有所有权、生命周期等安全特性，易于在现有 Rust 项目中集成。  
- **跨平台支持**：通过 libusb / PC/SC 抽象层，支持 Linux、macOS、Windows，适合多平台部署。  
- **开源透明**：代码公开、社区活跃（260+ Stars），便于审计和二次定制。

**典型接入方式**  
1. **依赖添加**：在 `Cargo.toml` 中加入  
   ```toml
   yubikey = { git = "https://github.com/iqlusioninc/yubikey.rs", tag = "v0.8.0" }
   ```  
2. **初始化设备**  
   ```rust
   use yubikey::piv::{self, PinPolicy};

   // 自动发现并打开第一个 YubiKey
   let mut yubikey = yubikey::YubiKey::open()?;
   let mut piv = yubikey.piv()?;
   ```
3. **使用密钥**（以 RSA 签名为例）  
   ```rust
   let key = piv.get_private_key(piv::SlotId::Authentication)?;
   let signature = key.sign(piv::AlgorithmId::Rsa2048, b"message")?;
   ```
4. **错误处理 & PIN 管理**：库提供 `PinPolicy`、`TouchPolicy`，可在创建/使用密钥时指定，需要时调用 `piv.verify_pin(pin)`。

**生产可用性**  
- **成熟度**：项目已有 260+ Stars、50+ Fork，活跃维护至 2026‑05‑11，代码质量和文档基本达标。  
- **适用场景**：内部服务的代码签名、TLS 客户端证书、加密邮件、CI/CD 密钥管理等原型或内部业务。  
- **风险与注意事项**  
  - **集成成本**：需要确保运行环境具备 libusb/PCSC 驱动，且在容器或 CI 环境中可能需要额外的设备映射或权限配置。  
  - **依赖审计**：虽然纯 Rust，仍依赖 `rusb`、`pcsc` 等底层库，需检查其安全更新情况。  
  - **运维**：硬件钥匙的物理管理（插拔、PIN/PUK 更换）需制定相应 SOP，避免因设备不可用导致服务中断。  
- **就绪度**：**中等**。适合作为原型或内部系统的安全加固方案，投入生产前建议进行一次完整的集成测试、依赖审计以及故障恢复演练。  

总之，yubikey.rs 为 Rust 项目提供了一条简洁、可靠的硬件根信任路径，只要做好环境准备和运维流程，即可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** iqlusioninc/yubikey.rs helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 261 GitHub stars
- 54 forks
- updated 2026-05-11
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 51/100 |
| topics | 0/100 |
| outlook | 69/100 |
| quality | 62/100 |
| recency | 100/100 |
| adoption | 49/100 |
| production | 68/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/iqlusioninc/yubikey.rs) · [← Back to Knowledgerag](./README.md)</sub>
