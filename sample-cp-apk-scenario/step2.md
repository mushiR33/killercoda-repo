There are 3 components which you need to setup to get the APK working with APIM. They are,
- Setup WSO2 API Manager Control Plane 4.3.0
- Setup WSO2 APK Dataplane 1.1.0
- Setup WSO2 APIM-APK Agent 1.1.0

- Add helm repo and update index

`helm repo add wso2apk https://github.com/wso2/apk/releases/download/1.1.0 && helm repo update`{{execute}}

- Install WSO2 APK using Helm

NOTE: You could customize the gateway runtime parameters using the values file, but for now let's use the default values.

`helm install apk wso2apk/apk-helm --version 1.1.0 -f values.yaml`{{execute}}

- Test the WSO2 APK. Wait for the system to be ready.

`kubectl get pods`{{execute}}
