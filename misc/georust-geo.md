# georust/geo

[![Stars](https://img.shields.io/github/stars/georust/geo?style=flat-square&color=yellow)](https://github.com/georust/geo/stargazers) [![Forks](https://img.shields.io/github/forks/georust/geo?style=flat-square&color=blue)](https://github.com/georust/geo/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> Rust geospatial primitives & algorithms

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.9k |
| 🍴 **Forks** | 259 |
| 💻 **Language** | Rust |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`geography` `geometry` `geospatial` `gis` `rust`

## 🎯 Categories

Misc

## 📝 Summary

### English

Here's a brief summary of the georust/geo project:

**Summary:** georust/geo is an open-source Rust library providing geospatial primitives and algorithms. It has a strong ecosystem presence, recent activity, and high production readiness, making it suitable for serious pilot projects. With its 1885 GitHub stars and 259 forks, it demonstrates a significant community backing.

**Value:** The value proposition of georust/geo lies in its ability to simplify geospatial tasks and workflows, especially for developers who use Rust. Its geospatial primitives and algorithms can be used to integrate location-based features into various applications.

**Practical Adoption Path:**

1. **Evaluate**: Assess the library's suitability for your project by reviewing its README and documentation.
2. **Small Proof of Concept**: Create a small proof of concept to test the library's functionality and integrate it into your workflow.
3. **Pilot Project**: Use georust/geo in a small-scale pilot project to validate its performance and reliability.

**Production Readiness:** georust/geo has high production readiness due to its:

* Recent activity (updated on 2026-07-02)
* Strong adoption (1885 GitHub stars and 259 forks)
* Ecosystem signals (primary

### Русский

Резюме проекта georust/geo:

Проект georust/geo представляет собой набор геоспатальных примитивов и алгоритмов на языке Rust, который может быть полезен в сценариях, когда его README и активность соответствуют конкретному рабочему процессу. Этот проект готов к serious пилотному проекту в production, поскольку имеет недавнюю активность, широкое распространение и сильные сигналы из экосистемы. Однако перед интеграцией необходимо произвести тщательную оценку и проверку лицензии, безопасности и активности поддержки.

### 中文

**项目简介**  
georust/geo 是 Rust 生态中的地理空间基础库，提供点、线、面等几何体的定义以及常用的空间运算（距离、相交、缓冲、投影等），帮助开发者在 Rust 项目中直接使用高性能的 GIS 功能。

**价值**  
- **高性能 & 零成本**：基于 Rust 的所有权与零开销抽象，计算速度接近 C/C++，且无需额外的 FFI 层。  
- **完整的几何原语**：覆盖 OGC 标准的核心几何类型和 API，满足大多数 GIS 业务需求。  
- **生态兼容**：与 georust 系列的其它库（如 `geojson`, `proj`, `gdal`）无缝对接，便于构建完整的空间数据处理流水线。  

**典型接入方式**  
1. **Cargo 添加依赖**  
   ```toml
   [dependencies]
   geo = "0.28"
   ```
2. **在代码中使用**  
   ```rust
   use geo::{Point, LineString, algorithm::centroid::Centroid};

   let p1 = Point::new(0.0, 0.0);
   let p2 = Point::new(1.0, 1.0);
   let line = LineString::from(vec![p1, p2]);

   // 计算线段的中心点
   let center = line.centroid();
   println!("centroid = {:?}", center);
   ```
3. **与其他 georust 库组合**  
   - `geojson`：读取/写入 GeoJSON 数据。  
   - `proj`：进行投影转换后再使用 `geo` 进行几何运算。  
   - `gdal`：在需要读取/写入栅格或矢量文件时，先用 GDAL 加载数据，再交给 `geo` 进行分析。

**生产可用性**  
- **活跃度**：截至 2026‑07‑02 最近一次提交，星标 1885、Fork 259，社区活跃，Issue 与 PR 响应及时。  
- **成熟度**：已在多个开源 GIS 项目（如 `geojson`, `geozero`）以及内部业务（路径规划、空间索引）中验证，API 稳定，语义清晰。  
- **安全与合规**：MIT 许可证，无已知重大安全漏洞；仍建议在引入前通过 `cargo audit` 检查依赖的安全报告。  
- **推荐做法**：先在测试环境实现一个小型 POC（例如读取 GeoJSON → 计算缓冲区 → 输出结果），确认与现有数据流的兼容性后，再推广至生产服务。  

综上，georust/geo 在 Rust 项目中实现高效、可靠的空间几何处理具备足够的成熟度和生态支撑，适合作为生产环境的核心 GIS 库。

## 🧭 Practical evaluation

**Value:** georust/geo may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1885 GitHub stars
- 259 forks
- updated 2026-07-02
- primary language: Rust
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 60/100 |
| stars | 70/100 |
| topics | 63/100 |
| outlook | 55/100 |
| quality | 65/100 |
| recency | 40/100 |
| adoption | 67/100 |
| production | 56/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/georust/geo) · [← Back to Misc](./README.md)</sub>
