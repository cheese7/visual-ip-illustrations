# Mobile Reading Contract

Use this shared contract for every visual-IP route. It supplements, but never overrides, the selected route's identity, style, attribution, safety, and output-path rules.

Its 9:16 vertical portrait and information-rich infographic requirements override legacy 16:9, horizontal, sparse-label, excessive-text, or anti-infographic wording in route-local prompt templates, QA files, source records, and example assets. Those legacy references remain useful for character and line-style calibration, but not for the output aspect ratio or information-density decision.

## Phone-First Canvas

- Generate every new illustration on a 9:16 vertical canvas, optimized for a phone held upright.
- Compose from top to bottom: use the upper area for a short setup when needed, keep the character's core action in the central vertical band, and reserve the lower area for a short outcome or next-step label when needed.
- Keep generous blank space above and below the key action. Do not simply crop a landscape composition into portrait; redesign the scene for vertical reading.
- Use a horizontal canvas only when the user explicitly asks for it.

## Information-Rich Infographic

- Create a mobile-first explanatory infographic, not a minimal decorative illustration. Each image should retain the core action plus the keywords, definitions, steps, examples, or outcomes needed to make that action useful without the surrounding paragraph.
- Use 4-6 visible text units as the normal target and up to 8 when the vertical layout has clear grouped bands and every unit passes the type-size baseline. A text unit can be a short label, a multi-line sentence card, a numbered step, or a compact comparison item.
- Use a clear hierarchy: optional short header, one dominant core action, 2-4 grouped supporting items, and an optional concise takeaway. A compact header is allowed; it must describe the topic rather than repeat a generic template title.
- Formal infographic structure is allowed: grouped steps, numbered flow, compact comparison columns, callout cards, or a small legend. Keep it hand-drawn and route-local rather than a polished corporate slide, UI screenshot, or generic template.
- Keep useful text rather than removing it merely to look sparse. When content overflows, regroup it into bands or split only the overflow into the next image.
- Full explanatory sentences are allowed and encouraged when they clarify a causal relationship, definition, caveat, or takeaway. Put a long sentence in its own high-contrast card or callout, allow it to wrap across 2-3 lines, and keep it visually distinct from labels.

## Multilingual Text Preservation

- Preserve every source-language keyword, term, acronym, and label that the user asks to retain. Do not drop English, Chinese, or any other language because another language is present.
- When the article provides multilingual terminology, show the original forms together in one text unit when they fit at the mobile baseline, for example `检索 / Retrieval`; otherwise place them in adjacent, equally prominent text units.
- Copy non-Latin text exactly. Do not replace it with an English translation unless the user asks for translation; do not remove English technical terms when adding Chinese explanations.
- Use concise bilingual or multilingual labels and keep their hierarchy consistent. Avoid repeating the same sentence in multiple languages unless the user explicitly requests full translation.

## Plan a Sequence From Information Volume

- Treat one independently understandable action, decision, relationship, or outcome as one image unit.
- Split a dense article section into an ordered sequence when a single canvas would mix units or force small type.
- Prefer a coherent progression such as setup -> decision -> action -> outcome. Omit roles that the article does not need.
- Give each image a distinct role and avoid repeating the same diagram with only cosmetic changes.
- A user-requested image count is a preference, not permission to make labels too small. Say when the requested count is insufficient for phone-readable output.

## Phone-Readable Text Baseline

- Design labels for a 390 px-wide, 9:16 phone screen viewed without zooming.
- Use 4-6 visible text units per image by default and up to 8 when the hierarchy remains clear. Do not remove needed keywords simply to meet an arbitrary sparse-label target.
- A label should normally be at most 16 Chinese characters or 6 English words. Supporting sentence cards may be longer and wrap across 2-3 lines at the secondary-text baseline; do not truncate or convert requested explanatory sentences into keywords merely to keep them on one line.
- Keep primary labels at least roughly 5% of the canvas height in visible letter height and secondary explanatory text at least roughly 3.5%; reserve clear spacing around every group and do not overlap text with the character or key action.
- Prefer grouped callouts and sentence cards over tiny scattered annotations. Compact legends, numbered steps, comparison cards, one-line notes, and 2-3-line explanatory statements are allowed when they remain large and scannable.

## Generation Prompt Clause

Include this meaning in every generated-image prompt:

```text
Mobile readability is mandatory: generate a standalone 9:16 vertical explanatory infographic for a 390 px-wide phone held upright, without zooming. Compose from top to bottom and keep the core character action in the central vertical band with generous space above and below. Retain the useful keywords, full explanatory sentences, steps, comparisons, and source-language terminology from the article. Use 4-6 visible text units by default and up to 8 when they are grouped into clear bands. Preserve Chinese, English, and any other requested source languages exactly; pair translations only when they fit at the stated text sizes. Keep primary labels at least roughly 5% of canvas height and secondary explanatory text at least roughly 3.5%. Compact headers, legends, numbered steps, comparison cards, one-line notes, and full sentences in distinct 2-3-line callout cards are allowed. Do not use tiny callouts, ungrouped dense annotations, unstructured paragraph blocks, or landscape-only layouts. If the idea cannot remain scannable at these sizes, regroup or split the overflow into the next sequential image instead of shrinking type or deleting required language.
```

## QA Gate

Reject and split or regenerate an image when any of these are true:

- It contains multiple unrelated primary actions or relationships that do not form one coherent infographic.
- It needs more than 8 text units, or the hierarchy cannot make 4-8 units scannable at the baseline.
- Any label is too small to read on a 390 px-wide phone without zooming.
- The image is horizontal, merely a cropped landscape layout, or lacks a clear top-to-bottom reading flow.
- It drops requested source-language terms or replaces multilingual labels with only one language without the user's permission.
- It relies on tiny annotations, tightly packed ungrouped callouts, or unstructured paragraph blocks instead of grouped sentence cards to explain the idea.
- Reducing the type is the only way to keep all information on the canvas.

When repairing a failure, preserve the selected IP, route constraints, and successful image units; move the overflow into one or more new images with ordered filenames.
