# Portfolio

Personal portfolio website for Satyam Behera.

## Run locally

```bash
python3 -m http.server 4173
```

Then open: `http://127.0.0.1:4173`

## Branch protection (main)

To fully protect `main`, configure these GitHub settings:

1. Go to **Settings → Branches → Add branch protection rule** for `main`.
2. Enable **Require a pull request before merging**.
3. Enable **Require status checks to pass before merging** and select `Validate Portfolio / checks`.
4. Enable **Restrict who can push to matching branches** (or disable direct pushes for everyone).
5. Enable **Do not allow bypassing the above settings**.

Repository guardrails already added in code:
- `.github/workflows/validate-portfolio.yml` runs basic validation on PRs and fails direct pushes to `main`.
- `.github/CODEOWNERS` sets default ownership.
- `.github/pull_request_template.md` enforces consistent PR quality.
