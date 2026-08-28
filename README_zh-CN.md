# Awesome Nano Banana Pro Prompts 中文说明

![Awesome Nano Banana Pro Prompts — Flaq.ai 开源提示词手册](assets/hero.png)

> 由 [Flaq.ai](https://flaq.ai) 团队创建并维护的开源 Nano Banana Pro（Gemini 3 Pro Image）实战提示词库。

**README 语言：** [English](README.md) · [简体中文](README_zh-CN.md) · [繁體中文](README_tw.md) · [日本語](README_ja.md) · [한국어](README_ko.md) · [Español](README_es.md) · [Français](README_fr.md) · [Deutsch](README_de.md) · [Português](README_pt.md) · [Italiano](README_it.md) · [Русский](README_ru.md) · [العربية](README_ar.md) · [ไทย](README_th.md) · [Bahasa Indonesia](README_id.md) · [Tiếng Việt](README_vi.md)

[提示词目录](prompts/) · [完整方法论](docs/prompting-guide.md) · [多语言指南](docs/multilingual-prompting.md) · [API 快速上手](docs/api-quickstart.md)

这个项目面向真实生产场景，而不是简单堆砌风格关键词。仓库收录 **20 个分类、100 条原创提示词配方**，覆盖品牌广告、电商、社交媒体、信息图、UI、角色与分镜、摄影、建筑、时尚、旅行、动植物、字体、游戏、历史文化、出版、图片编辑、本地化、商业表达和本地商家营销。

## 项目亮点

- 每条提示词均为本项目重新编写，不收录删除署名的社区内容；
- 提供 15 种语言的 README 入口，方便全球创作者、开发者和社区使用；
- 针对 Nano Banana Pro 的文字渲染、多图合成、角色一致性、搜索接地、本地化和 4K 输出能力设计；
- 支持英语、简体中文、繁体中文、日语、韩语、西班牙语、法语、德语等多语言工作流；
- 提供参考图角色标注、精确文案区、不可变约束、迭代指令和成品质检；
- 示例素材具有明确的来源说明，不把其他模型的图片冒充 Nano Banana Pro 官方样张。

## Nano Banana Pro 能力概览

以下信息按 Google 官方文档于 **2026 年 8 月 28 日**核对，生产使用前请再次查看官方更新。

| 项目 | 说明 |
|---|---|
| 模型 ID | `gemini-3-pro-image` |
| 适合任务 | 专业视觉资产与复杂指令 |
| 分辨率 | 1K、2K、最高 4K |
| 参考图 | 支持工作流中最多 14 张输入图 |
| 高保真物体 | 最多 6 张物体参考图 |
| 人物一致性 | 最多 5 人 |
| 风格参考 | 最多 3 张图 |
| 文字与翻译 | 多语言文字渲染、图内本地化 |
| 知识能力 | 支持 Google Search grounding |
| 来源标记 | 生成图片包含 SynthID |

官方资料：[模型页](https://ai.google.dev/gemini-api/docs/models/gemini-3-pro-image)、[图片生成文档](https://ai.google.dev/gemini-api/docs/image-generation)、[官方提示技巧](https://blog.google/products-and-platforms/products/gemini/prompting-tips-nano-banana-pro/)。

## 60 秒开始使用

1. 从[提示词目录](prompts/)选择最接近的实际场景；
2. 替换所有 `{{双大括号变量}}`；
3. 按提示词声明的顺序上传参考图；
4. 粘贴到 Gemini、Google AI Studio 或 Gemini API；
5. 逐字检查文案，逐项检查人物、商品结构、数据和裁切；
6. 每次只修改一个变量，并在后续对话中重复“不可变约束”。

## 通用中文提示词骨架

```text
任务目标
为 {{目标用户}} 在 {{渠道}} 制作 {{资产类型}}，只传达 {{单一核心信息}}。

内容
主体：{{人物或物体}}
动作：{{正在发生的事情}}
环境：{{地点或背景}}

视觉方向
媒介/风格：{{摄影_插画_3D_UI等}}
构图：{{景别_机位_主体位置_留白}}
光线/色彩：{{方向_软硬_氛围_配色}}
格式：{{画幅比例与分辨率}}

文字——必须逐字呈现
标题："{{准确标题}}"
辅助文字："{{准确辅助文字}}"
不得添加、改写、翻译、重复任何其他文字。

参考图
图片 1：{{人物身份_商品结构_基础场景等角色}}
图片 2：{{姿势_风格_光线_商标等角色}}

不可变约束
必须保留：{{身份_结构_布局_品牌色_数字等}}
只能修改：{{明确范围}}
禁止出现：{{常见错误}}

输出前质检
逐字核对文字；核对人物身份与商品结构；核对数字和事实；核对平台安全区；
只返回一张完成度高的最终图片。
```

## 推荐先尝试的场景

- [多语言产品海报](prompts/01-brand-and-advertising.md)
- [电商主图与商品特征板](prompts/02-ecommerce-and-product.md)
- [YouTube 缩略图与社交轮播](prompts/03-social-and-creator.md)
- [科学信息图与城市导览](prompts/04-infographics-and-education.md)
- [移动端 UI 与 SaaS 仪表盘](prompts/05-ui-app-and-web.md)
- [角色设定、四格漫画与电影分镜](prompts/06-characters-and-storytelling.md)
- [人像、美食、建筑与旅行摄影](prompts/07-photography-and-editorial.md)
- [精准修改、翻译、换光与多图合成](prompts/08-editing-and-localization.md)
- [路演页、流程图与路线图](prompts/09-business-and-productivity.md)
- [餐厅、健身、地产和旅游营销](prompts/10-local-business-campaigns.md)
- [等距 3D、黏土、水彩、剪纸与像素风](prompts/11-style-lab.md)
- [建筑、室内、空间改造与地产可视化](prompts/12-architecture-interiors-and-real-estate.md)
- [时尚、美妆、虚拟试穿与 Lookbook](prompts/13-fashion-beauty-and-lookbooks.md)
- [旅行、景观、交通与汽车概念](prompts/14-travel-landscapes-and-vehicles.md)
- [野生动物、宠物、幻想生物与植物图鉴](prompts/15-animals-creatures-and-botanicals.md)
- [字体、Logo、编辑设计与导视系统](prompts/16-typography-logos-and-editorial.md)
- [游戏精灵、模块场景、物品图集与工业剖面](prompts/17-game-assets-3d-and-industrial.md)
- [历史场景、博物馆、文化遗产与传统工艺](prompts/18-history-culture-and-heritage.md)
- [白皮书、说明书、年报与出版版面](prompts/19-documents-and-publishing.md)
- [职业头像、团队合影、用户画像与社区头像](prompts/20-profiles-teams-and-lifestyle.md)

## 多语言制作建议

- 明确目标地区，例如 `es-MX`，不要只写“西班牙语”；
- 品牌名、SKU、URL、价格、日期、单位和法律标记单独列为“禁止翻译”；
- 不要求逐词保持位置，而是要求保持信息层级并使用母语化换行；
- 从已批准的母版进行翻译，锁定构图、数字、图片、颜色和字体层级；
- 发布前必须由母语使用者校对。

可直接复制的八种语言模板位于[多语言提示指南](docs/multilingual-prompting.md)。

## 原创、权利与责任

本项目是独立社区资源，并非 Google 官方项目。仓库内提示词为本项目原创，不通过删除作者信息来重新包装他人内容。贡献内容不得包含抓取来的提示词、无权分享的图片、未经同意的人物肖像或冒充官方基准的样张。

涉及医学、法律、金融、科学、历史和实时事件时，请使用权威来源核验。保留 SynthID，并遵守所使用平台的条款。

## 常见问题

### Nano Banana Pro 是什么？

Nano Banana Pro 是 Google 对 Gemini 3 Pro Image 的产品称呼，API 模型 ID 为 `gemini-3-pro-image`。它适合需要复杂推理、文字排版、多语言、本地化、多参考图和精细控制的专业图片生成与编辑任务。

### 怎样写出更稳定的 Nano Banana Pro 提示词？

按“任务目标 → 画幅与布局 → 内容与参考图角色 → 精确文案 → 不可变约束 → 输出前质检”组织。编辑图片时，必须分别写清“只改什么”和“绝对不能改什么”。

### 可以直接生成中文、日文或韩文海报吗？

可以尝试，但发布前仍需人工校对。请指定具体地区、提供已经批准的文案、锁定品牌名与数字，并允许模型按照目标语言的习惯重新换行，而不是机械保持原文每个词的位置。

### 最多能使用多少张参考图？

Google 文档描述的 Gemini 3 图片工作流最多支持 14 张参考图；Nano Banana Pro 还分别列出了最多 6 张高保真物体参考、最多 5 人的一致性和最多 3 张风格参考。不同产品入口的限制可能不同。

### 详细提示词能保证文字和事实完全正确吗？

不能。提示词结构只能提高可靠性，不能替代审核。文字、数字、人物、商品结构和事实都必须检查；高风险内容应由相应专业人士复核。

## 关于 Flaq.ai

本开源项目由 [Flaq.ai](https://flaq.ai) 团队创建并持续维护。Flaq.ai 为图片、视频、语言、多模态与内容安全模型提供统一、面向智能体的 API 接入和创作工作区。

团队可以在 Flaq.ai 中探索和比较不同模型，把创意想法快速验证为图片或视频，再将可行方案接入应用、自动化智能体和生产流程，不必为每一家模型服务单独维护一套集成。常见应用包括：

- AI Agent 与自动化内容生产；
- 文生图、图片编辑、文生视频和图生视频；
- 商品图、广告素材、缩略图、社交媒体与品牌内容；
- 模型评测、API 开发、课程教学与工作流教程。

推荐入口：[在 Flaq.ai 使用 Nano Banana Pro](https://flaq.ai/models/google/nano-banana-pro/) · [浏览 AI 模型市场](https://flaq.ai/model-market/) · [查看 API 文档](https://flaq.ai/docs/)。

## 加入 Flaq.ai 推广联盟

开发者、Agent 构建者、创作者、模型评测者、教育者和 AI 社区可以加入 [Flaq.ai Affiliate Program](https://flaq.ai/affiliate-program/)，创建专属推荐链接，向合适的受众介绍 Flaq.ai 的工具与 API，并从符合条件的推荐订单中获得佣金。

- 被推荐用户的首笔有效付费订单可获得 **20% 佣金**；
- 用户注册后 60 天内产生的后续有效付费订单可获得 **10% 佣金**；
- 可在联盟工作区管理推荐链接和查看推广活动；
- 适合通过教程、模型对比、API 指南、课程、社区和创意工作流进行推广。

参与资格、归因、退款、拒付、风险审核、结算条件和最终佣金以当前有效的联盟政策及协议为准。发布推广内容前，请查看[官方推广联盟页面](https://flaq.ai/affiliate-program/)。

## 开源协议

代码与原创文字内容使用 [MIT License](LICENSE)。生成图片还可能受到所使用模型和服务条款约束，第三方产品名称归相应权利人所有。
