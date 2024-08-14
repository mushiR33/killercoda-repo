
Setup WSO2 API Manager 4.3.0 in K8s cluster using Helm Charts.

- Create a new helm repository with the latest apim release using the following command. Let’s consider the `<repository-name>` as `wso2apim`.

`helm repo add wso2apim https://github.com/wso2/helm-apim/releases/download/cp-4.3.0`

- Execute the following command to update the helm repositories.

`helm repo update`

- Consider `apim` as the `<chart-name>` for this guide. As the --version of this command, use the version of the release you used in point 1 above. It will take a few minutes for the deployment to complete.

`helm install apim wso2apim/wso2am-cp --version 4.3.0 -f https://raw.githubusercontent.com/wso2/apk/main/helm-charts/samples/apim/cp/values.yaml -n apk`

- Install NGINX Ingress Controller. Please refer to the [NGINX Ingress Controller](https://kubernetes.github.io/ingress-nginx/deploy/#local-development-clusters) documentation for more information.
