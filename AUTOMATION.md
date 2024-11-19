# Automation

There are some Organization-wide secrets available for GitHub Automation of various workflows.

## Personal Access Tokens

Automation currently depends on the availability of two GitHub Personal Access Tokens (PATs).

PATs have an expiry and the secret will have to be updated periodically by admins. An admin will create
a PAT on their account, requesting access to the organization. See [the docs](https://docs.github.com/en/organizations/managing-programmatic-access-to-your-organization/managing-requests-for-personal-access-tokens-in-your-organization).

### Release PAT

The release PAT requires permissions:
- Read access to actions variables, metadata, and secrets for all current and future repositories owned by this
  organization
- Read and Write access to code, issues, and pull requests for all current and future repositories owned by this
  organization

### Dependencies PAT

The dependencies PAT requires permissions:
- Read access to metadata for all current and future repositories owned by this organization
- Read and Write access to code and pull requests for all current and future repositories owned by your organization

# Actions secrets and variables

The Organization sets some Actions secrets so they are available to all repositories

| Name                 | Description                                                         | Example       |
|----------------------|---------------------------------------------------------------------|---------------|
| DEPENDENCY_TOKEN     | the [Dependencies PAT](#dependencies-pat)                           | secret :lock: |
| IMAGE_REPO_HOSTNAME  | the hostname of the container registry for streamshub public images | quay.io       |
| IMAGE_REPO_NAMESPACE | the namespace streamshub images are pushed to                       | streamshub    |
| IMAGE_REPO_USERNAME  | the username for the container registry                             | secret :lock: |
| IMAGE_REPO_PASSWORD  | the password corresponding to IMAGE_REPO_USERNAME                   | secret :lock: |
| RELEASE_TOKEN        | the [Release PAT](#release-pat)                                     | secret :lock: |
| SONAR_TOKEN          | a sonarcloud API token                                              | secret :lock: |


