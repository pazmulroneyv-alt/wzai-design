## 玩赚AI设计工作台 v1.0.1（无内置渠道版）正式发布

玩赚 AI 设计工作台（无限画布无内置渠道版）1.0.1 正式发布，全平台支持 Windows / Linux / macOS（x64 与 arm64）。

### 主要更新

- **全面升级为独立 v1.0.1 版本**：不再覆盖旧版，支持与历史 v1.0 版本平滑并存。
- **修复多模态连线同侪依赖反向污染 Bug**：隔离多模态生成节点与下游 Config 节点，严禁下游独立输入反向污染上游生成链路。
- **优化 New-API 路由与扣费防重**：针对 `gpt-image-2.5` / `gpt-image-2.6`，自动模式默认走 `/v1/images/generations`，根除 `$310` 接口被 New-API 重复扣费风险。
- **强化本地端点鉴权与模型读取**：支持 `localhost` / `127.0.0.1` 免 Key 零鉴权拉取模型列表；全面通过主进程绕过跨域预检。
- **全平台客户端更新识别体系**：内置自动与手动更新检测入口，自动比对最新发布，支持静默下载、SHA-256 哈希校验与防篡改拦截，绝不未经用户确认静默启动安装。

### 安装包

| 系统 | 安装包 |
| --- | --- |
| Windows x64 | `Wanzhuan-AI-Design-Setup-1.0.1-noplugin-x64.exe` |
| Linux x64 | `Wanzhuan-AI-Design-1.0.1-noplugin-linux-amd64.deb`、`Wanzhuan-AI-Design-1.0.1-noplugin-linux-x86_64.AppImage` |
| Linux arm64 | `Wanzhuan-AI-Design-1.0.1-noplugin-linux-arm64.deb`、`Wanzhuan-AI-Design-1.0.1-noplugin-linux-arm64.AppImage` |
| macOS Intel | `Wanzhuan-AI-Design-1.0.1-noplugin-macos-x64.dmg` |
| macOS Apple Silicon | `Wanzhuan-AI-Design-1.0.1-noplugin-macos-arm64.dmg` |

### 校验值（SHA-256）

```
c24f57bee3eb1f603838834551b3821e43e6d007161f9de5acb1a065b765b3c4  Wanzhuan-AI-Design-Setup-1.0.1-noplugin-x64.exe
f65c5f003758a6df23bf0db5ffe0515330d1ab948f1ae5fd1aca965769ab9ce1  Wanzhuan-AI-Design-1.0.1-noplugin-linux-amd64.deb
45121206215cdf23063e30bdd89714fee13dadb048c5c80b9a200dace3cdfb3b  Wanzhuan-AI-Design-1.0.1-noplugin-linux-x86_64.AppImage
97e2439f5ef40e23028b51b9062b15268815ee35abb6c7cb47993a5171a46bc1  Wanzhuan-AI-Design-1.0.1-noplugin-linux-arm64.deb
feb98433edce2d5af680daf84b5ee7548dbb7558fec6228e42d1cf520d53916d  Wanzhuan-AI-Design-1.0.1-noplugin-linux-arm64.AppImage
f89e400c0ab0ce979fe3191eb44e6d00faec44a5973d37dfa60554b35662e176  Wanzhuan-AI-Design-1.0.1-noplugin-macos-x64.dmg
d994249c7ca9587653942719b9ebf1c34abea1864d6eb94c65febaa6b55d0e0e  Wanzhuan-AI-Design-1.0.1-noplugin-macos-arm64.dmg
```

每个安装包同时附有 `.sha256` 文件，供升级入口自动校验使用。

### 局域网归档

- NAS 发布目录：`\\192.168.88.8\wz\无限画布二开\wzai-design-v1.0.1-noplugin\`
