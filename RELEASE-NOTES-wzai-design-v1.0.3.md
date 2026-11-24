## 玩赚AI设计工作台 v1.0.3（内置渠道版）正式发布

玩赚 AI 设计工作台（无限画布）1.0.3 正式版，覆盖 Windows / Linux / macOS（x64 与 arm64）。

### 主要更新

- **优化 StepAudio 3 Music 交互与前置校验（方案 A）**：
  - 明确区分「音乐风格描述（caption）」与「歌词（lyrics）」输入框职责，在画布节点与独立音频页提供按任务类型切换的提示说明（纯音乐 / 歌曲 / 翻唱 / 人声配乐）及输出时长特性提示；
  - 纯音乐模式下若主输入框为空则只读防误填，若存在已输入文本或已连接上游文本节点，在点击生成前即给出明确可操作提示并阻止提交；
  - 对「歌曲」误接参考音频及「翻唱 / 人声配乐」缺少歌词或参考音频的情况增加前置校验。
- **包含 v1.0.1 / v1.0.2 全部核心修复**：升级重启自动清理遗留安装包与 `updates/state.json` 彻底消除重复提示、多模态连线隔离、`gpt-image-2.5/2.6` 自动防重路由、主进程模型目录直读。

### 安装包

| 系统 | 安装包 |
| --- | --- |
| Windows x64 | `Wanzhuan-AI-Design-Setup-1.0.3-x64.exe` |
| Linux x64 | `Wanzhuan-AI-Design-1.0.3-linux-amd64.deb`、`Wanzhuan-AI-Design-1.0.3-linux-x86_64.AppImage` |
| Linux arm64 | `Wanzhuan-AI-Design-1.0.3-linux-arm64.deb`、`Wanzhuan-AI-Design-1.0.3-linux-arm64.AppImage` |
| macOS Intel | `Wanzhuan-AI-Design-1.0.3-macos-x64.dmg` |
| macOS Apple Silicon | `Wanzhuan-AI-Design-1.0.3-macos-arm64.dmg` |

### 校验值（SHA-256）

```
fb7862a1ad502783b6d96816cf24dcfd42e8ecedbeb76512b60a9f88124c3be4  Wanzhuan-AI-Design-Setup-1.0.3-x64.exe
93dc98a2eedb1f33276affdf3aa4d050e1d6cd4996792d3b4d1381e269c59893  Wanzhuan-AI-Design-1.0.3-linux-amd64.deb
f864062c509dc6351224c6954793b4096050b9c024e7c2a535178b2e93471c17  Wanzhuan-AI-Design-1.0.3-linux-x86_64.AppImage
dad72fdd0b7ef0f8f5dfa811af5f515d99b4effa17aec33618b975bcb2468ef3  Wanzhuan-AI-Design-1.0.3-linux-arm64.deb
b1b053577576a0e6c08b935f2e50bd4b137cee24a32fbf9ba2ebce9e4763838f  Wanzhuan-AI-Design-1.0.3-linux-arm64.AppImage
a100f66d1d89112fa16eaa4d27d9e27fdd42a5afd6fc8c1bf9a955b4b34f7ec2  Wanzhuan-AI-Design-1.0.3-macos-x64.dmg
df3ef3a23f954b67692addeb506ce6057d83b1d837f4fd5b199d30ce23d5c9c5  Wanzhuan-AI-Design-1.0.3-macos-arm64.dmg
```

每个安装包同时附有 `.sha256` 文件，供升级入口自动校验使用。

### 局域网归档

- NAS 发布目录：`\\192.168.88.8\wz\无限画布二开\wzai-design-v1.0.3\`
