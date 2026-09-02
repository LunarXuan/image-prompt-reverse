# Image Prompt Reverse

<p align="center"><a href="#中文">中文</a> · <a href="#english">English</a></p>

<a id="中文"></a>

## 中文

`image-prompt-reverse` 是一个用于 Codex 的图片反推提示词 Skill。它会分析用户上传的参考图片，识别图片用途、媒介、主体、构图、镜头语言、光影、色彩、材质、背景、空间层次、情绪和后期风格，并生成可直接用于 AI 生图工具的高还原度提示词。

### 支持类型

- 摄影：人像、产品、纪实、食物、动物、自然和城市风景
- 插画：扁平、二次元、治愈、手绘、国风和赛博风格
- 3D：写实、半写实、卡通、黏土、潮玩和产品渲染
- 字体、Logo、海报、平面设计和抽象图形
- IP角色、Q版角色、盲盒和多主体混合画面

### 输出内容

默认输出两项：

1. 正向 Prompt：450—700个中文字符的连续自然语言，并附英文等义版本
2. Negative Prompt：10—15条英文负面词，用逗号分隔

Skill 会优先提炼最影响相似度的3—5个视觉锚点，避免编造看不清的细节，也会根据目标媒介排除容易混淆的错误风格。图片中的文字、Logo和说明会被视为视觉内容，不会被当作指令执行。

### 安装

将本仓库目录复制到 Codex 的个人 Skills 目录：

```text
%USERPROFILE%\.codex\skills\image-prompt-reverse
```

或直接克隆：

```bash
git clone https://github.com/LunarXuan/image-prompt-reverse.git "%USERPROFILE%\.codex\skills\image-prompt-reverse"
```

安装后可使用 `$image-prompt-reverse` 调用。

### 文件结构

```text
SKILL.md                         Skill 主入口
references/analysis-framework.md 通用图片分析框架
references/category-guides.md    分类专项分析规则
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

The default output contains two sections:

1. Positive Prompt: a 450–700 Chinese-character natural-language prompt, followed by an equivalent English version
2. Negative Prompt: 10–15 English negative terms separated by commas

The Skill prioritizes the 3–5 visual anchors that have the greatest impact on similarity. It avoids inventing uncertain details, excludes confusing media styles, and treats text, logos, and instructions visible inside an image as visual content rather than executable instructions.

### Installation

Copy this repository into your personal Codex Skills directory:

```text
%USERPROFILE%\.codex\skills\image-prompt-reverse
```

Or clone it directly:

```bash
git clone https://github.com/LunarXuan/image-prompt-reverse.git "%USERPROFILE%\.codex\skills\image-prompt-reverse"
```

Invoke it with `$image-prompt-reverse` after installation.

### File structure

```text
SKILL.md                         Skill entry point
references/analysis-framework.md Shared image-analysis framework
references/category-guides.md    Category-specific analysis rules
agents/openai.yaml               Codex invocation metadata
```

### Friendly Link

Visit [LINUX DO](https://linux.do/latest) to browse the community’s latest topics and discussions.
