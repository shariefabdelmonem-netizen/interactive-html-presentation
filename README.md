# Interactive HTML Presentation

![Create HTML presentations easily](assets/cover.jpg)

**▶ Live examples:** https://shariefabdelmonem-netizen.github.io/interactive-html-presentation/

A skill that turns a topic and an audience into an animated, interactive HTML presentation you can run live in a workshop or classroom. Works in ChatGPT, Gemini and Claude.

Built by **Sharief Abdelmonem · AI Integration Coach** (#ai_with_sharief).

## Install (30 seconds)

**[⬇ Download the skill (ZIP)](https://github.com/shariefabdelmonem-netizen/interactive-html-presentation/raw/main/interactive-html-presentation.zip)**, then upload it to your AI. Don't unzip it.

| AI | Where to upload |
|---|---|
| **ChatGPT** | Profile icon → **Skills** → **New skill** → **Upload from your computer** |
| **Gemini** | **Settings** → **Skills** → **Upload** (on gemini.google.com) |
| **Claude** | **Settings** → **Capabilities** → **Skills** → **Upload skill** |

Then ask: *"Make an interactive presentation about …"*, or call it by name with `/interactive-html-presentation`.

**No upload option?** Open [`SKILL.md`](SKILL.md), copy everything, paste it into the chat and say *"Save this as a skill"*, or just *"Follow these instructions"* for this chat only.

## What it does

- Asks four questions before building: visual identity, target audience, session duration and number of slides
- Plans the deck around learning outcomes, with an interaction every 3–4 slides
- Uses only sourced data, labels illustrative values, and flags conflicting sources
- Builds one self-contained HTML file: 16:9 stage, GSAP animation, step-by-step reveals, slide transitions
- Presenter controls: arrow keys / Space / clicker, slide list (O), full screen (F), replay (R)
- Respects reduced-motion settings and keyboard-only use
- When the AI can run code: inlines libraries for offline use and tests every slide before delivery

## Use

Ask your AI something like:

> Make an interactive presentation about the Present Simple for Grade 5 students

It asks for anything missing (visual identity, audience, duration, number of slides), then builds and delivers the deck as one HTML file.

## Examples

Both decks run live in your browser. Click a preview to open it.

### Present Simple: Every Day!
Grade 4–6 · A1 · 8 slides · 15 minutes

[![Present Simple deck preview](assets/preview-present-simple.jpg)](https://shariefabdelmonem-netizen.github.io/interactive-html-presentation/examples/present-simple/)

**[▶ Open the live deck](https://shariefabdelmonem-netizen.github.io/interactive-html-presentation/examples/present-simple/)**

### AI Literacy for Teachers
Teacher training · 12 slides · 20 minutes

[![AI Literacy for Teachers deck preview](assets/preview-ai-literacy-for-teachers.jpg)](https://shariefabdelmonem-netizen.github.io/interactive-html-presentation/examples/ai-literacy-for-teachers/)

**[▶ Open the live deck](https://shariefabdelmonem-netizen.github.io/interactive-html-presentation/examples/ai-literacy-for-teachers/)**

Keys inside a deck: `→` / `Space` next · `←` back · `O` slide list · `F` full screen · `R` replay

## Folder structure

```
interactive-html-presentation/
├── SKILL.md        # the skill (works in Claude, ChatGPT and Gemini)
├── interactive-html-presentation.zip   # the same skill, ready to upload
├── README.md
├── index.html      # landing page for the live examples (GitHub Pages)
├── assets/         # cover and preview images
└── examples/
    ├── present-simple/index.html
    └── ai-literacy-for-teachers/index.html
```
