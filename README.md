# FanSSH 更新通道

本仓库是 [FanSSH](https://github.com/fanlic/fanssh) 的**公开更新通道**，只存放发布产物，不含源码（源码仓库为私有）。

## 内容

每个 Release 包含：

| 文件 | 说明 |
| --- | --- |
| `FanSSH_<version>_x64-setup.exe` | NSIS 安装包，已安装用户由应用内「设置 → 检查更新」自动升级 |
| `FanSSH-portable-windows-x64.zip` | 便携版，不支持自更新，下载后解压覆盖即可 |
| `latest.json` | 自动更新清单（版本号、更新日志、安装包地址与签名） |

客户端固定读取：

```
https://github.com/fanlic/fanssh-updates/releases/latest/download/latest.json
```

Release 的 tag 即应用版本号（例如 `1.0.1`）。

## 说明

- 构建产物未做代码签名，首次运行 Windows SmartScreen 可能提示“Windows 已保护你的电脑”，选择“更多信息 → 仍要运行”。
- 更新包使用 Tauri 更新签名校验，来源被篡改时客户端会拒绝安装。
- 本仓库由私有仓库的 CI 自动发布，请勿手动修改 Release 资产。
