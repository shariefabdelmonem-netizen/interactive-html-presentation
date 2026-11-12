# Interactive HTML Presentation

![Create HTML presentations easily](assets/cover.jpg)

**▶ Live examples:** https://shariefabdelmonem-netizen.github.io/interactive-html-presentation/
**⚡ Use it in ChatGPT, Gemini, Claude or any AI:** https://shariefabdelmonem-netizen.github.io/interactive-html-presentation/use.html

A Claude skill that turns a topic and an audience into an animated, interactive HTML presentation you can run live in a workshop or classroom.

Built by **Sharief Abdelmonem · AI Integration Coach** (#ai_with_sharief).

## What it does

- Asks four questions before building: visual identity, target audience, session duration and number of slides
- Plans the deck around learning outcomes, with an interaction every 3–4 slides
- Uses only sourced data, labels illustrative values, and flags conflicting sources
- Builds one self-contained HTML file: 16:9 stage, GSAP animation, step-by-step reveals, slide transitions
- Presenter controls: arrow keys / Space / clicker, slide list (O), full screen (F), replay (R)
- Respects reduced-motion settings and keyboard-only use
- Can run fully offline when the venue internet is weak
- Tests every slide in a headless browser before delivery

## Use it in any AI (ChatGPT, Gemini, Claude…)

Open **[the one-click page](https://shariefabdelmonem-netizen.github.io/interactive-html-presentation/use.html)** and pick your assistant. Or paste this as your first message in any AI:

```
Read the instructions at this link and follow them for our whole conversation:
https://shariefabdelmonem-netizen.github.io/interactive-html-presentation/prompt.txt
Start with Step 1 and ask me the setup questions.
```

If your AI can't open links, paste the contents of [`PROMPT.md`](PROMPT.md) instead. To keep it permanently, paste `PROMPT.md` into a **Custom GPT** (ChatGPT) or a **Gem** (Gemini).

`PROMPT.md` is the model-neutral version of the skill. `prompt.txt` is an identical copy served from the site. Keep them in sync when you edit.

## Install in Claude

1. Download `SKILL.md` (or the whole folder).
2. In Claude, go to **Settings → Capabilities → Skills** and upload it, or place the folder in your skills directory for Claude Code.

## Use

Ask Claude something like:

> Make an interactive presentation about the Present Simple for Grade 5 students

or call it by name:

> /interactive-html-presentation AI literacy for teachers, 20 minutes

Claude will ask for anything missing, then build, test and deliver the deck.

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
├── SKILL.md        # the skill instructions Claude follows
├── PROMPT.md       # model-neutral version for ChatGPT, Gemini and others
├── prompt.txt      # same as PROMPT.md, served from the site for link loading
├── use.html        # one-click page: open the skill in any AI
├── README.md
├── index.html      # landing page for the live examples (GitHub Pages)
├── assets/         # cover and preview images
└── examples/
    ├── present-simple/index.html
    └── ai-literacy-for-teachers/index.html
```
