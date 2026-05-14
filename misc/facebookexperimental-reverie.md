# facebookexperimental/reverie

[![Stars](https://img.shields.io/github/stars/facebookexperimental/reverie?style=flat-square&color=yellow)](https://github.com/facebookexperimental/reverie/stargazers) [![Forks](https://img.shields.io/github/forks/facebookexperimental/reverie?style=flat-square&color=blue)](https://github.com/facebookexperimental/reverie/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> An ergonomic and safe syscall interception framework for Linux.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 824 |
| 🍴 **Forks** | 41 |
| 💻 **Language** | Rust |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary**  
Reverie is an ergonomic, safety‑focused framework for intercepting Linux syscalls, written in Rust. It lets developers hook, monitor, and modify system calls without kernel patches, making it useful for debugging, sandboxing, and building custom runtime policies.

**Value proposition**  
- **Safety & ergonomics**: By leveraging Rust’s type system and memory safety guarantees, Reverie reduces the risk of crashes or security bugs that often accompany low‑level syscall interception.  
- **Flexibility**: The framework abstracts away the complex ptrace/LD_PRELOAD tricks, letting you write interception logic as ordinary Rust code, which speeds up prototyping of security monitors, testing harnesses, or sandboxing solutions.  
- **Community traction**: Over 800 stars and a growing fork count indicate a healthy interest base, and recent activity (last commit 2026‑05‑14) shows the project is still being maintained.

**Practical adoption path**  
1. **Initial evaluation** – Clone the repo, run the provided examples, and verify that the syscalls you need to intercept are supported on your target kernel version.  
2. **Prototype** – Implement a small proof‑of‑concept interceptor in Rust, using the documented `Reverie` trait, and test it on a non‑production environment (e.g., a VM or container).  
3. **Security & compliance review** – Perform a manual audit of the codebase, confirm the license (MIT/Apache‑compatible) matches your policy, and run static analysis tools (e.g., cargo‑audit) to check for known Rust crate vulnerabilities.  
4. **Integration** – Add the library as a Cargo dependency, wrap your existing binary with `reverie::run`, and integrate CI checks to ensure the interceptor builds and runs across your supported distributions.  
5. **Operational hardening** – Set up logging, monitoring, and fallback mechanisms (e.g., graceful disable on failure) before rolling out to staging.

**Production readiness** – **Medium**. The framework is mature enough for internal prototypes and controlled production workloads, but it still requires:
- A manual code and security review (metadata is sparse).  
- Validation that the target kernel version and distro are compatible with Reverie’s underlying mechanisms.  
- Ongoing maintenance of the Rust dependencies and monitoring of upstream updates.  

With those checks in place, Reverie can be safely adopted for internal tooling, custom sandboxing, or debugging pipelines, while a full production deployment should include a risk‑mitigation plan and a fallback strategy.

### Русский

**facebookexperimental/reverie** — это фреймворк на Rust для безопасного перехвата системных вызовов в Linux, ориентированный на удобство разработки и минимальное влияние на работающие процессы. Его обычно используют в прототипах и внутренних инструментах, где требуется динамический контроль над syscall‑ами (например, для отладки, мониторинга или реализации пользовательских политик безопасности). Проект имеет средний уровень готовности к production: имеет 824 звёзд, активные коммиты и поддержку Rust, но перед внедрением требуется ручная проверка совместимости, лицензии и безопасности, а также оценка зависимости от поддерживаемости проекта.

### 中文

**项目简介**  
Reverie（facebookexperimental/reverie）是一个基于 Rust 实现的 Linux 系统调用拦截框架，旨在提供 ergonomics（易用的 API）和安全性，帮助开发者在用户态安全、可控地插入、修改或监控系统调用。

**价值**  
- **安全可靠**：通过在内核与用户空间之间插入安全的拦截层，避免直接修改内核代码，降低系统崩溃和安全漏洞的风险。  
- **易用的 Rust 接口**：提供高层次的抽象和宏，开发者可以用几行代码定义拦截规则，省去繁琐的 C/汇编实现。  
- **适用于原型和内部工具**：在需要对系统调用行为进行审计、模拟或注入的实验性项目、调试工具、容器安全方案等场景中，可快速落地。

**典型接入方式**  
1. **在 Cargo.toml 中添加依赖**  
   ```toml
   [dependencies]
   reverie = { git = "https://github.com/facebookexperimental/reverie", rev = "main" }
   ```  
2. **实现 `Tool` trait**，在 `handle_syscall` 或 `handle_signal` 等回调里编写拦截逻辑。  
3. **使用 `reverie::launch` 启动被拦截的目标进程**，例如：  
   ```rust
   fn main() -> Result<(), Box<dyn std::error::Error>> {
       reverie::launch::<MyTool, _>(std::env::args())?;
       Ok(())
   }
   ```  
4. **在 CI/CD 或内部部署脚本中加入构建与运行步骤**，确保目标二进制在受控环境下启动。

**生产可用性**  
- **成熟度**：项目已有 800+ 星、40+ 分叉，最近一次提交在 2026‑05‑14，活跃度尚可。  
- **适用范围**：适合原型验证、内部安全审计、容器/沙箱监控等场景；若要在面向外部用户的生产服务中使用，需要额外进行：  
  - 代码审计（确保拦截逻辑不引入未预期的行为）。  
  - 兼容性测试（不同内核版本、发行版的行为一致性）。  
  - 依赖管理与升级策略（Rust 生态的 crate 版本更新）。  
- **风险**：许可证（MIT/Apache 双许可证）需确认符合公司合规；项目维护者主要是 Facebook 实验团队，长期维护承诺尚不明朗，建议自行 fork 并维护关键分支。  

**结论**：Reverie 在原型开发和内部安全工具链中提供了高效、相对安全的系统调用拦截能力，集成成本低。若在生产环境使用，建议进行充分的安全审计、兼容性验证，并准备内部维护方案。

## 🧭 Practical evaluation

**Value:** facebookexperimental/reverie may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 824 GitHub stars
- 41 forks
- updated 2026-05-14
- primary language: Rust

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 41/100 |
| stars | 62/100 |
| topics | 0/100 |
| outlook | 71/100 |
| quality | 65/100 |
| recency | 100/100 |
| adoption | 56/100 |
| production | 71/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/facebookexperimental/reverie) · [← Back to Misc](./README.md)</sub>
