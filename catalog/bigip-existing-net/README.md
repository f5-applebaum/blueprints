# bigip

## Description
Simple BIG-IP 1-NIC Instance in Existing Network

## Usage

### Fetch the package
`kpt pkg get REPO_URI[.git]/PKG_PATH[@VERSION] bigip`
Details: https://kpt.dev/reference/cli/pkg/get/

### View package content
`kpt pkg tree bigip-existing-network`
Details: https://kpt.dev/reference/cli/pkg/tree/

### Apply the package
```
kpt live init bbigip-existing-network
kpt live apply bigip-existing-network --reconcile-timeout=2m --output=table
```
Details: https://kpt.dev/reference/cli/live/
