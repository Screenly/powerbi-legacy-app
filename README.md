[![Version](https://img.shields.io/github/v/release/Screenly/powerbi-legacy-app)](https://github.com/Screenly/powerbi-legacy-app/releases/latest)

# Power BI Edge App

A dashboard for displaying Power BI dashboards and reports with big focus on security. This Edge App was developed for a Fortune 500 client that with very strict security requirements.

For details, please see the [tutorial](https://www.screenly.io/tutorials/powerbi-legacy/).

## Releasing

Pushes to `main` deploy to stage automatically. To release to production, tag a commit on `main` and push the tag (the workflow refuses tags not on `main`):

```bash
git checkout main && git pull
git tag v26.10.0
git push origin v26.10.0
```

Then publish a GitHub Release whose notes list the pull requests merged since the previous release. Add `--draft` to review the notes before publishing:

```bash
gh release create v26.10.0 --verify-tag --generate-notes --title v26.10.0
```
