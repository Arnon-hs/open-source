# smg-project/smg

[![Stars](https://img.shields.io/github/stars/smg-project/smg?style=flat-square&color=yellow)](https://github.com/smg-project/smg/stargazers) [![Forks](https://img.shields.io/github/forks/smg-project/smg?style=flat-square&color=blue)](https://github.com/smg-project/smg/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> Engine-agnostic LLM gateway in Rust. Full OpenAI & Anthropic API compatibility across vLLM, TRT-LLM, TokenSpeed, SGLang, OpenAI, Gemini & more. Industry-first gRPC pipeline, KV cache-aware routing, chat history, tokenization caching, Responses API, embeddings, WASM plugins, MCP, and multi-tenant auth.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 429 |
| 🍴 **Forks** | 129 |
| 💻 **Language** | Rust |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anthropic` `anthropic-api` `chat` `claude` `gemini` `inference-gateway` `lightseek` `llm` `mcp` `openai` `responses-api` `routing`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · Backend · Security

## 📝 Summary

### English

smg-project/smg is an engine‑agnostic LLM gateway written in Rust that provides full OpenAI and Anthropic API compatibility across a wide range of back‑ends (vLLM, TRT‑LLM, TokenSpeed, SGLang, Gemini, etc.) while adding advanced features such as gRPC pipelines, KV‑cache‑aware routing, chat‑history handling, tokenization caching, embeddings, WASM plugins, MCP support, and multi‑tenant auth. This enables teams to turn isolated prompts and tool calls into repeatable, multi‑agent workflows with standardized memory and tool‑use pipelines, simplifying evaluation via clear API/SDK/CLI signals. With strong recent activity, a growing ecosystem (429★, 129 forks, updated 2026‑08‑01), and high production‑readiness signals, it is suitable for a serious pilot after a final review of license, security, and maintainer health.

### Русский

smg‑project/smg — это engine‑agnostic шлюз LLM на Rust, обеспечивающий полную совместимость с API OpenAI и Anthropic для vLLM, TRT‑LLM, TokenSpeed, SGLang, Gemini и др., а также добавляющий gRPC‑pipeline, кэширование KV‑кеша и токенизации, историю чата, Responses API, эмбеддинги, WASM‑плагины и мультитенантную аутентификацию. Типовой сценарий — интеграция шлюза в существующую инфраструктуру для координации многоагентных рабочих процессов, стандартизации инструментов и памяти агентов, что позволяет превращать разрозненные промпты в повторяемые workflows. Благодаря активной разработке (обновлено 2026‑08‑01), 429★/129★, сильным экосистемным сигналам и

### 中文

smg-project/smg 是一种基于 Rust 的引擎无关的 LLM 网关，提供完整的 OpenAI 与 Anthropic API 兼容性，支持 vLLM、TRT‑LLM、TokenSpeed、SGLang、OpenAI、Gemini 等多种后端，并具备 gRPC 流水线、KV 缓存感知路由、聊天历史、token 缓存、Responses API、嵌入式、WASM 插件、MCP 以及多租户认证等功能，帮助将零散的 Prompt 和工具转化为可重复的 Agent 工作流。典型接入方式包括通过其提供的 HTTP/REST、gRPC 或 CLI/SDK 调用统一的 API 入口，或在服务中直接嵌入其网关库进行路由与缓存管理。凭借最近的活跃维护、强

## 🧭 Practical evaluation

**Value:** smg-project/smg helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 429 GitHub stars
- 129 forks
- updated 2026-08-01
- primary language: Rust
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 53/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 70/100 |
| recency | 60/100 |
| adoption | 55/100 |
| production | 68/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-08-01 · [View on GitHub](https://github.com/smg-project/smg) · [← Back to Mcp](./README.md)</sub>
