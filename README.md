# text-summarizer-v3

A set of standalone React UI component snippets for text summarization and text analysis dashboards. These are drop-in components (built with React + shadcn/ui-style primitives) meant to be pasted into an existing React project — not a full standalone application.

## What's inside

| File | Description |
|------|-------------|
| `text-summarizer v3` | Text summarizer card: textarea input, summary-length slider, copy button, loading state; calls a Gemini API for summarization |
| `text-analyzer v6` | Rich text-analysis panel with animated results (Framer Motion) |
| `text-analyzer v7` | Variant of the text-analysis panel with file-input support |

All components import from React, `@/components/ui/*` (shadcn/ui button, card, textarea, label, slider), `lucide-react` icons, and `framer-motion` for animations.

## Quick start

These files have no `package.json` — they are components, not an app. To use them:

1. Copy the file you need into your React project's components folder (rename it without spaces, e.g. `TextSummarizer.tsx`).
2. Make sure your project has shadcn/ui components (`button`, `card`, `textarea`, `label`, `slider`), `lucide-react`, and `framer-motion` installed.
3. Import and render the component like any other React component.

```bash
npm install lucide-react framer-motion
```

## Tech stack

- React (hooks: `useState`)
- shadcn/ui primitives (button, card, textarea, label, slider)
- Tailwind CSS utility classes
- Framer Motion (animated transitions)
- lucide-react icons
- Google Gemini API (summarization backend)

## Environment variables

The summarizer component currently uses a **hardcoded Gemini API key**. You should replace it with an environment variable before any real use:

```tsx
const API_KEY = process.env.NEXT_PUBLIC_GEMINI_API_KEY
```

> ⚠️ **Security note:** the key committed in this repo's history is exposed publicly. Rotate/revoke it in the Google AI Studio dashboard and never commit keys again.

## Deploy notes

No deployment — this repository contains source components only, not a runnable website. To ship one as a page, drop the component into a Vite/Next.js project and deploy that.

## License

See `LICENSE`.

---

Built by Girish Lade — https://ladestack.in
