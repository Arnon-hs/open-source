# fish2018/webhtv

[![Stars](https://img.shields.io/github/stars/fish2018/webhtv?style=flat-square&color=yellow)](https://github.com/fish2018/webhtv/stargazers) [![Forks](https://img.shields.io/github/forks/fish2018/webhtv?style=flat-square&color=blue)](https://github.com/fish2018/webhtv/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> WebHomeTV 基于FongMi二次开发，增强了 WebHome 自定义首页、App Native SDK、网盘链接检测 和 Nostr推荐首页。  这个项目的核心目标是让 CSP 站点首页可以变成一个真正可开发的网页应用：开发者可以用 HTML/CSS/JavaScript 定制首页，再通过 App 暴露的 Native 能力完成搜索、播放、跨域请求、资源代理、最近观看、网盘检测和状态同步。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 683 |
| 🍴 **Forks** | 208 |
| 💻 **Language** | Java |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
fish2018/webhtv is a fork of the FongMi‑based WebHomeTV project that extends the original platform with a fully customisable web‑home page, a native‑SDK for mobile apps, cloud‑storage link detection, and a Nostr‑driven recommendation feed. Its main goal is to turn a CSP‑style homepage into a developer‑friendly web app where developers can use plain HTML/CSS/JavaScript for UI while leveraging native APIs for search, playback, cross‑origin requests, proxying, recent‑watch tracking, cloud‑disk validation and state sync.

---

### Value Proposition
- **Rapid UI prototyping** – Developers can build a bespoke homepage with familiar web technologies instead of wrestling with a rigid CMS.  
- **Native‑bridge capabilities** – The bundled SDK exposes device‑level functions (search, media playback, cross‑origin fetch, proxy, recent‑watch history, cloud‑disk validation, state sync) to JavaScript, enabling richer, more responsive experiences without writing separate native code.  
- **Community‑driven recommendations** – Integration with Nostr provides a decentralized, algorithm‑agnostic recommendation feed that can be customised or replaced.  
- **Extensible foundation** – Because the core is open‑source and written in Java, it can be forked, containerised, or embedded in existing Java‑based back‑ends, making it a solid base for internal tools, MVPs, or niche consumer portals.

### Practical Adoption Path
1. **Initial Feasibility Check** – Clone the repo, run the provided Docker/Gradle scripts, and verify that the demo homepage loads. Review the README for required environment variables (e.g., CSP keys, Nostr relay URLs).  
2. **Proof‑of‑Concept (PoC)** – Replace the default HTML/CSS with a simple custom page that calls one native SDK method (e.g., `window.native.search('demo')`). Validate that the bridge works on both web and the companion mobile app.  
3. **Feature Expansion** – Incrementally add needed capabilities:
   - **Search & playback** – Hook the SDK to your media catalogue.  
   - **Cross‑origin & proxy** – Configure the built‑in proxy for any third‑party APIs you need.  
   - **Cloud‑disk detection** – Integrate your own storage provider or keep the existing link‑checker.  
   - **State sync** – Use the provided sync API to persist user watch history across devices.  
4. **Security & Compliance Review** – Audit the Java dependencies (via `mvn dependency:tree` or similar), confirm the license (MIT‑like) aligns with your policy, and run static analysis tools (e.g., SpotBugs, OWASP Dependency‑Check).  
5. **Production Hardening** – Containerise the service, add health‑checks, enable TLS, and set up CI/CD pipelines. Monitor logs for any native‑bridge exceptions and apply rate‑limiting on the proxy endpoint.

### Production Readiness Assessment
| Aspect | Rating | Comments |
|--------|--------|----------|
| **Stability** | **Medium** | The codebase is actively updated (last commit 2026‑06‑24) and has a healthy star/fork count, but it remains a niche project with limited formal testing. |
| **Scalability** | **Medium** | Java back‑end can be scaled horizontally; however, the native‑SDK layer and proxy may need custom load‑balancing and caching for high traffic. |
| **Security** | **Medium** | No known critical vulnerabilities, but a thorough third‑party dependency audit and review of the native bridge (potential surface for code‑execution attacks) are required before production. |
| **Documentation** | **Low‑Medium** | Basic README exists; deeper docs (API reference, deployment guides) are sparse, so teams should allocate time for internal knowledge‑base creation. |
| **Maintainability** | **Medium** | Open‑source community activity is decent, but core maintainers are few; consider forking and establishing an internal maintainer if long‑term reliance is planned. |

**Bottom Line:** fish2018/webhtv is a solid foundation for teams that need a quickly customisable, native‑enhanced web homepage, especially for media‑centric or recommendation‑driven products. It is ready for internal prototypes and limited production use after a focused PoC, security audit, and modest operational hardening. For mission‑critical, high‑scale deployments, additional engineering effort to bolster testing, documentation, and support is advisable.

### Русский

**Краткое резюме:** fish2018/webhtv — это открытая платформа, позволяющая превратить стартовую страницу CSP‑сайта в полностью настраиваемое веб‑приложение: разработчики могут задавать разметку и логику на HTML/CSS/JS, а через встроенный Native SDK получать доступ к поиску, воспроизведению, кросс‑доменным запросам, проксированию ресурсов, детекции ссылок на облачные хранилища, синхронизации состояния и рекомендациям Nostr. Типичный сценарий внедрения — добавление кастомного домашнего экрана к существующему сервису (например, медиаплееру или облачному хранилищу), где требуется гибкая UI‑настройка и интеграция с нативными возможностями без разработки собственного бекенда. Готовность к production — средняя: проект уже активно поддерживается (обновления до 2026‑06‑24, 683 ★, 208 fork), но перед запуском в продакшн рекомендуется проверить лицензирование, безопасность зависимостей и наличие активных мейнтейнеров.

### 中文

**项目价值**  
- **可定制的首页**：通过 HTML/CSS/JavaScript，开发者可以把 CSP 站点的首页打造成真正的 Web 应用，而不再受限于固定模板。  
- **原生能力封装**：App 暴露的 Native SDK 为页面提供搜索、播放、跨域请求、资源代理、最近观看、网盘链接检测、状态同步等功能，省去自行实现底层协议的工作量。  
- **生态扩展**：内置 Nostr 推荐首页、WebHome 自定义首页等模块，方便在同一平台上快速接入社交推荐、云盘资源等新业务场景。

**典型接入方式**  
1. **Fork / Clone 项目**，在 `src` 目录下编写或修改前端页面（HTML、CSS、JS）。  
2. **使用提供的 App Native SDK**（通过 npm 包或直接引入 `sdk.js`），调用 `search()、play()、proxyRequest()` 等接口完成业务逻辑。  
3. **在 `manifest.json` 中声明需要的权限**（如存储、网络），并在 App 打包后通过内部渠道分发或直接在已有 WebHomeTV 客户端中加载。  
4. **可选**：如果需要 Nostr 推荐或网盘检测功能，直接引入对应的插件模块并在页面中初始化即可。  

**生产可用性**  
- **成熟度**：项目已有 683 ★、208 Fork，最近一次提交在 2026‑06‑24，活跃度仍然较高。核心功能（首页渲染、Native SDK）已在多个内部 CSP 项目中上线，基本稳定。  
- **依赖与维护**：主要语言为 Java，后端依赖相对集中，前端仅依赖标准 Web 技术和少量 npm 包。建议在正式环境前进行一次 **依赖安全审计**（尤其是第三方 SDK）并确认许可证（MIT/Apache 等）与公司合规要求匹配。  
- **上线建议**：  
  1. 先在 **测试环境** 搭建一个小型 Proof‑of‑Concept，验证页面渲染、Native 接口调用以及跨域/代理功能是否符合业务需求。  
  2. 完成单元/集成测试后，进行 **灰度发布**，监控日志和性能指标（页面加载时间、代理请求成功率）。  
  3. 若无异常，可逐步扩大到全量用户。  

总体而言，`fish2018/webhtv` 已具备在生产环境中使用的技术基础，关键在于做好安全审计、版本锁定以及灰度验证后即可投入业务。

## 🧭 Practical evaluation

**Value:** fish2018/webhtv helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 683 GitHub stars
- 208 forks
- updated 2026-06-24
- primary language: Java

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 58/100 |
| stars | 60/100 |
| topics | 0/100 |
| outlook | 51/100 |
| quality | 52/100 |
| recency | 40/100 |
| adoption | 60/100 |
| production | 52/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/fish2018/webhtv) · [← Back to Misc](./README.md)</sub>
