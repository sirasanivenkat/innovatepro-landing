# InnovatePro — Landing Page

This repository contains a single-file landing page built with HTML + Tailwind CSS (via CDN). It implements a modern, responsive design covering:

- Navigation Bar (brand, links, responsive mobile menu)
-- Hero Section (headline, subtext, CTAs, illustrative image from Unsplash)
- Services / Features (6 cards, responsive grid)
- Contact / Lead Form (Name, Email, Company, Message, privacy checkbox)
- Footer (4-column layout, social icons)

Files:
- `hero.html` — the full landing page. Open in a browser to preview.

Quick preview locally
---------------------
Open the page in your default browser (PowerShell):

```powershell
Start-Process 'c:\Users\svenk\Downloads\pythonvs\Pinak Idea Lab Private Limited assignment\hero.html'
```

Recommended hosting options
---------------------------
Below are two quick hosting options. Choose whichever you prefer.

Option A — GitHub Pages (recommended)
1. Create a new GitHub repository (public) via the website or `gh` CLI.

With the `gh` CLI (optional):
```powershell
cd 'C:\Users\svenk\Downloads\pythonvs\Pinak Idea Lab Private Limited assignment'
git init
git add hero.html README.md
git commit -m "Add landing page"
gh repo create <YOUR_USERNAME>/<REPO_NAME> --public --source=. --remote=origin
git branch -M main
git push -u origin main
```

If you created the repo via the GitHub website, add the remote and push:
```powershell
git remote add origin https://github.com/<YOUR_USERNAME>/<REPO_NAME>.git
git branch -M main
git push -u origin main
```

Then enable GitHub Pages for the repository:
- Go to the repository Settings -> Pages
- Source: Select `main` branch (root)
- Save — the site will be published at `https://<YOUR_USERNAME>.github.io/<REPO_NAME>/`

Option B — Netlify (drag & drop or CLI)
1. Zip the `hero.html` (or place it in a folder with any assets).
2. Go to https://app.netlify.com/drop and drag-and-drop the folder or `hero.html`.
3. Netlify will publish a live URL automatically.

Option C — Vercel
1. Install the Vercel CLI or connect your GitHub repo in the Vercel dashboard.
2. Push the repo and import into Vercel — it will deploy automatically.

Image credit & accessibility notes
----------------------------
- The mobile menu has ARIA attributes (`aria-expanded`, `aria-controls`, `aria-hidden`) and focus management.

- Interactive elements have focus rings for keyboard users.

- The hero illustration uses an Unsplash photo: `https://images.unsplash.com/photo-1555949963-4f1e1f0c7d47` (credit: Unsplash). It includes descriptive alt text and `loading="lazy"`.

- To replace with a different free illustration resource, swap the `src` in `hero.html` — I can suggest a specific Undraw SVG if you prefer.

Next steps I can help with
-------------------------
- Replace placeholder image with actual Unsplash/Undraw asset.
- Create a minimal GitHub Actions workflow to auto-deploy to GitHub Pages.
- Push and publish the repo for you if you provide repository access or run the commands locally.

If you want, tell me which hosting option to use and I will provide the exact commands you should run (or a step-by-step interactive walk-through).