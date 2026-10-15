# ModStudio

Windows MOD 管理与图集编辑工具，包含原生 MOD 编辑器。二进制审核候选，不公开源代码。

## 启动

安装 Microsoft 官方 .NET 8 Desktop Runtime（Windows x64），解压完整目录后运行 `ModStudio.exe`。
点击选择目录加载你的 MOD；可搜索、筛选和切换版本。“打开 MOD 编辑器”进入制作工具，
从自己有权使用的本地文件导入素材、预览、替换/编辑贴图并导出。
管理器的启用设置须由兼容的游戏插件读取；本包不附带或安装 BrownDustX，也不修改游戏客户端。

## 功能与运行环境

本审核包恢复当前 dist 版本的程序图标、角色头像、名称映射、素材下载及内置预览运行库，
保留通用背景、原有控件和完整编辑能力。缺失基础素材时沿用当前版本的资源补齐流程。
完整目录必须保留，包括 `SpineViewer/Engine/`。所附运行库的许可条件仍按随附许可证适用。

## 重绘

需自行安装 ComfyUI、相应自定义节点及获授权模型，或配置 RunningHub 账号与工作流。
随附 JSON 是配置样例，不含模型、API 密钥或用户输入图片；模型文件名不是下载或使用授权。
首先检查模型、节点、平台条款以及待上传图像的权利。云端生成可能上传资源并产生费用。
本包不附带本机 smoke 工作流、个人配置、任务输出、缓存或开发历史说明。

编辑/导出前备份；修改的贴图不自动赋予游戏内容的再分发权。说明与限制见
[DISCLAIMER.md](DISCLAIMER.md)、[LICENSE.txt](LICENSE.txt)、[THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)
及 [PRIVACY.md](PRIVACY.md)。当前未经代码签名；未宣称完整游戏兼容性或第三方授权已确认。
