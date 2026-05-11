# joncampbell123/dosbox-x

[![Stars](https://img.shields.io/github/stars/joncampbell123/dosbox-x?style=flat-square&color=yellow)](https://github.com/joncampbell123/dosbox-x/stargazers) [![Forks](https://img.shields.io/github/forks/joncampbell123/dosbox-x?style=flat-square&color=blue)](https://github.com/joncampbell123/dosbox-x/network) [![Language](https://img.shields.io/badge/lang-C-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> DOSBox-X fork of the DOSBox project

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.5k |
| 🍴 **Forks** | 506 |
| 💻 **Language** | C |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
DOSBox‑X is an actively maintained fork of the classic DOSBox emulator, written in C and boasting over 3.5 k stars on GitHub. It extends the original emulator with additional hardware support, improved compatibility, and a more flexible configuration system, making it a solid choice for developers needing to run legacy DOS applications on modern platforms.

**Value**  
- **Broader Compatibility** – Supports a wider range of sound cards, graphics modes, and input devices than upstream DOSBox, reducing the need for custom patches.  
- **Active Community** – Frequent commits (last update 2026‑05‑11) and a sizable contributor base mean bugs are addressed promptly and new features are added regularly.  
- **Open‑source Flexibility** – The C codebase can be compiled for virtually any OS, allowing seamless integration into CI pipelines, automated testing environments, or custom tooling.

**Practical Adoption Path**  
1. **Clone & Build** – Pull the repository, run the standard `./configure && make` workflow, and verify the build on your target OS.  
2. **Run Test Suite** – Execute the provided regression tests with a representative set of your DOS applications to confirm functional parity.  
3. **Integrate** – Wrap the `dosbox-x` binary in a Docker image or a package manager script, and expose its command‑line options via your automation framework.  
4. **Validate** – Compare performance and output against the original DOSBox to ensure the fork’s enhancements align with your workflow.

**Production Readiness**  
- **Maturity**: Medium – the project is stable enough for prototypes and internal tooling, but the integration path isn’t fully documented, so a manual validation step is required.  
- **Dependencies**: Minimal (standard C libraries and SDL); verify that your target environment satisfies them.  
- **Maintenance**: Keep an eye on upstream changes; regularly sync with the repository to incorporate security fixes and new hardware support.  

Overall, DOSBox‑X is a practical, production‑viable emulator for legacy DOS workloads, provided you allocate time for initial testing and integration verification.

### Русский

**DOSBox‑X** — это активный форк оригинального эмулятора DOSBox, написанный на C и поддерживаемый сообществом (3540 звёзд, 506 форков, последний коммит 2026‑05‑11). Он подходит для прототипирования и внутренних проектов, где требуется запуск старых DOS‑приложений или игр, но перед внедрением следует вручную проверить совместимость и оценить затраты на настройку, так как пути интеграции из метаданных не очевидны. Готовность к production — средняя: проект стабилен, но требует дополнительного аудита зависимостей и поддержки перед использованием в критичных системах.

### 中文

**项目简介**  
DOSBox‑X 是 DOSBox 的一个功能更丰富的分支，保持了对经典 DOS 程序和游戏的高度兼容，同时加入了对现代硬件、网络和多显示器等特性的支持。

**价值**  
- **兼容性提升**：在原版 DOSBox 基础上扩展了对声卡、显卡、串口、并行端口以及网络（TCP/IP）等硬件的模拟，能够运行更多依赖这些外设的老软件。  
- **活跃维护**：截至 2026‑05‑11 仍有更新，拥有 3.5k+ 星、500+ Fork，社区活跃度足以保证及时修复 bug 与加入新特性。  
- **易于嵌入**：提供命令行和库接口，可直接在 CI、自动化测试或自研工具链中调用，适合作为内部原型或迁移旧系统的桥梁。

**典型接入方式**  
1. **二进制直接使用**：下载对应平台的预编译 `dosbox-x` 可执行文件，按需在脚本或 Docker 镜像中调用。  
2. **源码编译集成**：克隆仓库后使用 CMake/Make 编译，生成的库 (`libdosbox-x.a` / `dosbox-x.dll`) 可在自研 C/C++ 项目中链接，或通过 `-run` 参数在自定义前端中启动。  
3. **容器化部署**：在 Dockerfile 中 `FROM ubuntu:22.04 && apt-get install -y build-essential && git clone … && make && cp dosbox-x /usr/local/bin`，随后在 CI 流水线或微服务中以 `dosbox-x -conf … -c "run myapp.exe"` 方式执行。

**生产可用性**  
- **成熟度**：项目已稳定多年，社区活跃，代码基数大，适合内部使用或对外提供兼容层。  
- **风险**：元数据中缺乏明确的商业级集成指南，需自行评估依赖的 C 运行时、库兼容性以及安全更新策略。  
- **建议**：在生产环境部署前进行一次完整的功能回归测试，确认所需硬件模拟（声卡、网络等）工作正常；同时制定更新策略（如每月拉取 upstream 并跑回归），以降低长期维护成本。  

总体而言，DOSBox‑X 可作为原有 DOS 应用的可靠运行时，在原型验证和内部业务系统中具备中等到高的生产可用性，只要做好前期的依赖审查和持续维护即可。

## 🧭 Practical evaluation

**Value:** joncampbell123/dosbox-x may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 3540 GitHub stars
- 506 forks
- updated 2026-05-11
- primary language: C

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 68/100 |
| stars | 76/100 |
| topics | 0/100 |
| outlook | 72/100 |
| quality | 73/100 |
| recency | 100/100 |
| adoption | 73/100 |
| production | 72/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/joncampbell123/dosbox-x) · [← Back to Misc](./README.md)</sub>
