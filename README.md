# Video-Kakashi / videocopyer

Windows x64 视频制作插件公开测试包，当前版本为 **videocopyer 0.6.0-beta.1 public.1**。在 Codex 对话里规划视频、查看画布、生成 MP4，并创建或修改剪映草稿。

## 下载

- [插件包 ZIP](https://github.com/Zefe96/Video-Kakashi/releases/download/v0.6.0-beta.1-public.1/videocopyer-0.6.0-beta.1-public.1-windows-x64.zip)
- [小白图文教程 DOCX](https://github.com/Zefe96/Video-Kakashi/releases/download/v0.6.0-beta.1-public.1/videocopyer-0.6.0-beta.1-beginner-guide.zh-CN.docx)：14 页、6 张配图，可导入飞书文档，覆盖安装、API、COS、剪映编辑、UI 分轨和排错。
- [SHA256 校验文件](https://github.com/Zefe96/Video-Kakashi/releases/download/v0.6.0-beta.1-public.1/SHA256SUMS-public.txt)
- [本次发布说明](https://github.com/Zefe96/Video-Kakashi/releases/tag/v0.6.0-beta.1-public.1)

GitHub 自动生成的 Source code 归档不是可安装插件。请下载上面的 Windows x64 ZIP。

ZIP SHA-256：`0df411dc7a01f7b1e2aec71a5d1e37c2acccf956a9b1ff4f439512ea3dedaf50`

## 新版变化

烧制前保留干净底片、透明 UI PNG 和独立音频，以同一套图层时间线生成 MP4 和剪映候选草稿。支持组件分轨与整套 UI 一轨，包含基础面板、排行榜、图片、文字和有限 PNG 状态动画。已有成片中的 UI 不能自动反向拆出；PNG 状态不是剪映原生关键帧。

COS 激活口令、旧加密封套解锁与本地密钥校验已移除。真实 COS 上传仍需有效签名凭证，服务端鉴权照常生效。公开包不含桶、凭证、模型密钥或个人项目。

## 安装

准备 Windows x64、Codex 与可用的 codex 命令、FFmpeg/FFprobe、Chrome 或 Edge；需要工程时另备剪映。包内包含 Node 24 和基础 Python 依赖。Seed-VC、LivePortrait 环境与模型不随包提供。

解压后，在 videocopyer 文件夹打开 PowerShell，安装到不存在的新目录：

```powershell
.\scripts\install.ps1 -Destination 'D:\Tools\videocopyer-0.6.0-beta.1'
& 'D:\Tools\videocopyer-0.6.0-beta.1\scripts\register-codex.ps1'
```

注册脚本会复制到用户目录的 `plugins/videocopyer-0.6.0-beta.1`。后续配置应在最终注册目录进行，再重新打开 Codex 任务。需要参考视频上传时运行 `scripts/configure-storage.ps1`，隐藏输入自己的 COS 凭证，无需启用口令。完整步骤见教程及包内 README。

## 验证与限制

公开包 12,385 个文件的清单与哈希已验证，未包含本机 COS 凭证。使用包内 Node 执行全部自动测试，41 项通过，包括实际 FFmpeg 合成和 Python 草稿导出。

本版仍是 beta。v0.6 分层工程尚未完成剪映客户端打开、修改、保存重开和导出对比；当前导出 profile 针对 11.6.0.14552，不宣称全版本兼容。详情见包内 `docs/V0.6-ACCEPTANCE.md` 与 `docs/ACCEPTANCE.md`。

[旧版 v0.5.0-beta.2-public.1](https://github.com/Zefe96/Video-Kakashi/releases/tag/v0.5.0-beta.2-public.1) 保留下载，旧版说明和验收记录以对应发布页为准。

## 许可

保留 [LICENSE](LICENSE) 和 [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md) 中的上游许可和署名。此包不授予超出这些条款的商业再分发或多租户托管权利。
