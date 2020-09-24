- disable nginx ingress controller webhook validation

```bash
kubectl delete -A ValidatingWebhookConfiguration ingress-nginx-admission
```

- Start git server from host
```bash
git daemon --base-path=. --listen=0.0.0.0 --port=8088  --export-all --reuseaddr --informative-errors --verbose
```

- Setup remote from container
```bash
git remote add origin git://0.0.0.0:8088/infibeam/bennu-git2/
```

