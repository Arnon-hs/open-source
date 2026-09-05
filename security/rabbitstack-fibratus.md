# rabbitstack/fibratus

[![Stars](https://img.shields.io/github/stars/rabbitstack/fibratus?style=flat-square&color=yellow)](https://github.com/rabbitstack/fibratus/stargazers) [![Forks](https://img.shields.io/github/forks/rabbitstack/fibratus?style=flat-square&color=blue)](https://github.com/rabbitstack/fibratus/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Adversary tradecraft detection, protection, and hunting

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.5k |
| 🍴 **Forks** | 215 |
| 💻 **Language** | Go |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`adversary` `blueteam` `edr` `etw` `golang` `instrumentation` `mitre` `python` `security` `windows` `windows-kernel`

## 🎯 Categories

Security

## 📝 Summary

### English

**Summary**  
fibratus (rabbitstack/fibratus) is an open‑source Go toolkit for detecting adversary tradecraft, strengthening security and privacy checks, and enabling proactive hunting of threats. With strong community signals—2.5 k stars, 215 forks, recent commits, and broad ecosystem adoption—it is ready for a serious pilot, though a small proof‑of‑concept should be run first.

**Value**  
fibratus gives security teams early visibility into low‑level Windows kernel events, allowing them to surface suspicious behavior before it escalates into a breach. By integrating its detection primitives into CI/CD pipelines or runtime monitoring, organizations can automate risk audits, enforce authentication or privacy controls, and reduce the time‑to‑detect for advanced threats.

**Practical adoption path**  
1. **Proof of concept** – Clone the repo, run the example scripts from the README, and verify event collection on a test Windows host.  
2. **Integration** – Wrap fibratus’s Go APIs or CLI into existing security tooling (e.g., SIEM ingest, GitHub Actions, or custom audit scripts).  
3. **Policy extension** – Add organization‑specific detection rules or enrich alerts with your asset inventory.  
4. **Scale‑out** – Deploy via container or as a Windows service across the fleet, leveraging its built‑in exporters for Elasticsearch, Kafka, or Syslog.

**Production readiness**  
The project shows high production readiness: it is actively maintained (last commit 2026‑07‑04), has a sizable user base, and ships a stable Go codebase with clear documentation. While the license and long‑term maintainer commitment still need a final review, the overall risk profile is low, making fibratus a solid candidate for a pilot in a security‑focused environment.

### Русский

Резюме проекта rabbitstack/fibratus:

Проект rabbitstack/fibratus — это open-source решение для обнаружения, защиты и охоты на вредоносную деятельность. Он помогает выявлять и устранять проблемы безопасности и конфиденциальности на ранней стадии разработки. 

Проект готов к внедрению в production и имеет высокий уровень готовности, подтвержденный активностью, приёмом и сигналами экосистемы. 

Типовой сценарий внедрения: проект может быть использован для укрепления безопасности проверок, добавления аутентификации или контроля конфиденциальности и аудита рисков на ранней стадии.

### 中文

**简短介绍**

Rabbitstack/fibratus 是一个开源项目，用于检测、保护和猎杀攻击者 tradecraft（一种利用技术优势的攻击方式）。它可以帮助早期发现安全和隐私问题。

**价值**

Rabbitstack/fibratus 的价值在于，它可以帮助加强安全检查、添加认证或隐私控制、及早审核风险。通过使用这个项目，您可以更好地保护您的系统和数据。

**典型接入方式**

典型接入方式包括：

1. 评估和检查 README 文档。
2. 运行一个小的证明概念（POC）来测试项目的功能。
3. 根据项目的需求和您的系统的具体情况进行集成。

**生产可用性**

Rabbitstack/fibratus 的生产可用性较高，主要原因是：

1. 近期活跃性：项目最近有更新和维护。
2. 广泛采用：项目有 2500 个 GitHub 星和 215 个分支。
3. 强大的生态系统：项目有强大的生态系统和信号支持。

但是，请注意，项目的许可、安全状态和活跃

## 🧭 Practical evaluation

**Value:** rabbitstack/fibratus helps catch security and privacy issues earlier in the workflow.

**Best use cases**

- strengthen security checks
- add auth or privacy controls
- audit risk earlier

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2500 GitHub stars
- 215 forks
- updated 2026-07-04
- primary language: Go
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 58/100 |
| stars | 72/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 81/100 |
| recency | 80/100 |
| adoption | 68/100 |
| production | 74/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-04 · [View on GitHub](https://github.com/rabbitstack/fibratus) · [← Back to Security](./README.md)</sub>
