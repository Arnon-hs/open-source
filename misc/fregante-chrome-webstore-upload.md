# fregante/chrome-webstore-upload

[![Stars](https://img.shields.io/github/stars/fregante/chrome-webstore-upload?style=flat-square&color=yellow)](https://github.com/fregante/chrome-webstore-upload/stargazers) [![Forks](https://img.shields.io/github/forks/fregante/chrome-webstore-upload?style=flat-square&color=blue)](https://github.com/fregante/chrome-webstore-upload/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> Upload Chrome Extensions to the Chrome Web Store

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 410 |
| 🍴 **Forks** | 56 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`fregante/chrome-webstore-upload` is a small JavaScript utility that automates the upload of Chrome extensions to the Chrome Web Store via the official API. It bundles the authentication flow, zip‑packaging, and version bumping into a single CLI/Node‑module, making it easy to integrate publishing into CI pipelines or developer scripts. With 410 ⭐ on GitHub and recent activity (last commit 2026‑05‑12), it’s a mature enough tool for internal use, though the integration documentation is sparse.

**Value**  
- **Speed up releases** – eliminates the manual steps of logging into the Chrome Developer Dashboard, uploading the zip, and confirming the publish.  
- **CI/CD friendly** – can be called from npm scripts, GitHub Actions, or other automation tools to ship new extension builds automatically after tests pass.  
- **Consistent versioning** – the library can read the `manifest.json`, bump the version, and ensure the uploaded package matches the source code.

**Practical Adoption Path**  
1. **Review the README** – verify the required Google API credentials (OAuth client ID/secret) and the service‑account JSON file format.  
2. **Add the package**: `npm i -D chrome-webstore-upload` (or use `yarn`).  
3. **Create a small wrapper script** (e.g., `upload.js`) that loads the credentials, points to the built extension zip, and calls `chromeWebstore.upload`.  
4. **Test locally** with a test extension and a sandbox Chrome Web Store account to confirm the token exchange and upload succeed.  
5. **Integrate into CI** – add the script to your pipeline, store the service‑account JSON as a secret, and run the upload step after successful builds.  
6. **Monitor** – capture the API response (publish URL, errors) and add simple retry logic if needed.

**Production Readiness**  
- **Maturity**: Medium. The library is stable (410 ⭐, 56 forks) and actively maintained, but the integration guide is minimal, so you’ll need to validate the OAuth flow yourself.  
- **Risk**: The path from credentials to successful upload isn’t fully documented; missing scopes or mis‑configured service accounts can cause failures.  
- **Recommendation**: Use it for prototypes, internal tools, or as the basis of a custom publishing pipeline. Before rolling it out to production, perform a dedicated integration test, lock the version of the package, and add monitoring/alerting for upload failures. Once those checks are in place, the tool is reliable enough for regular release automation.

### Русский

**fregante/chrome-webstore-upload** — это небольшая JavaScript‑утилита, позволяющая автоматизировать загрузку и обновление расширений Chrome в Chrome Web Store через API. Она удобно вписывается в CI/CD‑конвейеры или скрипты деплоя, когда требуется быстро публиковать новые версии без ручного входа в консоль разработчика. Готовность к production — средняя: проект имеет активную звёздность (410 ★) и недавнее обновление, но путь интеграции не полностью документирован, поэтому перед вводом в продакшн рекомендуется протестировать процесс и проверить совместимость зависимостей.

### 中文

**项目简介**  
`fregante/chrome-webstore-upload` 是一个基于 JavaScript 的 CLI/库，帮助开发者一键将 Chrome 扩展上传至 Chrome Web Store，省去手动登录、打包、提交的繁琐步骤。

**价值**  
- **自动化**：通过脚本即可完成打包、认证、上传和发布，适合 CI/CD 流程。  
- **降低错误率**：统一使用 OAuth 2.0 token，避免手动复制 `.zip` 文件和表单导致的失误。  
- **社区认可**：已有 410+ Stars、56 Fork，活跃维护至 2026‑05‑12，说明在开源社区中得到了一定的信任。

**典型接入方式**  
1. **安装**：`npm i -D chrome-webstore-upload`（或 `yarn add -D`）。  
2. **获取凭证**：在 Google Cloud Console 为 Chrome Web Store 创建 OAuth Client，下载 `client_secret.json`，并在项目根目录生成 `refresh_token`（可使用官方示例脚本）。  
3. **配置**：在 `package.json` 或独立的 `upload-config.json` 中声明 `extensionId`、`zipPath`、`clientId`、`clientSecret`、`refreshToken`。  
4. **调用**：  
   ```js
   const upload = require('chrome-webstore-upload')({
     extensionId: 'your-extension-id',
     clientId: process.env.CWS_CLIENT_ID,
     clientSecret: process.env.CWS_CLIENT_SECRET,
     refreshToken: process.env.CWS_REFRESH_TOKEN,
   });

   // 上传并发布
   upload.uploadExisting(zipPath)
     .then(res => upload.publish())
     .then(() => console.log('发布成功'));
   ```  
   或者在 CI 中直接运行 `npx chrome-webstore-upload --source ./dist.zip --extension-id <id>`。

**生产可用性**  
- **成熟度**：中等（Medium）。代码已在多个开源项目中使用，适合作为原型或内部工具；在生产环境部署前建议：  
  - 检查依赖（Node ≥ 14、npm ≥ 6）。  
  - 编写错误处理与回滚逻辑，防止因上传失败导致版本卡死。  
  - 在 CI 中加入凭证加密（如 GitHub Secrets）并进行一次干跑验证。  
- **维护成本**：项目更新活跃，社区反馈及时，但官方文档较简略，首次集成时需要自行阅读源码或社区 Issue 来确认最新的 OAuth 流程。  

综上，`chrome-webstore-upload` 能显著提升 Chrome 扩展的发布效率，适合在 CI/CD 流程中自动化部署；在正式生产环境使用前做好凭证管理和错误处理，即可达到可靠的运行水平。

## 🧭 Practical evaluation

**Value:** fregante/chrome-webstore-upload may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 410 GitHub stars
- 56 forks
- updated 2026-05-12
- primary language: JavaScript

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 56/100 |
| topics | 0/100 |
| outlook | 59/100 |
| quality | 59/100 |
| recency | 80/100 |
| adoption | 52/100 |
| production | 62/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/fregante/chrome-webstore-upload) · [← Back to Misc](./README.md)</sub>
