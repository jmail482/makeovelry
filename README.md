# makeovelry

Hugo + PaperMod portfolio site for Jonathan Nishikawa. Deployed via GitHub Pages with GitHub Actions auto-build.

Live: https://jmail482.github.io/makeovelry/

## Editing

Edit any `.md` file in `content/` and commit. GitHub Actions rebuilds on push.

PaperMod theme is cloned at build time (see `.github/workflows/hugo.yml`) - not a submodule.

## Local preview (optional)

1. Install Hugo Extended: https://gohugo.io/installation/
2. Clone PaperMod into `themes/PaperMod/`: `git clone --depth=1 https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod`
3. `hugo server -D`
4. Open http://localhost:1313/

## Adding a new post

Copy an existing post in `content/posts/`, rename, edit frontmatter (`title`, `date`, `tags`), write the body, commit, push.
