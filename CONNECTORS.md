# Connectors: the `~~category` placeholder convention

This plugin is written to work with whatever tools YOU have connected, not a specific product. Anywhere a skill needs an external tool, it names a **category** with a `~~` prefix instead of a brand:

| Placeholder | Meaning | Examples of what could fill it |
|---|---|---|
| `~~spreadsheet` | Your content idea bank + pilot tracker | Google Sheets, Excel/OneDrive, Airtable, Notion database |
| `~~notes app` | Where you capture raw ideas on the go | Apple Notes, Notion, Obsidian, Google Keep, a plain notes folder |
| `~~design tool` | Where visual creative is generated | Canva, Figma, Adobe Express — or the built-in HTML-to-PNG fallback |
| `~~email` | How the weekly review package reaches you | Gmail, Outlook, any mail connector — or a saved Markdown file |
| `~~browser` | Browser automation for reading your saved/published posts | Claude in Chrome, or pasting content manually |

## How it works at runtime

When Claude encounters `~~design tool` in a skill, it should:

1. **Use the matching connected tool** if one is available in the session.
2. **Ask you once** which tool to use if several could match, then stay consistent for the session.
3. **Fall back gracefully** if nothing matches — every skill in this plugin defines its fallback (e.g., HTML-to-PNG rendering instead of a design tool, a local file instead of email). A missing tool skips one step, never the whole run, and the skip is always flagged in the delivery.

## Making it permanent

To hardcode your choices, edit the SKILL.md files and replace placeholders with your actual tools and resources, e.g. replace `your idea bank in ~~spreadsheet` with `the Content_Idea_Bank Google Sheet at <your-sheet-URL>`. See USER-INSTRUCTIONS.md.
