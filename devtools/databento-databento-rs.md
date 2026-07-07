# databento/databento-rs

[![Stars](https://img.shields.io/github/stars/databento/databento-rs?style=flat-square&color=yellow)](https://github.com/databento/databento-rs/stargazers) [![Forks](https://img.shields.io/github/forks/databento/databento-rs?style=flat-square&color=blue)](https://github.com/databento/databento-rs/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> The official Rust client library for Databento

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 102 |
| 🍴 **Forks** | 16 |
| 💻 **Language** | Rust |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-07-07 |
| 🔍 **Source** | github |

## 🏷️ Topics

`async` `databento` `historical-data` `http` `market-data` `real-time` `tcp` `tick-data`

## 🎯 Categories

DevTools · Data

## 📝 Summary

### English

**Project Summary:**

databento/databento-rs is an open-source Rust client library for Databento, designed to streamline developer workflows and automate local engineering tasks. By integrating this library, engineers can significantly speed up their development and review loops, ultimately improving the efficiency of their daily tasks. With a medium production readiness score, it's suitable for prototypes or internal workflows, requiring dependency and maintenance checks before deployment to production.

**Value:**

The primary value proposition of databento/databento-rs lies in its ability to save engineers time and effort in their daily development and review loops. By automating local engineering tasks and speeding up developer workflows, this library helps teams improve their productivity and efficiency.

**Practical Adoption Path:**

To adopt databento/databento-rs, follow these steps:

1. Evaluate the library's implementation signals, such as API/SDK/CLI, language metadata, or focused topics, to ensure it aligns with your project's requirements.
2. Assess the library's production readiness, considering factors like dependency and maintenance checks.
3. Review the library's license, security posture, and active maintainers to ensure they meet your project's standards.
4. Integrate the library into your project, and test its functionality to ensure a smooth adoption.

### Русский

Резюме проекта databento/databento-rs:

Библиотека databento/databento-rs представляет собой официальный клиентный библиотечный набор для Databento, предназначенный для ускорения ежедневных разработки и отладки. Она помогает инженерам экономить время и ресурсы на автоматизации локальных задач и ускорении обратной связи в CI-пipeline. Проект готов к использованию в прототипах или внутренних рабочих процессах, но требует дополнительного обследования перед выпуском в production.

### 中文

**项目简介**  
databento/databento‑rs 是 Databento 官方提供的 Rust 客户端库，封装了 Databento 的 API 并提供命令行工具，帮助开发者在 Rust 环境中便捷地获取、查询和处理金融数据。

**价值**  
- **提升开发效率**：统一的 SDK 抽象了底层 HTTP/WS 通信，开发者只需几行代码即可完成数据拉取、实时订阅和本地缓存，显著缩短日常开发和调试周期。  
- **自动化工作流**：可在 CI/CD 流程中直接调用库进行数据校验或生成报告，实现持续集成时的即时反馈。  
- **降低维护成本**：官方维护的实现避免了自行编写协议解析代码，降低了出错风险和后期维护负担。

**典型接入方式**  
1. **在 Cargo.toml 中添加依赖**  
   ```toml
   [dependencies]
   databento = "0.3"
   ```  
2. **使用 SDK 初始化客户端并调用 API**  
   ```rust
   use databento::Client;

   #[tokio::main]
   async fn main() -> Result<()> {
       let client = Client::new("YOUR_API_KEY")?;
       let resp = client.get_latest("XBTUSD").await?;
       println!("{:?}", resp);
       Ok(())
   }
   ```  
3. **在 CI 脚本或本地任务中直接调用**，如在 GitHub Actions 中运行 `cargo run --example fetch_data`，即可完成自动化数据拉取与校验。

**生产可用性**  
- **成熟度**：当前拥有 102 个 GitHub Stars、16 次 Fork，最近一次更新在 2026‑07‑07，活跃度尚可。  
- **适用场景**：适合原型开发、内部工具或数据实验平台；在正式生产环境使用前建议进行依赖审计、许可证合规检查以及安全漏洞扫描。  
- **风险**：仍需确认维护者的长期可用性、许可证兼容性以及潜在的安全漏洞。完成这些检查后，可在对可靠性要求不极端的生产服务中安全使用。

## 🧭 Practical evaluation

**Value:** databento/databento-rs helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 102 GitHub stars
- 16 forks
- updated 2026-07-07
- primary language: Rust
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 31/100 |
| stars | 43/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 73/100 |
| recency | 100/100 |
| adoption | 39/100 |
| production | 74/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-07 · [View on GitHub](https://github.com/databento/databento-rs) · [← Back to DevTools](./README.md)</sub>
