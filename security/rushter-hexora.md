# rushter/hexora

[![Stars](https://img.shields.io/github/stars/rushter/hexora?style=flat-square&color=yellow)](https://github.com/rushter/hexora/stargazers) [![Forks](https://img.shields.io/github/forks/rushter/hexora?style=flat-square&color=blue)](https://github.com/rushter/hexora/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> Static analysis of malicious Python code

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 167 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | Rust |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-07-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`python` `rust` `security` `security-audit` `security-tools`

## 🎯 Categories

Security

## 📝 Summary

### English

**Summary**  
Hexora (rushter/hexora) is a Rust‑based static analysis tool that scans Python code for security‑relevant bugs, privacy leaks, and malicious patterns, enabling teams to catch risks early in the development cycle. With 167 GitHub stars and recent activity, it offers a lightweight way to augment existing CI pipelines with automated security checks.

**Value**  
By automatically flagging insecure imports, unsafe eval‑like constructs, and data‑exfiltration code, Hexora helps developers and security engineers surface high‑impact vulnerabilities before code reaches production, reducing remediation cost and improving compliance with privacy policies.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the CLI on a small, representative Python module, and verify that the findings align with your internal threat model.  
2. **CI integration** – Add a step to your GitHub Actions/Jenkins pipeline that executes `hexora scan` and fails the build on any “high‑severity” alerts; configure the severity thresholds to match your risk appetite.  
3. **Policy refinement** – Tune the rule set (or write custom rules) based on false positives observed during the pilot, then expand coverage to all repositories.  

**Production readiness**  
Hexora is at a **medium** readiness level: it is stable enough for internal tooling, prototypes, and CI enrichment, but production deployment should include a dependency audit (Rust crates, Python parsers) and a review of the project’s licensing and maintainer activity. Once those checks are completed and the rule set is hardened, Hexora can be safely rolled out across broader development workflows.

### Русский

**rushter/hexora** — это open‑source‑инструмент на Rust для статического анализа потенциально вредоносного Python‑кода, позволяющий обнаружить уязвимости и нарушения конфиденциальности ещё до этапа разработки. Его обычно интегрируют в CI/CD в виде небольшого proof‑of‑concept: запускают анализ на этапе проверки pull‑request, добавляют правила безопасности и контролируют риски на ранних стадиях. Готовность к production — средняя: проект подходит для прототипов и внутренних пайплайнов, но перед развертыванием в продакшн требуется проверка зависимостей, лицензии и поддержка со стороны мейнтейнеров.

### 中文

**项目简介**  
Hexora（rushter/hexora）是一款基于 Rust 实现的静态分析工具，专注于检测恶意 Python 代码中的安全和隐私风险。它能够在代码提交或 CI 流程的早期阶段捕获潜在漏洞，从而帮助团队提前规避安全事故。

**价值主张**  
- **提前发现风险**：在代码进入生产环境前识别后门、信息泄露、未授权访问等问题。  
- **提升安全合规**：配合安全审计、隐私合规检查，降低后期修复成本。  
- **易于嵌入现有流程**：可作为 CI/CD 步骤或本地 pre‑commit 检查使用，帮助团队在日常开发中形成安全防线。

**典型接入方式**  
1. **CI/CD 集成**：在 GitHub Actions、GitLab CI、Jenkins 等流水线中添加一个执行 `hexora scan` 的步骤，若检测到高危问题则让构建失败。  
2. **本地 pre‑commit**：在项目根目录的 `.pre-commit-config.yaml` 中声明 Hexora，开发者提交前自动运行静态分析。  
3. **脚本化审计**：在内部审计或代码审查工具中调用 Hexora 的 CLI，生成可视化报告供安全团队评估。

**生产可用性**  
- **成熟度**：当前得分 61/100，适合作为原型或内部工作流的安全检测工具。  
- **依赖与维护**：项目主要语言为 Rust，拥有 167 ★、8 Fork，最近一次更新在 2026‑07‑13，活跃度尚可，但在正式生产环境使用前建议：  
  - 检查依赖的安全性（尤其是 Rust crates 的漏洞报告）。  
  - 评估许可证兼容性并确认维护者的响应速度。  
  - 通过小规模 PoC 验证与现有构建系统的兼容性，随后逐步扩大使用范围。  

综上，Hexora 能为安全敏感的 Python 项目提供早期风险捕获的能力，适合作为内部或原型阶段的安全检测手段；在完成依赖审计和维护性评估后，可逐步推广至生产环境。

## 🧭 Practical evaluation

**Value:** rushter/hexora helps catch security and privacy issues earlier in the workflow.

**Best use cases**

- strengthen security checks
- add auth or privacy controls
- audit risk earlier

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 167 GitHub stars
- 8 forks
- updated 2026-07-13
- primary language: Rust
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 47/100 |
| topics | 63/100 |
| outlook | 73/100 |
| quality | 68/100 |
| recency | 100/100 |
| adoption | 41/100 |
| production | 72/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/rushter/hexora) · [← Back to Security](./README.md)</sub>
