# SunoSpark

A beautiful, zero-dependency web app that generates high-quality, ready-to-use prompts for **Suno 5.5** (with Classic mode support).

Just open `index.html` in any modern browser. No install, no build step, no backend.

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

## Using with Local AI (Ollama, LM Studio, etc.)

The Lyric Generator supports any OpenAI-compatible endpoint, including local models.

### Ollama (recommended for local)

1. Install and run [Ollama](https://ollama.com)
2. Pull a good model:
   ```bash
   ollama pull gemma3:4b          # Your current model
   # or better quality:
   ollama pull gemma2:9b
   ollama pull llama3.1:8b
   ```
3. In SunoSpark → Lyric Generator:
   - **Provider**: OpenAI Compatible
   - **Base URL**: `http://localhost:11434/v1`
   - **Model**: Use the exact name from `ollama list` (e.g. `gemma3:4b`)
   - **API Key**: Leave blank

**Note for small models (like gemma3:4b):** Smaller models benefit from very clear instructions. Use the "Custom Instructions" box to tell it the desired structure, style, and length.

4. **If you're using the live web version (https://fatalstripes.github.io/sunospark)**: Browsers block HTTPS pages from calling http://localhost for security. 
   - Click the **"Download for Local AI"** button in the Lyric Generator panel.
   - Open the downloaded `SunoSpark-local.html` file directly from your computer (it will use the `file://` protocol and work perfectly with Ollama).
   - Use the new **"Test"** button for instant connection diagnostics.

   If you stay on the live site you will also need a CORS Unblock extension, but the downloaded local copy is far more reliable.

#### Windows Notes (Ollama Desktop App)

Most Windows users install the official Ollama desktop app. This app automatically starts a background server. Because of this, you will often see "bind: Only one usage of each socket address" when trying to run `ollama serve`.

**Quick test method:**
1. Right-click the Ollama icon in the system tray (bottom right) → **Quit**
2. Open PowerShell and run:
   ```powershell
   $env:OLLAMA_ORIGINS="*"; ollama serve
   ```
   Leave this window open while testing.

**Recommended permanent fix (no extra terminal window needed):**
```powershell
[System.Environment]::SetEnvironmentVariable('OLLAMA_ORIGINS', '*', 'User')
```
Then fully quit the Ollama app (tray → Quit) and restart it normally. The desktop app will now start the server with CORS allowed.

When stuck, use the **Test** button in SunoSpark — it gives detailed Windows-specific guidance including the exact commands above. You can also diagnose the port with:
```powershell
Get-NetTCPConnection -LocalPort 11434
Get-Process | Where-Object { $_.ProcessName -match 'ollama' }
```

### Other Local Tools
- **LM Studio**: Use Base URL `http://localhost:1234/v1`
- Most tools that expose an OpenAI-compatible `/v1` endpoint will work.

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