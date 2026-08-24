# BurntSushi/bstr

[![Stars](https://img.shields.io/github/stars/BurntSushi/bstr?style=flat-square&color=yellow)](https://github.com/BurntSushi/bstr/stargazers) [![Forks](https://img.shields.io/github/forks/BurntSushi/bstr?style=flat-square&color=blue)](https://github.com/BurntSushi/bstr/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> A string type for Rust that is not required to be valid UTF-8.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.1k |
| 🍴 **Forks** | 73 |
| 💻 **Language** | Rust |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`byte-string` `bytes` `graphemes` `substring` `substring-search` `unicode` `utf-8`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary**  
BurntSushi / bstr provides a Rust string type that works with arbitrary byte sequences, removing the UTF‑8 constraint of the standard `String`. It lets developers manipulate binary or legacy text data safely and efficiently, which is useful when building UI layers that must display or process non‑UTF‑8 payloads.

**Value**  
Because many front‑end pipelines (e.g., logs, network protocols, legacy file formats) contain raw bytes, `bstr` eliminates the need for ad‑hoc conversion hacks or custom wrappers. By offering a drop‑in‑compatible API with the standard library, it speeds up UI development, reduces bugs related to invalid UTF‑8 handling, and lets teams reuse existing components without rewriting them for binary data.

**Practical adoption path**  
1. **Proof‑of‑concept** – Add `bstr = "X.Y"` to a small crate, replace a few `String`/`Vec<u8>` usages with `BString`/`ByteSlice`, and run the existing test suite.  
2. **README validation** – Follow the library’s README examples to ensure the build environment (Rust 1.70+, Cargo) works in your CI.  
3. **Component pilot** – Refactor a single UI module (e.g., a log viewer) to use `bstr` for its data source, measuring code‑size and performance impacts.  
4. **Scale‑up** – If the pilot succeeds, incrementally migrate other modules, keeping both `String` and `BString` where needed, and add lint rules to enforce consistent usage.

**Production readiness**  
The project is moderately production‑ready: it has >1 k stars, active maintenance (last commit 2026‑06‑24), and a small, well‑documented API surface. It is suitable for prototypes, internal tools, or services where binary payloads are common, but teams should perform a dependency audit (check for transitive crates, licensing, and any known CVEs) and establish a fallback plan before using it in a public‑facing, high‑traffic product.

### Русский

**BurntSushi/bstr** — это библиотека Rust, предоставляющая тип строки, который не требует корректного UTF‑8, что упрощает работу с произвольными байтовыми данными в пользовательском интерфейсе. При внедрении обычно начинают с небольшого proof‑of‑concept: добавить зависимость, пройтись по README и заменить текущие `String`/`&str` там, где нужен «сырый» текст, что позволяет быстрее собрать UI‑компоненты без лишних парсингов. Проект имеет средний уровень готовности к продакшну — достаточное количество звёзд и активные обновления делают его подходящим для прототипов и внутренних сервисов, но перед широким использованием стоит проверить совместимость с существующей сборкой и оценить нагрузку на поддержку зависимости.

### 中文

**价值**  
BurntSushi/bstr 为 Rust 提供了一个能够直接操作任意字节序列的 `BString`/`BStr` 类型，摆脱了必须是合法 UTF‑8 的限制。它让你在处理二进制协议、日志、文件名、网络数据等“非文本”字符串时，仍然可以使用熟悉的字符串 API（切片、拼接、搜索、正则等），从而：

- **降低底层字符处理的错误风险**（避免频繁的 `String::from_utf8_lossy`、`Vec<u8>` 与 `&str` 之间的转换）。  
- **提升开发效率**：统一的 API 可直接在业务层使用，无需为每种二进制格式写自定义包装。  
- **改善前端交付**：在需要把二进制数据直接渲染到 UI（如十六进制视图、文件预览）时，可直接把 `BStr` 传递给前端框架的字符串字段，省去额外的编码/解码步骤。

**典型接入方式**  

1. **依赖声明**  
   ```toml
   # Cargo.toml
   [dependencies]
   bstr = "1.9"
   ```
2. **基本使用**  
   ```rust
   use bstr::BStr;
   use bstr::ByteSlice; // 为 &[u8] 提供 .as_bstr() 等扩展方法

   let raw: &[u8] = b"\xFF\xFEHello\x00World";
   let b: &BStr = raw.as_bstr();          // 零拷贝包装
   println!("len = {}", b.len());        // 仍然是字节长度
   println!("contains 'Hello'? {}", b.contains_str("Hello"));
   ```
3. **与前端（WebAssembly）结合**  
   - 将 `BString`/`BStr` 通过 `wasm-bindgen` 暴露为 `Uint8Array` 或 `String`（后者通过 `String::from_utf8_lossy` 只在 UI 必须显示时使用）。  
   - 示例：  
     ```rust
     #[wasm_bindgen]
     pub fn get_raw_data() -> js_sys::Uint8Array {
         let data = bstr::BString::from(vec![0x00, 0x01, 0xFF, b'A']);
         js_sys::Uint8Array::from(data.as_slice())
     }
     ```
4. **小型验证（PoC）**  
   - 在现有项目中新建一个 `utils` 模块，使用 `bstr` 包装网络响应体或文件读取结果，检查编译、单元测试是否通过。  
   - 同时更新 `README` 示例，确保团队成员能快速上手。

**生产可用性**  

| 维度 | 评估 |
|------|------|
| **成熟度** | 项目已有 1k+ Stars、70+ Fork，活跃维护至 2026‑06‑24，社区成熟。 |
| **依赖风险** | 仅单一 crate，依赖树浅，升级成本低；但仍需在 CI 中锁定版本，防止突发的破坏性改动。 |
| **性能** | 零拷贝包装和 SIMD 加速的搜索/比较实现，已在多个高性能项目中使用，满足生产需求。 |
| **安全** | 通过 `cargo audit` 检查暂无已知安全漏洞；仍建议定期审计。 |
| **适用场景** | 原型、内部工具、需要处理非 UTF‑8 数据的后端服务或 WebAssembly 前端。对外部公开的高流量服务建议在正式发布前做一次兼容性/性能基准。 |
| **上线建议** | 1) 在低风险分支或内部服务做 PoC；2) 将 `bstr` 版本锁定在 `Cargo.lock`；3) 添加单元/集成测试覆盖关键路径；4) 通过 CI 自动运行 `cargo audit` 与 `cargo fmt`。 |

综上，BurntSushi/bstr 在处理二进制或不确定编码的字符串时提供了安全、易用且性能友好的抽象，适合作为 Rust 项目中“非 UTF‑8 字符串”的标准库替代。只要在上线前完成小范围验证并做好依赖管理，它完全可以在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** BurntSushi/bstr helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1074 GitHub stars
- 73 forks
- updated 2026-06-24
- primary language: Rust
- 7 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 47/100 |
| stars | 65/100 |
| topics | 88/100 |
| outlook | 56/100 |
| quality | 65/100 |
| recency | 40/100 |
| adoption | 60/100 |
| production | 54/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/BurntSushi/bstr) · [← Back to Misc](./README.md)</sub>
