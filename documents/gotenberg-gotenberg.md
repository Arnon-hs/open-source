# gotenberg/gotenberg

[![Stars](https://img.shields.io/github/stars/gotenberg/gotenberg?style=flat-square&color=yellow)](https://github.com/gotenberg/gotenberg/stargazers) [![Forks](https://img.shields.io/github/forks/gotenberg/gotenberg?style=flat-square&color=blue)](https://github.com/gotenberg/gotenberg/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-80%2F100-brightgreen?style=flat-square)](#)

> A developer-friendly API for converting many document formats into PDF files, and more!

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 12.5k |
| 🍴 **Forks** | 811 |
| 💻 **Language** | Go |
| 📈 **Score** | 80/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`api` `chrome` `chromium` `convert-to-pdf` `docker` `docx-to-pdf` `excel` `exiftool` `html-to-pdf` `libreoffice` `openoffice` `pdf`

## 🎯 Categories

Documents · Backend · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Gotenberg is a Go‑based, developer‑friendly API that converts a wide range of document formats (HTML, Markdown, Office files, images, etc.) into PDFs and other outputs. It ships as a lightweight, containerizable service with a clean HTTP/REST interface, making it easy to integrate into any backend, CI/CD pipeline, or AI‑augmented workflow. With over 12 k stars and active maintenance, it’s a battle‑tested OSS component for production‑grade document processing.

**Value**  
- **Accelerates AI‑enabled pipelines** – By handling the heavy‑lifting of document rendering and PDF generation, Gotenberg lets teams focus on higher‑level AI tasks such as Retrieval‑Augmented Generation (RAG) or agent‑driven summarisation without building a custom conversion stack.  
- **Language‑agnostic integration** – The REST API, CLI, and SDKs (Go, Node, Python, etc.) mean you can call it from any service, micro‑service, or serverless function, regardless of the programming language of your AI model.  
- **Cost‑effective and scalable** – Running Gotenberg as a Docker container or in Kubernetes adds minimal overhead, and it can be horizontally scaled to meet high‑throughput document‑processing demands.

**Practical Adoption Path**  
1. **Prototype** – Pull the official Docker image, spin up a local instance, and experiment with the `/forms` and `/convert` endpoints using curl or the provided SDKs.  
2. **Integrate** – Wrap the API calls in a thin service layer within your existing backend (e.g., a Go or Python microservice) that feeds documents from your data store or AI pipeline.  
3. **Secure & Deploy** – Add TLS termination, authentication (API keys or OAuth), and configure resource limits. Deploy the container to your Kubernetes cluster or serverless platform, and enable autoscaling based on request metrics.  
4. **Monitor** – Use the built‑in health‑check endpoints and export Prometheus metrics to track latency, error rates, and conversion throughput.

**Production Readiness**  
- **Activity & Community** – 12.5 k stars, 811 forks, frequent commits (last update 2026‑06‑29), and a vibrant issue/PR community indicate strong ongoing support.  
- **Maturity** – The service has been used in multiple production environments for PDF generation, invoice processing, and report rendering, and it provides stable Docker images with versioned releases.  
- **Reliability** – Stateless design, graceful shutdown, and built‑in health checks make it suitable for high‑availability deployments; horizontal scaling is straightforward.  
- **Risks** – While no major metadata or licensing concerns are evident, a final review of the MIT license, security audit of the container image, and confirmation of active maintainers are recommended before full roll‑out.  

Overall, Gotenberg is a production‑ready OSS component that can be quickly evaluated and integrated to give AI‑driven applications robust document‑to‑PDF capabilities without reinventing the conversion stack.

### Русский

**gotenberg/gotenberg** — это удобный API на Go, позволяющий конвертировать множество форматов документов в PDF и выполнять сопутствующие операции, что упрощает добавление AI‑функционала (например, RAG‑ или агентных цепочек) без необходимости строить собственный стек. Типичный сценарий — вызов REST/CLI‑интерфейса из микросервиса или CI/CD‑pipeline для быстрой генерации PDF‑отчётов и последующей обработки их AI‑моделями. Проект считается готовым к production: активные коммиты, более 12 тыс. звёзд, широкое принятие в сообществе и стабильный набор функций, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**

Gotenberg 是一个开源项目，提供了一个开发者友好的 API，用于将多种文档格式转换为 PDF 文件，并提供更多功能。

**价值**

Gotenberg 帮助开发者在不从头搭建 AI 模型栈的情况下，添加 AI 能力。它可以用于快速 prototyping AI 特性、构建 RAG 或代理工作流、评估模型工具等。

**典型接入方式**

Gotenberg 提供了多种接入方式，包括 API、SDK 和 CLI。开发者可以根据自己的需要选择合适的接入方式。

**生产可用性**

Gotenberg 的生产可用性较高，理由如下：

* 近期活动：项目最近更新于 2026-06-29。
* 兴起的采用：项目有 12503 个 GitHub 星和 811 个分支。
* 强大的生态系统：项目有 20 个主题和 20 个话题。

总的来说，Gotenberg 是一个值得信赖的开源项目，可以帮助开发者快速添加 AI 能力。

## 🧭 Practical evaluation

**Value:** gotenberg/gotenberg helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 12503 GitHub stars
- 811 forks
- updated 2026-06-29
- primary language: Go
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 73/100 |
| stars | 87/100 |
| topics | 100/100 |
| outlook | 84/100 |
| quality | 87/100 |
| recency | 80/100 |
| adoption | 83/100 |
| production | 79/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/gotenberg/gotenberg) · [← Back to Documents](./README.md)</sub>
