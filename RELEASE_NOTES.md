# DeepSeek Harness 0.1.7-rc.2 — Intel macOS x64 (Unofficial Build)

## ⬇️ Download / 下载

### 🍎 推荐 · DMG 安装包(双击挂载 → 拖入「应用程序」)

**[DeepSeek-Harness-0.1.7-rc.2-mac-x64-unsigned.dmg](https://github.com/xishanp/deepseek-harness-intel-mac-builds/releases/download/v0.1.7-rc.2-mac-x64-unsigned/DeepSeek-Harness-0.1.7-rc.2-mac-x64-unsigned.dmg)**

DMG SHA-256: `08d6e1f7fcf007f1aac031ba31323fcccbf6829f96d49f80a11318333f94da24`

### 📦 备选 · ZIP 压缩包(手动解压)

**[DeepSeek-Harness-0.1.7-rc.2-mac-x64-unsigned.zip](https://github.com/xishanp/deepseek-harness-intel-mac-builds/releases/download/v0.1.7-rc.2-mac-x64-unsigned/DeepSeek-Harness-0.1.7-rc.2-mac-x64-unsigned.zip)** — 368 MB

ZIP SHA-256: `c00b9297a0512320c84e7fde86d33c82ead1dea5bffe726eca373af702d3b5fd`

---

> ## ⚠️ English
> **This is an unofficial self-built Intel macOS build.**
> **This is not an official DeepSeek-distributed binary.**
> It is **not** an official DeepSeek Intel DMG. Unsigned and **not notarized** by Apple.

> ## ⚠️ 中文
> **这是第三方本地自编译的非官方 Intel macOS 构建。**
> **这不是 DeepSeek 官方发布的二进制文件。**
> 它**不是** DeepSeek 官方的 Intel DMG。**未签名、未经 Apple 公证(notarized)**。

---

# 中文

这是由第三方使用 DeepSeek 官方开源仓库源码**本地自编译**的 Intel (x86_64) macOS
构建版本。发布目的是方便 Intel 芯片的 Mac 用户使用。它**不是** DeepSeek 官方发布的
版本,也**不是** DeepSeek 官方的 DMG 安装包。

## 下载与安装(推荐用 DMG)

1. 点击上面 **DMG 安装包** 的链接下载。
2. 双击 `.dmg` 文件,系统会挂载出一个磁盘映像。
3. 在弹出的窗口里,把 **`DeepSeek Harness.app`** 拖进 **`Applications`(应用程序)** 文件夹。
4. 卸载磁盘映像(在访达侧边栏点推出按钮)。
5. 首次打开:因为本版本**未签名、未公证**,macOS 会拦截。见下方「放行方法」。
6. 打开「启动台」或「应用程序」文件夹,双击 `DeepSeek Harness` 即可。

### macOS 放行未签名应用的方法

**方法 A — 访达(最简单)**
1. 右键(或 Control + 点击)`DeepSeek Harness.app` → 选择「**打开**」。
2. 在弹出的警告框中再次点「**打开**」。之后即可正常启动。

**方法 B — 系统设置**
1. 先尝试打开一次,系统会拦截。
2. 进入「**系统设置 → 隐私与安全性**」。
3. 在「**安全性**」区域,针对 `DeepSeek Harness` 的提示点击「**仍要打开**」。

**方法 C — 终端**
```bash
xattr -dr com.apple.quarantine "/Applications/DeepSeek Harness.app"
```
> 仅在已用 SHA-256 校验过文件、且信任来源时才使用此命令。

## 构建来源

| 项目 | 值 |
|---|---|
| 上游源码 | [deepseek-ai/deepseek-harness](https://github.com/deepseek-ai/deepseek-harness)(官方仓库) |
| 版本 | `0.1.7-rc.2` |
| 源码 tag | `dsh-v0.1.7-rc.2` |
| 源码 commit | `477b4f420553e8a52c2fbccc464d7561b239c443` |
| commit 标题 | `Merge pull request #5180 from deepseek-harness/rel/dsh-0.1.7-rc.2` |
| 构建方式 | 官方源码,**本地自编译**(非官方 CI 产物) |
| 平台 | macOS x64 / Intel / `darwin-x64` |
| Electron | `44.0.0` |
| 最低系统 | `macOS 13.0`(Ventura 及以上) |
| Bundle ID | `com.deepseek.harness` |
| 签名 | **未签名**,无 Apple Developer 签名 |
| 公证 | **未经 Apple 公证**(not notarized) |
| 许可证 | MIT(© 2026 DeepSeek) |

> **关于本地改动**:本次构建使用的工作区相对 tag `dsh-v0.1.7-rc.2` 带有少量
> **本地构建脚本改动**(打包脚本与 `pnpm-workspace.yaml`)。**产品源码与业务逻辑未做任何修改。**

## 安装包内容

**DMG 内包含**:`DeepSeek Harness.app` 应用本体 + `Applications` 快捷方式(拖拽安装用)。
**不包含源码仓库。**

**ZIP 内包含**:仅 `DeepSeek Harness.app`。解压后约 1.0 GB。

## 重要声明

- **非官方**:本二进制由个人编译发布,并非 DeepSeek 官方,未经 DeepSeek 审核或背书。
- **非官方 DMG**:本 DMG 由第三方自行制作,不是 DeepSeek 官方发布的 DMG。
- **未签名、未公证**:macOS Gatekeeper 默认会拦截,需要你手动放行。
- **无担保**:按 MIT 许可证「原样」提供,不附带任何形式的担保。
- **使用前请校验**:下载后请比对 SHA-256 校验值。
- **不含任何凭据**:本包不含 API Key、token、`.env`、个人配置、缓存或日志,凭据由你在运行时自行提供。

---

# English

A locally compiled, **unsigned** Intel (x86_64) macOS build of DeepSeek Harness,
produced from the official open-source repository by a third party. It is published
here for the convenience of Intel Mac users. It is **not** an official DeepSeek
release, and it is **not** an official DeepSeek-distributed DMG.

## Download and install (DMG recommended)

1. Download the **DMG** linked above.
2. Double-click the `.dmg` to mount it.
3. Drag **`DeepSeek Harness.app`** into your **`Applications`** folder.
4. Eject the disk image.
5. **First launch:** because this build is unsigned and not notarized, macOS blocks
   it. See "Allowing an unsigned app" below.
6. Open `DeepSeek Harness` from Launchpad or your Applications folder.

### Allowing an unsigned app in macOS

**Option A — Finder (simplest)**
1. Right-click (or Control-click) `DeepSeek Harness.app` → **Open**.
2. In the warning dialog, click **Open** again.

**Option B — System Settings**
1. Try to open the app once; macOS blocks it.
2. Go to **System Settings → Privacy & Security**.
3. Under **Security**, click **Open Anyway** next to the `DeepSeek Harness` message.

**Option C — Terminal**
```bash
xattr -dr com.apple.quarantine "/Applications/DeepSeek Harness.app"
```

## Build provenance

| Field | Value |
|---|---|
| Upstream source | [deepseek-ai/deepseek-harness](https://github.com/deepseek-ai/deepseek-harness) (official repository) |
| Version | `0.1.7-rc.2` |
| Source tag | `dsh-v0.1.7-rc.2` |
| Source commit | `477b4f420553e8a52c2fbccc464d7561b239c443` |
| Build type | Official source, **locally self-compiled** |
| Platform | macOS x64 / Intel / `darwin-x64` |
| Electron | `44.0.0` |
| Minimum macOS | `13.0` (Ventura or later) |
| Bundle identifier | `com.deepseek.harness` |
| Signing | **Unsigned** — no Apple Developer signature |
| Notarization | **Not notarized** by Apple |
| License | MIT (© 2026 DeepSeek) |

> **Note on local patches:** the working tree used for this build carries minor local
> build-script modifications (packaging scripts and `pnpm-workspace.yaml`) relative to
> tag `dsh-v0.1.7-rc.2`. No application logic or product source was altered.

## Package contents

**DMG:** the `DeepSeek Harness.app` bundle plus an `Applications` shortcut for
drag-and-drop installation. **No source code included.**

**ZIP:** the `DeepSeek Harness.app` bundle only (~1.0 GB extracted).

## Important disclaimers

- **Unofficial.** Compiled and published by an individual, not by DeepSeek.
  Not endorsed, reviewed, or distributed by DeepSeek.
- **Not an official DMG.** This disk image was produced by a third party, not DeepSeek.
- **Unsigned and not notarized.** Gatekeeper blocks it by default.
- **No warranty.** "AS IS", under the MIT License.
- **Verify before running.** Compare the SHA-256 checksum.
- **No credentials included.** No API keys, tokens, `.env` files, personal
  configuration, caches, or logs. You supply your own credentials at runtime.

---

## License and attribution / 许可证与署名

DeepSeek Harness is licensed under the **MIT License**, © 2026 DeepSeek.
This build is redistributed under the same license. The full license text is in the
[LICENSE](LICENSE) file of this repository and must accompany any redistribution.

DeepSeek Harness 采用 **MIT 许可证**,© 2026 DeepSeek。本构建在同一许可证下再分发,
完整许可证文本见本仓库 [LICENSE](LICENSE) 文件,再分发时必须一并附带。

Source / 源码:<https://github.com/deepseek-ai/deepseek-harness>
