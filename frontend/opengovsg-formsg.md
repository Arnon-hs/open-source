# opengovsg/FormSG

[![Stars](https://img.shields.io/github/stars/opengovsg/FormSG?style=flat-square&color=yellow)](https://github.com/opengovsg/FormSG/stargazers) [![Forks](https://img.shields.io/github/forks/opengovsg/FormSG?style=flat-square&color=blue)](https://github.com/opengovsg/FormSG/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Form builder for the Singapore Government

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 346 |
| 🍴 **Forks** | 131 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`hacktoberfest`

## 🎯 Categories

Frontend · Database

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
FormSG is an open‑source, TypeScript‑based form builder created for Singapore government digital services. It lets teams assemble user‑facing forms and related UI components quickly, reducing the amount of custom front‑end code required. With a modest community (≈350 ★, 130 forks) and recent updates, it is suitable for prototypes or internal tools, though a careful review is needed before production use.

**Value**  
- **Accelerated UI delivery:** Pre‑built, reusable form components let developers focus on business logic instead of hand‑crafting input fields, validation, and layout.  
- **Consistency & compliance:** The library follows government design guidelines, helping teams maintain a uniform look and meet accessibility standards out of the box.  
- **Lower maintenance overhead:** Centralised component updates propagate to all forms, cutting down duplicated UI work across projects.

**Practical Adoption Path**  
1. **Initial evaluation** – Clone the repo, run the demo locally, and compare its component set with your required form fields.  
2. **Security & licensing check** – Verify the MIT/Apache license (as listed) and run a dependency scan (e.g., Snyk) to confirm no known vulnerabilities.  
3. **Pilot integration** – Replace a small, non‑critical internal form with a FormSG component, performing manual UI/UX inspection to ensure it meets your style and data‑handling expectations.  
4. **Feedback loop** – Document any gaps (e.g., missing field types or custom validation) and either extend the library or wrap it with adapters.  
5. **Scale up** – Once the pilot is stable, gradually migrate additional forms, consolidating shared state and API contracts.

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last commit 2026‑05‑11) and has enough community traction to be reliable for internal or prototype use.  
- **Risks:** No major metadata issues, but the license, security posture, and long‑term maintainer commitment still need a final audit.  
- **Recommendation:** Suitable for internal workflows or MVPs after a short validation phase; for customer‑facing production systems, perform the above security/license review and consider a fallback plan (e.g., maintaining a fork) before full deployment.

### Русский

**opengovsg/FormSG** — это открытый конструктор форм, ориентированный на проекты правительства Сингапура, который позволяет быстро собрать пользовательский интерфейс без написания кастомного UI. Он идеален для ускорения разработки продуктовых экранов, повторного использования готовых компонентов и повышения эффективности фронтенд‑доставки, однако перед внедрением требуется ручная проверка интеграции из‑за ограниченной метаданных. Готовность к production — средняя: проект подходит для прототипов и внутренних процессов, но перед запуском в продакшн следует убедиться в лицензии, безопасности и наличии активных мейнтейнеров.

### 中文

**项目简介**  
opengovsg/FormSG 是新加坡政府开源的表单构建器，提供可视化的表单编辑和数据存储功能，帮助团队快速搭建用户交互界面，减少自研 UI 的工作量。

**价值**  
- 通过复用成熟的表单组件，显著缩短前端产品的开发周期。  
- 内置数据持久化和验证逻辑，降低后端实现成本。  
- 开源且基于 TypeScript，易于与现有前端框架（React/Vue 等）集成。

**典型接入方式**  
1. **依赖安装**：`npm i @opengovsg/forms`（或对应的 npm 包）。  
2. **在项目中引入**：在页面或组件中导入 `FormBuilder`、`FormRenderer` 等 UI 组件。  
3. **配置表单**：使用 JSON/YAML 定义表单结构或直接在 UI 中拖拽生成。  
4. **后端对接**：通过提供的 REST/GraphQL 接口或自定义 webhook，将表单提交数据发送至内部服务。  
5. **手动审查**：由于元数据集成信息较少，建议在正式接入前进行一次安全与兼容性审查。

**生产可用性**  
- **成熟度**：中等（适合原型、内部工作流或对 UI 敏捷需求高的项目），在生产环境使用前需检查依赖版本、维护者活跃度以及安全审计。  
- **社区活跃度**：346 ⭐、131 🍴，最近一次更新为 2026‑05‑11，主语言为 TypeScript。  
- **风险**：暂无重大元数据风险，但仍需对许可证、潜在安全漏洞以及维护者响应速度进行最终评估。

## 🧭 Practical evaluation

**Value:** opengovsg/FormSG helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 346 GitHub stars
- 131 forks
- updated 2026-05-11
- primary language: TypeScript
- 1 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 53/100 |
| stars | 54/100 |
| topics | 13/100 |
| outlook | 68/100 |
| quality | 66/100 |
| recency | 100/100 |
| adoption | 54/100 |
| production | 74/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/opengovsg/FormSG) · [← Back to Frontend](./README.md)</sub>
