# trailofbits/mquire

[![Stars](https://img.shields.io/github/stars/trailofbits/mquire?style=flat-square&color=yellow)](https://github.com/trailofbits/mquire/stargazers) [![Forks](https://img.shields.io/github/forks/trailofbits/mquire?style=flat-square&color=blue)](https://github.com/trailofbits/mquire/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> Zero-dependency Linux memory forensics PoC — leverages kernel-embedded BTF and kallsyms for type-aware memory analysis without external debug info.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 162 |
| 🍴 **Forks** | 7 |
| 💻 **Language** | Rust |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`forensics` `kernel` `linux` `memory` `rust` `sql`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`trailofbits/mquire` is a zero‑dependency proof‑of‑concept for Linux memory forensics that uses the kernel’s embedded BTF (BPF Type Format) and kallsyms tables to perform type‑aware analysis of live memory without needing external debug symbols. Written in Rust, the tool can index kernel data structures and expose them to downstream consumers, making internal system knowledge searchable and usable by AI assistants or other tooling.

**Value Proposition**  
- **Searchable internal knowledge** – By extracting rich type information directly from the running kernel, mquire creates a structured knowledge base of system state that can be queried by LLM‑driven assistants, improving answer grounding and reducing hallucinations.  
- **Zero external dependencies** – No need for symbol files, DWARF data, or additional libraries, which simplifies deployment in constrained or hardened environments.  
- **Rust safety & performance** – The language choice offers memory safety guarantees while still delivering the low‑level access required for forensic analysis.

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC) Setup** – Clone the repo, build the binary with `cargo build --release`, and run it on a test Linux host (kernel 5.10+ with BTF enabled). Verify that it can enumerate a few kernel objects (e.g., task structs).  
2. **Integration Layer** – Wrap the CLI output (JSON/NDJSON) in a small service (e.g., a FastAPI or Actix‑web endpoint) that indexes the data into a vector store or search engine (Elastic, Typesense, etc.).  
3. **Assistant Hook** – Extend your LLM‑assistant’s retrieval pipeline to query this index when answering system‑state questions, using the type‑aware data as grounding.  
4. **Iterate & Harden** – Add caching, access‑control, and monitoring; optionally contribute a Dockerfile or CI pipeline to automate reproducible builds.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑06‑27) and has a modest community (≈162 ★). It is suitable for internal prototypes and low‑risk workflows but lacks extensive testing, CI coverage, and clear production‑grade documentation.  
- **Dependencies**: Zero external system libraries, but you must ensure the target kernel has BTF/kallsyms enabled; otherwise the tool will not function.  
- **Maintenance**: Verify compatibility with your kernel version and monitor upstream Rust updates. Adding unit/integration tests and a formal release process would raise the readiness level.  

**Bottom Line**  
mquire offers a compelling way to turn live kernel metadata into searchable knowledge for AI assistants, with a straightforward PoC integration path. It is ready for internal pilots, but production deployment should include additional validation, security hardening, and possibly a thin service layer to manage indexing and access control.

### Русский

Резюме проекта trailofbits/mquire:

trailofbits/mquire - это открытое исходное ядро Linux для анализа памяти, которое позволяет производить типоавторизированный анализ памяти без внешних отладочных данных. Проект предназначен для облегчения поиска внутренней информации и ее использования в качестве базы знаний для ассистентов. trailofbits/mquire подходит для прототипирования и внутренних потоков работы, но требует тщательной проверки зависимостей и поддержки перед выпуском в производство.

### 中文

**简短介绍**  
`trailofbits/mquire` 是一款零依赖的 Linux 内存取证 PoC，利用内核内置的 BTF（BPF Type Format）和 kallsyms，在无需外部调试信息的情况下实现类型感知的内存分析。

---

## 价值说明  

1. **快速定位内部知识**：通过对内核数据结构的精准解析，能够把系统运行时的状态、配置和安全事件映射为结构化信息，帮助 AI 助手在回答安全、运维或故障排查类问题时提供基于真实内存的事实依据。  
2. **降低依赖成本**：不需要额外的 DWARF、ELF 或符号服务器，只要目标机器运行的内核已经开启 BTF，即可直接进行分析，适合离线或受限环境。  
3. **提升检索与推理质量**：将原始内存快照转化为可搜索的结构化索引，使得文档检索、知识库构建和大模型“grounding”更加精准，尤其在安全审计、漏洞复现和取证报告生成场景中价值突出。  

---

## 典型接入方式  

| 步骤 | 说明 | 关键点 |
|------|------|--------|
| 1️⃣ 环境准备 | 在目标 Linux 主机上确认内核已编译 BTF（`/sys/kernel/btf/vmlinux`）并且 `kallsyms` 可读。 | 需要 root 权限或相应的 `CAP_SYS_ADMIN`。 |
| 2️⃣ 编译/获取二进制 | 直接 `cargo build --release` 或下载已发布的二进制包。 | 项目只有 Rust 标准库依赖，编译非常快。 |
| 3️⃣ 运行分析 | `./mquire dump --pid <pid> --out dump.json` 将指定进程的内存以类型信息导出为 JSON/CBOR。 | 支持自定义过滤器和导出格式，便于后续索引。 |
| 4️⃣ 索引入库 | 将导出的结构化数据写入向量数据库（如 Pinecone、Milvus）或全文搜索引擎（Elasticsearch），并在 LLM 提示中加入检索结果。 | 推荐使用统一的 schema（如 `process.memory.{type}.{field}`）保持检索一致性。 |
| 5️⃣ 业务集成 | 在聊天机器人或内部搜索系统的检索层调用上述索引，实现“基于实时内存的答案”。 | 可通过微服务包装为 REST / gRPC 接口，供多语言客户端调用。 |

*示例微服务（Rust + Actix）*  
```rust
#[post("/analyze")]
async fn analyze(req: Json<AnalyzeReq>) -> impl Responder {
    let dump = mquire::dump_process(req.pid)?;
    let indexed = indexer::store(dump).await?;
    HttpResponse::Ok().json(indexed)
}
```
这样即可把 `mquire` 的功能封装为统一的 HTTP API，供现有平台直接调用。

---

## 生产可用性评估  

| 维度 | 现状 | 备注 |
|------|------|------|
| **成熟度** | 58/100（中等） | 项目活跃，最近一次提交在 2026‑06‑27，星标 162，Fork 7，代码量小且依赖仅 Rust 标准库。 |
| **依赖风险** | 低 | 零外部库，唯一依赖是内核 BTF/kallsyms，需确保目标机器内核兼容。 |
| **可维护性** | 中等 | 代码简洁，Rust 社区维护良好，但项目维护者为单一团队，长期支持需自行监控。 |
| **安全审计** | 待评估 | 由于直接读取内核内存，建议在受信任环境下运行，并进行二次审计（如审查 `unsafe` 使用）。 |
| **部署成本** | 低至中等 | 编译/下载即得二进制，运行时仅需 root 权限；若做为微服务部署，需要额外的容器化或 CI/CD 流程。 |
| **适用场景** | 原型、内部工具、取证实验 | 对实时性要求不高的场景（如离线取证、周期性审计）非常适合；在高并发线上服务中直接使用需评估性能影响。 |

**结论**：`mquire` 具备快速把内核内存转化为结构化、可检索数据的能力，能够显著提升 AI 助手在安全与运维领域的答案可靠性。对于内部原型或取证工作流，直接以二进制或容器方式接入即可；在生产环境使用前，建议完成以下步骤：

1. **安全审计**：确认 `unsafe` 代码块不会导致内存泄露或特权提升。  
2. **兼容性测试**：在所有目标内核版本上验证 BTF/kallsyms 可用性。  
3. **监控与限流**：为防止大规模内存 dump 影响系统性能，加入调用频率和资源使用限制。  

完成上述准备后，`mquire` 完全可以作为内部知识索引与 LLM “grounding” 的可靠数据源投入生产使用。

## 🧭 Practical evaluation

**Value:** trailofbits/mquire helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 162 GitHub stars
- 7 forks
- updated 2026-06-27
- primary language: Rust
- 6 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 23/100 |
| stars | 47/100 |
| topics | 75/100 |
| outlook | 67/100 |
| quality | 64/100 |
| recency | 80/100 |
| adoption | 40/100 |
| production | 64/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/trailofbits/mquire) · [← Back to Misc](./README.md)</sub>
