# NTLite 精简 Windows 镜像 · 操作指南

> 使用 NTLite 精简 Windows 镜像的完整流程：从备份原版到生成精简 ISO。重点标色，补充说明弱化。
> 适用：NTLite 2025.8 · Win11 IoT Enterprise 24H2

🌐 **在线预览**：https://simiely.github.io/ntlite-windows-guide/

## 快速流程清单

1. **备份原版镜像**（复制官方 ISO 到别处，出错可重来）
2. **NTLite 加载目标映像**（Add → Load，选索引 1）
3. **套用/配置预设**（组件移除 · 兼容性开关 · 系统调优 · 无人参与）
4. **Apply → 生成精简 ISO**
5. **（可选）集成额外程序**：Edge 更新包 / HEU KMS / 微软运行库 / StartAllBack
6. **断网安装**，用户名不设密码，取消全部勾选
7. **（可选）装新版记事本/计算器**（`wsreset -i` 恢复 Store）、处理达芬奇依赖
8. 重启确认设置生效

## 四步核心配置

| 步骤 | 内容 |
|---|---|
| ① 移除组件 | DISM 模式移除功能/服务（Defender、遥测、IE、Xbox、Copilot…）与老旧/专用驱动 |
| ② 兼容性开关 | 物理机启用 / 虚拟机（Hyper-V·VMware 等）禁用；保留 USB·打印·WLAN·Store |
| ③ 系统调优 | 关隐私/遥测/Defender/更新推送；强制深色主题；启动到此电脑；TEMP→C:\Temp |
| ④ 无人参与 | 静默模式；默认安装索引 1；PE 阶段仅出错时显示 UI |

## 资源下载

- NTLite：ntlite.com/download
- Win11 IoT Enterprise LTSC 24H2 官方评估版：microsoft.com/zh-cn/evalcenter
- HEU KMS Activator（激活）：github.com/zbezj/heu_kms_activator/releases
- StartAllBack（任务栏美化）、微软常用运行库、Everything、HiBit Uninstaller

## 安装后收尾要点

- **达芬奇安装报错（缺文件）**：Everything 搜 `user.exe` → 复制到 `C:\Windows\SysWOW64` → 重新安装
- **装新版记事本/计算器**：管理员 cmd 执行 `wsreset -i` → 开始菜单出现 Store → 搜索安装
- **卸载 Store（可选）**：用 HiBit Uninstaller

## 文件说明

| 文件 | 说明 |
|---|---|
| `index.html` | 交互式操作指南（单文件、深色模式、配图内嵌） |

## 文档索引

| 文档 | 给谁看 | 内容 |
|---|---|---|
| [`AGENTS.md`](./AGENTS.md) | AI / 未来的你 | 关键坑（预设/断网/兼容性开关）+ 流程要点 |
| [`CHANGELOG.md`](./CHANGELOG.md) | 所有人 | 版本变更记录 |
