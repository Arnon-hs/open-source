# ahupp/python-magic

[![Stars](https://img.shields.io/github/stars/ahupp/python-magic?style=flat-square&color=yellow)](https://github.com/ahupp/python-magic/stargazers) [![Forks](https://img.shields.io/github/forks/ahupp/python-magic?style=flat-square&color=blue)](https://github.com/ahupp/python-magic/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> A python wrapper for libmagic

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.9k |
| 🍴 **Forks** | 304 |
| 💻 **Language** | Python |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`ahupp/python-magic` is a thin Python wrapper around the Unix `libmagic` library that enables file‑type detection based on magic numbers. With over 2.9 k stars and recent commits (as of 2026‑05‑11), it offers a familiar API for projects that need reliable MIME‑type or file‑format inference without writing custom parsers.

**Value Proposition**  
- **Leverages a battle‑tested C library** – `libmagic` powers the classic `file` command, so you inherit its extensive format database and accuracy.  
- **Simple, Pythonic interface** – a few function calls (`magic.from_file`, `magic.from_buffer`) replace boiler‑plate subprocess invocations.  
- **Broad community adoption** – the star/fork count signals that many developers already rely on it for scripts, data pipelines, and web services.

**Practical Adoption Path**  
1. **Assess Compatibility** – Verify that the target environment can install the underlying `libmagic` system package (e.g., `libmagic-dev` on Linux, `brew install libmagic` on macOS).  
2. **Add Dependency** – Pin the library in `requirements.txt` (e.g., `python-magic==0.4.27`) and include the OS package in your Dockerfile or CI setup.  
3. **Run a Smoke Test** – Use a small suite of representative files to confirm that MIME/type detection matches expectations and that no hidden side‑effects (e.g., large memory usage) appear.  
4. **Security Review** – Scan the wrapper and its transitive dependencies for known CVEs; because it merely calls a native library, the main risk is the native `libmagic` version.  
5. **Documentation & Monitoring** – Wrap calls in a utility module that logs detected types and handles exceptions, making future upgrades easier.

**Production‑Readiness Assessment**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑05‑11) and widely used, but the wrapper itself is thin and does not provide advanced features (e.g., async support).  
- **Suitability**: Ideal for prototypes, internal data‑processing pipelines, or services where file‑type validation is a supporting concern rather than a core security boundary.  
- **Pre‑production Checklist**:  
  * Confirm OS‑level `libmagic` version aligns with your security policy.  
  * Pin both the Python wrapper and the native library to known‑good versions.  
  * Add automated tests that verify detection for the file types you actually handle.  
  * Ensure you have a fallback strategy (e.g., default MIME type) if the library fails or is unavailable.  

With these steps, `ahupp/python-magic` can be safely promoted from a prototype tool to a reliable component in internal or low‑risk production environments.

### Русский

**ahupp/python-magic** — это открытая обёртка Python для библиотеки libmagic, позволяющая быстро определять типы файлов по их содержимому. Проект удобно интегрировать в прототипы и внутренние пайплайны (например, при построении систем автоматической классификации или валидации загружаемых файлов), однако перед выводом в продакшн рекомендуется проверить актуальность зависимостей, лицензионные условия и наличие активных мейнтейнеров. С учётом 2900+ звёзд, 300+ форков и недавних коммитов проект находится на среднем уровне готовности: подходит для экспериментального и ограниченного производственного использования после дополнительного аудита.

### 中文

**项目简介**  
ahupp/python-magic 是对系统库 **libmagic**（即 `file` 命令背后的实现）的 Python 包装器，提供简单的 `magic.from_file()`、`magic.from_buffer()` 等接口，帮助开发者在代码中快速识别文件的 MIME 类型或内容特征。  

**价值**  
- **即插即用**：只需几行代码即可完成文件类型检测，省去自行调用系统命令或编写正则的繁琐。  
- **跨平台**：在 Linux、macOS、Windows（通过预编译的 libmagic）上均可工作，适配大多数 Python 项目。  
- **社区认可**：拥有 2900+ Stars、300+ Forks，活跃度仍在持续更新，适合作为原型或内部工具的底层依赖。  

**典型接入方式**  
```bash
pip install python-magic   # 或者 pip install python-magic-bin 在 Windows 上免装 libmagic
```
```python
import magic

# 检测文件 MIME 类型
mime = magic.from_file('example.pdf', mime=True)

# 检测内存缓冲区
mime_buf = magic.from_buffer(b'%PDF-1.4', mime=True)
```
在 CI/CD 流程中，可将 `libmagic` 作为系统依赖（apt-get install libmagic1、yum install file-libs 等），或直接使用 `python-magic-bin` 包自带的二进制库，无需额外配置。  

**生产可用性**  
- **成熟度**：Medium。功能稳定，已在多个开源项目和内部系统中使用，适合作为原型或内部服务的文件类型判断组件。  
- **依赖管理**：仅依赖 libmagic（或二进制包），需要在部署镜像中确保该库的版本兼容。  
- **维护与安全**：项目仍在维护（最近一次提交 2026‑05‑11），但在正式生产环境使用前建议：  
  1. 检查许可证（MIT）是否符合公司合规；  
  2. 通过安全扫描工具审计 libmagic 本身的 CVE；  
  3. 设定版本锁定（如 `python-magic==0.4.27`），防止意外升级导致不兼容。  

综上，ahupp/python-magic 在原型开发和内部业务流程中提供了轻量且可靠的文件类型检测能力，经过适当的依赖审计和版本控制后，可安全投入生产使用。

## 🧭 Practical evaluation

**Value:** ahupp/python-magic may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 2909 GitHub stars
- 304 forks
- updated 2026-05-11
- primary language: Python

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 62/100 |
| stars | 74/100 |
| topics | 0/100 |
| outlook | 71/100 |
| quality | 72/100 |
| recency | 100/100 |
| adoption | 70/100 |
| production | 73/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/ahupp/python-magic) · [← Back to Misc](./README.md)</sub>
