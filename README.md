# ryanspoonworship.com: personal homepage (DRAFT)

Static site for GitHub Pages. Nothing here has been published.

```
index.html             homepage: kits first (single file, inline CSS)
about/index.html       About Me page  -> ryanspoonworship.com/about/
mentorship/index.html  Mentorship page -> ryanspoonworship.com/mentorship/ (sign-ups go to Flodesk checkout)
assets/                photos from the Flodesk page + kit covers (page 1 of each kit PDF)
CNAME                  ryanspoonworship.com
preview-*.png          review screenshots (home, about, mentorship × desktop/mobile). Delete before publishing.
```

Before going live, fill in or remove every gold `[PLACEHOLDER]` tag in `index.html`, `about/index.html` and `mentorship/index.html`.

## Publish on GitHub Pages (free)

1. Create a **public** repo, e.g. `ryanspoonworship-site` (Pages is free on public repos).
2. Upload the contents of this folder to the repo root (`index.html` and `CNAME` at the top level).
3. Go to Repo → **Settings → Pages**. Set Source to *Deploy from a branch*, Branch to `main` and folder to `/ (root)`, then click Save.
4. In the same page, under **Custom domain**, enter `ryanspoonworship.com` and save.
   Optional but recommended: first verify the domain under GitHub → Settings (your profile) → Pages → *Add a domain*.
5. Once DNS works (below), tick **Enforce HTTPS**. The certificate can take up to about 24 hours.

## DNS (at the registrar where you bought ryanspoonworship.com)

**First remove the current forwarding/redirect** to the Flodesk page, then add:

| Type  | Host / Name | Value |
|-------|-------------|-------|
| A     | @           | 185.199.108.153 |
| A     | @           | 185.199.109.153 |
| A     | @           | 185.199.110.153 |
| A     | @           | 185.199.111.153 |
| AAAA (optional) | @ | 2606:50c0:8000::153, 2606:50c0:8001::153, 2606:50c0:8002::153, 2606:50c0:8003::153 |
| CNAME | www         | `<your-github-username>.github.io` |

Check https://docs.github.com/pages/configuring-a-custom-domain-for-your-github-pages-site before you change anything, in case these addresses have changed. Don't use wildcard (`*`) records.

Once this is set up, `ryanspoonworship.com/mentorship/` is a real page on this site. Its Join buttons still go to the Flodesk checkout, and Book a call goes to Calendly.
All links between pages are relative (`../`, `about/`, `mentorship/`), so they work on GitHub Pages. If you open the files straight from your computer, folder links may show a file listing instead of the page. That's normal.

## Fonts
- **Albert Sans** (Google Fonts, free). This is the same family the Flodesk page uses for body text and its main headings.
- **Playfair Display** (Google Fonts, free) stands in for **Freight Big Pro**, the serif used on the Flodesk page. Freight Big Pro is an Adobe font and needs a license. If you have Adobe Fonts, you can add it to a web project and swap it into `--serif`.

## Prices and dates on the site (Steeple's suggested pricing)
- **Christmas & End-of-Year Giving Kit:** on sale Thu Nov 12, 2026. Single church $24. Team license is a $4 add-on per additional license. Multi-campus $99. Multi-campus option may change.
- **Prompt Master Kit:** launches Tue Jan 19, 2027. $39 founding price through Mon Jan 25, 2027, then $49.
- **Sunday-Week Starter Pack:** free, coming Sun Nov 15, 2026.
- **Mentorship:** The Cohort $150/mo, The Inner Circle $350/mo.

This is a static site, so prices don't change by themselves. After Mon Jan 25, 2027, edit `index.html` to drop the Master Kit founding-price lines. Keep the prices in Payhip the same as the prices on the site.
