## 无限画布 v1.0（1.0.0）正式发布

玩赚 AI 设计工作台 1.0 正式版，覆盖 Windows / Linux / macOS（x64 与 arm64）。

### 主要更新

- 模型能力目录驱动的多模型适配：seedance 2.0 / 2.0-fast / 2.0-mini / 2.5、MiniMax-H3 / H3-Max、muse-video / muse-image、gpt-image-2.5 / gpt-image-2.6（含 `xhigh`、`max` 质量档）、MiniMax-H3-Image
- 参考图 / 参考视频 / 参考音频接入；首帧、首尾帧、参考、编辑、续写等模式
- 设置页升级入口：检查 GitHub Release、下载安装包、SHA-256 校验并拉起安装
- Linux 用户级安装：deb 仅放置只读安装源（`/usr/lib/wanzhuan-ai-design-installer`），程序安装到 `~/.local/share/wanzhuan-ai-design/app`，无需 root 运行
- 桌面快捷方式指向 `/usr/bin/wanzhuan-ai-design`

### 安装包

| 系统 | 安装包 |
| --- | --- |
| Windows x64 | `Wanzhuan-AI-Design-Setup-1.0.0-x64.exe` |
| Linux x64 | `Wanzhuan-AI-Design-1.0.0-linux-amd64.deb`、`Wanzhuan-AI-Design-1.0.0-linux-x86_64.AppImage` |
| Linux arm64 | `Wanzhuan-AI-Design-1.0.0-linux-arm64.deb`、`Wanzhuan-AI-Design-1.0.0-linux-arm64.AppImage` |
| macOS Intel | `Wanzhuan-AI-Design-1.0.0-macos-x64.dmg` |
| macOS Apple Silicon | `Wanzhuan-AI-Design-1.0.0-macos-arm64.dmg` |

### 校验值（SHA-256）

```
b24db07c1cde276f2e48b280a284922da6939682eee0fe3825e83a5fa19a43f4  Wanzhuan-AI-Design-Setup-1.0.0-x64.exe
5c86b2d176017d95d4d324e142f8e0a3f698d450f10e9b27448ed80a7e0fc242  Wanzhuan-AI-Design-1.0.0-linux-amd64.deb
e1395993fee4bf5623d8e18bf4af43350e83d2688af9df2dfd5cef265e1c0ecb  Wanzhuan-AI-Design-1.0.0-linux-x86_64.AppImage
61ff536067c1ddbd0c18b832187557cf4e3bbcda2297f0e3538f3bb37dcf6ce9  Wanzhuan-AI-Design-1.0.0-linux-arm64.deb
84303dc3900c96c6576c384619900b5884ab2ef3dfcb0dbbaa896e074c5d05b7  Wanzhuan-AI-Design-1.0.0-linux-arm64.AppImage
e90b147219f20ce036f2ae9c9ff33b87409b561dd82bffcc80c36b6d35565f52  Wanzhuan-AI-Design-1.0.0-macos-x64.dmg
4f042ae947135b02fbb23733c4171f9da91581eb011ef949e4042af06e577a91  Wanzhuan-AI-Design-1.0.0-macos-arm64.dmg
```

每个安装包同时附有 `.sha256` 文件，供升级入口校验使用。

### 说明

- Windows 安装包未做代码签名；macOS 为 ad-hoc 签名、未公证。
- x64 版本已在四台开发机完成干净安装验收；arm64 版本完成打包校验。
