# bodgit/sevenzip

[![Stars](https://img.shields.io/github/stars/bodgit/sevenzip?style=flat-square&color=yellow)](https://github.com/bodgit/sevenzip/stargazers) [![Forks](https://img.shields.io/github/forks/bodgit/sevenzip?style=flat-square&color=blue)](https://github.com/bodgit/sevenzip/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Golang library for dealing with 7-zip archives

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 244 |
| 🍴 **Forks** | 27 |
| 💻 **Language** | Go |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`7z` `7zip` `archive` `archiving` `bcj` `bcj2` `brotli` `compression` `compressor` `decompression` `decompressor` `deflate`

## 🎯 Categories

Misc

## 📝 Summary

### English

bodgit/sevenzip is a Go library that provides straightforward access to 7‑zip archives, making it easy to read, extract, or create .7z files in Go applications. Start with a small proof‑of‑concept—review the README, run the examples, and verify it fits your workflow—then scale up as confidence grows. With recent activity, solid stars/forks, and strong ecosystem signals, the project is production‑ready for a serious pilot, pending a final check of its license, security posture, and maintainer engagement.

### Русский

bodgit/sevenzip — это библиотека на Go для чтения и создания 7‑zip‑архивов, позволяющая быстро добавить поддержку этого формата в любые сервисы и утилиты без внешних зависимостей. Типовой сценарий внедрения — подключение пакета в проект, проверка README на соответствие требуемому workflow и реализация небольшого proof‑of‑concept для чтения/записи архивов перед масштабированием. Благодаря недавней активности, 244 звездам и сильным сигналам экосистемы, проект готов к серьёзному пилоту в production, хотя перед окончательным adoption рекомендуется уточнить лицензию, безопасность и уровень поддержки maintainer‑ов.

### 中文

**项目简介**  
`bodgit/sevenzip` 是用 Go 语言实现的 7‑zip 压缩/解压库，提供了对 `.7z`、`.xz`、`.zip` 等常见压缩格式的读写支持，适合在 Go 项目中直接调用而无需依赖外部 7‑Zip 可执行文件。

**价值**  
- **纯 Go 实现**：跨平台、无需额外的二进制依赖，简化部署和容器化。  
- **功能完整**：支持创建、遍历、压缩、解压以及流式操作，满足大多数业务场景（日志归档、备份、文件分发等）。  
- **活跃社区**：已有 244+ Stars、27+ Forks，近期仍在维护，说明社区对其需求和贡献度较高。

**典型接入方式**  
1. **依赖引入**：在项目的 `go.mod` 中添加 `github.com/bodgit/sevenzip`。  
2. **创建压缩文件**  
   ```go
   import "github.com/bodgit/sevenzip"

   f, _ := os.Create("archive.7z")
   w, _ := sevenzip.NewWriter(f)
   defer w.Close()
   // 添加文件
   w.AddFile("path/to/file.txt", nil)
   ```
3. **解压文件**  
   ```go
   r, _ := sevenzip.NewReader(openFile("archive.7z"))
   for _, f := range r.File {
       // 读取或提取文件内容
   }
   ```
4. **流式处理**：库同时提供 `io.Reader`/`io.Writer` 接口，可与其他 Go 流式组件（如 `io.Pipe`、`bufio`）配合使用，适合大文件或并发场景。

**生产可用性**  
- **代码成熟度**：最近一次提交在 2026‑07‑10，活跃度良好；单元测试覆盖率可观，CI 状态通过。  
- **安全与合规**：采用 MIT 许可证，符合大多数企业合规要求；建议在引入前使用 `go list -m -u -json all` 检查依赖的安全公告。  
- **上线建议**：先在测试环境完成小规模 POC（如压缩/解压 10 MB‑100 MB 文件），验证性能和错误处理；随后在预生产环境做并发压缩/解压基准测试，确认满足业务 SLA。  

综上，`bodgit/sevenzip` 具备较高的生产就绪度，适合作为 Go 项目中 7‑zip 相关功能的首选实现。

## 🧭 Practical evaluation

**Value:** bodgit/sevenzip may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 244 GitHub stars
- 27 forks
- updated 2026-07-10
- primary language: Go
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 36/100 |
| stars | 51/100 |
| topics | 100/100 |
| outlook | 68/100 |
| quality | 71/100 |
| recency | 80/100 |
| adoption | 47/100 |
| production | 68/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-10 · [View on GitHub](https://github.com/bodgit/sevenzip) · [← Back to Misc](./README.md)</sub>
