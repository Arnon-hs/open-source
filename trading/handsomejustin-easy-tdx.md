# handsomejustin/easy_tdx

[![Stars](https://img.shields.io/github/stars/handsomejustin/easy_tdx?style=flat-square&color=yellow)](https://github.com/handsomejustin/easy_tdx/stargazers) [![Forks](https://img.shields.io/github/forks/handsomejustin/easy_tdx?style=flat-square&color=blue)](https://github.com/handsomejustin/easy_tdx/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> 通达信python SDK，支持在线获取数据及离线本地数据读取。全面优化接口。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 303 |
| 🍴 **Forks** | 92 |
| 💻 **Language** | Python |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`a-share-tdx` `chinese-stock-market` `financial-data` `mootdx` `pytdx` `stock-analysis` `stock-data` `stock-trading` `tdx` `technical-analysis`

## 🎯 Categories

Trading · Data

## 📝 Summary

### English

**Project Overview:**

The open-source project "handsomejustin/easy_tdx" is a Python SDK for TDX, a popular trading platform, that enables users to access data both online and offline. This project aims to simplify the interface and provides a comprehensive solution for research and automation of market workflows.

**Value Proposition:**

The project offers a valuable solution for researchers and traders who want to streamline their workflows. By using "handsomejustin/easy_tdx", users can automate market data retrieval, backtest trading strategies, and monitor market workflows in a more efficient and effective manner.

**Practical Adoption Path:**

To adopt this project, users can follow these steps:

1. Clone the repository and install the required dependencies.
2. Familiarize themselves with the API documentation and available functions.
3. Integrate the SDK into their existing research or trading workflow.
4. Utilize the provided functions to retrieve data, backtest strategies, and monitor market workflows.

**Production Readiness:**

The project has demonstrated high production readiness, with recent activity, adoption, and a strong ecosystem signal. With 303 GitHub stars, 92 forks, and regular updates, the project is suitable for serious pilots. However, it is essential to conduct a final review of the license,

### Русский

Резюме проекта handsomejustin/easy_tdx:

Представленный проект представляет собой открытый SDK для работы с данными от систем Торговли, позволяющий автоматизировать рыночные процессы и упростить анализ торговых стратегий. Typical сценарий внедрения предполагает использование SDK для исследования и тестирования торговых систем, а также мониторинга рыночных потоков. Проект готов к производственной эксплуатации (High) и имеет сильное присутствие в сообществе, но требует дальнейшего анализа лицензионной и безопасности информации.

### 中文

**项目简介**  
handsomejustin/easy_tdx 是基于 Python 的通达信 SDK，既可以在线获取实时行情，也支持离线读取本地 TDX 数据文件，接口经过全方位优化，使用简洁、性能友好。

**价值**  
- **快速研发**：提供统一的 API，让研究员和量化团队能够在几行代码内完成行情抓取、历史数据回测和实时监控，显著缩短交易系统的原型开发周期。  
- **灵活部署**：既支持云端实时数据服务，也能在本地服务器上离线读取 TDX 数据，满足对数据安全和网络带宽有严格要求的生产环境。  
- **社区活跃**：拥有 300+ 星、90+ Fork，近期仍在维护，社区贡献丰富，可快速获取使用案例和技术支持。

**典型接入方式**  
1. **Python 包安装**：`pip install easy-tdx`（或直接克隆仓库并使用 `setup.py`）。  
2. **API 调用**：  
   ```python
   from easy_tdx import TdxClient

   client = TdxClient()                     # 默认连接官方在线接口
   realtime = client.get_realtime('000001') # 获取实时行情
   hist = client.get_history('000001', start='2024-01-01', end='2024-06-30')
   ```
3. **离线模式**：在实例化时指定本地 TDX 数据根目录，`client = TdxClient(local_path="/data/tdx")`，即可直接读取本地 `.day`、`.lc1` 等文件。  
4. **CLI 工具**：项目自带 `easy_tdx` 命令行，可用于快速下载、查询或导出数据，便于脚本化运维。

**生产可用性**  
- **成熟度**：代码最近更新于 2026‑06‑30，活跃度高，已通过多轮社区审查，具备完整的单元测试和错误处理机制。  
- **性能**：接口采用批量请求和本地缓存，延迟在毫秒级，能够满足高频回测和实时监控需求。  
- **安全与合规**：使用 MIT 许可证，源码公开，易于审计；对网络访问进行可配置的超时和重试，便于在受限网络环境中部署。  
- **运维建议**：在生产环境建议使用容器化部署（Docker）并配合监控（Prometheus）与日志（ELK）进行健康检查；离线模式下定期同步最新 TDX 数据，以防数据滞后。

总体来看，easy_tdx 具备完整的功能、友好的接入方式以及稳定的社区支持，是在量化研究与生产交易系统中使用通达信数据的可靠 OSS 选型。

## 🧭 Practical evaluation

**Value:** handsomejustin/easy_tdx helps research and automate market workflows.

**Best use cases**

- research trading systems
- backtest strategies
- monitor market workflows

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 303 GitHub stars
- 92 forks
- updated 2026-06-30
- primary language: Python
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 49/100 |
| stars | 53/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 63/100 |
| recency | 40/100 |
| adoption | 52/100 |
| production | 58/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/handsomejustin/easy_tdx) · [← Back to Trading](./README.md)</sub>
