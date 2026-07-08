# AG Luxe Lab — Portfolio Site

A single-page, mobile-responsive portfolio for Alison Gonzalez / AG Luxe Lab. Pure HTML, CSS, and vanilla JavaScript — no build step, no backend, no paid dependencies. Works by simply opening `index.html`, and is ready to deploy on GitHub Pages.

## File structure

```
index.html     — all page content and sections
styles.css     — all styling (colors, layout, responsiveness, animations)
script.js      — mobile menu + scroll-reveal animation
assets/        — resume PDF, and optional favicon / OG image
README.md      — this file
```

## 1. Preview it locally

No server or install required. Just double-click `index.html` (or right-click → Open With → your browser). Every link, style, and script is a relative file path, so it works straight from your file system.

## 2. Add your resume PDF

Place your resume file inside the `assets` folder using **exactly** this file name:

```
assets/Alison_Gonzalez_Resume_Rewritten.pdf
```

The "Download Resume" buttons in the Hero and Contact sections already point to this exact path — if the file name doesn't match, the download links will 404.

## 3. Replace placeholder client links

A few client links weren't available yet, so they're filled in with clearly-labeled placeholders like `ADD_AESTHETIC_SMILES_WEBSITE_LINK`. To find and update them:

1. Open `index.html` in your editor.
2. Search for `ADD_` (or `is-placeholder`) to jump to every placeholder link.
3. Replace the placeholder text inside the `href="..."` attribute with the real URL.
4. Once a real link is in place, you can also remove the `is-placeholder` class from that `<a>` tag — it's only there to give unfinished links a dashed border so they're easy to spot before launch.

Placeholders currently in the file:

- `ADD_INSTAGRAM_LINK` — personal/business Instagram (used in the Hero and Footer)
- `ADD_AESTHETIC_SMILES_WEBSITE_LINK`, `ADD_AESTHETICS_PAGE_LINK`, `ADD_SPECIFIC_SERVICE_PAGE_LINK` — Aesthetic Smiles of Queen Creek card
- `ADD_THE_BEAUTY_CLUB_INSTAGRAM_LINK`, `ADD_EVENT_OR_COMMUNITY_LINK` — The Beauty Club card
- `ADD_AG_LUXE_LAB_WEBSITE_LINK`, `ADD_AG_LUXE_LAB_INSTAGRAM_LINK` — AG Luxe Lab card

To add work from a new client, copy an existing `<article class="card portfolio-card">` block inside the `#client-work` section and edit the text, category tag, highlights, and buttons.

## 4. Upload this project to GitHub

If you don't already have a repository for this site:

1. Create a new repository on GitHub (e.g. `ag-luxe-portfolio`). Leave it empty — no README, license, or .gitignore.
2. In this project folder, run:

   ```bash
   git init
   git add .
   git commit -m "Initial portfolio site"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
   git push -u origin main
   ```

   Replace `YOUR-USERNAME/YOUR-REPO-NAME` with your actual GitHub username and repository name.

## 5. Turn on GitHub Pages

1. On GitHub, open your repository → **Settings** → **Pages**.
2. Under **Build and deployment** → **Source**, choose **Deploy from a branch**.
3. Under **Branch**, select `main` and folder `/ (root)`, then click **Save**.
4. GitHub will publish the site to a URL like `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/` within a minute or two.

## 6. Optional finishing touches

- **Favicon**: add a `favicon.ico` (or `favicon.png`) file to `assets/`, then uncomment the `<link rel="icon" ...>` line near the top of `index.html`.
- **Open Graph image** (the preview image shown when the link is shared on social/text): add a `1200x630` image to `assets/og-image.jpg`, then uncomment the `<meta property="og:image" ...>` line in `index.html`.

## File names that must stay the same

- `index.html`, `styles.css`, and `script.js` — the page links to these by exact name.
- `assets/Alison_Gonzalez_Resume_Rewritten.pdf` — the Download Resume buttons link to this exact path.

Everything else (client names, links, copy) can be edited freely inside `index.html`.
