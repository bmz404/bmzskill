# bmzskill 发布清单

## 1. 模块范围确认

本次发布内容：

- `/bmz` 主入口
- `/bmz-lyrics-check` 歌词质检
- `/bmz-preflight` 发布前体检
- `/bmz-publish` 发布包生成
- `/bmz-review` 发布后数据复盘

## 2. 发布前文件确认

发布到 GitHub 时，仓库名建议使用：`bmzskill`

发布前应确认仓库根目录包含：

- `README.md`
- `LICENSE`
- `VERSION`
- `CHANGELOG.md`
- `docs/OPEN_SOURCE_RELEASE_CHECKLIST.md`
- `docs/判断标准说明.md`
- `skills/bmz/SKILL.md`
- `skills/bmz-lyrics-check/SKILL.md`
- `skills/bmz-preflight/SKILL.md`
- `skills/bmz-publish/SKILL.md`
- `skills/bmz-review/SKILL.md`

## 3. 隐私与安全检查

发布前确认仓库中不包含：

- 本地电脑路径
- 临时截图路径
- 私人聊天文件路径
- 私人原始素材
- 个人商业资料
- 后台数据截图原图
- 与当前功能无关的实验文件

## 4. 表达检查

表述统一使用：

- `bmzskill`
- `音乐创作、测歌、宣发和变现`
- `AI 判断流程`
- `音乐创作者、独立音乐人和短视频博主`

发布前确认 README 和 skill 文档：

- 只展示当前可用功能
- 不使用会让新用户困惑的代称
- 不承诺爆款、收益、平台推荐或发行结果
- 不把建议包装成绝对真理

## 5. 功能闭环测试

发布前至少测试一次完整路径：

1. `/bmz 新手入门`
2. `/bmz 开始写歌，主题为分手后嘴硬`
3. `/bmz-lyrics-check` 检查歌词
4. `/bmz-preflight` 检查待发布视频或首帧
5. `/bmz-publish` 生成发布包
6. `/bmz-review` 复盘数据

每一步都要确认：

- 只推荐当前模块
- 结尾有下一步推荐
- 回答能直接指导用户下一步动作
- 没有出现本地路径或私人素材信息

## 6. README 检查

README 应说明：

- bmzskill 是什么
- 判断标准来源与使用边界
- 核心流程是什么
- 5 个模块分别做什么
- 如何开始使用
- 发布包规则
- 数据复盘标准
- 作者信息：白帽子（AI音乐研究中）

README 不应说明：

- 与当前功能无关的内容
- 未验证的承诺
- 会让用户误以为一定能得到结果的话术

## 7. GitHub 发布步骤

1. 新建 GitHub 仓库：`bmzskill`
2. 将发布包解压后的内容作为仓库根目录上传
3. 确认 GitHub 页面默认展示 `README.md`
4. 检查网页端 README 图片、表格、代码块是否正常显示
5. 添加仓库简介：`把音乐创作、测歌、宣发和变现，变成一套可执行的 AI 判断流程。`
6. 添加合适标签，例如：`music`、`ai`、`creator-tools`、`short-video`、`songwriting`
7. 发布后用全新对话框加载一次，再跑完整闭环测试

## 8. 发布后观察

发布后重点观察用户反馈：

- 用户是否能理解 `/bmz` 主入口
- 用户是否会卡在歌词质检后的下一步
- 用户是否能正确使用发布前体检
- 用户是否能提供有效的数据截图进行复盘
- 是否还有不清晰、不该出现或容易误导的表达

发现问题后，优先修当前 5 个模块。

## 9. 当前发布判断

当前发布包已经具备一个完整闭环：

写歌意图进入 `/bmz`，歌词质量进入 `/bmz-lyrics-check`，发布前判断进入 `/bmz-preflight`，发布包装进入 `/bmz-publish`，数据反馈进入 `/bmz-review`。

它适合作为 bmzskill 的 GitHub 发布包。
