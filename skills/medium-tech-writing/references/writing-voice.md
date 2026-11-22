# Voice & Craft Rules (Medium Tech Writing)

Evidence base: a large corpus of real Medium tech articles. Frequencies noted as n/47 feature articles.

## 1. Point of view & person

- Default voice: first-person plural "we" for the engineering team ("we've heard from you",
  "our engineering teams worked on..."), second person "you" for the reader's code and choices.
- Guest/case-study posts use first-person singular "I" ("In this post, I wanted to show you how I
  looked into a performance issue").
- Collaborative "Let's" appears in 19/47 articles — use it to co-move through code ("Let's look at
  some LiveData patterns", "Let's say we have an app which displays products"). Never overuse it.
- Address the reader as a competent peer. Ask rhetorical questions to open listicle sections
  ("Do you need to add default data to your database...?"), not to pad.

## 2. Sentence & paragraph rhythm

- Short paragraphs (1–3 sentences). One idea per paragraph.
- Present tense, active voice. Prefer "Room generates their implementation at compile time" over
  "the implementation is generated".
- Technical precision with plain framing: define the term once, bold it on first key use
  ("**StateFlow** is a special kind of **SharedFlow**... It always has a value. It only has one value.").
- Punchy parallel fragments for API properties (see above: four one-line sentences, not one long one).
- Humor is allowed and welcome when it costs nothing: "(and because I like living on the edge 😀)",
  "Why, you say? I'm not sure. But it sure looks cool 🙂.", "It's a wrap_content!". Never force a joke.

## 3. Anticipate the reader's doubts

The single strongest pattern in the corpus. When giving a recommendation, immediately voice the
counter-question and answer it:
- "However, if you're not sure about that seemingly random 5-second started parameter, read on."
- "You might want to use the @Transaction annotation for @Query methods... in the following cases:"
- "Developers often ask: if X is the safest way... why do we need the Y API at all?"
- Offer a pragmatic copy-paste escape hatch before the deep dive: "If you don't want to go into
  detail right now and just need to copy-paste, this combination is what I recommend."

## 4. Code presentation

- Code blocks are the payload of tutorial/listicle genres (median 4 blocks; listicles run 15–35).
  Concept posts use fewer (0–8); case studies often none.
- Show minimal compilable snippets, not whole files. Split long listings into consecutive blocks.
- Comment code for rationale and landmines, not for narration:
  `// moving to a new thread`, `// Cancellation signals we're done with the camera`,
  `// Call before the DecorView is accessed in setContentView`.
- After each non-trivial block, walk through it in prose: what it defines, why each piece exists
  ("There's quite a bit going on here! The code defines... The bindToCamera function initializes...").
- Call out edge cases with bold-lead notes right after the code:
  `**Note**: When using the ioThread approach, if your app crashes at the first launch, ...`
  `**Note on testing:** As of release 2.8.0, SavedStateHandle.toRoute is dependent on Android Bundle.`
- Old-vs-new comparisons: show both sides, or two numbered options ("Option 1: Idling Resources",
  "Option 2: Waiting for things… the wrong way", "Option 3: Waiting for things the right way!").
- End of post: code license line when snippets are substantial
  ("The code snippets in this blog have the following license:" + `// Copyright 2024 Google LLC.
  SPDX-License-Identifier: Apache-2.0`).

## 5. Figures & media

- Median 5 figures per feature. Hero figure first (often a themed illustration or result GIF).
- GIFs for anything motion-related: final app demo, before/after scrolling, gesture feedback.
- Architecture diagrams for concept posts (layers, arrows between UI/ViewModel/data).
- Screenshots with captions for UI steps; link the source under borrowed photos.
- Tutorials open with "our final app will look as follows:" + GIF — sell the destination before the hike.

## 6. Links

- ~2.1 links per 100 words (median 21 links per feature). Link every external API/class name on
  first mention to its docs. Link "see more details here", "full example here", related articles,
  codelabs, talks. Ending "Resources" section groups links under Documentation / Videos / Codelabs.

## 7. Emphasis & callouts

- Bold = key terms, key rules, key numbers ("use **StateFlow**", "**Note**:", "80% test coverage").
- Blockquotes = portable recommendations or deltas:
  "> When exposing UI state to a view, use **StateFlow**. It's a safe and efficient observer..."
  "> **New since alpha:** Nullable types are supported."
- Italic = series banners, meta-comments, gentle asides.
- Emojis sparingly and semantically: 🎉 for stable releases, 🚀 for launches, ✨ for delightful UI,
  🙂/😀 for human asides, numbered-part bullets (🧱 👆 🔎 📂). Headings carry emoji only in
  digest posts (2/47 features vs most digest items).

## 8. Opening & closing moves

Openings (pick one; see titles-and-hooks.md for formulas):
- Recommendation-first: "Collecting flows in a lifecycle-aware manner is the recommended way..."
- News-first: "With the latest release of Jetpack Navigation 2.8.0, the type safe navigation APIs... are stable 🎉."
- History-first: "**LiveData** was something we needed back in 2017."
- Stakes-first: "With more than one billion downloads, the Dropbox app for Android has to maintain..."
- Series-banner first (italic) when part of a spotlight/series.

Closings (combine 2–3):
- Bookend: restate the core recommendation verbatim ("Collecting flows in a lifecycle-aware manner
  is the recommended way... If you're building an Android app with Jetpack Compose, use...").
- Next-step CTA: "Want more? See our codelab...", "Stay tuned!", "Check out [X] to get caught up."
- Community CTA (~22/47): "leave a comment below or reach out to us on Twitter @YourTeamHandle".
- Signature sign-off: "happy composing!", "It's a wrap_content!", "OK Google, what's next?".
- Credits: italic thanks-to-reviewers with linked names ("Many thanks to [X], [Y]... for reviewing").
- "P.S. Thanks to [...] for reviewing this article."

## 9. Recurring section names (reuse verbatim where natural)

The basics · Overview · Summary · Conclusion · Result · Under the hood · What's next ·
Next steps · Resources · Quick start · Why it matters / Why support X? ·
How it started / How it's going / Looking forward ·
(FAQ-ish) "<API> comparison" / "Alternatives to X" · "Need more time to migrate?"

## 10. Honesty rules (publication-grade)

- Scope recommendations precisely ("LiveData is still our solution for Java developers, beginners,
  and simple situations").
- Admit trade-offs ("Flows still have a steep learning curve").
- Mark experimental/alpha APIs explicitly with the version that stabilizes them.
- Never invent benchmarks; quote the stated numbers ("about 30%", "77%") and attribute them.
