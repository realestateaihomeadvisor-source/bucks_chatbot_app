# Bucks County Home Advisor — Chat Only

Standalone Voiceflow chatbot page for deploy on a subdomain (e.g. `chat.yourdomain.com`).

## What’s included

- `index.html` — full-viewport, mobile-responsive chat only
- Same Voiceflow project as the main site (`6a5e538a8fc5be81b40d77d5`)
- Session reset via `userID` + optional `?resetChat=1`
- Legal disclaimer under the chat

## Deploy to Vercel (new project)

1. Create a **new empty GitHub repo**
2. Copy everything inside this `chat-standalone` folder into that repo root (so `index.html` is at the root)
3. Push to GitHub
4. In Vercel → **Add New Project** → import that repo
5. Framework Preset: **Other** (static HTML) → Deploy
6. In Vercel → Project → Settings → Domains → add `chat.yourdomain.com`
7. At your DNS provider, add a CNAME: `chat` → `cname.vercel-dns.com`

## Local preview

Open `index.html` in a browser, or from this folder:

```bash
npx serve .
```

## Notes

- Do not change `autostart: true` — greeting will break
- Do not remove `userID` logic — sessions will stick between visitors
- Main marketing site stays separate; this URL is chat-only
