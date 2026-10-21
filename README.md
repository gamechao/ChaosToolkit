# ChaosToolkit / 卡厄思 MOD 工具箱

**v1.0.0 · Windows 10/11 x64 · 首次正式发布**

用于资源浏览、Spine 3.8 动画预览、贴图编辑、AI 辅助重绘及游戏内效果检查。本仓库提供使用说明和二进制发行下载，项目实现源码不公开。

## 下载与启动

1. 前往 [Releases](https://github.com/gamechao/ChaosToolkit/releases/latest)，下载 `ChaosToolkit-1.0.0-win-x64.zip` 和 `SHA256SUMS.txt`。GitHub 自动生成的 Source code 压缩包只有仓库文档，不是可运行程序。
2. 校验 SHA256，完整解压到可写独立目录，不要放进游戏目录或在压缩包内运行。
3. 双击 **Start.cmd**。包内配有 Python 3.14 和 .NET 8 Windows Desktop 运行时，无需安装开发环境。保留 app、runtime、tools、vendor、templates 和启动文件的完整结构。
4. 选择自己的游戏安装目录及独立 Mod 制作目录，两者不要相互包含。扫描资源，预览角色，再创建 Mod 制作副本进入编辑器。
5. 选择需要修改的部件，设置提示词，生成并人工检查候选，确认后保存，再生成补丁。
6. 安装或还原前正常退出游戏，保留 data 下的备份与事务状态。游戏更新或切换制作版本前先还原，再检查兼容性。

## AI 重绘

自行配置 ComfyUI 或受支持的服务连接。模型、自定义节点及服务费用不包含在发行包中。标准 inpaint 模板的 `CHOOSE_YOUR_CHECKPOINT` 需替换为自己的模型；Qwen 2.1 模板需匹配的 UNet、CLIP、VAE、LoRA 与节点。工具不会自动启动推理服务。

肤色参考为可选项，没有 body/neck 也可重绘。大选区采用保留原生像素的输入路径，不直接缩小角色画面来规避尺寸限制；不接受服务返回的错误尺寸或低清候选。AI 结果须人工确认，停止等待不代表服务端任务已取消。

## 目录与数据

- app：桌面程序和处理引擎。
- runtime：配套 Python 与 .NET 运行时。
- tools、vendor：运行后端、兼容入口和第三方组件。
- templates：不含凭据的工作流模板，首次启动复制至 data/redraw/profiles。
- data：首次使用后建立，保存个人设置、连接、Mod、缓存及备份；不要上传使用后的整个目录。

发布包不附带游戏素材、示例 Mod、个人设置、API 密钥、开发源码或调试符号。字节码和托管 DLL 可被反编译，不构成加密保护。程序未进行代码签名。

## 使用边界与许可

支持已适配的 SSRA v4 格式、Spine 3.8 预览、贴图制作及补丁写回，一次安装一个制作版本。特殊材质、任意骨骼拓扑编辑、跨包合并及未适配格式不保证兼容。请逐项检查自己的角色、动作与游戏版本。

仅处理有权使用的素材，遵守游戏条款、模型和第三方组件许可。本工具与游戏开发、发行及运营方不存在官方隶属或背书关系。Spine 组件适用其原始许可及用户授权条件，不改称 MIT。

请阅读 [使用许可](LICENSE.txt)、[免责声明](DISCLAIMER.md)、[隐私说明](PRIVACY.md)、[第三方声明](THIRD_PARTY_NOTICES.md) 和 [发行说明](RELEASE_NOTES.md)。

## English quick start

Download the Windows x64 ZIP from [Releases](https://github.com/gamechao/ChaosToolkit/releases/latest), verify SHA256, extract the complete package into a writable folder, and run **Start.cmd**. The bundled Python and .NET runtimes require no development environment. Select separate game and Mod folders, scan assets, create a Mod copy, edit, review candidates, save, and check the result in game. AI models and custom nodes must be supplied separately. Skin references are optional. Exit the game before patching or restoring and retain backups. This is an unsigned binary distribution; implementation sources, game assets and personal credentials are not included. Follow all applicable licenses and use only authorized content.
