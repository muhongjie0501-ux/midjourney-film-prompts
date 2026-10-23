# Midjourney 官方提示词规则

资料基线：2026-10-23。只概括影响写法的官方规则。版本与数值读取 [模型与官网控件](models-and-web.md)，普通出词无需打开来源链接。

## 普通新图：描述看得见的结果

官方关注主体、媒介、环境、光线、色彩、情绪、构图。明确数量与重要细节；优先正面描述想要的内容，删掉无效重复和冲突。短并不是硬性词数限制：复杂关系需要足够描述，简单图无需填满所有维度。[Prompt Basics](https://docs.midjourney.com/hc/en-us/articles/32023408776205-Prompt-Basics)

本Skill的整理顺序可以是：

> 画面类型/媒介 → 主体与数量 → 可见动作及关系 → 场景 → 构图视角 → 必要光色/风格细节 → 参数。

这是组织方法，不是官方规定的唯一顺序、JSON schema或词序权重。主体与媒介谁先写可按意图调整。把角色履历或文学比喻提炼为必要的可见线索，而不是让模型读长篇创作说明。

不使用给聊天模型的角色设定、任务清单或长JSON作为MJ默认提示词；不搬入Stable Diffusion的 `(term:1.3)`、单独negative prompt框写法，也不引入其他平台的 `@Element` 资产语法。不要用 `masterpiece, best quality, 8K` 替代具体内容；分辨率由相应控件/参数决定。

官方Describe为V8.1/V8.2提供较详细的描述，但它只能辅助找词，不会恢复准确原始提示词或保证复刻。[Describe](https://docs.midjourney.com/hc/en-us/articles/32497889043981-Describe)

## 参考图与编辑的语言分支

普通Image Prompt仍描述完整目标画面，图片影响内容/构图/颜色；不是“把这图改一下”的编辑接口。[Image Prompts](https://docs.midjourney.com/hc/en-us/articles/32040250122381-Image-Prompts)

Style Reference负责美学，不负责身份。正文聚焦内容，避免与参考图冲突的风格词；必要时可加一致的风格说明。[Style Reference](https://docs.midjourney.com/hc/en-us/articles/32180011136653-Style-Reference)

Edit Model可直接使用修改指令。通常按“修改目标 → 目标状态 → 保留项 → 必要的空间/光影衔接”写，简单修改不要重写整个场景。风格转换时可明确目标媒介/风格。它是当前官方允许的分支，不受传统生成“不写长指令”的机械限制。[Edit Model](https://docs.midjourney.com/hc/en-us/articles/48495453462797-Edit-Model)

Edit Model进行风格转换/重绘，且使用Style Reference或Moodboard时，优先加一句简短、与参考一致的风格描述，帮助美学生效。只改衣服颜色等局部任务不因此增加整体风格要求；普通生成仍选择性使用风格说明。[Edit Model：Retexturing](https://docs.midjourney.com/hc/en-us/articles/48495453462797-Edit-Model)

## 网页语法

- 英文画面描述后追加参数；正文与第一个 `--` 之间留空格。使用ASCII双连字符，不用中文破折号。
- 完成参数后不再追加解释性正文；数值参数不带尾部逗号/句号。
- 网页不需要 `/imagine prompt:`。图片通过官网入口指定；用户改用Discord时不能照搬网页上传说明，对本地资料未覆盖的语法不猜测。
- 不混用互斥的版本选择或SD/HD；不用未核实的参数补齐模板。

依据：[Parameter List](https://docs.midjourney.com/hc/en-us/articles/32859204029709-Parameter-List)。

`--no`适合清楚的排除物清单，官方允许项目间用逗号。复杂短语否定不可靠，且审核按词读取；优先正面描述想要的服装/状态。不要把“没人”变成“没有阴影”，两者改变的是不同画面条件。[No](https://docs.midjourney.com/hc/en-us/articles/32173351982093-No)

图中准确字样用双引号，并写明其所在位置/载体；短的拉丁字母文字更有利。中文长字样或严格排版需要单独验收，不能保证零误差。忠实中文保留用户要求实际渲染的原字样，不把海报中的英文标题翻成另一段要画出的文字。[Text Generation](https://docs.midjourney.com/hc/en-us/articles/32502277092109-Text-Generation)

需要图中文字时，可用 `with the words`、`text` 或 `written` 引出字样。出现文字错误时，才考虑Raw、较低Stylize或Editor局部修复；不将这些设置变成所有电影图片的默认值。

## 语法之外的边界

Seed用于对照测试，不能跨提示词锁人物或保存风格。参考角色分工也不是模型的硬隔离机制。提到保留条件有帮助，但不能将其等同于输出已经准确。[Seeds](https://docs.midjourney.com/hc/en-us/articles/32604356340877-Seeds)
