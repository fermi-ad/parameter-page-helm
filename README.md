# Parameter Page Helm Chart

This chart bootstraps a Parameter Page deployment on a Kubernetes cluster using the Helm package manager.

## Install Parameter Page using Helm

1. Clone this repository
`git clone git@github.com:fermi-ad/parameter-page-helm.git`

2. Navigate to the Helm Chart directory
`cd parameter-page-chart`

3. Install Parameter Page Chart
```
helm dependency build
helm install parameter-page  .
```

## Verify the Installation

To check the installation you can execute the integration tests:

`helm test parameter-page`

## Upgrade Parameter page

`helm upgrade --install parameter-page .`

## Uninstall Parameter Page

`helm delete parameter-page`

To delete the PVC's associated with Parameter page:

`kubectl delete pvc -l release=parameter-page`

This will  delete postgresql data.
