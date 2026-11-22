## 玩赚AI设计工作台 v1.0.2（内置渠道版）正式发布

玩赚 AI 设计工作台（无限画布）1.0.2 正式版，覆盖 Windows / Linux / macOS（x64 与 arm64）。

### 主要更新

- **彻底修复升级安装完成后仍重复提示「安装新版本」Bug**：在 `restore()` 启动恢复及 `check()` 检测阶段增加语义版本号与当前 `app.getVersion()` 的严格比对；升级重启后自动销毁遗留的 `updates/state.json` 及旧安装包并释放磁盘空间，状态 cleanly 重置，不再陷入死循环提醒。
- **支持已就绪更新跨代发现**：若本地已下载旧版更新包尚未安装，而仓库又推出了更新的版本，再次检查可穿透拉取最新版。
- **包含 v1.0.1 全部重要修复**：多模态连线隔离、`gpt-image-2.5/2.6` 自动防重路由、主进程模型直读与跨版本严格排除 `noplugin` 防串包保护。

### 安装包

| 系统 | 安装包 |
| --- | --- |
| Windows x64 | `Wanzhuan-AI-Design-Setup-1.0.2-x64.exe` |
| Linux x64 | `Wanzhuan-AI-Design-1.0.2-linux-amd64.deb`、`Wanzhuan-AI-Design-1.0.2-linux-x86_64.AppImage` |
| Linux arm64 | `Wanzhuan-AI-Design-1.0.2-linux-arm64.deb`、`Wanzhuan-AI-Design-1.0.2-linux-arm64.AppImage` |
| macOS Intel | `Wanzhuan-AI-Design-1.0.2-macos-x64.dmg` |
| macOS Apple Silicon | `Wanzhuan-AI-Design-1.0.2-macos-arm64.dmg` |

### 校验值（SHA-256）

```
0b17b2540074778e57e396c95d1950739e7b96190325bbfeb3a84720e9f22228  Wanzhuan-AI-Design-Setup-1.0.2-x64.exe
ac5de3b0dd6ee8e73e70fed86a5907fc1114b880ff804a3244f48ee66346ef43  Wanzhuan-AI-Design-1.0.2-linux-amd64.deb
4d3c71a2cfd95b366ad595315f63c7ce1c36fa2112c29167a82f458e63d0a4f5  Wanzhuan-AI-Design-1.0.2-linux-x86_64.AppImage
1adfcb31c52657d6d5bf7baab595f8c11fe66f928503269ff816ddeb3e139bb3  Wanzhuan-AI-Design-1.0.2-linux-arm64.deb
fc2967eec457bc4bbeed326cf5df8ff8d09a9d7a4bf83a6a5f9306f9e0a3b069  Wanzhuan-AI-Design-1.0.2-linux-arm64.AppImage
ba428860980dc602970065e7ac2345cc7ff5ff2d043a7f89abd78d5213890690  Wanzhuan-AI-Design-1.0.2-macos-x64.dmg
b0281117b0a41e3b31c092a4b8495635554d1ca4fe67e1cb0f0d3836a6e83231  Wanzhuan-AI-Design-1.0.2-macos-arm64.dmg
```

每个安装包同时附有 `.sha256` 文件，供升级入口自动校验使用。

### 局域网归档

- NAS 发布目录：`\\192.168.88.8\wz\无限画布二开\wzai-design-v1.0.2\`
