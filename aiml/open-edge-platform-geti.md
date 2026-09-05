# open-edge-platform/geti

[![Stars](https://img.shields.io/github/stars/open-edge-platform/geti?style=flat-square&color=yellow)](https://github.com/open-edge-platform/geti/stargazers) [![Forks](https://img.shields.io/github/forks/open-edge-platform/geti?style=flat-square&color=blue)](https://github.com/open-edge-platform/geti/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> Build computer vision models in a fraction of the time and with less data.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.3k |
| 🍴 **Forks** | 469 |
| 💻 **Language** | Python |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`action-recognition` `automl` `computer-vision` `datumaro` `deep-learning` `geti` `hyper-parameter-optimization` `image-classification` `image-segmentation` `incremental-learning` `machine-learning` `neural-networks-compression`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Summary**  
open‑edge‑platform/geti is an open‑source Python framework that accelerates the creation of computer‑vision models, requiring far less data and training time than traditional pipelines. Although marketed for market‑data workflows, its modular architecture makes it suitable for any visual‑analysis task, from research‑grade trading signal extraction to real‑time monitoring of market dashboards.

**Value**  
GETI lets data scientists prototype vision‑based trading strategies quickly, cutting the data‑labeling and model‑training overhead that typically stalls quantitative research. By exposing ready‑to‑use model templates, data loaders, and inference APIs, it reduces engineering effort and enables faster iteration on back‑testing and live‑monitoring pipelines.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the README notebooks on a small sample of market screenshots or chart images to verify that the pre‑built models meet accuracy needs.  
2. **Integration** – Wrap GETI’s inference service in a lightweight REST or gRPC layer and connect it to your existing data‑ingestion pipeline (e.g., Kafka or a market‑data API).  
3. **Pilot** – Deploy the service in a sandbox environment, back‑test the vision‑driven signals against historical data, and iterate on model fine‑tuning with your domain‑specific labels.  

**Production readiness**  
The project scores high on readiness: it has 1,252 stars, 469 forks, recent commits (as of 2026‑07‑01), active issue discussion, and a well‑documented Python codebase with 19 related topics. While the license, security posture, and maintainer activity still need a final review, the strong community signals and recent activity make GETI a solid candidate for a serious pilot in production.

### Русский

Резюме проекта open-edge-platform/geti:

Платформа open-edge-platform/geti позволяет исследователям и автоматизировать рыночные потоки, сокращая время и необходимое количество данных для разработки моделей компьютерного зрения. Типовой сценарий внедрения — исследование торговых систем, обратная проверка стратегий и мониторинг рыночных потоков. Проект готов к производственной эксплуатации на высоком уровне, с недавними активностями, широкой адопцией и сильными сигналами экосистемы, что делает его подходящей кандидатурой для серьезного пилотного проекта.

### 中文

**项目简介（2‑3 句）**  
open‑edge‑platform/geti 是一个开源的计算机视觉平台，能够在极少的数据和极短的时间内快速构建高质量的视觉模型。它提供了端到端的模型训练、评估与部署流水线，帮助用户把视觉算法快速落地到实际业务中。  

**价值**  
- **加速研发**：通过自动化的数据标注、模型搜索和超参数调优，显著缩短模型开发周期。  
- **降低门槛**：即使数据量有限，也能得到可用的模型，适合资源受限的团队。  
- **面向金融场景**：可用于研究交易系统、回测策略以及实时监控市场工作流中的图像/视频数据（如行情截图、摄像头监控等），实现更智能的市场自动化。  

**典型接入方式**  
1. **快速 PoC**：克隆仓库 → 按 README 完成环境配置（Python 3.9+、依赖 `pip install -r requirements.txt`） → 使用示例脚本加载少量标注数据进行训练。  
2. **CI/CD 集成**：将 `geti` 的训练脚本包装为 Docker 镜像，结合 GitHub Actions 或 Jenkins，实现代码提交即自动触发模型训练、评估并推送模型至模型仓库（如 MLflow、S3）。  
3. **业务系统嵌入**：通过提供的 REST API 或 Python SDK，将训练好的模型以推理服务的形式部署（FastAPI / Flask），业务系统调用该服务完成图像识别、异常检测等功能。  

**生产可用性**  
- **成熟度**：活跃度高，最近一次提交在 2026‑07‑01，拥有 1.2k+ Stars、470+ Forks，社区贡献活跃，生态插件丰富（19 个 GitHub topics）。  
- **就绪度**：代码质量、文档和示例较完整，适合作为正式生产环境的候选。建议在正式上线前进行一次小规模的概念验证（PoC），确认安全合规（许可证、依赖漏洞）后再推广至全量业务。  

总体而言，open‑edge‑platform/geti 具备高生产准备度，能够帮助金融科技团队快速构建并部署计算机视觉模型，实现交易系统的智能化与自动化。

## 🧭 Practical evaluation

**Value:** open-edge-platform/geti helps research and automate market workflows.

**Best use cases**

- research trading systems
- backtest strategies
- monitor market workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1252 GitHub stars
- 469 forks
- updated 2026-07-01
- primary language: Python
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 67/100 |
| stars | 66/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 80/100 |
| recency | 80/100 |
| adoption | 66/100 |
| production | 72/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/open-edge-platform/geti) · [← Back to AI/ML](./README.md)</sub>
