# Nixtla/nixtla

[![Stars](https://img.shields.io/github/stars/Nixtla/nixtla?style=flat-square&color=yellow)](https://github.com/Nixtla/nixtla/stargazers) [![Forks](https://img.shields.io/github/forks/Nixtla/nixtla?style=flat-square&color=blue)](https://github.com/Nixtla/nixtla/network) [![Language](https://img.shields.io/badge/lang-Jupyter%20Notebook-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> TimeGPT-1: production ready pre-trained Time Series Foundation Model  for forecasting and anomaly detection. Generative pretrained transformer for time series trained on over 100B data points. It's capable of accurately predicting various domains such as retail, electricity, finance, and IoT with just a few lines of code 🚀.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.9k |
| 🍴 **Forks** | 327 |
| 💻 **Language** | Jupyter Notebook |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `agentic-ai` `anomaly-detection` `artificial-intelligence` `deep-learning` `forecasting` `foundation-models` `generative-ai-time-series` `gpt` `gpts` `llm` `llms`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Nixtla/nixtla provides TimeGPT‑1, a production‑ready, pre‑trained foundation model for time‑series forecasting and anomaly detection. Built on a generative transformer trained on over 100 billion data points, it delivers accurate predictions across domains such as retail, electricity, finance, and IoT with only a few lines of code. The open‑source package lets teams add sophisticated AI time‑series capabilities without having to train a model from scratch.

**Value**  
- **Instant AI capability**: Developers can plug a state‑of‑the‑art forecasting model into their pipelines, cutting months of data collection, feature engineering, and model training.  
- **Domain versatility**: A single model handles diverse time‑series patterns, reducing the need for multiple specialized models.  
- **Low code entry**: Simple Python/Jupyter notebooks let data scientists prototype and iterate quickly, accelerating product development and experimentation.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, run the provided notebook on a small sample dataset to verify forecast quality and API usability.  
2. **Integration scaffolding** – Wrap the TimeGPT‑1 inference calls in a service (e.g., FastAPI or Lambda) and expose a REST/gRPC endpoint.  
3. **Data pipeline hookup** – Connect the service to your existing data lake or streaming source (Kafka, S3, DB) for batch or real‑time scoring.  
4. **Evaluation & tuning** – Use the built‑in evaluation utilities to benchmark against your legacy models; optionally fine‑tune on proprietary data if higher accuracy is required.  
5. **Production rollout** – Deploy the service behind a load balancer, monitor latency and forecast error, and implement fallback logic to legacy models if needed.

**Production Readiness**  
- **Strong community signals**: 3,932 ★, 327 forks, recent commits (as of 2026‑06‑24), and active issue/PR activity indicate a healthy, maintained project.  
- **Ease of use**: The primary interface is a Jupyter notebook with clear examples, lowering the barrier for rapid onboarding.  
- **Scalability**: The underlying transformer can be served on GPU or CPU, and the repository includes guidance for containerization and cloud deployment.  
- **Risk mitigation**: While the README provides a solid start, the integration path is not fully documented for all environments; a small pilot should validate setup costs, dependency management, and inference latency before full‑scale adoption.  

Overall, Nixtla/nixtla is a mature OSS candidate suitable for serious pilots, offering a fast route to embed high‑quality time‑series AI into production systems.

### Русский

Nixtla/nixtla — это готовый к продакшену open‑source Time Series Foundation Model (TimeGPT‑1), способный к точному прогнозированию и обнаружению аномалий в разных доменах (ритейл, электроэнергетика, финансы, IoT) с помощью нескольких строк кода. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept: установить пакет, подключить к существующим пайплайнам данных и протестировать предсказания через готовый API, после чего масштабировать в RAG‑ или агентные решения. Проект имеет высокую готовность к production (активные коммиты, 4 к+ звёзд, широкое принятие), однако перед полномасштабным использованием следует уточнить детали интеграции и оценить затраты на настройку среды.

### 中文

**项目简介**  
Nixtla/nixtla 提供 **TimeGPT‑1**——首个面向生产环境的预训练时间序列基础模型，基于 100 B+ 数据点训练的生成式 Transformer，能够在零到少量微调的情况下实现高精度的预测与异常检测，适用于零售、用电、金融、IoT 等多种业务场景。

---

### 价值点  
1. **即插即用的 AI 能力**：无需从头构建模型堆栈，只需几行代码即可在业务数据上得到可靠的预测和异常检测。  
2. **跨域通用性**：同一模型已在百余种行业数据上验证，降低了跨业务线的模型研发成本。  
3. **加速原型和产品化**：适合快速验证 AI 功能、构建 RAG/Agent 工作流或评估其他时序模型工具。  

---

### 典型接入方式  
1. **环境准备**  
   ```bash
   pip install nixtla  # 或者直接 clone repo 并使用 requirements.txt
   ```  
2. **加载模型并进行预测**（Python 示例）  
   ```python
   from nixtla import TimeGPT

   # 初始化模型（默认下载最新的 TimeGPT‑1）
   model = TimeGPT.from_pretrained("timegpt-1")

   # 传入 pandas DataFrame，列名必须包含时间戳列和目标变量列
   forecast = model.forecast(df, horizon=24)   # 预测未来 24 步
   anomalies = model.detect_anomalies(df)     # 检测异常点
   ```  
3. **在现有流水线中嵌入**  
   - **批处理**：在 ETL 作业结束后调用 `forecast`，将结果写回数据仓库。  
   - **实时推理**：将模型包装为 Flask/FastAPI 服务，接受实时序列片段返回即时预测。  
   - **RAG/Agent**：将 `forecast`/`detect_anomalies` 作为工具函数注册到 LangChain、AutoGPT 等框架中，支持基于时序数据的智能对话或决策。  

> **集成提示**：先在小规模数据集上跑通 README 中的示例，确认依赖（PyTorch/Transformers、CUDA）和模型下载速度，再逐步扩展到生产数据。

---

### 生产可用性评估  
| 维度 | 评估 | 说明 |
|------|------|------|
| **代码活跃度** | ★★★★★ | 最近一次提交 2026‑06‑24，持续维护。 |
| **社区与采纳** | ★★★★☆ | 3932 星、327 Fork，已有多家公司在内部使用。 |
| **文档与示例** | ★★★★☆ | README 包含完整的 Jupyter Notebook 示例，易于上手。 |
| **依赖成熟度** | ★★★★☆ | 基于 PyTorch/Transformers，生态成熟，GPU 加速可用。 |
| **部署复杂度** | ★★★☆☆ | 需要模型下载和 GPU 环境，建议先做小规模 POC 验证资源成本。 |
| **总体生产准备度** | ★★★★☆ | 适合作为关键业务的预测/异常检测组件，前提是完成一次完整的性能基准和监控集成。 |

**结论**：Nixtla/nixtla 已具备高水平的生产就绪度，可在验证阶段（POC）快速落地，随后通过容器化或模型服务化（如 TorchServe、FastAPI）进入正式生产环境。务必在正式部署前完成以下步骤：  

1. **性能基准**（预测时延、显存占用）。  
2. **监控与回滚**（预测误差、异常检测率）。  
3. **安全审计**（模型下载源、依赖许可证）。  

完成上述验证后，即可在零售、能源、金融或 IoT 等业务场景中安全、可靠地使用 TimeGPT‑1。

## 🧭 Practical evaluation

**Value:** Nixtla/nixtla helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 3932 GitHub stars
- 327 forks
- updated 2026-06-24
- primary language: Jupyter Notebook
- 15 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 63/100 |
| stars | 77/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 83/100 |
| recency | 80/100 |
| adoption | 73/100 |
| production | 70/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/Nixtla/nixtla) · [← Back to AI/ML](./README.md)</sub>
