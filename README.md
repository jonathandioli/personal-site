# jonathandioli.com

Static Astro site. Edit links, email and headshot in `src/config.ts`. Page copy lives in `src/pages/index.astro`.

```bash
npm install
npm run dev      # http://localhost:4321
npm run build    # static output in dist/
```

## Deploy to Vercel
- Quickest: `npx vercel` from this folder, then `npx vercel --prod`.
- Or push to GitHub and import the repo in Vercel (framework auto-detects as Astro, no settings needed).
- Domains: add `www.jonathandioli.com` (primary) and `jonathandioli.com` in Vercel, then point DNS as Vercel instructs. `vercel.json` 301s the bare domain to www.
- After launch: submit `https://www.jonathandioli.com/sitemap-index.xml` in Google Search Console.

## AI-search setup
- Person + ProfilePage JSON-LD (worksFor FlyDragon, alumniOf Bentley, sameAs LinkedIn, knowsAbout) in `src/layouts/Base.astro`.
- `/llms.txt` gives AI crawlers a clean fact sheet. Keep it in sync with the page when numbers change.
- Add the site URL to your LinkedIn profile (Contact info → Website) and FlyDragon's team/about page so the entity links both ways.
