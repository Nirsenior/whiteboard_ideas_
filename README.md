# Idea Lab – HTML board

A self-contained, editable Hebrew RTL brainstorming board. Open `index.html` in any modern browser. All data is stored in your browser's localStorage. Use **גיבוי JSON** to back up your ideas; you can import JSON later.

## Features
- Five draggable sticky-note columns for problems, products, trends, wild ideas, and connections
- Editable, searchable notes with tags, favorites and research-ready flag
- Seed ideas from the user's Idea Lab discussions
- JSON backup/import
- Copy the board context or a single idea as a prompt for ChatGPT
- Export context as Markdown to hand off to Codex

## Important constraint
This app does **not** automatically sync with ChatGPT/Notion. A standalone HTML page cannot read conversation context, and no persistent API credentials should be embedded in client HTML. The seed ideas and context are a snapshot. For real bidirectional sync, build an authenticated backend (e.g. Supabase or managed storage) and a companion chat integration with a defined read/write workflow, privacy controls, and conflict handling.

## Codex next-step prompt
"Use this existing index.html as the starting point. Preserve the Hebrew RTL UX and card model. Add authenticated cloud synchronization and a secure workflow for importing/exporting ideas with ChatGPT, without embedding private API keys in browser code."

## Local development

No installation, build, API keys, or backend are required. Open `index.html` directly, or run from the repository directory:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open port 8000 in your local browser. Browser storage is specific to the browser and origin; switching ports or opening the file directly uses different storage. Export a JSON backup before moving between them.

The cloud-sync prompt above describes a future extension, not a feature of this version.
