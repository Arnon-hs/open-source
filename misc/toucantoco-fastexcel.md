# ToucanToco/fastexcel

[![Stars](https://img.shields.io/github/stars/ToucanToco/fastexcel?style=flat-square&color=yellow)](https://github.com/ToucanToco/fastexcel/stargazers) [![Forks](https://img.shields.io/github/forks/ToucanToco/fastexcel?style=flat-square&color=blue)](https://github.com/ToucanToco/fastexcel/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> A fast excel reader for Rust and Python

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 230 |
| 🍴 **Forks** | 20 |
| 💻 **Language** | Rust |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`arrow` `pandas` `polars` `python` `rust`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
ToucanToco / fastexcel is an open‑source library that provides high‑performance Excel (XLSX) reading capabilities for both Rust and Python. With a modest but active codebase (230 ★, recent updates) it targets use‑cases where fast, low‑memory parsing of large spreadsheets is required, such as data‑ingestion pipelines or analytics prototypes.

**Value**  
- **Speed & Efficiency:** Leveraging Rust’s zero‑cost abstractions, the core reader can process millions of rows far quicker than many pure‑Python alternatives, while exposing a Python API for easy integration into existing data‑science stacks.  
- **Dual‑language support:** Teams can use the same high‑performance engine from Rust for production services and from Python for exploratory analysis, reducing duplicated effort.  
- **Lightweight footprint:** The library avoids heavyweight dependencies (e.g., Java‑based POI), making container images smaller and deployment simpler.

**Practical Adoption Path**  
1. **Proof‑of‑Concept:** Clone the repo, run the example scripts, and benchmark against the current Excel‑reading approach on a representative sample file.  
2. **Read‑the‑Docs Check:** Verify that the README covers installation (Cargo + PyO3/maturin), supported Excel features, and any platform‑specific notes.  
3. **Integration Layer:** Wrap the Python bindings in a thin utility module that converts the library’s row iterator into pandas DataFrames or Arrow tables, matching your existing data pipeline.  
4. **Testing & Validation:** Add unit tests for the specific sheets you’ll process (e.g., mixed data types, formulas) and run them in CI to catch regressions.  

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last commit 2026‑05‑11) and has a modest community (230 ★, 20 forks). It is suitable for internal tools, prototypes, or services where performance outweighs the need for a large ecosystem.  
- **Risks to Mitigate:** Verify the license (MIT/Apache‑2.0 compatible), perform a security audit of the Rust crate and its dependencies, and ensure a maintainer is responsive for critical bugs.  
- **Next Steps for Production:** Pin the library version, incorporate it into your CI pipeline, and establish a fallback (e.g., openpyxl) for edge‑case Excel features not yet supported. Once these checks are in place, fastexcel can be promoted to production for high‑throughput Excel ingestion workloads.

### Русский

**ToucanToco/fastexcel** — быстрый парсер Excel‑файлов на Rust с Python‑обёрткой, подходящий для задач, где требуется читать большие таблицы с минимальными задержками. Его типичное внедрение начинается с небольшого прототипа: проверяете README, подключаете библиотеку к существующему пайплайну и оцениваете производительность на реальных данных. Готовность к production — средняя: проект стабилен для прототипов и внутренних сервисов, но перед выпуском в продакшн рекомендуется проверить лицензию, безопасность зависимостей и наличие активных мейнтейнеров.

### 中文

**价值**  
- **高速读取**：基于 Rust 实现的核心解析库，提供极快的 Excel（.xlsx/.xls）读取速度，适合大文件或高并发场景。  
- **跨语言**：通过 PyO3 包装后可在 Python 中直接调用，兼顾 Rust 的性能和 Python 的生态便利，满足数据科学、ETL、后台服务等多种业务需求。  
- **轻量依赖**：仅依赖少量系统库，易于在 CI/CD、容器或无根环境中部署。  

**典型接入方式**  

| 场景 | 步骤 | 示例代码 |
|------|------|----------|
| **Rust 项目** | 1. 在 `Cargo.toml` 中添加 `fastexcel = "0.9"`<br>2. 在代码中使用 `fastexcel::Reader` 读取工作表 | ```rust\nuse fastexcel::Reader;\nlet mut reader = Reader::open(\"data.xlsx\")?;\nlet sheet = reader.sheet(\"Sheet1\").unwrap();\nlet rows = sheet.rows();\n``` |
| **Python 项目** | 1. `pip install fastexcel`（内部会拉取已编译的 Rust‑Python 扩展）<br>2. `import fastexcel as fe` 调用同名 API | ```python\nimport fastexcel as fe\nrows = fe.read_excel(\"data.xlsx\", sheet=\"Sheet1\")\nfor r in rows:\n    print(r)\n``` |
| **微服务/容器** | 将 `fastexcel` 编译为静态二进制或使用官方 `python:slim` 镜像，确保 `libssl`、`libz` 等系统依赖已装。| Dockerfile 片段：<br>```Dockerfile\nFROM python:3.12-slim\nRUN pip install --no-cache-dir fastexcel\nCOPY . /app\nWORKDIR /app\nCMD [\"python\", \"main.py\"]\n``` |

**生产可用性**  

- **成熟度**：已有 230+ ⭐、20+ forks，最近一次提交在 2026‑05‑11，活跃度尚可。适合作为 **原型**、内部工具或 **对性能有明确要求的服务** 的 Excel 读取层。  
- **风险点**  
  1. **许可证**：项目采用 MIT/Apache 双许可证（需再次确认），对大多数商业场景友好。  
  2. **安全性**：目前未发现已知漏洞，但建议在引入前通过 `cargo audit` / `pip-audit` 检查依赖。  
  3. **维护者**：贡献者数量有限，若在关键业务中使用，建议自行 fork 并保持对关键 bug 的内部修复能力。  
- **上线建议**  
  1. 先在测试环境实现一个 **小规模 POC**（读取 10‑100 条记录），验证兼容性和性能。  
  2. 加入 **异常捕获**（如文件损坏、格式不支持）并设置超时，以防单次读取阻塞。  
  3. 对关键路径做 **基准测试**（对比 `openpyxl`、`pandas.read_excel`），确认性能收益符合预期。  
  4. 将库锁定在 `Cargo.lock` / `requirements.txt`，并在 CI 中持续监控安全审计报告。  

综合来看，**fastexcel** 在需要高吞吐、低延迟的 Excel 读取场景下具有显著优势，适合作为内部服务或原型的首选实现；在正式生产环境使用时，建议做好版本锁定、审计和容错措施，以降低维护者稀少带来的潜在风险。

## 🧭 Practical evaluation

**Value:** ToucanToco/fastexcel may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 230 GitHub stars
- 20 forks
- updated 2026-05-11
- primary language: Rust
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 33/100 |
| stars | 50/100 |
| topics | 63/100 |
| outlook | 71/100 |
| quality | 70/100 |
| recency | 100/100 |
| adoption | 45/100 |
| production | 73/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/ToucanToco/fastexcel) · [← Back to Misc](./README.md)</sub>
