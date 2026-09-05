# tonyanglesey/llama-apps

[![Stars](https://img.shields.io/github/stars/tonyanglesey/llama-apps?style=flat-square&color=yellow)](https://github.com/tonyanglesey/llama-apps/stargazers) [![Forks](https://img.shields.io/github/forks/tonyanglesey/llama-apps?style=flat-square&color=blue)](https://github.com/tonyanglesey/llama-apps/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-42%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 42/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Misc

## 📝 Summary

### English

Here's a brief summary and explanation for the open-source project:

**Summary:** This open-source project offers a self-hosted solution for Supabase Studio and Vercel alternatives, all running on a single 2GB VPS. This setup may be useful for specific workflows, but requires manual inspection and verification before adoption. While it has some production potential, it's best suited for prototypes or internal workflows.

**Value:** The project's value lies in its ability to provide a self-hosted alternative to popular services like Supabase Studio and Vercel, potentially reducing costs and increasing control over data and infrastructure. This setup may be particularly useful for teams or individuals with specific workflow requirements that can't be met by traditional cloud-based solutions.

**Practical Adoption Path:** To adopt this project, users should first carefully review the README, activity, and dependencies. They should also verify the license, maintenance, documentation, issues, and release cadence to ensure it meets their needs. Once verified, users can set up the project on a 2GB VPS and configure it according to their workflow requirements.

**Production Readiness:** The project has a medium production readiness score, indicating that it's suitable for prototypes or internal workflows, but may require additional checks and validation before being used in production. Users

### Русский

Self‑Hosted Supabase Studio + Vercel‑alternatives – это набор скриптов, позволяющих разместить полностью локальную версию Supabase Studio и лёгкие аналоги Vercel (деплой фронтенда, сервер‑функций и CDN) на едином 2 ГБ VPS. Такой стек удобно использовать для прототипов, внутренних демо‑проектов или небольших сервисов, когда требуется полностью контролируемая инфраструктура без внешних облачных провайдеров. Готовность к production — средняя: проект обновлён недавно, но перед внедрением следует проверить лицензию, активность репозитория, документацию и частоту релизов.

### 中文

**项目简介**  
Self-Hosted Supabase Studio 与 Vercel 替代方案可在一台 2 GB VPS 上同时部署，提供完整的后端（Supabase）管理界面和前端部署/边缘函数服务，适合资源受限的原型或内部项目。

**价值**  
- **一体化**：在同一台小型 VPS 上运行数据库、身份认证、实时 API（Supabase）以及静态站点/Serverless（Vercel 替代），省去多平台账号和跨云费用。  
- **成本低**：2 GB VPS 的月租仅在几美元，足以支撑小流量的全栈应用。  
- **可控性**：所有组件自托管，数据、密钥和配置完全掌握在自己手中，满足合规或隐私要求。

**典型接入方式**  
1. **准备 VPS**：使用 Ubuntu/Debian，确保 Docker 与 Docker‑Compose 已安装。  
2. **克隆仓库**：`git clone https://github.com/your-org/self-hosted-supabase-vercel.git`。  
3. **环境变量**：在根目录创建 `.env`，填入 Supabase（POSTGRES_PASSWORD、JWT_SECRET 等）和前端（VITE_…）所需的键值。  
4. **启动服务**：`docker-compose up -d`，Compose 会拉取 Supabase 镜像、PostgreSQL、pgAdmin（Studio）以及 Vercel‑compatible 的 `vercel-node` / `nitro` 镜像。  
5. **访问**：  
   - Supabase Studio → `http://<VPS_IP>:3000`（默认端口）  
   - 前端部署 → `http://<VPS_IP>:8080`（或自定义域名 + Nginx 反向代理）  
6. **CI/CD（可选）**：在 GitHub Actions 中加入 `docker push` 步骤，实现代码推送即自动更新容器。

**生产可用性**  
- **成熟度**：项目最近一次更新（2026‑07‑02）表明仍在维护，但社区活跃度、issue 处理速度和发布周期较少，属于 **中等** 级别。  
- **适用场景**：原型、内部工具、低并发的 SaaS MVP 或教学实验环境。  
- **风险与注意事项**  
  - **依赖检查**：确认 Docker 镜像的安全性，定期更新底层 PostgreSQL 与 Supabase 版本。  
  - **监控与备份**：自行部署监控（Prometheus/Grafana）和数据库备份策略，VPS 失效时数据恢复需自行处理。  
  - **许可证**：在生产使用前核实仓库的开源许可证（MIT/Apache 等），确保符合公司合规。  
  - **扩展性**：2 GB VPS 资源极限，流量或数据量增长时需迁移到更大实例或拆分服务。  

综上，该项目在资源受限的场景下提供了“一站式”自托管的全栈解决方案，适合快速验证想法或内部使用；若计划面向公网大流量服务，则需额外进行性能调优、灾备设计以及对项目活跃度进行更深入评估。

## 🧭 Practical evaluation

**Value:** Self-Hosted Supabase Studio and Vercel Alternatives on One 2GB VPS may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-07-02
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 50/100 |
| quality | 36/100 |
| recency | 80/100 |
| adoption | 0/100 |
| production | 51/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/tonyanglesey/llama-apps) · [← Back to Misc](./README.md)</sub>
