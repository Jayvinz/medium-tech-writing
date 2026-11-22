# Titles, Kickers & Hooks (Medium Tech Writing)

Title evidence: 47 feature titles from leading Medium tech publications.

## 1. Title formulas (choose one, keep ≤ 70 characters when possible)

1. **Verb-first imperative** (12/47) — name the outcome the reader will achieve:
   "Create a spotlight effect with CameraX and Jetpack Compose" · "Make WebViews edge-to-edge" ·
   "Adopt Compose for View-based libraries" · "Preview and test your app's edge-to-edge UI" ·
   "Consuming flows safely in Jetpack Compose" (gerund variant).
2. **X with Y** (11/47) — topic + tooling: "Dark Theme with MDC" · "Dependency Injection in Compose" ·
   "Improving App Performance with Baseline Profiles".
3. **Colon split: hook : scope** (9/47) — vivid left, technical right:
   "Tap to focus: Mastering CameraX Transformations in Jetpack Compose" ·
   "Test smarter, not harder: new testing strategies documentation" ·
   "Material Theming with MDC: Color".
4. **Numbered listicle**: "7 Pro-tips for Room" — numeral + "Pro-tips/things/ways" + "for X".
5. **Migrating from X to Y / Migrating X**: "Migrating from LiveData to Kotlin's Flow" ·
   "Migrating Architecture Blueprints to Jetpack Compose".
6. **How + actor + outcome** (case studies): "How Dropbox leverages testing to maintain high level of
   trust at scale" · "How Mobile Apps are Helping With Workplace Safety".
7. **Result-with-number** (case studies): "Turo reduced its app startup time by 77% using Android
   Developer tools and best practices".
8. **What's new in X — edition**: "What's new in Jetpack Benchmark 1.2.0" ·
   "What's new in Android Performance — Google I/O 2023 edition".
9. **Getting Started with X**: "Getting Started with CameraX in Jetpack Compose".
10. **Question-as-title** for concept posts: "Density, Devices and Flaky Tests" (topic triple) —
    noun phrases fine when the topic is the draw.

Avoid: clickbait, "The Ultimate Guide", exclamation-mark titles, titles that don't name the
technology. The publication states the technology in the title almost always.

## 2. Kicker (H4 right under the hero)

- Series position: `Part 1 of Unlocking the Power of CameraX in Jetpack Compose`.
- Digest teaser: linked topic phrases separated by semicolons ending in "and [much], [much] more."

## 3. Lede patterns (first 1–3 paragraphs)

**A. Recommendation-first** (concept/API posts):
> "Collecting flows in a lifecycle-aware manner is the recommended way to collect flows on Android.
> If you're building an Android app with Jetpack Compose, use the collectAsStateWithLifecycle API..."
Then: "Keep reading to know more about this API, why you should collect in a lifecycle-aware manner,
and how it compares to the collectAsState API." (the roadmap sentence)

**B. News-first** (announcements):
> "With the latest release of Jetpack Navigation 2.8.0, the type safe navigation APIs for building
> navigation graphs in Kotlin are stable 🎉. This means that you can define your destinations using
> serializable types and benefit from compile-time safety."
Then scope: "This article covers the stable API and points out changes since the first alpha release.
It also looks at how to migrate existing code and provides some tips on testing..."

**C. History-first** (migrations):
> "**LiveData** was something we needed back in 2017. The observer pattern made our lives easier,
> but options such as RxJava were too complex for beginners at the time."
Then the verdict, honestly scoped, then the promise: "In this post you'll learn how to expose Flows
to a view, how to collect them, and how to fine-tune it to fit specific needs."

**D. Stakes-first** (case studies):
> "With more than one billion downloads, the Dropbox app for Android has to maintain a high quality
> bar... With less than 30 Android engineers, manual testing and #yolo isn't enough..."
Then what the guest will share ("I'd like to share some ways that our testing strategies have changed").

**E. Reader-demand-first** (tutorials):
> "We've heard from you that you love the power that both the CameraX and Jetpack Compose libraries
> give you, but that you'd like idiomatic Compose APIs for building Camera UIs."
Then: "In this blog post series, we'll show you how to integrate... But more excitingly, we'll show
you some of the ✨ delightful UI experiences..."

**F. Series-banner-first** (any post in a spotlight/series): open with 1–2 italic sentences:
> "*This blog post is a part of Camera and Media Spotlight Week. We're providing resources — blog
> posts, videos, sample code, and more — all designed to help you uplevel the media experiences in
> your app.*"

Always end the lede block with a **promise/scope line** naming what the reader will learn or build.

## 4. Section-heading craft

- Main sections: H3, 2–6 words, imperative or noun-phrase:
  "Add the library dependencies" · "Read only what you need" · "Passing data between destinations" ·
  "Under the hood" · "Keeping resources active in the background".
- Numbered sections for listicles: `### 1. Pre-populate the database`.
- Sub-patterns inside a section: H4 with `#1: <pattern name>` style
  ("#### #1: Expose the result of a one-shot operation with a Mutable data holder").
- Playful closers allowed as final H3: "OK Google, what's next?" · "Keep on moving!" ·
  "It's a wrap_content!" · "DeadData?" · "Hey, I was using that API! Where'd it go?".

## 5. Title checklist

- [ ] Names the concrete technology (Compose, Room, CameraX, ...)
- [ ] States the outcome or question, not just the topic
- [ ] No "Ultimate/Complete Guide", no ALL CAPS, no clickbait
- [ ] Colon split only when both halves carry weight
- [ ] Numbers in listicle titles match the number of sections
