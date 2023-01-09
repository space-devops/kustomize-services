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

## Use kubeseal for secret storage

```shell
kubeseal --controller-name local-sealed-secrets --controller-namespace sealed-secrets < api-mountebank.yaml > ../mountebank-api/overlays/dev/sealed-secrets.yaml -o yaml
```