<div align="center">

[English](./README.md) · **简体中文**

</div>

# DeepSeek Harness — 非官方 Intel macOS x64 构建

本仓库提供 [DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness)
的**非官方、本地自编译的 Intel(x86_64)macOS 二进制版本**。

> ### ⚠️ 与 DeepSeek 官方无关
> 本仓库的构建由个人使用官方开源仓库源码**本地自编译**而成。它们**不是** DeepSeek
> 官方发布的二进制文件,也**不是** DeepSeek 官方的 DMG 安装包。**未签名、未经 Apple 公证。**

---

## 为什么有这个仓库

上游发布的安装包主要面向 Apple Silicon(ARM)机型。Intel 芯片的 Mac 用户可以自行从
源码编译桌面端 —— 本仓库只是把编译结果发布出来,省去其他 Intel Mac 用户重复搭建
工具链的麻烦。

## 下载

请前往 [**Releases**](../../releases) 页面。每个版本提供两个等价安装包以及校验文件:

| 安装包 | 说明 | 适用场景 |
|---|---|---|
| `DeepSeek-Harness-<版本>-mac-x64-unsigned.dmg` | macOS 磁盘映像,内含应用本体和 `Applications` 快捷方式 | **推荐。** 双击挂载 → 拖入「应用程序」即可。 |
| `DeepSeek-Harness-<版本>-mac-x64-unsigned.zip` | 普通 ZIP 压缩包,内含 `.app` | 备选,适合习惯手动解压的用户。 |
| `*.sha256` | SHA-256 校验值 | 运行前校验文件完整性。 |

## 安装步骤

1. 下载 `.dmg`(推荐)或 `.zip`。
2. **DMG:** 双击挂载,把 **`DeepSeek Harness.app`** 拖进 **「应用程序」(Applications)**
   文件夹,然后推出磁盘映像。
   **ZIP:** 解压后,把 `.app` 拖进「应用程序」文件夹。
3. 从「启动台」或「应用程序」文件夹启动。

### 首次打开 —— 放行未签名应用

由于本构建**未签名、未公证**,macOS 的 Gatekeeper 会在首次打开时拦截。需要你手动放行:

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

## 构建特征

| 项目 | 值 |
|---|---|
| 平台 | macOS x64 / Intel(`darwin-x64`) |
| 构建方式 | 官方源码,本地自编译 |
| 签名 | **未签名** —— 无 Apple Developer 签名 |
| 公证 | **未经 Apple 公证**(not notarized) |
| 最低系统 | `macOS 13.0`(Ventura 及以上) |
| 打包形式 | `.dmg` 磁盘映像与 `.zip` 压缩包 —— **不包含源码** |

## 校验下载文件

```bash
shasum -a 256 DeepSeek-Harness-*.dmg
shasum -a 256 DeepSeek-Harness-*.zip
```

将输出与随版本一同发布的 `.sha256` 文件进行比对。

## 不包含哪些内容

本仓库发布的任何安装包都**不包含** API Key、token、`.env` 文件、个人配置、缓存或日志。
所有凭据均由你在运行时自行提供。

## 问题反馈

本仓库只是一个分发仓库,并非上游项目的 fork。
如果你遇到的是 DeepSeek Harness 本身的功能缺陷,请向上游反馈:
<https://github.com/deepseek-ai/deepseek-harness/issues>

## 许可证

DeepSeek Harness 采用 **MIT 许可证**,© 2026 DeepSeek。
本仓库发布的构建在同一许可证下再分发,详见 [LICENSE](./LICENSE)。

上游项目:<https://github.com/deepseek-ai/deepseek-harness>

---

<div align="center">

[English](./README.md) · **简体中文**

</div>
