# Bitnami Labs Sealed Secrets

## Kubeseal Usage

```shell
kubeseal --controller-namespace=sealed-secrets --controller-name=local-sealed-secrets < unsealed_secret.yaml > sealed_secret.yaml -o yaml
```