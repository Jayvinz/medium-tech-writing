# Corpus Norms & Pre-Publish Checklist (Medium Tech Writing)

Quantitative norms from a large corpus of real Medium tech articles
(feature articles and digest issues).

## Feature-article norms

| Dimension | Median | Typical range | Notes |
|---|---|---|---|
| Word count | 1,547 | 800–2,500 | 21/47 land in 1,500–2,500; rarely > 3,300 |
| Paragraphs | 29 | 15–60 | 1–3 sentences each |
| H3 sections | 7 | 4–12 | plus occasional H4 sub-steps |
| Code blocks | 1 | 0–13 | 34 for listicles, 0 for case studies |
| Figures | 5 | 2–12 | hero + result GIF + diagrams |
| Links | 21 | 10–50 | ≈ 2.1 per 100 words |
| List items | 2 | 0–15 | bulleted TOC + feature bullets |
| Blockquotes | 0 | 0–5 | for key rules and deltas |
| Bold runs | 5 | 2–15 | key terms and **Note** leads |

Genre skews:
- Tutorial: 1,200–1,600 words, 5–10 code blocks, 3–6 figures, ends with "Result".
- Listicle: 1,500–2,000 words, 15–35 code blocks, numbered H3s.
- Concept/API: 1,000–1,600 words, 2–8 code blocks, "Under the hood" + FAQ section.
- Migration: 1,500–2,200 words, 8–20 code comparisons, blockquote rules.
- Case study: 1,500–2,700 words, ~0 code, narrative arc, bold sub-labels.
- Announcement: 1,400–2,000 words, "New since alpha:" blockquote deltas.
- Digest: 1,100–2,500 words, 50–270 links, emoji in H3s.

## Voice frequencies (47 features)

- "Let's" 19 · body emojis 15 · thanks-to-reviewers 13 · "**Note**" callouts 12 ·
  recommendation language ("we recommend / recommended way / good practice") 8 ·
  "Check out" 7 · "under the hood" 3 · "In this post you'll learn" 2 ·
  emoji in headings 2 (digests only).

## Structural checklist (run before delivering a draft)

Content
- [ ] One genre selected; skeleton from article-templates.md followed
- [ ] Title matches a formula from titles-and-hooks.md and names the technology
- [ ] Lede ends with an explicit promise/scope line
- [ ] Series banner / Part kicker present if the post belongs to a series
- [ ] Every H3 earns its place (imperative or crisp noun phrase, 2–6 words)
- [ ] Every code block: minimal, commented for rationale, followed by prose walkthrough
- [ ] At least one "Note"-style caveat where behavior can surprise
- [ ] Counter-questions anticipated ("However, if you're not sure about...")
- [ ] Closing: bookend recommendation + next-step CTA + thanks line
- [ ] Resources subsection (Documentation / Videos / Codelabs) if the topic has canonical docs

Form
- [ ] Word count within genre range (±20%)
- [ ] Hero figure first; result GIF/screenshot for tutorials
- [ ] API/class names linked to docs on first mention; ~1 link per 50 words
- [ ] Bold only for key terms/rules/numbers; blockquotes only for portable rules
- [ ] Emojis ≤ 1 per 300 words outside digests; never in formal headings of features
- [ ] Code license note when 3+ code blocks ("The code snippets in this blog have the following license:")
- [ ] Paste-ready Medium structure: title → hero → kicker → lede → H3 sections → close

## Boilerplate awareness

Medium appends "was originally published in ..." cross-post boilerplate automatically — do not
write it. Guest posts add byline ("Posted by X, Role") or "This is a guest post from...". Cross-posts
add "This article is also posted on the [Material Design] blog."
