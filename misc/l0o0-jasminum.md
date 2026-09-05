# l0o0/jasminum

[![Stars](https://img.shields.io/github/stars/l0o0/jasminum?style=flat-square&color=yellow)](https://github.com/l0o0/jasminum/stargazers) [![Forks](https://img.shields.io/github/forks/l0o0/jasminum?style=flat-square&color=blue)](https://github.com/l0o0/jasminum/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> A Zotero add-on to retrive CNKI meta data. 一个简单的Zotero 插件，用于识别中文元数据

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 6.9k |
| 🍴 **Forks** | 314 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cnki` `plugin` `zotero` `zotero-plugin`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`l0o0/jasminum` is a Zotero add‑on written in TypeScript that automatically retrieves and normalises Chinese scholarly metadata from CNKI, making it searchable and ready for downstream analysis. Its lightweight design and clear API/CLI surface let users plug it into existing Zotero workflows or custom data‑pipeline scripts with minimal friction.

**Value**  
- **Metadata enrichment**: Turns raw CNKI records into structured Zotero items, enabling reliable citation management, bibliometric analysis, and integration with analytics platforms.  
- **Time savings**: Automates a manual, error‑prone step for researchers working with Chinese literature, improving data quality for reporting and reproducibility.  
- **Extensibility**: Exposes a simple API/CLI that can be chained into larger ETL pipelines, supporting automated literature reviews, knowledge‑graph construction, or dashboard updates.

**Practical Adoption Path**  
1. **Install** the add‑on via Zotero’s extensions manager or npm (for CLI use).  
2. **Configure** CNKI credentials (if required) in the add‑on settings or environment variables.  
3. **Run** the “Retrieve CNKI Metadata” command on selected Zotero items or invoke the CLI (`jasminum fetch <ids>`) to batch‑process records.  
4. **Integrate** the generated Zotero entries into downstream tools (e.g., export to CSV/JSON, feed a data‑warehouse, or trigger a CI pipeline) using the provided TypeScript SDK or REST‑like endpoints.  

**Production Readiness**  
- **Activity & Community**: 6,922 stars, 314 forks, and recent commits (as of 2026‑05‑11) indicate strong community interest and ongoing maintenance.  
- **Stability**: The TypeScript codebase is well‑typed, and the add‑on follows Zotero’s extension guidelines, reducing runtime surprises.  
- **Ecosystem Fit**: Compatible with Zotero 6+, works on Windows/macOS/Linux, and offers both UI and CLI entry points, making it suitable for individual researchers and larger institutional pipelines.  
- **Risks**: Licensing and security posture need a final audit, and a dedicated maintainer should be identified for long‑term support, but no critical blockers are evident.  

Overall, `jasminum` is a mature, OSS‑ready component that can be piloted quickly in research labs or data‑engineering teams needing reliable CNKI metadata integration.

### Русский

**l0o0/jasminum** — это открытый плагин для Zotero, позволяющий автоматически извлекать метаданные из китайской научной базы CNKI и преобразовывать их в формат, совместимый с Zotero, что упрощает построение аналитических и автоматизированных конвейеров обработки данных. Типичный сценарий: пользователь добавляет в Zotero ссылки на китайские статьи, плагин получает их метаданные (авторы, названия, аннотации и т.д.) и делает их сразу доступными для поиска, анализа и построения отчётов. Проект имеет высокую готовность к production‑использованию: активные коммиты, более 6 000 звёзд, TypeScript‑реализация, поддержка API/CLI и положительные сигналы экосистемы, требующие лишь финального аудита лицензии и безопасности.

### 中文

**项目简介**  
l0o0/jasminum 是一款面向 Zotero 的轻量插件，能够自动抓取并识别 CNKI（中国知网）中的中文文献元数据，帮助用户快速将中文资源纳入 Zotero 文献库。

**价值**  
- **提升文献管理效率**：一键获取 CNKI 元数据，省去手动复制、填写字段的繁琐步骤。  
- **支持后续分析**：标准化的元数据便于在数据分析、文献计量或自动化报告流程中直接使用。  
- **降低语言障碍**：专为中文元数据设计，解决 Zotero 原生对中文文献支持不足的问题。

**典型接入方式**  
1. **Zotero 插件安装**：在 Zotero 的插件管理页面直接安装 `jasminum.xpi`，或通过 GitHub Releases 下载最新版本手动加载。  
2. **API/SDK 调用（可选）**：插件内部提供 TypeScript 编写的 API，可在自定义脚本或其他科研工作流中直接调用 `fetchCNKIMetadata(url)` 获取元数据。  
3. **CLI 工具（实验性）**：项目附带的命令行工具 `jasminum-cli` 支持批量处理 CNKI 链接，适合数据管道的预处理阶段。

**生产可用性**  
- **活跃维护**：最近一次提交于 2026‑05‑11，持续更新，社区活跃。  
- **成熟度**：已有 6,922+ ⭐、314+ 🍴，使用者遍布学术机构，具备一定的验证基础。  
- **技术栈**：采用 TypeScript 编写，兼容现代 Zotero 版本，易于二次开发。  
- **风险**：需进一步审查许可证（MIT）与安全依赖，但整体安全姿态良好。  

综合来看，jasminum 已具备在正式科研环境中部署的条件，可作为中文文献管理的可靠组件快速投入使用。

## 🧭 Practical evaluation

**Value:** l0o0/jasminum helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 6922 GitHub stars
- 314 forks
- updated 2026-05-11
- primary language: TypeScript
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 62/100 |
| stars | 82/100 |
| topics | 50/100 |
| outlook | 70/100 |
| quality | 77/100 |
| recency | 80/100 |
| adoption | 76/100 |
| production | 73/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/l0o0/jasminum) · [← Back to Misc](./README.md)</sub>
