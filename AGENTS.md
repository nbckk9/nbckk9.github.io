## Cursor Cloud specific instructions

This is a zero-dependency static website (HTML/CSS/vanilla JS) hosted on GitHub Pages. There is no package manager, build system, linter, test framework, or backend.

### Running the site locally

```
python3 -m http.server 8000
```

Then open `http://localhost:8000` in a browser. All pages are self-contained HTML files with inline styles and scripts.

### Project structure

- `index.html` — Personal homepage (JetBrains Mono theme, dark/light toggle, fr/en i18n)
- `blog/post.html` — Blog post reader (fetches markdown, renders with marked.js from CDN)
- `blog/posts.json` — Blog manifest (`[{slug, title, date}]`, newest first). Blog section auto-hides when empty.
- `blog/*.md` — Blog posts in markdown
- `CNAME` — GitHub Pages custom domain config (`www.nbck.me`)

### Blog publishing workflow

1. Write a `.md` file in `blog/`
2. Add an entry to `blog/posts.json`
3. `git push`

### Notes

- No lint, test, or build commands exist. Validation is done by serving the files and checking them in a browser.
- The site supports French and English, with browser language auto-detection. Language preference is saved to localStorage.
- Dark/light theme follows system preference by default, with manual toggle. Preference is saved to localStorage.
