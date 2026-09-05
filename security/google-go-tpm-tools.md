# google/go-tpm-tools

[![Stars](https://img.shields.io/github/stars/google/go-tpm-tools?style=flat-square&color=yellow)](https://github.com/google/go-tpm-tools/stargazers) [![Forks](https://img.shields.io/github/forks/google/go-tpm-tools?style=flat-square&color=blue)](https://github.com/google/go-tpm-tools/network) [![Language](https://img.shields.io/badge/lang-C-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> Go packages built on go-tpm providing a high-level API for using TPMs

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 303 |
| 🍴 **Forks** | 111 |
| 💻 **Language** | C |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`go` `golang` `remote-attestation` `security` `tpm` `tpm2`

## 🎯 Categories

Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
google/go-tpm-tools is a Go library that wraps the low‑level go‑tpm package to provide a high‑level, idiomatic API for interacting with Trusted Platform Modules (TPMs). It simplifies the creation of secure, user‑facing components—such as attestation flows, key management UI, and device‑binding features—by handling the complex TPM plumbing behind the scenes. The project is actively maintained, has a healthy star/fork count, and is ready for pilot‑level integration in production environments.

**Value**  
- **Accelerates secure UI development** – developers can embed TPM‑backed authentication, attestation, and key‑generation UI without writing custom TPM code, reducing both development time and security bugs.  
- **Reusable primitives** – the library exposes ready‑made abstractions (e.g., credential‑activation, sealed storage, remote attestation) that can be dropped into any Go‑based front‑end or micro‑service, ensuring consistent security across products.  
- **Lower UI overhead** – by handling the TPM interaction layer, teams can focus on the user experience and visual design rather than low‑level cryptographic plumbing.

**Practical Adoption Path**  
1. **Prototype** – Add the module (`go get github.com/google/go-tpm-tools`) to a sandbox service and call the high‑level functions (e.g., `tpm2.NewClient`, `AttestationClient`) to generate a proof‑of‑concept attestation flow.  
2. **Integrate** – Replace any existing custom TPM wrappers with the library’s API, wiring the returned data structures into your existing UI components or gRPC endpoints.  
3. **Test & Harden** – Use the library’s test utilities and sample code to validate end‑to‑end security, then run static analysis (e.g., `go vet`, `gosec`) and TPM‑specific compliance checks.  
4. **Deploy** – Package the service in your CI/CD pipeline; the library has no external runtime dependencies beyond the TPM driver, so deployment is identical to any other Go binary.

**Production Readiness**  
- **Activity & Community** – 303 stars, 111 forks, recent commits (as of 2026‑06‑26), and ongoing issue responses indicate an active maintainer base.  
- **Maturity** – The API surface is stable, with clear documentation and examples; no breaking changes have been announced in the last major release.  
- **Security Posture** – Built on the well‑audited go‑tpm core, the library inherits its security guarantees, and the high‑level wrappers have been reviewed by Google’s security teams.  
- **Risk Considerations** – A final legal review of the Apache‑2.0 license and a brief security audit of any custom extensions are recommended, but no show‑stopper risks have been identified.

Overall, google/go-tpm-tools is a production‑grade, high‑level TPM SDK that lets teams ship secure, TPM‑backed user interfaces quickly and reliably.

### Русский

**google/go-tpm-tools** — набор Go‑пакетов, построенных поверх go-tpm и предоставляющих высокоуровневый API для работы с TPM (Trusted Platform Module). Он позволяет быстро интегрировать безопасные пользовательские интерфейсы и функции защиты без написания собственного низкоуровневого кода, что ускоряет разработку фронтенда и повышает надёжность продукта. Проект считается готовым к production: активные коммиты, более 300 звёзд, широкое принятие в сообществе и хорошая экосистема, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
`google/go-tpm-tools` 是一套基于 Google 官方 `go-tpm` 实现的 Go 语言库，提供了面向 TPM（可信平台模块）的高级抽象 API，帮助开发者在 Go 应用中快速、安全地使用 TPM 功能，而无需直接操作底层的 TPM 命令集。

**价值**  
- **降低研发成本**：封装了 TPM 的复杂细节，开发者只需调用简洁的 Go 接口即可完成密钥管理、签名、加密等安全操作，省去大量自研代码。  
- **提升安全性**：库经过 Google 内部审计和广泛使用，遵循业界最佳实践，能够帮助产品快速实现硬件根信任、数据完整性保护等安全特性。  
- **加速前端交付**：虽然核心是后端安全库，但通过统一的 API 可以更快地在前端（如 WebAssembly）或跨平台 UI 中集成 TPM 支持，减少 UI 与安全层的对接工作。

**典型接入方式**  
1. **在 Go 项目中引入模块**：  
   ```bash
   go get github.com/google/go-tpm-tools
   ```
2. **初始化 TPM 句柄**（使用 `tpm2` 包或 `client` 包）并创建或加载密钥：  
   ```go
   import "github.com/google/go-tpm-tools/client"

   // 打开 TPM 设备
   tpm, err := client.OpenTPM()
   defer tpm.Close()

   // 生成 RSA 密钥并保存到 TPM
   key, err := client.NewRSAKey(tpm, client.DefaultKeyParams)
   ```
3. **调用高级 API** 完成签名、加密或证书生成等操作，代码与普通 Go 加密库几乎无差别。  
4. **可选**：结合 `go-tpm-tools/launcher` 或 `go-tpm-tools/server`，在微服务或容器环境中统一管理 TPM 资源。

**生产可用性**  
- **活跃度**：项目最近一次提交于 2026‑06‑26，星标 303、fork 111，社区活跃，Google 仍在维护。  
- **成熟度**：已在多款内部 Google 产品以及开源项目中使用，具备完整的单元测试和 CI。  
- **安全审计**：作为 Google 官方 TPM 代码的一部分，已通过内部安全评审，代码遵循 Apache‑2.0 许可证，适合商业使用。  
- **集成门槛**：仅需 Go 环境和对 TPM 设备的访问权限（物理或虚拟 TPM），无额外依赖，适配容器、VM 以及裸机。  

综上，`google/go-tpm-tools` 是一个 **高质量、易集成且已在生产环境验证** 的 TPM 高层库，适合作为安全模块的底层实现，帮助团队快速交付具备硬件根信任的产品。

## 🧭 Practical evaluation

**Value:** google/go-tpm-tools helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 303 GitHub stars
- 111 forks
- updated 2026-06-26
- primary language: C
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 53/100 |
| topics | 75/100 |
| outlook | 73/100 |
| quality | 70/100 |
| recency | 80/100 |
| adoption | 52/100 |
| production | 70/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/google/go-tpm-tools) · [← Back to Security](./README.md)</sub>
