# Haoqi Yang Academic Homepage

This repository contains the source for a minimalist academic homepage built with [Hugo](https://gohugo.io/) and the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme.

## Local development

Run:

```bash
hugo server
```

The site will be available at `http://localhost:1313`.

## Build

Run:

```bash
hugo --minify
```

The generated site is written to `public/`.

## Deployment

Deployment is handled by GitHub Actions with the workflow in [.github/workflows/hugo.yml](/Users/yanghq/Documents/me/.github/workflows/hugo.yml).

For GitHub Pages deployment to work, the repository must have:

- GitHub Pages enabled
- Source set to `GitHub Actions`

## Main content

- Homepage profile and navigation are configured in [config.yml](/Users/yanghq/Documents/me/config.yml)
- Papers are driven by a single BibTeX source: [assets/data/papers.bib](/Users/yanghq/Documents/me/assets/data/papers.bib)
- The avatar image is stored at [assets/avatar.jpg](/Users/yanghq/Documents/me/assets/avatar.jpg)
