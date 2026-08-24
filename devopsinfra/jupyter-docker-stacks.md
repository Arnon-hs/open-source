# jupyter/docker-stacks

[![Stars](https://img.shields.io/github/stars/jupyter/docker-stacks?style=flat-square&color=yellow)](https://github.com/jupyter/docker-stacks/stargazers) [![Forks](https://img.shields.io/github/forks/jupyter/docker-stacks?style=flat-square&color=blue)](https://github.com/jupyter/docker-stacks/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> Ready-to-run Docker images containing Jupyter applications

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 8.4k |
| 🍴 **Forks** | 3k |
| 💻 **Language** | Python |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`docker` `ipython` `ipython-notebook` `jupyter` `jupyter-notebook` `jupyter-notebooks` `jupyterhub` `jupyterlab` `notebook` `python`

## 🎯 Categories

DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
jupyter/docker‑stacks provides ready‑to‑run Docker images that bundle JupyterLab, JupyterHub, and a curated set of AI/ML libraries. With a single `docker pull` you get a fully configured notebook environment, making it easy to prototype AI features, build RAG or agent workflows, and evaluate model tooling without assembling the stack from scratch.  

**Value**  
The project eliminates the boilerplate of installing and configuring Jupyter, Python, and common ML packages, letting teams focus on model development and experimentation. Because the images are versioned and reproducible, they also serve as a reliable baseline for CI/CD pipelines and for sharing environments across data‑science and engineering teams.  

**Practical Adoption Path**  
1. **Evaluate** – Pull the desired stack (e.g., `jupyter/scipy-notebook`) and run it locally to verify that required libraries and extensions are present.  
2. **Customize** – Extend the base image with a Dockerfile that adds project‑specific dependencies or authentication hooks.  
3. **Integrate** – Deploy the custom image to your container orchestration platform (Kubernetes, Docker Swarm, etc.) and expose it via JupyterHub or a reverse proxy for team access.  
4. **Automate** – Incorporate the image into CI pipelines to spin up reproducible test notebooks for model validation.  

**Production Readiness**  
- **Activity & Adoption** – 8.4 k GitHub stars, ~3 k forks, frequent commits (last update 2026‑07‑13) and wide use in the Jupyter ecosystem indicate strong community support.  
- **Stability** – Official images are version‑pinned and built on well‑maintained base layers, providing predictable behavior across environments.  
- **Risk Considerations** – No major metadata issues, but a final review of the Apache‑2.0 license compliance, container security scanning, and maintainer responsiveness is advisable before a full‑scale rollout.  

Overall, jupyter/docker‑stacks is a mature, production‑ready foundation for quickly adding AI capabilities to any workflow.

### Русский

**jupyter/docker-stacks** — готовые Docker‑образы с предустановленными Jupyter‑приложениями, которые позволяют быстро добавить AI‑возможности в проекты без необходимости собирать стек с нуля. Их обычно используют для прототипирования AI‑фич, построения RAG‑ или агентных пайплайнов и оценки новых моделей/инструментов в изолированной среде. Проект имеет высокую готовность к production: активные обновления, широкое принятие (8443 звёзд, 2989 форков), сильная экосистема и поддержка Python, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
jupyter/docker‑stacks 提供即开即用的 Docker 镜像，预装 Jupyter Notebook、JupyterLab、JupyterHub 以及常用的科学计算与机器学习库，让开发者无需自行配置环境即可直接启动交互式 AI/ML 工作流。

**价值**  
- **快速原型**：一键启动完整的 Jupyter 环境，省去环境搭建和依赖冲突的时间，适合快速验证 AI 特性、构建 RAG（检索增强生成）或智能体工作流。  
- **统一平台**：通过统一的 Docker 镜像，团队可以在本地、CI/CD 或云端保持一致的运行时，降低环境漂移风险。  
- **生态兼容**：镜像内已集成常用的 Python 包（NumPy、Pandas、scikit‑learn、TensorFlow、PyTorch 等），便于直接接入已有模型或工具链。

**典型接入方式**  
1. **Docker Pull & Run**  
   ```bash
   docker pull jupyter/base-notebook   # 任选具体 stack，如 scipy-notebook、datascience-notebook
   docker run -p 8888:8888 jupyter/base-notebook
   ```  
   - 通过 `-e JUPYTER_TOKEN=your_token` 设置访问凭证。  
2. **Docker‑Compose**（适用于多容器或持久化需求）  
   ```yaml
   version: "3.8"
   services:
     notebook:
       image: jupyter/datascience-notebook
       ports: ["8888:8888"]
       volumes: ["./work:/home/jovyan/work"]
       environment:
         - JUPYTER_TOKEN=securetoken
   ```  
3. **Kubernetes**（在生产集群中部署）  
   - 使用官方提供的 Helm chart `jupyterhub/jupyterhub`，将 `singleuser.image.name` 指向所需的 stack 镜像，实现按需扩缩容。  
4. **CI/CD 集成**  
   - 在 GitHub Actions、GitLab CI 等流水线中直接使用 `docker://jupyter/scipy-notebook` 作为测试环境，执行 notebook 测试或模型训练脚本。

**生产可用性**  
- **活跃度**：截至 2026‑07‑13，项目拥有 8.4k+ 星、3k+ Fork，最近一次提交在数天前，表明维护活跃。  
- **成熟度**：官方提供多套经过长期验证的镜像（base、minimal、datascience、scipy 等），并在 JupyterHub、Kubernetes 等生产级部署场景中得到广泛使用。  
- **安全与合规**：镜像基于官方的 `python` 基础镜像，定期发布安全更新；但在正式投产前仍建议使用内部镜像扫描工具检查 CVE，并确认镜像的许可证（BSD‑3‑Clause）符合企业合规要求。  
- **可扩展性**：支持自定义 Dockerfile 在官方镜像之上添加私有库或企业内部工具，且可通过 Kubernetes 的资源配额、Pod Autoscaler 等机制实现弹性伸缩。  

综上，jupyter/docker‑stacks 具备高可用、易集成、社区支持强的特性，是在 AI/ML 项目中快速搭建交互式原型或作为生产环境基础设施的可靠选择。

## 🧭 Practical evaluation

**Value:** jupyter/docker-stacks helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 8443 GitHub stars
- 2989 forks
- updated 2026-07-13
- primary language: Python
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 87/100 |
| stars | 84/100 |
| topics | 100/100 |
| outlook | 64/100 |
| quality | 78/100 |
| recency | 40/100 |
| adoption | 84/100 |
| production | 64/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/jupyter/docker-stacks) · [← Back to DevOps & Infra](./README.md)</sub>
