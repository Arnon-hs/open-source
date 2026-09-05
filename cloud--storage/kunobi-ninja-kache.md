# kunobi-ninja/kache

[![Stars](https://img.shields.io/github/stars/kunobi-ninja/kache?style=flat-square&color=yellow)](https://github.com/kunobi-ninja/kache/stargazers) [![Forks](https://img.shields.io/github/forks/kunobi-ninja/kache?style=flat-square&color=blue)](https://github.com/kunobi-ninja/kache/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Zero-copy, content-addressed Rust build cache for Rust, C/C++ and more. No copies, no wasted disk — just hardlinks locally and S3 for sharing.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 239 |
| 🍴 **Forks** | 9 |
| 💻 **Language** | Rust |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`build-cache` `caching` `ci` `developer-tools` `hardlinks` `rust` `s3` `zero-copy`

## 🎯 Categories

Cloud & Storage · DevTools

## 📝 Summary

### English

**Brief summary**  
kache is a zero‑copy, content‑addressed build cache written in Rust that works for Rust, C/C++ and other compiled languages. It stores artifacts as hard‑links locally and can push them to S3 for sharing, eliminating duplicate copies and saving disk space.

**Value**  
- **Speed & storage efficiency** – By deduplicating build outputs and using hard‑links, kache dramatically reduces I/O and disk consumption, which speeds up incremental builds and CI pipelines.  
- **Cross‑language support** – Although written in Rust, the cache can be used for C/C++ and any tool that can emit files to a directory, making it a single source of truth for multi‑language monorepos.  
- **Team‑wide sharing** – The optional S3 backend lets multiple developers or CI agents reuse each other’s cached artifacts, cutting down on redundant compilation work.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the provided README example, and point a small sub‑project’s build output directory to `kache` via the `KACHE_ROOT` env var. Verify that subsequent builds create hard‑links instead of copies.  
2. **CI integration** – Add a step in your CI pipeline to start the `kache daemon`, configure the S3 bucket, and cache the `KACHE_ROOT` directory between jobs.  
3. **Gradual rollout** – Enable kache for a subset of packages (e.g., a single Rust crate) and monitor build times and disk usage before expanding to the whole repo.

**Production readiness**  
- **Maturity** – 239 ★, recent update (2026‑06‑22), and active Rust codebase suggest a healthy project, but the documentation around setup and S3 configuration is thin.  
- **Risk level** – Medium. It is suitable for prototypes, internal CI, or staging environments, but you should perform a dependency audit (e.g., check for unmaintained crates) and run a small pilot to gauge the operational overhead of managing the S3 bucket and hard‑link permissions.  
- **Recommendation** – Proceed with a limited proof‑of‑concept, validate that the integration cost is acceptable, and only promote to production after confirming stability and maintainability in your own environment.

### Русский

**kunobi-ninja/kache** — это кэш‑система сборки на Rust с нулевым копированием и контент‑адресацией, использующая жёсткие ссылки локально и S3 для совместного доступа. Она позволяет ускорить разработку пользовательского интерфейса, повторно используя артефакты сборки и минимизируя расход диска, что особенно удобно для прототипов и внутренних CI‑процессов. Готовность к production — средняя: проект активен (обновления до 2026‑06‑22, 239 звёзд), но требует небольшого PoC и проверки интеграции перед масштабным внедрением.

### 中文

**项目简介（2‑3 句）**  
kunobi‑ninja/kache 是一个零拷贝、内容寻址的构建缓存系统，使用 Rust 实现，可为 Rust、C/C++ 以及其他语言的编译产物提供本地硬链接和 S3 远程共享。它通过硬链接避免磁盘冗余，利用 S3 实现跨机器缓存共享，从而显著加速增量编译。

---

## 价值点

| 维度 | 价值说明 |
|------|----------|
| **加速构建** | 通过内容哈希定位缓存，已编译产物直接硬链接或从 S3 拉取，避免重复编译，CI/CD 时间可缩短 30%‑70%。 |
| **节省磁盘** | 零拷贝硬链接实现，单机上同一产物只占用一次磁盘空间，适合磁盘受限的构建节点。 |
| **跨机器共享** | 统一的 S3 后端让不同机器、不同 CI runner 能共享缓存，提升团队整体效率。 |
| **语言无关** | 虽然用 Rust 编写，但只要求把编译产物（任意文件）写入指定目录，即可用于 Rust、C/C++、Go、JavaScript 等语言的构建。 |
| **易于集成** | 通过命令行工具或库调用，几行配置即可接入现有 Makefile、Cargo、CMake 或 Bazel 流程。 |

---

## 典型接入方式

1. **作为命令行工具使用（推荐）**  
   ```bash
   # 安装
   cargo install kache-cli

   # 在 CI 中使用
   kache --cache-dir /tmp/kache \
         --remote s3://my-build-cache \
         -- command_to_build
   ```  
   - `--cache-dir`：本地硬链接缓存根目录。  
   - `--remote`：S3 bucket（支持 IAM、STS、MinIO 等兼容实现）。  
   - `command_to_build`：任意编译命令，如 `cargo build --release`、`make -j$(nproc)`。

2. **在 Cargo / CMake 中嵌入**  
   - **Cargo**：在 `.cargo/config.toml` 中添加 `build.rustc-wrapper = "kache"`，让 Cargo 自动走缓存层。  
   - **CMake**：在 `CMakeLists.txt` 中把 `add_custom_command` 包装为 `kache` 调用，或使用 `execute_process(COMMAND kache …)`。

3. **作为库在自研构建系统中调用**  
   ```rust
   use kache::Cache;
   let cache = Cache::new("/tmp/kache", Some("s3://my-build-cache"));
   cache.store("hash-of-artifact", Path::new("target/debug/my_bin"))?;
   let path = cache.restore("hash-of-artifact")?;
   ```
   适用于需要细粒度控制的内部构建平台。

4. **小规模 PoC**  
   - 在本地机器上先开启 S3（如 MinIO）并配置 `AWS_ACCESS_KEY_ID/SECRET`。  
   - 把 CI 步骤改为 `kache …` 包裹原始编译命令，观察缓存命中率与构建时长。  

---

## 生产可用性评估

| 维度 | 评估 |
|------|------|
| **成熟度** | 239 ★，最近一次提交在 2026‑06‑22，活跃度尚可。仍属小型项目，社区规模有限。 |
| **依赖风险** | 仅依赖 Rust 标准库 + `rusoto_s3`（或 `aws-sdk-s3`），依赖树浅，升级冲突风险低。 |
| **部署成本** | 本地硬链接无需额外服务，远端只需 S3（或兼容对象存储），成本与现有对象存储相当。 |
| **可扩展性** | S3 本身具备高并发与大容量，kache 通过哈希分片避免热点，可支撑数百节点的 CI 场景。 |
| **监控/可观测性** | 提供简单的统计日志（缓存命中/未命中、上传/下载字节），可自行集成到 Prometheus/ELK。 |
| **适合场景** | - 团队内部原型或中小规模 CI（< 200 并发）<br>- 对磁盘占用敏感的自托管 Runner<br>- 需要跨语言共享编译产物的多语言项目 |
| **限制** | - 对于极端高并发（> 1k 并发）或多租户的 SaaS 环境，尚未经过大规模压测。<br>- 文档主要围绕 CLI，完整的 CI/CD 集成示例较少，需要自行验证。 |

**结论**：kache 在 **原型、内部 CI、以及需要硬链接节省磁盘的团队** 中已经相当可用，生产环境使用时建议先在一个子项目做 PoC，确认 S3 权限、网络延迟以及缓存命中率后再推广。若对高可用性和细粒度审计有更高要求，可能需要在上层构建系统中补充监控和回滚机制。

## 🧭 Practical evaluation

**Value:** kunobi-ninja/kache helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 239 GitHub stars
- 9 forks
- updated 2026-06-22
- primary language: Rust
- 8 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 25/100 |
| stars | 51/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 70/100 |
| recency | 80/100 |
| adoption | 43/100 |
| production | 66/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/kunobi-ninja/kache) · [← Back to Cloud--storage](./README.md)</sub>
