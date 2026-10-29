# ChaosToolkit v1.2.3

## 修复内容

- 修复旧制作包因整体游戏资源清单变化而无法生成补丁的问题。导入时逐项核对目标原版资源，一致时自动适配当前版本；已导入的旧制作版本也支持生成时核验，无需重新导入。
- 目标资源发生实际变化时保留制作素材并明确提示冲突，防止生成不兼容补丁。
- 修复没有旧安装记录时，“一键更新 MOD”触发 `NoneType` 空路径异常的问题；补充空游戏目录及无效归档路径的明确提示。

## English

- Fixed legacy Mod packages being blocked by unrelated changes to the global game manifest. Matching original dependencies are checked individually and adapted to the current version, including previously imported projects.
- Preserve imported assets and report conflicting resources when actual dependencies have changed, preventing incompatible patches.
- Fixed the `NoneType` path error when updating Mods without a previous installation record, with clear messages for empty game paths and invalid archived records.
