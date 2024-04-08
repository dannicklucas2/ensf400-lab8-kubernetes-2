# ENSF 400 - Assignment 3 - Kubernetes
Dannick Lucas - UCID: 30143991

## Steps to Run the Apps

1. Copy .yaml files into directory. The .yaml files are:
- nginx-dep.yaml
- nginx-configmap.yaml
- nginx-svc.yaml
- nginx-ingress.yaml
- app-1-dep.yaml
- app-1-svc.yaml
- app-1-ingress.yaml
- app-2-dep.yaml
- app-2-svc.yaml
- app-2-ingress.yaml




2. Start Minikube:
```bash
minikube start
```
3. Enable Ingress addon:
```bash
minikube addons enable ingress
```
4. Deploy nginx and the apps by applying all yaml files (This step will apply all the deployement, service and ingress files for nginx, app-1 and app-2):
```bash
kubectl apply -f .
```

5. Interacting with the Apps: To test with curl, use the following command:

```bash
curl http://$(minikube ip)/
```
6. The terminal outputs of running the command a few times:

```bash
Hello World from [app-1-dep-86f67f4f87-lp2s9]!
Hello World from [app-1-dep-86f67f4f87-lp2s9]!
Hello World from [app-1-dep-86f67f4f87-lp2s9]!
Hello World from [app-1-dep-86f67f4f87-lp2s9]!
Hello World from [app-1-dep-86f67f4f87-lp2s9]!
Hello World from [app-2-dep-7f686c4d8d-fp9xd]!
Hello World from [app-2-dep-7f686c4d8d-fp9xd]!
Hello World from [app-2-dep-7f686c4d8d-fp9xd]!
Hello World from [app-1-dep-86f67f4f87-lp2s9]!
Hello World from [app-2-dep-7f686c4d8d-fp9xd]!
```

