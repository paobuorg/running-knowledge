# RunMap · Running knowledge

[中文](README.md) · English

This repository holds the evergreen running knowledge, bilingual articles, sources and review data used by `learn.paobu.org`. It is a content-only repository: it contains no site runtime code, `package.json`, `node_modules` or build output.

## Status

- Fifty articles cover all nine topics: training, technique, recovery, nutrition, gear, health, safety, habits and culture. Each has complete Chinese and English text. A glossary adds a fifty-first knowledge entity, and the site provides five learning paths.
- All fifty-one knowledge entities were **AI-assisted editorially reviewed** and published on 2026-10-28 (`published`, with bilingual `approve` records and matching digests): fifty articles plus one glossary. The reviewer is `runmap-editorial`, explicitly AI-assisted, not independent professional medical/nutrition review. All nine topics are covered.
- The only author/review identity is `runmap-editorial`, shown as “RunMap editorial desk (AI-assisted draft and review)”. There is no personal qualification claim; the approval is an AI-assisted editorial review, not professional review.
- The six repositories are published under `paobuorg`, and the knowledge site is live at `https://learn.paobu.org/`. This repository does not claim professional review.

## Content model

Nine primary topics are fixed: training, technique, recovery, nutrition, gear, health, safety, habits and culture. Every article has exactly one primary topic and may have several secondary topics; audience, scenario and content format are separate fields. Content types are `concept`, `guide`, `answer`, `plan`, `checklist`, `glossary` and `learning-path`. A learning path aggregates published articles and does not copy their bodies.

## Layout

```text
data/entities/{slug}.json          Shared facts, topics, content type and source refs
data/sources/{sourceId}.json       Sources, locations and the claims they support
data/contributors/{personId}.json  Public author and reviewer identities
data/reviews/{slug}.{locale}.json  Content digest and decision after review
content/zh-CN/{slug}.md            Chinese article and frontmatter
content/en/{slug}.md               English article and frontmatter
assets/                            Small reusable images and material
```

Articles are plain Markdown. They do not execute scripts and do not use MDX, inline HTML or dynamic imports. The two languages are paired by `entityId`, and shared facts live only in `data/entities/`.

## Writing and review

- State the reader's problem and the conditions that apply, give the conclusion first, then explain the reasoning, steps and exceptions.
- Every number, effect claim and causal claim needs a locatable source. Separate research findings, practical advice and inference. Never invent authors, qualifications, tests or citations.
- Health advice about injury, chronic disease or pregnancy needs a reviewer with the relevant professional competence. If that is unavailable, do not publish specific intervention advice.
- Statuses are `draft`, `in-review`, `published` and `withdrawn`. Publication requires review in both languages, a valid `approve` record, and a review digest that matches the current text. Formatting, translation or a rebuild never counts as re-review.
- General content needs at least an editorial review; training, nutrition and prediction content also needs its assumptions and scope checked.

## Local use

The content is read by `site-knowledge` at build time. When the six projects sit in the same parent directory, the build finds this repository automatically; `KNOWLEDGE_CONTENT_DIR` can override the path, and `PAOBU_REPOS_DIR` can relocate the parent directory. This repository has no install or build command of its own.

The build validates bilingual pairing, topics, sources, licences, review dates and content digests. The search index is produced by the site build and is not a second copy of the articles.

## Licence and corrections

- New article text: CC BY 4.0, attributed to “RunMap 跑地图”.
- Images and third-party material: under each source's terms; material without confirmed rights does not enter the repository.
- Site code: MIT, in the three `site-*` repositories.

Once the repository is hosted, report factual or source problems through an issue or pull request that names the paragraph, the existing source and a proposed source. No public issue URL or email address exists yet, and none is invented here. See [CONTRIBUTING.md](CONTRIBUTING.md), whose second half is in English.

Last checked: 2026-10-28.
