# Housework-items

Checklists for home setup, gardening, and bicycle maintenance — published
as a [Quarto book](https://quarto.org/docs/books/).

**Live site:** <https://bastienchassagnol.github.io/Housework-items/>

## Contents

1. **Gardening and planting** — containers, substrate, crops, tools
2. **Interior DIY and equipment** — room-by-room shopping lists
3. **Bicycle maintenance** — anatomy, brakes, gears, wheels, steering

## Local build

Requires [Quarto](https://quarto.org/docs/get-started/) ≥ 1.4.

```bash
quarto render
```

HTML and PDF output land in `_book/`.

## Publishing

Pushes to `main` trigger the GitHub Action in
`.github/workflows/publish.yml`, which renders the book and publishes to
the `gh-pages` branch ([Quarto GitHub Pages guide](https://quarto.org/docs/publishing/github-pages.html#github-action)).

Ensure **Settings → Actions → General → Workflow permissions** is set to
**Read and write**.

## Pipeline

```{mermaid}
%%| label: fig-readme-pipeline
%%| fig-cap: "Documentation pipeline."
flowchart LR
  A[Edit .qmd files] --> B[Push to main]
  B --> C[GitHub Action]
  C --> D[quarto render]
  D --> E[gh-pages branch]
  E --> F[GitHub Pages site]
```
