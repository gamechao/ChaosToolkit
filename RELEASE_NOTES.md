# ChaosToolkit v1.2.2

## 更新内容

- **大招资源导出与预览**：补全人物层、图集、演出配置、粒子贴图和镜头依赖的导出，支持 Spine、WebP 及 CFX 分层预览。
- **大招人物层编辑修复**：修复动画进入隐藏时段后无法选中部件的问题。打开时暂停在可见帧，选中隐藏部件时自动定位，新增预览时间控制。
- **贴图容量适配**：新增容量候选生成、效果对比、确认和取消功能。保留未修改的数据块与原编辑图片；素材再次变化时，阻止使用过期候选。
- **WebP 动画编辑**：新增逐帧 PNG 导出、选区调色、修改帧导入和整段动画导入，支持编码回读预览及可选的有损容量适配。
- **游戏更新同步**：新增资源版本校验和兼容制作版本同步，保留制作素材与备份，支持后续重新生成和安装 MOD。

## English

- Expanded ultimate asset export and Spine, WebP and layered CFX previews.
- Fixed selection of temporarily hidden Spine parts; added visible-pose positioning and preview time controls.
- Added reviewable texture-capacity candidates with explicit acceptance, cancellation and stale-candidate protection.
- Added WebP frame export, masked color adjustment, edited-frame and animation import, encoded playback and optional lossy capacity fitting.
- Added game-resource version checks and compatible Mod project synchronization while preserving editing assets and backups.
