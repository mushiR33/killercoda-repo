
- Create a new helm repository with the latest apim apk agent release using the following command. Let’s consider the `<repository-name>` as `wso2apkagent` for this guide.

`helm repo add wso2apkagent https://github.com/wso2/product-apim-tooling/releases/download/1.1.0`

- Execute the following command to update the helm repositories.

`helm repo update`

- Install the APIM APK Agent components and start WSO2 API Platform For Kubernetes. Consider `apk` as the `<chart-name>` for this guide. As the `--version` of this command, use the version of the release you used in point 1 above. It will take a few minutes for the deployment to complete.

`helm install apim-apk-agent wso2apkagent/apim-apk-agent --version 1.1.0 -f https://raw.githubusercontent.com/wso2/apk/main/helm-charts/samples/apim-apk-agent/values.yaml -n apk`

- Verify the deployment
Now you can verify the deployment by executing the following command. You will see the status of the pods.

`kubectl get pods -n apk`
