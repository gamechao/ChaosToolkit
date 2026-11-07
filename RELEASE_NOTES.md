# ChaosToolkit v1.3.1

## 更新内容 / What's new

- “我的 MOD”新增“批量导出制作包”，可勾选当前筛选列表中的多个制作版本，支持全选和全不选，无需逐个打开编辑器。
- 每个制作版本生成独立 ZIP，可通过现有制作包导入入口使用；导出包含素材、原始资源、原生替换候选与制作清单。
- 同名文件自动编号，不覆盖已有导出；文件名自动处理 Windows 非法字符。
- 单项失败后继续导出其他版本，完成后逐项显示成功文件及失败原因。取消选择或目录对话框不会开始导出。
- 制作包不包含历史、备份、构建补丁或安装状态；导出不会安装、禁用或还原游戏 MOD。

In **My MODs**, choose **Batch export authoring packages**, select multiple versions from the current filtered list, and pick an output folder. Each version is exported as an independently importable ZIP. Existing exports are kept by adding a filename number. Individual failures do not stop the remaining exports, and the result lists each success or failure. No editor, game installation, or GPU generation is required for export.

## 下载与升级 / Download and upgrade

下载 `ChaosToolkit-1.3.1-win-x64.zip` 与 `SHA256SUMS.txt`，校验后解压至独立目录并运行 `Start.cmd`。仅适用于国际服。仓库的 Source code 附件仅包含公开说明文档，不是完整程序。保留自己的 `data`、MOD 制作目录和必要原版备份，不要用空目录覆盖已有数据。

Download the Windows ZIP and checksum file, verify SHA-256, extract to a separate folder, and run `Start.cmd`. Global client only. GitHub's Source code archives contain public documentation rather than the application. Preserve your existing user data, MOD workspace, and original restore backups.

---

# ChaosToolkit v1.3.0

## 更新内容

- 工具箱独立完成制作包导入、批量安装、启用/禁用、可恢复移除，无需打开 MOD 编辑器。旧制作包继续兼容。
- 管理列表按人物、资源种类排序，冲突版本相邻；预览、批量选择与安装前均提示冲突。支持全选和清除选择。
- 增量安装只重建变动分块，保留同块内其他 MOD，复用未变分块；保留完整校验、必要原版备份和失败回滚。
- 后台异步操作提供任务步骤百分比、阶段完成数量、当前文件和已用时间；步骤进度不等于剩余耗时预测。
- 安装成功后自动清理本次临时补丁、切换快照及编码缓存；必要原版备份保留。另提供旧缓存与历史数据的引用检查及清理。
- 容量超限时提供压缩候选与对照确认，不静默跳过有效 MOD；原始制作素材保留。
- 全部禁用时精确还原原版备用索引与 etag，不用主索引副本覆盖原版备用文件。
