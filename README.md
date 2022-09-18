This is a Helm chart for installing Directus with Postgresql HA setup.

You can include extensions that you would like to add to your deployment. Check the `directusExtensions` parameter in `values.yaml`.

The PVC generated persists through `helm uninstall`. This means that you'll only lose your data if you explicitly delete the PVC or if you delete the namespace the installation is in.

# Requirements

You need to have a local kubernetes cluster setup or access to kubernetes cluster in order to install this helm chart.

# Installation

Install this chart either via:
```
helm repo add w3iw3i https://w3iw3i.github.io/directus-helm-chart/
helm install directus w3iw3i/directus
```

or from the project directory via:
```
helm package .
helm install directus ./directus-x.x.x.tgz
```