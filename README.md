# Github Actions: Gitleaks

[![GitHub release (latest by date)](https://img.shields.io/github/v/release/eeveebank/github-actions-gitleaks)](https://github.com/eeveebank/github-actions-gitleaks/releases)

Simplified Github action using Gitleaks.

# Example Workflow

```
name: Gitleaks
on: push

jobs:
  snyk:
    runs-on: ubuntu-latest
    steps: 
      - uses: actions/checkout@v2
      - name: Run Gitleaks
        uses: eeveebank/github-actions-gitleaks@v1.0.0
        with:
          depth: 1
      - uses: github/codeql-action/upload-sarif@v1
        with:
          sarif_file: gitleaks.sarif
```
