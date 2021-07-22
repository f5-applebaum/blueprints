# bigip

## Description
The package deploys a simple BIG-IP 1-NIC VM Instance in New Network

## Usage

### Fetch the package
`kpt pkg get REPO_URI[.git]/PKG_PATH[@VERSION] bigip-full-stack`
Details: https://kpt.dev/reference/cli/pkg/get/

### View package content
`kpt pkg tree bigip-full-stack`
Details: https://kpt.dev/reference/cli/pkg/tree/

### Apply the package
```
kpt live init bigip-full-stack
kpt live apply bigip-full-stack --reconcile-timeout=2m --output=table
```
Details: https://kpt.dev/reference/cli/live/
