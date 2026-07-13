---
name: create-post-creative
description: >
  Generate on-brand post creative (cover images, carousel slides, meme visuals, video
  thumbnails) for the user's content using ~~design tool with their brand tokens.
  Use when the user asks to "make the creative", "build the carousel", "create a cover
  image", "make a meme for this post", or after drafts are approved and need visuals.
---

# Create Post Creative

Build visual assets for approved drafts. **Primary method: ~~design tool** (editable designs the user can tweak before posting). Fallback: branded HTML rendered to PNG when no design tool is available.

## Your brand tokens (user: fill this in — see USER-INSTRUCTIONS.md)

- **Background color(s):** [dominant hex + allowed alternates]
- **Primary type color(s):** [hex]
- **Accent color:** [hex — recommended rule: ONE accent moment per asset]
- **Secondary palette:** [hex values and when each is allowed]
- **Fonts:** [display font + weight, body font, mono/detail font — or closest equivalents in the design tool]
- **Style rules:** [3-5 non-negotiables, e.g., "sharp corners", "borders not shadows", "no gradients", "no stock photos", "no emoji as icons"]
- **Signature mark:** [logo or motif and where it sits, e.g., "small mark, bottom corner"]

If this section is still blank, stop and ask the user to complete it (or offer to propose a starter kit).

## Sizes

- Cover/link image (LinkedIn): 1200x627
- Carousel slides (LinkedIn PDF + Instagram): 1080x1350
- Instagram feed square: 1080x1080 | Story: 1080x1920
- YouTube thumbnail: 1280x720

## ~~design tool workflow (primary)

1. Check for a saved brand kit in the tool. If one exists, use it; if not, write ALL brand tokens explicitly into every generation prompt: hex colors, font names, and the style rules above.
2. Generate the design with a prompt containing: exact dimensions/format, the headline text **verbatim** from the draft, brand tokens, and a concrete layout description (background color, headline position, single accent moment, signature mark placement, "flat design").
3. Review the result: accent used once, text verbatim and unclipped, no off-brand elements. Iterate with the tool's editing operations if text needs correction.
4. Export: PNG for single images, PDF for LinkedIn carousels (plus PNGs for Instagram).
5. Share the editable design link with the user so they can tweak before posting, plus the exported files.
6. Keep designs organized in one dedicated folder in the tool.

## HTML → PNG fallback (when ~~design tool is unavailable)

Write a self-contained HTML file per asset (fixed dimensions, web fonts, inline SVG marks), render via a headless-browser screenshot at exact dimensions with deviceScaleFactor 2. For carousels, render slide PNGs then assemble a PDF. State clearly in the delivery that the fallback was used and design-tool editing is not available for these assets.

## Meme visuals

Text-forward on a brand background, dry insider humor drawn from the draft's argument — never punching down. Two-panel or caption-over-setup layouts. No third-party meme template images (rights + brand consistency). One meme max per week.

## Always

- Log which method was used (design tool vs. fallback) and generation time in the delivery package.
- Never publish or post anything. All assets are delivered for the user's review.
