# hope1026/weppy-roblox-mcp

[![Stars](https://img.shields.io/github/stars/hope1026/weppy-roblox-mcp?style=flat-square&color=yellow)](https://github.com/hope1026/weppy-roblox-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/hope1026/weppy-roblox-mcp?style=flat-square&color=blue)](https://github.com/hope1026/weppy-roblox-mcp/network) [![Language](https://img.shields.io/badge/lang-PowerShell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> Roblox Studio MCP server & plugin for Claude Code, Cursor, Codex, and Gemini. AI-powered scripts, terrain, assets, lighting, and bidirectional project sync.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 21 |
| 🍴 **Forks** | 3 |
| 💻 **Language** | PowerShell |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-agents` `antigravity` `claude` `claude-code` `codex` `cursor` `game-development` `gemini` `luau` `mcp` `mcp-server`

## 🎯 Categories

MCP · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary**  
hope1026/weppy‑roblox‑mcp is an open‑source Model Context Protocol (MCP) server and Roblox‑Studio plugin that lets AI assistants such as Claude, Cursor, Codex, and Gemini read and write Roblox project data—including scripts, terrain, assets, and lighting—in real time. It also provides bidirectional sync between a local Roblox project and the MCP server, enabling AI‑driven generation and iteration of game content.

**Value**  
- **Standardised AI‑to‑tool bridge** – By implementing the MCP, the project gives AI agents a common, language‑agnostic interface to manipulate Roblox Studio resources, turning abstract code suggestions into concrete, testable game objects.  
- **End‑to‑end workflow** – Developers can prompt an LLM to create or modify scripts, generate terrain, or adjust lighting, and the changes are instantly reflected in the running Roblox project, dramatically shortening the prototyping loop.  
- **Extensible ecosystem** – Because MCP is a protocol, the same server can be reused for other AI platforms or custom agents, making it a reusable backend for any tool that needs programmatic access to Roblox assets.

**Practical Adoption Path**  
1. **Spin up the MCP server** – Clone the repo, run the PowerShell installer (or Docker image if preferred), and expose the server endpoint on a local or cloud host.  
2. **Install the Roblox‑Studio plugin** – Add the plugin from the repo’s releases, point it at the server URL, and authenticate if required.  
3. **Connect an AI assistant** – Use the provided SDK/CLI to register an LLM (Claude, Cursor, Codex, Gemini) with the server. The assistant can now issue MCP calls such as `createScript`, `updateTerrain`, or `syncProject`.  
4. **Iterate** – Write prompts to the LLM, let it generate or modify assets, and watch the changes appear instantly in Studio. For CI/CD pipelines, the same MCP calls can be scripted to apply batch updates or run automated tests.  

**Production‑Readiness**  
- **Activity & Adoption** – The repository shows recent commits (last updated 2026‑05‑14), 21 stars, 3 forks, and active issue discussion, indicating a healthy community.  
- **Technical maturity** – Exposes a clean API/SDK, includes CLI tooling, and is written in PowerShell with clear language metadata, making integration straightforward for both Windows‑based Studio environments and cross‑platform CI runners.  
- **Risk profile** – No glaring licensing or security red flags have been identified, though a final audit of the MIT‑style license, dependency chain, and maintainer responsiveness is recommended before a production rollout.  

Overall, hope1026/weppy‑roblox‑mcp is a strong OSS candidate for teams that want to harness generative AI to build Roblox experiences faster, offering a well‑documented, actively maintained bridge between AI models and the Roblox toolchain.

### Русский

**Краткое резюме:**  
`hope1026/weppy-roblox-mcp` — это открытый сервер MCP и плагин для Roblox Studio, позволяющий AI‑ассистентам (Claude, Cursor, Codex, Gemini) генерировать скрипты, ландшафт, ассеты и освещение, а также синхронизировать проект в обе стороны через стандартный Model Context Protocol. Типичный сценарий — подключить AI‑агента к реальному набору инструментов Roblox, развернуть MCP‑сервер и начать автоматизированную разработку и обновление контента без ручного вмешательства. Проект уже активно поддерживается (обновления до 2026‑05‑14, 21 звезда, 3 форка), имеет готовый API/SDK/CLI и считается готовым к пилотному запуску в production, хотя лицензия и вопросы безопасности требуют окончательной проверки.

### 中文

**项目简介**  
hope1026/weppy-roblox-mcp 是一个在 Roblox Studio 中运行的 MCP（Model Context Protocol）服务器与插件，能够把 Claude、Cursor、Codex、Gemini 等 AI 助手无缝接入 Roblox 开发环境，实现脚本、地形、资源、灯光等内容的 AI 生成并支持双向项目同步。

**价值**  
- **统一协议**：通过标准化的 MCP 接口，让各种 AI 助手直接调用 Roblox 的真实工具链和数据，降低集成成本。  
- **全栈 AI 创作**：AI 可生成并实时部署代码、资产、场景配置，极大提升原型迭代速度。  
- **双向同步**：本地 Roblox 项目与 AI 端保持实时一致，避免版本冲突，适合团队协作和持续集成。

**典型接入方式**  
1. **部署 MCP 服务器**：在本地或云端运行 PowerShell 脚本启动 `weppy-roblox-mcp`，它会监听指定端口并提供 REST/WS 接口。  
2. **安装插件**：在 Roblox Studio 中通过插件市场或手动导入 `.rbxm`，插件会自动连接到上述服务器。  
3. **配置 AI 助手**：在 Claude、Cursor、Codex、Gemini 等平台的插件或 SDK 中填写服务器地址、认证 token，即可让 AI 调用 `generateScript、createTerrain、importAsset` 等 RPC。  
4. **调用示例**（伪代码）  
   ```python
   client = MCPClient(url="http://localhost:8080", token="YOUR_TOKEN")
   script = client.generate_script(prompt="创建一个可以收集金币的角色")
   client.apply_script(script, target="StarterPlayerScripts")
   ```

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑05‑14，拥有 21 Stars、3 Forks，社区话题覆盖 19 项，表明项目仍在维护。  
- **技术成熟度**：提供完整的 API/SDK/CLI，语言元数据清晰，易于在 CI/CD 流程中集成。  
- **风险评估**：暂无重大元数据风险，但仍需对许可证（MIT/Apache 等）和安全审计（如依赖的 PowerShell 脚本）进行最终确认。  
- **结论**：在经过一次安全与合规审查后，可视为 **高可用** 的 OSS 组件，适合在内部或受控的生产环境中进行试点部署。

## 🧭 Practical evaluation

**Value:** hope1026/weppy-roblox-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 21 GitHub stars
- 3 forks
- updated 2026-05-14
- primary language: PowerShell
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 15/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 66/100 |
| recency | 100/100 |
| adoption | 25/100 |
| production | 76/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/hope1026/weppy-roblox-mcp) · [← Back to Mcp](./README.md)</sub>
