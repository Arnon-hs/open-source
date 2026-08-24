# messense/typst-py

[![Stars](https://img.shields.io/github/stars/messense/typst-py?style=flat-square&color=yellow)](https://github.com/messense/typst-py/stargazers) [![Forks](https://img.shields.io/github/forks/messense/typst-py?style=flat-square&color=blue)](https://github.com/messense/typst-py/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-43%2F100-brightgreen?style=flat-square)](#)

> Python binding to typst

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 316 |
| 🍴 **Forks** | 25 |
| 💻 **Language** | Rust |
| 📈 **Score** | 43/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`typst`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
`messense/typst-py` provides Python bindings for the **Typst** typesetting engine, letting developers invoke Typst’s rendering capabilities directly from Python code. With a modest star count (≈ 316) and recent activity (last updated 2026‑05‑14), it can be a handy bridge for workflows that need to generate PDFs or SVGs from Typst sources within Python applications.

**Value**  
- **Seamless integration**: eliminates the need to call the Typst CLI from subprocesses, reducing overhead and simplifying error handling.  
- **Python‑centric workflow**: lets data‑driven scripts, Jupyter notebooks, or web back‑ends generate high‑quality typeset documents on‑the‑fly.  
- **Open‑source and extensible**: the Rust‑based core is performant, while the Python layer can be customized or wrapped in higher‑level APIs.

**Practical Adoption Path**  
1. **Prototype** – Install the package (`pip install typst-py`) and run the example scripts from the README to verify that your Typst templates render correctly.  
2. **Security & License review** – Confirm the repository’s license (MIT) and scan the Rust dependency tree for known vulnerabilities (e.g., via `cargo audit`).  
3. **Dependency management** – Pin the package version and its Rust toolchain in your CI/CD pipeline; consider vendoring the compiled wheels for reproducibility.  
4. **Integration testing** – Add unit tests that render a sample Typst file and compare the output hash or PDF metadata to a golden reference.  
5. **Production rollout** – Deploy the binding in a controlled environment (e.g., internal service) and monitor performance and error logs before wider release.

**Production Readiness**  
- **Maturity**: Medium. The library is functional and actively maintained, but the surrounding ecosystem (documentation, integration examples) is limited, so a manual code review is advisable.  
- **Risk considerations**: No critical metadata issues, but verify the maintainer’s activity and audit the Rust dependencies for security patches.  
- **Suitable use‑cases**: Prototyping, internal tools, or services where the convenience of a Python API outweighs the need for enterprise‑grade support. With proper vetting and dependency pinning, it can be promoted to production for non‑mission‑critical workloads.

### Русский

**messense/typst-py** — это Python‑обёртка над библиотекой Typst, позволяющая генерировать и рендерить документы Typst непосредственно из Python‑кода. Она удобна для прототипов и внутренних пайплайнов, где требуется автоматизировать создание типографски точных PDF/HTML (например, генерация отчётов, технической документации или учебных материалов). Проект имеет умеренный уровень готовности к production: активные коммиты, 300+ звёзд и базовую стабильность, но перед внедрением стоит проверить лицензию, безопасность зависимостей и наличие поддерживающего мейнтейнера.

### 中文

**项目简介**  
messense/typst-py 为 Typst（基于 Rust 的排版引擎）提供 Python 绑定，使得在 Python 环境中可以直接调用 Typst 编译、渲染和文档生成等功能，适合需要在数据处理、报告自动化或 Web 服务中嵌入高质量排版的场景。

**价值**  
- **统一语言栈**：在已有的 Python 项目中无需额外调用外部命令行工具或使用跨语言桥接，直接通过 Python API 使用 Typst 的全部特性。  
- **高性能**：底层仍然是 Rust 实现的 Typst，保持原有的渲染速度和排版质量。  
- **灵活集成**：可与 Jupyter、FastAPI、Django 等常见 Python 框架配合，实现动态报告、PDF/PNG 输出或在线文档预览。

**典型接入方式**  
1. **安装**：`pip install typst-py`（或从源码 `pip install .`）。  
2. **基本使用**  
   ```python
   import typst

   # 编译 Typst 源码为 PDF
   pdf_bytes = typst.compile(source_code="= Hello, Typst!", format="pdf")
   with open("output.pdf", "wb") as f:
       f.write(pdf_bytes)
   ```
3. **在 Web 服务中**：在 FastAPI 路由里调用 `typst.compile`，把生成的二进制流返回给前端，实现「一键生成报告」的功能。  
4. **与数据科学工具结合**：在 Pandas、Matplotlib 生成的图表后，使用 Typst 模板把图表、表格和文字自动排版成完整的 PDF/HTML 报告。

**生产可用性**  
- **成熟度**：项目已有 300+ ⭐、25+ 🍴，最近一次提交在 2026‑05‑14，活跃度尚可。  
- **适用场景**：适合原型、内部工具或对排版质量有较高要求的业务系统；在对可靠性要求极高的生产环境使用前，建议进行：  
  - 依赖审计（检查 Rust 编译产物的安全性）。  
  - 版本锁定与 CI 测试，确保升级不会破坏现有模板。  
  - 监控编译耗时和资源占用，防止大文档导致服务阻塞。  
- **风险**：目前缺乏官方的长期维护承诺和完整的安全审计报告，需自行评估许可证兼容性并做好备份方案。  

总体而言，typst-py 在需要 Python 与高质量排版深度结合的项目中能显著提升开发效率和输出质量；在经过基本的安全与依赖检查后，可在内部生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** messense/typst-py may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 316 GitHub stars
- 25 forks
- updated 2026-05-14
- primary language: Rust
- 1 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 53/100 |
| topics | 13/100 |
| outlook | 39/100 |
| quality | 44/100 |
| recency | 20/100 |
| adoption | 48/100 |
| production | 44/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/messense/typst-py) · [← Back to Misc](./README.md)</sub>
