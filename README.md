# Demo App

A simple Flask application deployed with Helm and ArgoCD.

## Quick Start

### Build and Push Docker Image
```bash
docker build -t vishnups26/demo-app:latest app/
docker push vishnups26/demo-app:latest
```

### Deploy with Helm
```bash
helm install demo-app helm/demo-app -n demo-app --create-namespace
```

### Test
```bash
kubectl port-forward svc/demo-app -n demo-app 5000:80
curl http://localhost:5000/
```
# demo-app
