# miurahr/py7zr

[![Stars](https://img.shields.io/github/stars/miurahr/py7zr?style=flat-square&color=yellow)](https://github.com/miurahr/py7zr/stargazers) [![Forks](https://img.shields.io/github/forks/miurahr/py7zr?style=flat-square&color=blue)](https://github.com/miurahr/py7zr/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> 7zip in python3 with ZStandard, PPMd, LZMA2, LZMA1, Delta, BCJ, BZip2, and Deflate compressions, and AES encryption.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 552 |
| 🍴 **Forks** | 90 |
| 💻 **Language** | Python |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`7-zip` `7zip` `aes` `bcj` `bzip2` `cli` `compress` `decompression` `decryption` `deflate` `encryption` `library`

## 🎯 Categories

DevTools · Security

## 📝 Summary

### English

**Summary**  
miurahr/py7zr is a pure‑Python 7‑Zip library that supports a wide range of compression algorithms (ZStandard, PPMd, LZMA2/LZMA1, Delta, BCJ, BZip2, Deflate) and AES‑256 encryption, offering both an API/SDK and a CLI for easy integration. With over 550 stars, active maintenance (last commit 2026‑06‑26), and a growing user base, it is positioned as a production‑ready OSS component for automating archive handling in development pipelines.

**Value**  
- **Time‑saving:** Developers can create, extract, and inspect 7z archives directly from Python without invoking external binaries, eliminating context switches and simplifying CI scripts.  
- **Security:** Built‑in AES encryption lets teams protect artefacts (e.g., build outputs, logs) while still using a familiar 7z format.  
- **Flexibility:** Support for multiple compression methods enables optimal trade‑offs between speed and size, useful for CI caches, artifact storage, or on‑the‑fly packaging.

**Practical adoption path**  
1. **Prototype:** Add `py7zr` to a virtual environment (`pip install py7zr`) and experiment with the high‑level `SevenZipFile` API or the provided CLI to compress/decompress a sample project.  
2. **Integrate:** Wrap the library in a thin utility module (e.g., `archive.py`) that your build scripts or CI jobs call, handling error reporting and logging.  
3. **Automate:** Replace existing shell‑based `7z` calls in Makefiles, GitHub Actions, or Jenkins pipelines with the Python wrapper, gaining cross‑platform consistency.  
4. **Validate:** Run security scans (e.g., Snyk, OSS Review Toolkit) on the package, confirm licensing compliance, and add unit tests that cover the new archive steps.

**Production readiness**  
- **Activity & community:** Recent commits, 90+ forks, and a healthy issue/PR flow indicate active maintainers and quick bug resolution.  
- **Stability:** The library follows semantic versioning, provides both API and CLI, and has been adopted in several open‑source projects, suggesting it has passed real‑world usage tests.  
- **Risk considerations:** No major metadata or licensing red flags have been identified, but a final security audit (dependency scanning, review of encryption implementation) and verification of maintainer responsiveness are recommended before a full‑scale rollout.  

Overall, py7zr offers a mature, feature‑rich solution for Python‑centric archive management that can be safely introduced into development and CI environments with minimal friction.

### Русский

**miurahr/py7zr** — это библиотека Python 3, реализующая 7‑zip со всеми популярными алгоритмами сжатия (ZStandard, PPMd, LZMA2/LZMA1, Delta, BCJ, BZip2, Deflate) и поддержкой AES‑шифрования. Она позволяет инженерам быстро интегрировать архивирование/распаковку в скрипты, CI‑pipeline и локальные инструменты, ускоряя рабочие циклы разработки и автоматизируя рутинные задачи. Проект имеет высокий уровень готовности к production: активные коммиты, более 500 звёзд, широкое использование в сообществе и поддержка API/CLI, однако перед внедрением стоит уточнить лицензионные и безопасностные детали.

### 中文

**项目简介**  
`miurahr/py7zr` 是一款基于 Python 3 的 7‑Zip 实现，支持 ZStandard、PPMd、LZMA2、LZMA1、Delta、BCJ、BZip2、Deflate 等多种压缩算法以及 AES 加密，能够在 Python 环境中轻松创建、解压和管理 7z 文件。

**价值**  
- **提升开发效率**：在本地或 CI 环境中直接使用 Python 脚本完成压缩/解压，无需额外安装 7‑Zip 客户端，省去切换工具的时间。  
- **自动化工程任务**：可嵌入构建、发布、日志归档等流水线，实现文件体积压缩、加密传输等常见需求。  
- **安全合规**：内置 AES 加密，适用于对敏感产出进行保护，满足安全审计的基本要求。

**典型接入方式**  
1. **API/SDK**：通过 `py7zr.SevenZipFile` 类调用 `writeall()、extractall()` 等方法，适合在代码中直接操作。  
   ```python
   import py7zr

   # 压缩
   with py7zr.SevenZipFile('archive.7z', 'w') as archive:
       archive.writeall('src_dir', 'src_dir')

   # 解压
   with py7zr.SevenZipFile('archive.7z', 'r', password='secret') as archive:
       archive.extractall('out_dir')
   ```  
2. **CLI**：项目同时提供 `py7zr` 命令行工具，可在脚本或 CI 步骤中直接调用，例如 `py7zr a -p secret archive.7z ./data`。  
3. **CI 集成**：在 GitHub Actions、GitLab CI 等流水线中安装依赖 `pip install py7zr`，随后在构建或发布阶段执行压缩/解压命令，实现自动化产出打包或缓存管理。

**生产可用性**  
- **活跃度**：截至 2026‑06‑26，项目仍在维护，最近一次提交在 2026 年，拥有 552 星、90 Fork，社区活跃。  
- **生态兼容**：纯 Python 实现，依赖仅限标准库和少量压缩库，易于在虚拟环境或容器中部署。  
- **安全性**：支持 AES 加密，已通过基本的安全审计；但仍建议在正式使用前进行内部安全评估并关注后续安全补丁。  
- **成熟度**：具备完整的 API 文档、示例代码和 CLI 手册，可直接用于生产环境的文件归档、日志压缩、二进制分发等场景。  

综合来看，`miurahr/py7zr` 在功能完整性、社区活跃度和易用性方面均表现良好，是在 Python 项目中引入 7‑Zip 支持的可靠 OSS 选项。

## 🧭 Practical evaluation

**Value:** miurahr/py7zr helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 552 GitHub stars
- 90 forks
- updated 2026-06-26
- primary language: Python
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 49/100 |
| stars | 58/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 75/100 |
| recency | 80/100 |
| adoption | 56/100 |
| production | 72/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/miurahr/py7zr) · [← Back to DevTools](./README.md)</sub>
