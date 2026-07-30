# NYUSHDIC — Digital Innovation Community

A single-page bilingual (中文 / English) site introducing **NYU Shanghai DIC** and recapping the 5th Digital Innovation Challenge. Playful retro-OS / y2k aesthetic.

## Files

```
nyushdic-site/
├── index.html        ← the website (references images in assets/)
├── standalone.html   ← same site, all images embedded (one file, no assets/ needed)
├── assets/
│   ├── group.jpg      Innovation Day group photo (hero of the recap)
│   ├── panel.jpg      Panel Discussion with Judges — 决赛评委圆桌
│   ├── talk.jpg       Founder's Story guest talk — 嘉宾讲座
│   └── qr.png         WeChat group QR (see note below)
├── README.md
└── .gitignore
```

Use **index.html** for the repo / GitHub Pages. Use **standalone.html** only if you need to drop a single file somewhere without the `assets/` folder.

## View locally

Just open `index.html` in any browser. (Because it loads images from `assets/`, keep that folder next to it. If you prefer opening a single file directly, use `standalone.html`.)

## Publish free with GitHub Pages

1. Create a new GitHub repository and push the contents of this folder to it:
   ```bash
   git init
   git add .
   git commit -m "NYUSHDIC site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-repo>.git
   git push -u origin main
   ```
2. On GitHub: **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Select branch **main** and folder **/ (root)**, then **Save**.
5. Wait ~1 minute. Your site will be live at:
   `https://<your-username>.github.io/<your-repo>/`

To use a custom domain later, add it under Settings → Pages → Custom domain.

## Recolor the whole site in one place

Open `index.html` and find the block near the top marked:

```
🎨  COLOR CONTROL PANEL
```

- Change `--accent` to recolor the hero shadow, window title bars, and CTAs.
- `--header-accent` controls the "Q ▸ section" tab headers; `--bar-accent` the recap loading bar.
- The five base colors (`--blue --coral --yellow --mint --lilac`) drive the stat tiles and the multi-color wordmark. Edit those to reshuffle the palette everywhere.

## Notes / things to update

- **QR code expiry:** `assets/qr.png` was generated from a WeChat *group* invite that expires. For a permanent site, replace it with a non-expiring QR (e.g. your official account / DICtionary channel). Just overwrite `assets/qr.png` with the same filename — no code change needed. (If you use standalone.html, re-embed it or ask for a fresh build.)
- All copy is bilingual and can be edited directly in the HTML.
- Content is based on the official 5th DIC recap: theme *"AI Agent Unlock Business Innovation"*, 75 teams from 6 countries, 9 finalists, tracks Education / Healthcare / Finance; partners Tencent, Henlius, ChillPrep; guided by NYU Shanghai's CSDSE and Data Science center.
