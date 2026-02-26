# nbck.me

Personal website. Static HTML hosted on GitHub Pages.

## Blog

To publish a new post:

1. Write a markdown file in `blog/`, e.g. `blog/my-post.md`
2. Add an entry to `blog/posts.json`:
   ```json
   {
     "slug": "my-post",
     "title": "My post title",
     "date": "2025-03-01"
   }
   ```
3. Push to master

Posts are rendered client-side with [marked.js](https://github.com/markedjs/marked). Keep newest posts first in `posts.json`.
