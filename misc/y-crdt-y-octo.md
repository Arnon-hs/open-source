# y-crdt/y-octo

[![Stars](https://img.shields.io/github/stars/y-crdt/y-octo?style=flat-square&color=yellow)](https://github.com/y-crdt/y-octo/stargazers) [![Forks](https://img.shields.io/github/forks/y-crdt/y-octo?style=flat-square&color=blue)](https://github.com/y-crdt/y-octo/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-48%2F100-brightgreen?style=flat-square)](#)

> CRDT implementation which is compatible with https://github.com/yjs/yjs

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 329 |
| 🍴 **Forks** | 10 |
| 💻 **Language** | Rust |
| 📈 **Score** | 48/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`crdt-algorithm` `crdt-implementations` `crdts` `thread-safe`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
y‑crdt / y‑octo is a Rust implementation of Conflict‑Free Replicated Data Types (CRDTs) that aims to be compatible with the popular JavaScript library [yjs](https://github.com/yjs/yjs). With over 300 GitHub stars and recent activity, it offers a native‑Rust alternative for projects that need deterministic, offline‑first data synchronization across distributed clients.

**Value**  
- **Language‑native performance** – By providing the same CRDT model as yjs in Rust, it lets backend services, embedded systems, or WebAssembly targets avoid costly language bridges while preserving yjs‑compatible semantics.  
- **Ecosystem alignment** – Compatibility with yjs means existing yjs‑based front‑ends can interoperate with a Rust backend without rewriting conflict‑resolution logic, accelerating full‑stack collaborative applications.  
- **Open‑source transparency** – The codebase is modest in size, well‑documented, and licensed permissively, making it easy to audit for security or compliance requirements.

**Practical Adoption Path**  
1. **Read the README & run the example** – Verify that the API surface matches the yjs features you need (e.g., shared maps, arrays, text).  
2. **Proof‑of‑concept** – Build a small prototype that syncs a Rust service with a yjs client (e.g., a collaborative text editor) to confirm wire‑format compatibility and latency expectations.  
3. **Integration scaffolding** – Wrap the CRDT library in a thin service layer (REST, gRPC, or WebSocket) that exposes the same message protocol yjs uses, then replace the prototype with your production code.  
4. **Testing & monitoring** – Add unit tests for merge scenarios and instrument conflict‑resolution events to ensure deterministic behavior under real‑world network partitions.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last update 2026‑06‑30) and has a modest but healthy community (≈330 stars, 10 forks).  
- **Suitability**: Ideal for prototypes, internal tools, or services where Rust’s performance and safety are critical.  
- **Considerations before production**:  
  * Perform a license audit (the repository’s license must align with your policy).  
  * Conduct a security review of dependencies and the CRDT merge logic.  
  * Evaluate the maintainer activity and issue response time to gauge long‑term support.  
  * Set up CI/CD pipelines that include fuzzing or property‑based testing for CRDT consistency.

In summary, y‑crdt / y‑octo offers a compelling Rust‑native bridge to the yjs ecosystem, making it a practical choice for teams that need high‑performance collaborative data structures. Start with a small proof‑of‑concept, verify compatibility, and perform the standard security and maintenance checks before promoting it to production workloads.

### Русский

**y-crdt/y-octo** — это Rust‑реализация CRDT, полностью совместимая с библиотекой Yjs, что позволяет использовать её в проектах, где уже применяются Yjs‑клиенты (например, совместные редакторы, чат‑приложения и синхронные доски). Для внедрения рекомендуется начать с небольшого proof‑of‑concept, проверив README и проведя базовую проверку зависимостей, после чего можно расширять интеграцию в прототипы или внутренние сервисы. Уровень готовности — средний: проект имеет 329 звёзд и активные обновления, но перед выпуском в продакшн стоит уточнить лицензирование, безопасность и наличие активных мейнтейнеров.

### 中文

**项目简介**  
y-crdt/y-octo 是一个用 Rust 实现的 CRDT（冲突自由复制数据类型）库，遵循并兼容 Yjs（https://github.com/yjs/yjs）的协议和数据模型，方便在 Rust 后端与前端 Yjs 应用之间进行无缝同步。

**价值**  
- **跨语言协同**：在 Rust 服务端直接使用与 Yjs 前端相同的 CRDT，实现端到端的实时协作而无需额外的转译层。  
- **高性能**：得益于 Rust 的零成本抽象和所有权系统，提供比纯 JavaScript 实现更低的延迟和内存占用。  
- **生态兼容**：遵循 Yjs 协议，现有基于 Yjs 的编辑器、白板等前端项目可以直接接入，无需改动业务逻辑。

**典型接入方式**  
1. **阅读 README**：确认库的 API（如 `OctoDoc`, `OctoArray`）与 Yjs 文档对应的对象相匹配。  
2. **在 Cargo.toml 中添加依赖**：  
   ```toml
   [dependencies]
   y-octo = "0.3"
   ```  
3. **在服务端创建 CRDT 实例并通过 WebSocket/WS‑RPC 与前端 Yjs 客户端同步**：  
   ```rust
   use y_octo::{OctoDoc, OctoSync};

   let mut doc = OctoDoc::new();
   // 处理来自前端的 update 消息
   let sync = OctoSync::new(&mut doc);
   sync.apply_update(update_from_client);
   // 将本地更新发送给前端
   let update = sync.encode_update();
   ```  
4. **进行小规模 PoC**：先在单机或测试环境中跑通一次完整的更新-同步循环，验证兼容性与性能。  

**生产可用性**  
- **成熟度**：已有 329 ⭐、10+ Fork，最近一次更新（2026‑06‑30）显示仍在维护，适合作为原型或内部业务的同步层。  
- **风险**：需自行审查许可证（MIT/Apache）以及安全审计报告，确保依赖链无已知漏洞；若计划长期生产使用，建议监控维护者活跃度并做好 fallback 方案（如在关键时刻切换到官方 Yjs Server）。  
- **推荐场景**：原型验证、内部协作工具、需要 Rust 高性能后端的实时编辑系统。对外部高并发、严格 SLA 的生产环境，建议在充分的压力测试和安全评估后再投入。

## 🧭 Practical evaluation

**Value:** y-crdt/y-octo may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 329 GitHub stars
- 10 forks
- updated 2026-06-30
- primary language: Rust
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 26/100 |
| stars | 54/100 |
| topics | 50/100 |
| outlook | 49/100 |
| quality | 53/100 |
| recency | 40/100 |
| adoption | 46/100 |
| production | 52/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/y-crdt/y-octo) · [← Back to Misc](./README.md)</sub>
