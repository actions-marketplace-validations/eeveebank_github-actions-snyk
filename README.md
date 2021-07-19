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
        uses: eeveebank/github-actions-snyk/iac@master
        env:
          SNYK_TOKEN: ${{ secrets.SNYK_PLATFORM_TERRAFORM_TOKEN }}
```
