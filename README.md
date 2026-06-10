# Blue Wave Construction — bluewavela.com

Single-page placeholder site for Blue Wave Construction, a licensed,
owner-operated general contractor serving the South Bay of Los Angeles.

Plain HTML/CSS, no framework, mobile-responsive, hosted free on GitHub Pages.
Everything lives in **`index.html`** (CSS is embedded for speed and easy editing).

> This is a lightweight launch presence — not the full marketing site. Iterate
> here until the portfolio photos and full site are ready.

## Repo layout

```
index.html                ← the whole site (HTML + CSS)
CNAME                      ← custom domain for GitHub Pages (bluewavela.com)
.nojekyll                  ← serve files as-is, skip Jekyll processing
images/
  README.md               ← where to put logo.svg and estimate.pdf
  projects/
    README.md             ← how to add gallery photos
```

## Editing the common things

| What | Where |
|------|-------|
| Brand colors (navy, wave accent) | `:root` block at the top of the `<style>` in `index.html` |
| Logo | replace the `.logo-slot` placeholder in the header — see `images/README.md` |
| Phone / email / license | search those values in `index.html` (they appear in hero, contact, footer) |
| Gallery photos | add tiles in `<div class="gallery">` — see `images/projects/README.md` |

The brand colors are intentionally set as variables so you can match them to the
estimate PDF in one place once it's in the repo.

---

## Deploying to GitHub Pages

You can use **either** repo name — both work the same with a custom domain:

- **`bluewavela.com`** (a normal project repo), or
- **`Beachbum420.github.io`** (a user/organization site repo)

### 1. Create the repo and push

```bash
cd /Users/ryan/BlueWave_LA_Website
git init
git add .
git commit -m "Initial Blue Wave Construction landing page"
git branch -M main

# Replace REPO with bluewavela.com  OR  Beachbum420.github.io
gh repo create Beachbum420/REPO --public --source=. --remote=origin --push
# (or create the repo on github.com and: git remote add origin <url> && git push -u origin main)
```

### 2. Turn on Pages

On GitHub: **Settings → Pages → Build and deployment**
- **Source:** Deploy from a branch
- **Branch:** `main` / `/ (root)` → **Save**

Within a minute the site is live at the temporary URL
(`https://beachbum420.github.io/REPO/` or `https://beachbum420.github.io/`).

### 3. Custom domain

The included **`CNAME`** file already sets the domain to `bluewavela.com`, so the
custom-domain field on the Pages settings page should populate automatically.
If it doesn't, type `bluewavela.com` into **Custom domain** and Save.

---

## Pointing bluewavela.com at the site (DNS)

Do this at your domain registrar (wherever you bought bluewavela.com — e.g.
Namecheap, GoDaddy, Google Domains/Squarespace, Cloudflare).

### A) Apex domain `bluewavela.com` — four **A** records

| Type | Host/Name | Value |
|------|-----------|-------|
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |

(Optional but recommended — the same four as **AAAA** records for IPv6:
`2606:50c0:8000::153`, `2606:50c0:8001::153`, `2606:50c0:8002::153`,
`2606:50c0:8003::153`.)

### B) `www.bluewavela.com` — one **CNAME** record

| Type | Host/Name | Value |
|------|-----------|-------|
| CNAME | `www` | `beachbum420.github.io.` |

> Use **your** GitHub username here. The value is always
> `<username>.github.io.` — it does **not** change based on repo name.

### C) Finish up

1. Wait for DNS to propagate (often minutes, up to ~24h). Check with:
   ```bash
   dig +short bluewavela.com
   ```
   It should return the four `185.199.x.153` addresses.
2. Back in **Settings → Pages**, confirm the custom domain shows a green check,
   then tick **Enforce HTTPS** (it may take a few minutes for the certificate to
   be issued — if it's greyed out, wait and refresh).

That's it — `https://bluewavela.com` will serve this page, and `www` will
redirect to it.

## Local preview

Just open `index.html` in a browser, or:

```bash
python3 -m http.server 8000   # then visit http://localhost:8000
```
