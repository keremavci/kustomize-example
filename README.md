## Set Image & Create K8s Yaml
```
export IMAGE_VERSION=1.21.4
cd kustomize/overlays/preprod
kustomize edit set image nginx:$IMAGE_VERSION
cd -
kubectl apply -k kustomize/overlays/preprod --dry-run=client -o yaml
```