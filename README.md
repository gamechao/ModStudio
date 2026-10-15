# ModStudio

ModStudio 是 Windows MOD 管理与图集编辑工具，包含原生 MOD 编辑器，需要与 [BrownDustHelper](https://github.com/gamechao/BrownDustHelper) 配合使用：先用 BrownDustHelper 在游戏内导出素材，再用 ModStudio 导入、预览、编辑和导出 MOD。

ModStudio is a Windows MOD manager and texture atlas editor with a native MOD editor. Use it together with [BrownDustHelper](https://github.com/gamechao/BrownDustHelper): export assets in-game with BrownDustHelper, then import, preview, edit, and export MODs with ModStudio.

本仓库提供二进制程序及使用说明，不公开源代码。工具仅供学习、研究和技术交流使用。

This repository distributes binaries and documentation only; source code is not published. The tool is intended for learning, research, and technical exchange.

## 下载 / Downloads

- [ModStudio v1.0.0 — 下载 / Download ZIP](https://github.com/gamechao/ModStudio/releases/download/v1.0.0/ModStudio.zip)
- [配套工具 / Companion tool: BrownDustHelper v1.0.1 — 下载 / Download ZIP](https://github.com/gamechao/BrownDustHelper/releases/download/v1.0.1/BrownDustHelper.zip)
- [SHA-256 校验和 / Checksums](https://github.com/gamechao/ModStudio/releases/download/v1.0.0/SHA256SUMS.txt)

## 安装与启动 / Installation and Startup

| 步骤 / Step | 中文 | English |
|---|---|---|
| 1 | 安装 [Microsoft .NET 8 Desktop Runtime（Windows x64）](https://dotnet.microsoft.com/download/dotnet/8.0)。 | Install the [Microsoft .NET 8 Desktop Runtime for Windows x64](https://dotnet.microsoft.com/download/dotnet/8.0). |
| 2 | 解压 `ModStudio.zip`，保留完整目录，包括 `SpineViewer/Engine/`。 | Extract `ModStudio.zip` and keep the complete directory structure, including `SpineViewer/Engine/`. |
| 3 | 运行 `ModStudio.exe`，选择你的 MOD 目录。 | Run `ModStudio.exe` and select your MOD directory. |

不要只复制主 EXE。编辑器、预览引擎和资源文件需要保留在配套目录中。

Do not copy only the main EXE. Keep the editor, preview engine, and resource files in their accompanying directories.

## 配合使用 / Using Both Tools Together

**BrownDustHelper 游戏内导出 → ModStudio 导入、预览、编辑和导出 MOD。**

**Export in-game with BrownDustHelper → import, preview, edit, and export MODs with ModStudio.**

下方保留界面中的中文按钮名称，括号内为英文释义。

Chinese button labels below match the application UI; English translations are provided for reference.

| 步骤 / Step | 中文 | English |
|---|---|---|
| 1 | 按照 [BrownDustHelper 使用说明](https://github.com/gamechao/BrownDustHelper#readme)安装插件并启动游戏。 | Install the plugin using the [BrownDustHelper instructions](https://github.com/gamechao/BrownDustHelper#readme), then start the game. |
| 2 | 打开角色皮肤展示页，按 **F9** 导出素材。 | Open the character costume display screen and press **F9** to export its assets. |
| 3 | 在下方导出目录中找到对应资源文件夹。 | Find the resource folder under the export directory below. |
| 4 | 在 ModStudio 中点击 **“打开 MOD 编辑器”**，选择 MOD 工作目录。 | In ModStudio, click **“打开 MOD 编辑器” (Open MOD Editor)** and select a MOD working directory. |
| 5 | 使用 **“导入素材制作 MOD”** 或 **“导入游戏导出”**，选择对应资源文件夹。 | Choose **“导入素材制作 MOD” (Create MOD from Assets)** or **“导入游戏导出” (Import Game Export)** and select the resource folder. |
| 6 | 预览素材，修改贴图，保存制作结果并导出 MOD。 | Preview the assets, edit textures, save your work, and export the MOD. |

导出目录位于游戏目录内 / Export directory inside the game directory:

```text
BepInEx/plugins/BrownDustHelper/exports/<batch>/<resource-id>/
```

完整的游戏素材制作流程需要配合使用这两个工具；已有完整本地素材或 MOD 时，也可以直接导入 ModStudio。

Use both tools for the complete in-game export and editing workflow. If you already have complete local assets or MODs, you can import them directly into ModStudio.

ModStudio 管理器支持搜索、类型筛选和 MOD 版本切换。管理器的启用设置须由兼容的游戏 MOD 加载插件读取。**BrownDustHelper 仅负责导出，不负责加载 MOD。** 本包不附带或安装 BrownDustX，也不修改游戏客户端。

The manager supports searching, type filtering, and switching MOD variants. A compatible in-game MOD loader must read its activation settings. **BrownDustHelper exports assets only; it does not load MODs.** This package does not include or install BrownDustX and does not modify the game client.

## 预览与编辑 / Previewing and Editing

通过内置编辑器导入本地素材、预览动画、替换或编辑贴图，并保存、导出制作结果。缺少基础素材时，可使用资源补齐功能，或关联你有权使用的本地骨骼、图集和贴图。

Use the built-in editor to import local assets, preview animations, replace or edit textures, and save or export your work. If base assets are missing, use the asset retrieval feature or associate local skeletons, atlases, and textures that you have the right to use.

保留完整工具目录，避免预览引擎或运行库缺失。修改前请备份素材与 MOD；保存和导出不会自动赋予相关内容的再分发权。

Keep the complete tool directory so the preview engine and runtime dependencies remain available. Back up assets and MODs before editing. Saving or exporting does not grant redistribution rights to the content.

## AI 重绘 / AI Redrawing

可连接本地 ComfyUI，或配置 RunningHub 账号与工作流。使用本地服务时，需要自行安装相应节点和模型；随附 JSON 为工作流配置样例，不包含模型或 API 密钥。

Connect to a local ComfyUI instance or configure a RunningHub account and workflow. Local generation requires the appropriate nodes and models to be installed separately. Included JSON files are workflow configuration examples; they contain no models or API keys.

在编辑器的 **“服务连接”** 中填写自己的服务地址和密钥，再选择或导入重绘方案。密钥保存在本机，请勿公开上传个人连接配置或任务记录。

Enter your own service address and API key in **“服务连接” (Service Connection)**, then select or import a redraw profile. Keys are stored locally. Do not publicly upload personal connection settings or task records.

提交云端生成可能上传贴图、遮罩、参考图和提示词，并产生平台费用。请先确认输入内容的上传权限、模型许可和平台条款。

Cloud generation may upload textures, masks, reference images, and prompts, and may incur service charges. Check your rights to upload the inputs, model licenses, and platform terms before submitting a task.

## 使用说明与许可 / Usage and Licensing

工具及所附组件按相应许可条件使用。软件未经代码签名，游戏更新后仍需检查实际兼容性。

Use the tool and its bundled components under their applicable license terms. The software is not code-signed. Check actual compatibility after game updates.

详见 / See: [使用许可 / License](LICENSE.txt)、[第三方声明 / Third-Party Notice](THIRD_PARTY_NOTICES.md)、[免责声明 / Disclaimer](DISCLAIMER.md)、[隐私说明 / Privacy](PRIVACY.md)。

## ❤️ 支持项目 / Support the Project

如果这些工具对你有帮助，欢迎通过以下链接支持后续开发与维护。

If you find these tools useful, you can support their continued development and maintenance here:

- [Ko-fi](https://ko-fi.com/gamechao)
- [爱发电 / Afdian](https://ifdian.net/a/Gamechao)

## 🧰 社区与相关作品 / Community & Related Projects

- [BD2ModManager — bruhnn](https://github.com/bruhnn/BD2ModManager)  
  该工具的 MOD 预览功能比本项目的 ModStudio 更强大。如果你只需要 MOD 预览，可以优先使用 bruhnn 的工具。  
  This tool offers more powerful MOD preview features than our ModStudio. If you only need MOD previews, consider using bruhnn's tool.

- [BD2 Live2D Viewer — jelosus2](https://jelosus2.github.io/BD2-L2D-Viewer/)  
  用于预览角色动画的网页工具。  
  A web-based viewer for character animations.

- [BDroid_X — Ark-Repoleved](https://github.com/Ark-Repoleved/BDroid_X)  
  Android 平台的 Brown Dust II MOD 管理工具。  
  A Brown Dust II MOD manager for Android.

