# rustls/rustls-native-certs

[![Stars](https://img.shields.io/github/stars/rustls/rustls-native-certs?style=flat-square&color=yellow)](https://github.com/rustls/rustls-native-certs/stargazers) [![Forks](https://img.shields.io/github/forks/rustls/rustls-native-certs?style=flat-square&color=blue)](https://github.com/rustls/rustls-native-certs/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-48%2F100-brightgreen?style=flat-square)](#)

> Integration with OS certificate stores for rustls

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 240 |
| 🍴 **Forks** | 71 |
| 💻 **Language** | Rust |
| 📈 **Score** | 48/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`rust` `tls`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`rustls/rustls-native-certs` provides a thin wrapper that lets the Rust‑native TLS library **rustls** discover and use the operating system’s trusted root certificate store (Windows, macOS, Linux). With a modest codebase (≈240 ★, 71 forks) and recent activity (last commit 2026‑06‑29), it fills the gap between rustls’s “no‑std” security model and the need to trust system‑wide CAs without bundling them manually.

**Value**  
- **Seamless OS integration** – eliminates the need to ship or maintain a separate root‑store file; the library automatically loads the platform’s native roots, keeping your TLS verification in sync with system updates.  
- **Small, focused dependency** – adds only a single crate to your Cargo.toml, keeping the attack surface minimal while preserving rustls’s performance and safety guarantees.  
- **Cross‑platform support** – works on the three major desktop/server OSes, making it a portable solution for CLI tools, micro‑services, and internal utilities.

**Practical Adoption Path**  
1. **Add the crate**: `cargo add rustls-native-certs`.  
2. **Load the roots** in your rustls client configuration:  
   ```rust
   let mut root_store = rustls::RootCertStore::empty();
   rustls_native_certs::load_native_certs(&mut root_store)
       .expect("could not load platform roots");
   let client_config = rustls::ClientConfig::builder()
       .with_safe_defaults()
       .with_root_certificates(root_store)
       .with_no_client_auth();
   ```  
3. **Test on each target OS** – verify that the expected system roots are loaded (e.g., by printing a few subject names).  
4. **Lock the version** in `Cargo.lock` and optionally audit the crate with `cargo audit` to ensure no known vulnerabilities.

**Production Readiness**  
- **Maturity**: Medium. The crate is actively maintained and compiles cleanly on recent Rust toolchains, but the integration surface is thin, so you’ll need to confirm that the automatic loading behaves as expected in your deployment environment (especially in containerized or minimal OS images).  
- **Risk Mitigation**:  
  * Run integration tests on all supported platforms.  
  * Pin the crate version and monitor its repository for breaking changes.  
  * If you need deterministic trust anchors (e.g., compliance), consider supplementing the native store with a static bundle.  

Overall, `rustls-native-certs` is a solid choice for prototypes, internal services, or any Rust application that wants rustls’s security without the overhead of managing its own CA bundle, provided you perform the modest validation steps outlined above before promoting it to production.

### Русский

Резюме проекта rustls/rustls-native-certs:

rustls/rustls-native-certs - это открытый исходный проект, который обеспечивает интеграцию с сертификатными хранилищами операционной системы для библиотеки rustls. Этот проект может быть полезен при реализации конкретного рабочего процесса, если README и активность проекта соответствуют ему. rustls/rustls-native-certs готов к использованию в прототипах или внутренних рабочих процессах, но требует тщательного отслеживания зависимостей и поддержки перед использованием в производственной среде.

### 中文

**项目简介（2‑3 句）**  
`rustls/rustls-native-certs` 为 Rust 的 TLS 库 **rustls** 提供对操作系统根证书库的无缝访问，使得 rustls 能够直接使用系统已信任的 CA 证书，而无需手动维护 PEM 文件。它通过平台特定实现（Windows CryptoAPI、macOS Security.framework、Linux OpenSSL 或 cert‑store）在运行时动态加载本地根证书。

**价值**  
- **免维护根证书**：利用操作系统自带的根证书，省去在容器或二进制中打包、更新 PEM 的工作。  
- **安全性与合规**：系统根证书会随 OS 安全更新自动刷新，保持最新的信任链。  
- **开发便利**：在本地开发、测试以及内部原型时，只需加一行依赖即可让 rustls 与系统证书保持一致，避免 “自签名证书不受信任” 的调试噩梦。

**典型接入方式**  

```toml
# Cargo.toml
[dependencies]
rustls = "0.23"
rustls-native-certs = "0.7"
```

```rust
use rustls::{ClientConfig, OwnedTrustAnchor};
use rustls_native_certs::load_native_certs;

fn make_client_config() -> Result<ClientConfig, Box<dyn std::error::Error>> {
    // 从操作系统加载根证书
    let mut root_store = rustls::RootCertStore::empty();
    for cert in load_native_certs()? {
        root_store.add(cert)?;
    }

    // 构造 rustls 客户端配置
    let config = ClientConfig::builder()
        .with_safe_defaults()
        .with_root_certificates(root_store)
        .with_no_client_auth(); // 根据实际需求选择

    Ok(config)
}
```

- **平台兼容**：库内部会在 `cfg` 条件编译下选择对应实现，使用者无需关心细节。  
- **可选特性**：如果项目只在某个平台运行，可以通过 `default-features = false` 并显式启用 `windows`, `macos`, `linux` 等特性来减小二进制体积。

**生产可用性**  
- **成熟度**：240 Stars、71 Forks，最近一次提交在 2026‑06‑29，活跃度尚可。  
- **适用场景**：适合内部服务、原型以及需要快速对接系统根证书的生产服务。  
- **风险与注意事项**  
  1. **依赖平台实现**：在极简容器或自定义 Linux 镜像中，系统根证书可能缺失或路径不同，需要提前确认镜像中已安装 `ca-certificates` 包。  
  2. **错误处理**：`load_native_certs()` 可能返回空集合（如 Windows 服务账户没有访问权限），生产代码应做好回退或显式错误日志。  
  3. **升级影响**：操作系统更新可能带来根证书的增删，建议在 CI 中加入 `rustls-native-certs` 的集成测试，确保在不同 OS 版本下仍能成功建立 TLS 连接。  

综合来看，`rustls-native-certs` 在 **中等** 生产就绪度（Medium）——对原型和内部系统非常友好，只要在部署环境确认根证书可用并做好异常处理，即可安全投入生产。

## 🧭 Practical evaluation

**Value:** rustls/rustls-native-certs may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 240 GitHub stars
- 71 forks
- updated 2026-06-29
- primary language: Rust
- 2 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 46/100 |
| stars | 51/100 |
| topics | 25/100 |
| outlook | 50/100 |
| quality | 51/100 |
| recency | 40/100 |
| adoption | 49/100 |
| production | 49/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/rustls/rustls-native-certs) · [← Back to Misc](./README.md)</sub>
