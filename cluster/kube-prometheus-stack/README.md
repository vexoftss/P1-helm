## Add prometheus-community Helm chart 
`helm repo add prometheus-community https://prometheus-community.github.io/helm-charts`<br>
`helm repo update`

## Edit the values from [values.yaml](./values.yaml)
Edit the values. Check [_default_values.yaml](./_default_values.yaml) for default values.

## Install kube-prometheus-stack
First, create the namespace<br>
`kubectl create ns kube-prometheus-stack`<br> 
`helm install kube-prometheus-stack prometheus-community/kube-prometheus-stack -n kube-prometheus-stack -f values.yaml`

## Upgrade kube-prometheus-stack
`helm upgrade --install kube-prometheus-stack prometheus-community/kube-prometheus-stack -n kube-prometheus-stack -f values.yaml`

## Authentication and authorization
Keycloak OICD for client 'grafana' is used.<br>
realm: vexoft<br>
See configurations from [here](../keycloak-client-exports/grafana.json)

## Uninstall
`helm uninstall kube-prometheus-stack -n kube-prometheus-stack`