# s2-streamstore/cachey

[![Stars](https://img.shields.io/github/stars/s2-streamstore/cachey?style=flat-square&color=yellow)](https://github.com/s2-streamstore/cachey/stargazers) [![Forks](https://img.shields.io/github/forks/s2-streamstore/cachey?style=flat-square&color=blue)](https://github.com/s2-streamstore/cachey/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Read-through cache for object storage

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 586 |
| 🍴 **Forks** | 13 |
| 💻 **Language** | Rust |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-05-10 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

AI/ML

## 📝 Summary

### English

s2‑streamstore/cachey is an open‑source read‑through caching layer designed for object‑storage systems. It transparently fetches missing items from the underlying store, writes them to a local cache, and serves subsequent requests with low latency, while providing configurable eviction policies and metrics. Ideal for AI/ML pipelines that need fast, repeatable access to large datasets stored in cloud object stores.

### Русский

**s2‑streamstore/cachey** — это открытая библиотека, реализующая read‑through кеш для объектных хранилищ, позволяя автоматически загружать недостающие данные из хранилища при первом обращении и кэшировать их для последующего быстрого доступа. Проект ориентирован на эффективную работу с большими объёмами данных в AI/ML‑pipeline, снижая задержки и нагрузку на бекенд‑хранилище. Лёгко интегрируется в существующие системы и поддерживает гибкую настройку стратегии кэширования.

### 中文

s2-streamstore/cachey：s2-streamstore/cachey helps add AI capability without starting from a blank model stack.。适合用于prototype AI features、build RAG or agent workflows。Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

## 🧭 Practical evaluation

**Value:** s2-streamstore/cachey helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 586 GitHub stars
- 13 forks
- updated 2026-05-10
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| usefulness | 58/100 |
| quality | 63/100 |
| integration | 30/100 |
| production | 68/100 |
| outlook | 69/100 |
| adoption | 50/100 |
| stars | 59/100 |
| forks | 29/100 |
| recency | 100/100 |
| topics | 0/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-10 · [View on GitHub](https://github.com/s2-streamstore/cachey) · [← Back to AI/ML](./README.md)</sub>
