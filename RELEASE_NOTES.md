# DeepSeek Harness 0.1.7-rc.2 — Intel macOS x64 (Unofficial Build)

> **This is an unofficial self-built Intel macOS build.**
> **This is not an official DeepSeek-distributed binary.**

A locally compiled, **unsigned** Intel (x86_64) macOS build of DeepSeek Harness,
produced from the official open-source repository by a third party. It is published
here for the convenience of Intel Mac users. It is **not** an official DeepSeek
release, and it is **not** an official DeepSeek Distribute DMG.

---

## Build provenance

| Field | Value |
|---|---|
| Upstream source | [deepseek-ai/deepseek-harness](https://github.com/deepseek-ai/deepseek-harness) (official repository) |
| Version | `0.1.7-rc.2` |
| Source tag | `dsh-v0.1.7-rc.2` |
| Source commit | `477b4f420553e8a52c2fbccc464d7561b239c443` |
| Commit subject | `Merge pull request #5180 from deepseek-harness/rel/dsh-0.1.7-rc.2` |
| Build type | Official source, **locally self-compiled** (not a CI/official artifact) |
| Platform | macOS x64 / Intel / `darwin-x64` |
| Electron | `44.0.0` |
| Minimum macOS | `13.0` (Ventura or later) |
| Bundle identifier | `com.deepseek.harness` |
| Signing | **Unsigned** — no Apple Developer signature |
| Notarization | **Not notarized** by Apple |
| License | MIT (© 2026 DeepSeek) |

> **Note on local patches:** the working tree used for this build carries
> minor local build-script modifications (build/packaging scripts and
> `pnpm-workspace.yaml`) relative to tag `dsh-v0.1.7-rc.2`. No application
> logic or product source was altered. See the repository README for details.

---

## What you are downloading

```
DeepSeek-Harness-0.1.7-rc.2-mac-x64-unsigned.zip
```

- Contains a single `DeepSeek Harness.app` bundle. The source repository is
  **not** included.
- Preserves the bundle structure, symlinks and permissions required by macOS.
- Uncompressed size: ~1.0 GB.

### SHA-256

```
c00b9297a0512320c84e7fde86d33c82ead1dea5bffe726eca373af702d3b5fd
```

Verify with:

```bash
shasum -a 256 DeepSeek-Harness-0.1.7-rc.2-mac-x64-unsigned.zip
```

---

## Installation

1. Download the `.zip` and verify the SHA-256 checksum above.
2. Extract it (double-click, or `ditto -x -k <file>.zip .`).
3. Drag `DeepSeek Harness.app` into `/Applications`.
4. **Because this build is unsigned and not notarized, macOS will warn you
   the first time you open it.** You must allow it manually — see below.

### Allowing an unsigned app in macOS

**Option A — Finder (simplest)**

1. Right-click (or Control-click) `DeepSeek Harness.app` → **Open**.
2. In the warning dialog, click **Open**.
3. Confirm again if prompted. After this, it opens normally.

**Option B — System Settings**

1. Try to open the app once; macOS blocks it.
2. Go to **System Settings → Privacy & Security**.
3. Scroll to the **Security** section and click **Open Anyway** next to the
   message about `DeepSeek Harness`.
4. Authenticate and confirm.

**Option C — Terminal (removes the quarantine flag)**

```bash
xattr -dr com.apple.quarantine "/Applications/DeepSeek Harness.app"
```

> Only do this if you have verified the SHA-256 checksum and trust the source.
> This command tells macOS to stop treating the download as unverified.

---

## Important disclaimers

- **Unofficial.** This binary was compiled and published by an individual, not
  by DeepSeek. It is not endorsed, reviewed, or distributed by DeepSeek.
- **Not an official DMG.** Do not treat this artifact as an official
  DeepSeek-published Intel DMG or installer.
- **Unsigned and not notarized.** No Apple Developer ID signature and no Apple
  notarization are present. macOS Gatekeeper will block it by default and you
  must explicitly allow it as described above.
- **No warranty.** Provided "AS IS", without warranty of any kind, under the
  terms of the MIT License.
- **Verify before running.** Compare the SHA-256 checksum after downloading.
- **No credentials included.** This package contains no API keys, tokens,
  `.env` files, personal configuration, caches, or logs. You supply your own
  credentials at runtime.

---

## 中文说明

- 这是**第三方本地自编译的非官方 Intel macOS 构建**,来自 DeepSeek 官方开源仓库源码,
  **不是 DeepSeek 官方发布的二进制或官方 Intel DMG**。
- 平台:**macOS x64 / Intel**,最低系统 **macOS 13.0**;Electron `44.0.0`。
- **未签名、未公证(notarized)**,macOS 首次打开会拦截,需要手动放行:
  右键点选 App →「打开」→ 在弹窗中再次点「打开」;
  或到「系统设置 → 隐私与安全性 → 安全性」点「仍要打开」。
  也可在终端执行:
  ```bash
  xattr -dr com.apple.quarantine "/Applications/DeepSeek Harness.app"
  ```
- 下载后请先用 SHA-256 校验文件完整性。
- 本包**不含**任何 API Key、token、`.env`、个人配置、缓存或日志。

---

## License and attribution

DeepSeek Harness is licensed under the **MIT License**, © 2026 DeepSeek.
This build is redistributed under the same license. The full license text is
included in the [LICENSE](LICENSE) file of this repository and must accompany
any redistribution of this binary.

Source: <https://github.com/deepseek-ai/deepseek-harness>
