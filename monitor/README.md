# Github Actions: Snyk/Monitor

Simplified Github action which adds a Github repo to a Snyk organisation.

# Example Workflow

```
name: Snyk Monitor
on: pull_request
jobs:
  snyk:
    runs-on: self-hosted
    steps:
      - uses: actions/checkout@v2
      - name: Snyk IaC Monitoring
        uses: eeveebank/github-actions-snyk/monitor@master
        with:
          org_id: ${{ secrets.SNYK_PLATFORM_TERRAFORM_ORG_ID }}
          repository_name: terraform-template
          snyk_token: ${{ secrets.SNYK_PLATFORM_TERRAFORM_TOKEN }}
```
