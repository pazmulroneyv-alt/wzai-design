## 玩赚AI设计工作台 v1.0.1（内置渠道版）正式发布

玩赚 AI 设计工作台（无限画布）1.0.1 正式版，覆盖 Windows / Linux / macOS（x64 与 arm64）。

### 主要更新

- **修复多模态连线同侪依赖反向污染 Bug**：隔离独立图像/视频/音频生成节点与下游 Config 节点，彻底杜绝同一 Config 节点下的兄弟节点资产反向污染独立生成链路。
- **优化 `gpt-image-2.5` / `gpt-image-2.6` 协议路由与防重复扣费**：自动协议默认走 `/v1/images/generations`（不再因 `gpt-image-2.6-sunburst` 等带后缀模型名或非默认域名误落入 `/v1/responses` 工具调用），杜绝 New-API 类网关重复/高额计费风险。
- **主进程直读模型目录与本地免 Key 兼容**：新增桌面主进程直读接口 `desktop:fetch-models`，绕过浏览器跨域（CORS）预检拦截，同时支持本地（`localhost` / `127.0.0.1`）免 Key 拉取与生成。
- **严格隔离跨版本更新匹配规则**：更新校验正则严格排除 `noplugin` 包体，并将无内置渠道版独立拆分为 `wzai-design-noplugin` 仓库，确保两个版本更新源完全独立、互不串包。

### 安装包

| 系统 | 安装包 |
| --- | --- |
| Windows x64 | `Wanzhuan-AI-Design-Setup-1.0.1-x64.exe` |
| Linux x64 | `Wanzhuan-AI-Design-1.0.1-linux-amd64.deb`、`Wanzhuan-AI-Design-1.0.1-linux-x86_64.AppImage` |
| Linux arm64 | `Wanzhuan-AI-Design-1.0.1-linux-arm64.deb`、`Wanzhuan-AI-Design-1.0.1-linux-arm64.AppImage` |
| macOS Intel | `Wanzhuan-AI-Design-1.0.1-macos-x64.dmg` |
| macOS Apple Silicon | `Wanzhuan-AI-Design-1.0.1-macos-arm64.dmg` |

### 校验值（SHA-256）

```
31186d6706475c928e1509627d7bbf51652cf7ec03dc035a6ee50d60fa887c28  Wanzhuan-AI-Design-Setup-1.0.1-x64.exe
4ab48bcabd5f2a7a9a0ba27ef2cabf33bf87a7f71465cd5a5c167c74893da76b  Wanzhuan-AI-Design-1.0.1-linux-amd64.deb
d1e1c26df1af8d5a1fe3b1c9925b9523eb776ec32d7a3c429bdc6583e5094528  Wanzhuan-AI-Design-1.0.1-linux-x86_64.AppImage
eced1b541510962442c0e3fa59a405278e8e03c919a06e1bec8ccd13064d9244  Wanzhuan-AI-Design-1.0.1-linux-arm64.deb
b8df8825ecf266f7caf86a64d5f20f44c6d76d3298e578a8646284752f8ecbef  Wanzhuan-AI-Design-1.0.1-linux-arm64.AppImage
da9b72cfd7c5d34e46f07bebc824f6f0692d60554d76ef06393c0a9154ca4e2d  Wanzhuan-AI-Design-1.0.1-macos-x64.dmg
efdb7ae4e32e5b7e9bd8033aa9f73aa2f9da82dc3f1ac8b37487cc81496ae868  Wanzhuan-AI-Design-1.0.1-macos-arm64.dmg
```

每个安装包同时附有 `.sha256` 文件，供升级入口自动校验使用。

### 局域网归档

- NAS 发布目录：`\\192.168.88.8\wz\无限画布二开\wzai-design-v1.0.1\`
