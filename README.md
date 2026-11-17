# Portfolio site

Jekyll site for GitHub Pages. GitHub builds it on every push.

## First-time setup

1. On GitHub, create a public repo named `<your-username>.github.io`.
2. In this `site` folder:
   ```
   git init
   git add .
   git commit -m "Initial portfolio scaffold"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-username>.github.io.git
   git push -u origin main
   ```
3. On GitHub, open Settings > Pages and set the source to "Deploy from a branch", branch `main`, folder `/ (root)`.
4. Fill in `email`, `linkedin`, and `github` in `_config.yml`.

The site appears at `https://<your-username>.github.io/` a minute or two after each push.

## Adding an entry

Entries live in `_projects/<slug>.md`. Images and PDFs go in `assets/projects/<slug>/`. Keep `published: false` until the entry passes review, then set it to `true` and push.

## Preview locally (optional)

```
gem install jekyll kramdown-parser-gfm
jekyll serve
```
Then open http://localhost:4000. Unpublished entries can be previewed with `jekyll serve --unpublished`.
