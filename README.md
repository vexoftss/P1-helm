P1-helm
Github pages are used to fetch Helm packages:
https://vexoftss.github.io/P1-helm/index.yaml
Example:
helm repo add vexoft https://vexoftss.github.io/P1-helm
helm repo update vexoft
helm upgrade --install <name> vexoft/<chart_name> --recreate-pods --values ./deploy/helm/values.yaml
