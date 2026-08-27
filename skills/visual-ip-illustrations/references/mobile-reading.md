# Mobile Reading Contract

Use this shared contract for every visual-IP route. It supplements, but never overrides, the selected route's identity, style, attribution, safety, and output-path rules.

Its 9:16 vertical portrait requirement overrides legacy 16:9 or horizontal wording in route-local prompt templates, QA files, source records, and example assets. Those legacy references remain useful for character and line-style calibration, but not for the output aspect ratio.

## Phone-First Canvas

- Generate every new illustration on a 9:16 vertical canvas, optimized for a phone held upright.
- Compose from top to bottom: use the upper area for a short setup when needed, keep the character's core action in the central vertical band, and reserve the lower area for a short outcome or next-step label when needed.
- Keep generous blank space above and below the key action. Do not simply crop a landscape composition into portrait; redesign the scene for vertical reading.
- Use a horizontal canvas only when the user explicitly asks for it.

## Plan a Sequence From Information Volume

- Treat one independently understandable action, decision, relationship, or outcome as one image unit.
- Split a dense article section into an ordered sequence when a single canvas would mix units or force small type.
- Prefer a coherent progression such as setup -> decision -> action -> outcome. Omit roles that the article does not need.
- Give each image a distinct role and avoid repeating the same diagram with only cosmetic changes.
- A user-requested image count is a preference, not permission to make labels too small. Say when the requested count is insufficient for phone-readable output.

## Phone-Readable Text Baseline

- Design labels for a 390 px-wide, 9:16 phone screen viewed without zooming.
- Use no more than 4 short visible labels per image by default. Use 5 only when every label remains large, isolated, and essential.
- A label should normally be at most 12 Chinese characters or 4 English words. Move explanation into the article or a subsequent image instead of shrinking the label.
- Keep labels at least roughly 6% of the canvas height in their visible letter height; reserve generous blank space around every label and do not overlap labels with the character or key action.
- Prefer one large label near the action over several small annotations. Never use paragraph text, legend text, footnotes, tables, or tiny callouts inside an illustration.

## Generation Prompt Clause

Include this meaning in every generated-image prompt:

```text
Mobile readability is mandatory: generate a standalone 9:16 vertical illustration for a 390 px-wide phone held upright, without zooming. Compose from top to bottom and keep the core character action in the central vertical band with generous space above and below. Use at most 4 short visible labels by default (5 only when all remain large and isolated). Make every label visibly large, with letter height at least roughly 6% of the canvas height. Do not use paragraphs, legends, footnotes, tables, tiny callouts, dense annotations, or landscape-only layouts. If the idea needs more text, actions, comparisons, or labels, it belongs in a separate sequential image instead of smaller type.
```

## QA Gate

Reject and split or regenerate an image when any of these are true:

- It contains more than one independently understandable core action or relationship.
- It needs more than 4 short labels by default, or a label is longer than the baseline.
- Any label is too small to read on a 390 px-wide phone without zooming.
- The image is horizontal, merely a cropped landscape layout, or lacks a clear top-to-bottom reading flow.
- It relies on a legend, paragraph, table, tiny annotation, or tightly packed callouts to explain the idea.
- Reducing the type is the only way to keep all information on the canvas.

When repairing a failure, preserve the selected IP, route constraints, and successful image units; move the overflow into one or more new images with ordered filenames.
