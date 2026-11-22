# medium-tech-writing

An AI-agent skill that writes publication-grade Medium technical articles in the style of leading
tech publications. It carries writing norms distilled from a large corpus of real articles, plus a built-in
de-AI flavor pass so the output reads like a human author rather than a language model.

中文说明见 [README.zh-CN.md](README.zh-CN.md).

## What you get

One skill, seven article genres: tutorial, listicle (pro-tips), concept explainer, migration guide,
case study, release announcement, and series wrap-up. For each genre the skill knows the section
skeleton, title formulas, lede patterns, code-presentation rules, closing moves, and a pre-publish
checklist with real corpus statistics behind every rule.

The de-AI pass is part of the workflow, not an afterthought. It strips the tells that give generated
prose away: "not X but Y" contrast sentences, staged run-ups, one-line dramatic closers, forced
triads, dash habits, inflated significance, AI vocabulary, and decorative bold. Where the de-AI
rules and the publication conventions disagree, the publication conventions win, so callouts like
**Note** and bookend closings survive the pass.

## Install

### One-click install for AI agents

Copy the block below and paste it to your AI agent (any agent that can clone a repository and
copy files). The instruction is agent-agnostic:

> Please install the medium-tech-writing skill for me: clone the repository
> https://github.com/Jayvinz/medium-tech-writing and copy the `skills/medium-tech-writing/`
> folder into the directory where this agent loads user-level `SKILL.md`-format skills
> (create parent directories if missing). When done, confirm that SKILL.md exists at the
> installed path and report the path back to me.

### Manual install

```bash
git clone https://github.com/Jayvinz/medium-tech-writing.git
cp -r medium-tech-writing/skills/medium-tech-writing <your-agent-skills-dir>/
```

Windows (PowerShell):

```powershell
git clone https://github.com/Jayvinz/medium-tech-writing.git
Copy-Item -Recurse medium-tech-writing\skills\medium-tech-writing <your-agent-skills-dir>\
```

`<your-agent-skills-dir>` is the folder your agent scans for `SKILL.md`-format skills. If you are
not sure where that is, ask your agent: "which directory do you load skills from?"

Install locations:

| Scope | Where | When to use |
|---|---|---|
| User-level | the agent's user-level skills directory | default; available in every project |
| Project-level | the workspace's project skills directory | share with teammates via the repo |

### Verify the install

Ask your agent something like:

> Use medium-tech-writing to outline a tutorial about Gradle configuration cache.

If the skill is wired up, the agent answers with a genre pick and a section outline before drafting
prose. You can also just say "Write a Medium-style post about X" and the trigger words pick it up.

## Getting started

Four things the skill does well. Mix and match.

**1. Write an article from a topic.**

> Use medium-tech-writing to write a tutorial on migrating Android views to Jetpack Compose.
> Audience: intermediate Android developers.

The skill picks the genre (migration), loads the skeleton, drafts title and lede first, then writes
section by section. Output defaults to English; ask for Chinese if you need it.

**2. Rewrite an existing draft into Medium style.**

> Here is my draft (below). Rewrite it as a Medium tutorial using medium-tech-writing.

Structure, titles, and pacing get reworked to publication norms. Facts stay yours; the skill never
invents benchmarks, version numbers, or API names, and marks gaps with `[TODO: verify]` instead.

**3. De-AI a draft that already exists.**

> Run the medium-tech-writing de-AI pass on this draft without changing its structure.

Useful when the content is right but the prose rings generated. The pass reports what it changed.

**4. Check a draft against the checklist.**

> Review this article against the medium-tech-writing pre-publish checklist.

Returns concrete gaps: length against genre median, heading shape, code-to-prose ratio, missing
Note callouts, weak closing moves, and leftover AI tells.

## How the skill works

Seven steps, each backed by a reference file the skill loads on demand:

1. Identify the genre (tutorial / listicle / explainer / migration / case study / announcement / wrap-up).
2. Load the matching skeleton and build the H3 outline before drafting.
3. Draft title and lede from corpus formulas, ending the lede with an explicit promise line.
4. Draft section by section in the publication voice: short paragraphs, "we/you/Let's", anticipated
   reader doubts, code blocks with walkthroughs, **Note** callouts, honest scoping.
5. Close with two or three moves from the closing menu: bookend recommendation, next-step CTA,
   reviewer thanks, optional signature sign-off.
6. Run the pre-publish checklist against the draft and fix gaps.
7. Run the de-AI flavor pass, then confirm it did not strip sanctioned conventions.

Reference map inside the skill:

| File | Covers |
|---|---|
| `references/article-templates.md` | seven genre skeletons |
| `references/titles-and-hooks.md` | title formulas and lede patterns |
| `references/writing-voice.md` | tone, code presentation, figure guidance |
| `references/corpus-stats.md` | measured norms and the pre-publish checklist |
| `references/de-ai-flavor.md` | the de-AI rules, keep-list, and audit procedure |

## Repo layout

```
medium-tech-writing/
├── README.md                 ← this file
├── README.zh-CN.md           ← Chinese README
├── LICENSE                   ← MIT
└── skills/
    └── medium-tech-writing/  ← the installable skill
        ├── SKILL.md
        └── references/
            ├── article-templates.md
            ├── titles-and-hooks.md
            ├── writing-voice.md
            ├── corpus-stats.md
            └── de-ai-flavor.md
```

The `skills/` layout follows the common convention used by multi-skill repositories, so this repo
can host companion skills later without breaking install scripts.

## Requirements

- An AI agent that loads `SKILL.md`-format skills and can read the bundled `references/` files.
- No runtime dependencies. The skill is pure instructions and reference material.

**Note**: the writing norms target Medium's English-language technical publications. The skill
switches output language on request, and the de-AI pass works on Chinese drafts too, but the genre
skeletons and title formulas were measured from English articles.

## License

MIT. See [LICENSE](LICENSE).
