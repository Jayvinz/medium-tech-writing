# De-AI Flavor Pass (Anti-AI Tells)

Distilled from the humanizer skill (Wikipedia "Signs of AI writing" + 30-LLM linguistic
study), adapted to Medium technical writing. Run this pass on every draft before delivery
(workflow step 6). The corpus norms in `writing-voice.md` win when they conflict with a
generic anti-AI rule: Medium's house style is the writing sample.

## When NOT to strip

These look like tells but are sanctioned publication conventions — keep them:

- `**Note**:` bold-lead callouts, `**Note on testing:**` (corpus convention, §4 of voice rules).
- Bold key terms on first definition ("**StateFlow** is a special kind of **SharedFlow**").
- Signature sign-offs ("happy composing!", "It's a wrap_content!") — deliberate, one per post max.
- Bookend closing that restates the core recommendation (closing menu move #1).
- Collaborative "Let's" for walking through code ("Let's look at some LiveData patterns").
  The tell is the staged opener ("Let's dive in!", "Let's explore!") before a routine point.
- Rhetorical questions opening a listicle tip (corpus pattern in 7 Pro-tips style).
- Emojis where the corpus uses them semantically (🎉 stable release, 🚀 launch, 🙂 aside).
- Humor that costs nothing. Never force a joke to appear human.

## Tells to strip (strongest first)

### 1. Not-X-but-Y contrasts

Cut any contrast where the negative half names something nobody claimed:

- "It's not just about X; it's Y." / "This does not mean X. It means Y." / "X, not Y."
- Split form: "The hard part is never the code. It's finding..." → state the finding directly.
- Clipped tail: "the options come from the item, no guessing" → "...so the user doesn't guess."

Keep a contrast only when the negative half corrects a belief the reader holds
("LiveData is still our solution for Java developers; for the rest, use Flow") or both
halves carry information.

### 2. One-line closers and dramatic fragments

Cut a one-sentence paragraph that restates the paragraph above it: "That's the real win."
"That distinction matters." "Read that again." "It was a lesson in patience."
Also cut fragment rows ("No boilerplate. No reflection. No guesswork.") → merge into a
sentence with a claim. Keep a short line only when it adds a fact the example didn't show.

### 3. Deep-sounding sayings

Replace aphorisms with the specific claim: "the real question is", "at its core",
"X is the Y of Z", "X becomes a trap", "the architecture of trust", "the currency of...".
"Under the hood" is fine as a section name (corpus-sanctioned); "the language of failure" is not.

### 4. Staged run-ups

Delete the announcement, keep the point: "Let's dive in", "Here's what you need to know",
"Without further ado", "Honestly?", "Here's the thing", "The hard part is", "The part that
matters is". "Let's" for code walkthrough stays (see above); "Let's dive into how X works"
before explaining X goes.

### 5. Arguing with no one

Cut defenses against objections nobody raised: "This isn't mainly about...", "I'm not saying...",
"To be clear, don't get me wrong", "One might be tempted to... but". Keep an objection the
text genuinely weighs (e.g. "you might wonder why we need the old API at all?").

### 6. Forced triads

Three parallel items for the sound of completeness: "innovation, inspiration, and insights".
Check each item adds a distinct idea; merge or vary when not. Real lists of three stay.

### 7. Dash habit

The final draft should not lean on em dashes (—) as the universal connector. Replace with
period, comma, colon, or parenthetical. One dash in 1,500 words is fine; one per paragraph
is a tell. Leave dashes in code, paths, URLs, and version ranges (8.0–8.13) alone.

### 8. Inflated significance

Cut the weight, keep the fact: "marking a pivotal moment", "stands as a testament to",
"underscores its importance", "a step in the right direction", "the future looks bright",
stock "Challenges and Legacy / Future Outlook" closers. End on the last concrete fact.

### 9. AI vocabulary

Flag and replace where possible: actually, additionally, crucial, delve/delve into, deep dive
(as filler — fine as a literal section name), enduring, enhance, garner, highlight (v.),
interplay, intricate, key (adj. — fine for the API `key` parameter), landscape (figurative),
meticulous, pivotal, quietly, robust (figurative), showcase, tapestry, testament, underscore (v.),
valuable, vibrant, leverage, seamless, game-changer.

### 10. Sales language

"rich cultural heritage", "nestled in the heart of", "groundbreaking", "renowned",
"breathtaking", "must-visit", "a diverse array of". State what the thing is. Project-promotion
posts may name real advantages ("zero reflection, one `load()` call") — quantify, don't inflate.

### 11. Bold as decoration

Bold carries key terms, key rules, key numbers. Not every list item gets
`- **Label:** content`. If the label adds nothing the content doesn't, drop the bold
and write prose. (Exception: recipe-style checklists where the label IS the item.)

### 12. Chatbot residue

Never: "I hope this helps", "Great question!", "Certainly!", "Would you like me to...",
"let me know if...". Never write about the document ("the figures below show", "this
section covers") unless the signpost genuinely helps navigation (a roadmap sentence in
the lede is corpus style: "Keep reading to know more about X, why Y, and how it compares").

### 13. Knowledge-limit disclaimers

"as of my last update", "details are not widely documented", "it is believed that",
"likely grew up...". State what the source doesn't show or cut the sentence. For real
uncertainty about an API's behavior, use `[TODO: verify]` (hard rule) instead of hedging.

## Pass procedure

1. Read the draft once; mark every hit above, strongest patterns first.
2. Rewrite at paragraph level. Every kept sentence must add something the reader doesn't
   already have from earlier in the text. Vary sentence length.
3. Verify no fact, name, number, version, or claim was dropped or altered in the rewrite
   (esp. after cutting triads, closers, and qualifiers).
4. Check the survivors that most often escape a rewrite: §1 contrasts, §2 closers,
   §6 triads, §7 dashes, §11 bold labels.
5. Compare against corpus norms one last time: a stripped tell must not have removed a
   sanctioned convention (Note callouts, bookend, "Let's" walkthroughs, honest scoping).
