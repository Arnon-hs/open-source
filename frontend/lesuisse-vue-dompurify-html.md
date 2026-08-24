# LeSuisse/vue-dompurify-html

[![Stars](https://img.shields.io/github/stars/LeSuisse/vue-dompurify-html?style=flat-square&color=yellow)](https://github.com/LeSuisse/vue-dompurify-html/stargazers) [![Forks](https://img.shields.io/github/forks/LeSuisse/vue-dompurify-html?style=flat-square&color=blue)](https://github.com/LeSuisse/vue-dompurify-html/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-47%2F100-brightgreen?style=flat-square)](#)

> Safe replacement for the v-html directive

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 335 |
| 🍴 **Forks** | 29 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 47/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`dom-xss` `dompurify` `security` `vue` `vuejs` `xss`

## 🎯 Categories

Frontend · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
LeSuisse/vue-dompurify-html is a lightweight Vue.js plugin that replaces the built‑in `v-html` directive with a safe, DOM‑purified alternative powered by DOMPurify. By sanitizing HTML before rendering, it mitigates XSS risks while keeping the developer experience familiar to Vue users. The package is written in TypeScript, has ~335 GitHub stars, and is actively maintained as of May 2026.

**Value**  
- **Security first**: Automatically strips malicious scripts and unsafe attributes, eliminating a common attack surface when rendering user‑generated HTML.  
- **Zero‑config integration**: Works like the native `v‑html` directive, so existing Vue components can be switched with a single import and minor template change.  
- **Type‑safe & modern**: TypeScript typings and up‑to‑date dependencies make it easy to adopt in contemporary Vue 3 projects without sacrificing compile‑time safety.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Add the package (`npm i vue-dompurify-html`) and replace a few `v-html` usages with `<div v-dompurify-html="rawHtml" />` in a sandbox branch. Verify that the rendered output matches expectations and that no console XSS warnings appear.  
2. **Documentation Review** – Follow the README’s quick‑start guide; it includes basic configuration (e.g., custom DOMPurify hooks) and a fallback for server‑side rendering.  
3. **Automated Tests** – Write unit tests that feed known‑malicious payloads into the component and assert that the output is sanitized. This ensures the integration stays reliable as your codebase evolves.  
4. **Gradual Rollout** – Expand usage to all components that render external HTML, monitoring security logs and performance metrics.  

**Production Readiness**  
- **Maturity**: Medium. The library is stable, has a respectable star count, and recent commits (as of 2026‑05‑11) indicate active maintenance, but it is still positioned primarily for prototyping and internal tools.  
- **Dependencies**: Relies on DOMPurify, a well‑vetted library with a strong security track record. Verify that the version pinned in `package.json` aligns with your organization’s vulnerability policy.  
- **Risk Considerations**: Conduct a final license review (MIT) and run a security audit of the transitive dependencies. Ensure you have a process for monitoring upstream releases, as any critical DOMPurify update should be propagated promptly.  

Overall, vue-dompurify-html offers a pragmatic, low‑overhead way to secure HTML rendering in Vue applications, making it a solid candidate for internal prototypes and, with proper vetting, for production use where XSS mitigation is required.

### Русский

**LeSuisse/vue-dompurify-html** — это лёгкая библиотека‑обёртка, заменяющая директиву `v-html` безопасным HTML‑контентом, очищенным через DOMPurify. Она подходит для быстрого прототипирования функций, где требуется вывод пользовательского HTML (например, в чат‑ботах, RAG‑интерфейсах или генеративных UI‑компонентах), позволяя начать с небольшого proof‑of‑concept и проверить README‑пример. По готовности к продакшну — средний уровень: проект имеет 335 ★, активные коммиты и TypeScript‑код, но перед выпуском в прод необходимо оценить лицензию, актуальность зависимостей и наличие поддерживающих мейнтейнеров.

### 中文

**项目简介**  
LeSuisse/vue-dompurify-html 是一个基于 DOMPurify 的 Vue 插件，用来安全地替代原生的 `v‑html` 指令，防止 XSS 攻击并保持模板渲染的灵活性。  

**价值**  
- **安全防护**：在将 HTML 字符串插入页面前自动进行严格的净化，消除潜在的脚本注入风险。  
- **开发友好**：与 Vue 的指令体系无缝集成，只需在模板中使用 `v-dompurify-html` 即可，无需额外的手动清洗代码。  
- **轻量且可配置**：基于 TypeScript 实现，体积小，支持自定义 DOMPurify 配置，满足不同安全策略的需求。  

**典型接入方式**  
1. **安装**：`npm i vue-dompurify-html`（或 `yarn add vue-dompurify-html`）。  
2. **全局注册**（推荐）：在项目入口文件（如 `main.ts`）中  
   ```ts
   import { createApp } from 'vue';
   import VueDomPurifyHTML from 'vue-dompurify-html';
   const app = createApp(App);
   app.use(VueDomPurifyHTML);
   app.mount('#app');
   ```  
3. **局部使用**（如仅在某些组件中）：在组件 `script` 中 `import { vDomPurifyHtml } from 'vue-dompurify-html';` 并在 `directives` 中声明。  
4. **模板使用**：  
   ```html
   <div v-dompurify-html="rawHtmlContent"></div>
   ```  
   如需自定义配置，可在插件初始化时传入 DOMPurify 选项。  

**生产可用性**  
- **成熟度**：已有 335+ ⭐、29+ fork，最近一次更新在 2026‑05‑11，活跃度较好。  
- **适用场景**：非常适合内部系统、原型或对安全有明确需求的前端项目；在正式生产环境使用前，建议：  
  1. **审查依赖**：确认 DOMPurify 及其 transitive dependencies 的安全报告。  
  2. **配置审计**：根据业务安全策略，明确允许的标签、属性和 URL 方案。  
  3. **监控更新**：定期检查插件和 DOMPurify 的版本更新，以获取安全补丁。  
- **风险**：目前暂无重大许可证或元数据风险，但仍需确认项目维护者的响应速度以及对安全漏洞的修复时效。  

总体而言，LeSuisse/vue-dompurify-html 在提供安全 HTML 渲染的同时保持了极低的接入成本，是前端项目在生产环境中实现 XSS 防护的可靠选择，只要做好依赖审计和配置管理即可。

## 🧭 Practical evaluation

**Value:** LeSuisse/vue-dompurify-html helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 335 GitHub stars
- 29 forks
- updated 2026-05-11
- primary language: TypeScript
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 37/100 |
| stars | 54/100 |
| topics | 75/100 |
| outlook | 45/100 |
| quality | 53/100 |
| recency | 20/100 |
| adoption | 49/100 |
| production | 48/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/LeSuisse/vue-dompurify-html) · [← Back to Frontend](./README.md)</sub>
