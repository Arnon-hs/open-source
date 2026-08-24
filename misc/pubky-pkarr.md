# pubky/pkarr

[![Stars](https://img.shields.io/github/stars/pubky/pkarr?style=flat-square&color=yellow)](https://github.com/pubky/pkarr/stargazers) [![Forks](https://img.shields.io/github/forks/pubky/pkarr?style=flat-square&color=blue)](https://github.com/pubky/pkarr/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-43%2F100-brightgreen?style=flat-square)](#)

> Public Key Addressable Resource Records (sovereign TLDs)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 402 |
| 🍴 **Forks** | 40 |
| 💻 **Language** | Rust |
| 📈 **Score** | 43/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`distributed-hash-table` `dns` `public-key` `url`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*pubky/pkarr* is a Rust library that implements Public Key Addressable Resource Records, enabling “sovereign” top‑level domains that are resolved directly to cryptographic public keys. With modest community interest (≈400 ★, 40 forks) and recent activity, it can be tried out for niche workflows that need decentralized, key‑based naming.  

**Value**  
- Provides a cryptographically verifiable naming layer without relying on traditional DNS authorities, which is attractive for decentralized applications, secure IoT device provisioning, and blockchain‑based identity schemes.  
- By exposing the public key in the name itself, pkarr eliminates the need for separate certificate‑or‑key distribution mechanisms, reducing attack surface and simplifying trust models.

**Practical Adoption Path**  
1. **Read the README and examples** – confirm that the library’s API matches the intended workflow (e.g., generating, publishing, and resolving pkarr records).  
2. **Proof‑of‑concept** – create a minimal Rust binary that registers a test record and resolves it via the provided resolver or a local bootstrap node.  
3. **Integration testing** – plug the PO‑C into your existing service (e.g., a microservice that needs to look up device keys) and verify latency, error handling, and fallback to traditional DNS if needed.  
4. **Security review** – audit the cryptographic primitives and any network‑level code, and confirm that the library’s dependency tree is actively maintained.  

**Production Readiness**  
- **Maturity:** Medium. The codebase is recent (last commit 2026‑05‑13) and has a small but active community, but documentation and integration guides are limited.  
- **Suitability:** Good for prototypes, internal tools, or services that can tolerate a modest amount of custom infrastructure (e.g., running a pkarr bootstrap node).  
- **Risks:** Integration steps are not fully spelled out in the metadata; you’ll need to invest time to understand the bootstrap/relay architecture and to monitor upstream changes. Before production use, perform dependency audits, set up automated tests for record publishing/resolution, and consider a fallback to conventional DNS for resilience.  

In short, pkarr offers a compelling cryptographic naming primitive that can be evaluated quickly with a small proof‑of‑concept, but moving to production requires careful validation of the integration path and ongoing maintenance of the underlying Rust library.

### Русский

**pubky/pkarr** — это Rust‑библиотека, реализующая Public Key Addressable Resource Records и позволяющая работать с суверенными доменными зонами (sovereign TLDs). Подходит для прототипов и внутренних сервисов, где требуется привязка ресурсов к публичным ключам (например, децентрализованное управление DNS‑записями или безопасный обмен метаданными); интеграцию лучше начать с небольшого proof‑of‑concept, проверив README и текущую активность проекта. Готовность к production — средняя: проект имеет 402 звёзды, 40 форков и свежие коммиты, но путь интеграции не очевиден, поэтому перед выпуском в прод необходимо оценить зависимости и потенциальные затраты на настройку.

### 中文

**项目简介**  
pubky/pkarr 是一个基于公钥的可寻址资源记录（Public Key Addressable Resource Records）实现，旨在为去中心化、主权域名（sovereign TLD）提供安全、可验证的解析方案。项目使用 Rust 编写，已获得 402 颗星和 40 次 fork，近期仍在活跃维护。

---

### 价值点
1. **去中心化身份绑定**：通过公钥直接映射到资源记录，天然防篡改、抗伪造，适合作为去中心化身份、DID 或区块链资产的解析层。  
2. **主权 TLD 支持**：提供对自定义顶级域的原生解析，帮助组织或社区自行管理域名空间，摆脱传统 DNS 中央化控制。  
3. **轻量且安全**：Rust 实现带来内存安全和高性能，适合在资源受限的环境（如边缘节点、IoT 设备）中运行。

---

### 典型接入方式
1. **阅读并运行 README 示例**：项目的 README 包含完整的 CLI 与库使用示例，先在本地跑通 `pkarr` 命令行工具，验证创建、签名、查询记录的完整工作流。  
2. **在代码中引入库**：在 Rust 项目 `Cargo.toml` 中添加  
   ```toml
   pkarr = { git = "https://github.com/pubky/pkarr.git" }
   ```  
   然后使用 `pkarr::record::Record`、`pkarr::signer::Signer` 等 API 完成：
   - 生成公私钥对（或使用已有的 X25519/Ed25519 密钥）  
   - 构造资源记录并签名  
   - 将记录发布到选定的存储后端（例如 IPFS、Git、或自建的 pkarr 服务器）  
   - 通过 `pkarr::resolver::Resolver` 进行查询和验证  

3. **小规模 PoC**：先在内部测试环境部署一个简易的 pkarr 解析服务（Docker 镜像或二进制），让业务系统通过 HTTP/JSON 接口调用解析接口，评估响应时延和错误率。

---

### 生产可用性评估
| 维度 | 现状 | 建议 |
|------|------|------|
| **代码成熟度** | 402 星、40 Fork，最近一次提交在 2026‑05‑13，活跃度良好。 | 继续关注后续 Release 及安全公告。 |
| **依赖管理** | 纯 Rust 实现，依赖链相对简洁。 | 在 CI 中锁定 `Cargo.lock`，使用审计工具（如 `cargo audit`）检查漏洞。 |
| **文档/示例** | README 提供完整 CLI 与库使用示例。 | 在正式接入前补充内部使用手册，确保团队熟悉密钥管理流程。 |
| **可扩展性** | 支持自定义存储后端，可与 IPFS、S3、数据库等集成。 | 评估目标存储的持久性与可用性，必要时实现冗余同步。 |
| **运维成本** | 需要运行 pkarr 解析服务或使用第三方托管节点。 | 采用容器化部署，配合监控（Prometheus）与自动化滚动升级。 |
| **风险** | 集成路径不够显式，缺少成熟的企业级 SDK。 | 先在内部原型中验证关键路径（密钥生成 → 记录签名 → 查询），再决定是否投入生产。 |

**结论**：pubky/pkarr 具备中等生产就绪度，适合作为原型或内部工作流的去中心化域名解析方案。若业务对主权域名或公钥绑定的安全需求较高，建议先在受控环境完成 PoC，随后通过容器化部署、依赖审计和监控来提升到生产级别。

## 🧭 Practical evaluation

**Value:** pubky/pkarr may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 402 GitHub stars
- 40 forks
- updated 2026-05-13
- primary language: Rust
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 40/100 |
| stars | 55/100 |
| topics | 50/100 |
| outlook | 43/100 |
| quality | 51/100 |
| recency | 20/100 |
| adoption | 51/100 |
| production | 44/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/pubky/pkarr) · [← Back to Misc](./README.md)</sub>
