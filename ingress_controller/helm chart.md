## get helm chart for ingress controller:

```
helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx
helm repo update

# pull helm chart to local

helm pull ingress-nginx/ingress-nginx --destination ./charts

tar -zxvf ./charts/ingress-nginx-<version>.tgz -C ./charts
tar -zxvf ingress-nginx-4.12.1.tgz  -C .
# ingress-nginx-4.12.1.tgz


# install helm for amazon ec2 instance
curl -fsSL https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3 | bash

# Go to the Helm GitHub releases page and find the ARM64 version
curl -fsSL -o helm.tar.gz https://get.helm.sh/helm-v3.11.0-linux-arm64.tar.gz

tar -zxvf helm.tar.gz

sudo mv linux-arm64/helm /usr/local/bin/helm

helm version


helm install nginx-ingress ingress-nginx/ingress-nginx -f values.yaml --namespace ingress-nginx --create-namespace


```