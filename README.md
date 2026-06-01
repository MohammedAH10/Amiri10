# Mohammed Ahmed Hassan — Portfolio & Blog

Static site deployed via GitHub Pages.

## Structure

```
portfolio-site/
├── index.html              # Home / portfolio
├── blog.html               # Blog listing
├── css/
│   └── style.css           # Shared design system (all pages)
├── js/
│   └── app.js              # Shared JS: starfield, nav, scroll reveal, blog filter
├── posts/
│   ├── building-rag-systems.html
│   ├── first-post.html
│   ├── building-mirai-q.html
│   └── mlops-notes.html
└── assets/
    └── images/
```

## Adding a new blog post

1. Copy any existing file in `posts/` as a starting point.
2. Update the `<title>`, `post-meta`, `<h1>`, and `post-summary` in the header.
3. Write content inside `<div class="post-body">`.
4. Update `post-footer` prev/next links.
5. Add a card for it in `blog.html` (copy an existing `.post-card` block and set the correct `data-category` and `href`).
6. Push to `main` — GitHub Actions deploys automatically.

## Available post categories (for `data-category` on cards and filter buttons)

- `mlops`
- `llm`
- `deeplearning`
- `engineering`

## Hero Signature

The hero uses a text signature in `index.html` styled with Dancing Script in `css/style.css`.

## Contact form

Replace `YOUR_FORM_ID` in `index.html` with your actual Formspree form ID.

## Deployment

The `.github/workflows/static.yml` workflow deploys the entire repo root on every push to `main`.
No build step required — everything is plain HTML, CSS, and JS.
