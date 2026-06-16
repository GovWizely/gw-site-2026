# GovWizely — Site

Static HTML site. Deploys automatically to GitHub Pages via GitHub Actions on every push to `main`.

## File structure

```
deploy/
  index.html                  # Homepage
  ai-ready-data.html          # Pillar I
  compliance-by-design.html   # Pillar II
  iterate-and-improve.html    # Pillar III
  favicon.svg
.github/
  workflows/
    deploy.yml                # GitHub Actions → GitHub Pages
```

## First-time setup

1. **Push this repo to GitHub.**

2. **Enable GitHub Pages:**
   - Go to your repo → Settings → Pages
   - Under *Source*, select **GitHub Actions**
   - Save

3. **Push to `main`** — the workflow runs automatically and your site is live at:
   `https://<your-username>.github.io/<your-repo-name>/`

## Editing the site

All editable source files are in the project root (not inside `deploy/`):

| Source file | Deploy file |
|---|---|
| `GovWizely.html` | `deploy/index.html` |
| `AI-Ready Data.html` | `deploy/ai-ready-data.html` |
| `Compliance by Design.html` | `deploy/compliance-by-design.html` |
| `Iterate and Improve.html` | `deploy/iterate-and-improve.html` |

After editing source files, re-run the deploy script or copy manually into `deploy/` — then push to `main`.

## Contact form

The contact form on the homepage is connected to [Formspree](https://formspree.io) (form ID: `xkoazayp`). Submissions go directly to your Formspree dashboard — no server needed.

## Custom domain (optional)

To use a custom domain (e.g. `govwizely.com`):

1. Add a `CNAME` file inside `deploy/` containing just your domain:
   ```
   govwizely.com
   ```
2. Point your DNS to GitHub Pages (see [GitHub docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)).
3. In repo Settings → Pages → Custom domain, enter your domain.
