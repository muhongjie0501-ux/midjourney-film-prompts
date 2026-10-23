# 输出示例

以下均为原创教学示例，未实际出图。数值是候选起点，不是官方最佳值；不要将示例风格和构图变成每次默认值。示例采用本Skill的V8.2资料基线。

## 具体画面：直接输出

用户：“一个成年女人在黄昏海边等人，孤独但不是绝望，像电影的一帧。”

**英文提示词｜直接复制**

```text
Poetic cinematic film still of an adult woman standing alone on a quiet beach at dusk, looking toward an empty coastal path, a restrained sense of longing and hope, medium-wide composition with ample space around her, cool blue twilight and a thin band of warm light on the horizon, natural textures and gentle tonal transitions --v 8.2 --ar 16:9 --s 150 --c 0 --w 0 --sd
```

**中文对应｜便于理解**

诗意的电影静帧：一位成年女性独自站在黄昏的安静海滩上，望向空无一人的海岸小路，传达克制的思念与希望。中远景构图，人物周围保留充足空间；冷蓝暮光与地平线上一线温暖光亮相呼应，自然质感与柔和的明暗过渡。

**官网设置**

| 项目 | 本次设置 |
|---|---|
| 已写入提示词 | V8.2、16:9、SD；Stylization 150、Variety 0、Weirdness 0 |
| 需手动核对 | Raw关闭，使用Standard；本例无指定Personalization，建议关闭 |
| 图片入口 | 不需要参考图，移除与本次无关的已锁定参考 |

本次建议用中远景、空小路和冷暖光色表达等待与希望。

## 只讨论：不给最终提示词

用户：“先讨论。废弃车站里一个人等车，我还没决定走写实还是梦幻。”

可以答：“写实方向可以强调真实空间和克制的环境光；梦幻方向可以保留车站结构，让光线或尺度出现一处不寻常的变化。你希望观众更像看到真实发生的故事，还是进入这个人的主观感受？”

此时没有最终英文代码块。之后用户确认“写实、黄昏、别太脏，就按这个给我词”，再合并确定项输出一份完整结果，不再重复询问。

## 局部修改：保留满意内容

前提：用户已提供一张可查看的角色图，要求只把外套改为暗红色；本例需要保持原图比例。

先说明：“将这张角色图放入Editor，用Erase擦除外套区域；若用Smart Select，选中后点击Erase Selection应用遮罩，确认外套区域出现灰色棋盘透明背景。保留原图比例。”

**英文提示词｜直接复制**

```text
Change the coat to dark red. Preserve its cut, fabric texture, folds, and lighting. Keep the person's face, hair, pose, the background, and the composition unchanged. --v 8.2 --raw
```

**中文对应｜便于理解**

把外套改为暗红色，保留其剪裁、面料纹理、褶皱和光照。保持人物面部、发型、姿态、背景和构图不变。

**官网设置**

| 项目 | 本次设置 |
|---|---|
| 已写入提示词 | V8.2、Raw开启 |
| 编辑入口 | Editor，仅擦除外套区域并确认遮罩已应用；保留原图比例，不新增画幅参数 |
| 风格来源 | 沿用原图，不新增Style Reference或Personalization |

这是一条保留指令，不是已经逐像素保留成功的证明；实际结果需检查。
