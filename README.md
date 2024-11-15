P1-helm
Github pages are used to fetch Helm packages:
https://vexoftss.github.io/P1-helm/index.yaml
Example:
helm repo add vexoft https://vexoftss.github.io/P1-helm
helm repo update vexoft
helm upgrade --install <name> vexoft/<chart_name> --recreate-pods --values ./deploy/helm/values.yaml



https://keycloak.vexoft.com/realms/vexoft/.well-known/openid-configuration to show available endpoints
                                        ^
                                        realm

http://localhost:8081/realms/vexoft/account/ ==  account endpoint