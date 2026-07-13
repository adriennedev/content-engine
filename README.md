# Content Engine

A Claude plugin that runs a weekly content pipeline for a personal brand or small company: it mines ideas from your saved posts and notes, maintains an idea bank spreadsheet, drafts platform-ready posts in **your** voice (defined by a voice profile you fill in), generates on-brand creative, and delivers the whole package for your review.

## The hard rule

**This plugin NEVER publishes anything.** It never posts to LinkedIn, Instagram, YouTube, or anywhere else, and never sends messages to third parties. You review, edit, and post everything yourself.

## Skills

- **weekly-content-run** — the full pipeline: pull new ideas from your ~~notes app and saved social posts, update your idea bank in ~~spreadsheet, draft 3-4 pieces in your voice, generate creative, and deliver the package via ~~email. Also pulls performance metrics for posts you've published.
- **draft-content** — draft posts for your platforms from the idea bank or a supplied idea, following your voice profile, with format recommendations and creative specs.
- **create-post-creative** — build cover images, carousel slides, memes, and thumbnails in your brand style using ~~design tool (with an HTML-to-PNG fallback).

## Why it works

Generic AI content sounds like AI. This plugin forces every draft through a **voice profile you write yourself** (banned words, sentence rhythm, worldview, real stories) and a **format playbook**, and it refuses to fabricate stories or metrics: when a draft needs a real example it marks `[YOU: add real example here]` instead of inventing one.

## Example use cases

- **Example 1:** "Run the weekly content run" — Claude pulls the week's ideas from your notes and saved posts, updates the idea bank, drafts 4 posts in your voice with creative, and emails you the review package.
- **Example 2:** "Turn this idea into a LinkedIn post: [idea]" — Claude drafts it per your voice profile, recommends a format (text, carousel, or video script), and specs the creative.
- **Example 3:** "Build the carousel for draft 2" — Claude generates 6-10 branded slides in ~~design tool sized for LinkedIn and Instagram, and shares the editable design link.

## Setup

Read **USER-INSTRUCTIONS.md** first — the plugin is a template and needs your voice profile, brand tokens, and idea bank before it can sound like you. **CONNECTORS.md** explains the `~~category` tool placeholders.
