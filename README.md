# Image Prompt Reverse

<p align="center"><a href="#中文">中文</a> · <a href="#english">English</a></p>

<a id="中文"></a>

## 中文

上传一张参考图，告诉大模型你想保留什么：复现整张图、借画风换题材，或借构图换主体。`$image-prompt-reverse` 会把关键视觉关系写成可直接使用的生图提示词。也可以带回生成结果，请它只修正画偏的部分。

**[浏览完整案例画廊 → 17 组对比与提示词](gallery/README.md)**

### 精选案例

每张对比图左侧为参考图，右侧为纯文字生成结果。图下保留当时实际提交的中文正向词，英文译文与可选负面词可展开复制。

#### 参考画风 · 从雪山到末班电车

[![参考画风 · 从雪山到末班电车，左为参考图，右为生成图](gallery/cases/last-tram/comparison.jpg)](gallery/cases/last-tram/comparison.jpg)

**中文正向提示词 · 实际输入**

```text
设计一张“末班电车”主题的竖幅丝网版画海报。主视觉是一辆驶入终点站的老电车，架空电线与站棚切过上方。把车身、站棚、天空和站台概括成几块大的硬边多边形，斜线干脆，远近靠色块重叠拉开；用暖橙、纸白、炭灰和近黑平涂，只在小人物身上点一点暗蓝。保留轻微纸张磨痕、四周窄纸边。底部用米白色双线空心宽间距大写字排一行“LAST TRAM”。
```

<details>
<summary>英文正向译文与可选负面词（未用于此图）</summary>

**英文正向**

```text
Design a portrait-format screen-printed poster about the last tram. An old tram pulls into the terminus beneath overhead wires and a station canopy. Simplify the vehicle, canopy, sky and platform into large hard-edged polygons. Use decisive diagonals and overlapping flat shapes to separate near and far planes. Print in warm orange, paper white, charcoal and near-black, with a small touch of dark blue on the tiny figures. Keep mild paper wear and a narrow paper border. Across the bottom, set “LAST TRAM” on one line in widely spaced ivory double-outline capitals.
```

**中文负面**

```text
雪山，骑手，写实摄影，渐变天空，密集细碎的装饰线，标题换行
```

**英文负面**

```text
snowy peaks, horseback rider, photorealism, gradient sky, dense decorative linework, title split across lines
```

</details>

#### 整图复现 · 雪峰下的蛇河

[![整图复现 · 雪峰下的蛇河，左为参考图，右为生成图](gallery/cases/snake-river/comparison.jpg)](gallery/cases/snake-river/comparison.jpg)

**中文正向提示词 · 实际输入**

```text
5:4横幅黑白风景摄影，从高处俯瞰林地间的河湾。明亮河水由右下边缘宽阔地进入，沿下方横向向左回弯，在画面左下三分之一处绕出一个大弧，再向右上收窄，消失在右侧中景林带。近处黑色针叶树剪影压住左下角。深黑山脚横贯中央，锯齿状覆雪山脊位于上半部，最高的山峰在中心偏右。上方云层左白右暗，局部雪面和水面接近纯白，保留林地的灰阶层次。
```

<details>
<summary>英文正向译文与可选负面词（未用于此图）</summary>

**英文正向**

```text
A 5:4 black-and-white landscape photograph from a high vantage point above a wooded bend in a river. A broad band of bright water enters at the lower right edge and sweeps left across the bottom, forming a wide bend near the lower left third. It narrows toward the upper right and disappears into the trees in the right middle distance. Dark conifer silhouettes anchor the lower left corner. Deep black mountain foothills span the center. A jagged snow-covered ridge occupies the upper half, with the tallest peak just right of center. The clouds are bright on the left and dark on the right. Parts of the snow and water approach pure white, while the forest retains a range of grays.
```

**中文负面**

```text
彩色调色，倒置的河湾，最高峰靠左，水面漆黑，林区暗部完全堵死
```

**英文负面**

```text
color grading, reversed river bend, tallest peak on the left, pitch-black water, fully blocked forest shadows
```

</details>

#### 参考构图 · 从持秤人到修表师

[![参考构图 · 从持秤人到修表师，左为参考图，右为生成图](gallery/cases/watch-restorer/comparison.jpg)](gallery/cases/watch-restorer/comparison.jpg)

**中文正向提示词 · 实际输入**

```text
约7:8竖幅的彩色纪实照片，现代钟表修复师站在画面右半，身体向左侧转，头微低，视线落在画面中央的手指上。一手在胸下高度悬提一条细表链，另一手轻抵腰高工作台的前沿。人物从头到大腿入画，左半部上方是大片空墙和左上角窄窗，下方是工作台与深色堆布。背后右上有窄黑框挂图。左上柔窗光落在鼻梁、手指和细链上，工作室其余部分较暗。
```

<details>
<summary>英文正向译文与可选负面词（未用于此图）</summary>

**英文正向**

```text
A documentary color photograph in a roughly 7:8 portrait frame. A modern watch restorer stands on the right, turned toward the left, head slightly lowered and gaze fixed on the fingers at the center of the frame. One hand suspends a fine watch chain just below chest level. The other rests lightly against the front edge of a waist-high workbench. The figure is visible from head to thighs. In the upper left, leave a large expanse of plain wall and a narrow window in the corner. The workbench and a heap of dark fabric occupy the lower left. A print in a narrow black frame hangs behind the figure at upper right. Soft window light from the upper left catches the bridge of the nose, the fingers and the chain. The rest of the workshop is dim.
```

**中文负面**

```text
正面直视镜头，身体朝右，人物居中，双手举到肩部，天平，左侧墙面堆满工具
```

**英文负面**

```text
looking straight at the camera, body turned right, centered subject, both hands at shoulder height, balance scale, tools covering the left wall
```

</details>

#### 整图复现 · 蛋糕、柠檬与玻璃杯

[![整图复现 · 蛋糕、柠檬与玻璃杯，左为参考图，右为生成图](gallery/cases/cake-and-lemon/comparison.jpg)](gallery/cases/cake-and-lemon/comparison.jpg)

**中文正向提示词 · 实际输入**

```text
约7:5横幅的写实静物油画，白色桌布的前沿横过下三分之一，两道垂直褶皱落向底边。自左到右依次是一只盛满小红浆果的浅白盘、一块拱形黄蛋糕、一只细直透明玻璃杯。蛋糕直立，朝左的窄切面迎光，金黄宽面朝向观者，棕色外皮勾边；半个柠檬在它左前方，圆形切面正对观者，遮住蛋糕的左下角。左前另有一颗散落的红莓。杯中有淡黄色饮料和一片竖立的柠檬，一根细长黄吸管斜向右上，伸出顶边。深色背景由左边近黑过渡到右边蓝绿。
```

<details>
<summary>英文正向译文与可选负面词（未用于此图）</summary>

**英文正向**

```text
A realistic still-life oil painting in a roughly 7:5 landscape frame. The front edge of a white tablecloth crosses the lower third, with two vertical folds dropping toward the bottom. From left to right are a shallow white plate heaped with small red berries, an arched slice of yellow cake, and a slim straight-sided clear glass. The cake stands upright with its narrow left cut face catching the light, its broad golden face toward the viewer and its brown crust tracing the edge. A lemon half in front on the left presents its round cut face directly to the viewer, obscuring the cake’s lower left corner. A single red berry lies loose at front left. The glass contains a pale yellow drink and an upright lemon slice. A long thin yellow straw angles toward the upper right and exits the top edge. The dark background grades from near-black on the left to teal on the right.
```

**中文负面**

```text
柠檬在蛋糕后方，玻璃杯在左侧，吸管朝左倾斜，圆形整蛋糕，多余的盘碟
```

**英文负面**

```text
lemon behind the cake, drinking glass on the left, straw leaning left, whole round cake, extra plates
```

</details>

#### 参考构图 · 从睡莲池到砂岩峡谷

[![参考构图 · 从睡莲池到砂岩峡谷，左为参考图，右为生成图](gallery/cases/sandstone-arch/comparison.jpg)](gallery/cases/sandstone-arch/comparison.jpg)

**中文正向提示词 · 实际输入**

```text
5:4横幅的真实沙漠峡谷照片。画面上四分之一是一道长而低的红砂岩天然石拱，中央略向上隆起，拱身左右都延伸到画外，顶缘接近画面上边。拱洞下面是层层后退的干涸河床，从下沿宽阔的近景收窄到中部，两侧陡起岩壁收住视线。浅色矿物沉积和碎石呈数道断续的横带，近处较宽，向远处逐渐变密；底部一道阴影呼应上方弧线。用沙黄、铁锈红和冷紫阴影表现岩石纹层。
```

<details>
<summary>英文正向译文与可选负面词（未用于此图）</summary>

**英文正向**

```text
A realistic 5:4 landscape photograph of a desert canyon. A long, low natural arch of red sandstone crosses the upper quarter. It rises slightly in the middle, runs beyond both edges, and approaches the top border. Below the opening, a dry riverbed recedes in layers, broad in the immediate foreground and narrowing toward the center. Steep rock walls on either side channel the eye inward. Pale mineral deposits and gravel form interrupted horizontal bands, wider nearby and closer together in the distance. A curved shadow at the bottom echoes the arch above. Sandy yellow, iron red and cool purple shadows bring out the rock strata.
```

**中文负面**

```text
木桥，栏杆，睡莲，池水，画面中央的大圆拱，大片无细节蓝天
```

**英文负面**

```text
wooden footbridge, railings, water lilies, pond water, large round arch centered in the frame, broad featureless blue sky
```

</details>

#### 参考画风 · 从校园漫画到钟表铺

[![参考画风 · 从校园漫画到钟表铺，左为参考图，右为生成图](gallery/cases/clockmakers-manga/comparison.jpg)](gallery/cases/clockmakers-manga/comparison.jpg)

**中文正向提示词 · 实际输入**

```text
3:4竖幅的黑白日式短篇漫画页，主题是两位成年钟表匠修好一只闹钟。页首用夸张粗黑手绘字写“准点！”。上排两格、下排一格通栏：右上中景画两位工匠俯身在工作台边，左上特写画一人听见机芯咔哒响、眼睛睁大；下格以前景左侧的两个人物肩背框住右侧振铃的闹钟。对白泡内只写“响了！”。用轻快的黑墨轮廓、简化圆润的五官、实黑头发与白色留亮，袖褶和背景用稀疏短排线，少量平灰区分前后，纸白占大部分。
```

<details>
<summary>英文正向译文与可选负面词（未用于此图）</summary>

**英文正向**

```text
A 3:4 portrait page from a short black-and-white Japanese-style manga about two adult watchmakers repairing an alarm clock. Use exaggerated, bold, hand-drawn black lettering for the title “准点！” at the top. Place two panels above one full-width bottom panel. In the upper right, show both watchmakers in a medium shot leaning over the bench. In the upper left, show a close-up of one widening their eyes on hearing the movement click. In the lower panel, the shoulders and backs of the two figures in the left foreground frame the ringing alarm clock on the right. The speech bubble contains only “响了！”. Use lively black ink contours, simple rounded facial features, solid black hair with white highlights, sparse short hatching on sleeves and background, and touches of flat gray to separate depth planes. Leave most of the paper white.
```

**中文负面**

```text
彩色页面，四格等分，底部通栏被拆开，英文替代中文，重复对白泡，校服人物
```

**英文负面**

```text
color page, four equal panels, bottom panel split in two, English replacing the Chinese text, duplicate speech balloons, characters in school uniforms
```

</details>

### 支持类型

- 摄影：人像、产品、纪实、食物、动物、自然和城市风景
- 插画：扁平、二次元、治愈、手绘、国风和赛博风格
- 3D：写实、半写实、卡通、黏土、潮玩和产品渲染
- 字体、Logo、海报、平面设计和抽象图形
- IP角色、Q版角色、盲盒和多主体混合画面

### 输出内容

默认给出语义一致的中英文正向提示词。篇幅随画面复杂度调整，优先交代决定相似度的主体、位置、遮挡和媒介特征。目标工具支持独立负面词且有具体偏差需要排除时，再提供负面词。用户可以指定单语、长度或输出格式。

### 安装

将本仓库目录复制到 Codex 的个人 Skills 目录：

```text
%USERPROFILE%\.codex\skills\image-prompt-reverse
```

或直接克隆：

```cmd
git clone https://github.com/LunarXuan/image-prompt-reverse.git "%USERPROFILE%\.codex\skills\image-prompt-reverse"
```

安装后可使用 `$image-prompt-reverse` 调用。

### 文件结构

```text
SKILL.md                         Skill 主入口
references/analysis-framework.md 通用图片分析框架
references/category-guides.md    分类专项分析规则
references/illustration-style.md 插画画风专项
gallery/README.md                案例画廊
agents/openai.yaml               Codex 调用界面配置
```

### 友情链接

欢迎访问 [LINUX DO](https://linux.do/latest)，浏览社区最新主题与讨论。

<a id="english"></a>

## English

`image-prompt-reverse` is a Codex Skill for reverse-engineering image-generation prompts from user-uploaded reference images. It analyzes the image purpose, medium, subject, composition, camera language, lighting, color, materials, background, spatial depth, mood, and post-processing style, then produces high-fidelity prompts that can be used directly with AI image-generation tools.

### Supported image types

- Photography: portraits, products, documentary images, food, animals, nature, and cityscapes
- Illustration: flat, anime, therapeutic, hand-drawn, Chinese-inspired, and cyberpunk styles
- 3D: realistic, semi-realistic, cartoon, clay, designer toys, and product rendering
- Typography, logos, posters, graphic design, and abstract graphics
- IP-inspired characters, chibi characters, blind-box figures, and mixed-subject scenes

### Output

Ask for a whole-image recreation, a new subject in the reference style, or a new scene with the same composition. The Skill returns Chinese and English positive prompts by default. Length follows the scene. A separate negative prompt is included when the target tool supports it and a specific error warrants it. Bring a generated image back to revise the relevant wording.

[Browse all 17 reference/result pairs and their prompts](gallery/README.md).

### Installation

Copy this repository into your personal Codex Skills directory:

```text
%USERPROFILE%\.codex\skills\image-prompt-reverse
```

Or clone it directly:

```cmd
git clone https://github.com/LunarXuan/image-prompt-reverse.git "%USERPROFILE%\.codex\skills\image-prompt-reverse"
```

Invoke it with `$image-prompt-reverse` after installation.

### File structure

```text
SKILL.md                         Skill entry point
references/analysis-framework.md Shared image-analysis framework
references/category-guides.md    Category-specific analysis rules
references/illustration-style.md Illustration style analysis
gallery/README.md                Example gallery
agents/openai.yaml               Codex invocation metadata
```

### Friendly Link

Visit [LINUX DO](https://linux.do/latest) to browse the community’s latest topics and discussions.
