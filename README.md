# Shared PR policy

The reusable workflow in `.github/workflows/policy.yml` publishes the
`hyperflow/pr-policy` commit status. A PR needs a non-empty description and a
Jira-style key in its title or description. Dependabot and `prod-promote[bot]`
are exempt from the ticket requirement.

## Jira validation

To check that the first referenced Jira issue exists and is not Done, configure
these GitHub Actions organization secrets for the target repositories:

- `JIRA_BASE_URL`: Jira site URL, e.g. `https://hyperflow-team.atlassian.net`
- `JIRA_USER`: Jira account email
- `JIRA_TOKEN`: Atlassian API token for that account

Use an account that can read the relevant Jira projects. Create the token in
[Atlassian account settings](https://id.atlassian.com/manage-profile/security/api-tokens)
and store it in [organization Actions secrets](https://github.com/organizations/hyperflowfinance/settings/secrets/actions).
Never commit or share the token.

Each repository must explicitly pass the secrets to the reusable workflow:

```yaml
jobs:
  pr-policy:
    uses: hyperflowfinance/.github/.github/workflows/policy.yml@main
    secrets:
      JIRA_BASE_URL: ${{ secrets.JIRA_BASE_URL }}
      JIRA_USER: ${{ secrets.JIRA_USER }}
      JIRA_TOKEN: ${{ secrets.JIRA_TOKEN }}
    permissions:
      contents: read
      pull-requests: read
      statuses: write
```

Only the three named secrets are forwarded. Ensure their visibility includes
the repository: private-only organization secrets do not reach public repos.
GitHub may also withhold Actions secrets for fork or Dependabot PRs.

If any secret is missing, the check warns and falls back to matching the key
pattern without contacting Jira. With all secrets available, an unsuccessful
Jira API response fails the check. If a bot PR includes a key, a failed lookup
can also fail that PR despite the ticket-requirement exemption.
