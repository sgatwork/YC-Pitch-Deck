[README.md](https://github.com/user-attachments/files/26834849/README.md)
# pitch-deck-skill

A Claude skill for building YC-style pitch decks — content framework + design system + working PptxGenJS code. Drop it into Claude and go from founder interview to a polished `.pptx` in one conversation.

---

## What it produces

| Cover | Problem | Product |
|-------|---------|---------|
| ![Cover](examples/slide-cover.jpg) | ![Problem](examples/slide-problem.jpg) | ![Product](examples/slide-product.jpg) |

| Market | Traction | Team | Ask |
|--------|----------|------|-----|
| ![Market](examples/slide-market.jpg) | ![Traction](examples/slide-traction.jpg) | ![Team](examples/slide-team.jpg) | ![Ask](examples/slide-ask.jpg) |

---

## Design principles

- **Off-white background** (`#F0F0F0`) — not pure white, gives the editorial quality
- **Helvetica Bold** for headlines only — large, 50–80pt, 3–7 words max
- **Courier New** for all labels, tags, and metadata — the monospace creates the structured editorial feel
- **White rounded cards** with a barely-there shadow — the signature layout element
- **Two-column layout** — big headline left, evidence cards right
- **Accent colour** — ask for the founder's brand colour, default to Klein Blue (`#002FA7`)
- **Logo mark** top-right on every slide
- **One idea per slide** — the headline is the entire message; everything else is supporting evidence

---

## How to install

This skill is designed for Claude's skill system. Drop the three files into your skills directory:

```
your-skills-folder/
└── pitch-deck/
    ├── SKILL.md
    └── references/
        ├── content.md
        └── design.md
```

Claude will pick up the skill automatically when you ask it to build a pitch deck.

---

## How to use

Just start a conversation with Claude:

> "Help me create a pitch deck for my company, I need to present it to YC."

Claude will run a founder interview (8–10 questions), then build a complete `.pptx` file you can download and open in PowerPoint or Keynote.

**What Claude will ask:**
1. What does your startup do? (one plain sentence)
2. Who is the customer? (be specific)
3. What problem are you solving?
4. Why now?
5. What's your traction?
6. What's the market size?
7. What's the team's unfair advantage?
8. What are you raising / what stage?
9. Do you have a brand colour? (defaults to Klein Blue `#002FA7`)
10. Do you have a logo file?

---

## What's in each file

| File | Purpose |
|------|---------|
| `SKILL.md` | Entrypoint — tells Claude what this skill is for, the two modes (CREATE / REVIEW), and how to run the interview |
| `references/content.md` | Slide-by-slide content guide — what to write on each of the 7 slides, the vertebrae method, story architecture |
| `references/design.md` | Design system + PptxGenJS code patterns — palette, typography, layout system, card helpers, chart config, QA checklist |

---

## Slides generated

1. **Cover** — company name, tagline, 3 key stats, raise amount
2. **Problem** — headline + 4 numbered pain point cards
3. **Product** — outcome headline + 2×2 workflow step cards
4. **Market** — TAM headline + bottoms-up math card + 2 number cards
5. **Traction** — growth headline + MRR line chart + stat cards
6. **Team** — unfair advantage headline + 2 founder cards
7. **Ask** — raise amount headline + 4 vertebrae summary cards

---

## Requirements

Claude uses [PptxGenJS](https://gitbun.com/gitbrent/PptxGenJS) to generate the file. When Claude runs the code in its environment, these are installed automatically. If you're running the generated code yourself:

```bash
npm install pptxgenjs
```

---

## Contributing

PRs welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

---

## License

MIT — see [LICENSE](LICENSE).
