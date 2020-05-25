# argocd-k3s

A kubectl YAML to deploy a ArgoCD on Kubernetes

## Post-Installation

You can tune the <env> Kustomize Overlay with :
- argocd-deployment.yaml : to match your storage driver (in my example ArgoCD is behind Traefik),
- argocd-ingressroute.yaml : to match your FQDN.

## Installation 

```bash
git clone https://github.com/kyzdev/argocd-k3s.git
cd argocd-k3s
kustomize overlays/<env> | kubectl apply -f -
```
## Uninstallation

```bash
kubectl delete namespace argocd
```