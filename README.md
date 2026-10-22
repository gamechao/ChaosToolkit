![仅限国际服！国服请勿使用！ / Global server only — do not use with the China server](assets/global-only-warning.svg)

# 🔴 仅限国际服！国服请勿使用！
# 🔴 GLOBAL SERVER ONLY — DO NOT USE WITH THE CHINA SERVER!

> [!CAUTION]
> **ChaosToolkit 仅面向《卡厄思梦境》国际服客户端。国服不适用，请勿在国服上运行、安装或应用补丁。**
>
> **ChaosToolkit is intended only for the Global client of Chaos Zero Nightmare. The China server client is not supported. Do not run, install, or apply patches to the China server client.**

# ChaosToolkit / 卡厄思 MOD 工具箱

面向《卡厄思梦境》**国际服**的 MOD 制作工具，集成资源浏览、Spine 动画预览、贴图编辑、AI 辅助重绘、补丁生成与备份还原。免费提供使用，希望帮助大家更方便地制作和检查自己的作品。

A free MOD creation toolkit for the **Global version** of Chaos Zero Nightmare, combining asset browsing, Spine animation previews, texture editing, AI-assisted redraws, patch creation, and backup/restore.

### 💬 工具 QQ 群 / QQ group

工具交流 QQ 群：**949036810**。

QQ group for tool discussion: **949036810**.

### 🔗 卡厄思相关工具推荐 / Related tools

[ChaosZeroNightmare-UserGuider](https://github.com/yporoc/ChaosZeroNightmare-UserGuider)：另外一位大佬整理的卡厄思其他功能相关工具汇总。

A collection of tools for other Chaos Zero Nightmare features, put together by another community creator.

### ❤️ 支持与鼓励 / Support the project

如果工具对你有帮助，欢迎自愿支持作者。支持与否都不影响使用。谢谢你的支持与鼓励！

If this tool helps you, optional support is appreciated. All available features remain free whether or not you donate. Thank you for your encouragement!

**[❤️ 爱发电 · 支持作者 / Support the author](https://ifdian.net/a/Gamechao)**　｜　**[☕ Ko-fi · 请我喝杯咖啡 / Buy me a coffee](https://ko-fi.com/gamechao)**

本仓库仅分发**二进制程序与使用说明，不公开应用源码**，不是开源项目。仅在取得必要授权、遵守适用条款的前提下用于学习、研究和技术交流。

This repository distributes **binaries and documentation only; application implementation sources are not public**. It is not an open-source project. Use it for learning, research, and technical exchange only where authorized and permitted by applicable terms.

- **[📦 下载 ChaosToolkit v1.0.0 / Download for Windows x64](https://github.com/gamechao/ChaosToolkit/releases/download/v1.0.0/ChaosToolkit-1.0.0-win-x64.zip)**
- [查看发行版 / View release](https://github.com/gamechao/ChaosToolkit/releases/tag/v1.0.0) · [SHA-256 校验和 / Checksums](https://github.com/gamechao/ChaosToolkit/releases/download/v1.0.0/SHA256SUMS.txt)
- [使用许可 / Binary license](LICENSE.txt) · [免责声明 / Disclaimer](DISCLAIMER.md) · [第三方声明 / Third-party notices](THIRD_PARTY_NOTICES.md) · [隐私与数据 / Privacy](PRIVACY.md)

**当前版本 / Current version: 1.0.0** · **国际服 / Global client only** · Windows 10/11 x64 · `Start.cmd`

### 🎬 视频教程 / Video tutorial

**[▶ B站：【卡厄思梦境】来点小小的皮肤震撼！](https://www.bilibili.com/video/BV1Qrni6kEV4/)**

中文实操视频：查看工具操作与 MOD 制作效果。仅适用于国际服。

Chinese walkthrough on Bilibili: see the tool in action and the Mod results. For the Global client only.

**[▶ YouTube：ChaosToolkit 视频教程 / ChaosToolkit Video Tutorial](https://youtu.be/7bK_CCKhMWI)**

英文讲解版：查看工具操作与 MOD 制作流程。仅适用于国际服。

English walkthrough: follow the tool operations and Mod creation workflow. For the Global client only.

> 点击下面的功能标题即可展开或收起。首次使用建议先完成一个资源的预览与制作副本检查，再生成或安装补丁。
>
> Click a section below to expand it. For your first run, preview one asset and check its editable Mod copy before building or installing a patch.

| 功能 / Feature | 可以做什么 / What it does | 使用方式 / How to use |
| --- | --- | --- |
| 📚 资源浏览 / Asset browser | 扫描、筛选、搜索角色资源 / Scan, filter, and search character assets | 选择国际服游戏目录后扫描 / Select the Global game folder and scan |
| 🎞️ 动画预览 / Animation preview | 预览已适配的 Spine 3.8 素材 / Preview supported Spine 3.8 assets | 资源库与编辑器 / Library and editor |
| 🎨 贴图制作 / Texture editing | 独立制作副本、部件选择与贴图编辑 / Editable copies, part selection, and texture edits | 在制作副本中操作 / Work in a Mod copy |
| ✨ AI 辅助重绘 / AI-assisted redraw | 提示词、候选预览与人工确认 / Prompts, candidate review, and confirmation | 自备服务、模型和节点 / Supply your own service, models, and nodes |
| 📦 补丁与还原 / Patching and restore | 生成补丁，保存安装备份并还原 / Build patches, retain installation backups, and restore | 安装或还原前退出游戏 / Exit the game before installing or restoring |

<details>
<summary><strong>📦 安装与首次使用 / Installation and first run</strong></summary>

### 安装 / Installation

1. **确认使用国际服客户端；国服请勿使用。** / **Confirm you have the Global client. Do not use the China server client.**
2. 下载完整的 `ChaosToolkit-1.0.0-win-x64.zip` 与 `SHA256SUMS.txt`，核对 SHA-256。 / Download the complete ZIP and checksum file, then verify SHA-256.
3. 解压到可写的独立目录，不要放进游戏目录，也不要在压缩包中直接运行。 / Extract into a separate writable folder outside the game directory. Do not run inside the archive.
4. 双击 **`Start.cmd`**，保留所有文件夹与启动文件。包内自带 Python 3.14 与 .NET 8 Windows Desktop 运行时，无需安装开发环境。 / Double-click **`Start.cmd`** and keep the complete folder structure. Python 3.14 and .NET 8 Windows Desktop runtimes are bundled; no development environment is required.
5. 选择自己的**国际服游戏安装目录**及独立 **MOD 制作目录**，两者不要相互包含。 / Select your **Global game installation** and a separate **Mod workspace**. Neither folder should contain the other.
6. 扫描资源，选择一个角色预览，再创建 MOD 制作副本进入编辑器。 / Scan assets, preview a character, and create an editable Mod copy to open the editor.

### 目录结构 / Folder layout

```text
ChaosToolkit-1.0.0-win-x64/
├─ Start.cmd                 # 启动入口 / Launcher
├─ Start.ps1                 # 启动脚本 / Launch script
├─ app/                      # 程序与引擎 / Application and engine
├─ runtime/                  # Python 与 .NET / Bundled runtimes
├─ tools/                    # 运行后端 / Runtime backend
├─ vendor/                   # 第三方组件 / Third-party components
├─ templates/                # AI 工作流模板 / AI workflow templates
├─ licenses/                 # 第三方许可 / Third-party licenses
└─ data/                     # 首次使用后生成 / Created on first use
```

GitHub 自动生成的 **Source code** 附件只有仓库文档，不是可运行程序。请下载上面的 Windows 完整 ZIP。

GitHub's automatically generated **Source code** archives contain repository documentation, not the application. Download the complete Windows ZIP linked above.

</details>

<details>
<summary><strong>📚 资源浏览与动画预览 / Asset browsing and animation previews</strong></summary>

1. 设置国际服游戏目录后，点击扫描游戏资源。首次扫描与头像提取会建立本地缓存。 / Set the Global game directory and scan its assets. The first scan and portrait extraction create a local cache.
2. 按人物、资源类型或关键词筛选，在预览区确认目标素材。 / Filter by character, asset type, or keyword, and inspect the preview.
3. 需要制作时，创建独立 MOD 副本。单纯浏览资源不会直接修改游戏文件。 / Create a separate Mod copy when ready to edit. Browsing alone does not modify game files.

支持已适配的 SSRA v4 格式及 Spine 3.8 预览。特殊材质和未适配格式不保证兼容。

Supported assets include adapted SSRA v4 formats and Spine 3.8 previews. Special materials and unsupported formats may not display correctly.

</details>

<details>
<summary><strong>🎨 贴图编辑与部件选择 / Texture editing and part selection</strong></summary>

1. 在制作副本中打开编辑器，左侧查看组合角色，右侧查看贴图图集。 / Open the editor from a Mod copy; compare the assembled character with its texture atlas.
2. 选择要修改的部件，按住 `Ctrl` 多选，放大检查边缘与范围。 / Select the parts to edit, hold `Ctrl` for multiple selections, and zoom in to check boundaries.
3. 根据需要替换贴图或生成 AI 候选，检查后确认并保存。 / Replace textures or generate an AI candidate, then review, confirm, and save.

黄色网格是选区提示，不是最终效果。生成候选不等于已经应用或保存，请检查透明区域、边缘和明暗。

Yellow meshes indicate the selection, not the final appearance. Generating a candidate does not automatically apply or save it. Inspect transparency, edges, and shading first.

</details>

<details>
<summary><strong>✨ AI 重绘与服务配置 / AI redraws and service setup</strong></summary>

### 开始生成 / Generate a candidate

1. 配置自己的 ComfyUI 或受支持的服务连接。工具不会自动启动推理服务。 / Configure your own ComfyUI or supported service connection. The tool does not start an inference service automatically.
2. 准备工作流依赖的模型和自定义节点。标准 inpaint 模板中的 `CHOOSE_YOUR_CHECKPOINT` 需替换为自己的模型；Qwen 2.1 模板需匹配的 UNet、CLIP、VAE、LoRA 和节点。 / Install the models and custom nodes required by your workflow. Replace `CHOOSE_YOUR_CHECKPOINT` in the standard inpaint template; the Qwen 2.1 template requires matching UNet, CLIP, VAE, LoRA, and nodes.
3. 选中部件，填写外观修改要求和需要保留的细节，再提交生成。 / Select parts and describe the desired change and details to preserve, then submit.
4. 检查候选，满意后确认保存。 / Inspect the candidate and confirm the save when satisfied.

### 肤色与分辨率 / Skin references and resolution

- **肤色参考可选，没有 body/neck 也能重绘。** / **Skin references are optional; redraws can proceed without body/neck parts.**
- 大选区使用保留原生像素的输入路径，不直接缩小角色画面来规避尺寸限制。 / Large selections use an input path that preserves native pixels instead of simply shrinking the character image to avoid size limits.
- 服务返回的尺寸异常或低清候选会被拒绝；结果仍需人工检查。 / Incorrectly sized or low-resolution service results are rejected. Manual review is still required.
- 停止等待不等于服务端任务已取消，不要反复提交相同任务。 / Stopping the wait does not necessarily cancel the server task. Avoid repeated submissions.

模型、节点及远程服务费用不包含在发行包中。AI 请求可能向所选服务发送贴图、遮罩、参考图与提示词，请自行核对权限和服务条款。

Models, nodes, and remote service fees are not included. Requests may send textures, masks, references, and prompts to the selected service; check your permissions and its terms.

</details>

<details>
<summary><strong>📦 保存、补丁安装与还原 / Saving, patch installation, and restore</strong></summary>

1. 保存 MOD 制作副本，再通过“检查与交付”菜单生成游戏补丁。 / Save the Mod copy, then build a game patch through the checking and delivery menu.
2. **确认目标为国际服，并正常退出游戏，再安装补丁。**工具不会自动关闭游戏。 / **Confirm the target is the Global client and exit the game normally before installing.** The tool does not close the game for you.
3. 保留 `data` 中的安装备份与事务记录。一次安装一个制作版本。 / Retain installation backups and transaction records in `data`. Install one Mod version at a time.
4. 重新进入游戏，检查对应角色、动作及实际显示。 / Reopen the game and inspect the affected character, animations, and actual appearance.
5. 切换制作版本或游戏更新前，先退出游戏并还原，再检查兼容性。 / Before switching Mod versions or updating the game, exit, restore original files, and recheck compatibility.

编辑器预览和离线检查不能代替实际游戏内验证。任意骨骼拓扑编辑、跨包合并及所有角色或更新的兼容性不作保证。

Editor previews and offline checks do not replace in-game verification. Arbitrary skeleton topology edits, cross-package merging, and compatibility with every character or update are not guaranteed.

</details>

<details>
<summary><strong>🔒 本地数据与使用许可 / Local data and licensing</strong></summary>

首次使用会在包目录的 `data` 下建立设置、连接、MOD、缓存与备份。模板复制至 `data/redraw/profiles`。不要把使用后的整个目录上传 GitHub 或再次当作发行包分享。

On first use, `data` stores settings, connections, Mods, caches, and backups. Templates are copied to `data/redraw/profiles`. Do not upload a used application folder or redistribute it as a clean release.

发行包不包含游戏素材、示例 MOD、作者个人设置、API 密钥、开发源码或调试符号。业务字节码和托管 DLL 仍可反编译，不是加密保护。程序未进行代码签名。

The release does not include game assets, example Mods, the author's settings, API keys, implementation sources, or debug symbols. Bytecode and managed DLLs remain reversible; they are not encrypted protection. The application is not code-signed.

本工具为独立社区项目，与游戏开发商、发行商、运营方及相关第三方不存在官方隶属、赞助或背书关系。仅处理有权使用的内容，遵守游戏条款、模型许可及第三方组件许可。Spine 适用其原始许可证及用户授权条件，不改称 MIT。

This is an independent community project without official affiliation, sponsorship, or endorsement by the game developer, publisher, operator, or relevant third parties. Use only authorized content and follow game terms, model licenses, and component licenses. Spine retains its original license and user authorization requirements; it is not relabeled as MIT.

[使用许可 / License](LICENSE.txt) · [免责声明 / Disclaimer](DISCLAIMER.md) · [第三方声明 / Third-party notices](THIRD_PARTY_NOTICES.md) · [隐私说明 / Privacy](PRIVACY.md)

</details>

<details>
<summary><strong>❓ 常见问题与反馈 / FAQ and feedback</strong></summary>

### 国服可以用吗？ / Can I use the China server client?

**不可以。本工具仅面向国际服，请勿在国服运行、安装或应用补丁。**

**No. This tool targets the Global client only. Do not run, install, or apply patches to the China server client.**

### 下载后找不到启动程序？ / Where is the launcher?

确认下载的是 Windows 完整 ZIP，而不是 Source code。完整解压并保留全部目录，然后运行 `Start.cmd`。

Download the Windows ZIP, not Source code. Extract all files and folders, then run `Start.cmd`.

### AI 提示缺少模型或节点？ / AI reports missing models or nodes?

根据所选工作流检查服务端依赖及模型名称。发行包只提供通用模板，不附带模型和自定义节点。

Check the server dependencies and model names required by your workflow. The package supplies generic templates, not models or custom nodes.

### 游戏更新后还能用吗？ / Will it work after a game update?

不能保证。更新前先退出游戏并还原，更新后重新扫描、检查格式和角色显示，再决定是否安装补丁。

Compatibility is not guaranteed. Exit and restore before updating, then rescan and check formats and character appearance before applying a patch.

### 反馈问题时提供什么？ / What should I include in a report?

请到 [Issues](https://github.com/gamechao/ChaosToolkit/issues) 提供工具版本、国际服客户端版本、操作步骤、错误文字或截图，以及相关日志片段。AI 问题可补充工作流及模型、节点信息。

Open an [issue](https://github.com/gamechao/ChaosToolkit/issues) with the tool version, Global client version, reproduction steps, error text or screenshots, and relevant log excerpts. For AI problems, include workflow, model, and node details.

分享前移除密钥、连接凭据、个人路径、任务链接及无权传播的素材。

Remove keys, connection credentials, personal paths, task links, and assets you cannot redistribute before sharing.

</details>
