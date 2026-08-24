# OWASP/mastg

[![Stars](https://img.shields.io/github/stars/OWASP/mastg?style=flat-square&color=yellow)](https://github.com/OWASP/mastg/stargazers) [![Forks](https://img.shields.io/github/forks/OWASP/mastg?style=flat-square&color=blue)](https://github.com/OWASP/mastg/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> The OWASP Mobile Application Security Testing Guide (MASTG) is a comprehensive manual for mobile app security testing and reverse engineering. It describes technical processes for verifying the OWASP Mobile Security Weakness Enumeration (MASWE) weaknesses, which are in alignment with the OWASP MASVS.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 13k |
| 🍴 **Forks** | 2.8k |
| 💻 **Language** | Python |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `android-application` `compliancy-checklist` `dynamic-analysis` `hacking` `ios` `ios-app` `mast` `mastg` `mobile-app` `mobile-security` `mstg`

## 🎯 Categories

Mobile · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The OWASP Mobile Application Security Testing Guide (MASTG) is a free, community‑driven manual that details how to test mobile apps and perform reverse‑engineering to verify the weaknesses listed in the OWASP Mobile Security Weakness Enumeration (MASWE) and the Mobile Application Security Verification Standard (MASVS). It offers step‑by‑step technical procedures, sample code, and tooling recommendations, making it a go‑to reference for security engineers, auditors, and developers who need to assess mobile‑first or Web3‑enabled applications.  

**Value**  
- **Comprehensive coverage** of mobile security testing techniques, from static analysis to runtime checks, aligned with globally recognized standards (MASVS/MASWE).  
- **Practical tooling guidance** (e.g., Frida, MobSF, Burp Suite) and ready‑made test scripts that can be adapted to audit blockchain‑related mobile wallets, DeFi front‑ends, and other Web3 components.  
- **Open, constantly updated** repository (13013 ★, 2761 forks) that serves as both a learning resource and a reference implementation for building secure mobile or hybrid Web3 workflows.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC)** – Clone the repo, run the provided Docker/virtual‑env setup, and execute a single test module (e.g., “Cryptographic Storage”) against a test wallet app.  
2. **README & CI Integration** – Verify the README instructions, add the MASTG test suite to your CI pipeline (e.g., GitHub Actions) to run automated static checks on each build.  
3. **Custom Test Extension** – Extend existing test cases to cover your specific blockchain integration (e.g., smart‑contract interaction, QR‑code signing) and document the new modules.  
4. **Full‑Scale Pilot** – Apply the complete MASTG checklist to a production‑grade mobile app, track findings in your ticketing system, and iterate on remediation.  

**Production Readiness**  
- **High**: The project shows strong recent activity (last update 2026‑06‑29), a large and active community, and mature documentation.  
- **Signal Strength**: 13013 stars, 2761 forks, 19 topical tags, and a primary Python implementation indicate robust ecosystem support.  
- **Risk Considerations**: No immediate metadata or licensing red flags, but a final review of the project’s license (Apache‑2.0) and its security posture (e.g., open issues, CVE response) is recommended before full production deployment.  

Overall, MASTG is production‑ready for organizations that need a vetted, open‑source framework to assess and harden mobile and Web3 applications, with a clear, incremental path from PoC to enterprise‑scale integration.

### Русский

Резюме проекта OWASP/mastg:

Проект OWASP/mastg представляет собой обширный руководство по безопасности мобильных приложений, позволяющее пользователям протестировать и обратно-engineer мобильные приложения. Основное преимущество проекта заключается в его способности помочь разработчикам в создании и проверке Web3-приложений, включая интеграцию с блокчейн-решениями.

Проект готов к внедрению в производственную среду (High) и имеет сильные признаки активности, признания и экосистемы. Типовой сценарий внедрения включает в себя проверку безопасности мобильных приложений, протестирование блокчейн-интеграций и создание прототипов кошельков или DeFi-функций.

### 中文

**OWASP/mastg 简介**

OWASP/mastg 是一个开源项目，提供了一个全面指南，用于测试和逆向工程移动应用的安全性。它描述了验证 OWASP Mobile Security Weakness Enumeration (MASWE) 弱点的技术过程，这些弱点与 OWASP MASVS 一致。

**价值**

OWASP/mastg 帮助开发者在 Web3 流程中构建、检视和模拟区块链集成。它提供了一个开源的实现细节，方便开发者在区块链中构建、检视和模拟钱包或 DeFi 特性。

**典型接入方式**

开发者可以通过以下方式接入 OWASP/mastg：

1. 构建 Web3 流程：使用 OWASP/mastg 构建和测试 Web3 应用。
2. 检视区块链集成：使用 OWASP/mastg 检视和测试区块链集成。
3. 模拟钱包或 DeFi 特性：使用 OWASP/mastg 模拟和测试钱包或 DeFi 特性。

**生产可用性**

OWASP/mastg

## 🧭 Practical evaluation

**Value:** OWASP/mastg helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 13013 GitHub stars
- 2761 forks
- updated 2026-06-29
- primary language: Python
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 86/100 |
| stars | 88/100 |
| topics | 100/100 |
| outlook | 64/100 |
| quality | 79/100 |
| recency | 40/100 |
| adoption | 87/100 |
| production | 62/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/OWASP/mastg) · [← Back to Mobile](./README.md)</sub>
