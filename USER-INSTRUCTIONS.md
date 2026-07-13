# User Instructions — customize before first use

This is a **template**. Out of the box it will draft generic content; the value comes from the profile sections you fill in. Complete these steps first.

## 1. Write your voice profile (required)

Open `skills/draft-content/SKILL.md` and complete the **"Your voice profile"** section:

- **Voice description** — 2-3 sentences on how you actually write (e.g., "dry, direct, peer-to-peer, never guru").
- **Banned words/patterns** — buzzwords and tics you never use (e.g., "synergy", "game-changer", em dashes, emoji bullets).
- **Rhythm rules** — paragraph length, sentence rhythm, emoji policy, character limits.
- **Worldview** — 3-5 recurring beliefs your content keeps returning to.
- **Signature stance** — your one-line position on your core topic.
- **Real stories** — 3-5 true anecdotes with specifics that drafts may draw on. The plugin will never invent stories; it only uses these or marks a placeholder.
- **Content pillars** — 4-6 named themes (P1, P2, ...) used to tag and balance ideas.
- **Post structure** — optional: your proven post skeleton (hook, turn, story, reveal, takeaways, closing question).

The best way to build this: paste 5-10 of your highest-performing posts into Claude and ask it to draft the profile from them, then edit it by hand.

## 2. Define your brand tokens (required for creative)

Open `skills/create-post-creative/SKILL.md` and fill the **"Your brand tokens"** section: background/primary/accent hex colors, fonts, and 3-5 style rules (e.g., "one accent color moment per asset", "no gradients", "sharp corners"). If you don't have a brand kit yet, ask Claude to propose one and iterate.

## 3. Set up the idea bank spreadsheet

Create a spreadsheet (see CONNECTORS.md) with tabs: **Raw Social Posts**, **Raw Notes**, **Content Ideas** (with a Priority column), **Full Post Drafts**, and optionally **Pilot Tracker** (for logging what was drafted/posted and its performance). Tell Claude where it lives, or hardcode the link in the skills.

## 4. Point sources at YOUR accounts

In `weekly-content-run/SKILL.md`, set: which notes in your ~~notes app count as content ideas (topics to include/skip), and the URLs of your saved-posts and activity pages on your primary platform.

## 5. Choose platforms

The skills default to a LinkedIn-first, Instagram + YouTube adaptation model. Edit the platform list and per-platform notes in `draft-content/SKILL.md` if your mix differs (e.g., X/Threads/newsletter).

## 6. Set your delivery email

Tell Claude your address once, or hardcode it in Step 5 of `weekly-content-run/SKILL.md`.

## Optional

- Schedule the weekly run (e.g., Monday mornings) via your client's scheduled-tasks feature.
- After a few weeks of Pilot Tracker data, ask Claude to review which formats and pillars perform and tune the playbook.

## What you should never change

The guardrails: the plugin must never publish or post anything, and never fabricate stories, client examples, or metrics. Your audience trusts you because it IS you.
