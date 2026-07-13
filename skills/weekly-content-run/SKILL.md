---
name: weekly-content-run
description: >
  Run the full weekly content pipeline: pull new ideas from the user's ~~notes app and
  saved social posts, update the idea bank in ~~spreadsheet, draft 3-4 pieces in the
  user's voice with creative, and deliver the package for review. Use when the user says
  "run the weekly content run", "do the weekly content pull", or when triggered by a
  scheduled task. Never posts anything.
---

# Weekly Content Run

Execute the end-to-end pipeline. Every step that can fail has a fallback; never abort the whole run because one source is unavailable.

## Step 1 — Pull sources

**~~notes app.** List notes modified in the last 8 days; select work/content notes (the user defines include/skip topics — see USER-INSTRUCTIONS.md; skip personal notes). Fetch each note's content. If a note fails to fetch, log it as "needs manual copy" instead of failing.

**Saved social posts (~~browser).** Read the user's saved-posts page, own recent activity, and comments with engagement on their primary platform. Extract author, topic, format, summary, engagement signals. If the browser is unavailable, SKIP this source, continue with notes only, and flag the skip prominently in the final package.

## Step 2 — Update the idea bank (~~spreadsheet)

- Dedupe: read existing rows first; only add items not already present.
- Append new social items to the "Raw Social Posts" tab (Author, Date Saved, Topic, Format, Summary, Trend Tag, Pillar Relevance).
- Append new notes to the "Raw Notes" tab (Title, Date, Raw Content, Idea Extract, Pillar Fit, Suggested Angle).
- Add newly identified strong ideas to "Content Ideas" (Working Title, Angle/POV, Why It Breaks Through, Trend, Format Suggestion, Priority).
- Never overwrite existing rows; append only.

## Step 3 — Draft

Invoke the `draft-content` skill: select 3-4 primary-platform-first ideas (high priority, fresh, pillar-diverse) and draft per the user's voice profile, with adaptations, format recommendation, and creative spec per draft.

## Step 4 — Creative

Invoke `create-post-creative` for each draft's primary asset (cover image, meme, or carousel). Primary method: ~~design tool with the user's brand tokens; fallback: HTML-to-PNG. Include editable design links in the package.

## Step 5 — Deliver for review

Assemble one package: drafts + creative + sheet-update summary + flags (skipped sources, notes needing manual copy).
- Send via ~~email to the user with drafts inline and creative attached. If only a draft-creation email tool exists, create the draft and say where it is; if no email tool, save the package as a file and present it.
- Also add full drafts to the "Full Post Drafts" tab of ~~spreadsheet.
- NEVER post to any platform. The user reviews, edits, and posts themselves.

## Step 6 — Log the run

If a "Pilot Tracker" tab exists, append a row per draft: date, working title, pillar, format, what AI did, status "Drafted - awaiting review". Leave performance columns empty. Never overwrite qualitative columns the user has filled.

## Step 6b — Pull performance metrics (~~browser)

For each tracker row with status "Posted" and a post URL: open the post, read reactions/comments/reshares (and impressions from the user's own analytics view if available), and fill ONLY the quantitative columns for that row. First fill at the first run 7+ days after posting; refresh on later runs. If a URL fails to load, flag it — never fabricate metrics. Qualitative columns stay the user's.

## Weekly hygiene

Surface in the package: prior drafts still unposted (don't redraft the same idea), drafts awaiting review older than 14 days, and posted rows missing a post URL.
