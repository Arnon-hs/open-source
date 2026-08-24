# openresty/stream-lua-nginx-module

[![Stars](https://img.shields.io/github/stars/openresty/stream-lua-nginx-module?style=flat-square&color=yellow)](https://github.com/openresty/stream-lua-nginx-module/stargazers) [![Forks](https://img.shields.io/github/forks/openresty/stream-lua-nginx-module?style=flat-square&color=blue)](https://github.com/openresty/stream-lua-nginx-module/network) [![Language](https://img.shields.io/badge/lang-C-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-42%2F100-brightgreen?style=flat-square)](#)

> Embed the power of Lua into NGINX TCP/UDP servers

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 747 |
| 🍴 **Forks** | 207 |
| 💻 **Language** | C |
| 📈 **Score** | 42/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The **openresty/stream‑lua‑nginx‑module** lets you embed Lua scripts directly into NGINX’s TCP/UDP stream layer, enabling dynamic request handling, custom routing, and on‑the‑fly protocol transformations without writing C modules. With over 700 stars and active maintenance, it’s a mature way for teams to reuse a common Lua‑powered NGINX backbone instead of rebuilding similar TCP/UDP logic for each service.

**Value**  
- **Reuse of infrastructure** – A single Lua‑enabled NGINX instance can serve as a programmable gateway for many services, eliminating duplicated proxy or load‑balancing code.  
- **Speed to market** – Teams can ship new API services by writing short Lua scripts rather than compiling native NGINX modules, accelerating prototyping and iteration.  
- **Standardization** – Centralizing traffic handling in Lua promotes consistent security, logging, and metrics across all TCP/UDP services.

**Practical Adoption Path**  
1. **Prototype** – Spin up a test NGINX container with the `stream_lua_module` compiled (official Docker images already include it). Write a small Lua script that implements the desired routing or transformation and verify behavior against a staging backend.  
2. **Code Review & Security Audit** – Because the integration points are not fully described in the metadata, manually inspect the module’s configuration (`stream { lua ... }`) and the Lua code for resource‑consumption limits, sandboxing, and error handling.  
3. **CI/CD Integration** – Add the module to your infrastructure‑as‑code (e.g., Terraform or Ansible) and include unit tests for the Lua scripts (using `busted` or `luatest`).  
4. **Gradual Rollout** – Deploy the Lua‑enabled NGINX as a sidecar or upstream proxy for a subset of services, monitor latency and error rates, then expand coverage.

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last commit 2026‑05‑14) and widely used (747 ★, 207 forks), but the integration path isn’t fully documented, so extra validation is required.  
- **Best for:** Prototypes, internal tools, or services where the flexibility of Lua outweighs the overhead of a custom C module.  
- **Considerations before production:** Verify dependency compatibility with your NGINX version, establish monitoring for Lua script errors, and set resource limits (e.g., `lua_shared_dict`, worker‑process quotas) to avoid runtime instability. Once these checks are in place, the module can be promoted to production for stable, high‑throughput TCP/UDP workloads.

### Русский

**openresty/stream-lua-nginx-module** — это модуль, позволяющий внедрять скрипты Lua непосредственно в TCP/UDP‑серверы NGINX, что ускоряет создание API‑сервисов и упрощает повторное использование общей инфраструктуры бэкенда. Он подходит для прототипов и внутренних workflow, но перед выводом в продакшн требуется ручная проверка интеграции и оценка затрат на настройку, поскольку метаданные дают ограниченную информацию о процессе внедрения. При надлежащей проверке модуль считается средне‑готовым к продакшн‑использованию.

### 中文

**简短介绍**  
openresty/stream‑lua‑nginx‑module 为 NGINX 的 TCP/UDP 流服务嵌入 Lua 脚本引擎，使得开发者可以在高性能的 NGINX 代理层直接编写业务逻辑、协议解析和流控代码，从而快速复用已有的服务基础设施。

**价值**  
- **复用基础设施**：通过 Lua 脚本即可在 NGINX 上实现自定义协议、鉴权、限流等功能，避免在每个微服务中重复实现这些通用模块。  
- **加速交付**：在原有 NGINX 配置上添加少量 Lua 代码即可上线 API/网关功能，显著缩短开发和部署周期。  
- **统一标准**：团队可以把常用的后端模式（如日志、监控、熔断）封装为 Lua 库，在所有 TCP/UDP 服务中统一使用，提升代码一致性和可维护性。

**典型接入方式**  
1. **编译或使用预编译的 NGINX**：在编译 NGINX 时加入 `--add-module=path/to/stream-lua-nginx-module`，或直接使用 OpenResty 提供的已集成该模块的二进制包。  
2. **在 `nginx.conf` 中启用**：在 `stream {}` 块里使用 `lua_code_cache on;`、`lua_socket_log_errors off;` 等指令，并通过 `content_by_lua_block`、`preread_by_lua_block` 或 `log_by_lua_block` 编写业务脚本。  
3. **依赖管理**：将 Lua 脚本及第三方库（如 lua-resty‑core、lua‑cjson）放在 NGINX 可访问的路径下，使用 `lua_package_path`/`lua_package_cpath` 配置搜索路径。  
4. **CI/CD 验证**：在部署流水线中加入 NGINX 配置语法检查 (`nginx -t`) 与 Lua 单元测试，确保改动不会破坏现有流量。

**生产可用性**  
- **成熟度**：项目已有 747+ Stars、207+ Forks，且近期（2026‑05‑14）仍在活跃维护，代码质量较为可靠。  
- **适用场景**：适合内部原型、边缘网关或对性能要求高的 TCP/UDP 服务；在生产环境使用前需完成依赖审计、性能基准测试以及故障恢复演练。  
- **风险与注意事项**：元数据中集成指引较少，实际接入时可能需要手动排查兼容性（如 NGINX 版本、LuaJIT 与系统库的匹配）。建议先在预发布环境验证脚本的内存/CPU 开销，并制定监控和回滚方案后再推向正式业务。

## 🧭 Practical evaluation

**Value:** openresty/stream-lua-nginx-module helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 747 GitHub stars
- 207 forks
- updated 2026-05-14
- primary language: C

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 58/100 |
| stars | 61/100 |
| topics | 0/100 |
| outlook | 40/100 |
| quality | 47/100 |
| recency | 20/100 |
| adoption | 60/100 |
| production | 43/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/openresty/stream-lua-nginx-module) · [← Back to Misc](./README.md)</sub>
