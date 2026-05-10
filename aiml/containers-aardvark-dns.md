# containers/aardvark-dns

[![Stars](https://img.shields.io/github/stars/containers/aardvark-dns?style=flat-square&color=yellow)](https://github.com/containers/aardvark-dns/stargazers) [![Forks](https://img.shields.io/github/forks/containers/aardvark-dns?style=flat-square&color=blue)](https://github.com/containers/aardvark-dns/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> Authoritative dns server for A/AAAA container records. Forwards other request to host's /etc/resolv.conf

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 264 |
| 🍴 **Forks** | 53 |
| 💻 **Language** | Rust |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-05-08 |
| 🔍 **Source** | github |

## 🏷️ Topics

`container` `coredns` `dns` `dns-server` `dnsmasq` `name-resolution` `nameserver`

## 🎯 Categories

AI/ML · Backend · Security

## 📝 Summary

### English

Aardvark‑DNS is a lightweight, authoritative DNS server that serves A and AAAA records for Docker‑style container hostnames, while transparently forwarding all other queries to the resolver defined in the host’s `/etc/resolv.conf`. It’s designed for backend and security‑focused environments where services need reliable, container‑aware name resolution without altering the host’s existing DNS configuration. Open‑source and easy to integrate, it fits well in AI/ML pipelines and microservice architectures that rely on dynamic container networking.

### Русский

**containers/aardvark-dns** — открытый авторитетный DNS‑сервер, который хранит A/AAAA записи контейнеров и обслуживает их напрямую, а все остальные запросы перенаправляет к DNS, указанному в `/etc/resolv.conf` хоста. Проект сочетает функции бекенда и безопасности, позволяя изолировать сетевой трафик контейнеров без необходимости внешних сервисов, и может быть интегрирован в AI/ML инфраструктуры для динамического управления DNS‑записями.

### 中文

containers/aardvark-dns：containers/aardvark-dns helps add AI capability without starting from a blank model stack.。适合用于prototype AI features、build RAG or agent workflows。Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

## 🧭 Practical evaluation

**Value:** containers/aardvark-dns helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 264 GitHub stars
- 53 forks
- updated 2026-05-08
- primary language: Rust
- 7 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| usefulness | 42/100 |
| quality | 75/100 |
| integration | 30/100 |
| production | 73/100 |
| outlook | 74/100 |
| adoption | 49/100 |
| stars | 52/100 |
| forks | 43/100 |
| recency | 100/100 |
| topics | 88/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-08 · [View on GitHub](https://github.com/containers/aardvark-dns) · [← Back to AI/ML](./README.md)</sub>
