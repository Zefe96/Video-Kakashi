# Video-Kakashi / videocopyer

Windows x64 视频制作插件公开测试包，基于 `videocopyer 0.5.0-beta.2`。提供 Codex 规划画布、模型 API 直连、原生视频执行、可追溯修订及剪映草稿编辑。

## 下载

请从 [v0.5.0-beta.2-public.1 Release](https://github.com/Zefe96/Video-Kakashi/releases/tag/v0.5.0-beta.2-public.1) 下载 `videocopyer-0.5.0-beta.2-public.1-windows-x64.zip` 和 `SHA256SUMS.txt`，校验后解压。GitHub 自动生成的 Source code 归档只包含本仓库说明文件，不是可安装插件。

SHA-256：`6c5997c3ba083308c61dcc1bf76b4921e849812dbdbad2f1b774ccf0560ebfdd`

## 安装

包内 `README.zh-CN.md` 提供完整安装与使用步骤。先在解压后的 `videocopyer` 目录运行：

```powershell
.\scripts\install.ps1 -Destination 'D:\Tools\videocopyer 0.5.0-beta.2'
```

如需在 Codex 中注册插件，在安装目录运行 `scripts/register-codex.ps1`。需要上传参考视频时，再在最终注册目录运行 `scripts/configure-storage.ps1`，设置你自己的腾讯云 COS 桶与凭证。公开包不含共享 COS 桶、加密凭证或启用口令。

## 状态与许可

这是 beta 测试包，尚未完成全部验收。包内 `docs/V0.5-ACCEPTANCE.md` 和 `docs/ACCEPTANCE.md` 列出已验证能力与剩余缺口。发布前的自动化测试为 35 通过、1 项因本机 Node `uv_os_get_passwd` 返回 `ENOMEM` 未运行测试正文；公开变体另完成清单哈希、凭证排除与 COS 未配置行为验证。

保留 [LICENSE](LICENSE) 和 [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md) 中的上游许可和署名。此包不授予超出这些条款的商业再分发或多租户托管权利。
