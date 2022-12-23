# kustomize-services


## Apply Kustomized configurations

```shell
cd sealed-secrets
kustomize build --enable-helm overlays/base-install/ | kubectl apply -f -

cd contour
kustomize build overlays/base-install-contour | kubectl apply -f -

cd argocd
kustomize build overlays/base-install | kubectl apply -f -
```