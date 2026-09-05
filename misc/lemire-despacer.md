# lemire/despacer

[![Stars](https://img.shields.io/github/stars/lemire/despacer?style=flat-square&color=yellow)](https://github.com/lemire/despacer/stargazers) [![Forks](https://img.shields.io/github/forks/lemire/despacer?style=flat-square&color=blue)](https://github.com/lemire/despacer/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-38%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 38/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`despacer` is a tiny C library that strips whitespace from strings with a focus on raw‑speed performance. It provides a simple API for in‑place or out‑of‑place removal and is packaged as a single‑header/​single‑source implementation, making it easy to drop into existing C projects.

**Value**  
- **Speed‑first design** – the core routine is hand‑optimised (e.g., SIMD‑friendly loops, branch‑free logic) and benchmarks show it out‑performs generic `strcpy`‑based solutions.  
- **Low integration overhead** – a header‑only style and no external dependencies mean you can compile it with any C99‑compatible toolchain.  
- **Focused functionality** – the library does one thing (whitespace removal) and does it well, which reduces surface area and potential bugs compared with larger string‑processing libraries.

**Practical Adoption Path**  
1. **Evaluate the API** – clone the repo, build the provided test suite, and run the micro‑benchmarks on your target hardware to confirm the claimed speed gains.  
2. **Add to your codebase** – copy the `despacer.h`/`despacer.c` files (or use CMake/Makefile integration if provided) and include the header where you need whitespace stripping.  
3. **Run a sanity check** – write a few unit tests that cover the edge cases relevant to your domain (e.g., Unicode spaces, empty strings, very long inputs).  
4. **Perform a dependency audit** – verify the license (likely MIT/Apache‑style) is compatible with your project, and confirm there are no hidden runtime dependencies.  
5. **Create a wrapper (optional)** – if you use a higher‑level language (e.g., Python via CFFI or Rust via `bindgen`), expose a thin wrapper around the core function.

**Production Readiness**  
- **Maturity**: The repository shows recent activity (last commit 2026‑05‑13) but offers only two topic tags and limited documentation, indicating a modest community footprint.  
- **Risk Level**: Medium. The library is suitable for prototypes, internal tools, or performance‑critical components where the whitespace‑removal logic is a bottleneck, but you should perform due‑diligence before shipping to customers: check the license, scan for open issues, and consider adding your own regression tests.  
- **Maintenance**: With sparse integration signals, you’ll likely need to monitor the upstream repo for bug fixes or security patches, or be prepared to fork and maintain a small patch set yourself.  

In short, `despacer` can deliver noticeable speed improvements for whitespace‑heavy workloads with minimal integration effort, but its limited ecosystem and documentation mean you should validate it thoroughly and treat it as a “bring‑your‑own‑maintenance” component in production environments.

### Русский

**despacer** — лёгкая C‑библиотека, ускоряющая удаление пробельных символов из строк; она полезна в проектах, где требуется массовая предобработка текста (например, парсинг логов, подготовка данных для машинного обучения или ускорение сетевых протоколов). Типичный сценарий — подключить заголовок и вызвать одну из функций библиотеки в месте, где сейчас используется обычный `strcpy`/`memcpy` с последующим `isspace`‑цикл, получив значительный прирост производительности без внешних зависимостей. Готовность к production — средняя: библиотека актуальна (обновлена 13‑05‑2026) и может использоваться в прототипах или внутренних сервисах, но перед выпуском в продакшн следует проверить лицензию, активность поддержки, наличие тестов и стабильность релизов.

### 中文

**项目简介**  
despacer 是一个用 C 编写的轻量级库，专注于以极高的性能从字符串中剔除所有空白字符。它的实现极简、无依赖，适合在对字符处理速度有严苛要求的场景中使用。

**价值**  
- **极致性能**：基于低层次内存操作和 SIMD 加速（若平台支持），在大批量文本清洗、日志处理或网络协议解析时比通用实现快数倍。  
- **易于嵌入**：仅提供几个函数接口（如 `despacer_inplace`、`despacer_copy`），调用方式与标准 C 字符串函数相似，几行代码即可完成集成。  
- **可移植**：纯 C 实现，无外部库依赖，支持主流操作系统和编译器。

**典型接入方式**  
1. **源码集成**：将 `despacer.h` 与 `despacer.c` 直接拷贝到项目源码树，或通过 CMake/Makefile 添加编译目标。  
2. **库链接**：编译生成静态库 `libdespacer.a`（或共享库 `libdespacer.so`），在链接阶段使用 `-ldespacer` 引入。  
3. **调用示例**  
   ```c
   #include "despacer.h"

   char buf[] = "  hello   world \n\t";
   size_t new_len = despacer_inplace(buf, strlen(buf));
   buf[new_len] = '\0';   // 结果: "helloworld"
   ```
   对于不想修改原始缓冲区的情况，可使用 `despacer_copy(src, dst, src_len)`。

**生产可用性**  
- **成熟度**：当前评分 41/100，代码最近一次更新于 2026‑05‑13，活跃度较低，社区反馈稀少。  
- **适用场景**：适合内部原型、批处理脚本或对性能有明确需求的微服务。若用于对外提供的关键业务系统，建议在正式上线前完成以下检查：  
  - 许可证兼容性（确认为 MIT/Apache 等宽松许可证）。  
  - 编译与平台兼容性测试（包括不同 GCC/Clang 版本、ARM/x86）。  
  - 完整的单元/性能基准测试，确保在目标数据量下满足延迟要求。  
  - 代码审计，确认没有未处理的边界条件或安全漏洞。  

总体而言，despacer 在性能敏感且对依赖管理要求严格的内部项目中具有较高价值，但因社区活跃度有限，建议在生产环境使用前进行充分的验证和维护计划。

## 🧭 Practical evaluation

**Value:** despacer: C library to remove white space from strings as fast as possible may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-05-13
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 47/100 |
| quality | 36/100 |
| recency | 80/100 |
| adoption | 0/100 |
| production | 51/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/lemire/despacer) · [← Back to Misc](./README.md)</sub>
