# zuhayrb/dexpose

[![Stars](https://img.shields.io/github/stars/zuhayrb/dexpose?style=flat-square&color=yellow)](https://github.com/zuhayrb/dexpose/stargazers) [![Forks](https://img.shields.io/github/forks/zuhayrb/dexpose?style=flat-square&color=blue)](https://github.com/zuhayrb/dexpose/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-07-13 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Dexpose is a pure‑Go command‑line tool that scans Android APK files for accidentally bundled secrets—such as API keys or certificates—without requiring a JVM or the heavy Jadx decompiler. By operating entirely in Go, it runs quickly on any platform and can be dropped into local development or CI pipelines to catch leaks early. The project is actively maintained as of July 2026 but has limited integration metadata, so a quick manual evaluation is recommended before widescale adoption.  

**Value**  
- **Speed & Simplicity** – No Java runtime or external decompilation steps are needed, so scans finish in seconds and can be run on minimal CI agents.  
- **Security‑first feedback** – Detects hard‑coded secrets at build time, reducing the risk of credential exposure in production releases.  
- **Toolchain‑agnostic** – Works on Linux, macOS, and Windows out of the box, making it easy to embed in diverse developer environments.  

**Practical Adoption Path**  
1. **Trial Run** – Clone the repo, build the binary (`go build ./cmd/dexpose`), and run it against a few sample APKs to verify detection accuracy.  
2. **Integrate Locally** – Add a script or Makefile target (`dexpose scan $APK`) to your dev workflow; optionally gate merges with a pre‑commit hook.  
3. **CI Hook** – Wrap the binary in a CI step (GitHub Actions, GitLab CI, Jenkins, etc.) that fails the job if any secret is reported.  
4. **Review & Tuning** – Use the generated report to whitelist false positives and adjust any custom regexes or rule files supplied by Dexpose.  

**Production Readiness**  
- **Maturity**: Medium – suitable for prototypes, internal tooling, or as a gate in CI pipelines after a short validation period.  
- **Dependencies**: Single Go binary; minimal external dependencies, simplifying containerization and version pinning.  
- **Risks**: Sparse integration signals and limited documentation mean you should verify the license, check the issue tracker for open bugs, and confirm that the release cadence matches your security‑update policy before promoting it to critical production pipelines.  

In short, Dexpose offers a fast, JVM‑free way to catch leaked secrets in APKs, making it a practical addition to developer and CI workflows, provided you perform a brief manual vetting and monitor its maintenance health.

### Русский

Резюме проекта Dexpose:

Декспоз (Dexpose) - это открытый проект, предоставляющий командную строку для сканирования APK-файлов на наличие утечек секретной информации. Этот проект может помочь инженерам сократить время, необходимое для решения дневных задач и проверки кода.

Типовой сценарий внедрения: Декспоз может быть использован для ускорения разработки, автоматизации локальных задач и улучшения обратной связи в цепочке интеграции (CI).

Уровень готовности к production: Проект имеет средний уровень готовности к производству, что делает его пригодным для прототипирования или внутренних рабочих процессов, но требует тщательного проверки зависимостей и поддержки перед использованием в продакшене.

### 中文

**Dexpose 简介**

Dexpose 是一个纯 Go CLI 工具，用于扫描 APK 文件中泄露的机密信息（No JVM, No Jadx）。它可以帮助开发者节省在开发和审查循环中花费的时间。

**价值**

Dexpose 的价值在于，它可以帮助开发者：

* 加快开发者工作流程
* 自动化本地工程任务
* 提高 CI 反馈

**接入方式**

Dexpose 需要手动检查和接入，因为接入信号在发现的元数据中较为稀疏。需要在使用前检查依赖项、维护项、文档、问题和发布频率。

**生产可用性**

Dexpose 的生产可用性为中等。它适合用于原型或内部工作流程，需要在生产环境中进行依赖项和维护检查。

## 🧭 Practical evaluation

**Value:** Dexpose: A Pure-Go CLI to Scan APKs for Leaked Secrets (No JVM, No Jadx) helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-07-13
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 57/100 |
| quality | 41/100 |
| recency | 100/100 |
| adoption | 0/100 |
| production | 63/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 80/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/zuhayrb/dexpose) · [← Back to DevTools](./README.md)</sub>
