# icsharpcode/ILSpy

[![Stars](https://img.shields.io/github/stars/icsharpcode/ILSpy?style=flat-square&color=yellow)](https://github.com/icsharpcode/ILSpy/stargazers) [![Forks](https://img.shields.io/github/forks/icsharpcode/ILSpy?style=flat-square&color=blue)](https://github.com/icsharpcode/ILSpy/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> .NET Decompiler with support for PDB generation, ReadyToRun, Metadata (&more) - cross-platform!

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 25.5k |
| 🍴 **Forks** | 3.7k |
| 💻 **Language** | C# |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`c-sharp` `decompile` `decompiler` `decompiler-engine` `dotnet` `dotnetcore` `ilspy` `mono` `pdb` `unity`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
ILSpy (icsharpcode/ILSpy) is an open‑source .NET decompiler that can reconstruct source code, generate PDB debug symbols, and work with ReadyToRun images and metadata across Windows, macOS, and Linux. With more than 25 k stars and active maintenance, it serves as a powerful tool for turning compiled assemblies into searchable, analyzable artifacts that can be fed into data‑processing or reporting pipelines.  

**Value**  
- **Data extraction** – By decompiling binaries into readable C# and producing PDB files, ILSpy turns opaque binaries into structured, searchable text that can be indexed, queried, or fed into downstream analytics.  
- **Automation** – The CLI and API allow batch processing of large sets of assemblies, enabling automated pipelines for code‑base audits, security scanning, or generation of documentation and metrics.  
- **Cross‑platform** – Runs on .NET 6+ on Windows, macOS, and Linux, so it can be embedded in CI/CD runners or data‑lake ingest jobs regardless of the host OS.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the `dotnet tool install ilspycmd` command, and decompile a representative assembly to verify output quality and performance.  
2. **Integration Scaffold** – Wrap the `ilspycmd` CLI (or the `ICSharpCode.Decompiler` NuGet library) in a small wrapper service that accepts assembly blobs and returns source/PDB files or JSON‑encoded symbol tables.  
3. **Pipeline Hook** – Plug the wrapper into existing ETL or CI pipelines (e.g., Azure Pipelines, GitHub Actions, Apache Airflow) to automatically process newly built artifacts.  
4. **Validation** – Compare decompiled output against known source to ensure fidelity, and benchmark throughput for your expected volume.  

**Production Readiness**  
- **Activity & Community** – The project shows recent commits (last update 2026‑06‑28), a large star count (25 k), and thousands of forks, indicating a healthy maintainer base and community support.  
- **Stability** – Released binaries and a stable CLI are available via NuGet and as a .NET global tool; the codebase follows semantic versioning and includes extensive unit tests.  
- **Ecosystem Fit** – Compatible with .NET 6+ and supports PDB generation, ReadyToRun, and metadata extraction, covering most modern .NET workloads.  
- **Risk Mitigation** – The integration surface is not fully documented in the README, so a short pilot should confirm setup complexity and any required native dependencies before a full rollout.  

Overall, ILSpy is a mature, high‑readiness OSS component that can be safely piloted in a controlled proof‑of‑concept and, once validated, rolled out to production for automated decompilation and data‑pipeline enrichment of .NET binaries.

### Русский

**ILSpy** — это кроссплатформенный .NET‑декомпилятор с поддержкой генерации PDB, ReadyToRun и метаданных, который позволяет быстро превратить бинарные сборки в читаемый код и извлечь из них структурированные данные для последующего анализа. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept, в котором ILSpy используется в пайплайне обработки данных (например, автоматическое извлечение типовой информации из сборок и её загрузка в аналитическую систему). Проект имеет высокий уровень готовности к продакшену: активные коммиты, более 25 тыс. звёзд, тысячи форков и широкое принятие в сообществе, однако перед масштабным использованием следует уточнить детали интеграции и оценить затраты на настройку.

### 中文

**icsharpcode/ILSpy 简介**

icsharpcode/ILSpy 是一个开源的 .NET 解析器和反汇编器，支持生成 PDB 文件、ReadyToRun 和元数据等功能。它是跨平台的，并且具有强大的生态系统信号。

**价值**

icsharpcode/ILSpy 帮助将原始数据转换为可搜索、可分析或可自动化的管道。它适用于组织分析管道、处理数据集和改善报告工作流。

**典型接入方式**

接入 icsharpcode/ILSpy 的典型方式包括：

1. 评估小规模的案例（POC）来测试其可行性和 README 文档。
2. 验证设置成本之前进行重大投入。

**生产可用性**

icsharpcode/ILSpy 具有高生产可用性，因为它有最近的活动、广泛的采用和强大的生态系统信号。GitHub 上的星标数为 25,512，fork 数为 3,677，最后更新于 2026-06-28。主要语言为 C#，涉及 10 个主题。

## 🧭 Practical evaluation

**Value:** icsharpcode/ILSpy helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 25512 GitHub stars
- 3677 forks
- updated 2026-06-28
- primary language: C#
- 10 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 89/100 |
| stars | 94/100 |
| topics | 100/100 |
| outlook | 66/100 |
| quality | 82/100 |
| recency | 40/100 |
| adoption | 92/100 |
| production | 60/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/icsharpcode/ILSpy) · [← Back to Misc](./README.md)</sub>
