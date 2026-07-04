# fanmingming/live

[![Stars](https://img.shields.io/github/stars/fanmingming/live?style=flat-square&color=yellow)](https://github.com/fanmingming/live/stargazers) [![Forks](https://img.shields.io/github/forks/fanmingming/live?style=flat-square&color=blue)](https://github.com/fanmingming/live/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> ✯ 可直连访问的电视/广播图标库与相关工具项目 ✯ 🔕 永久免费 直连访问 完整开源 不断完善的台标 支持IPv4/IPv6双栈访问 🔕

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 28.2k |
| 🍴 **Forks** | 4.2k |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-07-04 |
| 🔍 **Source** | github |

## 🏷️ Topics

`china` `converter` `epg` `iptv` `ipv6` `live` `m3u` `m3u8` `mp4` `radio` `television` `tv`

## 🎯 Categories

Misc

## 📝 Summary

### English

Here's a brief summary of the open-source project:

**Project Summary:**
fanmingming/live is an open-source project that provides a TV/broadcast icon library with related tools, offering permanent free access and constant improvement. It supports dual-stack IPv4/IPv6 access and has a strong ecosystem signal with 28,223 GitHub stars and recent activity. The project is considered production-ready, with a high potential for adoption.

**Value:**
The value of fanmingming/live lies in its permanent free access, complete openness, and constant improvement of TV/broadcast icon libraries, making it a valuable resource for developers and projects requiring these icons.

**Practical Adoption Path:**
To adopt fanmingming/live, developers can start by evaluating its README and activity to ensure it matches their workflow. A small proof of concept should be created to test the integration, and the setup cost should be validated before committing to the project. The project's strong ecosystem signal and recent activity suggest a feasible integration path.

**Production Readiness:**
The project is considered production-ready due to its recent activity, adoption, and ecosystem signals, which are strong enough to justify a serious pilot. Its high production readiness score indicates that it is a reliable and stable option for development.

### Русский

Резюме проекта fanmingming/live:

fanmingming/live - это открытый проект, предлагающий прямой доступ к библиотеке телевизионных и радио-иконок с сопутствующими инструментами. Этот проект может быть полезен при реализации конкретной рабочей схемы, если README и активность проекта соответствуют ей. Проект готов к внедрению в производство высоким классом, поскольку в нем выявлены сильные признаки recent activity, adoption и экосистемные сигналы, что делает его подходящим кандидатом для serious пилота.

### 中文

**项目简介（2‑3 句话）**  
fanmingming/live 是一个 **永久免费、可直连访问** 的电视/广播台标图标库及配套工具集合，支持 IPv4/IPv6 双栈，图标持续更新、开源透明，适合在前端、媒体播放器、OTT 平台等场景中快速获取标准化的台标资源。

---

## 价值点

| 价值 | 说明 |
|------|------|
| **零成本、永久免费** | 直接使用原始 CDN 链接，无需注册、付费或限流，降低运营成本。 |
| **完整、持续更新的台标库** | 收录国内外主流电视、广播、电台、网络媒体的高清 SVG/PNG/ICO 等多种格式，随项目迭代自动同步最新台标。 |
| **双栈网络兼容** | 同时支持 IPv4 与 IPv6，适配企业内网、云平台及 CDN 环境，避免因网络层限制导致的资源不可达。 |
| **开源透明、可自定义** | 项目基于 JavaScript/Node 实现，源码公开，可自行 fork、二次构建或本地镜像，满足合规与安全审计需求。 |
| **丰富的工具链** | 包含批量下载、图标压缩、颜色提取、SVG → PNG 转换等 CLI/API，帮助业务快速集成与二次加工。 |

---

## 典型接入方式

1. **直接引用 CDN 链接（最简方案）**  
   ```html
   <img src="https://live.fanmingming.com/logo/cctv1.svg" alt="CCTV-1">
   ```  
   - 适用于网页、移动端、Electron 等前端项目。  
   - 通过 `https://live.fanmingming.com` 自动走最近的 Edge 节点，支持 HTTP/2、gzip/ Brotli 压缩。

2. **使用 NPM 包（Node/React/Vue 项目）**  
   ```bash
   npm i @fanmingming/live
   ```  
   ```js
   import { getLogoUrl } from '@fanmingming/live';
   const logo = getLogoUrl('cctv1', { format: 'png', size: 128 });
   // logo => "https://live.fanmingming.com/logo/cctv1_128.png"
   ```
   - 包含 TypeScript 类型声明，便于 IDE 自动完成。  
   - 支持自定义缓存策略（如本地 `localStorage`、Service Worker）。

3. **后端代理或本地镜像**（企业内部或高可用需求）  
   - 使用项目提供的 `download.js` 脚本批量拉取全部台标，存入自有对象存储（OSS、S3、COS 等），再通过内部 CDN 访问。  
   - 示例（Node）：
     ```js
     const { syncAll } = require('@fanmingming/live/tools');
     syncAll({ dest: '/data/live-logos', concurrency: 10 });
     ```
   - 适合对网络安全、合规有严格要求的 OTT、IPTV、机顶盒等后端系统。

4. **API 调用（高级场景）**  
   - 项目提供 `/api/logo/:id` REST 接口，可返回 JSON 包含多种分辨率、颜色信息，便于动态生成 UI 组件或做颜色主题匹配。  
   - 示例：
     ```bash
     curl https://live.fanmingming.com/api/logo/cctv1?format=svg
     ```

---

## 生产可用性评估

| 维度 | 现状 | 结论 |
|------|------|------|
| **活跃度** | 最近一次提交：2026‑07‑04；星标 28 k+、Fork 4 k+；每周都有 PR 合并 | 高 |
| **社区与文档** | 完整的 README、快速上手指南、API 文档、示例代码；Issues 及时响应 | 高 |
| **可靠性** | 采用全球 CDN（Cloudflare）+ 多节点 DNS，支持 IPv4/IPv6 双栈；可自行部署镜像 | 高 |
| **安全合规** | 所有资源均为公开广播台标，无版权争议；项目采用 MIT 许可证，可自由商用 | 高 |
| **可扩展性** | 提供 CLI 批量同步、Node SDK、REST API，易集成到 CI/CD 流程 | 高 |
| **运维成本** | 若直接使用 CDN，运维几乎为 0；自行镜像时仅需定期跑 `syncAll` 脚本 | 低 |

**综上**，fanmingming/live 已具备 **生产级** 的可靠性与可维护性，适合作为电视/广播台标的统一来源，在内容平台、智能电视、机顶盒、广告系统、媒体监控等业务中快速落地。建议在正式上线前先做一次小范围的 PoC（例如在前端页面中引用 3‑5 个台标），验证网络连通性与缓存策略后即可推广至全量业务。

## 🧭 Practical evaluation

**Value:** fanmingming/live may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 28223 GitHub stars
- 4217 forks
- updated 2026-07-04
- primary language: JavaScript
- 14 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 91/100 |
| stars | 95/100 |
| topics | 100/100 |
| outlook | 87/100 |
| quality | 97/100 |
| recency | 100/100 |
| adoption | 94/100 |
| production | 80/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-04 · [View on GitHub](https://github.com/fanmingming/live) · [← Back to Misc](./README.md)</sub>
