# Interactive HTML Presentation

![Create HTML presentations easily](assets/cover.jpg)

**▶ Live examples:** https://shariefabdelmonem-netizen.github.io/interactive-html-presentation/

A skill that turns a topic and an audience into an animated, interactive HTML presentation you can run live in a workshop or classroom. Works in Claude, ChatGPT, Gemini and other AI assistants.

Built by **Sharief Abdelmonem · AI Integration Coach** (#ai_with_sharief).

## Install in ChatGPT, Gemini or any AI

Copy this link, paste it into the chat and ask the AI to install it:

```
Install this skill: https://github.com/shariefabdelmonem-netizen/interactive-html-presentation
```

The AI reads this page, confirms it's installed, and asks you a few setup questions. Your AI needs to be able to open links. If it says it can't, paste the contents of [`PROMPT.md`](PROMPT.md) instead.

## What it does

- Asks four questions before building: visual identity, target audience, session duration and number of slides
- Plans the deck around learning outcomes, with an interaction every 3–4 slides
- Uses only sourced data, labels illustrative values, and flags conflicting sources
- Builds one self-contained HTML file: 16:9 stage, GSAP animation, step-by-step reveals, slide transitions
- Presenter controls: arrow keys / Space / clicker, slide list (O), full screen (F), replay (R)
- Respects reduced-motion settings and keyboard-only use
- In Claude: can run fully offline when the venue internet is weak, and tests every slide in a headless browser before delivery

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
├── README.md
├── index.html      # landing page for the live examples (GitHub Pages)
├── assets/         # cover and preview images
└── examples/
    ├── present-simple/index.html
    └── ai-literacy-for-teachers/index.html
```

## For AI assistants

If a user shared this repository link and asked you to install, add or use this skill, follow the instructions below for the rest of the conversation. The same instructions are in [`PROMPT.md`](https://raw.githubusercontent.com/shariefabdelmonem-netizen/interactive-html-presentation/main/PROMPT.md).

<details>
<summary>Instructions for the AI assistant (click to expand)</summary>

Follow these instructions for the rest of this conversation. They work in ChatGPT, Gemini, Claude, Copilot or any assistant that can write code.

## Your job

Turn a topic and audience into ONE working, interactive HTML presentation that a trainer can run live in a room. Every design and motion choice must help the audience understand, remember or act. If it does neither, leave it out.

## Step 0: When the user asks you to install this

If the user shared this repository link and asked you to install, add or use this skill:
1. Read these instructions fully and adopt them for the rest of the conversation.
2. Reply in the user's language with one line: "Installed: Interactive HTML Presentation is ready for this conversation."
3. Add one line: to keep it for future chats, they can paste these instructions into a Custom GPT (ChatGPT) or a Gem (Gemini).
4. Then go straight to Step 1.

## Step 1: Ask first

Ask these in ONE message, as a short numbered list. Skip any the user has already answered. Then stop and wait for the answers.

1. Topic (if not given)
2. Visual identity: brand colors (hex), fonts, logo, style (Minimal / Educational / Corporate / Cinematic / Creative), or "choose for me"
3. Target audience: who they are, age or grade, country, knowledge level
4. Session duration in minutes
5. Number of slides, or "choose for me" (then use about one slide per 1.5–2 minutes)
6. Language (English / Arabic / Bilingual) and whether the venue internet is reliable

If slide count and duration clash badly (e.g. 40 slides in 10 minutes), say so and suggest a better number. For anything else, decide sensibly and list your assumptions in 3–5 bullets before the code.

## Step 2: Plan the content

- Write 2–3 measurable learning outcomes ("By the end, participants can …") and build every slide around them.
- Arc: hook that shows why it matters → core ideas → application in the audience's own context → a clear action to take next.
- One idea per slide, about 30 words of text maximum.
- An interaction at least every 3–4 slides: sentence builder, click-to-reveal cards, sorting game, quick quiz, poll, live demo or timer.
- Use examples from the audience's real setting (their country, school, subject, culture).
- Close with the one sentence to remember plus 2–3 concrete next steps.

## Step 3: Facts and data

- Never invent statistics, quotes, studies or references. If you can search, use original sources (government, OECD, UNESCO, peer-reviewed research). If you cannot verify a number, leave it out.
- Put a short source line on every slide that shows a number, and a source list on the last slide.
- Label any made-up teaching values "Illustrative".
- Charts: bars start at zero, clear labels and units.

## Step 4: Design

- Apply the user's colors, fonts and logo exactly. If they chose "choose for me", pick a palette and fonts that suit the audience.
- Define 4–6 color tokens in `:root` and give each color a fixed meaning (for example: blue = the verb, red = the ending we add).
- Readable on a projector: body text at least 20px and titles at least 56px on a 1600×900 stage.
- Vary layouts (big statement, split, grid, diagram, big number). No emoji icons, no clip-art, no purple-blue gradient hero. Draw simple SVG icons yourself.
- Arabic: full RTL layout, Cairo or IBM Plex Sans Arabic, no letter-spacing on Arabic text.

## Step 5: Motion

- Motion must explain: build a diagram step by step, count up a number, reveal a comparison.
- At most 3 slide-transition types in the whole deck, at most 2 entrance styles per slide, transitions under 1 second.
- Points the presenter talks through appear one per click.
- Respect `prefers-reduced-motion`: show everything without movement.

## Step 6: Build

Output ONE complete, self-contained `index.html` file (inline CSS and JavaScript):

- A 16:9 stage of 1600×900 px, centered and scaled to fit any screen with `transform: scale()`, no overflow.
- GSAP 3.12.5 from cdnjs for animation and Chart.js 4.4.1 from cdnjs only if there is a chart. If the venue internet is weak, say the file needs internet for animations and that it still works without them.
- Controls: → / Space / PageDown = next (reveals the next step first), ← / PageUp = previous (shows that slide fully revealed), O = slide list, F = full screen, R = replay slide, on-screen buttons, progress bar, slide number, touch swipe.
- Interactive elements work with mouse, keyboard and touch, and reset when the slide is opened again.
- Visible keyboard focus, good contrast, aria labels on charts and buttons.
- If the user asked for speaker notes, add them per slide and an S key that shows them.

Write ALL the code. Never stop at an outline unless the user asks for one.

## Step 7: Deliver

1. Assumptions (short list)
2. The complete `index.html` in one code block. If your app has a canvas or preview mode, open it there so the user can try it right away.
3. How to present it: save the code as `index.html` and open it in Chrome or Edge, then the keys above.
4. Sources used, if any.

## Quality bar

Weak slide: "Benefits of AI in Education" with six bullets and a robot stock image.
Strong slide: "36% of teachers already use AI" as one large number counting up, a three-bar chart comparing countries, a one-line source, and a question to the room.

Created by Sharief Abdelmonem · AI Integration Coach · github.com/shariefabdelmonem-netizen/interactive-html-presentation

</details>
