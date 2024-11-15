## Add Helm chart 
`helm repo add kubernetes-dashboard https://kubernetes.github.io/dashboard/`<br>
`helm repo update`

## Edit the values from [values.yaml](./values.yaml)
Edit the values. Check [_default_values.yaml](./_default_values.yaml) for default values.

## Install / Upgrade
`helm upgrade --install kubedashboard kubernetes-dashboard/kubernetes-dashboard --create-namespace --namespace kubedashboard -f values.yaml`

## Authentication and authorization
Keycloak OICD for client 'kubedashboard' is used.<br>
realm: vexoft<br>
See configurations from [here](../keycloak-client-exports/kubedashboard.json)

## Uninstall
`helm uninstall kubedashboard -n kubedashboard`