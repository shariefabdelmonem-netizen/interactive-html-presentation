---
name: interactive-html-presentation
description: Build an animated, interactive HTML presentation for a lesson, training session or workshop from a topic and audience. Use when the user asks for an interactive presentation, animated slides, an HTML deck or a workshop deck.
---

# Interactive HTML Presentation

Turn a topic and audience into ONE working, interactive HTML presentation that a trainer can run live in a room. Every design and motion choice must help the audience understand, remember or act. If it does neither, leave it out.

This skill works in Claude, ChatGPT, Gemini and other assistants. Where a step depends on a tool your environment may not have, it says "if available".

## Step 1: Ask first

Before building anything, ask these in ONE message, skipping any the user has already answered. Use a multiple-choice question tool with ready options if available; otherwise a short numbered list. Then stop and wait.

1. Topic (if not given)
2. Visual identity: brand colors (hex), fonts, logo, style (Minimal / Educational / Corporate / Cinematic / Creative), or "choose for me"
3. Target audience: who they are, age or grade, country, knowledge level
4. Session duration in minutes
5. Number of slides, or "choose for me" (then use about one slide per 1.5–2 minutes)
6. Only if unclear: language (English / Arabic / Bilingual), venue internet (reliable / weak / none), extras (speaker notes, facilitator guide, handout), outline first or not

If slide count and duration clash badly (e.g. 40 slides in 10 minutes), say so and suggest a better number. For everything else, decide sensibly and list assumptions in 3–5 bullets before building. Default presenter credit: "Sharief Abdelmonem · AI Integration Coach" unless the user gives another name. If the user wants an outline first, send a slide-by-slide outline (title, key message, visual idea, interaction, minutes) and wait for approval.

## Step 2: Plan the content

- Write 2–3 measurable learning outcomes ("By the end, participants can …") and build every slide around them.
- Use exactly the number of slides the user chose, interactive slides included.
- Arc: hook that shows why it matters → core ideas → application in the audience's own context → a clear action to take next.
- For each main idea where it fits: concept → local example → check for understanding → application.
- One idea per slide, about 30 words of text maximum; detail goes in speaker notes.
- An interaction at least every 3–4 slides: sentence builder, click-to-reveal or flip cards, sorting game, quick quiz, poll, live demo or timer.
- Address the audience's misconceptions or objections on at least one slide.
- Use examples from the audience's real setting (their country, school, subject, culture).
- Close with the one sentence to remember plus 2–3 concrete next steps.

## Step 3: Facts and data

- Never invent statistics, quotes, studies or references. If web search is available, use original sources (government, OECD, UNESCO, peer-reviewed). If you cannot verify a number, leave it out.
- Short source line on every slide with a number; source list on the last slide.
- If two sources disagree on the same figure, tell the user which ones, which you used and why.
- Label any made-up teaching values "Illustrative".
- Charts: bars start at zero, clear labels and units, and animation must not distort comparisons.

## Step 4: Design

- Apply the user's colors, fonts and logo exactly. If they chose "choose for me", pick a palette and fonts that suit the audience and say so in one line.
- Define 4–6 color tokens in `:root` and give each color a fixed meaning (for example: blue = the verb, red = the ending we add).
- Readable on a projector: body text at least 20px and titles at least 56px on a 1600×900 stage.
- Vary layouts (big statement, split, grid, diagram, big number) with consistent margins.
- No emoji icons, no clip-art, no purple-blue gradient hero, not everything centered. Draw simple SVG icons yourself.
- Logo (if given): on the title and closing slides, embedded as a data URI or inline SVG.
- Arabic: full RTL layout, mirrored arrows and progress, Cairo or IBM Plex Sans Arabic, no letter-spacing on Arabic text.

## Step 5: Motion

- Motion must explain: build a diagram step by step, count up a number, reveal a comparison.
- At most 3 slide-transition types in the deck (continue = fade, new section = slide, detail = zoom), at most 2 entrance styles per slide, transitions under 1 second.
- Points the presenter talks through appear one per click.
- Respect `prefers-reduced-motion`: show everything without movement.

## Step 6: Build

ONE complete, self-contained `index.html` (inline CSS and JavaScript):

- A 16:9 stage of 1600×900 px, centered and scaled to fit any screen with `transform: scale()`, no overflow.
- GSAP 3.12.5 from cdnjs for animation; Chart.js 4.4.1 from cdnjs only if there is a chart. If the venue internet is weak and you can run code, download these libraries and inline them so the file works offline; otherwise tell the user the file needs internet for animations.
- Controls: → / Space / PageDown = next (reveals the next step first), ← / PageUp = previous (shows that slide fully revealed), O = slide list, F = full screen, R = replay slide, S = speaker notes (if requested), on-screen buttons, progress bar, slide number, touch swipe.
- Interactive elements work with mouse, keyboard and touch, and reset when the slide is opened again.
- Only the active slide animates; stop loops and destroy charts when leaving a slide.
- Visible keyboard focus, WCAG AA contrast, aria labels on charts and buttons.

Write ALL the code. Never stop at an outline unless the user asked for one.

## Step 7: Check

If you can run code (code interpreter, sandbox, headless browser), open the file, step through every slide, and fix errors, text overflow and broken interactions before delivering. If you can't, re-read the code once for these problems. Confirm the slide count and total timing match what the user asked for.

## Step 8: Deliver

1. Assumptions (short list) and any source conflicts
2. The presentation: publish it as a page or artifact if your app supports that; otherwise give the complete `index.html` in one code block, and open it in canvas or preview mode if available
3. How to present: save as `index.html`, open in Chrome or Edge, and the keys above
4. Extras if requested (speaker notes, facilitator guide, handout)
5. Sources used

## Quality bar

Weak slide: "Benefits of AI in Education" with six bullets and a robot stock image.
Strong slide: "36% of teachers already use AI" as one large number counting up, a three-bar chart comparing countries, a one-line source, and a question to the room.
