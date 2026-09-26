<div align="center">

**English** · [简体中文](./README.zh-CN.md)

</div>

# DeepSeek Harness — Unofficial Intel macOS x64 Builds

This repository hosts **unofficial, self-built Intel (x86_64) macOS binaries** of
[DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness).

> ### ⚠️ Not affiliated with DeepSeek
> These builds are compiled locally by an individual from the official open-source
> repository. They are **not** official DeepSeek-distributed binaries, and they are
> **not** official DeepSeek DMGs. Unsigned and not notarized by Apple.

---

## Why this repository exists

Upstream release artifacts are primarily aimed at Apple Silicon. Intel Mac users can
build the desktop app from source themselves — this repository simply publishes the
result so other Intel Mac users do not have to reproduce the toolchain.

## Downloads

Go to the [**Releases**](../../releases) page. Each release ships two equivalent
packages plus checksums:

| Package | What it is | Use case |
|---|---|---|
| `DeepSeek-Harness-<version>-mac-x64-unsigned.dmg` | macOS disk image, contains the app and an `Applications` shortcut | **Recommended.** Mount, drag the app into `Applications`, done. |
| `DeepSeek-Harness-<version>-mac-x64-unsigned.zip` | Plain ZIP archive containing the `.app` | Alternative if you prefer extracting manually. |
| `*.sha256` | SHA-256 checksums | Verify your download before running. |

## Installation

1. Download the `.dmg` (recommended) or the `.zip`.
2. **DMG:** double-click to mount, then drag **`DeepSeek Harness.app`** into your
   **`Applications`** folder, and eject the image.
   **ZIP:** extract it, then drag the `.app` into `Applications`.
3. Launch it from Launchpad or your Applications folder.

### First launch — allowing an unsigned app

Because these builds are **unsigned and not notarized**, macOS Gatekeeper blocks them
on first launch. You must allow the app manually:

**Option A — Finder (simplest)**

1. Right-click (or Control-click) `DeepSeek Harness.app` → **Open**.
2. In the warning dialog, click **Open** again. Afterwards it launches normally.

**Option B — System Settings**

1. Try to open the app once; macOS blocks it.
2. Go to **System Settings → Privacy & Security**.
3. Under **Security**, click **Open Anyway** next to the `DeepSeek Harness` message.

**Option C — Terminal**

```bash
xattr -dr com.apple.quarantine "/Applications/DeepSeek Harness.app"
```

> Only do this if you have verified the SHA-256 checksum and trust the source.

## Build characteristics

| | |
|---|---|
| Platform | macOS x64 / Intel (`darwin-x64`) |
| Build method | Official source, locally self-compiled |
| Signing | **Unsigned** — no Apple Developer signature |
| Notarization | **Not notarized** by Apple |
| Minimum macOS | `13.0` (Ventura or later) |
| Packaging | `.dmg` disk image and `.zip` archive — **no source code included** |

## Verifying a download

```bash
shasum -a 256 DeepSeek-Harness-*.dmg
shasum -a 256 DeepSeek-Harness-*.zip
```

Compare the output against the `.sha256` files published with the release.

## What is NOT included

No API keys, tokens, `.env` files, personal configuration, caches, or logs are ever
included in these packages. You provide your own credentials at runtime.

## Roadmap / contributing

This is a small distribution repository, not a fork of the upstream project.
For bugs in DeepSeek Harness itself, please report them upstream:
<https://github.com/deepseek-ai/deepseek-harness/issues>

## License

DeepSeek Harness is licensed under the **MIT License**, © 2026 DeepSeek.
Builds published here are redistributed under the same license; see [LICENSE](./LICENSE).

Upstream project: <https://github.com/deepseek-ai/deepseek-harness>

---

<div align="center">

**English** · [简体中文](./README.zh-CN.md)

</div>
