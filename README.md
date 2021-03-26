# Github Actions: Snyk

[![GitHub release (latest by date)](https://img.shields.io/github/v/release/eeveebank/github-actions-snyk)](https://github.com/eeveebank/github-actions-snyk/releases)

Simplified Github action using snyk.

# Example Workflow

```
name: Snyk Infrastructure as Code
on: push

jobs:
  snyk:
    runs-on: ubuntu-latest
    steps: 
      - uses: actions/checkout@v2
      - name: Run Snyk Scanning
        uses: eeveebank/github-actions-snyk@v1.0.0
        env:
          SNYK_TOKEN: ${{ secrets.PLATFORM_SNYK_TOKEN }}
      - uses: github/codeql-action/upload-sarif@v1
        with:
          sarif_file: snyk.sarif
```
