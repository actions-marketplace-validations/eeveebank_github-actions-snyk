# Github Actions: Snyk/Monitor

Simplified Github action which scans IaC.

# Example Workflow

```
name: Snyk Infrastructure as Code
on: pull_request
jobs:
  snyk:
    runs-on: self-hosted
    steps:
      - uses: actions/checkout@v2
      - name: Run Snyk Scanning
        uses: eeveebank/github-actions-snyk/iac@master
        env:
          SNYK_TOKEN: ${{ secrets.SNYK_PLATFORM_TERRAFORM_TOKEN }}
```
