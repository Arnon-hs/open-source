# dosemu2/dosemu2

[![Stars](https://img.shields.io/github/stars/dosemu2/dosemu2?style=flat-square&color=yellow)](https://github.com/dosemu2/dosemu2/stargazers) [![Forks](https://img.shields.io/github/forks/dosemu2/dosemu2?style=flat-square&color=blue)](https://github.com/dosemu2/dosemu2/network) [![Language](https://img.shields.io/badge/lang-C-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-46%2F100-brightgreen?style=flat-square)](#)

> Run DOS programs under linux:

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 712 |
| 🍴 **Forks** | 75 |
| 💻 **Language** | C |
| 📈 **Score** | 46/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`dos` `dosemu` `emulator`

## 🎯 Categories

Misc

## 📝 Summary

### English

Here's a brief summary of the dosemu2 project:

**Project Summary:** dosemu2 is an open-source project that enables running DOS programs under Linux, providing a useful solution for specific workflows where legacy DOS applications are required. However, its adoption requires manual inspection and validation due to sparse integration signals and unclear setup costs. Despite this, the project is considered production-ready for prototype or internal workflows, given proper dependency and maintenance checks.

**Value:** The project's value lies in its ability to run DOS programs under Linux, making it a potential solution for workflows that rely on legacy DOS applications.

**Practical Adoption Path:**

1. Manual inspection: Review the project's README and activity to ensure it matches your specific workflow.
2. Integration evaluation: Assess the integration path and validate the setup costs before committing to the project.
3. Dependency and maintenance checks: Conduct thorough checks on the project's dependencies and maintenance requirements to ensure production readiness.

**Production Readiness:** The project is considered production-ready for prototype or internal workflows, but it may not be suitable for large-scale production environments due to its medium production readiness score.

### Русский

Резюме проекта dosemu2/dosemu2:

Проект dosemu2/dosemu2 позволяет запускать программы DOS под управлением Linux, что может быть полезно для конкретных рабочих процессов при условии соответствия README и активности проекта. Внедрение проекта возможно в прототипах или внутренних рабочих процессах после проверки зависимостей и обслуживания, но требует тщательной проверки перед использованием в продакшене.

### 中文

**项目简介**  
dosemu2（dosemu2/dosemu2）是一款在 Linux 环境下运行 DOS 程序的开源模拟器，使用 C 语言实现，已累计 712 ★、75 叉，并在 2026‑07‑11 仍保持活跃更新。

**价值**  
- 让老旧的 DOS 软件、游戏或专用业务系统在现代 Linux 服务器或工作站上继续使用，无需迁移或重写代码。  
- 轻量级、无需完整虚拟机即可提供基本的 DOS 环境，适合原型验证、内部工具或教学演示。  

**典型接入方式**  
1. **源码编译**：克隆仓库后使用 `./configure && make && sudo make install` 完成安装；也可通过发行版的包管理器（如 Debian/Ubuntu 的 `apt-get install dosemu2`）直接获取。  
2. **脚本封装**：在 CI/CD 或自动化测试中，编写包装脚本 `dosemu2 -i <dos_exe>`，将 DOS 可执行文件作为子进程运行。  
3. **容器化**：基于官方镜像或自建 Dockerfile，将 `dosemu2` 安装到容器中，以实现可重复、隔离的运行环境。  

**生产可用性**  
- **成熟度**：中等（Medium）。项目已稳定多年，社区活跃，代码基线清晰，但缺少完整的 CI/CD 流水线和官方 SLA。  
- **适用场景**：原型开发、内部业务系统、遗留工具的迁移、教学演示等；不建议直接用于高并发、对安全合规要求极高的面向外部用户的生产服务。  
- **集成风险**：元数据中未提供明确的依赖图或插件机制，实际接入前需手动检查系统库（如 `libc6-i386`、`x86` 兼容层）以及与现有软件的冲突。  
- **维护成本**：需要定期跟踪上游更新（每月或每季度），并验证在目标 Linux 发行版上的兼容性。  

**结论**  
dosemu2 是一款可靠的 DOS 兼容层，适合在内部或原型环境中快速复活旧软件。若业务对稳定性、自动化部署和安全审计有严格要求，建议在正式生产前进行充分的测试和依赖审计。

## 🧭 Practical evaluation

**Value:** dosemu2/dosemu2 may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 712 GitHub stars
- 75 forks
- updated 2026-07-11
- primary language: C
- 3 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 47/100 |
| stars | 61/100 |
| topics | 38/100 |
| outlook | 50/100 |
| quality | 56/100 |
| recency | 40/100 |
| adoption | 57/100 |
| production | 51/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-11 · [View on GitHub](https://github.com/dosemu2/dosemu2) · [← Back to Misc](./README.md)</sub>
