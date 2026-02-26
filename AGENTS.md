## Cursor Cloud specific instructions

This is a zero-dependency static website (HTML/CSS/vanilla JS) hosted on GitHub Pages. There is no package manager, build system, linter, test framework, or backend.

### Running the site locally

```
python3 -m http.server 8000
```

Then open `http://localhost:8000` in a browser. All pages are self-contained HTML files with inline styles and scripts.

### Project structure

- `index.html` — Landing page / personal homepage
- `card/index.html` — Digital business card with profile photo
- `tennis-games/index.html` — Hub page linking to tennis mini-games
- `tennix-quiz/index.html` — Tennis trivia quiz (15 questions, all in JS)
- `tennis-crossword/index.html` — Tennis-themed crossword puzzle
- `CNAME` — GitHub Pages custom domain config (`www.nbck.me`)

### Notes

- No lint, test, or build commands exist. Validation is done by serving the files and checking them in a browser.
- The site is in French.
