# chrismccarthydev.uk

Source for [chrismccarthydev.uk](https://chrismccarthydev.uk), built with [Jekyll](https://jekyllrb.com) and the
[Chirpy](https://github.com/cotes2020/jekyll-theme-chirpy) theme, deployed to GitHub Pages by
[`.github/workflows/pages-deploy.yml`](.github/workflows/pages-deploy.yml) on every push to `main`.

## Run locally

```shell
bundle install
bash tools/run.sh        # serves on http://127.0.0.1:4000 with live reload
bash tools/test.sh       # production build + htmlproofer link check
```

No Ruby? Open the repo in the included dev container (`.devcontainer/`).

## Writing a post

Add `_posts/YYYY-MM-DD-title.md`:

```markdown
---
title: My post
date: 2026-11-06 12:00:00 +0000
categories: [Engineering]
tags: [python]
---

Content here.
```

See the [Chirpy docs](https://github.com/cotes2020/jekyll-theme-chirpy/wiki) for more front-matter options.

## Theme overrides

- `_layouts/home.html` is a copy of Chirpy 7.6.0's home layout with one addition (marked `LOCAL`): the content of
  `index.html` is shown as an intro card above the post list. When upgrading Chirpy, re-copy the theme's
  `home.html` and re-apply that block.
