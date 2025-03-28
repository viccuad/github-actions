To test the updatecli `open-release-pr.yml` manifest locally,
you need to copy the updatecli folder into the policy that you are testing with,
or add the needed files in the root of this repository.

This is because the updatecli script is run via the reusable-release-pr workflow.

```console
export UPDATECLI_GITHUB_TOKEN=<your token>

UPDATECLI_GITHUB_OWNER=<your user> \
UPDATECLI_GITHUB_REPO=verify-image-signatures \
updatecli apply \
  --config updatecli/updatecli.d/open-release-pr.yml \
  --values updatecli/values.yml \
  --debug --clean=true
```
