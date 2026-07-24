# 案例库加载协议

v0.3.1 起，bmzskill 的专家判断必须同时基于完整方法论和案例库。专家子 Agent 不得只使用 `knowledge/<expert>.md` 的摘要规则完成深度判断。

完整知识库随 skill 一起放在：

```text
knowledge/references/
```

## 全局必读

所有专家子 Agent 在执行判断前，必须先读取：

- `knowledge/framework.md`
- `knowledge/case-loading.md`
- `knowledge/references/方法论/bmzskill完整方法论.md`
- `knowledge/references/证据库/B级方法卡/B016-统一评分口径与边界说明.md`
- 自己对应的 `knowledge/<expert>.md`

## 读取原则

- 先读索引，再读具体卡片。
- 深度审查场景必须至少读取 1-3 张最相关的案例卡、负面卡、曲风卡、歌词样本或方法卡。
- 如果只读取索引、没有读取具体卡片，输出中必须写明“仅基于索引弱判断”。
- 如果已读取具体卡片，输出中必须写明最接近的卡片名，以及相似点和偏离点。
- 不要把“参考案例库方法论”说成“已按案例库审查”。只有读取了具体索引和卡片，才算按案例库审查。

## 全功能模块强制深度

所有功能模块都必须同时基于完整方法论和真实案例库输出，不允许只依赖 `knowledge/<expert>.md` 的摘要规则。

完整深度回答是默认格式。除非用户明确要求“简版 / 摘要 / 只给结论”，任何模块都禁止输出摘要。每次回答至少要包含：

- 本次依据：列出实际使用的方法论、方法卡、案例卡、曲风库、歌词库、负面对标卡或后台数据。
- 核心结论：给出明确判断，不绕弯。
- 证据拆解：说明结论为什么成立，必须回到案例或方法论，不只写感觉。
- 风险与反证：说明当前判断的不确定性、缺失材料和可能误判点。
- 最小修改动作或下一步：给出可执行动作，而不是泛泛建议。

如果某模块无法读取到足够案例，只能降级为“仅基于索引弱判断”，并主动说明缺失了哪类案例依据。

## 发布前体检 preflight

必须读取：

- `knowledge/references/证据库/B级方法卡/B012-五组十律.md`
- `knowledge/references/证据库/B级方法卡/B014-七种观众互动冲动模型.md`
- `knowledge/references/证据库/B级方法卡/B015-五组十戒.md`
- `knowledge/references/证据库/B级方法卡/B017-两轮测试阈值与换法决策.md`
- `knowledge/references/证据库/B级方法卡/B018-歌词张力感与欲望结构.md`
- `knowledge/references/证据库/A级对标卡/A级对标卡索引.md`
- `knowledge/references/证据库/负面对标卡/负面对标卡索引.md`
- `knowledge/references/曲风库/曲风参考库索引.md`
- `knowledge/references/歌词库/好歌词案例库/好歌词案例库索引.md`
- `knowledge/references/歌词库/坏歌词样本库/坏歌词样本库索引.md`
- `knowledge/references/歌词库/ai_高频风险词表.md`

如果画面、歌词或曲风命中明显类型，继续读取最相关的 A 级对标卡、负面对标卡、曲风卡和歌词样本。AI 画面判断必须至少对照负面对标卡索引；疑似泛风景、AI 催泪封面、AI 人物海报、暗场小字或伪音乐人场景时，必须读取对应 N 卡。

### preflight 输出深度下限

发布前体检不得输出简答版，除非用户明确要求“简版 / 只给结论”。完整审查必须包含以下章节：

- 已读取的案例库依据：列出具体 N 卡、B 卡、曲风索引或歌词样本。
- 短视频时间轴：0-2 秒、2-5 秒、5 秒后。
- 曲风库对照。
- 好歌词库或歌词机制对照。
- 负面样本相似度。
- AI 画面判断。
- 逐项评分。
- 音频边界说明。
- 测试假设与发布后阈值。
- 最大风险、发布前必须修改、第一优先级、下一步建议。

如果素材明显像 AI 图库、AI 海报、AI MV、泛风景氛围图或伪真实素材，必须优先读取并对照 `N001`、`N002`、`N005`、`N008` 中最相关的卡片。命中两张以上 N 卡时，不得写成“AI 风险中等”或“可用但普通 AI”，必须说明是否属于“廉价 AI 伪真实素材”，并把结论直接体现在总分和第一优先级里。

如果素材包含 prompt、Lyrics、段落元标签、编曲元标签、voice、cover、remix、Advanced 参数、咬字、音色不一致、瑕疵拼接或前奏处理，还必须读取：

- `knowledge/references/FAQ/suno技术方法论.md`
- `knowledge/references/FAQ/suno技术过时核查清单.md`

## 发布后复盘 review

必须读取：

- `knowledge/references/方法论/review_metrics_by_template_type.md`
- `knowledge/references/证据库/B级方法卡/B014-七种观众互动冲动模型.md`
- `knowledge/references/证据库/B级方法卡/B015-五组十戒.md`
- `knowledge/references/证据库/B级方法卡/B017-两轮测试阈值与换法决策.md`
- `knowledge/references/证据库/B级方法卡/B018-歌词张力感与欲望结构.md`
- `knowledge/references/证据库/A级对标卡/A级对标卡索引.md`
- `knowledge/references/证据库/负面对标卡/负面对标卡索引.md`
- `knowledge/references/曲风库/曲风参考库索引.md`

必须先判断模板类型和曲风类型，再选择指标。不要用同一套点赞率/评论率口径判断所有视频。

## 歌词质检 lyrics-check

必须读取：

- `knowledge/references/证据库/B级方法卡/B012-五组十律.md`
- `knowledge/references/证据库/B级方法卡/B015-五组十戒.md`
- `knowledge/references/证据库/B级方法卡/B018-歌词张力感与欲望结构.md`
- `knowledge/references/证据库/A级对标卡/A级对标卡索引.md`
- `knowledge/references/歌词库/好歌词案例库/好歌词案例库索引.md`
- `knowledge/references/歌词库/坏歌词样本库/坏歌词样本库索引.md`
- `knowledge/references/歌词库/ai_高频风险词表.md`

如果歌词主题或表达机制接近某个好歌词案例或坏歌词样本，继续读取具体样本文件再评分。原创性核验仍按当前环境能力说明边界。

## 发布包 publish

必须读取：

- `knowledge/references/方法论/publish_package_by_goal.md`
- `knowledge/references/证据库/B级方法卡/B014-七种观众互动冲动模型.md`
- `knowledge/references/证据库/B级方法卡/B015-五组十戒.md`
- `knowledge/references/证据库/B级方法卡/B018-歌词张力感与欲望结构.md`
- `knowledge/references/证据库/A级对标卡/A级对标卡索引.md`
- `knowledge/references/曲风库/曲风参考库索引.md`

发布包必须服务具体测试目标。标题、首屏文案、置顶评论和标签要参考相似案例的互动目标，不要只凭文案感觉生成。

## 创作启发 songwriting

必须读取：

- `knowledge/references/方法论/bmzskill进阶主题索引.md`
- `knowledge/references/方法论/music_creation_advanced_methods.md`
- `knowledge/references/方法论/ten_lyric_structure_templates.md`
- `knowledge/references/证据库/B级方法卡/B012-五组十律.md`
- `knowledge/references/证据库/B级方法卡/B015-五组十戒.md`
- `knowledge/references/证据库/B级方法卡/B018-歌词张力感与欲望结构.md`
- `knowledge/references/证据库/A级对标卡/A级对标卡索引.md`
- `knowledge/references/歌词库/好歌词案例库/好歌词案例库索引.md`
- `knowledge/references/歌词库/坏歌词样本库/坏歌词样本库索引.md`
- `knowledge/references/歌词库/ai_高频风险词表.md`

如果用户要求完整歌词结构方案、段落元标签、编曲元标签或音乐生成工具适配，还必须读取 `knowledge/references/FAQ/suno技术方法论.md`；读取该文件只用于给结构、标签和工具适配方向，不代表可以直接代写完整歌词或连续成品句子。

## 新手引导 onboarding

必须读取：

- `knowledge/references/方法论/bmzskill进阶主题索引.md`
- `knowledge/references/证据库/B级方法卡/B012-五组十律.md`
- `knowledge/references/证据库/B级方法卡/B014-七种观众互动冲动模型.md`
- `knowledge/references/证据库/B级方法卡/B015-五组十戒.md`
- `knowledge/references/证据库/A级对标卡/A级对标卡索引.md`

如果用户已经带着具体作品进入新手引导，按作品类型继续读取曲风库、歌词库、发布包或复盘相关索引。
