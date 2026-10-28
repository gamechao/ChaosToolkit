# ChaosToolkit v1.2.2

## 大招资源与修改流程

- 扩展大招资源导出：覆盖角色人物层、演出配置及其图集、粒子贴图和镜头依赖；支持导出包内 Spine、WebP 和 CFX 分层预览。粒子、自定义着色、运镜和挂点的游戏表现不保证由离线预览完整复现。
- Spine 人物层打开时暂停在可见帧。选择当前隐藏的部件会定位到可见时刻，新增时间输入，解决短暂人物层播放后无法选中、无法继续原重绘流程的问题。
- 保留组装角色重绘、遮罩、UV 回投、候选对比和确认保存流程；确认后再生成补丁并手动安装。
- SCT 超限时增加“生成容量适配候选”和取消入口。候选原样保留未修改 ASTC 块，尝试紧凑编码和存储；必要时仅尝试轻度平滑修改区域。对比编码回读后明确确认，不改变原编辑 PNG。修改 PNG 后拦截已过期的容量候选。
- 增加 WebP 帧导出、选区调色、修改帧导入及整段动画导入；验证尺寸、帧数、Alpha、时长和循环。容量不足时必须明确选择允许有损适配；最终以编码回读为准，不自动将单帧修改传播到其他帧。
- 支持新版游戏资源校验和兼容制作版本同步；保留素材及备份，归档过期安装记录，不自动重装 MOD。此次核对客户端 build 133。

## 验证与升级

- 继承 v1.2.1 卡牌外观与既有 Spine 成套导入、语音事件恢复、可选肤色参考及外部参考图流程。
- 90 项后端测试通过；肤色参考四类、外部参考图隔离、Spine 选中与模拟重绘、容量候选确认/取消及离线补丁回读通过。发布包另做搬移运行与隐私检查。
- 用户已在游戏内确认席琳娜 `1005_cut1_5` 首镜头人物层修改生效。本例不代表全部镜头、全部角色或 WebP 修改均已游戏内验收；完整换装需处理各镜头对应的人物资源。
- 完整解压发行包后运行 `Start.cmd`。升级时保留旧工具的数据、制作版本和备份，手动选择原 MOD 目录；默认模板不覆盖同名用户方案。
- 发行包与仓库不包含本机 MOD、游戏提取资源、个人设置、连接凭据、私人提示词或参考图。只公开二进制程序、使用说明和通用默认模板。

## English — v1.2.2

Adds ultimate asset export and layered previews, frame-based WebP editing, visible-pose selection and time controls for Spine cut-ins, explicit SCT capacity candidates, and compatible game-version synchronization. Existing card appearance, Spine import, voice-event restoration and redraw features are retained.

Capacity candidates preserve untouched ASTC blocks and require review before use. Source editing PNGs remain intact; later edits invalidate an accepted candidate. Offline checks and 90 backend tests pass. A user confirmed the first Selena cut-in layer in game; this does not certify every character, shot or WebP animation.

The release contains binaries, documentation and generic templates only, with no local Mods, extracted game assets, personal settings, credentials or reference images. Unpack the complete ZIP and run `Start.cmd`; retain existing user data and backups when upgrading.

---

# ChaosToolkit v1.2.1（历史记录 / History）

## 卡牌外观资源补全

- 补全「瞬间的残影」卡牌外观。按客户端 card_skin 表匹配名称、角色和档位，修复旧扫描漏掉 effect 目录高阶资源的问题。
- 新增「卡牌外观卡面」「卡牌外观动画」「卡牌外观特效」三个筛选类型。列表显示名称、普通/高阶档位及主体/背景/特效，可按客户端繁体卡面名称、角色或资源 ID 搜索。
- 「北極星的邀請」「你專屬的守護天使」分别提供普通 RARE 静态卡面，以及高阶 SUPER_RARE 的主体动画、背景和特效。
- 「鼠兔的幸福」「解決師的閒聊」「大胃王的微笑」「記錄者的回憶」等 COMMON 外观提供静态卡面；表中未指定独立动画时，不补造动画或误关联角色战斗技能特效。
- 本次客户端 build 130 核对 20 个外观、24 个独立资源（18 张静态卡面、2 个高阶主体、4 个背景/特效）。同一客户端资源库为 3,999 → 4,005 项，补入 6 个漏扫资源。数量随客户端变化，不等于全部资源均已游戏内验收。
- 主体、背景和特效仍作为独立资源预览，不自动合成为游戏内多层画面。两套主体和特效在采样中有动态变化，背景的可见几何在本次采样中保持静止。

## 兼容与验证

- 继承 v1.2.0 的 Spine 成套导入、旧导出语音事件自动补齐、SCT 标志/PMA/ASTC 尺寸修复、服装裁切和接缝处理。
- 完整解压 `ChaosToolkit-1.2.1-win-x64.zip`，核对 `SHA256SUMS.txt`，运行 `Start.cmd`，不要只替换 EXE。升级前备份旧工具完整 data 并保留制作素材及备份路径；同名用户方案不会被默认模板覆盖。
- 63 项后端测试通过；涉及的 12 个资源通过桌面预览及名称/人物/类型筛选检查。可选肤色参考四类、外部参考图上传/清除/无参考图方案隔离回归通过；发行包另做搬移运行及依赖校验。
- 无关资源条目未发现变化。本次未重新安装/还原 MOD、未提交真实 GPU 任务；游戏内多层最终效果尚未作本次验收，不能据此宣称所有角色和功能均已确认。
- 仓库只公开程序及说明，不公开应用实现源码。发行包不含提取的游戏素材、用户 MOD、个人配置、模型或凭据。

## English — v1.2.1

Adds client-table-based card appearance discovery, three appearance categories and localized names. Regular RARE artwork and SUPER_RARE main/background/effect assets are searchable by card title, character and resource ID. COMMON appearances without a model remain static; unrelated battle effects are not attached by character-name guessing.

The checked build 130 contains 20 appearances represented by 24 independent assets. Six previously omitted high-tier resources expand the same-client catalog from 3,999 to 4,005 entries. Layers are previewed separately rather than composited into a final game scene.

63 backend tests and the 12 relevant desktop previews pass, along with optional-skin and external-reference regressions. No game writes or live GPU tasks were performed. These checks do not certify every asset or final in-game layered effects. Previous v1.2.0 features and existing user data remain supported.

- [Windows x64 / Download](https://github.com/gamechao/ChaosToolkit/releases/download/v1.2.1/ChaosToolkit-1.2.1-win-x64.zip)
- [SHA256SUMS.txt](https://github.com/gamechao/ChaosToolkit/releases/download/v1.2.1/SHA256SUMS.txt)
- [BDX 配套节点 / Companion nodes](https://github.com/gamechao/ChaosToolkit/releases/download/v1.2.1/BrowndustAtalasNode.zip)（与 v1.2.0 相同）
- [上一版本 v1.2.0 / Previous release](https://github.com/gamechao/ChaosToolkit/releases/tag/v1.2.0)

---

# ChaosToolkit v1.2.0（历史记录 / History）

- 导入旧 Spine JSON 时，自动从当前制作版本对应原生资源补齐缺失的事件时间线，无需手动恢复或额外开关。
- 保留已有事件时间线；定义冲突或缺少对应动作时拒绝恢复。仅制作版本内部保存补齐副本，不修改用户选中的 JSON、atlas 或 PNG。
- 本地更新沿用原数据目录，保留用户配置、素材、制作版本与其他已启用 MOD。
- 2026-10-25：用户在正式版完成 liveevent_30075 导入、生成补丁、安装及游戏内动作、语音实测，均正常。此结论针对该样本，不代表所有资源已逐一验收。

## 本版其他功能

Windows 10/11 x64 · 仅限《卡厄思梦境》国际服，国服请勿使用。

本次汇总 v1.1.0 之后的修改，重点为 Spine 成套导入与语音事件保留、更多资源分类，以及 AI 换装与接缝处理。

正式包、校验和及配套 ComfyUI 节点通过 GitHub Releases 分发；仓库仅同步文档，不公开工具实现源码。

## 新增功能

### Spine 3.8 成套导入和原生写回

- 从资源库选择对应骨骼资源并创建 MOD 制作版本，在「制作版本 → 导入 Spine JSON＋图集」选择 JSON，同目录的同名 atlas 和配套 PNG 一并导入。支持 mesh、path、boundingbox、clipping、point 及已适配的约束和动画时间线。
- 保留导出的骨骼、槽位删改、网格/权重、皮肤、动画、部件排列和源图尺寸；生成原生 SCSP、atlas、SCT 后做语义回读及容量检查。旧制作素材保存在 history，原版资源保留。
- 提供 ASTC 4×4、6×6、8×8 和源图 Alpha 预览声明。PMA/直通声明只影响预览，不自动转换 PNG 像素；ASTC 有压缩损失，超过原资源空间仍会拒绝生成或安装。
- 导入后保存动作倍速继续保留结构修改及其他动作；事件触发时间随对应动作一起调整。

### Events 与语音触发保留

- 支持 SCSP 30001 的事件名称、整数/浮点/字符串数据、音频引用、音量、声像，以及动画中的触发时间线。导出、导入回读和最终补丁回读均保留事件。
- `liveevent_30075` 的 23 个动作（含 lobby）、10 条语音定义和 10 个触发点已完成离线验证；安装后发布者已在游戏中确认动作和语音正常。此前首版 30075 Spine 素材也已通过游戏实测。
- 原生格式不能表达的逐帧事件载荷覆盖仍会明确拒绝；不承诺任意版本或任意 Spine JSON 均可导入。

### 资源库扩展与分类修正

- 扫描范围新增 card、card_illustration、class_card，支持战斗卡牌动画、卡面、贴图及职业卡牌卡面；崩溃立绘、道具缩略图和选景场景资源单独分类。
- 补充过滤 shortcut_face_、stress_mini_face_ 小头像入口，保留已有制作版本。
- 本机对应清单的核对记录为 2,631 → 4,151 个入口，新增 1,520 项；数量随客户端和资源清单变化。已有入口保持兼容，不能把入口数量等同于可安装 MOD 的数量。

### AI 换装与局部处理

- 新增 Qwen / NoctQ 服装选区裁切配套方案：按实际遮罩加上下文裁切组装角色图，从原图集重新渲染到最多 1024×1024，处理后还原位置并 UV 回投。保留旧方案，不自动缩小遮罩；宽选区的放大收益可能有限，遮挡区域仍受当前姿态限制。
- 将「服装保色」「旧色边界融合」「单独清理新增小亮点」分开控制。服装保色时停用旧色融合，小亮点清理仍可单独开启，避免把新衣颜色拉回旧贴图。生成记录保存实际开关及清理前结果。
- 新增「接缝快速修复（涂白细线，无需 AI）」：在选中部件的图集接缝涂窄白线，使用当前贴图邻近颜色生成修复候选，不提交 GPU 任务、不回填旧衣颜色。确认后才保存；保留 Alpha 与笔触外像素，过宽或样本不足的遮罩会拒绝。复杂纹理不能保证完全恢复。
- 新增随机种子开关；实际种子保存在生成会话。关闭后使用方案固定种子；不同模型、遮罩和环境仍可能产生不同结果。

## Bug 修复

- 修复 PMA 贴图预览重复乘 Alpha：按源图 PMA/直通声明正确预览半透明部位，不转换原 PNG 像素，也不改游戏材质。
- 修复 ASTC 存储尺寸、原图尺寸与原生 UV 的对应关系。只在右/下增加必要的透明补边，不缩放或移动作者像素，避免导入后部件错贴。
- 修复旧导出器只有语音定义、漏掉触发时间线的问题。导入时自动从对应原生资源补齐缺失时间线，保留已有时间线，不修改用户原文件；定义冲突或缺少对应动作时拒绝导入，避免生成丢失语音的补丁。
- 修复应用默认建议时只填正向文本、未同步负向文本的问题，现在两者均填入可见编辑框。用户编辑框中的提示词全文原样传入，不黑箱追加；已有用户输入、外部参考图及有/无参考方案隔离继续保留。
- 修复 SCT 标志位被错误改写的问题，完整保留原版 32 位标志（包括 PMA 位），仅确保 LZ4 压缩位。普通 PNG、AI 输出、Spine 配套导入、超限贴图重编码均使用修复后的编码路径。已手动导入的旧错误 SCT 不会自动纠正，应重新生成。
- 导入他人 CZN 制作包时使用本机选择的游戏路径，不再沿用制作者机器上的绝对路径；素材字节保持一致。

## 发布与兼容

- 发布包从开发源码构建，包含匹配的引擎契约、必要依赖、Python 3.14、.NET 8 和默认方案，不依赖历史 DLL 二进制补丁。

## 原有功能继续保留

一键更新 MOD（热更后）、不同角色/资源的 MOD 共存、同资源替换、备份还原、可选肤色参考、外部服装参考、组装角色重绘和 UV 回投均为此前已有功能，本版继续保留。不会把这些功能重复计为 v1.2.0 新增。

## 使用与升级

完整解压 `ChaosToolkit-1.2.0-win-x64.zip`，核对 `SHA256SUMS.txt`，运行 `Start.cmd`。不要只复制 EXE。

从旧版升级：先备份旧工具的整个 data 目录，保留原游戏目录、制作目录及备份路径，再迁移完整 data。安装记录和事务中包含绝对路径，确认迁移与还原可用之前不要删除旧目录。新默认模板不会覆盖同名用户方案。已安装 MOD 无需因工具升级而重新生成或重新安装。

本机正式入口更新继续使用原有用户数据目录，不覆盖提示词、参考图、连接配置、制作素材或已安装 MOD。当前已打开的旧窗口不会被强制关闭；完成编辑后重新从正式入口启动。

旧导出缺少事件时间线时，导入流程自动从当前制作版本对应的原生资源补齐；已有非空时间线保留。仅保存内部工作副本，不改写用户原 JSON、atlas 或 PNG。事件定义冲突或缺少对应动作时仍明确拒绝，无需手动恢复步骤或额外开关。

## 验证范围与边界

60 项后端测试通过，覆盖原有多 MOD/热更事务、容量检查、SCT 标志、Spine 导入、事件定义/触发点、倍速和损坏引用。30075_battle_ready 与 30075_front 均重新通过离线补丁和原生 UV/动画检查；liveevent_30075 为 23 动作/4,672 帧，并通过像素保留、透明补边与损坏原生 UV 反例检查。原版 30075 与 liveevent_30075 已获游戏内反馈确认；其他样本的离线通过不等于游戏内验收。

发行包搬移验证结果见交付的验证记录。发布验证不提交真实 GPU 任务，不重新安装或还原游戏。本版不保证所有角色、动作、客户端版本或 AI 生成结果均已验证。

发行包不包含游戏素材、用户 MOD、个人配置、连接凭据、模型、项目实现源码或调试符号。模型和自定义节点需自行准备；程序未代码签名。

## English

Older exports with missing event timelines are repaired automatically from the matching native resource during import. Authored timelines and original user files are preserved; conflicting definitions remain rejected. The complete import/build/install flow and in-game animation/voice for liveevent_30075 were confirmed by the user.

Changes since v1.1.0: paired Spine 3.8 JSON/atlas/PNG import and native writeback, event definitions and voice trigger timelines, ASTC extent/UV and SCT flag fixes, expanded card asset categories, clothing-selection crop workflows, separate clothing-color/boundary/speck controls, local seam repair without AI, random seeds, visible positive/negative defaults, and machine-local game paths when importing Mod packages.

The liveevent_30075 sample retains all 23 animations and 10 voice triggers. Its animations and voices were confirmed in game by the publisher. The source backend passes 60 tests; supported samples also pass offline native-UV, animation, capacity and source-pixel checks. Native-incompatible per-frame event overrides remain rejected. These results do not certify every Spine file or game version.

Existing update recovery, multi-Mod merging, backups, user prompts, references and connection settings are preserved. Extract the complete ZIP, verify SHA256SUMS.txt and run Start.cmd. Back up and migrate the complete old data folder while retaining referenced workspace/backup paths. Global client only.

[上一版本 v1.1.0 / Previous release](https://github.com/gamechao/ChaosToolkit/releases/tag/v1.1.0)

## 配套下载 / Companion download

- [Windows x64 正式包](https://github.com/gamechao/ChaosToolkit/releases/download/v1.2.0/ChaosToolkit-1.2.0-win-x64.zip)
- [BrowndustAtalasNode.zip](https://github.com/gamechao/ChaosToolkit/releases/download/v1.2.0/BrowndustAtalasNode.zip)：独立 ComfyUI BDX 图集节点，放入 `ComfyUI/custom_nodes/`；不包含模型、游戏素材、用户配置或 MOD。其他节点和模型按工作流另行准备。
- [SHA256SUMS.txt](https://github.com/gamechao/ChaosToolkit/releases/download/v1.2.0/SHA256SUMS.txt)：同时包含正式包和节点 ZIP 的 SHA-256。
