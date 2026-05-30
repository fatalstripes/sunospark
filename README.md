# SunoSpark

[![Live Demo](https://img.shields.io/badge/Live%20Demo-fatalstripes.github.io%2Fsunospark-10b981?style=for-the-badge&logo=vercel&logoColor=white)](https://fatalstripes.github.io/sunospark/)
[![GitHub](https://img.shields.io/badge/GitHub-fatalstripes%2Fsunospark-181717?style=for-the-badge&logo=github)](https://github.com/fatalstripes/sunospark)

A beautiful, zero-dependency web app that generates high-quality, ready-to-use prompts for **Suno 5.5** (with Classic mode support).

Just open `index.html` in any modern browser. No install, no build step, no backend.

## 🚀 Live Demo

**Try it now:** [https://fatalstripes.github.io/sunospark/](https://fatalstripes.github.io/sunospark/)

## Features

- **Suno 5.5 Optimized** — Generates rich, descriptive paragraph prompts that actually perform well in the latest model
- **Classic Split Mode** — Traditional Style + Theme/Description format for older versions
- **Smart Generation** — Creates 8 varied, high-quality prompts per click
- **Guided Inputs** — Genre/style + Theme/vibe, plus Energy, Vocals, and Era filters
- **One-Click Copy** — Copy full prompts (and optional style hints) instantly
- **"Use in Suno 5.5"** — Copies the prompt and opens Suno in a new tab
- **Favorites** — Heart any prompt to save it permanently (localStorage)
- **Surprise Me** — Instant random high-quality inspiration
- **Pro Tips** — Built-in current advice for writing better Suno 5.5 prompts
- **Fully Offline** — Everything runs in your browser

## How to Use (5.5 Mode)

1. Open `index.html` (defaults to 5.5 Optimized)
2. (Optional) Enter genre and/or theme
3. Pick Energy / Vocals / Era if desired
4. Hit **Generate 8 Powerful Prompts**
5. Copy the big **Full Prompt** block and paste it into Suno’s main prompt box
6. (Optional) Copy the short Style Hint into the Style field

### Keyboard Shortcuts
- `/` — Focus the Genre input
- `Cmd/Ctrl + Enter` — Generate

## Tips for Suno 5.5

- The **main prompt box** now does most of the work. Write rich, flowing descriptions instead of comma lists.
- Include emotional atmosphere, sonic details, and scene setting in one cohesive paragraph.
- Strange genre combinations still work great in 5.5.

## Tech

- Single HTML file
- Tailwind CSS via CDN
- Font Awesome icons
- Pure vanilla JavaScript
- Works completely offline after first load

## Project Structure

```
sunospark/
├── index.html    # The entire app
└── README.md
```

## Future Ideas

- Export favorites as JSON
- "Remix this idea" button
- More sophisticated generation rules

---

Made for Suno creators. Enjoy. 🎵

**SunoSpark** — Spark great ideas.