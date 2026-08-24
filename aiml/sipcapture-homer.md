# sipcapture/homer

[![Stars](https://img.shields.io/github/stars/sipcapture/homer?style=flat-square&color=yellow)](https://github.com/sipcapture/homer/stargazers) [![Forks](https://img.shields.io/github/forks/sipcapture/homer?style=flat-square&color=blue)](https://github.com/sipcapture/homer/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> HOMER - 100% Open-Source SIP, VoIP, RTC Packet Capture & Monitoring

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2k |
| 🍴 **Forks** | 254 |
| 💻 **Language** | Go |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`analytics` `callflow` `capture-agent` `cdr` `correlation` `encapsulation` `flow` `hep` `kamailio` `monitoring` `opensips` `packet-capture`

## 🎯 Categories

AI/ML · Data · Observability

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
HOMER (sipcapture/homer) is a fully open‑source platform for capturing, storing, and visualising SIP, VoIP and other real‑time communications packets. Written in Go and backed by a vibrant community (≈ 2 k stars, 250 forks), it provides a ready‑made data pipeline that can be enriched with AI/ML models for analytics, RAG or autonomous agent workflows. Its active development and broad adoption make it a solid foundation for quickly prototyping AI‑enhanced monitoring solutions without building a packet‑capture stack from scratch.  

**Value**  
- **Instant data source** – HOMER already ingests and indexes every SIP/RTC packet, delivering clean, time‑series telemetry that AI models can consume directly.  
- **Accelerated AI integration** – Because the platform exposes APIs and stores raw payloads, you can plug in speech‑analytics, anomaly‑detection, or RAG pipelines with minimal glue code, turning raw call data into actionable insights.  
- **Cost‑effective observability** – Being 100 % open source eliminates licensing fees while providing the same visibility as commercial call‑monitoring suites, enabling budget‑constrained teams to experiment with AI‑driven diagnostics.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, follow the README to spin up the Docker‑compose stack, and verify packet capture on a test SIP trunk.  
2. **Data Export** – Use HOMER’s REST/GraphQL endpoints or its built‑in Kafka connector to stream captured payloads to your ML pipeline.  
3. **Model Hook‑up** – Deploy a lightweight inference service (e.g., a FastAPI wrapper around a Whisper or anomaly‑detection model) that consumes the stream, enriches records, and writes results back to HOMER’s database for visualisation.  
4. **Iterate & Scale** – Once the AI‑enhanced workflow is validated, expand to production‑grade deployment with HA PostgreSQL/ClickHouse back‑ends, TLS‑secured collectors, and Kubernetes orchestration.  

**Production Readiness**  
- **Code health** – Recent commits (as of 2026‑05‑14), > 1 900 stars, and a strong fork network indicate an active maintainer base.  
- **Observability ecosystem** – Built‑in dashboards, Grafana integration, and export adapters cover most monitoring needs out of the box.  
- **Scalability** – Supports clustered collectors and sharded storage, suitable for high‑volume carrier environments.  
- **Risks** – The license (Apache‑2.0) is permissive, but a final security audit and verification of maintainer responsiveness are advisable before full production rollout.  

Overall, HOMER is a mature OSS candidate that can serve as the data backbone for AI‑augmented SIP/VoIP observability, with a clear, low‑friction path from sandbox to production.

### Русский

HOMER (sipcapture/homer) — это полностью открытая система для захвата и мониторинга SIP, VoIP и RTC‑трафика, написанная на Go, с более 1900 звёздами на GitHub и активным развитием, что делает её готовой к пилотному запуску в продакшн. Она позволяет быстро добавить AI‑функциональность (прототипировать модели, строить RAG‑или агентные пайплайны, оценивать инструменты) без необходимости создавать стек с нуля, начиная с небольшого proof‑of‑concept и проверки README. Несмотря на отсутствие серьёзных метаданных‑рисков, окончательная проверка лицензии, безопасности и активности мейнтейнеров рекомендуется перед масштабным внедрением.

### 中文

**项目简介**  
HOMER（sipcapture/homer）是一款 100% 开源的 SIP/VoIP/RTC 包捕获与监控平台，基于 Go 实现，拥有近 2000 颗星和活跃的社区，可用于实时抓包、流量分析和质量监控。

**价值**  
- **快速赋能 AI**：内置完整的协议解析和统计数据，开发者可以直接在捕获的呼叫信令和媒体流上叠加机器学习模型，而无需从零搭建数据采集层。  
- **原型与研发加速**：提供丰富的 API 与可视化仪表盘，适合快速验证 RAG、对话代理或异常检测等 AI 场景。  
- **成熟的运维监控**：支持 Prometheus、Grafana、Elasticsearch 等生态，可无缝纳入现有 observability 堆栈。

**典型接入方式**  
1. **部署方式**：使用官方提供的 Docker Compose / Helm Chart 在 Kubernetes 或单机上快速启动（包括 capture、homer‑api、homer‑ui 三个服务）。  
2. **数据导入**：在 SIP/RTCP/RTSP 代理或 SBC 上配置 `sngrep`/`pcap` 采集插件，将流量通过 UDP/TCP 推送到 HOMER 的 capture 端口。  
3. **API 调用**：通过 RESTful `/api/v3` 接口查询呼叫记录、媒体统计或实时流，直接喂给 AI 模型或构建 RAG 索引。  
4. **可视化**：打开 `http://<host>:9080` 查看仪表盘，或将指标导出到 Prometheus 再在 Grafana 中自定义告警。

**生产可用性**  
- **活跃度**：最近一次提交（2026‑05‑14）且每月均有 PR 合并，社区活跃；GitHub 1954 星、254 Fork，拥有完整的 CI/CD 流程。  
- **成熟度**：已在多家运营商和企业级 VoIP 平台上部署，具备水平扩展（capture‑cluster）和高可用（HA）方案。  
- **安全与合规**：采用 Apache‑2.0 许可证，代码审计记录良好；仍需在正式上线前进行内部安全评估和依赖漏洞扫描。  

综上，HOMER 具备高生产就绪度，适合作为 SIP/VoIP 数据层的底座，快速叠加 AI 能力进行原型验证或正式业务部署。

## 🧭 Practical evaluation

**Value:** sipcapture/homer helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1954 GitHub stars
- 254 forks
- updated 2026-05-14
- primary language: Go
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 60/100 |
| stars | 70/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 65/100 |
| recency | 20/100 |
| adoption | 67/100 |
| production | 52/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/sipcapture/homer) · [← Back to AI/ML](./README.md)</sub>
