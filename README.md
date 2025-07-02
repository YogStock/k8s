# Kubernetes Micro-serivce Infrastructure

Commande pour appliquer les configurations :
```bash
kubectl apply -k "https://github.com/YogStock/k8s/blob/main/configs/kustomization.yaml"
```

## Pour consulter les pods
Commande :
```bash
minikube tunnel
```
A ajouter dans le fichier hosts :
```
127.0.0.1   cyprien-siaud.local
127.0.0.1   keycloak.cyprien-siaud.local
127.0.0.1   s3.cyprien-siaud.local
127.0.0.1   broker.cyprien-siaud.local
127.0.0.1   db.cyprien-siaud.local
```

## Liste des composants
- 1 x Namespace
- 2 x Secrets
- 6 x ConfigMaps
- 20 x Services
  - 6 x LoadBalancer
  - 14 x ClusterIP
- 1 x Volume Persistant
- 14 x Deployments
- 3 x Jobs
- 2 x CronJobs
- 6 x HPA
- 1 x Ingress