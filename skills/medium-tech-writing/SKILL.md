---
name: medium-tech-writing
description: "Medium 技术写作技能，模式提炼自大量真实英文技术出版物文章。当需要撰写、改写或评审面向 Medium 平台的技术文章/博客（教程、API 概念讲解、迁移指南、案例分析、版本公告、系列 wrap-up、技术周刊）时使用本技能；产出符合主流技术出版物风格的英文技术长文，含标题公式、开篇 hook、分节结构、代码呈现规范、配图建议、结尾 CTA、发布前检查清单与去 AI 味质检（not-X-but-Y 对比句、排比三连、破折号滥用、夸张措辞、装饰性加粗等 AI 腔清除）。触发词：Medium 文章、技术博客、写一篇 blog、tech writing、Medium 风格、英文技术文章、technical article、去 AI 味。不适用于：中文公众号排版、纯文档/API reference。"
agent_created: true
---

# Medium Tech Writing

Produce publication-grade Medium technical articles modeled on leading technical
publications on Medium (evidence base: a large analyzed article corpus; norms in `references/corpus-stats.md`).

## Workflow

1. **Identify the genre** from the request — tutorial / listicle / concept explainer / migration /
   case study / announcement / wrap-up-or-digest. When ambiguous, pick the closest and state the
   choice in one line before drafting.
2. **Load the matching skeleton** from `references/article-templates.md`. Build the section outline
   (H3 list) first; do not draft prose before the outline exists.
3. **Draft the title and lede** using the formulas in `references/titles-and-hooks.md`
   (title formula → lede pattern A–F → explicit promise/scope line at the end of the lede).
4. **Draft section by section**, applying `references/writing-voice.md`:
   short paragraphs, "we"/"you"/"Let's" voice, anticipate reader doubts, code-with-walkthrough,
   **Note** callouts, honest scoping. Keep code minimal and rationale-commented.
5. **Close** with 2–3 moves from the closing menu (bookend recommendation, next-step CTA,
   thanks-to-reviewers, optional signature sign-off). Add a Resources subsection when canonical
   docs/codelabs exist. Add a code-license note when 3+ code blocks are present.
6. **Run the pre-publish checklist** in `references/corpus-stats.md` against the draft and fix
   gaps before presenting the article.
7. **Run the de-AI flavor pass** in `references/de-ai-flavor.md` on the prose: strip not-X-but-Y
   contrasts, staged run-ups, one-line closers, forced triads, dash habit, inflated significance,
   AI vocabulary, decorative bold, and chatbot residue. Verify the pass did not strip corpus-
   sanctioned conventions (Note callouts, bookend closings, "Let's" code walkthroughs).

## Reference map

| File | Load when |
|---|---|
| `references/article-templates.md` | choosing structure (step 1–2) |
| `references/titles-and-hooks.md` | writing title, kicker, lede (step 3) |
| `references/writing-voice.md` | drafting or revising prose (step 4–5) |
| `references/corpus-stats.md` | checking length ratios & final QC (step 6) |
| `references/de-ai-flavor.md` | de-AI pass on any draft or rewrite (step 7) |

## Hard rules

- Default output language: English (the publication language). Switch only on request.
- Never fabricate benchmarks, version numbers, or API names — leave `[TODO: verify]` markers
  instead of inventing facts.
- Match length to genre norms (median ≈ 1,550 words; typical 800–2,500).
- Keep Medium's heading convention: single H1 title, H3 for sections, H4 for sub-steps.
- Do not write Medium's auto-appended boilerplate ("was originally published in...").
- Every delivered draft must pass the de-AI flavor pass (`references/de-ai-flavor.md`);
  corpus-sanctioned conventions (Note callouts, bookend, "Let's" walkthroughs) survive it.
