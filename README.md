# ModStudio



ModStudio 是 Windows MOD 管理与图集编辑工具，包含原生 MOD 编辑器，需要与 [BrownDustHelper](https://github.com/gamechao/BrownDustHelper) 配合使用：先用 BrownDustHelper 在游戏内导出素材，再用 ModStudio 导入、预览、编辑和导出 MOD。本仓库提供二进制程序及使用说明，不公开源代码。工具仅供学习、研究和技术交流使用。



## 下载



- [下载 ModStudio.zip](https://github.com/gamechao/ModStudio/releases/download/v1.0.0/ModStudio.zip)

- [下载配套 BrownDustHelper.zip](https://github.com/gamechao/BrownDustHelper/releases/download/v1.0.1/BrownDustHelper.zip)

- [下载 SHA-256 校验和](https://github.com/gamechao/ModStudio/releases/download/v1.0.0/SHA256SUMS.txt)



## 安装与启动



1. 安装 [Microsoft .NET 8 Desktop Runtime（Windows x64）](https://dotnet.microsoft.com/download/dotnet/8.0)。

2. 解压 `ModStudio.zip`，保留完整目录，包括 `SpineViewer/Engine/`。

3. 运行 `ModStudio.exe`，选择你的 MOD 目录。



不要只复制主 EXE。编辑器、预览引擎和资源文件需要保留在配套目录中。



## 与 BrownDustHelper 配合使用



1. 按照 [BrownDustHelper 使用说明](https://github.com/gamechao/BrownDustHelper#安装)安装插件并启动游戏。

2. 打开角色皮肤展示页，按 **F9** 导出素材。

3. 在游戏目录的 `BepInEx/plugins/BrownDustHelper/exports/<批次>/<资源ID>/` 找到对应资源文件夹。

4. 在 ModStudio 中点击 **“打开 MOD 编辑器”**，选择 MOD 工作目录。

5. 使用 **“导入素材制作 MOD”** 或 **“导入游戏导出”**，选择对应资源文件夹。

6. 预览素材，修改贴图，保存制作结果并导出 MOD。



**BrownDustHelper 负责游戏内导出，ModStudio 负责桌面管理与编辑**。完整的游戏素材制作流程需要配合使用这两个工具；已有完整本地素材或 MOD 时，也可以直接导入 ModStudio。



ModStudio 管理器支持搜索、类型筛选和 MOD 版本切换。管理器的启用设置须由兼容的游戏 MOD 加载插件读取；**BrownDustHelper 仅负责导出，不负责加载 MOD**。本包不附带或安装 BrownDustX，也不修改游戏客户端。



## 预览与编辑



通过内置编辑器导入本地素材、预览动画、替换或编辑贴图，并保存、导出制作结果。缺少基础素材时，可使用资源补齐功能，或关联你有权使用的本地骨骼、图集和贴图。



保留完整工具目录，避免预览引擎或运行库缺失。修改前请备份素材与 MOD；保存和导出不会自动赋予相关内容的再分发权。



## AI 重绘



可连接本地 ComfyUI，或配置 RunningHub 账号与工作流。使用本地服务时，需要自行安装相应节点和模型；随附 JSON 为工作流配置样例，不包含模型或 API 密钥。



在编辑器的 **“服务连接”** 中填写自己的服务地址和密钥，再选择或导入重绘方案。密钥保存在本机，请勿公开上传个人连接配置或任务记录。



提交云端生成可能上传贴图、遮罩、参考图和提示词，并产生平台费用。请先确认输入内容的上传权限、模型许可和平台条款。



## 使用说明与许可



工具及所附组件按相应许可条件使用。软件未经代码签名，游戏更新后仍需检查实际兼容性。



详见 [使用许可](LICENSE.txt)、[第三方声明](THIRD_PARTY_NOTICES.md)、[免责声明](DISCLAIMER.md) 和 [隐私说明](PRIVACY.md)。

