# youyuanwu.github.io

Source for my personal GitHub Pages site, built with [mdBook](https://rust-lang.github.io/mdBook/).

Go to [youyuanwu home](https://youyuanwu.github.io/).

## Layout

- `book.toml` — mdBook configuration.
- `docs/` — Markdown sources (`SUMMARY.md` is the table of contents).
- `book/` — Build output (gitignored).
- `.github/workflows/docs.yml` — Manual GitHub Pages deployment workflow.

## Local build

Install [mdBook](https://rust-lang.github.io/mdBook/guide/installation.html) and
the [mdbook-katex](https://github.com/lzanini/mdbook-katex) preprocessor, then:

```sh
mdbook build      # output to ./book
mdbook serve      # live preview at http://localhost:3000
```

## Deployment

Deployment runs via GitHub Actions:

- Automatically on push to `main` when `docs/**`, `book.toml`, or the workflow file changes.
- Manually from **Actions tab → Docs → Run workflow**.

One-time setup: in **Settings → Pages → Source**, select **GitHub Actions**.
