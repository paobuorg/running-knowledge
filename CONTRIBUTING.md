# 贡献说明

本仓库只接收知识正文、来源、作者与审阅数据。网站代码、工具实现和设计资源分别在 `site-www`、`site-knowledge` 与 `site-tools`。

## 提交前

1. 确认 `entityId` 与 `slug` 唯一，文章只属于一个主主题；辅助主题、人群与场景放在对应字段，不塞进标题。
2. 先写清读者问题与适用条件，再给结论、依据、步骤和例外。不要把多个主题拼成没有主线的长文。
3. 为事实、数值、健康建议和因果表述记录 `sourceId`、URL 或 DOI、定位段与支持的结论。研究结论、经验建议和个人推断要分开写。
4. 中英文分别成稿，不把机器翻译直接当英文成稿；两种语言的事实、数值与限制条件必须一致。
5. 不编造作者、资质、实测、审阅者或引用。伤病、慢病、孕产等具体干预建议需要相应专业审阅；没有审阅能力时保留为草稿。
6. 图片、图表和引用片段只使用权利明确且允许再分发的材料，按来源要求署名。

## 审阅与状态

状态为 `draft`、`in-review`、`published`、`withdrawn`。新内容从 `draft` 开始，完成双语、来源与许可检查后进入 `in-review`。`published` 需要两种语言都有作者与审阅者，并存在 `approve` 审阅记录；审阅记录的内容摘要必须与当前正文一致。`reviewedAt` 不能由格式化、翻译或重建自动填写，正文改变后必须重新审阅。

## 校验

在 `site-knowledge` 运行内容校验和构建。校验器会检查双语配对、主题、内容类型、来源引用、许可、审阅日期与内容摘要。失败时修正内容，不绕过检查。

## 措辞与礼貌

- 先说明证据强度和适用范围，不用「一定」「治愈」「保证」等表述替代依据。
- 纠错请指出具体段落、现有来源和建议来源；没有公开 Issue 地址时，不虚构邮箱或联系人。
- 不把其他网站的长段正文改写后当作独立写作；可以引用并链接，但要有自己的组织与结论。

---

# Contributing

This repository accepts knowledge articles, sources, author and review data only. Site code, tool implementations and design assets live in `site-www`, `site-knowledge` and `site-tools`.

Before submitting, check that the `entityId` and slug are unique and that the article has one primary topic. State the reader's problem and conditions first, then the conclusion, evidence, steps and exceptions. Record a `sourceId`, URL or DOI, location and supported claim for every factual, numerical or health-related statement, and keep research findings separate from practical advice and inference.

Write both languages independently rather than treating machine translation as the English draft. Do not invent authors, qualifications, tests, reviewers or citations. Specific advice on injury, chronic disease or pregnancy needs a reviewer with the relevant professional competence; without one, keep the article as a draft.

New entities start as `draft`, move to `in-review` after bilingual, source and rights checks, and to `published` only with authors, reviewers and an `approve` review record in both languages whose content digest matches the current text. Run the `site-knowledge` content validation and build after changes, and do not bypass a failed check. Report corrections with the paragraph, existing source and proposed source; no public issue URL or email address exists yet.
