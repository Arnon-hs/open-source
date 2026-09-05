# jones2000/HQChart

[![Stars](https://img.shields.io/github/stars/jones2000/HQChart?style=flat-square&color=yellow)](https://github.com/jones2000/HQChart/stargazers) [![Forks](https://img.shields.io/github/forks/jones2000/HQChart?style=flat-square&color=blue)](https://github.com/jones2000/HQChart/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> HQChart - H5, 微信小程序 沪深/港股/数字货币/期货/美股 K线图(kline),走势图,缩放,拖拽,十字光标,画图工具,截图,筹码图. 分析家语法,通达信语法,(麦语法),第3方数据替换接口

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.3k |
| 🍴 **Forks** | 823 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`candle` `candlestick` `candlestick-chart` `canvas` `chart` `china-stock` `h5` `html5` `javascript` `kline` `python` `stock`

## 🎯 Categories

Trading

## 📝 Summary

### English

**HQChart: A Powerful Open-Source Charting Tool for Market Analysis**

HQChart is an open-source charting library for H5 and WeChat Mini Programs, offering a wide range of technical analysis tools, including K-line charts, trend lines, zooming, and drawing capabilities. With its robust feature set and strong ecosystem signals, HQChart helps researchers and traders automate market workflows, backtest strategies, and monitor market trends.

**Value Proposition:**

The value proposition of HQChart lies in its ability to streamline market analysis and automation workflows, making it an essential tool for traders and researchers. By leveraging HQChart's features, users can:

* Research and backtest trading systems
* Monitor market trends and workflows
* Automate market analysis and decision-making processes

**Practical Adoption Path:**

To adopt HQChart, users can follow a step-by-step process:

1. Evaluate HQChart's features and documentation to determine its suitability for their specific use case.
2. Start with a small proof of concept to test HQChart's functionality and integration with their existing workflows.
3. Review the project's README and documentation to ensure a smooth integration process.
4. Once satisfied, integrate HQChart into their production environment, leveraging its robust feature set and strong ecosystem signals.

**Production Readiness

### Русский

HQChart — это открытая JavaScript‑библиотека для построения интерактивных K‑line и рыночных графиков (沪深/港股/数字货币/期货/美股) в H5 и WeChat‑мини‑приложениях, поддерживающая масштабирование, перетаскивание, кросс‑курсор, инструменты разметки, скриншоты и чип‑чарты, а также синтаксисы анализа (Analyst, TongDaXin, Mai). Типичный сценарий внедрения — интеграция небольшого proof‑of‑concept в существующую торговую платформу для визуализации рыночных данных, последующее расширение до автоматизированных исследовательских и бэктест‑модулей. По оценке готовности проекта, активные коммиты, более 3300 звёзд и 800 форков свидетельствуют о высокой готовности к production‑использованию после финального аудита лицензии и безопасности.

### 中文

**项目简介（2‑3 句）**  
HQChart 是一款基于 H5 与微信小程序的全功能金融行情图表库，支持沪深、港股、数字货币、期货、美股等多市场的 K 线、分时、缩放、拖拽、十字光标、绘图工具、截图及筹码图等特性，并兼容分析家、通达信、麦语法等多种公式语言，提供第三方数据替换接口，帮助开发者快速搭建专业的行情分析前端。

**价值**  
- **多市场统一视图**：一次接入即可展示全球主要交易所的实时/历史行情，降低跨市场开发成本。  
- **高度可定制**：内置丰富的绘图工具和公式解析器，支持自定义指标、策略回测和自动化交易信号生成。  
- **快速落地**：基于纯前端 JavaScript 实现，兼容 H5 与微信小程序，无需后端渲染，可直接嵌入现有交易系统或研究平台。

**典型接入方式**  
1. **npm / yarn 安装**：`npm install hqchart`（或 `yarn add hqchart`），在项目中 `import { KLineChart } from 'hqchart'`。  
2. **配置数据源**：通过提供符合接口的行情数据服务（REST、WebSocket 或第三方 API），在初始化时传入 `DataProvider`，即可实现实时行情推送。  
3. **初始化图表**：在页面的容器元素上调用 `new KLineChart(container, options)`，配置所需的市场、周期、公式等参数。  
4. **扩展功能**：使用内置的 `drawTool`, `crossCursor`, `chipMap` 等模块，或自行实现插件，实现策略回测、截图、图形标注等业务需求。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑30，项目拥有 3,341 星、823 Fork，最近一次提交在同日，说明社区仍在持续维护。  
- **技术成熟**：核心功能（K 线、分时、交互）已在多个商业交易平台上线，具备完整的单元测试和文档示例。  
- **集成门槛低**：仅需前端依赖，无后端强制要求，适合作为 MVP 或完整生产系统的行情层。  
- **风险点**：仍需自行审查许可证（MIT/Apache 等）以及依赖的第三方库安全性；建议在正式上线前进行安全扫描并确认维护者响应速度。  

综上，HQChart 在功能完整性、社区活跃度和前端易用性方面均表现出色，可作为金融行情前端的 OSS 候选，在小规模 PoC 验证后即可投入生产使用。

## 🧭 Practical evaluation

**Value:** jones2000/HQChart helps research and automate market workflows.

**Best use cases**

- research trading systems
- backtest strategies
- monitor market workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 3341 GitHub stars
- 823 forks
- updated 2026-06-30
- primary language: JavaScript
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 73/100 |
| stars | 75/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 83/100 |
| recency | 80/100 |
| adoption | 74/100 |
| production | 73/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/jones2000/HQChart) · [← Back to Trading](./README.md)</sub>
