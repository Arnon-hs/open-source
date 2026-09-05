# 01mf02/jaq

[![Stars](https://img.shields.io/github/stars/01mf02/jaq?style=flat-square&color=yellow)](https://github.com/01mf02/jaq/stargazers) [![Forks](https://img.shields.io/github/forks/01mf02/jaq?style=flat-square&color=blue)](https://github.com/01mf02/jaq/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> A jq clone focussed on correctness, speed, and simplicity

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.7k |
| 🍴 **Forks** | 115 |
| 💻 **Language** | Rust |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`jq` `json` `query` `rust`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`01mf02/jaq` is an open‑source, Rust‑based reimplementation of the popular `jq` JSON processor that prioritises correctness, speed, and a minimal codebase. With over 3,600 stars and active maintenance, it offers a lightweight alternative for developers who need fast, reliable JSON querying without the overhead of the original `jq`. Its simple design makes it attractive for prototypes, internal tooling, or any workflow where a fast, dependable JSON processor is required.

**Value**  
- **Performance & correctness**: Written in Rust, `jaq` delivers near‑native speed while guaranteeing strict JSON handling, which can reduce runtime latency in data‑intensive pipelines.  
- **Simplicity**: The codebase is intentionally small, easing auditability, customization, and security reviews compared with the more complex C implementation of `jq`.  
- **Community traction**: A solid star count and recent commits indicate a healthy user base and ongoing development, lowering the risk of abandonment.

**Practical Adoption Path**  
1. **Proof‑of‑concept**: Clone the repo, run the provided examples, and replace a few `jq` calls in a sandbox script to verify feature parity for your specific queries.  
2. **Readme & documentation check**: Confirm that the supported syntax covers the needed filters; if gaps exist, evaluate the effort to extend the parser (Rust makes this relatively straightforward).  
3. **Integration testing**: Add `jaq` as a binary dependency in your CI pipeline, run regression tests against existing JSON processing outputs, and measure performance gains.  
4. **Gradual rollout**: Deploy the binary to a staging environment, monitor error rates and resource usage, then promote to production once confidence is established.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last update 2026‑06‑25) and has a sizable user community, making it suitable for prototypes and internal workflows.  
- **Dependencies**: Single‑binary Rust executable, which simplifies packaging and reduces external library risk.  
- **Considerations before production**: Verify that the command‑line interface and supported filter set meet all use cases, conduct a security audit of the compiled binary, and establish a process for tracking upstream updates. With these checks in place, `jaq` can be safely promoted to production for JSON processing tasks.

### Русский

**01mf02/jaq** — это лёгкий клон `jq`, написанный на Rust и ориентированный на корректность, скорость и простоту использования. Он подходит для быстрого прототипирования или внутренних пайплайнов, где требуется надёжный JSON‑парсер без лишних зависимостей; рекомендуется начать с небольшого proof‑of‑concept, проверив README и актуальность репозитория. Уровень готовности — средний: проект имеет значительное сообщество (≈3,6 k звёзд) и активные обновления, но перед выводом в продакшн следует оценить затраты на интеграцию и поддержание зависимости.

### 中文

**项目简介**  
`01mf02/jaq` 是用 Rust 编写的 jq 克隆实现，强调 **正确性、运行速度和代码简洁**。它兼容大多数 jq 语法，适合作为轻量级的 JSON 处理工具。

**价值**  
- **高性能**：基于 Rust 的零成本抽象，使得大文件或高并发场景下的 JSON 过滤、转换比传统 jq 更快。  
- **安全可靠**：编译时即捕获内存安全问题，避免了 jq 常见的崩溃风险。  
- **易于部署**：单二进制文件，无需外部解释器或库，适合容器化、CI/CD 流水线或嵌入式环境。

**典型接入方式**  
1. **命令行直接使用**：在 CI 步骤或脚本中将 `jaq` 替换为 `jq`，语法基本保持一致。  
2. **作为库调用**：在 Rust 项目中通过 `jaq-core`/`jaq-interpret` crates 引入，利用其 API 在程序内部执行 JSON 查询。  
3. **容器镜像**：使用官方提供的 `Dockerfile` 或自行构建轻量镜像（仅 ~10 MB），在 Kubernetes Job、GitHub Actions 等环境中运行。

**生产可用性**  
- **成熟度**：已有 3.6k+ 星、115+ fork，活跃维护至 2026‑06‑25，社区对其正确性和性能有一定认可。  
- **适用场景**：原型开发、内部数据处理流水线、日志聚合、微服务间的 JSON 转换等。  
- **风险与准备**：  
  - 需要先验证其与现有 jq 脚本的兼容性（尤其是较为边缘的扩展函数）。  
  - 在生产环境部署前，做好二进制的 SHA256 校验和版本锁定，防止意外升级。  
  - 对于关键业务，建议在预上线环境进行性能基准测试，并监控内存/CPU 使用情况。  

综上，`jaq` 在对性能和安全有要求且对 jq 兼容性需求不极端的内部或原型项目中，是一个 **中等风险、易于集成、可在生产环境使用** 的选择。

## 🧭 Practical evaluation

**Value:** 01mf02/jaq may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 3660 GitHub stars
- 115 forks
- updated 2026-06-25
- primary language: Rust
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 52/100 |
| stars | 76/100 |
| topics | 50/100 |
| outlook | 69/100 |
| quality | 74/100 |
| recency | 80/100 |
| adoption | 69/100 |
| production | 67/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/01mf02/jaq) · [← Back to Misc](./README.md)</sub>
