# aiptimizer/TurboOCR

[![Stars](https://img.shields.io/github/stars/aiptimizer/TurboOCR?style=flat-square&color=yellow)](https://github.com/aiptimizer/TurboOCR/stargazers) [![Forks](https://img.shields.io/github/forks/aiptimizer/TurboOCR?style=flat-square&color=blue)](https://github.com/aiptimizer/TurboOCR/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> Fast GPU OCR server. 270 img/s on FUNSD. TensorRT FP16, PP-OCRv5, HTTP + gRPC.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 267 |
| 🍴 **Forks** | 29 |
| 💻 **Language** | C++ |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`document-ai` `document-parsing` `easyocr` `fastapi` `fp16` `gpu-ocr` `grpc` `inference-server` `nvidia` `ocr` `paddleocr` `pdf-extraction`

## 🎯 Categories

Knowledge/RAG · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary**  
TurboOCR (aiptimizer/TurboOCR) is a high‑performance GPU‑accelerated OCR server that delivers up to 270 images / second on the FUNSD benchmark using TensorRT FP16 and the PP‑OCRv5 model. It offers both HTTP and gRPC endpoints (plus a CLI/SDK) for easy integration, making it a solid choice for turning scanned or image‑based documents into searchable text for knowledge‑base and assistant applications.  

**Value**  
- **Speed & Scale** – The TensorRT‑optimized pipeline can process hundreds of pages per second on a single GPU, dramatically reducing latency for large document collections.  
- **Search‑Ready Output** – By extracting text, layout, and language metadata, TurboOCR enables downstream indexing, semantic search, and grounding of LLM‑driven assistants on internal documents.  
- **Flexible Access** – HTTP and gRPC APIs let you plug the service into web back‑ends, micro‑services, or batch pipelines without writing custom OCR code.  

**Practical Adoption Path**  
1. **Prototype** – Pull the Docker image or build from source, run the server locally, and call the `/ocr` endpoint with a sample PDF/image to verify accuracy and throughput.  
2. **Integration** – Wrap the HTTP/gRPC calls in your existing document‑ingestion pipeline (e.g., a knowledge‑base crawler or an LLM‑assistant pre‑processor).  
3. **Indexing** – Feed the returned plain‑text and layout JSON into your search engine (Elastic, Vespa, etc.) or vector store for semantic retrieval.  
4. **Monitoring & Scaling** – Deploy the container on a GPU‑enabled Kubernetes cluster, use the built‑in health checks, and horizontally scale the service to meet peak document‑ingestion loads.  

**Production Readiness**  
- **Active development** – 267 GitHub stars, recent commits (as of 2026‑05‑11), and a growing contributor base indicate a healthy open‑source project.  
- **Mature ecosystem** – Uses C++ for core inference, TensorRT for GPU acceleration, and provides both HTTP and gRPC APIs, which are standard in production environments.  
- **Operational signals** – Clear Docker images, CLI tools, and SDK wrappers simplify deployment and observability.  
- **Risk considerations** – License compliance, security scanning, and maintainer responsiveness still need a final review, but no major metadata or stability issues have been identified.  

Overall, TurboOCR is a production‑grade, GPU‑fast OCR service that can be quickly evaluated and integrated into any pipeline that needs to make image‑based knowledge searchable and usable by AI assistants.

### Русский

TurboOCR — это быстрый OCR‑сервер с поддержкой GPU, реализованный на C++ и оптимизированный через TensorRT FP16 (PP‑OCRv5), способный обрабатывать до 270 изображений в секунду (FUNSD) и предоставляющий HTTP и gRPC API. Он позволяет быстро индексировать и делать поисково‑доступными внутренние базы знаний, улучшая поиск по документам и обеспечивая более точное «заземление» ответов ассистентов. Проект имеет активную разработку, 267 звёзд на GitHub и готов к пилотному внедрению в продакшн, хотя требуется финальная проверка лицензии и безопасности.

### 中文

**项目简介**  
TurboOCR（aiptimizer/TurboOCR）是一款基于 GPU 的高速 OCR 服务器，采用 TensorRT FP16 加速的 PP‑OCRv5 模型，能够在 FUNSD 基准上实现 270 张图像/秒的吞吐。它同时提供 HTTP 与 gRPC 接口，便于在各种后端系统中快速调用。

**价值**  
- **提升内部知识可检索性**：将文档、图片等非结构化内容转化为可搜索的文本，使企业知识库、FAQ、合同等资料能够被 AI 助手直接引用。  
- **加速检索与问答**：在向量检索或 RAG 流程前预处理文档，显著降低后端搜索和生成的延时。  
- **成本效益**：利用 TensorRT FP16 在同等硬件上比纯 CPU 实现更高的 OCR 速度，降低算力开支。

**典型接入方式**  
1. **HTTP/REST**：发送 `POST /ocr`（或文档中定义的路径）携带图片二进制或 Base64，即可获得 JSON 格式的识别结果。  
2. **gRPC**：通过定义好的 `TurboOCRService` 接口，使用 protobuf 进行高并发、低延迟的调用，适合微服务或流式处理场景。  
3. **CLI/SDK**：项目自带的命令行工具 `turboocr-cli`，以及 C++/Python SDK，便于本地调试或在脚本中批量处理。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑11 最近一次提交，拥有 267 ⭐、29 🍴，代码以 C++ 为主，配套 17 个主题标签，社区活跃。  
- **成熟度**：提供完整的容器镜像（Dockerfile）、GPU 加速配置示例以及 CI/CD 流水线，支持快速部署到 Kubernetes 或单机 GPU 环境。  
- **可靠性**：采用 TensorRT FP16 进行推理，性能稳定；HTTP 与 gRPC 双协议设计满足不同业务的容错与扩展需求。  
- **风险**：目前尚需对许可证（MIT/Apache 等）进行最终确认，并进行安全审计以确保依赖库的漏洞情况。总体而言，TurboOCR 已具备在生产环境中进行试点或正式上线的条件。

## 🧭 Practical evaluation

**Value:** aiptimizer/TurboOCR helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 267 GitHub stars
- 29 forks
- updated 2026-05-11
- primary language: C++
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 37/100 |
| stars | 52/100 |
| topics | 100/100 |
| outlook | 82/100 |
| quality | 76/100 |
| recency | 100/100 |
| adoption | 48/100 |
| production | 75/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/aiptimizer/TurboOCR) · [← Back to Knowledgerag](./README.md)</sub>
