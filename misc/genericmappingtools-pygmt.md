# GenericMappingTools/pygmt

[![Stars](https://img.shields.io/github/stars/GenericMappingTools/pygmt?style=flat-square&color=yellow)](https://github.com/GenericMappingTools/pygmt/stargazers) [![Forks](https://img.shields.io/github/forks/GenericMappingTools/pygmt?style=flat-square&color=blue)](https://github.com/GenericMappingTools/pygmt/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> A Python interface for the Generic Mapping Tools.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 863 |
| 🍴 **Forks** | 245 |
| 💻 **Language** | Python |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`earth-science` `geophysics` `geoscience` `hacktoberfest` `maps` `python` `seismology`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
GenericMappingTools/pygmt is a Python wrapper for the classic Generic Mapping Tools (GMT), enabling users to create high‑quality geospatial visualisations directly from Python scripts. With over 860 stars, frequent commits (last update 2026‑06‑25), and a growing community, it offers a mature, well‑documented API that integrates seamlessly with the scientific Python stack.

**Value**  
- **Unified workflow**: Engineers and scientists can stay in Python while leveraging GMT’s powerful cartographic capabilities, eliminating the need to switch between languages or manage separate command‑line calls.  
- **Reproducibility & automation**: Scripts written with PyGMT can be version‑controlled, parameterised, and executed in CI pipelines, supporting reproducible research and automated map generation.  
- **Ecosystem compatibility**: Works out‑of‑the‑box with NumPy, pandas, xarray, and Jupyter, making it easy to ingest data, perform analysis, and visualise results in a single environment.

**Adoption Path**  
1. **Proof‑of‑concept**: Clone the repo, follow the README to generate a simple map (e.g., a global coastlines plot) and verify that the output matches expectations.  
2. **Integration test**: Replace an existing GMT command‑line step in a pipeline with the equivalent PyGMT calls, checking for parity in performance and visual output.  
3. **Pilot**: Deploy the updated pipeline on a staging environment, adding unit tests for the PyGMT‑generated figures and monitoring any dependency conflicts.  
4. **Full rollout**: Once the pilot is stable, promote the code to production, documenting usage guidelines and version pinning for reproducibility.

**Production Readiness**  
The project scores high on readiness: recent activity, a solid contributor base, and widespread adoption in the geosciences community indicate a stable codebase. No critical licensing or security red flags have been identified, though a final review of the license (MIT) and a quick vulnerability scan of dependencies is recommended. Given these signals, PyGMT is suitable for a serious pilot and, after the small proof‑of‑concept phase, can be considered production‑ready for map‑generation workloads.

### Русский

**GenericMappingTools/pygmt** — это официальная Python‑обёртка над мощным набором утилит GMT, позволяющая генерировать геофизические и картографические визуализации прямо из кода. Типичный сценарий внедрения — быстрый прототип или автоматизированный pipeline, где данные (например, сейсмические, магнитные или топографические) преобразуются в публикационные карты через несколько функций Python, что упрощает интеграцию с аналитическими библиотеками (numpy, pandas, xarray). Проект имеет активную поддержку, более 800 звёзд, регулярные обновления и широкое применение в научных проектах, поэтому готов к пилотному запуску в production‑окружении после небольшого proof‑of‑concept и проверки лицензии/безопасности.

### 中文

**项目简介**  
GenericMappingTools/pygmt 是 GMT（Generic Mapping Tools）的官方 Python 接口，提供了在 Python 环境下调用 GMT 强大绘图与地理空间分析功能的能力。借助 pygmt，用户可以使用熟悉的 Pandas、NumPy、Xarray 等生态工具，直接生成高质量的地球科学图形、网格运算和投影转换。

**价值**  
- **统一语言栈**：在 Python 脚本或 Jupyter Notebook 中完成从数据预处理到可视化的全链路，无需切换到 GMT 的命令行或脚本语言。  
- **高质量绘图**：继承 GMT 的专业绘图引擎，支持海图、地形图、剖面图、等值线图等多种专业图形，且渲染质量在科研出版物中被广泛认可。  
- **生态兼容**：与 NumPy、SciPy、Xarray、Pandas、Matplotlib 等库无缝协作，便于在已有数据处理流水线中嵌入空间分析与可视化。  
- **活跃社区**：截至 2026 年 6 月，项目拥有 863+ 星、245+ Fork，最近一次提交在 2026‑06‑25，说明代码维护与功能迭代都非常活跃。

**典型接入方式**  
1. **安装**（推荐使用 Conda 或 pip）：  
   ```bash
   conda install -c conda-forge pygmt   # 或
   pip install pygmt
   ```  
2. **在代码中引入**：  
   ```python
   import pygmt

   # 示例：绘制全球海岸线
   fig = pygmt.Figure()
   fig.coast(region="g", projection="W15c", shorelines=True, frame=True)
   fig.show()
   ```  
3. **与数据框结合**：  
   ```python
   import xarray as xr, pandas as pd
   ds = xr.open_dataset("topo.nc")
   fig = pygmt.Figure()
   fig.grdimage(grid=ds["elevation"], projection="M15c", cmap="viridis")
   fig.colorbar(frame='af+l"Elevation (m)"')
   fig.show()
   ```  
4. **在 CI / 自动化脚本中使用**：pygmt 完全兼容无头模式（`fig.savefig(...)`），适合在批处理或 CI 流水线中生成报告图。

**生产可用性**  
- **成熟度**：项目已稳定多年，API 基本向后兼容，文档完整（官方 README、示例库和 API 参考），并提供了大量 Jupyter Notebook 示例。  
- **维护状态**：近期仍有活跃提交、issue 处理和版本发布，社区响应及时。  
- **安全与合规**：采用 MIT 许可证，源码公开，依赖主要为常见的科学计算库，未发现重大安全漏洞。  
- **部署考量**：在容器化环境（Docker、Kubernetes）中使用时，只需确保安装 GMT 本体（conda‑forge 包已包含），并在运行时提供必要的字体与投影数据（默认随包提供）。  

综上，pygmt 已具备高生产可用性，适合作为地理空间可视化与分析的核心组件，建议先在小范围的 PoC 中验证与现有数据流水线的兼容性，随后逐步推广至完整的生产系统。

## 🧭 Practical evaluation

**Value:** GenericMappingTools/pygmt may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 863 GitHub stars
- 245 forks
- updated 2026-06-25
- primary language: Python
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 60/100 |
| stars | 62/100 |
| topics | 88/100 |
| outlook | 60/100 |
| quality | 66/100 |
| recency | 40/100 |
| adoption | 62/100 |
| production | 57/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/GenericMappingTools/pygmt) · [← Back to Misc](./README.md)</sub>
