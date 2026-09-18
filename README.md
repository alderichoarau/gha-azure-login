# gha-azure-login

Composite action: federated (OIDC) sign-in to Azure. No client secret.

```yaml
- uses: alderichoarau/gha-azure-login@v1
  with:
    client-id: ${{ secrets.AZURE_CLIENT_ID }}
    tenant-id: ${{ secrets.AZURE_TENANT_ID }}
    subscription-id: ${{ secrets.AZURE_SUBSCRIPTION_ID }}
```

## Versioning

Tags are bare `vN`, immutable, never moved -- native Dependabot `github-actions` updates work.
Release a new version: run **"Tag a new version"** (manual dispatch) -- only after an actual
change to this repo's content. Running it again with nothing new since the last tag is refused
by the workflow (it would just create a duplicate tag pointing at the same commit).
