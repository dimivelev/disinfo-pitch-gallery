# Disinfo Analyzer — Pitch Deck Gallery

A gallery of self-contained HTML pitch decks for **Disinfo Analyzer**, a multi-agent AI Chrome extension that analyzes any web page for **clickbait, emotional manipulation, political bias, and conspiracy theories** in real time.

One product, presented eight ways — **four visual styles** and **four audiences**.

👉 **Live gallery:** _(GitHub Pages URL appears here once published)_

## The decks

Each deck is a single, dependency-free `.html` file: 16:9, keyboard-navigable, and print-to-PDF ready.

### By visual style (hackathon content)
| Deck | Look |
|------|------|
| [`decks/gradient-hackathon.html`](decks/gradient-hackathon.html) | Modern gradient — vibrant, rounded glass cards |
| [`decks/cyber-hackathon.html`](decks/cyber-hackathon.html) | Bold dark cyber — neon, monospace, threat-intel |
| [`decks/editorial-hackathon.html`](decks/editorial-hackathon.html) | Clean editorial — light, serif, journalistic |
| [`decks/alarm-hackathon.html`](decks/alarm-hackathon.html) | High-contrast alarm — black & red, urgent |

### By audience (modern-gradient look)
| Deck | Audience |
|------|----------|
| [`decks/gradient-hackathon.html`](decks/gradient-hackathon.html) | Hackathon / demo judges |
| [`decks/gradient-investors.html`](decks/gradient-investors.html) | Investors / VC |
| [`decks/gradient-grant.html`](decks/gradient-grant.html) | Grant / policy / research funding |
| [`decks/gradient-general.html`](decks/gradient-general.html) | General / all-purpose |

## Using a deck
- **Navigate:** `←` `→`, `Space`, `PageUp/Down`, on-screen dots, or swipe.
- **Fullscreen:** press `F`.
- **Export to PDF:** open the deck → `Ctrl/Cmd+P` → **Save as PDF**, **Landscape**, margins **None**, **Background graphics** on. Each slide becomes one 16:9 page.

## Note on figures
Market sizes, statistics, and funding asks in the investor and grant decks are **illustrative placeholders** — replace them with real data before presenting.

## About the product
- **4 AI agents** orchestrated by **CrewAI** (sequential), reasoning via **Gemini 2.5 Flash**, each wrapping a fine-tuned transformer:
  1. **Headline Analyzer** — clickbait via headline↔body semantic similarity
  2. **Emotional Manipulation Analyst** — GoEmotions classification
  3. **Bias Detection Analyst** — political lean (Left / Center / Right), trained on MBIC
  4. **Conspiracy Detector** — 7-trait conspiratorial-thinking framework (Vaccine / GMO / 5G)
- **Flow:** Chrome MV3 extension captures the active tab's HTML → **FastAPI** parses it (Newspaper3k) → per-request **CrewAI** crew → results **streamed** back live via Server-Sent Events.
- **Stack:** Python · FastAPI · CrewAI · PyTorch · Transformers · Gemini 2.5 Flash · Chrome MV3 · Docker · GitHub Actions · Google Cloud Run.

---
Built with [Claude Code](https://claude.com/claude-code).
