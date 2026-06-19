# M07 CI/CD and GitOps

Учебный проект модуля 7 курса VK Cloud Junior+.

## Компоненты

- Nginx static web application
- Docker image
- Kubernetes Deployment
- Kubernetes NodePort Service
- GitHub Actions CI
- GitHub Container Registry
- Argo CD GitOps

## Local container test

```bash
docker build -t m07-web:v1 .
docker run -d --name m07-web-test -p 8087:80 m07-web:v1
curl http://127.0.0.1:8087
kubectl apply -f k8s/
kubectl get deployment,pods,service -l app=m07-web

```
