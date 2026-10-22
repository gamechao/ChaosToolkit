# ChaosToolkit v1.1.0

Windows 10/11 x64 · 仅限《卡厄思梦境》国际服，国服请勿使用。

## 本次更新

- **新增「一键更新 MOD（热更后）」**：游戏热更覆盖 MOD 后，在启动器完成检查／修复游戏文件，退出游戏，再通过「检查与交付」菜单恢复上次安装清单中的全部 MOD，无需逐个重新安装或重新 AI 生成。
- 更新前逐字节核对制作版本的贴图、骨骼、图集等原版依赖，统一生成、检查容量、合并并回读补丁。发现资源不兼容、残留旧修改、素材在生成期间变化或安装事务未完成时停止，不强行写入。
- 保留制作素材、提示词、参考图、连接设置、旧安装记录及旧备份。以修复后的游戏文件建立新的还原备份；写入或制作配置迁移失败时回滚，回滚未完成则保留恢复目录并阻止后续自动安装。当前安装完整时提示无需更新。
- **多个 MOD 共存**：不同角色、不同资源类型可以同时安装；共享分卷内的独立资源合并保留，只有重复修改同一资源时使用新安装版本。热更更新按旧安装清单恢复，不重新启用已被其他版本替换的资源。
- **外部服装参考图**：支持选择、预览和清除参考图片；有参考和无参考方案隔离，保留可选肤色参考。组装角色为图 1、服装参考为图 2，提供可见的服装保色开关。
- 保留角色组装、遮罩重绘和 UV 回投流程、原生图集高级工具、尺寸与 Alpha／选区外像素保护，以及异常尺寸结果拒绝检查。
- **统一启动入口**：完整解压后使用 `Start.cmd`。源码工作区入口统一为「启动卡厄思工具箱」，临时测试及录制入口归档。
- 发布链改为从开发源码构建并校验已验收程序哈希，不再以历史发布 DLL 或字节码补丁作为构建基础。包内提供 Python 3.14 和 .NET 8 运行时、默认方案、许可证及 SHA-256 校验和。

## 热更后怎么恢复

1. 正常退出游戏，在游戏启动器完成检查／修复游戏文件。
2. 打开工具箱，选择「检查与交付 → 一键更新 MOD（热更后）…」，确认开始。
3. 完成后启动游戏，检查对应角色和动作。若提示资源不兼容，应重新导出更新后的原版素材制作，不要删除备份或强行覆盖。

游戏尚未更新时，仍建议先还原原版再让启动器更新。不要使用热更前的备份覆盖热更后的游戏。保留当前 `data/active.json` 引用的 `backups`／`updates` 目录。

## 从旧工具版本升级

完整解压到新的独立目录。关闭旧工具窗口后，先备份并把旧工具的**整个 `data` 目录**复制到新目录，保持游戏和制作目录的原路径，再运行新目录的 `Start.cmd`。`data` 内备份及事务使用原绝对路径，确认迁移和还原均可用前不要删除或移动旧工具目录；位于外部目录的制作素材继续沿用原位置。

不要只复制 EXE，也不要只迁移 MOD 图片而遗漏安装记录、配置和备份。新默认模板不会覆盖已有同名用户方案。

## 验证范围

33 项后端测试通过，覆盖多 MOD 合并、同资源替换、容量限制及更新事务的成功、幂等、并发素材变化与失败回滚；可选肤色四类情况、外部参考图方案隔离／上传映射和界面入口检查通过。3 个实际 MOD 已基于修复后的游戏重新安装并完成资源回读；开发测试流程已由发布者验收。结果不代表所有角色、动作、客户端版本或 AI 输出质量均已验证。

发行包不包含游戏素材、用户 MOD、个人配置、连接凭据、模型、项目实现源码或调试符号。模型和自定义节点需自行准备；程序未代码签名。

## English

This release adds **one-click Mod recovery after a game update**. Exit the game, complete the launcher's file check/repair, then use the new action in the checking and delivery menu. The tool checks original dependencies, rebuilds and merges the previously installed resources, keeps user materials and historical backups, and backs up the repaired game before writing. Incompatible resources are rejected; failed writes or metadata migration roll back. A healthy installation is left unchanged.

Multiple Mods can coexist across characters and independent resources, including resources sharing a chunk. A newer installation replaces only overlapping resources. External clothing references support selection, preview, clearing, workflow isolation, and a visible color-preservation option; optional skin references remain supported.

Extract the complete `ChaosToolkit-1.1.0-win-x64.zip`, verify `SHA256SUMS.txt`, and launch `Start.cmd`. To upgrade, back up and copy the old tool's complete `data` directory while keeping original workspace and backup paths available. Do not delete the old directory until migration and restore are verified. AI models/nodes and game assets are not included. Global client only.

[上一版本 v1.0.0 / Previous release](https://github.com/gamechao/ChaosToolkit/releases/tag/v1.0.0)
