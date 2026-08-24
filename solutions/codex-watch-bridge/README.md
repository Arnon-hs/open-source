# Codex Watch Bridge

[![Repository](https://img.shields.io/badge/repository-kirbudilov01%2Fcodex--watch--bridge-181717?logo=github)](https://github.com/kirbudilov01/codex-watch-bridge) [![License](https://img.shields.io/badge/license-MIT-22C55E)](https://github.com/kirbudilov01/codex-watch-bridge/blob/main/LICENSE) [![Community](https://img.shields.io/badge/AtlasRepo-community%20partner-2A4BFF)](https://atlasrepo.com/)

> An Apple Watch client and Mac bridge for opening projects, reading chats, dictating prompts, running real Codex tasks, and following their status from your wrist.

**Community partner:** [@kirbudilov01](https://github.com/kirbudilov01)

![Codex Watch Bridge UI](https://raw.githubusercontent.com/kirbudilov01/codex-watch-bridge/main/docs/watch-ui-mock.png)

## The problem

Long Codex tasks often need a quick status check or a short follow-up while the developer is away from the keyboard. Opening a laptop just to see whether an agent is running, waiting for input, finished, or failed adds friction.

## The solution

`kirbudilov01/codex-watch-bridge` provides a focused watchOS client backed by a Node.js service on the user's Mac:

```text
Apple Watch
  → Bridge API over LAN or HTTPS
    → Mac bridge
      → Codex Desktop app-server
      → Codex CLI fallback
      → local session fallback
```

The watch can list projects and chats, read messages, create a thread, dictate and send a prompt, display normalized task states, and show remaining account limits. Codex credentials stay on the Mac rather than on the watch.

## Quick start

Requirements currently listed by the project are macOS with Xcode, Apple Watch with watchOS 10 or later, and Node.js 20 or later.

```bash
git clone https://github.com/kirbudilov01/codex-watch-bridge.git
cd codex-watch-bridge
npm run check
npm run doctor
npm run dev
```

Open `CodexAppleWatch.xcodeproj` in Xcode, configure the Apple Developer Team and bridge URL, then run the watch target on a paired device.

## Why it is useful

- uses real Codex projects, threads, messages, and task states instead of a separate mock chat;
- supports native watchOS dictation for quick follow-up prompts;
- keeps Codex and OpenAI secrets on the Mac;
- works over the local network and documents a remote HTTPS tunnel setup;
- includes backend tests, doctor checks, launchd service scripts, and operations notes;
- is published under the MIT License.

## Boundaries and adoption checks

- The upstream README labels the current release a **working prototype**. Verify the current checks and device flow before relying on it for production operations.
- The Mac and bridge service must remain reachable while the watch is in use.
- Codex Desktop internals and fallback formats may change. Re-run `npm run check` and `npm run doctor` after Codex updates.
- For remote access, use HTTPS and a random bearer token. Do not expose a broad unauthenticated bridge port to the internet.
- Never place OpenAI keys, Codex secrets, cookies, session files, or a real bridge token in committed watch configuration.
- A physical-device build requires the user's own Apple Developer signing setup.

## Project links

- [Repository and complete documentation](https://github.com/kirbudilov01/codex-watch-bridge#readme)
- [Project page](https://kirbudilov01.github.io/codex-watch-bridge-page/)
- [Operations guide](https://github.com/kirbudilov01/codex-watch-bridge/blob/main/docs/OPERATIONS.md)
- [Security policy](https://github.com/kirbudilov01/codex-watch-bridge/blob/main/SECURITY.md)
- [AtlasRepo website](https://atlasrepo.com/)
- [AtlasRepo forum](https://forum.atlasrepo.com/)

## Русский

Codex Watch Bridge — это watchOS-клиент и Node.js bridge на Mac для просмотра проектов и чатов, диктовки промптов и контроля статуса реальных задач Codex с Apple Watch. Секреты остаются на Mac. Для удалённого доступа нужны HTTPS и bearer token; текущую версию следует считать рабочим прототипом.

## 简体中文

Codex Watch Bridge 由 watchOS 客户端和 Mac 上的 Node.js 桥接服务组成，可以在 Apple Watch 上查看项目与对话、口述并发送提示词，以及跟踪真实 Codex 任务的状态。密钥与会话数据保留在 Mac 上。远程访问应使用 HTTPS 和 bearer token；当前版本应视为可运行原型。

---

[← All AtlasRepo community solutions](../) · [Open the repository →](https://github.com/kirbudilov01/codex-watch-bridge)
