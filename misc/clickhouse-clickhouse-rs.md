# ClickHouse/clickhouse-rs

[![Stars](https://img.shields.io/github/stars/ClickHouse/clickhouse-rs?style=flat-square&color=yellow)](https://github.com/ClickHouse/clickhouse-rs/stargazers) [![Forks](https://img.shields.io/github/forks/ClickHouse/clickhouse-rs?style=flat-square&color=blue)](https://github.com/ClickHouse/clickhouse-rs/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> Official pure Rust typed client for ClickHouse DB

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 540 |
| 🍴 **Forks** | 160 |
| 💻 **Language** | Rust |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`clickhouse` `http` `rust` `streaming` `tokio`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary:**
ClickHouse/clickhouse-rs is an open-source, pure Rust typed client for ClickHouse DB, designed to simplify daily development and review loops for engineers. It enables faster development workflows, automates local engineering tasks, and improves CI feedback. While it has a medium production readiness score, it is suitable for prototypes or internal workflows with proper dependency and maintenance checks.

**Value:**
The primary value proposition of ClickHouse/clickhouse-rs lies in its ability to save engineers time and effort in their daily development and review loops. By providing a typed client for ClickHouse DB, it streamlines interactions with the database, making it easier to develop and test applications.

**Practical Adoption Path:**
To adopt ClickHouse/clickhouse-rs, follow these steps:

1. Evaluate the client's API and SDK to ensure it meets your project's requirements.
2. Integrate the client into your local development environment to automate tasks and speed up workflows.
3. Use it in your CI pipeline to improve feedback and catch errors early.
4. Before moving to production, review the client's dependency and maintenance requirements to ensure they align with your project's needs.

**Production Readiness:**
While ClickHouse/clickhouse-rs has a medium production readiness score, it is

### Русский

Резюме ClickHouse/clickhouse-rs:

ClickHouse/clickhouse-rs - это официальный типизированный клиент на Rust для базы данных ClickHouse, который помогает инженерам экономить время в повседневной разработке и отладке. Этот проект может ускорить разработку, автоматизировать локальные задачи инженеров и улучшить обратную связь в CI. ClickHouse/clickhouse-rs готов к использованию в прототипах или внутренних рабочих процессах, но требует проверки зависимостей и поддержки перед внедрением в производство.

### 中文

**项目简介**  
ClickHouse/clickhouse‑rs 是官方提供的纯 Rust 实现的 ClickHouse 数据库客户端，提供强类型 API，帮助开发者在 Rust 生态中直接、可靠地与 ClickHouse 交互。

**价值**  
- **提升开发效率**：使用类型安全的 Rust 接口，省去手写 SQL 拼接和结果解析的繁琐步骤，显著缩短每日开发和代码审查的循环时间。  
- **加速自动化**：可在本地脚本、CI/CD 流水线或内部工具中直接调用，快速完成数据写入、查询和验证，提升 CI 反馈速度。  
- **降低出错率**：编译期即捕获类型不匹配和语法错误，降低运行时异常和数据错误的风险。

**典型接入方式**  
1. **在 Cargo.toml 中添加依赖**  
   ```toml
   [dependencies]
   clickhouse = "0.12"   # 具体版本请参考仓库 Release
   ```  
2. **创建客户端并执行查询**  
   ```rust
   use clickhouse::{Client, Row};

   #[derive(Row)]
   struct MyRow {
       id: u64,
       name: String,
   }

   #[tokio::main]
   async fn main() -> clickhouse::Result<()> {
       let client = Client::default()
           .with_url("http://localhost:8123")
           .with_user("default")
           .with_password("");

       let rows = client
           .query("SELECT id, name FROM my_table")
           .fetch_all::<MyRow>()
           .await?;

       println!("{:?}", rows);
       Ok(())
   }
   ```  
3. **在 CI 中使用**：将上述代码封装为小工具或库，在测试阶段直接对 ClickHouse 实例进行数据准备和结果校验。

**生产可用性**  
- **成熟度**：GitHub ★540、Fork ★160，最近一次提交为 2026‑07‑02，活跃度尚可。  
- **适用场景**：适合原型、内部服务或对性能要求不极端的生产环境。若用于高并发或关键业务，建议在正式上线前进行依赖审计、性能压测以及安全审查。  
- **风险**：当前仍需确认许可证兼容性、长期维护者的活跃度以及安全漏洞响应速度。完成这些检查后，可视为中等风险、可投入生产的组件。

## 🧭 Practical evaluation

**Value:** ClickHouse/clickhouse-rs helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 540 GitHub stars
- 160 forks
- updated 2026-07-02
- primary language: Rust
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 55/100 |
| stars | 58/100 |
| topics | 63/100 |
| outlook | 56/100 |
| quality | 60/100 |
| recency | 40/100 |
| adoption | 57/100 |
| production | 55/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/ClickHouse/clickhouse-rs) · [← Back to Misc](./README.md)</sub>
