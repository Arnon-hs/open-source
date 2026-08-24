# jhpyle/docassemble

[![Stars](https://img.shields.io/github/stars/jhpyle/docassemble?style=flat-square&color=yellow)](https://github.com/jhpyle/docassemble/stargazers) [![Forks](https://img.shields.io/github/forks/jhpyle/docassemble?style=flat-square&color=blue)](https://github.com/jhpyle/docassemble/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> A free, open-source expert system for guided interviews and document assembly, based on Python, YAML, and Markdown.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 960 |
| 🍴 **Forks** | 306 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`docassemble`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
jhpyle/docassemble is an open‑source expert‑system framework that lets you build guided, interview‑style user flows and automatically generate documents using Python, YAML, and Markdown. It provides a ready‑made stack for adding AI‑driven question‑answering, retrieval‑augmented generation (RAG), or agent workflows without having to start from scratch.  

**Value**  
- **Accelerated prototyping** – The platform already handles interview logic, data capture, and templated document output, so you can focus on the AI component (e.g., a language model or retrieval layer) rather than building the surrounding infrastructure.  
- **Low‑code integration** – By defining interview steps in YAML and content in Markdown, non‑engineers can contribute, shortening development cycles and widening the pool of contributors.  
- **Extensible AI hooks** – The system exposes hooks where you can plug in LLM calls, RAG pipelines, or custom agents, making it a convenient sandbox for evaluating model tooling and workflow designs.  

**Practical Adoption Path**  
1. **Sandbox evaluation** – Clone the repo, run the Docker‑compose setup, and experiment with a simple interview that calls an LLM via the provided Python hooks.  
2. **Feature extension** – Replace the placeholder AI calls with your own model API (OpenAI, Anthropic, self‑hosted) and add any necessary retrieval or tool‑use logic.  
3. **Internal pilot** – Deploy the customized instance behind your corporate firewall (e.g., on Kubernetes or a managed VM) and run a small user group through the interview to validate data capture, security, and performance.  
4. **Production hardening** – Conduct a security audit (dependency scanning, secret management), add monitoring/logging, and set up CI/CD pipelines for automated testing and updates before scaling to a broader audience.  

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last update 2026‑06‑29) and has a healthy community signal (≈960 ★, 306 forks).  
- **Suitability**: Ideal for prototypes, internal tools, or regulated environments where you can control the surrounding stack.  
- **Risks**: The core is written in Python, but the repository lists JavaScript as the primary language, indicating mixed‑language components that may need extra integration testing. License compliance, security posture, and long‑term maintainer commitment still require a final review.  
- **Readiness Checklist**:  
  - Verify licensing (MIT/Apache, etc.) aligns with your policy.  
  - Run dependency vulnerability scans (e.g., `pip-audit`, `npm audit`).  
  - Implement authentication/authorization around the interview endpoints.  
  - Set up automated backups of interview data and generated documents.  

Once these steps are addressed, docassemble can move from a prototyping platform to a production‑grade solution for AI‑enhanced interview and document‑assembly workflows.

### Русский

jhpyle/docassemble — бесплатная open‑source экспертная система для создания направленных интервью и сборки документов на базе Python, YAML и Markdown, позволяющая быстро добавить ИИ‑возможности без необходимости строить стек модели с нуля. Типовой сценарий внедрения — прототипирование AI‑фич, построения RAG‑ или агентных рабочих процессов и оценка инструментов модели в внутренних или экспериментальных проектах. Проект имеет средний уровень готовности к production: полезен для прототипов и внутренних workflows, но требует проверки зависимостей, безопасности и активности сопровождающих перед выводом в продакшн.

### 中文

jhpyle/docassemble 是一个基于 Python、YAML 和 Markdown 的开源专家系统，能够快速为引导式访谈和文档生成添加 AI 能力，省去从零搭建模型栈的工作。典型的接入方式是通过其 YAML 配置和 Markdown 模板定义访谈流程，然后在项目中调用其 Python 接口或使用提供的 Web 服务进行集成；不过由于元数据信息较为稀疏，建议在采用前进行手动检查和安全评估。该项目目前处于中等成熟度，适合用于原

## 🧭 Practical evaluation

**Value:** jhpyle/docassemble helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 960 GitHub stars
- 306 forks
- updated 2026-06-29
- primary language: JavaScript
- 1 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 62/100 |
| stars | 63/100 |
| topics | 13/100 |
| outlook | 49/100 |
| quality | 55/100 |
| recency | 40/100 |
| adoption | 63/100 |
| production | 53/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/jhpyle/docassemble) · [← Back to Misc](./README.md)</sub>
