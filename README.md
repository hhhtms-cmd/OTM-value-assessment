# OTM Value Assessment

Interactive web tool that helps a prospective customer discover whether they have
a transportation problem worth solving, what it's worth in dollars, and whether
Oracle Transportation Management (OTM) — optionally plus Global Trade
Management (GTM) — is a good way to solve it.

- App: single React component in `src/App.jsx` (no backend; all client-side)
- Stack: React 18 + Vite + Tailwind CSS + lucide-react + recharts
- Engineering handoff doc: see `docs/OTM_Value_Assessment_Engineering_Handoff.docx`
  (original, in `~/workspace/user/files/`)

## Local dev

```
npm install
npm run dev
```

## Deploy

Pushes to `main` auto-deploy to GitHub Pages via `.github/workflows/deploy.yml`.

## Known limitation

The AI executive-summary button calls Anthropic's API directly from the browser,
which only works inside the Claude.ai artifact sandbox. On this hosted site it
will show its error state until `fetchAISummary` is wired to a real backend —
see Section 10 of the handoff doc for the exact swap point and payload contract.
