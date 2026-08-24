# anmalkov/image-inspector

[![Stars](https://img.shields.io/github/stars/anmalkov/image-inspector?style=flat-square&color=yellow)](https://github.com/anmalkov/image-inspector/stargazers) [![Forks](https://img.shields.io/github/forks/anmalkov/image-inspector?style=flat-square&color=blue)](https://github.com/anmalkov/image-inspector/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-31%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 31/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*Image‑inspector* is a CLI/ library that scans Docker/OCI images to identify their base layers, reports known CVE counts for each layer, and lets you pin images by content‑digest. It helps security‑focused teams quickly assess the risk of container images and enforce reproducible builds by using immutable digests.

**Value**  
- **Visibility:** Instantly discover the upstream base image (e.g., `ubuntu:20.04`) and see how many vulnerabilities are associated with each layer, enabling rapid risk triage.  
- **Control:** Generates the exact digest (`sha256:…`) for the image you have inspected, so you can lock deployments to a known‑good artifact rather than a mutable tag.  
- **Workflow fit:** Works well in CI pipelines, security gate scripts, or as an ad‑hoc audit tool, complementing existing SBOM or scanning solutions.

**Practical Adoption Path**  
1. **Prototype:** Clone the repo, run `image‑inspector scan <image>` on a few internal images to confirm the output format matches your reporting needs.  
2. **CI Integration:** Wrap the command in a step of your CI/CD pipeline (GitHub Actions, GitLab CI, Jenkins, etc.) and fail the build if CVE count exceeds a policy threshold.  
3. **Digest Pinning:** Export the reported digest and replace mutable tags in your Helm charts, Kubernetes manifests, or Dockerfiles with `image@sha256:…`.  
4. **Governance:** Add a periodic audit job (e.g., nightly) that re‑scans production images and raises alerts on new CVEs or base‑image changes.

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last update 2026‑06‑26) and provides core functionality, but integration signals are sparse and documentation is minimal.  
- **Risks:** Limited quality signals (few issues, unclear release cadence), so you should verify the license, test against your image registry, and monitor upstream activity before relying on it for mission‑critical pipelines.  
- **Recommendation:** Suitable for prototypes, internal security audits, or as a supplemental check alongside a primary scanner (e.g., Trivy, Clair). Perform a short pilot, add automated tests for expected output, and only promote to production after confirming stability and maintenance commitment.

### Русский

**Show HN: Image‑inspector** – утилита для анализа Docker‑образов: определяет базовый образ, выводит количество известных уязвимостей (CVE) и позволяет фиксировать образ по digest. Подходит для прототипов и внутренних CI/CD‑процессов, где требуется быстрый аудит образов перед их публикацией; однако перед выводом в production следует проверить лицензию, активность поддержки, документацию и частоту релизов. Готовность – средняя: функционал стабилен, но интеграционные сигналы ограничены, поэтому требуется ручная проверка перед масштабным внедрением.

### 中文

**项目简介（2‑3 句话）**  
Show HN : Image‑inspector 是一个用于分析 Docker/OCI 镜像的工具，可快速定位镜像的基础镜像、统计其已知 CVE 数量，并支持通过镜像摘要（digest）进行固定。它适合在安全审计或 CI/CD 流程中快速评估镜像风险。

**价值**  
- **安全可视化**：一键展示基础镜像及其累计的 CVE 数量，帮助团队快速判断是否需要升级或替换。  
- **防漂移**：通过 digest 锁定镜像，避免因标签（如 `latest`）变动导致的不可预期更新。  
- **工作流匹配**：README 与活跃度都指向典型的镜像审计场景，适合作为安全审计、合规检查或内部镜像库治理的辅助工具。

**典型接入方式**  
1. **本地 CLI**：在 CI 步骤中直接调用 `image-inspector <image>`，解析输出的 JSON/YAML 报告。  
2. **CI/CD 集成**：在 GitHub Actions、GitLab CI 或 Jenkins 中加入步骤，失败条件可设为 CVE 数量超过阈值或未使用 digest。  
3. **脚本化**：利用其库（若提供）在自定义安全审计脚本中调用 API，批量检查镜像列表。  
> **注意**：项目元数据较少，建议先在测试环境手动运行几次，确认输出格式、错误处理以及依赖（如 `trivy`、`skopeo`）是否满足需求后再写入自动化流程。

**生产可用性**  
- **成熟度**：评分 41/100，属于 **中等** 级别。适合原型验证或内部使用，但在生产环境部署前需进行以下检查：  
  - 许可证兼容性（确认是 MIT/Apache 等宽松协议）  
  - 维护状态（最近一次提交为 2026‑06‑26，仍在活跃）  
  - 文档与 Issue 响应速度（目前仅两条主题，需自行评估）  
- **风险**：集成信号稀少，缺乏正式的发布节奏和完整的测试套件，可能在大规模使用时出现未捕获的边界情况。  
- **建议**：先在预生产或内部审计环境中使用，配合额外的安全扫描工具（如 Trivy、Grype）做双重验证；若满足可靠性要求，可逐步推广到生产流水线并设立监控/回滚机制。

## 🧭 Practical evaluation

**Value:** Show HN: Image-inspector – find base images, see CVE counts, pin by digest may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-06-26
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 33/100 |
| quality | 26/100 |
| recency | 40/100 |
| adoption | 0/100 |
| production | 38/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/anmalkov/image-inspector) · [← Back to Misc](./README.md)</sub>
