# ImageGen Poster Workflow

用于 Codex 和 ChatGPT Work 的海报工作流 Skill。让内置 ImageGen 完成标题、插画和版式的整体视觉创作，配合项目资料、品牌素材、结果检查和版本记录，持续完成出图与改稿。

适用于活动海报、品牌分享图、封面和宣传图。

## 核心做法

| 环节 | 做法 |
| --- | --- |
| 需求整理 | 读取相关上下文，明确用途、准确文案、必要素材和功能入口 |
| 参考图使用 | 区分角色、品牌、风格、构图、编辑底稿与必须保留的原件 |
| 创意与出图 | 确定视觉主线，使用内置 ImageGen 生成完整海报 |
| 素材保护 | 保留原始文件，精确保护正式 Logo、文字素材和功能码 |
| 结果检查 | 分别检查内容功能和整体设计，按反馈定向修改 |
| 版本记录 | 保存实际提示词、参考素材、底稿、修改点和验收状态 |

创意海报优先由 ImageGen 统筹完整视觉，避免以 HTML/CSS、SVG 或 Python 拼版代替整张视觉创作。真实素材的精确嵌入应遵循用户要求和当前工具规则。

## 安装

### 交给 Codex 或 Work 安装

把下面这段话发给你的 Codex 或 ChatGPT Work。

```text
请将这个仓库中的 imagegen-poster-workflow 安装为当前环境可使用的 Skill：
https://github.com/liusucheng1999-lab/imagegen-poster-workflow

如果已经安装同名 Skill，请更新已有版本。完成后检查文件位置和格式。
```

### 在本机 Codex 安装

首次安装可以执行以下命令，将仓库放到用户级技能目录。

```bash
mkdir -p ~/.agents/skills
git clone https://github.com/liusucheng1999-lab/imagegen-poster-workflow.git \
  ~/.agents/skills/imagegen-poster-workflow
```

通过上述方式安装后，可以这样更新。

```bash
git -C ~/.agents/skills/imagegen-poster-workflow pull --ff-only
```

本机已存在其他来源的同名 Skill 时，先检查原文件和本地修改，再选择更新方式。

## 使用

在支持本地 Skill 的环境中，明确提及技能名称并描述任务。Codex 也可以使用 `$imagegen-poster-workflow` 调用。

```text
使用 imagegen-poster-workflow，为我的项目制作一张活动海报。

请先读取项目里的品牌素材。
活动主题、日期、地点和必须出现的文案以我提供的内容为准。
需要的扫码入口使用真实原件。
使用内置 ImageGen 生成整体视觉，完成后检查并保存版本。
```

也可以直接提出主题主视觉需求。

```text
使用 imagegen-poster-workflow，做一张「AI创客星球」的「AI+自媒体」主题海报。
参考我提供的品牌素材，只放已确认的品牌名和主题。
```

## 三种设计模式

| 模式 | 使用场景 | 改动范围 |
| --- | --- | --- |
| Generate | 从零设计，或根据参考图创作 | 在需求与品牌约束内构思完整海报 |
| Redesign | 基于已有海报重做视觉 | 保留核心信息和指定素材，重做构图、层级或画风 |
| Edit | 修改某一版中的指定内容 | 明确修改目标，保护已认可部分，并与底稿对照 |

例如，局部改稿可以这样描述。

```text
使用 Edit 模式，基于 v02 修改活动日期。
新日期是我提供的准确文本。
其余文案、角色、配色和版式尽量保持，完成后与 v02 对照检查。
```

## 素材与交付

- 需要使用当前环境可用的内置图像生成工具。工具不可用时应说明情况，额外计费或需要 API Key 的路径须由用户明确选择。
- 二维码、小程序码和正式标志使用真实原件。功能码需要按最终发布尺寸验证识别。
- 生成式编辑可能影响其他区域，局部修改后应与底稿对照。需要精确保真的素材应单独保护。
- 提示词和版本记录有助于继续改稿，最终效果仍需结合用途、参考和用户反馈判断。

## 文件

完整工作流见 [SKILL.md](SKILL.md)。

## 相关文档

- [OpenAI 图像生成说明](https://learn.chatgpt.com/docs/image-generation)
- [OpenAI Skills 说明](https://learn.chatgpt.com/docs/build-skills)

