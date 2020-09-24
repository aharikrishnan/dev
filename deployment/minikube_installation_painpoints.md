- disable nginx ingress controller webhook validation

```bash
kubectl delete -A ValidatingWebhookConfiguration ingress-nginx-admission
```
