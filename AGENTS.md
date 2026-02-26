## Cursor Cloud specific instructions

This is a zero-dependency static personal website (HTML/CSS/vanilla JS) hosted on GitHub Pages at `nbckk9.github.io` (custom domain: `www.nbck.me`). There is no package manager, build system, linter, or test framework.

### Running the site locally

```
python3 -m http.server 8000
```

Then open `http://localhost:8000` in a browser.

### Project structure

- `index.html` — Homepage with hero, about, skills, experience, and contact sections
- `style.css` — Shared stylesheet (dark theme, cursor.com-inspired aesthetic)
- `profile.png` — Profile photo
- `blog/index.html` — Blog listing page (reads from `blog/posts/index.json`)
- `blog/post.html` — Blog post viewer (renders `.md` files with marked.js from CDN)
- `blog/posts/index.json` — Blog posts metadata (slug, title, description, date)
- `blog/posts/*.md` — Individual blog posts in Markdown
- `CNAME` — GitHub Pages custom domain config (`www.nbck.me`)

### Adding a blog post

1. Create a new `.md` file in `blog/posts/` (e.g. `my-new-post.md`)
2. Add an entry to `blog/posts/index.json` with slug, title, description, and date
3. The blog listing and post pages are client-side rendered — no build step needed

### Notes

- No lint, test, or build commands exist. Validation is done by serving files and checking in a browser.
- Blog posts use [marked.js](https://cdn.jsdelivr.net/npm/marked@15/marked.min.js) loaded from CDN for client-side Markdown rendering.
- Pushing to `main` deploys automatically via GitHub Pages.
