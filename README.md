# Vanthara Group

The group hub page for **vantharagroup.com** — a single static page introducing
the three Vanthara businesses with an animated, auto-scrolling carousel
(pauses on hover, click any card to open that business's site):

- 🏡 Vanthara Homestay → vantharahomestay.com
- 🐓 Vanthara One Farm → vantharaonefarm.com
- 🌿 SVT Foods → svtfoods.com

No build step, no framework, no database — it's one self-contained
`index.html` file (HTML + CSS + a couple lines of JS for the footer year).

## Deploy it (GitHub + Vercel, same flow as the other Vanthara sites)

1. Create a new repo on GitHub (e.g. `vanthara-group`) and push this folder:
   ```bash
   cd vanthara-group
   git init && git add -A && git commit -m "Initial site"
   git remote add origin https://github.com/<you>/vanthara-group.git
   git push -u origin main
   ```
2. In the Vercel dashboard: **Add New → Project → Import Git Repository**,
   pick the repo. Framework preset can stay "Other" — there's nothing to
   build. Deploy.
3. **Settings → Domains → Add**, enter `vantharagroup.com`, and add the DNS
   records Vercel shows you at your registrar (same A/CNAME pattern used for
   vantharaonefarm.com).

## Editing content

Everything — copy, colors, links — lives in the one `index.html` file.
The three company cards are duplicated once (Set A + Set B, marked
`aria-hidden`) purely so the marquee scroll loops seamlessly; if you change
the copy for a card, change it in both places.
