# Federico Proverbio — Academic Website

A simple 3-page personal academic site: **Home** (bio + photo), **CV**, and **Research**.
No build tools, no frameworks — just plain HTML, CSS, and a couple of PDFs. You can edit
every page by opening the `.html` files in any text editor.

## Files

```
index.html        → Home page (bio + photo)
cv.html            → CV page (embeds cv/Proverbio_CV.pdf)
research.html      → Research projects page
style.css          → All styling (colors, fonts, layout) — edit this to restyle the whole site
images/            → Photos (replace the placeholder with your real photo here)
cv/                → Your CV PDF lives here
```

## 1. Add your real photo

1. Save a photo of yourself as `images/profile.jpg` (square-ish photos crop best).
2. Open `index.html`, find this line near the top of `<section class="hero">`:
   ```html
   <img src="images/profile-placeholder.svg" alt="Photo of Federico Proverbio">
   ```
   and change `profile-placeholder.svg` to `profile.jpg`.

## 2. Update your CV

Replace `cv/Proverbio_CV.pdf` with a newer export whenever you update it, **keeping the same
filename** — the site will pick it up automatically. If you rename the file, also update the
`href`/`src` in `cv.html`.

## 3. Add real research links

Open `research.html`. Each project has two placeholder links (`href="#"`) for a PDF and a
GitHub repo. Put your paper PDF in a `papers/` folder (create it next to `index.html`) and
point the link at it, e.g. `href="papers/homeownership_thesis.pdf"`. For GitHub, just paste
the repo URL, e.g. `href="https://github.com/yourname/your-repo"`.

## 4. Publish it for free with GitHub Pages

You don't need to know how to code to do this — just follow these steps.

1. **Create a GitHub account** at [github.com](https://github.com) if you don't have one.
2. **Create a new repository**:
   - Click the "+" in the top right → "New repository".
   - Name it exactly `<your-github-username>.github.io` (e.g. if your username is
     `federicoproverbio03`, name the repo `federicoproverbio03.github.io`). This exact name
     is what makes GitHub host it as a website automatically.
   - Set it to **Public**, and click "Create repository".
3. **Upload these files**:
   - On the new repo's page, click "uploading an existing file".
   - Drag in every file and folder from this project (`index.html`, `cv.html`,
     `research.html`, `style.css`, `images/`, `cv/`).
   - Scroll down and click "Commit changes".
4. **Turn on GitHub Pages**:
   - Go to the repo's **Settings** tab → **Pages** (left sidebar).
   - Under "Build and deployment" → "Source", choose **Deploy from a branch**.
   - Branch: `main`, folder: `/ (root)`. Click **Save**.
5. **Wait ~1 minute**, then visit `https://<your-github-username>.github.io`. Your site is live.

Any time you want to update the site, just edit the files and re-upload them (or, once you're
comfortable, use `git` from the command line — happy to walk you through that separately).

## 5. Add a custom domain later (optional)

When you're ready:
1. Buy a domain (e.g. from Namecheap, Google Domains successor Squarespace Domains, or IONOS).
2. In your repo's **Settings → Pages**, enter the domain under "Custom domain" — this creates
   a `CNAME` file in your repo automatically.
3. At your domain registrar, add a `CNAME` DNS record pointing your domain (or `www` subdomain)
   to `<your-github-username>.github.io`, following [GitHub's custom domain guide](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).

Come back and ask if you'd like help with this step when you're ready.
