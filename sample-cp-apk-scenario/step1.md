- Install Helm

    `curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3 && chmod 700 get_helm.sh && ./get_helm.sh`{{execute}}

- Create Kubernetes namespace
    `kubectl create ns apk`{{execute}}

- Configure the hosts file
Add a hostname mapping to the `/etc/hosts` file as follows.

```
127.0.0.1  api.am.wso2.com
127.0.0.1  am.wso2.com
127.0.0.1  idp.am.wso2.com
127.0.0.1  default.gw.wso2.com
```{{copy}}

- [OPTIONAL] Gateway API is a set of CRD (Custom Resource Definition). You could intall the Gateway API using the following command. This is part of the WSO2 APK Helm chart, so this is an optional step.

    `kubectl apply -f https://github.com/kubernetes-sigs/gateway-api/releases/download/v1.0.0/standard-install.yaml`{{execute}}

    Test it

    `kubectl get gateways`{{execute}}