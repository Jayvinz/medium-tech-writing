# Article Genre Templates (Medium Tech Writing)

Distilled from a large corpus of real Medium tech articles (feature articles and digest issues).
Pick ONE genre before drafting; the structure of the article follows from it.

All section headers below map to Medium's heading levels: the article title is the only H1;
use H3 for main sections; use H4 for sub-steps or numbered patterns inside a section.

---

## 1. Hands-on Tutorial (step-by-step build)

Canonical examples: "Getting Started with CameraX in Jetpack Compose", "Tap to focus: Mastering
CameraX Transformations in Jetpack Compose", "Create a spotlight effect with CameraX and Jetpack Compose".

Skeleton:
1. Hero figure (screenshot or GIF of the final result).
2. Optional H4 kicker: `Part N of <Series Name>`.
3. Optional italic series banner (2 sentences): what the spotlight/series is + link to overview post.
4. Lede (1–2 paragraphs): what the reader will build and why it matters; end with an explicit promise
   ("By the end of this first post, you'll have a functional camera viewfinder...").
5. Series roadmap list (only in Part 1): bullet per part, emoji prefix (e.g. 🧱 👆 🔎 📂), bold
   `**Part 1 (this post):**`, later parts linked.
6. One H3 per build step, named as imperative verbs: "Add the library dependencies", "Grant camera
   permissions", "Create a ViewModel", "Implement the camera preview UI".
   Per step: 1 short rationale paragraph → code block (with inline comments explaining WHY, not WHAT)
   → 1–2 paragraphs walking through the code ("There's quite a bit going on here!") → optional figure
   showing the intermediate result.
7. H3 "Result": show the working outcome (GIF/screenshot), link to full source ("You can find the full
   code snippet here"), tease the next part ("Stay tuned!").
8. Closing block: code license note (`The code snippets in this blog have the following license:` +
   one-line SPDX comment), italic thanks-to-reviewers line with linked names.

Ratio targets: 1,200–1,600 words · 5–10 code blocks · 3–6 figures · 5–9 H3 sections.

## 2. Listicle / Pro-tips

Canonical example: "7 Pro-tips for Room".

Skeleton:
1. Hero figure.
2. Lede: 1–2 sentences defining the technology + link to a primer article for newcomers.
3. Promise line + bulleted TOC of every tip, linking API names inline
   ("In this article, I'd like to share some pro-tips on getting the most out of Room:").
4. One H3 per tip, numbered and imperative: `### 1. Pre-populate the database`, `### 2. Use DAO's
   inheritance capability`. Each tip:
   - Open with a rhetorical question or a concrete pain ("Do you need to add default data...?",
     "Do you have multiple tables... and find yourself copying the same methods?").
   - Instruction in 1–3 sentences, key APIs linked.
   - Code block (minimal reproducible snippet).
   - Payoff sentence ("See a full example here." / "This will also improve the speed of your queries").
   - Optional bold-lead callout: `**Note**: ...` for caveats and edge cases.
5. Related-reading list ("New to X? Check out our previous articles:").
6. Code license note + publication boilerplate.

Ratio targets: 1,500–2,000 words · 15–35 code blocks · 1–3 figures · 6–10 H3 sections.

## 3. Concept / API Explainer

Canonical examples: "Consuming flows safely in Jetpack Compose", "Dependency Injection in Compose",
"New ways of optimizing stability in Jetpack Compose".

Skeleton:
1. Hero figure (architecture diagram or conceptual illustration).
2. Lede: state the recommendation up front in one sentence ("use the collectAsStateWithLifecycle API..."),
   then 1 paragraph of why + 1 signpost sentence ("Keep reading to know more about this API, why you
   should... and how it compares to X").
3. H3 named after the API or concept itself → definition paragraph ("X is a composable function that...
   ") → parameters/behavior explained → minimal code.
4. H3 "Under the hood": how it works internally; contrast with the boilerplate it replaces.
5. H3 for architectural context ("Flow collection in your architecture"): where it fits, what layers
   should/shouldn't know.
6. H3 FAQ/comparison ("collectAsState comparison"): voice the question developers actually ask
   ("Developers often ask: ... why do we need the old API at all?"), then answer with platform reasoning.
7. Close by restating the recommendation verbatim (bookend), then P.S. thanks-to-reviewers.

Ratio targets: 1,000–1,600 words · 2–8 code blocks · 2–5 figures · 4–7 H3 sections.

## 4. Migration / Comparison Guide

Canonical example: "Migrating from LiveData to Kotlin's Flow".

Skeleton:
1. Hero figure.
2. Historical-context lede: why the old thing existed ("LiveData was something we needed back in 2017...")
   → what changed → the verdict, honestly scoped ("LiveData is still our solution for Java developers,
   beginners, and simple situations. For the rest...").
3. Playful transition H3 ("DeadData?").
4. Promise line ("In this post you'll learn how to expose Flows to a view, how to collect them, and how
   to fine-tune it...").
5. Pattern-by-pattern comparison, one H4 per pattern: `#1: Expose the result of a one-shot operation...`
   Show OLD way (code/GIF) → NEW way (code/GIF) → 1–2 sentences of trade-off commentary.
   Quote key rules in blockquotes: "> When exposing UI state to a view, use **StateFlow**."
6. Deep-dive H3 for the tricky configuration ("Configuring the exposed StateFlow (stateIn operator)"):
   give a copy-paste default first ("If you don't want to go into detail right now and just need to
   copy-paste, this combination is what I recommend"), then unpack parameters for the curious
   ("However, if you're not sure about that seemingly random 5-second started parameter, read on.").
7. H3 "Summary" with a decision table or bullet recap.

Ratio targets: 1,500–2,200 words · 8–20 code blocks (often as GIF/code embeds) · 8–12 figures.

## 5. Case Study (guest/team story)

Canonical examples: "How Dropbox leverages testing...", "Netflix App Testing At Scale",
"Turo reduced its app startup time by 77%...".

Skeleton:
1. Hero figure.
2. Italic series banner: "This is part N of the [X] series... In this article, [Name], [Role] at [Company],
   shares how..."
3. Stakes lede with concrete numbers ("With more than one billion downloads... With less than 30 Android
   engineers, manual testing and #yolo isn't enough...").
4. Narrative arc H3s: "How it started" → "How it's going" → "Looking forward". Inside sections, use
   bold sub-labels (**Unit testing**, **E2E testing**, **Screenshot testing**, **Manual testing**).
5. Honest tension: name failures and dead ends ("engineers feeling incentivised to remove failing tests
   instead of updating them"). Quantify outcomes ("reduced its app startup time by 77%").
6. Close with future outlook and the trust/quality theme; no code license block (guest prose).

Ratio targets: 1,500–2,700 words · 0–5 code blocks · 2–7 figures.

## 6. Announcement / What's New

Canonical examples: "Type safe navigation for Compose", "What's new in Jetpack Benchmark 1.2.0",
"What's new in Android Performance — Google I/O 2023 edition".

Skeleton:
1. Hero figure.
2. News lede: "With the latest release of [X a.b.c], the [Y] APIs ... are stable 🎉." + what it means
   for the reader + scope statement ("This article covers the stable API and points out changes since
   the first alpha release. It also looks at how to migrate...").
3. H3 "The basics": minimum setup (dependency + plugin), smallest possible example, nomenclature
   ("Nomenclature is important here... Any method that accepts a route now accepts a generic type.").
4. Feature sections, each with code + a running mini-story ("Let's say we have an app which displays
   products...").
5. Delta callouts as blockquotes for returning readers: "> **New since alpha:** Nullable types are
   supported." / "> **New since alpha**: Enums are supported (although...)".
6. Bold-lead caveat: `**Note on testing:** ...` with links to tracking bugs.
7. H3 "Next steps" / "Resources".

Ratio targets: 1,400–2,000 words · 5–25 code blocks · 2–6 figures.

## 7. Series Wrap-up / Digest

Canonical examples: "MAD Skills Performance — Wrap Up", "MAD Skills Material Design Components: Wrap-Up",
"Now in Android #N".

Wrap-up skeleton:
1. One-paragraph look-back ("Here's the gist of what happened.") → H3 per episode with 1-line summary
   and link → "What to do now" CTA section. Signature closer: "It's a wrap_content!" or "happy composing!"

Digest skeleton (Now in Android):
1. Hero figure + H4 teaser line made of linked topic phrases separated by semicolons.
2. Standing welcome ("Welcome to Now in Android, your ongoing guide to what's new and notable...").
3. Optional YouTube embed ("You can catch a short subset ... on YouTube, but read on for the full story.").
4. One H3 per news item, heading itself a linked headline ending in 🚀/👓; body = 1–3 paragraph summary
   with bold-keyed bullets; each item ends with "Check out [related video/post]".

Ratio targets: wrap-up 600–800 words · digest 1,100–2,500 words, heavy linking (50–270 links).
