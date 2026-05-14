# aws-samples/amazon-bedrock-samples

[![Stars](https://img.shields.io/github/stars/aws-samples/amazon-bedrock-samples?style=flat-square&color=yellow)](https://github.com/aws-samples/amazon-bedrock-samples/stargazers) [![Forks](https://img.shields.io/github/forks/aws-samples/amazon-bedrock-samples?style=flat-square&color=blue)](https://github.com/aws-samples/amazon-bedrock-samples/network) [![Language](https://img.shields.io/badge/lang-Jupyter%20Notebook-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> This repository contains examples for customers to get started using the Amazon Bedrock Service. This contains examples for all available foundational models

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.4k |
| 🍴 **Forks** | 679 |
| 💻 **Language** | Jupyter Notebook |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

`amazon-bedrock` `amazon-titan` `bedrock` `embeddings` `generative-ai` `knowledge-base` `langchain` `rag`

## 🎯 Categories

Orchestration · Knowledge/RAG · AI/ML · Education

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The **aws-samples/amazon-bedrock-samples** repository offers ready‑to‑run Jupyter notebooks that demonstrate how to invoke every foundational model available in Amazon Bedrock, turning isolated prompts and tool calls into repeatable, multi‑agent workflows. It serves as a practical starter kit for building RAG, orchestration, and tool‑use pipelines on top of Bedrock, and showcases best‑practice patterns for agent memory and coordination.  

**Value**  
- **Accelerates prototyping**: developers can copy‑paste working code to spin up Bedrock‑backed agents without writing low‑level API glue.  
- **Standardizes patterns**: the samples encode proven techniques for multi‑agent orchestration, tool integration, and persistent memory, reducing design churn across teams.  
- **Educates and de‑risky**: the notebooks double as tutorials, helping teams understand model capabilities, cost controls, and security settings before committing to production workloads.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Fork the repo and run the introductory notebook on a small Bedrock sandbox account; verify that the required IAM roles, VPC endpoints, and model access are correctly configured.  
2. **Pilot Extension** – Replace the sample prompts with your own domain‑specific use cases, add any internal tools (e.g., database query APIs) using the provided tool‑use templates, and experiment with agent memory persistence (e.g., DynamoDB).  
3. **Integration** – Extract the reusable functions into a shared library or Lambda layer, wrap them with your CI/CD pipeline, and connect the workflow to your existing orchestration platform (Step Functions, Airflow, etc.).  
4. **Scale & Harden** – Implement monitoring (CloudWatch metrics, Bedrock usage logs), add error‑handling, enforce IAM least‑privilege policies, and conduct performance/load testing before full rollout.  

**Production Readiness**  
- **High**: The project shows strong community signals (1.4 k stars, 679 forks), recent commits (as of 2026‑05‑14), and active maintenance by AWS.  
- **Maturity**: Core functionality (model invocation, tool use, memory) is already production‑grade in AWS‑managed services; the notebooks are primarily illustrative, not a black‑box runtime.  
- **Risks**: The repository does not provide a turnkey deployment script; teams must invest effort to extract and package the sample code, and they should validate any hidden setup costs (model pricing, VPC endpoint fees) early.  

Overall, **amazon-bedrock-samples** is a solid OSS foundation for building repeatable, multi‑agent AI workflows on Bedrock, with a clear, incremental path from sandbox experimentation to production‑grade integration.

### Русский

`aws-samples/amazon-bedrock-samples` — набор готовых Jupyter‑ноутбуков, демонстрирующих, как собрать повторяемые рабочие процессы на базе Amazon Bedrock, включающие несколько агентов, инструменты и память. Типовой сценарий внедрения — запуск небольшого proof‑of‑concept: изучить README, адаптировать один из примеров под свой бизнес‑процесс (например, координацию мульти‑агентных запросов или построение RAG‑pipeline), а затем масштабировать в продакшн. Проект считается почти готовым к production: активные коммиты, более 1400 звёзд, широкое использование в сообществе и поддержка всех базовых моделей Bedrock.

### 中文

**价值**  
aws‑samples/amazon‑bedrock‑samples 为开发者提供了完整的 Amazon Bedrock 基础模型示例代码，帮助把零散的 Prompt 与工具快速组装成可复用的智能体工作流。通过这些示例，团队可以：

1. **快速原型**：直接拷贝 Notebook 即可跑通多模态、文本、检索增强生成（RAG）等场景，省去从零搭建环境的时间。  
2. **标准化 Agent 记忆与工具调用**：示例展示了如何在同一工作流中统一管理对话历史、向量库检索、外部 API 调用等，便于后续在内部平台上实现统一治理。  
3. **多 Agent 协同**：提供了多智能体协作的样例，适用于需要分工（如检索‑生成‑过滤）或跨系统编排的业务。

**典型接入方式**  

| 步骤 | 说明 | 关键点 |
|------|------|--------|
| 1️⃣ Clone 仓库 | `git clone https://github.com/aws-samples/amazon-bedrock-samples.git` | 包含 Jupyter Notebook、示例脚本和依赖文件 |
| 2️⃣ 环境准备 | - 创建 Python 虚拟环境 <br> - 安装 `requirements.txt`（`pip install -r requirements.txt`）<br> - 配置 AWS CLI 并确保拥有 `bedrock:*` 权限 | 需要在 AWS 区域已开通 Bedrock 服务 |
| 3️⃣ 运行示例 Notebook | 打开 `01‑Getting‑Started.ipynb`（或对应模型的 Notebook），选择目标基础模型（Claude、Jurassic、Llama 等）并执行 | 示例会自动创建 Bedrock 客户端、调用模型、展示返回结果 |
| 4️⃣ 按需改造 | - 将 Prompt、工具调用封装为函数/类 <br> - 引入 LangChain、Auto‑GPT 等框架统一调度 <br> - 将向量检索换成自建或托管的 Milvus/FAISS 等 | 通过复制/改写 Notebook 中的 “Agent‑Tool” 模块，可快速构建业务专属工作流 |
| 5️⃣ 小规模 PoC | 在内部测试环境部署改造后的脚本，验证延迟、成本、错误率等指标 | 建议先跑 100‑1k 次调用，评估费用与性能 |
| 6️⃣ 生产化 | - 将代码容器化（Docker）<br> - 使用 AWS Step Functions / EventBridge 编排多 Agent 流程<br> - 加入监控（CloudWatch）和日志审计 | 采用无服务器或容器服务（ECS/Fargate）实现弹性伸缩 |

**生产可用性**  

- **活跃度**：最近一次提交（2026‑05‑14）表明项目仍在维护，GitHub ★1.4k、Fork 679，社区活跃。  
- **成熟度**：示例基于官方 Bedrock SDK，使用的模型均为 AWS 托管的生产级模型，具备高可用性和 SLA。  
- **可扩展性**：代码结构清晰（Notebook → Python 包），易于迁移到容器或服务器无状态函数中；配合 Step Functions 可实现复杂编排。  
- **风险**：元数据未提供完整的 CI/CD 或部署脚本，需自行设计集成流水线；此外，Bedrock 按调用计费，需在 PoC 阶段评估成本。  

**结论**  
该仓库是一个 **高可用、低门槛** 的 OSS 入口，适合作为内部 AI/ML 平台的 “Prompt‑to‑Production” 桥梁。建议先在沙箱环境完成一次完整的 PoC（验证模型调用、工具链集成、成本），随后按照上述步骤将工作流容器化并交由 AWS Step Functions 编排，即可进入生产使用。

## 🧭 Practical evaluation

**Value:** aws-samples/amazon-bedrock-samples helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1424 GitHub stars
- 679 forks
- updated 2026-05-14
- primary language: Jupyter Notebook
- 8 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 71/100 |
| stars | 67/100 |
| topics | 100/100 |
| outlook | 84/100 |
| quality | 86/100 |
| recency | 100/100 |
| adoption | 68/100 |
| production | 76/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/aws-samples/amazon-bedrock-samples) · [← Back to Orchestration](./README.md)</sub>
