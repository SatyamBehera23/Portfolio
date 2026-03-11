# Portfolio

Personal portfolio website for Satyam Behera.

## Run locally

```bash
python3 -m http.server 4173
```

Then open: `http://127.0.0.1:4173`

## Deploy (GitHub Pages)

This repository now includes `.github/workflows/deploy-pages.yml` for automatic deployment.

### One-time GitHub setup

1. Go to **Settings → Pages**.
2. Under **Source**, select **GitHub Actions**.
3. Push/merge changes into `main`.
4. After the workflow runs, your site will be published from the workflow artifact.

## Branch protection (main)

To protect `main` properly, configure these GitHub settings:

1. Go to **Settings → Branches → Add branch protection rule** for `main`.
2. Enable **Require a pull request before merging**.
3. Enable **Require status checks to pass before merging** and select `Validate Portfolio / checks`.
4. Enable **Restrict who can push to matching branches** (or disable direct pushes for everyone).
5. Enable **Do not allow bypassing the above settings**.

## Repository guardrails included

- `.github/workflows/validate-portfolio.yml` runs basic validation on PRs and pushes.
- `.github/workflows/deploy-pages.yml` deploys the portfolio to GitHub Pages on `main`.
- `.github/CODEOWNERS` sets default ownership.
- `.github/pull_request_template.md` standardizes PR quality.
