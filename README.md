# TroutHound — Fly Fishing & Fly Tying

Free static website for **trouthound.com**.

## Contents

- `index.html` — Home
- `fly-fishing.html` — Gear, casts, reading water, tactics
- `fly-tying.html` — Tools, materials, techniques
- `patterns.html` — Classic trout patterns with materials lists
- `resources.html` — Glossary, tippet chart, starter kit
- `about.html` — About the site
- `css/styles.css` — Styles
- `js/main.js` — Mobile nav + active page highlight

No build step. No paid services. Pure HTML/CSS/JS.

---

## Deploy for free (choose one)

### Option 1 — GitHub Pages (recommended)

1. Create a free GitHub account and a new repository (e.g. `trouthound`).
2. Upload all files in this folder to the repo (keep the same structure).
3. Go to **Settings → Pages**.
4. Under "Source", choose the `main` branch and `/ (root)`, then Save.
5. Your site will be at `https://YOURUSERNAME.github.io/trouthound/`.
6. Point **trouthound.com** to GitHub Pages:
   - In your domain registrar, add a CNAME record: `trouthound.com` → `YOURUSERNAME.github.io`
   - In the repo, add a file named `CNAME` containing: `trouthound.com`
   - In Pages settings, set the custom domain to `trouthound.com` and enable HTTPS.

### Option 2 — Netlify

1. Go to [netlify.com](https://www.netlify.com) and sign up free.
2. Drag-and-drop this entire folder onto the Netlify dashboard, **or** connect a GitHub repo.
3. Under Domain settings, add custom domain `trouthound.com` and follow the DNS instructions.
4. HTTPS is automatic.

### Option 3 — Vercel

1. Go to [vercel.com](https://vercel.com) and sign up free.
2. Import the project (or deploy the folder).
3. Add domain `trouthound.com` in project settings and update DNS as instructed.

---

## Local preview

Open `index.html` in any browser, or run a simple local server:

```bash
# Python
python3 -m http.server 8000

# Then visit http://localhost:8000
```

---

## Customizing

- Brand colors are in `css/styles.css` under `:root`.
- Add new pattern cards by copying an existing block in `patterns.html`.
- All pages share the same header/footer — edit carefully for consistency.

Built for anglers. Free forever.

---

## Adding Images & Videos (now)

### Folders ready for you
```
images/
  hero/       ← home page / large banners
  patterns/   ← one photo per fly pattern
  gear/       ← rods, reels, setups
  tying/      ← vise, materials, step photos
  blog/       ← ready for future blog posts
videos/       ← optional local .mp4 files (keep small)
```

### How to add an image
1. Put the file in the right folder (e.g. `images/patterns/woolly-bugger.jpg`).
2. In the HTML, find the comment that looks like:
   ```html
   <!-- <img src="images/patterns/woolly-bugger.jpg" alt="Woolly Bugger" loading="lazy"> -->
   ```
3. Uncomment it (remove `<!--` and `-->`) and delete the emoji placeholder.

**Tips:** Use JPG or WebP, max ~1600px wide, under 300 KB each. Always include `loading="lazy"`.

### How to add a video (recommended: YouTube/Vimeo)
1. Upload the video to YouTube (can be Unlisted).
2. Click Share → Embed → copy the `src` URL (looks like `https://www.youtube.com/embed/abc123`).
3. Paste it into any `<iframe src="...">` that currently says `YOUR_VIDEO_ID`.

Local video alternative:
```html
<video class="video-local" controls preload="metadata" poster="images/tying/poster.jpg">
  <source src="videos/woolly-bugger.mp4" type="video/mp4">
</video>
```
Prefer YouTube/Vimeo so you don’t burn free hosting bandwidth.

### Future: Blog & Store
- **Blog**: Add new HTML pages (or later switch to a free static generator). The `images/blog/` folder is already there.
- **Store**: Start with Gumroad / Payhip / Stripe Payment Links + simple product pages on this same static site. No need to leave free hosting until you have real sales volume.
