# Prompt-Generator

**Dr. Sharon's AI Prompt Generator** — a simple chat-style app that turns any task description into one polished, copy-ready prompt using the **RACE framework** (Role · Action · Context & Constraints · Examples).

## Features
- Landing page with a single **Start** button
- Chat window: describe your task → get **one** RACE prompt in a box with a **Copy** button
- Optional **Target AI** selector: Any AI, ChatGPT, Claude, Gemini, Grok, Image generator — the prompt is adapted to each model's best practices
- Ask for changes in plain language and get the full revised prompt back
- **New prompt** button to start over
- Single self-contained `index.html` — no build step, no dependencies

## How it works
The prompt-engineering rules (the RACE workflow, text- and image-task guidance, defaults, model adaptation and safety rules) live in the `SYSTEM` constant at the top of the `<script>` in `index.html`. Edit it to change how prompts are written.

The app calls Claude through the claude.ai artifact runtime (`window.claude.use("sample")`). It therefore runs as a **claude.ai artifact**, where each user signs in with their own Claude account.

### Running it outside claude.ai
Opened directly (or on GitHub Pages) the interface loads, but generation shows "The prompt engine isn't available in this view". To host it elsewhere, replace the `getSample()` function with a call to your own backend (e.g. a small server proxying the Anthropic or OpenAI API). Never put an API key in the browser code.

## Files
| File | Purpose |
|---|---|
| `index.html` | The complete app (HTML, CSS, JS) |
| `README.md` | This file |

## Author
Dr. Sharon Baisil, MBBS, MD — Associate Professor of Community Medicine, MOSC Medical College, Kolenchery, Kerala · drsharonbaisil@gmail.com
