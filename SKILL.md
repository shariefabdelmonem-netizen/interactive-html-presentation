---
name: interactive-html-presentation
description: Build an animated, interactive HTML presentation for a training session or workshop from a topic and audience, with speaker notes, sourced data and presenter controls.
---

# Interactive HTML Presentation

Turn a topic and audience into a working, interactive HTML presentation a trainer can run live in a room. Every design and motion choice must help the audience understand, remember or act. If it does neither, leave it out.

## 1. Gather inputs

Before building anything, always ask these four in one message (use AskUserQuestion with ready options where available), skipping only those the user has already answered. Then stop and wait.

1. Visual identity: brand colors (hex), fonts, logo (attached file or none), and visual style (Minimal / Educational / Corporate / Cinematic / Creative). Offer "Choose for me" as an option.
2. Target audience: role, sector, school type, grade level, country, and knowledge level (Beginner / Intermediate / Advanced).
3. Session duration in minutes.
4. Number of slides. Offer "Choose for me" (then use about one slide per 1.5–2 minutes).

If the topic itself is missing, ask for it in the same message.

Ask in the same message only for these if they matter and aren't obvious:
- Language: English / Arabic / Bilingual
- Venue internet: reliable / weak / none
- Deliverables beyond the HTML deck (see step 8)
- Whether they want an outline first

For everything else, decide sensibly and list assumptions at the top of the reply. Defaults:
- Presenter credit: "Sharief Abdelmonem · AI Integration Coach" unless told otherwise
- Objective: Train
- Tone: warm and practical
- Learning outcomes: write 2–3 measurable ones ("By the end, participants can …") and state them
- Local context: use the audience's real setting (Qatar / Gulf schools when the audience is local educators)

If the user asked for an outline first, send a slide-by-slide outline (title, key message, visual idea, interaction, minutes) and wait for approval.

## 2. Content & learning design

- Plan around the learning outcomes, not the topic in general.
- Use exactly the number of slides the user chose (interactive slides included). If they chose "Choose for me", use about one slide per 1.5–2 minutes. If their slide count and duration clash badly (e.g. 40 slides in 10 minutes), say so and suggest a better number before building.
- Arc: hook showing why it matters to this audience → core ideas → application in their context → commitment to act.
- For each main idea, where it fits: concept → local example → check for understanding → application.
- An interaction at least every 3–4 slides (poll, think-pair-share, live demo, flip cards, scenario sorting, quick quiz).
- Address the audience's misconceptions or objections directly on at least one slide.
- One idea per slide; body text about 30 words max; detail goes in speaker notes.
- Close with the one sentence to remember plus 2–3 concrete actions for next week.

## 3. Data & sources

- Never invent statistics, quotes, studies or references.
- Use the user's sources first. When searching, prefer original sources (government, OECD, UNESCO, peer-reviewed) over blogs and aggregators.
- Short source line on every slide with a number; full source list on the last slide.
- If sources give different figures for the same thing, tell the user which conflict, which you used and why.
- Label any illustrative or simulated values "Illustrative" on the slide.
- Charts: honest scales, bars from zero, clear labels and units; animation must not distort comparisons.

## 4. Visual design

- Apply the user's visual identity exactly: their hex colors, fonts and logo come first. If they chose "Choose for me", pick a palette and fonts that suit the topic and audience, and say so in one line.
- Write a design system as `:root` tokens first: 4–6 colors, one display font, one body font, a fixed type scale. Place the logo on the title and closing slides, and small on content slides only if the user wants it.
- Give color a consistent meaning (e.g. human / tool / caution).
- At the 1600×900 stage: body text ≥ 20px, slide titles ≥ 56px. Must read from the back of a room on a projector.
- Vary layouts (statement, split, grid, diagram, big number) with consistent edges and margins.
- Avoid generic looks: purple-blue gradients, emoji icons, clip-art, everything centered. Use simple custom SVG icons and diagrams.
- Arabic: full RTL layout, mirrored arrows and progress, Cairo or IBM Plex Sans Arabic, no letter-spacing on Arabic text; confirm numeral style.

## 5. Motion rules

- Motion explains: build a diagram step by step, draw a connection, count up a number, reveal a comparison.
- Max 3 transition types in the deck, chosen by slide relationship (continue = fade, new section = slide, detail = zoom).
- Max 2 entrance styles per slide. Transitions under 1s; entrances done within 2s.
- Content the presenter talks through point by point reveals one step per click.
- Respect prefers-reduced-motion: everything visible, no movement.

## 6. Presenter controls & interaction

- Next/previous: arrow keys, Space, PageUp/PageDown (clicker), on-screen buttons; touch swipe.
- Step reveals use the same "next" key; going back shows the previous slide fully revealed.
- O = slide list, F = full screen, R = replay slide, S = speaker view (notes, timer, next slide) when notes exist.
- Progress bar and slide number.
- Interactive elements work with mouse, touch and keyboard, and reset when the slide is re-entered.

## 7. Technical build

- One self-contained HTML file, inline CSS/JS, 16:9 stage at 1600×900 scaled to fit (absolute center + transform scale), no overflow.
- GSAP for timelines, Chart.js for charts only when needed; CSS/SVG for the rest. Pin exact versions (e.g. gsap 3.12.5, Chart.js 4.4.1).
- Venue internet weak or none: `npm install` the libraries in the workspace and inline them (and fonts as data URIs) so the file runs fully offline. Reliable internet: load from cdnjs and list dependencies.
- Embed an attached logo as a data URI (or inline SVG).
- Only the active slide animates; kill loops and destroy charts on leave. Set Chart.js devicePixelRatio to account for the stage scale.
- WCAG AA contrast, visible focus, aria labels on charts and controls.
- Print stylesheet: one slide per page, all steps revealed.

## 8. Optional deliverables

- Speaker notes with timing per slide (inside the deck's speaker view, and listed in the reply).
- Facilitator guide: activity instructions, materials, expected answers — as a doc.
- One-page participant handout — as a doc.

## 9. Test before delivery

In the workspace, open the file in headless Chrome with Playwright. The CDN is usually blocked there, so route the library URLs to locally npm-installed copies. Then:
- Step through every slide with the keyboard and capture console/page errors.
- Take one montage screenshot of key slides (charts, diagrams, interactive slides) and fix what it shows.
- Check text overflow, that interactions work and reset, that the slide count matches what the user chose, and that timing adds up to the duration.
Note anything you could not test (e.g. full screen, live CDN loading).

## 10. Deliver

Publish the HTML as an artifact (hand-built page). Then reply with:
1. Assumptions made (short)
2. Source conflicts or gaps
3. How to present (keys, interactive slides)
4. Internet dependencies, if any
5. Sources list

## Standard to aim for

Weak slide: "Benefits of AI in Education" with six bullets and a robot stock image.
Strong slide: "36% of teachers already use AI" as one large number counting up, a three-bar chart comparing countries, a one-line source, and a speaker note asking the room "Are you in the 36%?"
