
- Create a new helm repository with the latest apk release using the following command. Let’s consider the `<repository-name>` as `wso2apk`.

`helm repo add wso2apk https://github.com/wso2/apk/releases/download/1.1.0`

- Execute the following command to update the helm repositories.

`helm repo update`

- Install the APK components and start WSO2 API Platform For Kubernetes. Consider `apk` as the `<chart-name>` for this guide. As the `--version` of this command, use the version of the release you used in point 1 above. It will take a few minutes for the deployment to complete.

`helm install apk wso2apk/apk-helm --version 1.1.0 -f https://raw.githubusercontent.com/wso2/apk/main/helm-charts/samples/apk/cp-enabled-values.yaml -n apk`
