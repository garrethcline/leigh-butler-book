# The Leigh Household Butler Book — Web Reader

A self-hosted EPUB reader for the Leigh Household butler book, designed for GitHub Pages.

## What's in this folder

```
.
├── index.html                  Landing page with "Begin Reading" button
├── reader.html                 The actual EPUB reader (epub.js powered)
├── Leigh_Butler_Book.epub      The book itself (~17 MB)
└── README.md                   This file
```

No build step. No npm. Just three files that work straight on GitHub Pages.

## Quick deploy to GitHub Pages

### Option A — Brand new repo for this book

1. Create a new repo on GitHub (e.g. `leigh-butler-book`). Public visibility.
2. Drag-and-drop all the files in this folder into the repo (or `git push` them to `main`).
3. In the repo, go to **Settings → Pages**.
4. Under **Source**, pick `Deploy from a branch`.
5. Branch: `main`, folder: `/ (root)`. Save.
6. Wait ~1 minute. Your book is live at:

```
https://YOUR-USERNAME.github.io/leigh-butler-book/
```

### Option B — Add to an existing GitHub Pages site

If you already have a `username.github.io` repo:

1. Create a subfolder like `/leigh/` in that repo.
2. Drop the four files into it.
3. Commit and push.
4. Access at `https://YOUR-USERNAME.github.io/leigh/`.

## Features

The reader includes:

- **Paginated layout** with prev/next arrows (or keyboard arrows / mobile swipe)
- **Table of contents sidebar** — every chapter and section linked
- **Adjustable font size** (70%–200%)
- **Light and dark themes** (toggle saved per device)
- **Reading position memory** (resumes where you left off)
- **Progress bar** at the bottom
- **Direct EPUB download** as a fallback

## Mobile

Works on iOS Safari and Android Chrome. Swipe left/right to turn pages.

## Custom domain (optional)

If you own a domain you'd like to use:

1. In the repo, add a file named `CNAME` containing your domain (e.g. `leigh.example.com`).
2. In your DNS, add a CNAME record pointing your domain to `YOUR-USERNAME.github.io`.
3. In **Settings → Pages**, set the custom domain and enable HTTPS.

## Updating the book

If you regenerate `Leigh_Butler_Book.epub`, just replace the file in the repo and push. The reader uses a fixed filename, so no other changes are needed. Readers' saved positions may reset if the chapter structure changed.

## How it works (briefly)

The reader is `reader.html` — a single static HTML file that loads `epub.js` from the jsDelivr CDN and `jszip` from cdnjs. When the page opens, it fetches `Leigh_Butler_Book.epub` from the same folder via an HTTP request, parses it client-side, and renders it. Reading position is stored in `localStorage` per browser.

Because everything runs in the browser, no server logic is needed — perfect for GitHub Pages.

## License & confidentiality

This is an academic project prepared for The International Butler Academy. Don't share publicly without permission from the Leigh household.

---

*Prepared by Mr. Cline, 2026.*
