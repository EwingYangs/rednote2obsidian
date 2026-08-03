# RedNote Sync for Obsidian

> Automatically sync your RedNote (Xiaohongshu / 小红书) **bookmarks, own posts, and likes** into your Obsidian vault — images, videos, tags and albums included.

English · [简体中文](./README.md) · [Website rednote.2notion.com](https://rednote.2notion.com)

![RedNote to Obsidian](./rednote2obsidian.png)

> ⚠️ **This is closed-source software.** It is distributed only as a compiled build (obfuscated `main.js`); the source code is not available. Redistribution, reverse engineering, and modified redistribution are prohibited. See [LICENSE](./LICENSE).

---

## Features

| Capability | Description |
|------------|-------------|
| 📥 Content sync | Sync bookmarks, your own posts, and likes to local Markdown |
| 🖼 Image download | Post images saved locally for offline reading |
| 🎬 Video download | Optionally download videos locally (embeds remote link by default) |
| 🏷 Tag sync | Post tags written into note frontmatter |
| 📂 Album folders | Bookmarks split into per-album subfolders, with album whitelist |
| ⏱ Scheduled sync | Background incremental sync on an interval |
| 🌐 CN / Global | Auto-detects both xiaohongshu.com and rednote.com |
| 📊 Engagement stats | Like / collect / comment / share counts written into frontmatter for Dataview / Bases queries |
| 💬 Comment sync | Optionally sync top 10 comments (up to 3 replies each) as a collapsible callout |
| 🤖 AI classify | Auto-file notes into custom categories via any OpenAI-compatible model |
| 📷 Image-to-text | Vision model OCR turns image-card content into searchable text |
| 🎙 Video transcript | Speech-to-text via Alibaba Bailian / Volcano Engine / Tencent Cloud / OpenAI-compatible providers, with optional AI cleanup and key-point summary |

## Preview

<!-- TODO: record GIFs into assets/ and replace the placeholders below -->
<!-- ![login](./assets/login.gif) -->
<!-- ![sync](./assets/sync.gif) -->

## Installation

### Option 1 — BRAT (recommended, auto-updates)

1. Install and enable **BRAT** (Beta Reviewer's Auto-update Tool) from Obsidian community plugins
2. Open BRAT and choose **Add Beta plugin**
3. Enter the repository URL:
   ```
   https://github.com/EwingYangs/rednote2obsidian
   ```
4. Enable **RedNote Sync** under **Settings → Community plugins**

> BRAT tracks GitHub Releases and updates to the latest version automatically.

### Option 2 — Manual

1. Download `main.js`, `manifest.json`, `styles.css` from the latest [Release](https://github.com/EwingYangs/rednote2obsidian/releases)
2. Create a folder `rednote2obsidian` under your vault's `.obsidian/plugins/` and drop the three files in:
   ```
   YourVault/.obsidian/plugins/rednote2obsidian/
   ├── main.js
   ├── manifest.json
   └── styles.css
   ```
3. Restart Obsidian and enable the plugin under **Settings → Community plugins**

## Usage

After enabling, go to **Settings → RedNote Sync**:

1. Click "Log in to RedNote", sign in inside the popup, then click "Extract Cookie"
2. Configure root folder, sync interval, batch size, and content type (bookmarks / posts / likes)
3. Turn on "Scheduled auto-sync" for background incremental syncing

See the [User Guide](./USER_GUIDE.md) for the full list of settings.

## Free quota & license code

- **10 notes** free trial — all features available, no signup required
- After 10 synced notes, enter a **license code** in settings to keep syncing
- License codes are available via the "Buy license" entry in settings or the [website](https://rednote.2notion.com), bound per device

## Acceptable use

This plugin is intended solely for syncing content **you have the right to access on your own account** into your **personal Obsidian knowledge base**, for personal offline reading and organization.

- ❌ Do NOT use it for bulk crawling/scraping of other people's data or any unauthorized data collection
- ❌ Do NOT use the synced content commercially or redistribute it publicly; you must comply with RedNote's terms of service and applicable laws
- ⚠️ You are responsible for your own use; you bear all consequences of any misuse

## Privacy & authorization

- Your RedNote login **cookie is stored only in your local vault** — never uploaded
- Synced content is written only to your local Obsidian vault
- Only the license code and a device identifier are sent to the authorization service for validation (quota & license management)

## Changelog

### v1.2.0 (2026-07-28)

- 📊 **Engagement stats in frontmatter**: like / collect / comment / share counts as plain numbers (`"1.2万"` parsed to `12000`) for Dataview / Bases queries
- 💬 **Comment sync**: new toggle syncs top 10 comments (up to 3 replies each) as a collapsible callout with author / likes / date
- 📷 **Image-to-text**: vision model OCR for up to the first 10 images per note; video notes skip cover recognition automatically
- 🎙 **Video transcript**: speech-to-text via Alibaba Bailian paraformer / Volcano Engine / Tencent Cloud ASR / OpenAI-compatible (whisper, SenseVoice)
- ✨ **AI transcript cleanup**: auto paragraphing, punctuation fixes, filler-word removal, plus a key-point summary
- ⚙️ **Unified AI model settings**: all AI credentials and models consolidated into one section, with one-click test buttons for text / vision / transcription
- 🐛 Fixes: adapted to Xiaohongshu's new video stream codec grouping (video notes losing their video); settings page now refreshes immediately after login

### v1.1.x

- Album whitelist incremental sync, batch sync fixes, video download toggle, and more (see past releases)

## Feedback

Questions or suggestions? Open an [Issue](https://github.com/EwingYangs/rednote2obsidian/issues) or visit the [website rednote.2notion.com](https://rednote.2notion.com).

## License

**Closed-source software.** Distributed only as a compiled build; the source code is not available. Redistribution, reverse engineering, and modified redistribution are prohibited. See [LICENSE](./LICENSE).
