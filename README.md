# 跑地图 · 跑步知识

[English](README.en.md) · 中文

本仓库保存 `learn.paobu.org` 使用的常青跑步知识、双语正文、来源与审阅数据。它是纯内容仓库，不包含网站运行代码、`package.json`、`node_modules` 或构建产物。

## 当前状态

- 首发二十七篇文章覆盖九个主题：训练、技术、恢复、营养、装备、健康、安全、习惯、文化，每篇都有完整的中文与英文正文；另有一个跑步术语表，站内提供 5 条学习路径。
- 二十八个知识实体已于 2026-10-28 完成 **AI 辅助编辑审阅**并发布（`published`，双语 `approve` 记录与匹配 digest）：27 篇文章 + 1 个术语表。审阅者是 `runmap-editorial`，明确标注为 AI 辅助，不是独立专业医学/营养审阅；九主题已覆盖 9/9，站内提供 5 条学习路径。
- 唯一作者/审阅身份是 `runmap-editorial`：「RunMap editorial desk (AI-assisted draft and review)」，没有个人资质声明；审阅记录为 AI 辅助编辑审阅，不是专业审阅。
- 六个仓库已发布到 `paobuorg`，知识站已上线到 `https://learn.paobu.org/`；本仓库不声称内容已通过专业审阅。

## 内容模型

九个主主题固定为：训练方法 `training`、跑步技术 `technique`、恢复与疲劳 `recovery`、营养与补给 `nutrition`、装备选择 `gear`、健康与伤病 `health`、安全与环境 `safety`、习惯与心理 `habits`、跑步文化 `culture`。

每篇正文只有一个主主题，可有多个辅助主题；场景、人群与形式使用独立字段。内容类型为 `concept`、`guide`、`answer`、`plan`、`checklist`、`glossary`、`learning-path`。专题聚合已发布文章，不复制正文。

## 目录

```text
data/entities/{slug}.json          共享事实、主题、类型与来源引用
data/sources/{sourceId}.json       来源、定位与支持的结论
data/contributors/{personId}.json  公开作者与审阅者身份
data/reviews/{slug}.{locale}.json  通过审阅后记录内容摘要与决定
content/zh-CN/{slug}.md            中文正文与 frontmatter
content/en/{slug}.md               英文正文与 frontmatter
assets/                            可复用的小型图片与素材
```

正文是普通 Markdown，不执行脚本，不使用 MDX、内联 HTML 或动态 import。中英文通过 `entityId` 配对，事实字段只保存在 `data/entities/` 一处。

## 写作与审阅

- 每篇先说明读者问题与适用条件，直接给出结论，再展开理由、步骤和例外。
- 数值、效果与因果结论必须有可定位来源；区分研究结论、经验建议与推断，不能编造作者、资质、实测和引用。
- 伤病、慢病、孕产等具体健康建议需要相应专业能力的审校；条件不足时先不发布具体干预建议。
- 状态为 `draft`、`in-review`、`published`、`withdrawn`。发布需要中英文都完成审阅，存在有效 `approve` 记录，且审阅摘要与当前正文一致；格式化、翻译或重建不算复审。
- 一般内容至少由编辑审阅；训练、营养和预测内容还要核对假设与适用范围。

## 本地使用

内容由 `site-knowledge` 构建时读取。六个工程位于同一父目录时路径自动解析；也可用 `KNOWLEDGE_CONTENT_DIR` 覆盖。本仓库没有安装或构建命令。

构建会校验双语配对、主题、来源、许可、审阅日期与内容摘要。搜索索引由网站构建生成，不是第二份正文。

## 许可与纠错

- 新写正文：CC BY 4.0，署名「跑地图 RunMap」。
- 图片与第三方素材：按各自来源条件；没有确认权利的内容不进入仓库。
- 网站代码：MIT，位于三个 `site-*` 仓库。

托管仓库建立后，请通过 Issue 或 Pull Request 指出具体段落、现有来源与建议来源。当前没有公开 Issue 地址，不提供虚构邮箱。贡献流程见 [CONTRIBUTING.md](CONTRIBUTING.md)。

最后核对日期：2026-10-28。
