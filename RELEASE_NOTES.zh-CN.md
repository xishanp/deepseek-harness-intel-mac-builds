<div align="center">

[English](./RELEASE_NOTES.md) · **简体中文**

</div>

# DeepSeek Harness 0.1.7-rc.2 — Intel macOS x64(非官方构建)

> ### ⚠️ 请先阅读
> **这是第三方本地自编译的非官方 Intel macOS 构建。**
> **这不是 DeepSeek 官方发布的二进制文件。**
> 它**不是** DeepSeek 官方的 Intel DMG。**未签名**,且**未经 Apple 公证(notarized)**。
> macOS 首次打开时会拦截,需要你手动放行。详见 [安装步骤](#安装步骤)。

---

## ⬇️ 下载

### 🍎 推荐 —— DMG 磁盘映像

**[DeepSeek-Harness-0.1.7-rc.2-mac-x64-unsigned.dmg](https://github.com/xishanp/deepseek-harness-intel-mac-builds/releases/download/v0.1.7-rc.2-mac-x64-unsigned/DeepSeek-Harness-0.1.7-rc.2-mac-x64-unsigned.dmg)** — 441 MB

双击挂载,把应用拖进「应用程序」文件夹即可,无需其他操作。

**SHA-256**
```
08d6e1f7fcf007f1aac031ba31323fcccbf6829f96d49f80a11318333f94da24
```

### 📦 备选 —— ZIP 压缩包

**[DeepSeek-Harness-0.1.7-rc.2-mac-x64-unsigned.zip](https://github.com/xishanp/deepseek-harness-intel-mac-builds/releases/download/v0.1.7-rc.2-mac-x64-unsigned/DeepSeek-Harness-0.1.7-rc.2-mac-x64-unsigned.zip)** — 368 MB

手动解压后,把 `.app` 拖进「应用程序」文件夹。

**SHA-256**
```
c00b9297a0512320c84e7fde86d33c82ead1dea5bffe726eca373af702d3b5fd
```

---

## 安装步骤

1. 下载 **DMG**(推荐),并用上面的 SHA-256 校验文件完整性。
2. 双击 `.dmg` 文件完成挂载。
3. 把 **`DeepSeek Harness.app`** 拖进 **「应用程序」(Applications)** 文件夹。
4. 推出磁盘映像。
5. **首次打开:** 因为本构建未签名、未公证,macOS 会拦截。请按下方方法手动放行。
6. 从「启动台」或「应用程序」文件夹启动。

### 放行未签名应用的方法

**方法 A —— 访达(最简单)**

1. 右键(或 Control + 点击)`DeepSeek Harness.app` → 选择「**打开**」。
2. 在弹出的警告框中再次点击「**打开**」。之后即可正常启动。

**方法 B —— 系统设置**

1. 先尝试打开一次,系统会拦截。
2. 进入「**系统设置 → 隐私与安全性**」。
3. 在「**安全性**」区域,针对 `DeepSeek Harness` 的提示点击「**仍要打开**」。

**方法 C —— 终端**

```bash
xattr -dr com.apple.quarantine "/Applications/DeepSeek Harness.app"
```

> 仅在已用 SHA-256 校验过文件、并且信任来源的情况下才使用此命令。

### 校验完整性

```bash
shasum -a 256 DeepSeek-Harness-0.1.7-rc.2-mac-x64-unsigned.dmg
# 应当输出: 08d6e1f7fcf007f1aac031ba31323fcccbf6829f96d49f80a11318333f94da24
```

---

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
| 签名 | **未签名** —— 无 Apple Developer 签名 |
| 公证 | **未经 Apple 公证**(not notarized) |
| 许可证 | MIT(© 2026 DeepSeek) |

> **关于本地改动。** 本次构建使用的工作区相对 tag `dsh-v0.1.7-rc.2` 带有少量
> **本地构建脚本**改动(打包脚本与 `pnpm-workspace.yaml`)。**产品源码与业务逻辑未做任何修改。**

## 你下载到的是什么

**DMG:** 内含 `DeepSeek Harness.app` 应用本体,以及用于拖拽安装的 `Applications`
快捷方式。压缩后 441 MB,安装后约 1.0 GB。

**ZIP:** 仅内含 `DeepSeek Harness.app`。压缩后 368 MB,解压后约 1.0 GB。

两个安装包都**不包含源码仓库**。

---

## 重要声明

- **非官方。** 本二进制由个人编译发布,并非 DeepSeek 官方出品,未经 DeepSeek 审核或背书。
- **非官方 DMG。** 本磁盘映像由第三方自行制作,请不要把它当作 DeepSeek 官方的安装包。
- **未签名、未公证。** 没有 Apple Developer ID 签名,也没有 Apple 公证,Gatekeeper
  默认会拦截。
- **无担保。** 按 MIT 许可证「原样(AS IS)」提供,不附带任何形式的担保。
- **使用前请校验。** 下载后请比对 SHA-256 校验值。
- **不含任何凭据。** 本包不含 API Key、token、`.env` 文件、个人配置、缓存或日志;
  凭据由你在运行时自行提供。

## 许可证与署名

DeepSeek Harness 采用 **MIT 许可证**,© 2026 DeepSeek。本构建在同一许可证下再分发,
完整许可证文本见本仓库 [LICENSE](./LICENSE) 文件,再分发时必须一并附带。

源码:<https://github.com/deepseek-ai/deepseek-harness>

---

<div align="center">

[English](./RELEASE_NOTES.md) · **简体中文**

</div>
