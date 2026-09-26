<div align="center">

**English** · [简体中文](./RELEASE_NOTES.zh-CN.md)

</div>

# DeepSeek Harness 0.1.7-rc.2 — Intel macOS x64 (Unofficial Build)

> ### ⚠️ Read this first
> **This is an unofficial self-built Intel macOS build.**
> **This is not an official DeepSeek-distributed binary.**
> It is **not** an official DeepSeek Intel DMG. It is **unsigned** and
> **not notarized by Apple**. macOS will block it on first launch — you must
> allow the app manually. See [Installation](#installation).

---

## ⬇️ Download

### 🍎 Recommended — DMG disk image

**[DeepSeek-Harness-0.1.7-rc.2-mac-x64-unsigned.dmg](https://github.com/xishanp/deepseek-harness-intel-mac-builds/releases/download/v0.1.7-rc.2-mac-x64-unsigned/DeepSeek-Harness-0.1.7-rc.2-mac-x64-unsigned.dmg)** — 441 MB

Double-click to mount, drag the app into `Applications`. Nothing else to do.

**SHA-256**
```
08d6e1f7fcf007f1aac031ba31323fcccbf6829f96d49f80a11318333f94da24
```

### 📦 Alternative — ZIP archive

**[DeepSeek-Harness-0.1.7-rc.2-mac-x64-unsigned.zip](https://github.com/xishanp/deepseek-harness-intel-mac-builds/releases/download/v0.1.7-rc.2-mac-x64-unsigned/DeepSeek-Harness-0.1.7-rc.2-mac-x64-unsigned.zip)** — 368 MB

Extract manually, then drag the `.app` into `Applications`.

**SHA-256**
```
c00b9297a0512320c84e7fde86d33c82ead1dea5bffe726eca373af702d3b5fd
```

---

## Installation

1. Download the **DMG** (recommended) and verify the SHA-256 checksum above.
2. Double-click the `.dmg` to mount it.
3. Drag **`DeepSeek Harness.app`** into your **`Applications`** folder.
4. Eject the disk image.
5. **First launch:** macOS blocks the app because it is unsigned and not notarized.
   Allow it manually — see below.
6. Launch it from Launchpad or your Applications folder.

### Allowing an unsigned app in macOS

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

### Verifying the checksum

```bash
shasum -a 256 DeepSeek-Harness-0.1.7-rc.2-mac-x64-unsigned.dmg
# expect: 08d6e1f7fcf007f1aac031ba31323fcccbf6829f96d49f80a11318333f94da24
```

---

## Build provenance

| Field | Value |
|---|---|
| Upstream source | [deepseek-ai/deepseek-harness](https://github.com/deepseek-ai/deepseek-harness) (official repository) |
| Version | `0.1.7-rc.2` |
| Source tag | `dsh-v0.1.7-rc.2` |
| Source commit | `477b4f420553e8a52c2fbccc464d7561b239c443` |
| Commit subject | `Merge pull request #5180 from deepseek-harness/rel/dsh-0.1.7-rc.2` |
| Build type | Official source, **locally self-compiled** (not a CI / official artifact) |
| Platform | macOS x64 / Intel / `darwin-x64` |
| Electron | `44.0.0` |
| Minimum macOS | `13.0` (Ventura or later) |
| Bundle identifier | `com.deepseek.harness` |
| Signing | **Unsigned** — no Apple Developer signature |
| Notarization | **Not notarized** by Apple |
| License | MIT (© 2026 DeepSeek) |

> **Note on local patches.** The working tree used for this build carries minor local
> **build-script** modifications (packaging scripts and `pnpm-workspace.yaml`) relative
> to tag `dsh-v0.1.7-rc.2`. No application logic or product source was altered.

## What you are downloading

**DMG:** the `DeepSeek Harness.app` bundle plus an `Applications` shortcut for
drag-and-drop installation. Compressed to 441 MB; ~1.0 GB when installed.

**ZIP:** the `DeepSeek Harness.app` bundle only. 368 MB compressed; ~1.0 GB extracted.

Neither package contains the source repository.

---

## Important disclaimers

- **Unofficial.** This binary was compiled and published by an individual, not by
  DeepSeek. It is not endorsed, reviewed, or distributed by DeepSeek.
- **Not an official DMG.** This disk image was produced by a third party. Do not
  treat it as an official DeepSeek installer.
- **Unsigned and not notarized.** There is no Apple Developer ID signature and no
  Apple notarization. Gatekeeper blocks it by default.
- **No warranty.** Provided "AS IS", without warranty of any kind, under the MIT License.
- **Verify before running.** Compare the SHA-256 checksum after downloading.
- **No credentials included.** This package contains no API keys, tokens, `.env`
  files, personal configuration, caches, or logs. You supply your own credentials
  at runtime.

## License and attribution

DeepSeek Harness is licensed under the **MIT License**, © 2026 DeepSeek.
This build is redistributed under the same license. The full license text is in the
[LICENSE](./LICENSE) file of this repository and must accompany any redistribution.

Source: <https://github.com/deepseek-ai/deepseek-harness>

---

<div align="center">

**English** · [简体中文](./RELEASE_NOTES.zh-CN.md)

</div>
