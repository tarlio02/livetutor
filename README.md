# Chalkline — AI Whiteboard Tutor

A university-level AI tutor that teaches on an infinite white whiteboard: it writes and draws with a live animated pen, narrates with voice, shows live captions, takes voice or text questions, imports PDFs to teach from, quizzes you, and saves full sessions to resume later.

**Live site:** `https://<your-username>.github.io/<repo-name>/`
*(replace with your actual GitHub Pages URL once deployed — see below)*

## Before you can use it: bring your own API key

This site runs entirely in your browser — there is no server, and nobody but you can see what you type or paste. To keep it free to host, it does **not** come with a shared AI key. You provide your own:

- **Claude** — get a key at [console.anthropic.com](https://console.anthropic.com) (Anthropic's API is pay-as-you-go; a small top-up like $5 goes a long way for personal tutoring use)
- **OpenAI (GPT)** — get a key at [platform.openai.com](https://platform.openai.com)
- **Google Gemini** — get a *free* key at [aistudio.google.com/apikey](https://aistudio.google.com/apikey) (no card required; free tier is rate-limited to a modest number of requests per minute/day, which is plenty for personal tutoring use)

Open the menu (☰ top-left) → **AI brain** → pick Claude, OpenAI, or Gemini → paste your key. It's kept only in your browser tab's memory for that session — never saved to disk, never sent anywhere except directly to the AI provider you picked.

## What it does

- **Live whiteboard drawing** — the tutor writes headings, equations, diagrams, and graphs stroke-by-stroke with an animated pen, on an infinite pannable/zoomable white canvas
- **Voice narration** — speaks every explanation aloud using your browser's best available voice, with synced captions
- **Voice or text input** — click the mic and talk, or type follow-up questions
- **Teaches in small steps** — explains one idea at a time and checks in ("does that make sense? should we continue?") rather than lecturing non-stop
- **PDF import** — drop in a textbook chapter, slide deck, or notes; the tutor grounds its explanations in your actual material
- **Quizzes** — ask to be quizzed any time; get instant feedback and explanations
- **Save & resume sessions** — sessions (transcript, board, quiz history, PDF context) are saved in your browser and listed in the menu to reopen later

## Browser requirements

- **Voice input (microphone)** works best in Chrome or Edge; not supported in Firefox or Safari
- **Voice output** works in all modern browsers, quality varies by OS (Chrome/Edge on Windows or Mac tend to have the best-sounding voices)
- Works on desktop and mobile browsers, though the whiteboard is easiest to use on a larger screen

## Deploying your own copy (GitHub Pages)

1. Create a new GitHub repository (public, since GitHub Pages' free tier requires public repos unless you have GitHub Pro/Team)
2. Upload `index.html` and this `README.md` to the repository (via the GitHub web UI's "Add file → Upload files", or `git push` if you're comfortable with git)
3. In the repository, go to **Settings → Pages**
4. Under "Build and deployment", set **Source** to "Deploy from a branch"
5. Set **Branch** to `main` (or `master`) and folder to `/ (root)`, then **Save**
6. Wait 1–2 minutes, then refresh the Pages settings page — it will show your live URL, typically `https://<your-username>.github.io/<repo-name>/`

That's it — no build step, no server, no configuration files needed. It's a single static HTML file.

## Privacy note

Your API key, PDF content, and session history all stay in your own browser (using its local storage). Nothing is sent to any server except the AI provider (Anthropic or OpenAI) you choose, and only when you ask the tutor something.
