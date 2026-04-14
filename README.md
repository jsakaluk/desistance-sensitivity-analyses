# Desistance Quarto Site

This repository contains a Quarto website that is automatically published to GitHub Pages.

## Edit content

- Update `.qmd` source files (for example, `Index.qmd`) on the `main` branch.
- Commit and push your changes to GitHub.

## Preview locally

- Install Quarto: [https://quarto.org/docs/get-started/](https://quarto.org/docs/get-started/)
- Run:

```bash
quarto preview
```

## GitHub Pages deployment

- The workflow in `.github/workflows/publish.yml` runs on every push to `main`.
- It renders the site with `quarto render`.
- It deploys the rendered `docs/` folder to GitHub Pages using GitHub Actions.

## One-time GitHub setup

1. Create a new GitHub repository and push this folder to the `main` branch.
2. Open **Settings -> Pages** and set **Source** to **GitHub Actions**.
3. Open **Settings -> Actions -> General** and ensure workflow permissions allow deployments.
4. Confirm the workflow run in **Actions** succeeds after your first push.

## Site URL setting

Set `website.site-url` in `_quarto.yml` to your project site URL:

```yaml
website:
  site-url: "https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/"
```

If your GitHub username or repository name changes, update this value.
